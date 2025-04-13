# AWS CodePipeline

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ DevOps Engineer – Professional (DOP)

---

## What is it?

**AWS CodePipeline** is a fully managed continuous integration and continuous delivery (CI/CD) service that automates the build, test, and deployment phases of your release process. It enables rapid and reliable delivery of features and updates by orchestrating various AWS services and third-party tools into a cohesive workflow.

---

## Why should I care?

CodePipeline streamlines the software release process, allowing for:

- **Rapid delivery**: Automate the release process for faster and more reliable updates.
- **Consistency**: Ensure uniformity across development, testing, and production environments.
- **Integration**: Seamlessly connect with AWS services like CodeCommit, CodeBuild, CodeDeploy, and third-party tools such as GitHub and Jenkins.
- **Scalability**: Handle complex workflows with multiple stages and parallel actions.

---

## When to use it

Use CodePipeline when you need to:

- Automate the end-to-end software release process.
- Integrate various tools and services into a unified workflow.
- Implement continuous delivery practices for faster time-to-market.
- Maintain high standards of software quality through automated testing and deployment.

---

## Key features

- **Pipeline modeling**: Define a sequence of stages (e.g., source, build, test, deploy) representing your release process.
- **Integration with AWS services**: Connect with CodeCommit, CodeBuild, CodeDeploy, Lambda, and more.
- **Third-party integrations**: Incorporate external tools like GitHub, Bitbucket, and Jenkins.
- **Manual approvals**: Insert approval steps to control the progression of changes.
- **Parallel execution**: Run multiple actions concurrently within a stage.
- **Automatic triggers**: Initiate pipelines based on events such as code commits or pull requests.

---

## Common use cases

- **Continuous delivery**: Automate the release of applications to various environments.
- **Infrastructure as code**: Deploy infrastructure changes using tools like AWS CloudFormation.
- **Multi-environment deployments**: Promote code through development, staging, and production stages.
- **Microservices orchestration**: Manage the deployment of multiple services in a coordinated manner.

---

## Integrations

- **AWS CodeCommit**: Source control repository.
- **AWS CodeBuild**: Build and test automation.
- **AWS CodeDeploy**: Deployment automation to various compute services.
- **AWS Lambda**: Custom logic execution within pipelines.
- **Amazon S3**: Artifact storage and retrieval.
- **AWS CloudFormation**: Infrastructure deployment and management.
- **Third-party tools**: GitHub, Bitbucket, Jenkins, and more.

---

## Pricing

CodePipeline pricing is based on the number of active pipelines per month. The AWS Free Tier includes one active pipeline per month at no charge. Additional pipelines incur a monthly fee.

[Pricing details →](https://aws.amazon.com/codepipeline/pricing/)

---

## Learn More

- [AWS CodePipeline Documentation](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html)
- [Getting Started with AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/getting-started.html)
- [AWS CodePipeline FAQs](https://aws.amazon.com/codepipeline/faqs/)
- [AWS CodePipeline Pricing](https://aws.amazon.com/codepipeline/pricing/)
