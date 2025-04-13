# Amazon RDS (Relational Database Service)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon RDS (Relational Database Service) is a fully managed service for running relational databases in the cloud. It automates tasks like provisioning, patching, backups, and replication, allowing you to focus on your applications instead of database administration.

RDS supports multiple engines:
- **Amazon Aurora**
- **PostgreSQL**
- **MySQL**
- **MariaDB**
- **Oracle**
- **SQL Server**

---

## Why should I care?

RDS simplifies the operation of production-grade databases:

- **Automated management** – Handles backups, patching, monitoring, and failover.
- **High availability** – Multi-AZ deployments with automated failover.
- **Security** – Integration with IAM, KMS, and VPC for encryption and access control.
- **Scalability** – Vertical scaling (instance class) and horizontal read scaling via read replicas.
- **Cost-efficient** – Pay only for what you use, with options like Reserved Instances.

---

## When to use it

Use RDS when:

- You need a managed relational database for your application.
- You want to avoid database maintenance and focus on development.
- You need high availability, automated backups, and monitoring.
- You require compliance features like encryption at rest and in transit.
- You’re migrating an on-prem database to AWS with minimal changes.

---

## Key features

- **Multi-AZ deployments** – Automated failover and data replication.
- **Automated backups** – Daily snapshots and transaction logs for point-in-time recovery.
- **Read replicas** – Asynchronous replicas for scaling reads (not supported in all engines).
- **Encryption** – At rest (KMS) and in transit (SSL/TLS).
- **Monitoring** – Native integration with Amazon CloudWatch and Performance Insights.
- **Maintenance windows** – Define update periods for patches and upgrades.
- **Snapshots** – Manual snapshots for long-term backup or migration.

---

## Common use cases

- **Web app backends** – Store user data, sessions, orders, content, etc.
- **Internal tools** – Reporting, dashboards, or intranet applications.
- **Legacy migrations** – Move existing Oracle, SQL Server, or MySQL databases to AWS.
- **Multi-tier architectures** – Use with EC2, Lambda, or ECS-based application layers.
- **Analytics staging** – Prepare structured data before ETL to Redshift or S3.

---

## Integrations

- **Amazon EC2 / Lambda / ECS** – App-level access to your database.
- **Amazon CloudWatch** – Monitor performance, connections, and IOPS.
- **Amazon S3** – Import/export data via RDS integration or custom scripts.
- **AWS IAM** – Control database access (for some engines).
- **AWS Secrets Manager / SSM** – Securely store DB credentials.
- **AWS Database Migration Service (DMS)** – Migrate from on-prem or other cloud databases.

---

## Pricing

RDS pricing depends on:

- **Database engine**
- **Instance type and size**
- **Storage type (gp3, io1, magnetic) and provisioned IOPS**
- **Multi-AZ vs Single-AZ**
- **Backup and snapshot storage**
- **Data transfer out**

A free tier is available for 750 hours/month on db.t3.micro with 20 GB storage (MySQL, PostgreSQL, MariaDB only).

[Pricing details →](https://aws.amazon.com/rds/pricing/)

---

## Learn More

- [Amazon RDS Documentation](https://docs.aws.amazon.com/rds/index.html)
- [Multi-AZ Deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html)
- [RDS Feature Availability by Engine](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Engine_Overview.html)
- [Using Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html)
- [Backup and Restore](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html)
