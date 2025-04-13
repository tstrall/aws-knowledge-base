# Amazon Aurora

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon Aurora is a **fully managed, high-performance relational database engine** built for the cloud. It is compatible with both **MySQL** and **PostgreSQL**, but delivers up to **5x the throughput of MySQL** and **3x that of PostgreSQL**, with the same code and tools.

Aurora is part of the Amazon RDS family, but it uses a distributed, fault-tolerant storage engine designed to support massive read/write throughput, fast failover, and automated replication.

---

## Why should I care?

Aurora is a best-of-both-worlds database for many workloads:

- **Performance + Compatibility** – Faster than standard MySQL/PostgreSQL but uses the same drivers, queries, and tools.
- **High availability** – Storage spans 3 AZs, with optional Multi-AZ failover and global clusters.
- **Cost-efficient scalability** – Supports up to 15 low-latency read replicas.
- **Resilience** – Auto-healing, fault-tolerant, and continuously backed up to S3.
- **Security & compliance** – Supports encryption, IAM auth, VPC, and auditing.

It’s often featured in AWS certification scenarios involving scalable, resilient databases.

---

## When to use it

Use Aurora when:

- You need a **drop-in replacement** for MySQL or PostgreSQL with better performance.
- You want **high availability** and **fast failover** without managing replication.
- You need **multi-region read scaling** or global distribution.
- You're running **SaaS, e-commerce, analytics, or financial** workloads.
- You want fully managed backups, patching, and monitoring out of the box.

---

## Key features

- **MySQL and PostgreSQL compatibility**
- **Aurora Storage Engine** – Distributed, self-healing, and auto-scaling (up to 128 TB).
- **Aurora Replicas** – Up to 15 read replicas per cluster with <100 ms lag.
- **Global Databases** – Read from other regions with low-latency replication.
- **Backtrack** – Rewind your database without restoring from a snapshot.
- **Serverless (v2)** – Automatically scales based on load (supports instant scaling).
- **Multi-AZ and failover** – Primary and standby DBs across Availability Zones.

---

## Common use cases

- **SaaS applications** – Multitenant or high-throughput relational workloads.
- **Read-heavy apps** – Scale with many read replicas and fast reader failover.
- **Disaster recovery** – Use global clusters for region-level HA.
- **Serverless apps** – Scale Aurora Serverless with unpredictable workloads.
- **Lift-and-improve** – Migrate from self-hosted MySQL/PostgreSQL and gain performance/reliability.

---

## Integrations

- **Amazon RDS** – Managed via the same console, API, and CLI.
- **Amazon Lambda / EC2 / ECS** – Common application consumers of Aurora.
- **Amazon S3** – Export/import data (e.g., data lake pipelines).
- **AWS DMS** – Migrate data to/from Aurora clusters.
- **AWS IAM / Secrets Manager** – Secure and manage access credentials.
- **CloudWatch & Performance Insights** – Monitor query performance and system metrics.

---

## Pricing

Aurora is priced based on:

- **Instance size and uptime** (vCPU + memory)
- **Aurora I/O requests** (read/write to storage)
- **Storage usage** (auto-scales up to 128 TB)
- **Backup storage** (beyond your retention period)
- **Optional features** like Global Databases or Serverless v2

[Pricing details →](https://aws.amazon.com/rds/aurora/pricing/)

---

## Learn More

- [Amazon Aurora Overview](https://aws.amazon.com/rds/aurora/)
- [Aurora MySQL vs Aurora PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)
- [Aurora Serverless v2](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html)
- [Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html)
- [Backtrack Feature](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-backtrack.html)
