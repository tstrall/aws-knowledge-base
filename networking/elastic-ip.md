# Elastic IPs

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

An **Elastic IP address (EIP)** is a **static, public IPv4 address** that you can allocate in AWS and associate with EC2 instances or network interfaces. It allows you to maintain a consistent public IP address **even when underlying infrastructure changes**, such as stopping/restarting an instance.

Elastic IPs are managed independently from your EC2 instances and can be remapped quickly for **failover or recovery scenarios**.

---

## Why should I care?

Elastic IPs provide **flexibility, control, and continuity**:

- **Consistent public endpoints** – Useful for DNS, firewall rules, or external integrations.
- **Manual failover support** – Quickly reassign to standby instances.
- **Infrastructure decoupling** – Public IP isn’t tied to a specific instance lifecycle.
- **Vital for legacy or manually managed architectures** where DNS or dynamic IPs aren’t practical.

---

## When to use it

Use an Elastic IP when:

- You need a **fixed public IP** for an EC2 instance that may stop/start.
- You want to implement **manual or scriptable failover** between instances.
- You are using **on-prem firewall rules or DNS** that require stable IP addresses.
- You’re building **hybrid environments** that expect a known external endpoint.

---

## Key features

- **Static allocation** – Remains yours until you release it.
- **Fast reassignment** – Switch between instances or ENIs in seconds.
- **Integration with ENIs** – Attach directly to network interfaces for more control.
- **Regional scope** – EIPs are allocated per region and must be used within that region.
- **Charges apply when unused** – Encourages efficient resource usage.

---

## Common use cases

- **Web servers or APIs** with whitelisted IPs.
- **VPN endpoints** requiring fixed IPs on both sides.
- **Disaster recovery** – Point DNS or traffic to standby EC2 in another AZ.
- **Remote SSH access** when DNS isn’t used.
- **Legacy systems** that require fixed source/destination IPs.

---

## Integrations

- **Amazon EC2** – Assign EIP to an instance or launch template.
- **Elastic Network Interfaces (ENIs)** – Use EIPs at the network level for high-availability setups.
- **Route 53 / DNS** – Use with static DNS mappings.
- **AWS Auto Scaling / Lambda** – Not typically used; dynamic services handle IP differently.

---

## Pricing

Elastic IPs are **free when associated with a running EC2 instance**, but incur charges when:

- Allocated but **not associated**.
- Associated with a **stopped instance**.
- **More than one** EIP is associated with the same instance.

[Pricing details →](https://aws.amazon.com/ec2/pricing/on-demand/#Elastic_IP_Addresses)

---

## Learn More

- [Elastic IP Addresses (EC2 Docs)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)
- [Managing EIPs in the Console](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip-console.html)
- [Using EIPs with ENIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
- [Best Practices for Public IPs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-ip-addressing.html#vpc-eips)
