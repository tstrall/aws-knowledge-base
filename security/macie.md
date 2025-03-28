# Amazon Macie

> 🔖 **Relevant for**:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Solutions Architect – Professional (SAP)  
> ✅ Machine Learning – Specialty (MLS-C01)

---

## What is it?

Amazon Macie is a fully managed data security and privacy service that uses machine learning and pattern matching to discover and protect sensitive data in Amazon S3 buckets. It’s especially useful for identifying personal data such as PII (e.g., names, addresses, credit card numbers).

---

## Why should I care?

If you're storing **sensitive or regulated data** in S3, Macie can help you:

- Automatically identify unencrypted or publicly accessible data
- Detect PII and other sensitive information at scale
- Stay ahead of compliance audits (HIPAA, GDPR, etc.)
- Monitor for new buckets and data drift over time

It helps reduce your **attack surface** and **regulatory risk** without needing to manually inspect every file.

---

## When to use it

Use Macie when:

- You manage large or dynamic sets of S3 data
- You need to identify where sensitive data is located across your buckets
- You want automated data classification to support compliance or auditing
- You're building a data governance program and want visibility into who can access what

---

## Related Services

| Service | How it connects |
|---------|------------------|
| **Amazon S3** | Macie scans your S3 objects directly |
| **AWS KMS** | Works with encrypted data (Macie decrypts using KMS, if it has permission) |
| **Amazon GuardDuty** | Both are part of the AWS security suite, but GuardDuty focuses on threats, not data classification |
| **Security Hub** | Can ingest Macie findings for central visibility |
| **AWS Organizations** | Macie supports delegated admin and multi-account scanning setups |

---

## Learn More

- 📘 [Macie Documentation](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)  
- 💵 [Macie Pricing](https://aws.amazon.com/macie/pricing/)  
- 📺 [AWS Macie Overview Video](https://www.youtube.com/watch?v=nk3yRfG7Rhk)

---

## Checklist Reference

- [CHECKLIST_SAA.md](../CERTIFICATION_GUIDES/CHECKLIST_SAA.md)  
- [CHECKLIST_SAP.md](../CERTIFICATION_GUIDES/CHECKLIST_SAP.md)  
- [CHECKLIST_ML-Specialty.md](../CERTIFICATION_GUIDES/CHECKLIST_ML-Specialty.md)
