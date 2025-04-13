# AWS Lambda

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS Lambda is a serverless compute service that lets you run code in response to events — without provisioning or managing servers. You simply upload your code, configure a trigger, and Lambda handles the rest: scaling, fault tolerance, and billing based on execution time.

Lambda supports multiple runtimes (Node.js, Python, Java, Go, etc.) and can be invoked by over 200 AWS and external services.

---

## Why should I care?

Lambda is foundational to **serverless architecture** on AWS:

- **No infrastructure management** – AWS runs and scales your code automatically.
- **Event-driven** – Great for reacting to changes in S3, DynamoDB, SNS, API Gateway, etc.
- **Scalable** – Instantly handles from zero to thousands of requests per second.
- **Cost-effective** – Pay only for the compute time you consume (down to the millisecond).
- **Widely used** – Core component of modern, decoupled cloud architectures.

Understanding Lambda is essential for building efficient, scalable, and loosely coupled systems on AWS.

---

## When to use it

Use Lambda when:

- You want to run backend code without provisioning servers.
- You need to respond to events (e.g., S3 file uploads, SNS messages).
- You're building APIs or backend logic with Amazon API Gateway.
- You want to glue together AWS services with small bits of logic.
- You’re implementing automation or cron jobs using EventBridge rules.

---

## Key features

- **Fully managed** – No servers to manage or patch.
- **Scales automatically** – Instantly responds to traffic spikes.
- **Supports multiple runtimes** – Python, Node.js, Java, Go, .NET, custom runtimes.
- **Event sources** – Trigger from S3, API Gateway, DynamoDB, Kinesis, SQS, EventBridge, and more.
- **Environment variables** – Pass config and secrets securely.
- **Layers** – Share code (e.g., libraries, dependencies) across multiple functions.
- **Versions and aliases** – Support for CI/CD and traffic shifting.
- **VPC integration** – Securely access resources in private subnets.

---

## Common use cases

- **API backends** – Use with API Gateway to handle HTTP requests.
- **Data processing** – Transform files uploaded to S3 or events from DynamoDB/Kinesis.
- **Automation** – Trigger workflows or infrastructure updates.
- **Chatbots and webhooks** – Lightweight event handlers.
- **Scheduled jobs** – Run periodic tasks using EventBridge (formerly CloudWatch Events).

---

## Integrations

- **Amazon S3 / DynamoDB / Kinesis / SNS / SQS** – Built-in triggers.
- **Amazon API Gateway** – Use Lambda as a backend for REST or HTTP APIs.
- **AWS Step Functions** – Coordinate Lambda functions in a workflow.
- **AWS CloudFormation / SAM / CDK** – Define Lambda functions as infrastructure as code.
- **AWS IAM** – Grant functions permission to access other AWS resources.

---

## Pricing

Lambda pricing is based on:

- **Number of requests** (first 1M free per month)
- **Duration of execution** (billed in 1 ms increments)
- **Memory size allocated** (128 MB to 10 GB)
- **Optional features**: Provisioned concurrency, data transfer, etc.

[Pricing details →](https://aws.amazon.com/lambda/pricing/)

---

## Learn More

- [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [Supported Event Sources](https://docs.aws.amazon.com/lambda/latest/dg/lambda-services.html)
- [Lambda Limits and Quotas](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html)
- [Building with AWS SAM](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html)
