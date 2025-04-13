# Amazon ElastiCache

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon ElastiCache is a **fully managed in-memory data store and caching service** that supports two open-source engines: **Redis** and **Memcached**. It is designed to deliver ultra-fast performance by reducing load on your databases and applications through caching.

Use ElastiCache when you need **microsecond-level latency**, **high throughput**, and **real-time performance**.

---

## Why should I care?

ElastiCache helps you build **scalable, high-performance applications**:

- **Improves performance** – Reduces response times for frequently accessed data.
- **Reduces backend load** – Offloads repetitive queries from databases and APIs.
- **Fully managed** – AWS handles patching, failure recovery, backups, and scaling.
- **Supports real-time use cases** – Ideal for session stores, leaderboards, queues, and pub/sub systems.
- **Battle-tested tech** – Powered by Redis and Memcached, both widely adopted.

Caching is a key concept in AWS certification questions around performance optimization and cost reduction.

---

## When to use it

Use ElastiCache when:

- You need **sub-millisecond latency** for frequently accessed data.
- You want to **cache database queries** or REST API responses.
- You're implementing **real-time analytics**, session stores, or gaming leaderboards.
- You need **pub/sub messaging**, distributed locks, or rate limiting.
- You're replacing self-managed Redis or Memcached clusters with a managed solution.

---

## Key features

- **Redis and Memcached engines** – Choose based on feature set and use case.
- **In-memory speed** – Orders of magnitude faster than disk-based DBs.
- **Cluster mode for Redis** – Horizontal partitioning for scalability.
- **Replication and Multi-AZ** – High availability with automatic failover (Redis only).
- **Backup and restore** – Snapshot backups and point-in-time recovery (Redis only).
- **Encryption** – At rest and in transit using KMS and TLS.
- **Security** – VPC support, IAM integration, and Redis AUTH.

---

## Common use cases

- **Database caching** – Cache frequently queried data to reduce DB load.
- **Session storage** – Store short-lived user session data for web/mobile apps.
- **Leaderboards** – Real-time scoring systems using sorted sets in Redis.
- **Rate limiting** – Track request counts and throttle as needed.
- **Pub/Sub messaging** – Decouple microservices using Redis publish/subscribe.

---

## Redis vs Memcached

| Feature                | Redis                   | Memcached              |
|------------------------|--------------------------|--------------------------|
| Data structures        | Strings, lists, sets, etc. | Strings only            |
| Persistence            | Optional (RDB, AOF)      | No                      |
| Replication & failover | Yes                      | No                      |
| Pub/Sub                | Yes                      | No                      |
| Clustering             | Yes                      | No (sharding only)      |
| Use cases              | Complex caching, queues, leaderboards | Simple key-value caching |

---

## Integrations

- **Amazon RDS / DynamoDB / S3** – Cache results from slow or expensive queries.
- **Amazon EC2 / Lambda / ECS** – Used by apps and APIs to retrieve cached content.
- **AWS CloudWatch** – Monitor metrics like memory usage, evictions, and CPU.
- **Amazon VPC** – Launch ElastiCache clusters inside private subnets.
- **AWS IAM** – Control access using resource policies and tags.

---

## Pricing

Pricing is based on:

- **Node type (memory + CPU)**
- **Number of nodes and shards**
- **Backup storage (Redis)**
- **Data transfer out of the cluster**
- **Optional features** (e.g., Multi-AZ, enhanced metrics)

[Pricing details →](https://aws.amazon.com/elasticache/pricing/)

---

## Learn More

- [Amazon ElastiCache Overview](https://aws.amazon.com/elasticache/)
- [Choosing Redis vs Memcached](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/SelectEngine.html)
- [ElastiCache for Redis Best Practices](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/best-practices.html)
- [Redis Clustering Explained](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/Redis-Cluster.html)
- [Using Redis as a Pub/Sub System](https://redis.io/docs/interact/pubsub/)
