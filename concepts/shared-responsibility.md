# AWS Shared Responsibility Model

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

The **Shared Responsibility Model** defines the division of security and compliance responsibilities between **AWS** and **the customer**.

- **AWS is responsible for security *of* the cloud** — the infrastructure that runs AWS services.
- **Customers are responsible for security *in* the cloud** — the configuration and management of their own resources and data.

This model applies to all AWS services and underpins how cloud security is structured.

---

## Why should I care?

Understanding the Shared Responsibility Model is **critical for AWS certifications** and real-world cloud security:

- **Clarifies who secures what** – Avoids assumptions that AWS covers customer-side misconfigurations.
- **Impacts compliance** – You remain responsible for protecting customer data, access, and configurations.
- **Varies by service type** – More managed services (e.g., Lambda, S3) shift more responsibility to AWS.

AWS exam questions often focus on **who is responsible** for specific layers of infrastructure or application security.

---

## When to use it

Use the model when:

- **Designing secure architectures** – Know your responsibilities for IAM, encryption, and monitoring.
- **Conducting compliance audits** – Separate AWS’s compliance scope from your own.
- **Using new AWS services** – Understand what controls are managed by AWS vs. configurable by you.
- **Responding to incidents** – Identify who owns remediation actions at each layer.

---

## Key concepts

| Responsibility Area                   | AWS Responsibility         | Customer Responsibility                |
|--------------------------------------|----------------------------|----------------------------------------|
| **Physical infrastructure**          | ✅                          | ❌                                      |
| **Hypervisor, host OS, networking**  | ✅                          | ❌                                      |
| **AWS global infrastructure**        | ✅                          | ❌                                      |
| **IAM and access control**           | ❌                          | ✅ (IAM users, roles, MFA)              |
| **Data encryption and classification** | ❌                        | ✅ (e.g., KMS, S3 bucket policies)      |
| **Patching guest OS and apps**       | ❌ (for EC2)                | ✅ (EC2, RDS custom OS, containers)     |
| **Application-level security**       | ❌                          | ✅ (validation, secrets, logging)       |
| **Compliance configuration**         | ❌                          | ✅ (tags, SCPs, backup, logging policies) |

---

## Common examples

- **S3 bucket with public access** – AWS secures the storage service, *you* must configure access correctly.
- **EC2 instance patching** – AWS secures the host, *you* are responsible for patching the guest OS.
- **Lambda function permissions** – AWS secures execution, *you* must configure IAM roles and resource access.
- **RDS backup retention** – AWS stores backups, *you* choose retention and encryption settings.

---

## Service spectrum

The more **managed** the service, the **less responsibility** you manage directly:

| Service Type         | Example              | Customer Responsibility           |
|----------------------|----------------------|-----------------------------------|
| IaaS                 | EC2, VPC             | High – full OS and app config     |
| PaaS                 | RDS, Elastic Beanstalk | Medium – app config, access control |
| Serverless / SaaS    | Lambda, S3, DynamoDB | Low – mostly access and data      |

---

## Integrations

- **IAM** – You manage access policies and credential management.
- **KMS / S3 / RDS** – You configure encryption and backup settings.
- **CloudTrail / Config / GuardDuty** – You monitor and detect misconfigurations.
- **AWS Organizations / SCPs** – You enforce governance at scale.

---

## Pricing

The Shared Responsibility Model is **not a service**, so it has no cost — but **failures to uphold it can be costly**, in terms of:

- Security breaches
- Compliance violations
- Data loss or leakage
- Downtime from misconfiguration

---

## Learn More

- [Shared Responsibility Model (AWS Overview)](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [Whitepaper PDF](https://d1.awsstatic.com/whitepapers/aws-shared-responsibility-model.pdf)
- [Customer vs AWS Responsibilities by Service](https://docs.aws.amazon.com/securityhub/latest/userguide/shared-responsibility.html)
- [Security Best Practices Center](https://aws.amazon.com/architecture/security-best-practices/)
