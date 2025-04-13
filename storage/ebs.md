# Amazon EBS (Elastic Block Store)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Amazon Elastic Block Store (EBS)** provides **block-level storage volumes** for use with Amazon EC2. EBS volumes behave like hard drives: they persist beyond instance termination, support snapshots, and can be resized or moved independently of the EC2 instance.

EBS is optimized for **low-latency, high-performance workloads**, including boot volumes, transactional databases, and custom file systems.

---

## Why should I care?

EBS is a key storage option when working with **EC2-based architectures**:

- **Durable** – Automatically replicated within the Availability Zone.
- **Flexible** – Choose volume types optimized for throughput, IOPS, or cost.
- **Persistent** – Volumes survive instance stops and can be reattached.
- **Snapshot support** – Back up volumes to Amazon S3 for DR and migration.
- **Encrypted and secure** – Native integration with AWS KMS and IAM.

Understanding EBS is crucial for AWS exams involving EC2, storage optimization, and disaster recovery.

---

## When to use it

Use Amazon EBS when:

- You need **persistent storage for EC2** (e.g., root, data, or database volumes).
- Your application requires **low-latency, random access to disk**.
- You want to take **point-in-time backups or snapshots**.
- You need a **resizable storage volume** without restarting the instance.
- You’re building a **lift-and-shift** architecture from on-prem to cloud.

---

## Key features

- **Volume types**:
  - `gp3`: General-purpose SSD (baseline performance + burst)
  - `io2/io2 Block Express`: Provisioned IOPS SSD for high-throughput apps
  - `st1`: Throughput-optimized HDD for big sequential workloads
  - `sc1`: Cold HDD for infrequently accessed data
- **Snapshots** – Incremental backups stored in S3, usable for restoration or cloning.
- **Encryption** – Use KMS-managed keys for at-rest encryption (default for new volumes).
- **Multi-attach (io1/io2 only)** – Attach a single volume to multiple EC2 instances (within the same AZ).
- **Elastic Volumes** – Resize or change type without downtime.

---

## Common use cases

- **Boot volumes** for EC2 instances.
- **Databases** (e.g., MySQL, PostgreSQL, MongoDB) requiring consistent low-latency disk.
- **Application data** that must persist and scale independently.
- **Analytics or log processing** requiring high-throughput SSD or HDD.
- **Disaster recovery** via snapshot replication and automation.

---

## Integrations

- **Amazon EC2** – Attach/detach volumes, auto-mount on boot.
- **AWS Backup / Data Lifecycle Manager (DLM)** – Automate snapshot creation and retention.
- **Amazon S3** – Store snapshots (managed transparently by AWS).
- **AWS KMS** – Encrypt volumes and snapshots with customer-managed keys.
- **AWS Lambda / CloudWatch / EventBridge** – Trigger automation based on snapshot or volume events.

---

## Pricing

You pay for:

- **Provisioned GB/month** for each volume (based on type)
- **Provisioned IOPS** (for `io1/io2`)
- **Snapshots** stored in S3 (incremental after first snapshot)
- **Data transfer** when copying snapshots across regions

[Pricing details →](https://aws.amazon.com/ebs/pricing/)

---

## Learn More

- [Amazon EBS Documentation](https://docs.aws.amazon.com/ebs/)
- [EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)
- [Using Snapshots](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)
- [Elastic Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-modifying-volume.html)
- [Performance Optimization](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-io-characteristics.html)
