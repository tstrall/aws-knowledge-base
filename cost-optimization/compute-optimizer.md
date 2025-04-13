# AWS Compute Optimizer

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS Compute Optimizer is a service that uses machine learning to recommend optimal AWS resource configurations for performance and cost. It analyzes usage patterns for services like EC2, Lambda, EBS volumes, and ECS services, and suggests improvements such as better instance types, memory allocation, or over-provisioning corrections.

Compute Optimizer helps you **right-size** your resources — avoiding both under- and over-provisioning.

---

## Why should I care?

Compute Optimizer gives you **data-backed recommendations** for reducing costs and improving performance:

- **Finds overprovisioned resources** – Save money by scaling down where usage is low.
- **Avoids underprovisioning** – Prevent performance degradation due to resource constraints.
- **Supports continuous optimization** – Regularly updated as your workload evolves.
- **No manual tuning required** – Uses ML models built from your own historical data.
- **Minimal effort, high impact** – Easy win for cost optimization with almost no setup.

---

## When to use it

Use Compute Optimizer when:

- You want to identify EC2 instances that are too large or too small.
- You’re preparing a cost or architecture review.
- You're managing environments with inconsistent or variable workloads.
- You want to improve performance without blindly scaling up.
- You're automating cost savings analysis across multiple accounts.

---

## Key features

- **EC2 instance recommendations** – Right-size based on CPU, memory, disk, and network metrics.
- **EBS volume recommendations** – Suggests better volume types (e.g., gp2 → gp3) and provisioning.
- **Lambda function recommendations** – Optimizes memory size and execution time.
- **ECS service on Fargate** – Suggests better CPU/memory configuration.
- **Exportable reports** – Download recommendations to CSV or view in the Console.
- **Cross-account visibility** – Available with AWS Organizations integration.

---

## Common use cases

- **Monthly resource optimization** – Regularly tune compute resources as workloads shift.
- **Rightsizing EC2 fleets** – Identify candidates for Reserved Instance or Savings Plans.
- **Post-deployment validation** – Confirm sizing assumptions made during initial rollout.
- **CI/CD optimization** – Tune Lambda or ECS tasks used in automation pipelines.
- **Budget enforcement** – Prevent waste from idle or oversized resources.

---

## Integrations

- **Amazon CloudWatch** – Uses historical performance data (e.g., CPU, memory, I/O).
- **AWS Organizations** – Centralized recommendations across accounts.
- **AWS Budgets & Cost Explorer** – Combine for deeper cost analysis.
- **IAM policies** – Control who can view or apply recommendations.
- **Tagging** – Filter recommendations by project, team, or workload.

---

## Pricing

AWS Compute Optimizer is **free** for basic recommendations.  
Additional features like enhanced infrastructure metrics (15 months of history instead of 3 days) may incur a small fee if enabled.

[Pricing details →](https://aws.amazon.com/compute-optimizer/pricing/)

---

## Learn More

- [AWS Compute Optimizer Overview](https://aws.amazon.com/compute-optimizer/)
- [Supported Resources](https://docs.aws.amazon.com/compute-optimizer/latest/ug/what-is.html)
- [Understanding EC2 Recommendations](https://docs.aws.amazon.com/compute-optimizer/latest/ug/ec2-recommendations.html)
- [Using Compute Optimizer with Organizations](https://docs.aws.amazon.com/compute-optimizer/latest/ug/organization-integration.html)
