# Apache Flink (Stream Processing)

**What it is:**
- A distributed, real-time stream processing framework
- Designed for low-latency, stateful computations over unbounded (and bounded) data

**How it's different from Spark:**
- **True streaming engine** vs. Spark’s micro-batching (Structured Streaming)
- **Native support for event time**, watermarks, and windowing

---

## Core Concepts

- **Stream vs. Table API**: High-level APIs for stream and batch jobs
- **Operators**: Map, Filter, KeyBy, Reduce, etc.
- **Windowing**:
  - Tumbling, Sliding, Session
  - Based on event time or processing time
- **Watermarks**:
  - Handle out-of-order events
  - Estimate event-time progress
- **Checkpointing**:
  - Enables fault tolerance and state recovery
- **Stateful Processing**:
  - Maintain state across events per key
  - E.g., running totals, session data

---

## Example (DataStream API in Java)
```java
DataStream<String> input = env.socketTextStream("localhost", 9999);
input
  .flatMap(new LineSplitter())
  .keyBy(value -> value.word)
  .window(TumblingProcessingTimeWindows.of(Time.seconds(5)))
  .sum("count")
  .print();
```

---

## Deployment Options

- **Standalone cluster**
- **YARN / Kubernetes / Mesos**
- **Flink on AWS with Kinesis Data Analytics**

---

## Common Use Cases

- Real-time ETL pipelines
- Anomaly detection in logs or metrics
- Streaming joins (enriching with reference data)
- Event-driven applications (IoT, fraud detection)

---

## Things to Know for Interviews

- How Flink handles backpressure
- How checkpointing differs from Spark’s lineage-based recovery
- How windowing and watermarking work together
- When to choose Flink over Spark Streaming
