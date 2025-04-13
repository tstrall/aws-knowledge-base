# AWS Elastic Beanstalk

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

AWS Elastic Beanstalk is a Platform-as-a-Service (PaaS) offering that allows you to deploy, manage, and scale web applications and services developed with a variety of languages and frameworks (e.g., Python, Node.js, Java, .NET, Go) — without managing the underlying infrastructure.

You simply upload your code, and Elastic Beanstalk automatically handles provisioning of EC2, load balancing, Auto Scaling, monitoring, and more.

---

## Why should I care?

Elastic Beanstalk makes it easy to get started on AWS without needing deep infrastructure knowledge:

- **Reduces complexity** – Handles the provisioning and orchestration of compute, networking, and storage.
- **Customizable** – Full control over resources if needed (e.g., customize EC2 instances or VPC settings).
- **Integrated monitoring** – Provides environment health dashboards, logs, and metrics.
- **Ideal for rapid prototyping** – Great for developers who want to deploy apps quickly.
- **Launchpad for exam topics** – Covers EC2, Auto Scaling, ELB, CloudWatch, IAM, and more.

---

## When to use it

Use Elastic Beanstalk when:

- You want to deploy code quickly without managing infrastructure.
- You're running common web app stacks (e.g., Node.js, Java Spring Boot, Flask).
- You need simplified deployment for full-stack applications (frontend + backend).
- You want a managed environment but with EC2-level control when needed.
- You need a starting point to scale into more customized AWS architectures later.

---

## Key features

- **Supports multiple platforms** – Java, .NET, Node.js, Python, PHP, Ruby, Go, Docker.
- **Managed environment** – Automatically handles capacity provisioning, load balancing, scaling, and health monitoring.
- **Custom configurations** – Use `.ebextensions` or environment variables for fine-tuning.
- **Rolling deployments** – Supports blue/green and canary-style deployments.
- **Full EC2 access** – Under the hood, it uses EC2 instances that you can customize.

---

## Common use cases

- **Web applications** – Deploy monolithic or lightweight web apps with ease.
- **APIs** – Host RESTful APIs with automatic scaling.
- **Prototypes and demos** – Quickly test and share ideas without setting up infra manually.
- **CI/CD integration** – Use with CodePipeline or GitHub Actions to automate deployments.
- **Small teams / startups** – Great for launching MVPs without DevOps overhead.

---

## Integrations

- **Amazon EC2** – Hosts your application.
- **Elastic Load Balancing (ELB)** – Distributes traffic across instances.
- **Auto Scaling** – Automatically adjusts instance count based on demand.
- **Amazon RDS** – Can be configured to provision a relational DB alongside your app.
- **Amazon CloudWatch** – Monitors logs and metrics for environment health.
- **AWS CodePipeline** – Automates deployment workflows.

---

## Pricing

Elastic Beanstalk itself is **free** — you only pay for the underlying resources it provisions (EC2, ELB, RDS, EBS, etc.).

[Pricing details →](https://aws.amazon.com/elasticbeanstalk/pricing/)

---

## Learn More

- [Elastic Beanstalk Developer Guide](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html)
- [Supported Platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html)
- [Using Configuration Files (`.ebextensions`)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/ebextensions.html)
- [Customizing EC2 Instances in Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/customize-containers-ec2.html)
