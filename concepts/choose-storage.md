# Choosing the Right AWS Storage & Database Option

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

AWS offers a **wide range of storage and database services**, each optimized for different use cases — from object storage to high-performance transactional databases.

Choosing the right storage or database option requires understanding tradeoffs around:

- **Latency**
- **Durability**
- **Cost**
- **Access patterns**
- **Structure vs flexibility**
- **Scalability**

---

## Why should I care?

Selecting the wrong service can lead to:

- **Higher costs**  
- **Poor performance**  
- **Complexity in development or scaling**  

Understanding when to use **S3 vs EBS**, or **RDS vs DynamoDB**, is a common topic in AWS certification exams and real-world architecture decisions.

---

## When to use what

### 🗃️ Object Storage

| Service | Use When | Notes |
|--------|----------|-------|
| **Amazon S3** | Storing large files, backups, logs, or static web assets | Durable, low-cost, eventual consistency |
| **S3 Glacier** / Deep Archive | Long-term archival, compliance backups | Cheapest option; high latency retrieval (minutes to hours) |

---

### 💽 Block Storage

| Service | Use When | Notes |
|--------|----------|-------|
| **Amazon EBS** | Persistent disk for EC2 instances | High IOPS, low latency; requires EC2 |
| **Instance Store** | Temp scratch space tied to EC2 lifecycle | Lost when instance stops or fails |

---

### 📁 File Storage

| Service | Use When | Notes |
|--------|----------|-------|
| **Amazon EFS** | Shared access from multiple Linux EC2s | Scales automatically; POSIX-compliant |
| **FSx** | Need Windows file system or Lustre performance | FSx for Windows = SMB; FSx for Lustre = high-speed compute apps |

---

### 🗄️ Relational Databases

| Service | Use When | Notes |
|--------|----------|-------|
| **Amazon RDS** | Traditional SQL workloads (OLTP) | Fully managed; supports PostgreSQL, MySQL, SQL Server, etc. |
| **Amazon Aurora** | Cloud-optimized SQL with MySQL/Postgres compatibility | Higher performance, HA, and scaling; multi-AZ + read replicas |

---

### ⚡ NoSQL / Key-Value / Document Stores

| Service | Use When | Notes |
|--------|----------|-------|
| **Amazon DynamoDB** | Low-latency, scalable NoSQL with flexible schema | Serverless, multi-region, millisecond latency |
| **Amazon ElastiCache** | Caching or real-time leaderboard/session data | In-memory; Redis or Memcached |

---

## Summary: Storage Comparison

| Service      | Type       | Durability | Access Speed | Cost | Use Case |
|--------------|------------|------------|---------------|------|----------|
| S3           | Object     | 99.999999999% | Moderate     | Low  | Files, backups, static sites |
| Glacier      | Archive    | 99.999999999% | Slow (min–hrs) | Very Low | Compliance storage |
| EBS          | Block      | 99.999%    | High          | Medium | Boot volumes, databases |
| EFS          | File       | 99.999999999% | High        | Medium | Shared Linux file systems |
| FSx          | File       | 99.999999% | High          | Medium | Windows/Linux HPC apps |

---

## Summary: Database Comparison

| Service      | Type     | Scale      | Schema | Best For |
|--------------|----------|------------|--------|----------|
| RDS          | Relational | Vertical + Read Replicas | Structured | Traditional apps |
| Aurora       | Relational | Horizontal Read Scale | Structured | High-performance SQL |
| DynamoDB     | NoSQL    | Fully Managed | Flexible | Serverless, web/mobile apps |
| ElastiCache  | In-memory| Fully Managed | Key-value | Caching, pub/sub |
| Neptune      | Graph DB | Managed     | Graph    | Connected data (social, fraud) |
| Timestream   | Time Series | Serverless | Time-indexed | Metrics, IoT, logs |

---

## Learn More

- [S3 vs EBS vs EFS](https://aws.amazon.com/blogs/storage/choosing-between-amazon-s3-amazon-ebs-and-amazon-efs/)
- [DynamoDB vs RDS](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SQLtoNoSQL.html)
- [AWS Storage Services Overview](https://aws.amazon.com/products/storage/)
- [Database Decision Guide](https://aws.amazon.com/nosql/)
