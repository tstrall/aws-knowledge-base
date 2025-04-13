# AWS CodeDeploy

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ DevOps Engineer – Professional (DOP)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**AWS CodeDeploy** is a fully managed deployment service that automates code deployments to:

- **Amazon EC2 instances**
- **On-premises servers**
- **AWS Lambda functions**
- **Amazon ECS services (blue/green only)**

It supports both **in-place deployments** and **blue/green strategies**, reducing downtime and risk during application updates.

---

## Why should I care?

CodeDeploy helps you safely deploy new code without impacting users:

- **Minimizes downtime** – Supports canary, linear, and all-at-once rollout strategies.
- **Reduces risk** – Includes automatic rollback on failure.
- **Unified experience** – Works with EC2, Lambda, and ECS through a consistent deployment model.
- **Integrates with CI/CD** – Acts as a deployment step in CodePipeline workflows.

---

## When to use it

Use CodeDeploy when:

- You want to automate **deployments across multiple instances**.
- You need **controlled rollout strategies** (canary, blue/green).
- You're deploying code to **EC2, Lambda, or on-prem infrastructure**.
- You want **rollback safety** and lifecycle hooks for pre/post-deploy actions.

---

## Key features

- **Deployment types**:
  - *In-place* (EC2/On-prem): Stop app, replace code, restart.
  - *Blue/green* (Lambda, ECS): Deploy to a new environment, then switch traffic.
- **Lifecycle hooks** – Run scripts at key points during deployment (e.g., `BeforeInstall`, `AfterInstall`).
- **Health checks** – Monitor status of each instance or traffic shift.
- **Rollback** – Automatically revert to previous version if a failure is detected.
- **Traffic shifting (Lambda/ECS)** – Shift traffic in percentages to the new version.
- **Integration with CodePipeline** – Automate deployment step in full CI/CD flow.

---

## Common use cases

- **Web applications on EC2** – Deploy new versions with minimal disruption.
- **Serverless updates** – Shift traffic between Lambda versions.
- **Container upgrades** – Roll out changes in ECS with rollback capability.
- **Hybrid cloud** – Consistent deployment process for on-prem servers and AWS.

---

## Integrations

- **CodePipeline** – Used as the deployment stage.
- **CodeBuild / CodeCommit / GitHub** – Source and build steps for deployment pipelines.
- **CloudWatch Logs / Metrics** – Monitor deployment status and instance health.
- **SNS / EventBridge** – Notifications and automation on deployment events.
- **IAM roles** – Secure and control which entities can perform deployments.

---

## Pricing

- **Free for EC2/On-prem deployments**
- **Billed per Lambda or ECS deployment** (based on number of updated instances and traffic shifts)

[Pricing details →](https://aws.amazon.com/codedeploy/pricing/)

---

## Learn More

- [AWS CodeDeploy Documentation](https://docs.aws.amazon.com/codedeploy/)
- [AppSpec Reference (EC2/On-Prem)](https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file.html)
- [AppSpec for Lambda](https://docs.aws.amazon.com/codedeploy/latest/userguide/app-spec-ref-lambda.html)
- [Deployment Strategies](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html)
- [CodeDeploy + CodePipeline Tutorial](https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-codepipeline-codecommit.html)
