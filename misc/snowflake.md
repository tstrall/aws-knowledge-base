# Snowflake

**What it is:**
- A fully-managed, cloud-native data warehouse built for analytics at scale
- Available on AWS, Azure, and Google Cloud
- Uses a multi-cluster shared data architecture for elastic compute and storage

---

## Core Concepts

| Concept             | Description |
|---------------------|-------------|
| **Database**        | Logical container for schemas, tables, views |
| **Warehouse**       | Compute cluster for executing queries (can scale independently) |
| **Schema**          | Namespaces for tables and other objects |
| **Virtual Warehouse** | Compute layer that can scale up/down or auto-suspend |
| **Stage**           | Temporary file storage for loading/unloading data |
| **Time Travel**     | Enables querying historical data (up to 90 days) |
| **Zero-Copy Cloning** | Fast cloning of tables/schemas for testing/dev |

---

## SQL & Performance Features

- ANSI SQL compliant
- Automatic clustering (optional manual with `CLUSTER BY`)
- Materialized views
- Query result caching
- Built-in support for semi-structured data: `VARIANT`, `ARRAY`, `OBJECT`
- JSON, Avro, ORC, Parquet ingestion

---

## Common Use Cases

- Data warehouse for BI tools
- Central data lake with structured + semi-structured data
- ELT pipelines (e.g., dbt)
- Rapid test/dev environments via cloning

---

## Data Loading / Integration
- Native `COPY INTO` from S3, Azure Blob, or GCS
- External stage integration (including S3 buckets)
- Connectors: dbt, Fivetran, Airbyte, Snowpipe (for continuous loading)

---

## Pros
- Fully serverless: no infrastructure to manage
- Instant scaling of compute (multi-cluster)
- Excellent support for semi-structured data
- Time Travel + Cloning enable safe experimentation

## Cons
- Proprietary (not open-source)
- Cost can grow rapidly with large or always-on compute
- Limited support for procedural logic compared to PostgreSQL/Oracle

---

## Interview Tips
- Be prepared to explain Time Travel and Zero-Copy Cloning
- Know how Snowflake separates storage from compute
- Understand the tradeoffs of Snowflake vs Redshift vs BigQuery
- Describe how you’d ingest and query JSON data
