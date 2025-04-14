# PySpark (Spark in Python)

**What it is:**
- Python API for Apache Spark

**Typical Workflow:**
```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("MyApp").getOrCreate()
df = spark.read.csv("data.csv", header=True)
df.filter(df.age > 30).groupBy("country").count().show()
```

**Functions to Know:**
- `read.json`, `read.parquet`
- `filter`, `select`, `groupBy`, `agg`
- `withColumn`, `drop`, `orderBy`
- `.write.mode("overwrite").parquet("/path")`

**Schema Management:**
- Explicit schemas reduce parsing errors
