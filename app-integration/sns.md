Here’s a Markdown page for **Amazon SNS (Simple Notification Service)** that follows the same style and structure you used for [`s3.md`](https://github.com/tstrall/aws-knowledge-base/blob/main/storage/s3.md) and your updated `sqs.md`:

---

# Amazon SNS (Simple Notification Service)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon Simple Notification Service (SNS) is a fully managed pub/sub (publish-subscribe) messaging service that enables systems to send messages to multiple subscribers in real time. It decouples message producers from consumers, allowing for scalable and fan-out architectures.

SNS supports multiple subscriber types, including:

- **Email**
- **SMS**
- **HTTP/S endpoints**
- **AWS Lambda**
- **Amazon SQS**

This makes SNS ideal for event-driven systems, alerting mechanisms, and loosely coupled microservices.

---

## Why should I care?

SNS is foundational for building responsive, decoupled applications:

- **Enables real-time notifications** across services and platforms.
- **Supports high fan-out** — one message can be delivered to many subscribers instantly.
- **Simplifies architecture** by decoupling producers and consumers.
- **Integrates with other AWS services** like Lambda, SQS, CloudWatch, and EventBridge.

SNS is frequently referenced in certification scenarios involving messaging, alerting, or loosely coupled service design.

---

## When to use it

Use SNS when:

- You need to broadcast messages to multiple endpoints or systems.
- You want to notify users via email or SMS.
- You’re integrating systems using an event-based architecture.
- You need to trigger workflows in response to events.
- You want to decouple services to improve scalability and fault tolerance.

---

## Key features

- **Multiple protocols** – Supports HTTP/S, email, SMS, Lambda, SQS, and mobile push notifications.
- **Message fan-out** – One-to-many message delivery to subscribed endpoints.
- **Message filtering** – Use message attributes to control which subscribers receive which messages.
- **Durability** – Messages are stored across multiple AZs during delivery attempts.
- **Security** – Fine-grained access via IAM and encryption using AWS KMS.

---

## Common use cases

- **Application alerts and monitoring** – Send notifications for CloudWatch alarms, health checks, or operational issues.
- **Order or signup confirmations** – Notify users via email or SMS when actions are taken.
- **System integration** – Trigger Lambda functions or push messages to SQS queues for backend processing.
- **Fan-out messaging** – Broadcast events to multiple systems or services.

---

## Integrations

- **Amazon SQS** – Fan out messages from SNS to multiple queues.
- **AWS Lambda** – Trigger code execution in response to published events.
- **CloudWatch Alarms** – Send alert notifications when thresholds are breached.
- **AWS EventBridge** – Used alongside SNS for advanced event routing and analytics.

---

## Pricing

Amazon SNS offers a free tier that includes 1 million publish requests and 100,000 HTTP/S deliveries per month. Additional charges apply based on the number of messages, delivery protocols used (e.g., SMS is more expensive), and data transfer.

[Pricing details →](https://aws.amazon.com/sns/pricing/)

---

## Learn More

- [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/welcome.html)
- [Amazon SNS API Reference](https://docs.aws.amazon.com/sns/latest/api/Welcome.html)
- [AWS SNS + Lambda Tutorial](https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html)
- [Using SNS with CloudWatch Alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)
