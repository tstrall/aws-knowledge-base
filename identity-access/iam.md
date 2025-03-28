# AWS Identity and Access Management (IAM)

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Associate (ML)  
> ✅ Machine Learning – Specialty (MLS-C01)

---

## What is it?

AWS Identity and Access Management (IAM) is the core service for managing **who can do what in your AWS environment**. It lets you define:

- **Users**: for individual human access
- **Roles**: for machines, services, and federated users
- **Groups**: to manage permissions in bulk
- **Policies**: documents that define what’s allowed or denied

IAM controls access to **every AWS resource**.

---

## Why should I care?

IAM is **foundational to security and architecture** in AWS. Everything else relies on it.

IAM lets you:

- Grant or restrict access to AWS services
- Assign least privilege to users and workloads
- Securely delegate access between services (e.g., Lambda assuming a role)
- Enable cross-account access
- Support identity federation (e.g., corporate SSO via IAM Identity Center)

---

## When to use it

Always. IAM is not optional.

Use it to:

- Define **fine-grained permissions** for services and actions
- Assign temporary, scoped credentials to applications or users
- **Audit access** using CloudTrail
- Manage **multi-account access** using roles and trust relationships

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **STS (Security Token Service)** | Issues temporary credentials for assumed roles |
| **IAM Access Analyzer** | Detects risky or unintended access in policies |
| **IAM Identity Center (formerly SSO)** | Central identity source across multiple AWS accounts |
| **AWS Organizations** | Uses service control policies (SCPs) in addition to IAM |
| **CloudTrail** | Logs all IAM-related API activity for auditing |

---

## Learn More

- 📘 [IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)  
- 💵 IAM is free — no additional cost  
- 🎥 [AWS IAM Explained](https://www.youtube.com/watch?v=jkCqpNQSSog)

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)  
- [CHECKLIST_DEV.md](../CERTIFICATION_GUIDES/CHECKLIST_DEV.md)  
- [CHECKLIST_ML-Associate.md](../CERTIFICATION_GUIDES/CHECKLIST_ML-Associate.md)  
- [CHECKLIST_ML-Specialty.md](../CERTIFICATION_GUIDES/CHECKLIST_ML-Specialty.md)
