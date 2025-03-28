# AWS Security Hub

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)

---

## What is it?

AWS Security Hub is a centralized service that aggregates and prioritizes security findings from multiple AWS services and third-party tools. It gives you a single dashboard to **view, analyze, and respond to security issues** across your AWS accounts and regions.

It automatically runs security checks based on AWS best practices (e.g., CIS benchmarks).

---

## Why should I care?

Without Security Hub, you'd have to review findings in multiple services like:

- GuardDuty (threat detection)
- Macie (sensitive data discovery)
- Inspector (vulnerability scans)
- Firewall Manager (rule enforcement)

Security Hub brings all these into one place, letting you:

- Monitor and prioritize findings in a unified view
- Enable **automated response** using EventBridge rules
- Check compliance against **security standards** (CIS, PCI DSS, etc.)
- Use **delegated admin** to manage org-wide visibility

---

## When to use it

Use Security Hub when:

- You need a **central view of security posture** across multiple AWS accounts
- You use GuardDuty, Macie, Inspector, or third-party integrations
- You're implementing security automation
- You're preparing for compliance audits or reviews

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **GuardDuty** | Feeds threat detections into Security Hub |
| **Macie** | Shares sensitive data findings |
| **Inspector** | Contributes vulnerability assessments |
| **Firewall Manager** | Helps assess rule compliance |
| **AWS Organizations** | Enables central management via delegated admin |
| **Amazon EventBridge** | Triggers automated remediation from findings |

---

## Learn More

- 📘 [Security Hub Documentation](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)  
- 💵 [Security Hub Pricing](https://aws.amazon.com/security-hub/pricing/)  
- 🎥 [Overview Video](https://www.youtube.com/watch?v=uejcLWX5xgA)

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)
