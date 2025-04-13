# Amazon S3 Glacier & Glacier Deep Archive

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Amazon S3 Glacier** and **S3 Glacier Deep Archive** are **low-cost, long-term archival storage classes** within Amazon S3. They are designed for data that is infrequently accessed but must be durably retained for compliance, backup, or archival purposes.

Glacier and Deep Archive offer a tradeoff: **very low storage costs** in exchange for **high retrieval latency** (minutes to hours).

---

## Why should I care?

Glacier classes are essential for **data lifecycle management and cost control**:

- **Extremely low cost** – Up to 90% cheaper than S3 Standard.
- **Durable and secure** – 99.999999999% durability with optional encryption.
- **Compliance-ready** – Ideal for WORM (write once, read many) storage.
- **Integrates with S3 lifecycle policies** – Automate transitions from hot to cold storage.

They're frequently tested in exam questions around storage lifecycle, compliance, and cost optimization.

---

## When to use it

Use S3 Glacier or Glacier Deep Archive when:

- You need to **retain data long-term** but rarely access it.
- You have **compliance or regulatory requirements** for archives.
- You're backing up logs, reports, raw datasets, or application snapshots.
- You want to reduce S3 costs by **automatically archiving infrequently used objects**.
- You can tolerate **retrieval delays** of minutes to hours.

---

## Key features

- **S3-native** – Archive data within the S3 console and API.
- **Retrieval tiers** (Glacier):
  - *Expedited* (1–5 minutes)
  - *Standard* (3–5 hours)
  - *Bulk* (5–12 hours)
- **Retrieval tiers** (Deep Archive):
  - *Standard* (12 hours)
  - *Bulk* (up to 48 hours)
- **Lifecycle transitions** – Move objects from S3 Standard → Glacier automatically.
- **Restore requests** – Temporarily make archived data accessible.
- **Vault lock** (for Glacier direct, not S3) – Enforce compliance retention rules.

---

## Common use cases

- **Compliance archiving** – Retain logs, health records, or audit data for 7+ years.
- **Backup storage** – Store snapshots or exports of RDS, DynamoDB, etc.
- **Digital preservation** – Media libraries, scientific research datasets, or legal documents.
- **Cold tier for big data** – Archive raw data that's been processed but must be saved.

---

## Integrations

- **Amazon S3** – Use S3 lifecycle policies to move data automatically to Glacier tiers.
- **AWS Backup / RDS / DynamoDB** – Archive backups to Glacier or Deep Archive.
- **AWS Athena / S3 Select** – Restore objects first; cannot query Glacier directly.
- **Amazon KMS** – Encrypt data at rest with customer-managed keys.
- **AWS Lake Formation** – Catalog long-term data as part of a data lake.

---

## Pricing

You pay for:

- **Storage (per GB/month)** – Extremely low rates compared to S3 Standard.
- **Retrieval requests** – Charged per GB and per request.
- **Early deletion fee** – If deleted within the minimum retention period (90 days for Glacier, 180 days for Deep Archive).

[Pricing details →](https://aws.amazon.com/s3/pricing/)

---

## Learn More

- [S3 Glacier Storage Class Overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-glacier.html)
- [Glacier Deep Archive](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-glacier-deep.html)
- [S3 Lifecycle Configuration](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-configuration-examples.html)
- [Restore Archived Objects](https://docs.aws.amazon.com/AmazonS3/latest/userguide/restoring-objects.html)
- [Glacier Direct Access (API Vaults)](https://docs.aws.amazon.com/amazonglacier/latest/dev/introduction.html)
