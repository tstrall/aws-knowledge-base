# AWS CodeBuild

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ DevOps Engineer – Professional (DOP)

---

## What is it?

**AWS CodeBuild** is a fully managed **build service** that compiles source code, runs tests, and produces deployable artifacts. It eliminates the need to provision, manage, and scale your own build servers.

You define builds using a `buildspec.yml` file or by configuring the steps in the console. CodeBuild can be used standalone or as part of a larger CI/CD pipeline (e.g., with CodePipeline).

---

## Why should I care?

CodeBuild provides **scalable, pay-as-you-go build infrastructure** with deep AWS integrations:

- **Zero infrastructure** – AWS handles provisioning, scaling, and maintenance.
- **Custom environments** – Use standard or custom Docker images.
- **Security** – Supports IAM roles, VPC access, and secrets from AWS Secrets Manager or Parameter Store.
- **Cost-effective** – Billed per-minute of actual build time.
- **Integrated** – Works with GitHub, CodePipeline, CodeCommit, S3, and more.

---

## When to use it

Use CodeBuild when:

- You want to automate build and test steps in a CI/CD pipeline.
- You need an ephemeral, container-based build environment.
- You require scalable parallel builds or long-running builds.
- You want to build Docker images in a secure, isolated environment.

---

## Key features

- **`buildspec.yml`** – Define build commands, environment variables, reports, and artifact handling.
- **Environment types** – Use AWS-provided images or bring your own Docker image.
- **Reports** – Output test reports (e.g., JUnit) for pass/fail visibility.
- **Build caching** – Reuse artifacts across builds to improve speed.
- **Batch builds** – Build multiple source variants simultaneously.
- **Integration with CodePipeline** – Use as a build step in automated workflows.

---

## Common use cases

- **Compiling code** (Java, Python, Node.js, Go, etc.).
- **Running tests** and publishing test results.
- **Packaging Lambda or container artifacts** for deployment.
- **Building and pushing Docker images** to ECR or Docker Hub.
- **Custom build steps** for IaC tools (e.g., Terraform, CDK).

---

## Integrations

- **CodePipeline** – Use as the `Build` action in a deployment pipeline.
- **CodeCommit / GitHub / Bitbucket** – Pull source code from a repository.
- **S3 / ECR** – Upload artifacts or container images.
- **CloudWatch Logs** – View detailed logs and troubleshoot build failures.
- **CloudTrail / EventBridge** – Monitor build status or trigger workflows.
- **IAM** – Fine-grained access control for build environments.

---

## Pricing

Billed per **build minute** based on the compute type:

- `BUILD_GENERAL1_SMALL`: Lower cost, suitable for lightweight tasks.
- `BUILD_GENERAL1_MEDIUM / LARGE`: More CPU/memory for bigger builds.
- **Free Tier**: 100 build minutes per month for free.

[Pricing details →](https://aws.amazon.com/codebuild/pricing/)

---

## Learn More

- [AWS CodeBuild Docs](https://docs.aws.amazon.com/codebuild/)
- [Buildspec Reference](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html)
- [CodeBuild + Docker Walkthrough](https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html)
- [CodeBuild and CodePipeline Integration](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference-CodeBuild.html)
