# Amazon Cognito

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Machine Learning – Specialty (MLS-C01)

---

## What is it?

**Amazon Cognito** is a fully managed service that provides authentication, authorization, and user management for web and mobile applications. It supports both user directory management and federated identity, allowing users to sign in directly or through third-party identity providers.

---

## Why should I care?

Cognito simplifies the implementation of secure user sign-up, sign-in, and access control, enabling you to:

- **Manage user directories** with customizable sign-up and sign-in experiences.
- **Authenticate users** via social identity providers (e.g., Google, Facebook) or enterprise identity providers using SAML or OIDC.
- **Authorize access** to AWS services by assigning roles to users, facilitating fine-grained access control.
- **Enhance security** with features like multi-factor authentication (MFA), passwordless login, and adaptive authentication.

---

## When to use it

Use Amazon Cognito when:

- You need to **add user authentication** to your application without building it from scratch.
- You want to **federate identities** from social or enterprise identity providers.
- You require **secure access control** to AWS resources based on user identity.
- You're building **serverless applications** and need seamless integration with AWS services.

---

## Key features

- **User Pools**: Manage user directories and authentication flows.
- **Identity Pools**: Grant users access to AWS services via temporary credentials.
- **Federated Identities**: Support for social and enterprise identity providers.
- **Security Features**: MFA, adaptive authentication, compromised credential detection.
- **Customization**: Lambda triggers for custom workflows and user migration.
- **Scalability**: Handles millions of users with high availability.

---

## Common use cases

- **Web and mobile app authentication**: Implement user sign-up and sign-in flows.
- **Federated access**: Allow users to sign in using existing identities (e.g., Google, Facebook).
- **Access control**: Assign roles to users for accessing AWS resources like S3 or DynamoDB.
- **Serverless applications**: Integrate with services like API Gateway and Lambda for secure backend access.

---

## Integrations

- **AWS Lambda**: Customize authentication flows with triggers.
- **API Gateway**: Use Cognito authorizers for securing APIs.
- **AWS IAM**: Define roles and permissions for authenticated users.
- **AWS Amplify**: Simplify front-end integration with Cognito.

---

## Pricing

- **User Pools**: Free for up to 50,000 monthly active users (MAUs) for users signing in directly or through social identity providers. Beyond that, pricing is tiered based on MAUs.
- **Federated Identities**: Free for up to 50 MAUs for SAML or OIDC federated users; additional usage incurs charges.

[Pricing details →](https://aws.amazon.com/cognito/pricing/)

---

## Learn More

- [Amazon Cognito Documentation](https://docs.aws.amazon.com/cognito/)
- [Authentication and Authorization with Amazon Cognito](https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-net-applications-security/cognito.html)
- [AWS Cognito Developer Guide](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html)
