# AWS CloudFormation

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

AWS CloudFormation is an **Infrastructure as Code (IaC)** service that lets you define, provision, and manage AWS infrastructure using human-readable templates in **JSON or YAML**. With CloudFormation, you can describe your entire AWS environment as code and deploy it in a predictable, repeatable manner.

Templates define resources like EC2 instances, VPCs, S3 buckets, IAM roles, Lambda functions, and more — all managed together as a **stack**.

---

## Why should I care?

CloudFormation enables **automation and consistency** in infrastructure provisioning:

- **Reduces human error** – Infrastructure is version-controlled and repeatable.
- **Saves time** – Automates complex provisioning processes.
- **Tracks changes** – Changes are managed via updates to templates (change sets).
- **Integrated with AWS** – Deep support for nearly all AWS services.
- **Foundation for DevOps** – Enables CI/CD, infrastructure automation, and compliance as code.

It’s frequently covered in AWS exams as the default IaC option.

---

## When to use it

Use CloudFormation when:

- You want to manage AWS resources using code (IaC).
- You need repeatable deployments across environments (dev, staging, prod).
- You're setting up CI/CD or automated provisioning pipelines.
- You need change tracking and rollback for infrastructure.
- You want to enforce consistent security, tagging, and networking policies.

---

## Key features

- **Stacks** – Deploy and manage infrastructure resources as a single unit.
- **Templates (JSON/YAML)** – Declaratively define resources and configuration.
- **Parameters** – Inject values at runtime for flexibility.
- **Outputs** – Export useful data like ARNs or URLs between stacks.
- **Nested stacks** – Modularize templates for reuse and clarity.
- **Change sets** – Preview impact of updates before applying.
- **Drift detection** – Identify manual changes outside CloudFormation.
- **StackSets** – Deploy stacks across multiple accounts or regions.

---

## Common use cases

- **VPC and networking setup** – Consistent, reproducible VPC deployments.
- **Application stacks** – Deploy Lambda, API Gateway, S3, and DynamoDB together.
- **CI/CD environments** – Automatically spin up infrastructure from code.
- **IAM and security management** – Define roles, policies, and permissions in code.
- **Multi-account deployments** – Use StackSets for organizational rollouts.

---

## Integrations

- **AWS CodePipeline / CodeBuild** – Automate infrastructure deployment.
- **Amazon S3** – Store templates for versioning and reuse.
- **IAM** – Apply fine-grained permissions for creating/updating stacks.
- **CloudWatch Logs** – View detailed stack events and troubleshooting logs.
- **SSM Parameter Store / Secrets Manager** – Inject runtime configuration values.
- **AWS Config / Audit Tools** – Track changes and verify compliance.

---

## Pricing

CloudFormation itself is **free**.  
You only pay for the AWS resources it provisions (e.g., EC2, S3, Lambda).  
Exceptions: You may incur costs when using StackSets with AWS Organizations (e.g., in automation regions).

[Pricing details →](https://aws.amazon.com/cloudformation/pricing/)

---

## Learn More

- [CloudFormation Documentation](https://docs.aws.amazon.com/cloudformation/index.html)
- [Template Anatomy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)
- [Built-In Functions (Fn::)](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html)
- [Change Sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html)
- [Drift Detection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)
