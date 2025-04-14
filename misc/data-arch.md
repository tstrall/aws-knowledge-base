# Data Architecture Patterns

**What it is:**
- Data architecture defines how data is collected, stored, processed, and accessed across systems
- Good architecture balances performance, reliability, and scalability for both batch and real-time workloads

---

## Common Architecture Models

| Pattern         | Description |
|-----------------|-------------|
| **Batch Pipeline**   | Scheduled jobs (e.g. nightly) to extract, transform, and load data |
| **Streaming Pipeline** | Continuous ingestion and processing via Kafka, Flink, Spark Streaming |
| **Lambda Architecture** | Combines batch (accurate) + speed (real-time) layers |
| **Kappa Architecture** | Streaming-only pipeline, using compacted/replayable log (e.g. Kafka) |
| **Lakehouse**         | Merges data lake flexibility with data warehouse consistency (e.g. Delta, Iceberg) |

---

## Ingestion Patterns

| Type         | Description |
|--------------|-------------|
| **Batch Load**     | Scheduled file-based loads (e.g., CSV to S3 or RDBMS) |
| **CDC (Change Data Capture)** | Incremental updates from upstream databases (Debezium, DMS) |
| **Event Stream**   | High-throughput pub/sub systems (Kafka, Pulsar) |
| **Manual Upload**  | Ad-hoc sources for backfills, vendor drops |

---

## Storage Layers

| Layer          | Description |
|----------------|-------------|
| **Raw**        | Untransformed, immutable ingestion (S3, GCS, HDFS) |
| **Staging**    | Cleaned and normalized (but not yet modeled) |
| **Curated / Gold** | Ready for analytics and modeling (joins, business logic) |

---

## Data Access Patterns

- **OLTP**: Transactional workloads (e.g., PostgreSQL, Aurora)
- **OLAP**: Analytical workloads (e.g., Redshift, Snowflake, BigQuery)
- **Data Lakes**: Schema-on-read, flexible ingestion
- **Data Warehouses**: Schema-on-write, optimized for SQL analytics
- **Federated Queries**: Span across multiple sources

---

## Data Modeling Approaches

- **Star Schema / Snowflake Schema**: Dimensional modeling for BI
- **3NF (Third Normal Form)**: OLTP transactional modeling
- **Entity-Attribute-Value (EAV)**: Flexible schema for sparse data
- **Wide Tables**: For analytics when denormalization is needed
- **Lakehouse Delta Tables**: With schema enforcement and versioning

---

## Interview Tips
- Be able to diagram a data pipeline with raw → bronze → silver → gold layers
- Know tradeoffs between batch and streaming systems
- Explain when to use normalization vs denormalization
- Mention how you manage schema evolution and support backfills
