# Elastic Load Balancing (ELB)

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Developer – Associate (DVA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

Elastic Load Balancing (ELB) is a fully managed service that automatically distributes incoming application traffic across multiple targets (such as EC2 instances, containers, IPs, or Lambda functions) in one or more Availability Zones. It increases the fault tolerance, scalability, and availability of your applications.

There are three main types of load balancers:

- **Application Load Balancer (ALB)** – Operates at Layer 7 (HTTP/HTTPS), ideal for routing based on URL paths, hostnames, headers, or query strings.
- **Network Load Balancer (NLB)** – Operates at Layer 4 (TCP/UDP), built for extreme performance and low latency.
- **Gateway Load Balancer (GWLB)** – Designed for third-party virtual appliances like firewalls or packet inspection systems.

Classic Load Balancer (CLB) is legacy and not recommended for new architectures.

---

## Why should I care?

ELB is essential for building highly available and resilient applications:

- **Increases fault tolerance** by distributing traffic across multiple instances and AZs.
- **Improves scalability** by working seamlessly with Auto Scaling.
- **Supports microservices** by routing requests to containers or Lambda functions.
- **Handles SSL termination** and offloads encryption overhead from backend targets.
- **Deep AWS integration** makes it a go-to choice for most architectures.

Understanding the differences between ALB, NLB, and GWLB is critical for exams and real-world system design.

---

## When to use it

Use ELB when:

- You need to spread traffic across multiple backend instances or containers.
- You're deploying a scalable, multi-AZ application.
- You want to route HTTP(S) traffic based on paths or hostnames (use ALB).
- You need ultra-low latency, TCP-level routing, or static IPs (use NLB).
- You're inserting a virtual appliance into your traffic flow (use GWLB).
- You want built-in health checks, session stickiness, or automatic scaling.

---

## Key features

- **Health checks** – Automatically detect and remove unhealthy targets.
- **SSL termination** – Manage HTTPS certificates at the load balancer layer.
- **Sticky sessions** – Support session affinity using cookies.
- **Path-based and host-based routing** – Direct requests to different targets based on URL or hostname (ALB).
- **WebSockets and HTTP/2 support** – Available in ALB.
- **Static IPs / Elastic IPs** – Supported by NLB for predictable networking.
- **Zonal isolation** – ALB and NLB maintain traffic availability even during AZ outages.

---

## Common use cases

- **Web applications** – Route traffic to EC2 instances, containers, or Lambda functions.
- **Microservices** – Use ALB to route requests to services by path or hostname.
- **IoT or real-time systems** – Use NLB for high-throughput TCP/UDP traffic.
- **Virtual firewalls / middleboxes** – Use GWLB to scale security appliances.
- **Multi-tenant SaaS** – Route traffic by tenant domain using host-based routing.

---

## Integrations

- **EC2 / ECS / Lambda** – Register targets for routing.
- **Auto Scaling Groups** – Instances are added/removed automatically.
- **Certificate Manager (ACM)** – Easily manage TLS/SSL certificates.
- **WAF / Shield** – Add web security protections to ALBs.
- **CloudWatch** – Monitor request counts, latencies, error rates.

---

## Pricing

Pricing is based on:

- **Hours the load balancer is running**
- **Number of Load Balancer Capacity Units (LCUs) used**
- **Data processed through the load balancer**

Each load balancer type has its own pricing structure. ALB and NLB are billed differently based on their capabilities and use cases.

[Pricing details →](https://aws.amazon.com/elasticloadbalancing/pricing/)

---

## Learn More

- [Elastic Load Balancing Documentation](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html)
- [ALB vs NLB vs GWLB Comparison](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-types.html)
- [Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-target-groups.html)
- [Troubleshooting Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-troubleshooting.html)
