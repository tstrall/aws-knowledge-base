# Amazon EC2 (Elastic Compute Cloud)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Amazon EC2 (Elastic Compute Cloud) is AWS's core Infrastructure-as-a-Service (IaaS) offering. It provides secure, resizable virtual machines (“instances”) in the cloud. You can choose from a wide variety of instance types tailored for different workloads (general-purpose, compute-optimized, memory-optimized, GPU, etc.).

EC2 gives you full control over the OS, networking, storage, and installed software — similar to a traditional server environment but highly scalable and pay-as-you-go.

---

## Why should I care?

EC2 is a foundational AWS service and shows up in nearly every AWS architecture:

- **Flexibility** – Full control over OS, network, storage, and instance lifecycle.
- **Scalability** – Easily scale horizontally or vertically using Auto Scaling Groups.
- **Integration** – Works with EBS, VPC, Load Balancers, IAM, CloudWatch, and more.
- **Wide range of instance types** – Optimize cost and performance for your workload.
- **Core to many exam scenarios** – Especially important for cost optimization, availability, and security topics.

---

## When to use it

Use EC2 when:

- You need full OS-level access or to run traditional server-based applications.
- You want to self-manage your compute environment.
- Your application requires specific libraries, runtimes, or low-level tuning.
- You're migrating existing workloads that aren't suitable for containers or serverless.
- You need long-running, persistent compute capacity.

---

## Key features

- **Custom AMIs** – Launch instances with preconfigured operating systems and software.
- **Elastic IPs** – Static public IP addresses that can be reassigned between instances.
- **Instance metadata** – Retrieve instance-level info from within the VM.
- **Placement groups** – Control physical placement for latency or HA needs.
- **Auto Scaling** – Automatically add/remove instances based on demand.
- **Spot Instances** – Purchase unused capacity at steep discounts.
- **Elastic Load Balancing** – Distribute traffic across EC2 instances.

---

## Common use cases

- **Web applications** – Host scalable web servers or application servers.
- **Lift-and-shift workloads** – Migrate existing VMs to the cloud.
- **Custom compute environments** – Machine learning, rendering, gaming, simulations.
- **Self-hosted services** – Databases, Elasticsearch, Jenkins, etc.
- **Bastion hosts and NAT instances** – Secure VPC access and outbound routing.

---

## Integrations

- **Amazon EBS** – Attach persistent block storage volumes to EC2.
- **Elastic Load Balancer** – Distribute traffic across multiple instances.
- **Amazon CloudWatch** – Monitor metrics, set alarms, and trigger Auto Scaling.
- **IAM roles** – Grant instances permissions to access other AWS services.
- **Amazon SSM** – Remotely manage instances without opening SSH ports.

---

## Pricing

EC2 pricing is based on:

- **Instance type and size**
- **Pricing model** (On-Demand, Reserved, Spot, or Savings Plans)
- **Region and availability zone**
- **Attached storage (EBS), data transfer, and other resources**

The Free Tier includes 750 hours per month of a t2.micro or t3.micro instance for 12 months.

[Pricing details →](https://aws.amazon.com/ec2/pricing/)

---

## Learn More

- [Amazon EC2 Developer Guide](https://docs.aws.amazon.com/ec2/index.html)
- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
- [EC2 User Data and Metadata](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html)
- [Spot Instance Best Practices](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html)
