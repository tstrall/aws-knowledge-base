# AWS Trusted Advisor

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS Trusted Advisor is an online resource that provides **real-time recommendations** to help you optimize your AWS infrastructure for:

- **Cost savings**
- **Performance**
- **Security**
- **Fault tolerance**
- **Service limits**

It analyzes your AWS environment and compares it against AWS best practices. Some checks are available for all accounts, while full access requires a Business or Enterprise Support plan.

---

## Why should I care?

Trusted Advisor helps you **identify inefficiencies and vulnerabilities** in your AWS setup:

- **Spot underused resources** to reduce cost.
- **Identify security misconfigurations**, like open ports or public S3 buckets.
- **Prevent service interruptions** by monitoring service limits.
- **Improve resiliency** with fault tolerance checks.
- **Optimize performance** by validating configuration choices.

It’s also a common reference in AWS certification exams, particularly around cost optimization and operational excellence.

---

## When to use it

Use Trusted Advisor when:

- You're regularly reviewing cost or usage.
- You want an automated “second opinion” on your AWS configuration.
- You're managing infrastructure at scale or across teams.
- You're implementing a Well-Architected Framework review.
- You need to track compliance with best practices.

---

## Key features

- **Cost Optimization** – Detects unused or idle resources (e.g., underutilized EC2, low-utilization EBS, idle load balancers).
- **Security** – Flags open security groups, public S3 buckets, exposed IAM keys, etc.
- **Fault Tolerance** – Checks for proper backups, multi-AZ deployments, and service health.
- **Performance** – Suggests instance type upgrades, overprovisioned resources, and latency improvements.
- **Service Limits** – Warns if you're nearing AWS service quotas.
- **Dashboard and API** – View checks in the AWS Console or retrieve results via the API.

---

## Common use cases

- **Monthly billing reviews** – Identify cost savings opportunities.
- **Security audits** – Spot misconfigured security settings.
- **Limit tracking** – Prevent service disruptions by monitoring account-level quotas.
- **Environment reviews** – Perform architecture reviews and apply AWS best practices.
- **Operational dashboards** – Integrate results with internal tools or ticketing systems.

---

## Integrations

- **AWS Support Plans** – Full Trusted Advisor access requires Business or Enterprise support.
- **AWS Organizations** – Use the Organizational View to consolidate recommendations across accounts.
- **AWS CLI / SDK** – Programmatically retrieve check results for automation.
- **AWS Health Dashboard** – Pair with health events to improve operational awareness.

---

## Pricing

- **Free tier** includes 7 core checks:
  - Service limits
  - IAM use
  - MFA on root account
  - S3 bucket permissions
  - Security groups (open ports)
  - EBS public snapshots
  - RDS public snapshots

- **Business or Enterprise Support** is required to unlock all checks.

[Pricing and support plan details →](https://aws.amazon.com/premiumsupport/trustedadvisor/)

---

## Learn More

- [AWS Trusted Advisor Overview](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)
- [List of Trusted Advisor Checks](https://docs.aws.amazon.com/awssupport/latest/user/trusted-advisor.html)
- [Using Trusted Advisor Organizational View](https://docs.aws.amazon.com/awssupport/latest/user/organizational-view.html)
- [Trusted Advisor API Reference](https://docs.aws.amazon.com/awssupport/latest/APIReference/API_Operations_AWS_Trusted_Advisor.html)
