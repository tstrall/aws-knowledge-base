# Amazon EventBridge

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon EventBridge is a serverless event bus service that makes it easy to connect applications using data from your own applications, AWS services, and integrated SaaS providers. It helps build event-driven architectures where components respond automatically to state changes or events, without tight coupling.

EventBridge evolved from **Amazon CloudWatch Events**, and offers more features, such as schema discovery, cross-account delivery, and event archiving.

---

## Why should I care?

EventBridge is central to building **modern, loosely coupled systems**:

- **Decouples producers and consumers** — services don't need to know about each other.
- **Enables real-time automation** based on changes in AWS or custom applications.
- **Simplifies workflows** by routing events to AWS services like Lambda, SQS, Step Functions, etc.
- **Increases agility** — easily add new consumers without touching producers.

It frequently shows up in certification scenarios involving event-driven design or automation between AWS services.

---

## When to use it

Use EventBridge when:

- You want to trigger workflows based on AWS service events (e.g., EC2 state change, S3 object upload).
- You need to ingest events from SaaS providers (e.g., Zendesk, Datadog).
- You’re building loosely coupled microservices using events.
- You need to route events conditionally based on pattern matching.
- You want to enable cross-account or cross-region event flows.

---

## Key features

- **Event buses** – Each account has a default bus; you can create custom buses or use partner/SaaS event sources.
- **Event routing** – Route events based on rules that match event patterns.
- **Schema registry** – Automatically discover event structure and generate code bindings.
- **Event archiving and replay** – Archive events and replay them for testing or recovery.
- **Cross-account delivery** – Send events to other AWS accounts securely.

---

## Common use cases

- **Triggering automation** – Auto-remediate security findings or deploy infrastructure changes.
- **Microservice orchestration** – Coordinate independent services using custom application events.
- **SaaS integration** – React to events from tools like Auth0, Segment, or PagerDuty.
- **Audit and compliance** – Archive and replay events for traceability and debugging.
- **Custom workflows** – Route domain-specific events to different consumers (e.g., Lambda, Step Functions).

---

## Integrations

- **AWS Lambda** – Trigger serverless functions for event handling.
- **Amazon SQS & SNS** – Forward events to queues or topic-based notification systems.
- **Step Functions** – Start state machines in response to events.
- **CloudWatch Logs / Insights** – Monitor and query event flow.
- **SaaS Platforms** – Use EventBridge SaaS integration for supported vendors.

---

## Pricing

EventBridge pricing is based on:

- Number of **events published**
- Number of **rules matched**
- Optional **schema discovery** and **event archiving**

A free tier is available (e.g., 100,000 events per month). Pricing is affordable for typical automation workflows, but can scale up with high-volume event ingestion.

[Pricing details →](https://aws.amazon.com/eventbridge/pricing/)

---

## Learn More

- [Amazon EventBridge Developer Guide](https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html)
- [Event Patterns and Rules](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html)
- [Schema Registry and Discovery](https://docs.aws.amazon.com/eventbridge/latest/userguide/discovering-schemas.html)
- [EventBridge vs SNS vs SQS](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-saas.html#eb-saas-comparison)
