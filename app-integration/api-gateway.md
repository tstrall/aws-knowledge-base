# Amazon API Gateway

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Amazon API Gateway** is a fully managed service that allows you to create, publish, maintain, monitor, and secure APIs at any scale. It acts as the **front door** to your backend services—such as Lambda functions, EC2 instances, or any publicly addressable endpoint.

It supports both **RESTful APIs** and **WebSocket APIs**, making it suitable for request-response and real-time communication patterns.

---

## Why should I care?

API Gateway is a central component in many AWS-based applications:

- **Serverless integration** – Works seamlessly with AWS Lambda for event-driven apps.
- **Centralized routing** – Exposes your backend via stable URLs and versioned endpoints.
- **Built-in security** – Supports IAM, Cognito, API keys, usage plans, and custom authorizers.
- **Throttling and rate limiting** – Protects your backend from abuse or spikes.
- **Monitoring** – Native integration with CloudWatch for metrics, logging, and tracing.

It simplifies API lifecycle management and enforces best practices by default.

---

## When to use it

Use API Gateway when:

- You need a **public or private API layer** in front of services like Lambda, ECS, EC2, or HTTP endpoints.
- You want **authentication, caching, throttling, and monitoring** in a central place.
- You’re building **mobile, web, or IoT** applications that require secure API access.
- You want to enable **versioning** and stage-based deployments (e.g., `dev`, `prod`).
- You need to **scale APIs automatically** with minimal operational overhead.

---

## Key features

- **REST APIs** – Traditional HTTP-based APIs with request/response patterns.
- **HTTP APIs** – Lower-latency and lower-cost alternative to REST APIs (limited features).
- **WebSocket APIs** – Bi-directional, event-based APIs for real-time apps.
- **Authentication** – Supports IAM, Cognito user pools, Lambda authorizers, and API keys.
- **Request/response transformation** – Modify payloads between client and backend.
- **Usage plans** – Rate-limit or throttle clients based on API key.
- **Monitoring & logging** – Full CloudWatch integration including logs and latency metrics.
- **Deployment stages** – Deploy different versions to environments like dev, test, and prod.

---

## Common use cases

- **Serverless apps** – API Gateway → Lambda → DynamoDB/S3.
- **Microservices gateway** – Central API routing for backend services.
- **Public or third-party APIs** – Expose services with throttling and monetization.
- **WebSocket chat apps** – Real-time, persistent connections for collaboration tools or dashboards.
- **Request transformation** – Reshape incoming or outgoing JSON payloads.

---

## Integrations

- **AWS Lambda** – Most common backend target for serverless APIs.
- **Amazon Cognito** – Manage API authentication for mobile/web users.
- **CloudWatch** – Monitor metrics and create alarms.
- **WAF** – Protect APIs from common web exploits (e.g., SQLi, XSS).
- **Route 53** – Custom domain name management.
- **AWS X-Ray** – Trace full request lifecycle through backend systems.

---

## Pricing

You pay per:

- **API calls** (based on type: REST, HTTP, WebSocket)
- **Data transferred out**
- **Optional features** like caching and custom domains

HTTP APIs are more cost-effective than REST APIs for most use cases.

[Pricing details →](https://aws.amazon.com/api-gateway/pricing/)

---

## Learn More

- [API Gateway Developer Guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)
- [Choosing Between HTTP and REST APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html)
- [API Gateway + Lambda Tutorial](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-getting-started-with-rest-apis.html)
- [Monitoring APIs with CloudWatch](https://docs.aws.amazon.com/apigateway/latest/developerguide/set-up-monitoring.html)
