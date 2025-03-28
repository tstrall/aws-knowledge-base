# Amazon VPC: Virtual Private Cloud (Basics)

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)

---

## What is it?

Amazon VPC (Virtual Private Cloud) is the foundational networking layer in AWS.  
It lets you **provision a logically isolated network** within the AWS cloud, where you can launch AWS resources like EC2 instances, RDS databases, and Lambda functions — all with full control over IP ranges, subnets, routing, and firewall rules.

A VPC is like your **own private data center inside AWS**.

---

## Why should I care?

Almost every AWS architecture — even serverless — touches a VPC.  
You need to understand VPCs to:

- Control **network-level access** to your services
- Connect **securely to the internet or your on-prem network**
- Deploy resources in **public vs private subnets**
- Use security groups and network ACLs for **firewall-like protection**

It’s also the key to **multi-tier architectures**, **hybrid connectivity**, and **VPC peering** between apps.

---

## When to use it

Always — VPCs are the **default networking environment** in AWS.

Use your knowledge of VPCs when:

- Deciding **where to place** EC2, RDS, Lambda, etc.
- Designing **private/public subnet separation**
- Setting up **NAT gateways** for outbound internet access
- Connecting to on-prem using VPN or Direct Connect
- Enabling secure, isolated environments for dev/test/prod

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **EC2, RDS, Lambda, ECS** | Deployed inside a VPC |
| **Security Groups / NACLs** | Act as firewalls for instances and subnets |
| **NAT Gateway / Internet Gateway** | Control internet access from inside the VPC |
| **VPC Peering / Transit Gateway** | Allow cross-VPC communication |
| **AWS PrivateLink** | Secure access to services without using public IPs |
| **Route Tables / Subnets** | Core building blocks of VPC routing logic |

---

## Learn More

- 📘 [VPC Documentation](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)  
- 🎥 [VPC Overview Video](https://www.youtube.com/watch?v=9Y9KVcYm2z0)  
- 💵 [VPC Pricing](https://aws.amazon.com/vpc/pricing/) *(mostly free unless using NAT Gateway or PrivateLink)*

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)
