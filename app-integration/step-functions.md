# AWS Step Functions

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS Step Functions is a serverless orchestration service that lets you coordinate multiple AWS services into workflows using visual state machines. It’s designed for building resilient, scalable application logic that can manage retries, timeouts, branching, and error handling with minimal custom code.

Each workflow is defined in Amazon States Language (ASL), a JSON-based DSL for expressing task flow and conditions.

---

## Why should I care?

Step Functions let you simplify complex application logic by breaking it into manageable steps:

- **Visual workflows** – Easy to understand, debug, and maintain.
- **Resilient and fault-tolerant** – Built-in error handling, retries, and timeouts.
- **Integrates natively with AWS services** – Direct integration with Lambda, DynamoDB, ECS, SQS, SageMaker, and more.
- **Reduces boilerplate code** – Move control logic from application code into declarative workflow definitions.

Step Functions are a common solution for orchestration in real-world systems and AWS certification scenarios.

---

## When to use it

Use Step Functions when:

- You need to coordinate multiple AWS services in sequence or in parallel.
- You want to implement retry logic and branching without writing code.
- You need to build **long-running workflows** that can pause and resume.
- You want visibility into workflow progress and state transitions.
- You need to simplify complex processes like ML pipelines, ETL jobs, or approval flows.

---

## Key features

- **Standard vs Express workflows**  
  - *Standard*: Durable and auditable, up to 1 year in duration.  
  - *Express*: High throughput, short duration, best for event processing.

- **State machines** – Define tasks, choices, waits, parallelism, and error handling.
- **Built-in service integrations** – Call over 200 AWS services without writing Lambda wrappers.
- **Visual editor** – View, design, and debug workflows visually in the AWS Console.
- **Audit trail** – Track every execution with detailed logging and tracing.

---

## Common use cases

- **ETL workflows** – Chain together data extraction, transformation, and loading steps.
- **Approval pipelines** – Wait for manual or automated approvals before continuing.
- **Error recovery** – Retry or route failed steps to fallback processes.
- **ML pipelines** – Manage data preparation, model training, and evaluation stages.
- **API composition** – Call multiple APIs in sequence and return a single result.

---

## Integrations

- **AWS Lambda** – Invoke functions as steps in a workflow.
- **Amazon SQS / SNS** – Queue or broadcast tasks between steps or services.
- **Amazon DynamoDB / S3 / ECS / Batch / Glue** – Orchestrate compute, storage, and analytics operations.
- **AWS SDK integrations** – Call supported AWS APIs directly with service integrations (no Lambda needed).
- **Amazon EventBridge** – Start Step Functions in response to events.

---

## Pricing

Pricing depends on the workflow type:

- **Standard workflows** – Pay per state transition (first 4,000 free each month).
- **Express workflows** – Pay per request and execution duration (better for high-throughput, short-lived jobs).

[Pricing details →](https://aws.amazon.com/step-functions/pricing/)

---

## Learn More

- [AWS Step Functions Developer Guide](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html)
- [Amazon States Language Specification](https://states-language.net/spec.html)
- [Step Functions Service Integrations](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-service-integrations.html)
- [Visual Workflow Examples](https://docs.aws.amazon.com/step-functions/latest/dg/tutorials.html)
