# AWS SAM (Serverless Application Model)

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ DevOps Engineer – Professional (DOP)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**AWS SAM** is an open-source framework for building serverless applications. It extends AWS CloudFormation with simplified syntax to define Lambda functions, APIs, DynamoDB tables, SQS queues, and more—all in one concise template.

SAM also includes the **`sam` CLI**, which helps you build, test, and deploy applications locally and in the cloud.

---

## Why should I care?

SAM streamlines the development and deployment of serverless apps:

- **Simplified YAML syntax** – Reduces boilerplate compared to raw CloudFormation.
- **Local testing** – Run Lambda functions and API Gateway locally using Docker.
- **Native IaC** – Built on top of CloudFormation with full compatibility.
- **Built-in best practices** – Supports gradual deployments, parameters, environment variables, and permissions.

It’s ideal for teams adopting Infrastructure as Code (IaC) in serverless-first projects.

---

## When to use it

Use SAM when:

- You're building **Lambda-based apps** with API Gateway, DynamoDB, etc.
- You want to **define infrastructure as code** with a short learning curve.
- You want to **test Lambda functions locally** during development.
- You prefer to **package and deploy apps consistently** using a CLI tool.

---

## Key features

- **Resources**: `AWS::Serverless::Function`, `API`, `Table`, `LayerVersion`, and more.
- **Simplified configuration**:
  - Inline policies
  - Environment variables
  - Event sources (e.g., `Api`, `S3`, `Schedule`)
- **SAM CLI**:
  - `sam build`: Compile and prepare artifacts
  - `sam local invoke`: Run a Lambda locally
  - `sam local start-api`: Emulate API Gateway locally
  - `sam deploy`: Deploy to AWS with guided setup
- **Templates** are just CloudFormation → can use `!Ref`, `!Sub`, `Mappings`, etc.
- **Supports deployment hooks**, versioning, and gradual traffic shifting (with CodeDeploy)

---

## Common use cases

- **Serverless web APIs** using Lambda + API Gateway
- **Data processing pipelines** triggered by S3 or SQS
- **Scheduled tasks** via CloudWatch Events (`Schedule`)
- **CI/CD deployments** with GitHub Actions, CodePipeline, or Jenkins

---

## Integrations

- **Lambda** – Simplifies deployment and permissions
- **API Gateway / EventBridge / S3 / SQS** – Common event sources for Lambda
- **DynamoDB / RDS / Aurora Serverless** – Backing data stores
- **AWS CodeDeploy** – Enables canary and linear traffic shifting
- **CloudFormation Stack Outputs** – Integrate with other stacks

---

## Pricing

SAM itself is **free and open source**. You pay only for the underlying AWS resources deployed (e.g., Lambda, S3, API Gateway).

[Pricing details →](https://aws.amazon.com/lambda/pricing/)

---

## Learn More

- [SAM Developer Guide](https://docs.aws.amazon.com/serverless-application-model/)
- [SAM GitHub Repo](https://github.com/aws/aws-sam-cli)
- [Official Templates & Examples](https://github.com/aws-samples/aws-sam-cli-app-templates)
- [SAM CLI Commands Reference](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-commands.html)
