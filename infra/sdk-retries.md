# AWS SDK Retry Behavior

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS SDKs implement automatic retry logic to handle transient failures when making requests to AWS services. This includes retries for network errors, throttling, and service-side issues. The retry behavior is configurable and varies across SDKs.

---

## Why should I care?

Understanding and configuring retry behavior is crucial for:

- **Resilience**: Ensures applications can recover from transient failures without manual intervention.
- **Performance**: Optimizes request handling, reducing unnecessary delays.
- **Cost Management**: Prevents excessive retries that could lead to increased costs.

---

## Retry Modes

AWS SDKs support different retry modes:

- **Standard**: Default mode with a maximum of 3 attempts (1 initial request + 2 retries).
- **Adaptive**: Includes client-side rate limiting and adjusts retry behavior based on observed throttling.
- **Legacy**: Older retry mode with behavior specific to each SDK.

You can configure the retry mode using environment variables, shared config files, or directly in code.

---

## Configuration Examples

### Java SDK v2

Set retry mode and maximum attempts via environment variables:

```bash
export AWS_RETRY_MODE=standard
export AWS_MAX_ATTEMPTS=5
```




Or configure in code:

```java
DynamoDbClient client = DynamoDbClient.builder()
    .overrideConfiguration(o -> o.retryPolicy(RetryMode.STANDARD))
    .build();
```




Customize maximum attempts:

```java
StandardRetryStrategy strategy = StandardRetryStrategy.builder()
    .maxAttempts(5)
    .build();

DynamoDbClient client = DynamoDbClient.builder()
    .overrideConfiguration(o -> o.retryStrategy(strategy))
    .build();
```



### JavaScript SDK v3

Configure retry strategy:

```javascript
import { DynamoDBClient } from "@aws-sdk/client-dynamodb";
import { StandardRetryStrategy } from "@aws-sdk/middleware-retry";

const client = new DynamoDBClient({
  maxAttempts: 5,
  retryStrategy: new StandardRetryStrategy(async () => 5),
});
```




Customize delay with a delay decider:

```javascript
const client = new DynamoDBClient({
  retryStrategy: new StandardRetryStrategy(async () => 5, {
    delayDecider: (delayBase, attempts) => Math.min(1000 * 2 ** attempts, 20000),
  }),
});
```



### Rust SDK

Set maximum attempts and backoff durations:

```rust
let retry_config = RetryConfig::standard()
    .with_max_attempts(5)
    .with_initial_backoff(Duration::from_millis(100))
    .with_max_backoff(Duration::from_secs(5));

let config = aws_config::from_env()
    .retry_config(retry_config)
    .load()
    .await;
```



---

## Considerations

- **Adaptive Retry Mode**: Suitable for applications where request rates need to adjust dynamically based on service responses.
- **Standard Retry Mode**: Recommended for most applications due to its balance between retry attempts and backoff strategy.
- **Legacy Retry Mode**: Maintained for backward compatibility; consider migrating to standard or adaptive modes.

---

## Learn More

- [Retry behavior in AWS SDKs and Tools](https://docs.aws.amazon.com/sdkref/latest/guide/feature-retry-behavior.html)
- [AWS SDK for Java Retry Strategies](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/retry-strategy.html)
- [AWS SDK for JavaScript v3 Retry Strategy](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/middleware-retry.html)
- [AWS SDK for Rust Retry Configuration](https://docs.aws.amazon.com/sdk-for-rust/latest/dg/retries.html)
