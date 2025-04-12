# AWS WAF (Web Application Firewall)

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)

---

## What is it?

AWS WAF is a Web Application Firewall that protects web apps from common threats like:

- SQL injection
- Cross-site scripting (XSS)
- Bad bot traffic
- Malicious IPs or geographies

It lets you define **rules to allow, block, or monitor** (count) web requests based on conditions that you specify.

---

## Why should I care?

AWS WAF is critical for **layer 7 (application-level)** protection. It gives you:

- Fine-grained traffic control at the edge
- Mitigation of known OWASP Top 10 vulnerabilities
- Rate limiting to slow down DDoS attacks
- Integration with **CloudFront**, **API Gateway**, and **ALB**

Use it when you want to **control and inspect HTTP(S) traffic before it reaches your app**.

---

## When to use it

Use AWS WAF when:

- You're deploying public-facing APIs or websites
- You want to defend against injection, bots, or scrapers
- You need to **throttle** abusive users or IPs
- You want to apply rules **centrally** across multiple applications

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **Amazon CloudFront** | Deploy WAF at the edge for global coverage |
| **API Gateway** | Add protection to REST or HTTP APIs |
| **Application Load Balancer (ALB)** | Add WAF filtering before request reaches EC2/Lambda |
| **AWS Firewall Manager** | Centralize and automate WAF policy management across accounts |
| **AWS Shield** | WAF handles app-layer threats; Shield focuses on network-level DDoS protection |

---

## Learn More

- [WAF Documentation](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)  
- [WAF Pricing](https://aws.amazon.com/waf/pricing/)  
- [Intro to WAF Video](https://www.youtube.com/watch?v=bKM3c_BUBuE)

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)
