# Database Review

## Relational Databases (RDBMS)

| DB         | Notes |
|------------|-------|
| PostgreSQL | Feature-rich, open-source, strong SQL compliance, supports JSONB |
| MySQL      | Widely used, fast reads, default for many LAMP stacks |
| Oracle     | Enterprise-grade, robust features, expensive licensing |
| SQL Server | Microsoft's RDBMS, well-integrated with .NET |
| SQLite     | Lightweight, serverless, good for mobile/dev/test |

**Features to Compare:**
- ACID compliance
- Joins, constraints, stored procedures
- Index types (B-Tree, GIN, Hash, etc.)
- Partitioning, replication, sharding

---

## NoSQL Databases

| DB        | Type         | Notes |
|-----------|--------------|-------|
| MongoDB   | Document     | JSON-like documents, flexible schema |
| Cassandra | Wide-column  | High availability, write-optimized, tunable consistency |
| Redis     | Key-value    | In-memory, great for caching and fast lookups |
| DynamoDB  | Key-value / Doc | AWS-managed, scalable, low-latency |
| Couchbase | Document     | High-throughput and mobile sync support |
| HBase     | Wide-column  | Built on HDFS, used in Hadoop ecosystems |

**NoSQL Considerations:**
- Schema flexibility
- CAP theorem tradeoffs (Consistency, Availability, Partition tolerance)
- Secondary indexes, TTL support
- Query expressiveness

---

## PostgreSQL vs Aurora PostgreSQL vs Redshift

| Feature                      | PostgreSQL                         | Aurora PostgreSQL                            | Amazon Redshift                              |
|-----------------------------|-------------------------------------|-----------------------------------------------|----------------------------------------------|
| Type                        | RDBMS                              | RDBMS (PostgreSQL-compatible)                | OLAP (Columnar Data Warehouse)               |
| Use Case                    | General purpose transactional DB   | Scalable PostgreSQL on AWS                   | Analytics, large-scale reporting             |
| Storage                     | Single-node or managed (RDS)       | Distributed, auto-replicated                 | Columnar storage, compressed, distributed    |
| Performance                 | Strong but single-node limited     | Faster failover, parallel query engine       | Optimized for large analytical queries       |
| High Availability           | Manual or with RDS Multi-AZ        | Built-in (multi-AZ, auto-healing)            | Clusters with node replication               |
| Cost Model                  | Instance-based                     | Instance-based (better scaling)              | Per-node, separate storage/compute (RA3)     |
| Compatibility               | Full PostgreSQL                    | Mostly compatible (some features lag behind) | Redshift SQL (PostgreSQL-like, not full)     |
| Backup & Restore            | Manual or RDS snapshots            | Continuous backup to S3                      | Snapshots and restore from S3                |

**Summary:**
- Use **PostgreSQL** if you want control, open-source, or are self-hosting
- Use **Aurora PostgreSQL** for managed, resilient, scalable PostgreSQL in AWS
- Use **Redshift** when you need high-performance analytics over very large datasets

---

## When to Use What

| Use Case                          | Preferred DB Type |
|----------------------------------|-------------------|
| Complex queries, joins, reporting| RDBMS             |
| High write throughput, HA        | Wide-column (Cassandra, HBase) |
| Flexible schema, nested objects  | Document (MongoDB, DynamoDB) |
| Caching or pub/sub               | Key-value (Redis) |
| Mobile or embedded use           | SQLite, Couchbase |
