# ETL (Extract, Transform, Load)

**What it is:**
- A data pipeline pattern used to move and reshape data from source systems to targets (like a data warehouse)
- Typically involves:
  - **Extract:** Read raw data from source systems
  - **Transform:** Clean, standardize, and enrich the data
  - **Load:** Write the processed data to a destination

---

## Variations

| Pattern | Description |
|---------|-------------|
| **ETL** | Classic approach: transform data before loading it into the warehouse |
| **ELT** | Load raw data first (into warehouse or lake), then transform inside (e.g. using SQL) |
| **Streaming ETL** | Real-time pipelines (e.g., Kafka → Flink → S3) |

---

## Tools by Stage

| Stage     | Common Tools |
|-----------|---------------|
| Extract   | Sqoop, NiFi, Kafka Connect, Airbyte, AWS Glue |
| Transform | Spark, dbt, Python, Flink, Pandas, SQL |
| Load      | Redshift, BigQuery, Snowflake, S3, PostgreSQL |

---

## Example (PySpark-based ETL)
```python
# Extract
df = spark.read.csv("raw/events.csv", header=True)

# Transform
df_clean = df.filter(df["status"] == "OK")

# Load
df_clean.write.mode("overwrite").parquet("s3://my-bucket/clean/events")
```

---

## Key Considerations
- **Data quality:** Nulls, type coercion, deduplication
- **Orchestration:** Use Airflow, Step Functions, or Prefect to run ETL jobs
- **Performance:** Partitioning, pushdown filters, minimizing shuffles
- **Auditability:** Logging, versioning, and lineage

---

## Interview Tips
- Know tradeoffs of ETL vs ELT
- Be ready to describe a pipeline you built or maintained
- Emphasize reproducibility and testability of transformation logic
