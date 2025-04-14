# PyFlink (Apache Flink in Python)

**What it is:**
- Python API for Apache Flink
- Supports batch and streaming jobs using Table API and DataStream API (limited)

---

## Getting Started

```bash
pip install apache-flink
```

Start a local environment:
```bash
./bin/start-cluster.sh
```

---

## Basic Example (Table API)
```python
from pyflink.datastream import StreamExecutionEnvironment
from pyflink.table import StreamTableEnvironment

env = StreamExecutionEnvironment.get_execution_environment()
t_env = StreamTableEnvironment.create(env)

t_env.execute_sql("""
    CREATE TABLE source (
        user_id STRING,
        action STRING,
        event_time TIMESTAMP(3),
        WATERMARK FOR event_time AS event_time - INTERVAL '5' SECOND
    ) WITH (
        'connector' = 'kafka',
        'topic' = 'user-events',
        'properties.bootstrap.servers' = 'localhost:9092',
        'format' = 'json'
    )
""")

result = t_env.sql_query("""
    SELECT user_id, COUNT(*)
    FROM source
    GROUP BY user_id
""")

result.execute().print()
```

---

## Table vs DataStream API
- **Table API:** Declarative, SQL-like
- **DataStream API:** More flexible, but less Python support

---

## Key Concepts in PyFlink
- Event-time vs processing-time semantics
- Watermarks and windowing
- Connectors: Kafka, filesystem, JDBC, etc.
- Catalogs and schemas
- Resource configs via `env_settings` or `TableConfig`

---

## Deployment
- Local execution for dev/test
- Remote to standalone/YARN/Kubernetes
- JAR packages may be required for some connectors in PyFlink

---

## When to Use PyFlink
- Need for Python + Flink features (esp. SQL/Table API)
- Integrating with Python ML or analytics workflows

---

Let me know if you'd like a DataStream API example or PyFlink + Pandas integration demo!

