# Apache NiFi

**What it is:**
- A visual, low-code data integration and flow management tool
- Designed for automating the movement and transformation of data between systems

---

## Core Concepts

| Concept        | Description |
|----------------|-------------|
| **FlowFile**   | The basic unit of data in NiFi (content + attributes) |
| **Processor**  | A component that performs an action (e.g. fetch, transform, route) |
| **Connection** | A queue between processors; holds FlowFiles |
| **Process Group** | A container for grouping processors and connections |
| **Controller Service** | Shared service used by processors (e.g. database connection) |
| **Reporting Task** | Gathers stats/metrics from the NiFi instance |

---

## Key Features

- Visual drag-and-drop interface
- Back-pressure and prioritization for flow control
- Provenance tracking (complete data lineage)
- Built-in processors for Kafka, S3, HTTP, FTP, DBs, JSON, CSV, etc.
- Fine-grained security (TLS, LDAP, multi-tenant access)
- Flow versioning via NiFi Registry

---

## Typical Use Cases

- Real-time log/event ingestion
- ETL between databases, filesystems, message queues
- Streaming data preparation for analytics or ML
- Data masking and enrichment pipelines

---

## Example Flow
1. `GetFile` (monitor a directory)
2. `UpdateAttribute` (add metadata)
3. `ConvertRecord` (CSV to JSON)
4. `PutKafka` (send to Kafka topic)

---

## Deployment Options
- Standalone or cluster
- On-prem, cloud VM, or containerized
- Managed: Cloudera DataFlow, Amazon EC2 deployments

---

## Interview Tips
- Know when to use NiFi vs. Airflow, Flink, or Spark
- Be able to explain provenance and back-pressure
- Understand how to handle high-throughput + failure scenarios
- Describe how you'd version, deploy, and monitor a flow
