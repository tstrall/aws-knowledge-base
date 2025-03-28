# ✅ AWS Certified Solutions Architect – Professional (SAP-C02) Checklist

Track your coverage of advanced architectural topics for the SAP exam.  
✅ = Complete 🔲 = To do  
Includes short descriptions so you can review without clicking into every link.

---

<details>
<summary><strong>🛡️ Multi-Account & Governance</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [AWS Organizations & SCPs](../multi-account/organizations.md) | Manage multi-account governance with Service Control Policies |
| 🔲 | [AWS Control Tower](../multi-account/control-tower.md) | Automates setup of secure, multi-account AWS environments |
| 🔲 | [Delegated Admin Patterns](../multi-account/delegated-admin.md) | Let member accounts manage specific services under control |
| 🔲 | [Landing Zone Design](../multi-account/landing-zone.md) | Foundation for scalable, secure multi-account architecture |

</details>

---

<details>
<summary><strong>🔗 Advanced Networking</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [Transit Gateway](../advanced-networking/transit-gateway.md) | Central hub for inter-VPC and on-prem network routing |
| 🔲 | [VPC Peering](../advanced-networking/vpc-peering.md) | Direct connection between VPCs for private communication |
| 🔲 | [PrivateLink](../advanced-networking/privatelink.md) | Access services securely over AWS internal network |
| 🔲 | [Route 53 DNS Patterns](../advanced-networking/route53-design.md) | Complex DNS routing patterns for distributed apps |
| 🔲 | [Centralized Egress/Ingest Routing](../advanced-networking/central-egress.md) | Route internet or internal traffic through shared VPCs |

</details>

---

<details>
<summary><strong>🧩 Disaster Recovery & Multi-Region</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [DR Strategies](../resiliency/dr-strategies.md) | Backup & Restore, Pilot Light, Warm Standby, Active/Active |
| 🔲 | [Multi-Region Active/Passive](../resiliency/multi-region-ha.md) | Failover-based HA across AWS regions |
| 🔲 | [Route 53 Failover](../resiliency/route53-failover.md) | DNS-based routing to healthy regions |
| 🔲 | [RTO / RPO](../resiliency/rto-rpo.md) | Recovery Time and Recovery Point Objectives for DR planning |
| 🔲 | [Data Replication Techniques](../resiliency/replication-strategies.md) | Options like S3 CRR, Aurora Global, or DMS |

</details>

---

<details>
<summary><strong>⚙️ Deployment & Automation at Scale</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [CloudFormation StackSets](../infra/stacksets.md) | Deploy resources across accounts and regions |
| 🔲 | [AWS CDK](../infra/cdk.md) | Define cloud infrastructure in code using Python, TypeScript, etc. |
| 🔲 | [CI/CD with CodePipeline](../infra/pipelines.md) | Automate software delivery from source to deployment |
| 🔲 | [Canary / Blue-Green Deployments](../infra/canary-bluegreen.md) | Gradual rollout or swap routing for safe deployments |
| 🔲 | [Centralized CloudWatch/CloudTrail](../monitoring/cloudwatch-central.md) | Unified monitoring and audit logging in multi-account setups |

</details>

---

<details>
<summary><strong>💸 Cost & Billing Strategy</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [Custom Cost Tags](../cost-optimization/cost-tags.md) | Tag-based allocation of AWS usage across teams or projects |
| 🔲 | [Consolidated Billing / CUR](../cost-optimization/consolidated-billing.md) | Combine charges and analyze usage with Cost & Usage Reports |
| 🔲 | [Cross-Account Budgeting](../cost-optimization/multi-account-budget.md) | Set cost limits and alerts across linked accounts |

</details>

---

<details>
<summary><strong>🚚 Data Transfer & Hybrid</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [Snowball vs DataSync](../data-transfer/snowball-vs-datasync.md) | Physical vs online data migration tools |
| 🔲 | [Transfer Acceleration](../data-transfer/transfer-acceleration.md) | Speed up S3 uploads using global edge locations |
| 🔲 | [VPN vs Direct Connect](../data-transfer/vpn-direct-connect.md) | Secure connectivity options to on-premises data centers |
| 🔲 | [Storage Gateway](../storage/storage-gateway.md) | Hybrid storage for backups or caching between on-prem and AWS |

</details>

---

<details>
<summary><strong>📊 Compliance & Monitoring</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [AWS Config (multi-account)](../monitoring/aws-config.md) | Track resource configurations and changes across accounts |
| 🔲 | [CloudTrail Aggregation](../monitoring/cloudtrail.md) | Centralize API audit logs for compliance auditing |
| 🔲 | [Security Hub Aggregation](../security/security-hub.md) | View findings across accounts from GuardDuty, Macie, etc. |
| ✅ | [KMS](../security/kms.md) | Encryption key management for AWS services |
| ✅ | [Macie](../security/macie.md) | S3 data classification and sensitive data detection |
| ✅ | [GuardDuty](../security/guardduty.md) | Monitors accounts for threats and unusual behavior |
| 🔲 | [IAM Access Analyzer](../identity-access/iam-access-analyzer.md) | Detects unintended access via IAM policies and roles |

</details>

---

<details>
<summary><strong>🧠 Design Tradeoffs & Scenarios</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| 🔲 | [Availability vs Cost Tradeoffs](../concepts/design-tradeoffs.md) | Balance redundancy, scaling, and price per use case |
| 🔲 | [Migration Phases & Rollback](../concepts/migration-planning.md) | Plan safe migrations with rollback and verification |
| 🔲 | [Choosing Storage/DB per Use Case](../concepts/choose-storage.md) | Compare S3, EFS, EBS, Aurora, RDS, DynamoDB, etc. |

</details>

---

📘 See [Study Strategy](./STUDY_STRATEGY.md) to learn how this checklist fits into your exam prep process.
