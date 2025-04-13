# DLQs & Retry Strategies

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Dead Letter Queues (DLQs)** are used to capture messages or events that **could not be successfully processed** after multiple attempts.  
**Retry strategies** define how AWS services attempt to reprocess failed invocations.

DLQs help isolate and debug failures in **asynchronous systems**, especially with services like **Lambda**, **SQS**, **SNS**, and **EventBridge**.

---

## Why should I care?

Without DLQs, failed messages may silently disappear or get retried endlessly. DLQs enable:

- **Debugging and alerting** – Capture failed events for inspection.
- **Operational visibility** – Know when and why retries fail.
- **Resilience** – Prevent failed events from blocking queues or Lambda functions.
- **Controlled retries** – Balance throughput and reliability.

Understanding retry and failure-handling behavior is essential for **event-driven and serverless architectures**.

---

## When to use it

Use DLQs and custom retry logic when:

- You need to **preserve failed messages** for later analysis or reprocessing.
- You want to avoid **silent data loss** in Lambda, SQS, or SNS workflows.
- You’re building systems that must **never drop events** (e.g., audit logs, billing, alerts).
- You want to **automate alerts** when failure patterns emerge.

---

## Key features

- **DLQ destinations**: Typically an **SQS queue** or an **SNS topic**.
- **Integration points**:
  - Lambda → DLQ if invocation fails after all retries
  - SNS → DLQ if delivery to subscribers fails
  - SQS → DLQ after maximum receives (`maxReceiveCount`)
  - EventBridge → custom retry rules or dead-letter config
- **Configurable retry behavior**:
  - *Retry count*
  - *Backoff strategy* (linear, exponential)
  - *Timeout windows*

---

## Common use cases

- **Lambda function errors** – Capture failed invocations for offline reprocessing.
- **Order processing** – Retain failed transactions for human intervention.
- **IoT pipelines** – Keep data from devices even when downstream is temporarily broken.
- **Compliance systems** – Ensure no event is lost, even if processing fails.

---

## Integrations

- **Amazon Lambda** – Configure a DLQ and visibility timeout for async errors.
- **Amazon SQS** – Automatically reroutes messages to a DLQ after `maxReceiveCount`.
- **Amazon SNS** – Sends failed messages to a DLQ if subscribers fail or reject.
- **Amazon EventBridge** – DLQs catch failed rule targets.
- **CloudWatch Logs / Metrics** – Monitor retry attempts and failures.

---

## Example: Lambda DLQ config (CloudFormation)

```yaml
MyFunction:
  Type: AWS::Lambda::Function
  Properties:
    ...
    DeadLetterConfig:
      TargetArn: arn:aws:sqs:us-east-1:123456789012:my-dlq
```

---

## Pricing

You pay only for the **underlying services** (e.g., SQS, SNS, Lambda) used in your retry and DLQ setup. There is no separate charge for using a DLQ.

[Pricing – SQS](https://aws.amazon.com/sqs/pricing/)  
[Pricing – Lambda](https://aws.amazon.com/lambda/pricing/)

---

## Learn More

- [AWS DLQ Overview](https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html#invocation-dlq)
- [Configuring SQS DLQs](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html)
- [SNS DLQ Configuration](https://docs.aws.amazon.com/sns/latest/dg/sns-dead-letter-queues.html)
- [Retry Behavior Across Services](https://docs.aws.amazon.com/lambda/latest/dg/invocation-retries.html)
