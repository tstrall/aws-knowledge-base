# IAM Trust Policies

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ DevOps Engineer – Professional (DOP)

---

## What is it?

An **IAM trust policy** defines **who (which principal) can assume a role** in AWS. Unlike permission policies, which define **what** an identity can do, trust policies define **who can use the role**.

Trust policies are required for **IAM roles** and are written in JSON using the same policy syntax as permission policies. They are attached to the **role itself**, not the principal.

---

## Why should I care?

Trust policies are essential for:

- **Cross-account access** – Allow principals from one AWS account to assume a role in another.
- **Federated access** – Allow external identities (e.g., Cognito, SAML, OIDC) to assume roles.
- **Service roles** – Allow AWS services (e.g., Lambda, EC2) to assume a role on your behalf.
- **Delegation** – Enable secure and auditable access across systems.

Trust policies are foundational to understanding **role assumption**, especially in automation and multi-account environments.

---

## When to use it

Use trust policies when:

- Creating any **IAM role** (service role, cross-account, federated).
- You want to let **EC2, Lambda, or other AWS services** assume a role.
- Granting **a user or role in another AWS account** permission to access your resources.
- Setting up **federated access** using Cognito, SAML, or custom identity providers.

---

## Key concepts

- **Principal** – The AWS entity allowed to assume the role (e.g., user, role, service).
- **Action** – Must be `sts:AssumeRole`, `sts:AssumeRoleWithWebIdentity`, or `sts:AssumeRoleWithSAML`.
- **Condition** – Optional conditions (e.g., on IP address, source VPC, MFA).

---

## Example: EC2 role trust policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "Service": "ec2.amazonaws.com" },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

---

## Example: Cross-account trust policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::123456789012:role/ExternalRole" },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

---

## Common use cases

- **Service roles** – Allow Lambda, ECS, or EC2 to perform tasks on your behalf.
- **Delegation** – Let other accounts or org units assume a role in your account.
- **Federation** – Authenticate users via identity providers like Google or Okta.
- **IAM Identity Center** – Backend mechanism for temporary credentials and role assumption.

---

## Integrations

- **IAM roles** – Trust policies are required for every role.
- **STS** – Role assumption happens through the AWS Security Token Service.
- **Organizations** – Simplify trust setup with org paths (`aws:PrincipalOrgID` condition).
- **CloudTrail** – Logs `AssumeRole` events for auditing.

---

## Learn More

- [IAM Trust Policies Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_manage_modify.html)
- [Understanding AWS STS](https://docs.aws.amazon.com/STS/latest/APIReference/Welcome.html)
- [Federated Users and Identity Providers](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers.html)
- [Cross-Account Access with Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_aws-accounts.html)
