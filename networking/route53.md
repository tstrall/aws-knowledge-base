# Amazon Route 53

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

**Amazon Route 53** is a **highly available and scalable Domain Name System (DNS) web service**. It translates human-friendly domain names (e.g., `example.com`) into IP addresses and supports routing traffic to AWS and external resources using intelligent routing policies.

Route 53 also supports **domain registration** and **health checks** for routing decisions.

---

## Why should I care?

Route 53 is core to **global routing, custom domain hosting, and resilient architecture**:

- **Scalable DNS** – Ultra-low-latency name resolution worldwide.
- **Custom domain support** – For websites, APIs, and services on AWS.
- **Smart routing policies** – Latency-based, weighted, geolocation, and failover.
- **Tight AWS integration** – Easily map domain names to S3, CloudFront, API Gateway, or ALB.
- **Global health checking** – Redirect traffic away from unhealthy endpoints.

---

## When to use it

Use Route 53 when:

- You’re hosting **a public website, app, or API** with a custom domain.
- You want **low-latency, global DNS** with AWS-native features.
- You need **routing control** based on location, latency, or health.
- You’re implementing **multi-region or multi-endpoint failover**.
- You want to **register or transfer a domain** via AWS.

---

## Key features

- **Hosted zones** – Containers for DNS records in a domain.
- **Record types** – A, AAAA, CNAME, MX, TXT, NS, PTR, etc.
- **Alias records** – Point to AWS resources (e.g., CloudFront, ELB) with zero cost.
- **Routing policies**:
  - *Simple* – Default DNS response
  - *Failover* – Route based on endpoint health
  - *Weighted* – Split traffic for A/B testing or traffic shifting
  - *Latency-based* – Route to region with lowest latency
  - *Geolocation / Geoproximity* – Route based on user’s location
  - *Multivalue answer* – Return multiple healthy IPs (basic round-robin + health check)
- **Domain registration** – Manage your domain directly in Route 53.

---

## Common use cases

- **Web hosting** – Serve `example.com` from S3 or EC2 with public DNS.
- **Global application routing** – Use latency-based routing across AWS regions.
- **Disaster recovery** – Implement active-passive routing with health checks and failover.
- **SaaS and multi-tenant apps** – Manage subdomain routing (e.g., `tenant1.example.com`).
- **Hybrid DNS** – Combine Route 53 for public domains with Route 53 Resolver for private DNS.

---

## Integrations

- **Amazon S3 / CloudFront / ALB / API Gateway** – Use Alias records to route traffic.
- **AWS Certificate Manager (ACM)** – Use DNS validation for SSL/TLS certificates.
- **AWS Lambda / Step Functions** – Trigger automation based on DNS state or traffic shifts.
- **Amazon CloudWatch** – Monitor health checks and set alarms.
- **Route 53 Resolver** – Extend DNS resolution to on-prem or hybrid cloud networks.

---

## Pricing

You pay for:

- **Hosted zones** (per month)
- **DNS queries** (per million)
- **Health checks** (per check + queries)
- **Domain registration** (optional; priced per TLD)

[Pricing details →](https://aws.amazon.com/route53/pricing/)

---

## Learn More

- [Route 53 Documentation](https://docs.aws.amazon.com/route53/)
- [Routing Policy Types](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html)
- [Using Alias Records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-elb-load-balancer.html)
- [Domain Registration Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html)
- [Route 53 Resolver](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/route-53-resolver.html)
