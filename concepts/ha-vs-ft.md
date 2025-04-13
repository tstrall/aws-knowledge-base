# High Availability vs Fault Tolerance

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**High Availability (HA)** and **Fault Tolerance (FT)** are architectural design principles used to improve system reliability:

- **High Availability**: Aims to minimize downtime by designing systems that can quickly recover from failures.
- **Fault Tolerance**: Aims to eliminate downtime entirely by designing systems that continue to operate correctly even if components fail.

Both are critical in cloud architecture and frequently appear in AWS certification exams.

---

## Why should I care?

Designing for HA and FT is essential when building **resilient, production-grade applications**:

- Reduces the impact of failures on users.
- Increases trust and uptime for mission-critical workloads.
- Influences decisions on **regions, AZs, replication, load balancing**, and **cost**.
- Helps prioritize tradeoffs (e.g., recovery speed vs. complexity).

Understanding the difference helps you choose the right AWS services and architectures.

---

## Key definitions

| Concept           | High Availability                                  | Fault Tolerance                                      |
|------------------|----------------------------------------------------|------------------------------------------------------|
| Goal             | Minimize downtime                                  | Prevent downtime                                     |
| Behavior on failure | Recover quickly (failover, restart)              | Continue operating with no disruption                |
| Example approach | Active/passive with health checks & failover       | Active/active with full duplication                  |
| Downtime         | Possible, but short                                | None (in theory)                                     |
| Cost             | Moderate                                            | High (due to duplication and isolation)              |
| Typical use cases| Web apps, SaaS, non-critical services              | Payment systems, aerospace, life-critical systems    |

---

## AWS examples

| AWS Service or Feature            | HA Support        | FT Support         | Notes                                                   |
|----------------------------------|-------------------|--------------------|---------------------------------------------------------|
| **Auto Scaling Groups (EC2)**    | ✅ Yes            | ❌ No              | Restarts failed instances; not seamless                 |
| **Elastic Load Balancer (ALB/NLB)** | ✅ Yes         | ❌ No              | Routes to healthy targets; doesn’t duplicate logic      |
| **RDS Multi-AZ**                 | ✅ Yes            | ❌ No              | Automated failover; brief downtime during switch        |
| **Aurora Multi-AZ + Reader**     | ✅ Yes            | ✅ (partial)       | Reader may take over; very short failover               |
| **S3**                           | ✅ (designed)     | ✅ (built-in)      | Data is replicated across AZs automatically             |
| **Route 53 Failover**            | ✅ Yes            | ❌ No              | Redirects DNS to healthy endpoints                      |
| **Lambda with retries**          | ✅ (retry logic)  | ❌ No              | Retries errors, but does not prevent all failures       |

---

## When to choose which?

- Choose **High Availability** when:
  - Downtime is tolerable but should be short.
  - You need to balance availability and cost.
  - You’re running typical web apps, APIs, or internal tools.

- Choose **Fault Tolerance** when:
  - Any downtime is unacceptable (e.g., real-time billing, aviation systems).
  - You can afford to fully duplicate systems.
  - You're designing for extreme reliability or compliance (e.g., PCI, HIPAA).

---

## Related design patterns

- **Active-Active**: All nodes serve traffic; improves fault tolerance.
- **Active-Passive**: One node serves traffic; the other takes over on failure (HA).
- **Stateless Services**: Easier to scale and failover.
- **Cross-region replication**: Supports both HA and FT in global designs.

---

## Learn More

- [AWS Reliability Pillar (Well-Architected)](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)
- [Designing for Failure – AWS Best Practices](https://aws.amazon.com/architecture/well-architected/)
- [Amazon RDS Multi-AZ Deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html)
- [Disaster Recovery Options in AWS](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-workloads-on-aws.html)
