# Amazon EFS (Elastic File System)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Amazon Elastic File System (EFS)** is a **fully managed, scalable, POSIX-compliant file storage service** that allows multiple EC2 instances to share access to the same file system. It grows and shrinks automatically and supports thousands of concurrent connections, making it ideal for shared storage workloads.

---

## Why should I care?

EFS enables **shared, persistent storage** for Linux-based workloads:

- **Serverless and elastic** – Automatically scales with usage; no provisioning needed.
- **POSIX-compliant** – Supports standard file system semantics, permissions, and APIs.
- **Multi-AZ availability** – Can be accessed across multiple Availability Zones.
- **Use-case fit** – Ideal for lift-and-shift apps, CMS systems, dev environments, and more.
- **Mountable via NFS** – Easy integration with Linux servers and containers.

It’s commonly tested in scenarios where shared access, compatibility, or scaling is important.

---

## When to use it

Use Amazon EFS when:

- You need a **shared file system** accessible by multiple EC2 instances.
- You're migrating an application that expects a traditional file system.
- You want **auto-scaling storage** without provisioning.
- Your workload benefits from **read/write concurrency** (e.g., web farms, content repos).
- You want durable storage with **zero administration overhead**.

---

## Key features

- **Elastic storage** – Automatically grows and shrinks with your data.
- **Multiple performance modes**:
  - *General Purpose* (default, good for most apps)
  - *Max I/O* (for highly parallel workloads)
- **Throughput modes**:
  - *Bursting* (default; based on file system size)
  - *Provisioned* (fixed baseline throughput)
- **Standard vs One Zone**:
  - *Standard* = Multi-AZ (higher durability)
  - *One Zone* = Single AZ (lower cost)
- **Lifecycle management** – Move infrequently accessed files to IA (Infrequent Access) tier.
- **Encryption** – At rest (KMS) and in transit (TLS).
- **Access points** – Fine-grained user and path-level permissions.

---

## Common use cases

- **Web and application servers** – Shared content and assets.
- **Home directories** – User-specific storage in dev or remote environments.
- **Machine learning** – Shared access to large training datasets.
- **Media workflows** – Multiple workers accessing raw and processed assets.
- **CMS and monolithic apps** – Apps needing persistent shared state.

---

## Integrations

- **Amazon EC2** – Mount via NFSv4 for Linux instances.
- **Amazon ECS / EKS** – Share persistent storage across containerized workloads.
- **AWS Backup** – Protect EFS file systems with backup policies.
- **Amazon CloudWatch** – Monitor I/O operations, throughput, and storage.
- **AWS IAM / KMS** – Control access and encryption settings.

---

## Pricing

You pay for:

- **Storage (per GB/month)** – Based on usage in Standard or One Zone.
- **Infrequent Access tier (EFS-IA)** – Lower storage price + small access fee.
- **Provisioned throughput** – Optional fixed throughput charges (if selected).

[Pricing details →](https://aws.amazon.com/efs/pricing/)

---

## Learn More

- [Amazon EFS Documentation](https://docs.aws.amazon.com/efs/)
- [Mounting EFS on EC2](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html)
- [EFS Performance Modes](https://docs.aws.amazon.com/efs/latest/ug/performance.html)
- [EFS Access Points](https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html)
- [Storage Classes and Lifecycle Management](https://docs.aws.amazon.com/efs/latest/ug/lifecycle-management-efs.html)
