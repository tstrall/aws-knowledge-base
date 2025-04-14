# Apache Kafka (Stream Processing)

**What it is:**
- Distributed event streaming platform
- Pub/sub model using topics and partitions

**Core Concepts:**
- **Producer/Consumer:** Write/read messages
- **Topic:** Named stream
- **Partition:** Unit of parallelism & ordering
- **Consumer Group:** Allows parallel processing
- **Offset:** Position of message in partition
- **Retention:** Time or size-based message retention

**Key Features:**
- Scalable horizontally
- High throughput
- Durable (disk-backed)

**Use Cases:**
- Microservice messaging backbone
- Event-driven pipelines
- Log/event aggregation

**CLI Example:**
```bash
kafka-console-producer --broker-list localhost:9092 --topic test-topic
```
