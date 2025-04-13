# AWS Systems Manager

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

AWS Systems Manager (SSM) is a **unified management service** that provides operational control over AWS resources. It allows you to **automate configuration, manage infrastructure at scale, and securely access EC2 instances** — all without needing to SSH into your servers.

SSM is modular and includes capabilities such as:

- **Parameter Store** (secure configuration)
- **Session Manager** (remote shell access)
- **Automation** (runbooks and workflows)
- **Patch Manager** (OS updates at scale)
- **Inventory & Compliance** (visibility + policy enforcement)

---

## Why should I care?

Systems Manager is a **centralized toolkit** for infrastructure automation and security:

- **Secure remote access** – No need for bastion hosts or open SSH ports.
- **Environment configuration** – Centralized config using Parameter Store.
- **Auditability** – All activity is logged to CloudTrail.
- **Automation-ready** – Run commands or workflows across large fleets.
- **Works across accounts and regions** – Ideal for enterprise management at scale.

SSM often shows up in certification scenarios related to automation, patching, secrets management, and security hardening.

---

## When to use it

Use AWS Systems Manager when:

- You want secure shell access to EC2 without SSH keys.
- You need to store app configs, secrets, or feature flags centrally.
- You're managing OS patching, updates, or software installs.
- You want to automate common ops tasks (e.g., AMI creation, cleanup).
- You need an auditable, automated way to run commands across many instances.

---

## Key features

- **Session Manager** – Browser- or CLI-based shell access to EC2 instances with full logging.
- **Parameter Store** – Secure, hierarchical storage for strings, secrets, and config values.
- **Automation** – Define and run documents (runbooks) to automate common tasks.
- **Run Command** – Execute shell commands or scripts across managed nodes.
- **Patch Manager** – Automatically apply OS updates by schedule or policy.
- **Inventory** – Collect metadata (e.g., software versions) from managed instances.
- **OpsCenter / Explorer** – Dashboards and ticket tracking for operational issues.

---

## Common use cases

- **SSM + Lambda** – Retrieve parameters or secrets without bundling them into code.
- **EC2 access** – Log in to instances without managing SSH keys or jump boxes.
- **Secure secrets** – Use Parameter Store (or Secrets Manager) for app configs.
- **Fleet management** – Patch, update, or inspect instances in bulk.
- **Provisioning** – Automate resource setup or maintenance using runbooks.

---

## Integrations

- **IAM** – Fine-grained control over session access and parameter usage.
- **CloudWatch / CloudTrail** – Audit logs and session history.
- **EC2 / EKS / Hybrid instances** – Systems Manager can manage on-prem or multi-cloud nodes too.
- **AWS Lambda / CodePipeline / CDK** – Access or inject SSM parameters during deployments.
- **Secrets Manager** – Use alongside for advanced secret lifecycle features.

---

## Pricing

Most Systems Manager features are **free for basic usage**, including:

- **Session Manager**
- **Parameter Store** (standard tier)
- **Run Command**
- **Patch Manager**

Charges apply for:

- **Parameter Store Advanced Tier**
- **Automation executions**
- **OpsCenter / Explorer**
- **Inventory beyond default limits**

[Pricing details →](https://aws.amazon.com/systems-manager/pricing/)

---

## Learn More

- [AWS Systems Manager Overview](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html)
- [Working with Session Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html)
- [Parameter Store Guide](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html)
- [Automation with SSM Documents](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-automation.html)
- [SSM Agent Setup](https://docs.aws.amazon.com/systems-manager/latest/userguide/ssm-agent.html)
