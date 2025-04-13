# AWS Certified Solutions Architect – Associate (SAA-C03) Checklist

Track your coverage of all relevant topics for the SAA exam.  
✅ = Complete 🔲 = To do  
Topics include short descriptions for quick review.  
Linked entries point to your knowledge base `.md` files.

---

<details>
<summary><strong>Application Integration</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Amazon SQS](../app-integration/sqs.md) | Simple queueing service for decoupled workloads |
| ✅ | [Amazon SNS](../app-integration/sns.md) | Pub/sub messaging with email, SMS, Lambda triggers |
| ✅ | [Amazon EventBridge](../app-integration/eventbridge.md) | Event bus for application and service events |
| ✅ | [AWS Step Functions](../app-integration/step-functions.md) | Orchestrates workflows using AWS services |

</details>

---

<details>
<summary><strong>Compute</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Amazon EC2](../compute/ec2.md) | Virtual servers in the cloud |
| ✅ | [Auto Scaling](../compute/auto-scaling.md) | Automatically adjusts capacity based on demand |
| ✅ | [Elastic Load Balancer (ALB/NLB)](../compute/elb.md) | Distributes traffic across targets |
| ✅ | [AWS Lambda](../compute/lambda.md) | Serverless functions that scale automatically |
| ✅ | [Elastic Beanstalk](../compute/beanstalk.md) | Platform-as-a-service for quick app deployment |

</details>

---

<details>
<summary><strong>Cost Optimization</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Trusted Advisor](../cost-optimization/trusted-advisor.md) | Recommends optimizations for cost, security, and more |
| ✅ | [Compute Optimizer](../cost-optimization/compute-optimizer.md) | Recommends better EC2 instance types based on usage |

</details>

---

<details>
<summary><strong>Databases</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Amazon RDS](../databases/rds.md) | Managed relational databases with backups and HA |
| ✅ | [Amazon Aurora](../databases/aurora.md) | High-performance version of RDS (MySQL/Postgres compatible) |
| ✅ | [Amazon DynamoDB](../databases/dynamodb.md) | Fully managed NoSQL database |
| ✅ | [Amazon ElastiCache](../databases/elasticache.md) | In-memory caching for speed (Redis/Memcached) |

</details>

---

<details>
<summary><strong>Deployment & Automation</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [AWS CloudFormation](../infra/cloudformation.md) | IaC for automating AWS resource provisioning |
| ✅ | [AWS CLI / SDK](../infra/cli.md) | Programmatic access to AWS APIs |
| ✅ | [AWS Systems Manager](../infra/systems-manager.md) | Manage EC2, patching, parameters, and remote commands |

</details>

---

<details>
<summary><strong>Design Principles</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Well-Architected Framework](../concepts/well-architected.md) | AWS’s pillars for reliable and efficient cloud design |
| ✅ | [Shared Responsibility Model](../concepts/shared-responsibility.md) | Clarifies security roles between AWS and you |
| ✅ | [High Availability vs Fault Tolerance](../concepts/ha-vs-ft.md) | Design patterns for resilient applications |
| ✅ | [Storage & DB Tradeoffs](../concepts/choose-storage.md) | Choosing the right data store for each use case |

</details>

---

<details>
<summary><strong>Monitoring & Logging</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Amazon CloudWatch](../monitoring/cloudwatch.md) | Logs, metrics, alarms, dashboards |
| ✅ | [AWS CloudTrail](../monitoring/cloudtrail.md) | Records API calls across the account for auditing |

</details>

---

<details>
<summary><strong>Networking</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [VPC Basics](../networking/vpc-basics.md) | Isolated virtual network where AWS resources live |
| ✅ | [Route 53](../networking/route53.md) | Scalable DNS and traffic routing service |
| ✅ | [Elastic IPs](../networking/elastic-ip.md) | Static public IP addresses for EC2 and other services |

</details>

---

<details>
<summary><strong>Security & Identity</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [AWS IAM](../identity-access/iam.md) | Core service for controlling access to AWS resources |
| ✅ | [AWS KMS](../security/kms.md) | Manages encryption keys used to protect data |
| ✅ | [Amazon Macie](../security/macie.md) | Scans S3 for sensitive data (e.g., PII, PHI) |
| ✅ | [Amazon GuardDuty](../security/guardduty.md) | Detects threats using CloudTrail, VPC logs, and DNS activity |
| ✅ | [AWS Security Hub](../security/security-hub.md) | Centralized view of security findings across AWS |
| ✅ | [AWS WAF](../security/waf.md) | Protects web apps from common attacks (e.g., XSS, SQLi) |

</details>

---

<details>
<summary><strong>Storage</strong></summary>

| Status | Topic | Description |
|--------|-------|-------------|
| ✅ | [Amazon S3](../storage/s3.md) | Scalable, durable object storage for nearly any workload |
| ✅ | [S3 Glacier / Deep Archive](../storage/glacier.md) | Long-term cold storage with low retrieval frequency |
| ✅ | [Amazon EBS](../storage/ebs.md) | Block storage volumes for EC2 instances |
| ✅ | [Amazon EFS](../storage/efs.md) | Fully managed NFS-based file system |

</details>

---

See [Study Strategy](./STUDY_STRATEGY.md) to learn how this checklist fits into your exam prep process.