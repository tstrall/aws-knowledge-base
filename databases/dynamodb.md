# Amazon DynamoDB

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon DynamoDB is a fully managed **NoSQL database** service designed for high-performance applications that require **millisecond latency at any scale**. It supports key–value and document data models, and can handle massive workloads without provisioning infrastructure.

DynamoDB is serverless, automatically scales based on usage, and provides built-in **replication, backup, security, and caching** features.

---

## Why should I care?

DynamoDB is ideal for **low-latency, high-scale workloads**:

- **Fully serverless** – No infrastructure to manage.
- **Highly scalable** – Supports global applications and burst traffic.
- **Single-digit millisecond latency** – Consistent performance under heavy load.
- **Built-in durability and replication** – Across multiple AZs by default.
- **Event-driven ready** – Integrates with Lambda, Streams, EventBridge.

It’s commonly referenced in AWS certification scenarios around serverless design, microservices, and data modeling.

---

## When to use it

Use DynamoDB when:

- You need **consistent low-latency reads and writes** at any scale.
- Your data access patterns are well-defined (e.g., by partition key).
- You're building **serverless** or **event-driven** applications.
- You need **global replication** with low-latency access in multiple regions.
- You want **auto scaling** with little to no operations overhead.

---

## Key features

- **Key–value and document store** – Use a flexible schema for semi-structured data.
- **On-demand or provisioned capacity** – Choose auto-scaling or fixed throughput.
- **DAX (DynamoDB Accelerator)** – In-memory cache for microsecond response times.
- **Streams** – Capture item-level changes for event-driven applications.
- **Global tables** – Multi-region, active-active replication.
- **Time-to-live (TTL)** – Automatically expire stale items.
- **Backup and restore** – On-demand and continuous backups.
- **Encryption** – At rest (KMS) and in transit (TLS).
- **Fine-grained access control** – Integrates with IAM policies and condition keys.

---

## Common use cases

- **Gaming** – Real-time player data and session state.
- **IoT** – High-speed ingestion and lookup of telemetry data.
- **E-commerce** – Shopping cart, inventory, user profiles.
- **Mobile/web apps** – Serverless backends with dynamic content.
- **Event sourcing** – Paired with DynamoDB Streams and Lambda for audit trails.

---

## Integrations

- **AWS Lambda** – Trigger functions from DynamoDB Streams.
- **Amazon API Gateway** – Create REST APIs with DynamoDB as the backend.
- **Amazon Kinesis** – Ingest and analyze data alongside DynamoDB.
- **Amazon EventBridge** – Emit events via Streams for broader routing.
- **AWS DMS** – Migrate relational data to DynamoDB.
- **IAM / KMS / CloudWatch** – Secure, monitor, and analyze access and usage.

---

## Pricing

DynamoDB pricing depends on:

- **Capacity mode**:
  - *On-Demand* – Pay per read/write request.
  - *Provisioned* – Set read/write throughput (with optional auto-scaling).
- **Data storage**
- **Streams, backups, TTL deletes**
- **DAX (optional in-memory caching)**
- **Global Tables (multi-region replication)**

[Pricing details →](https://aws.amazon.com/dynamodb/pricing/)

---

## Learn More

- [DynamoDB Documentation](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)
- [Best Practices for DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html)
- [Working with DynamoDB Streams](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html)
- [Choosing Between On-Demand and Provisioned](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html)
- [Data Modeling for DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-modeling-nosql.html)
