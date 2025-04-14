# Apache ZooKeeper

**What it is:**
- A centralized service for maintaining configuration, naming, synchronization, and group services in distributed systems.
- Often used as a coordination layer for tools like Apache Kafka, HBase, Hadoop YARN, etc.

---

## Core Concepts

| Concept      | Description |
|--------------|-------------|
| **ZNode**    | Node in ZooKeeper's hierarchical namespace (like a filesystem path) |
| **Ensemble** | A group of ZooKeeper servers (usually odd-numbered) for quorum |
| **Session**  | Connection between client and ZooKeeper server |
| **Watcher**  | A one-time trigger for state changes (node added/changed/deleted) |
| **Leader Election** | Mechanism to coordinate master selection in distributed systems |

---

## ZooKeeper in Kafka

- Used to store:
  - Broker metadata
  - Topic configs and partitions
  - Controller election
- Kafka 2.8+ supports **KRaft** (Kafka Raft mode) to remove ZooKeeper dependency.

---

## CLI Commands
```bash
# Connect to local server
zkCli.sh -server localhost:2181

# View tree
ls /
get /brokers/ids/0

# Create node
create /myapp "hello"

# Set data
set /myapp "new data"

# Delete node
delete /myapp
```

---

## Use Cases
- Configuration registry
- Service discovery
- Distributed locking / leader election
- Coordination of distributed workers

---

## Design Properties
- CP system (Consistent + Partition tolerant)
- Strong ordering guarantees
- Low write throughput (use for metadata, not large-scale data)

---

## When to Use / Avoid
✅ Use:
- When you need coordination (e.g. master election, locking)
- When you need distributed config management

🚫 Avoid:
- As a general-purpose database
- For high-volume event streams (Kafka is better)
