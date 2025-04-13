# AWS CLI & SDK

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

The **AWS Command Line Interface (CLI)** and **AWS SDKs** allow you to interact with AWS services **programmatically or via terminal**, rather than using the AWS Management Console.

- **AWS CLI**: A unified tool for managing AWS services from your terminal or scripts.
- **AWS SDKs**: Language-specific libraries (Python, JavaScript, Go, etc.) for interacting with AWS APIs in your code.

Both are essential for **automation, scripting, and building custom applications** that integrate with AWS.

---

## Why should I care?

Using the CLI and SDK unlocks a powerful set of tools for building and managing AWS environments:

- **Automation** – Script repeatable workflows (infrastructure, backups, deployments).
- **Efficiency** – Perform complex operations quickly (bulk S3 deletes, IAM audit, etc.).
- **CI/CD** – Integrate AWS actions into pipelines and deployments.
- **Infrastructure as Code** – Drive provisioning tools like CloudFormation, CDK, Terraform.
- **Custom integrations** – Use SDKs to build apps that trigger AWS services directly.

Both are covered in AWS exams, especially in deployment, automation, and monitoring scenarios.

---

## When to use it

Use the **AWS CLI** when:

- You want to script or automate infrastructure tasks.
- You’re operating via shell (Bash, PowerShell, etc.).
- You need quick one-off operations without the console.

Use **AWS SDKs** when:

- You're building an application that uses AWS services programmatically.
- You need typed, language-native access to AWS APIs (Python, JavaScript, Java, etc.).
- You want to build serverless apps, bots, or backend systems integrated with AWS.

---

## Key features

### AWS CLI
- Supports all AWS services and APIs.
- Output in text, table, or JSON format.
- Profile support for multi-account setups.
- Works with AWS IAM, SSO, MFA, and environment credentials.
- Can be used in automation scripts, cron jobs, CI/CD tools.

### AWS SDKs
- Language-specific clients with API abstraction (e.g., `boto3` for Python).
- Handle retries, pagination, and auth under the hood.
- Integrated with cloud-native frameworks (Flask, Express, Spring, etc.).
- Enable service orchestration within apps (e.g., uploading to S3, invoking Lambda).

---

## Common use cases

- **CLI**
  - Automate deployments or rollbacks (e.g., `aws cloudformation deploy`)
  - Query cost and usage data
  - Manage IAM users and policies
  - Inspect logs and metrics from CloudWatch

- **SDK**
  - Write code that uploads to S3 or queries DynamoDB
  - Trigger workflows via Lambda or EventBridge
  - Build dashboards that pull live metrics from CloudWatch
  - Implement permission-aware apps using STS and IAM

---

## Integrations

- **AWS CloudFormation / CDK / Terraform** – Use CLI in provisioning workflows.
- **CI/CD tools** – Common in GitHub Actions, CodeBuild, Jenkins pipelines.
- **Local dev tools** – SDKs integrate with IDEs and debuggers.
- **AWS IAM / SSO / STS** – Secure CLI/SDK operations with temporary credentials.
- **AWS Config / CloudTrail / CloudWatch** – Monitor and audit scripted activity.

---

## Pricing

Both AWS CLI and SDKs are **free** tools provided by AWS.  
You only pay for the AWS services you use with them.

---

## Learn More

- [AWS CLI Documentation](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)
- [AWS SDKs Overview](https://aws.amazon.com/tools/)
- [Configure Named Profiles](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html)
- [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/)
- [boto3 SDK for Python](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [AWS SDK for JavaScript](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/)
