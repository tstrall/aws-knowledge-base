# Apache Spark (Batch + Stream Processing)

**What it is:**
- Cluster computing framework for processing large data

**Core Concepts:**
- **RDDs:** Resilient Distributed Datasets (low-level)
- **DataFrames:** Optimized tabular abstraction (like Pandas)
- **Lazy evaluation:** Transformations are deferred until an action
- **Spark SQL:** Run SQL queries over distributed data
- **Spark Streaming:** Micro-batch stream processing

**Optimization Features:**
- Catalyst (query optimization)
- Tungsten (memory mgmt + codegen)
- Partitioning & caching

**Common Actions:**
- `collect()`, `count()`, `show()`, `write()`
