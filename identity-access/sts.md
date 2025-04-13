# AWS Security Token Service (STS)

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**AWS Security Token Service (STS)** is a web service that enables you to request temporary, limited-privilege credentials for AWS Identity and Access Management (IAM) users or federated users. These temporary credentials consist of an access key ID, a secret access key, and a security token, and they are valid for a specified duration, ranging from a few minutes to several hours. STS is commonly used to grant secure, short-term access to AWS resources without the need to create permanent IAM users.

---

## Why should I care?

Using AWS STS provides several benefits:

- **Enhanced Security**: Temporary credentials reduce the risk associated with long-term credentials, as they automatically expire after a set period.
- **Flexibility**: You can grant access to AWS resources without creating permanent IAM users, which is especially useful for external users or applications.
- **Simplified Credential Management**: There's no need to rotate or revoke credentials manually; they expire automatically.
- **Support for Federated Users**: STS allows integration with external identity providers, enabling single sign-on (SSO) and federated access.

---

## When to use it

Consider using AWS STS in the following scenarios:

- **Cross-Account Access**: Grant users in one AWS account temporary access to resources in another account.
- **Federated Access**: Allow users authenticated by external identity providers (e.g., Active Directory, Google, Facebook) to access AWS resources.
- **Temporary Elevated Permissions**: Provide users with temporary access to perform specific tasks without granting permanent permissions.
- **Applications Running on EC2**: Assign IAM roles to EC2 instances, allowing applications to access AWS resources securely without embedding credentials.

---

## Key features

- **Temporary Credentials**: Generate credentials that are valid for a limited time (from 15 minutes up to 12 hours).
- **AssumeRole API**: Allow users to assume roles and obtain temporary credentials with specified permissions.
- **Federation Support**: Integrate with external identity providers using SAML 2.0 or OpenID Connect (OIDC).
- **Session Tags**: Pass session-specific information for attribute-based access control.
- **MFA Support**: Enforce multi-factor authentication when assuming roles.

---

## Common use cases

- **Single Sign-On (SSO)**: Enable users to access AWS resources using existing corporate credentials.
- **Cross-Account Access**: Allow users or services in one AWS account to access resources in another account securely.
- **Mobile and Web Applications**: Provide temporary credentials to applications, reducing the need to store long-term credentials.
- **Third-Party Access**: Grant external partners or vendors temporary access to specific AWS resources.

---

## Integrations

- **IAM Roles**: Define roles with specific permissions that can be assumed using STS.
- **Amazon Cognito**: Manage user authentication and provide temporary credentials for mobile and web applications.
- **AWS SDKs and CLI**: Use built-in support to request and use temporary credentials.
- **External Identity Providers**: Integrate with SAML 2.0 or OIDC-compatible identity providers for federated access.

---

## Example: Using AssumeRole with AWS CLI

To assume a role using the AWS CLI and obtain temporary credentials:

```bash
aws sts assume-role \
  --role-arn arn:aws:iam::123456789012:role/ExampleRole \
  --role-session-name ExampleSession
```




This command returns temporary security credentials (AccessKeyId, SecretAccessKey, SessionToken) that you can use to access AWS resources with the permissions defined in the assumed role.

---

## Learn More

- [Temporary security credentials in IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp.html)
- [AssumeRole API Reference](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html)
- [Using IAM Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)
- [Identity providers and federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers.html)
