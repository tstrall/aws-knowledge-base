# AWS X-Ray

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**AWS X-Ray** is a distributed tracing service that helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture. It provides end-to-end view of requests as they travel through your application, and shows a map of your application’s underlying components. citeturn0search0

---

## Why should I care?

In complex, distributed systems, pinpointing the root cause of performance issues or errors can be challenging. AWS X-Ray provides:

- **End-to-end tracing** of requests across services.
- **Visual service maps** to identify bottlenecks and dependencies.
- **Detailed insights** into individual requests, including latency and error information.

This enables faster troubleshooting and performance optimization.

---

## When to use it

Use AWS X-Ray when:

- You need to trace requests across multiple AWS services.
- You're debugging latency issues in a microservices architecture.
- You require insights into the performance of your application components.
- You're monitoring applications running on AWS Lambda, Amazon EC2, Amazon ECS, or AWS Elastic Beanstalk.

---

## Key features

- **Trace collection**: Captures data about requests and responses, including metadata about AWS resources.
- **Service maps**: Visual representation of your application's components and their interactions.
- **Annotations and metadata**: Add custom data to traces for filtering and analysis.
- **Sampling**: Control the amount of data collected to balance cost and performance.
- **Integration with AWS services**: Works seamlessly with AWS Lambda, Amazon EC2, Amazon ECS, and more.

---

## Common use cases

- **Performance bottleneck identification**: Trace slow requests to their source.
- **Error analysis**: Understand where and why errors are occurring in your application.
- **Dependency visualization**: See how different parts of your application interact.
- **Monitoring AWS Lambda functions**: Gain insights into function performance and invocation patterns.

---

## Integrations

- **AWS Lambda**: Automatically captures trace data for Lambda functions.
- **Amazon EC2 and ECS**: Install the X-Ray daemon to collect trace data.
- **AWS SDKs**: Instrument your applications using AWS X-Ray SDKs for various programming languages.
- **AWS Distro for OpenTelemetry (ADOT)**: Use OpenTelemetry SDKs to send trace data to X-Ray.

---

## Example: Instrumenting a Python application

Install the AWS X-Ray SDK for Python:

```bash
pip install aws-xray-sdk
```



Instrument your application:

```python
from aws_xray_sdk.core import xray_recorder
from aws_xray_sdk.core import patch_all

patch_all()

@xray_recorder.capture('my_function')
def my_function():
    # Your code here
    pass
```



This setup enables X-Ray to trace requests and visualize the interactions within your application.

---

## Pricing

AWS X-Ray pricing is based on the number of traces recorded, retrieved, and scanned. As of the latest information:

- **Recorded traces**: $5.00 per million traces recorded.
- **Retrieved traces**: $0.50 per million traces retrieved.
- **Scanned traces**: $0.50 per million traces scanned.

Note: AWS offers a free tier that includes 100,000 traces recorded, 1,000,000 traces retrieved, and 1,000,000 traces scanned per month.

For the most up-to-date pricing, refer to the [AWS X-Ray Pricing](https://aws.amazon.com/xray/pricing/) page.

---

## Learn More

- [AWS X-Ray Developer Guide](https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html)
- [Getting Started with AWS X-Ray](https://docs.aws.amazon.com/xray/latest/devguide/xray-gettingstarted.html)
- [AWS X-Ray SDK for Python](https://github.com/aws/aws-xray-sdk-python)
