# Amazon EC2 Auto Scaling

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon EC2 Auto Scaling is a service that automatically adjusts the number of EC2 instances in a group based on defined conditions. It ensures that you always have the right amount of compute capacity to meet demand while minimizing cost.

Auto Scaling Groups (ASGs) are defined with launch templates or launch configurations, scaling policies, and instance health checks.

---

## Why should I care?

Auto Scaling helps you build **resilient, cost-efficient systems**:

- **Optimizes cost** – Scale in when demand drops to save money.
- **Improves availability** – Replace unhealthy instances automatically.
- **Handles bursts of traffic** – Add instances during high load automatically.
- **Enables self-healing** – Automatically restarts failed instances.
- **Reduces manual intervention** – Once configured, scaling is automatic and policy-driven.

It's commonly tested in exam scenarios related to high availability, performance efficiency, and cost optimization.

---

## When to use it

Use Auto Scaling when:

- You run stateless or loosely coupled workloads on EC2.
- You want to ensure minimum and maximum instance counts.
- Your traffic varies (e.g., day/night cycles, promotions, batch jobs).
- You want automatic recovery from EC2 instance failure.
- You need predictive or scheduled scaling for known usage patterns.

---

## Key features

- **Launch templates** – Define instance type, AMI, key pair, security groups, etc.
- **Scaling policies**:
  - *Target tracking* – Maintain a metric like CPU at a target value.
  - *Step scaling* – Add/remove instances based on threshold breaches.
  - *Scheduled scaling* – Scale at specific times.
  - *Predictive scaling* – Forecast demand and scale accordingly.
- **Health checks** – Automatically replace failed or unresponsive instances.
- **Elastic Load Balancer integration** – Evenly distribute traffic across ASG members.
- **Lifecycle hooks** – Run custom actions when instances launch or terminate.

---

## Common use cases

- **Web applications** – Handle traffic spikes and scale back down during off-hours.
- **Batch processing** – Automatically scale out to run jobs, then scale in when finished.
- **Microservices** – Keep service-level compute reactive and cost-efficient.
- **Dev/test environments** – Auto-scale for scheduled test runs or CI/CD pipelines.

---

## Integrations

- **EC2** – Launch and manage compute instances.
- **Elastic Load Balancing (ELB)** – Auto-register new instances and route traffic.
- **CloudWatch** – Trigger scaling actions based on monitored metrics.
- **SNS / Lambda** – Use lifecycle hooks to send notifications or run automation.
- **Amazon SSM** – Automate config management during launch.

---

## Pricing

There is **no additional cost** for using EC2 Auto Scaling. You only pay for the EC2 instances and other resources provisioned (e.g., EBS, data transfer).

[Pricing details →](https://aws.amazon.com/ec2/autoscaling/pricing/)

---

## Learn More

- [EC2 Auto Scaling Developer Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
- [Scaling Policies](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html)
- [Auto Scaling Lifecycle Hooks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html)
- [Predictive Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html)
