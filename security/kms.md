# AWS Key Management Service (KMS)

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Associate (ML)  
> ✅ Machine Learning – Specialty (MLS-C01)

---

## What is it?

AWS Key Management Service (KMS) is a fully managed service that enables you to create and control the cryptographic keys used to protect your data across AWS services and custom applications.

It supports **symmetric and asymmetric encryption**, **automatic key rotation**, and integration with **most AWS services**.

---

## Why should I care?

KMS is at the heart of AWS encryption. It lets you:

- Secure S3, EBS, RDS, DynamoDB, and Lambda data at rest
- Encrypt data directly using the KMS API or AWS SDK
- Automatically rotate keys and manage access
- Meet compliance standards (HIPAA, GDPR, PCI, etc.)

You’ll see KMS **everywhere** — if you encrypt data in AWS, it’s likely using KMS under the hood.

---

## When to use it

Use KMS when:

- You're storing **sensitive or regulated data**
- You want to control **who can decrypt or manage** a resource
- You need centralized key lifecycle management
- You want to encrypt data before storing it (client-side or server-side)

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **Amazon S3, EBS, RDS, DynamoDB** | All integrate with KMS for server-side encryption |
| **AWS Secrets Manager** | Uses KMS to encrypt secrets at rest |
| **AWS Lambda** | Can decrypt environment variables or payloads using KMS |
| **CloudTrail** | Can log access to KMS keys |
| **AWS Config** | Can monitor key rotation and usage compliance |

---

## Learn More

- [KMS Documentation](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html)  
- [KMS Pricing](https://aws.amazon.com/kms/pricing/)  
- [KMS Explained (AWS Video)](https://www.youtube.com/watch?v=XrPZSq5YXqc)

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)  
- [CHECKLIST_DEV.md](../CERTIFICATION_GUIDES/CHECKLIST_DEV.md)  
- [CHECKLIST_ML-Associate.md](../CERTIFICATION_GUIDES/CHECKLIST_ML-Associate.md)  
- [CHECKLIST_ML-Specialty.md](../CERTIFICATION_GUIDES/CHECKLIST_ML-Specialty.md)
