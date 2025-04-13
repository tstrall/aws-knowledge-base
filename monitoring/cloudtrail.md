# AWS CloudTrail

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

**AWS CloudTrail** is a service that **records API activity and account-level actions** across your AWS environment. It captures details like **who did what, when, and from where**, including both **console actions** and **programmatic calls** via the CLI, SDKs, or services.

CloudTrail helps you enable **governance, compliance, operational auditing, and security analysis**.

---

## Why should I care?

CloudTrail provides a **complete audit trail** of all activity in your AWS account:

- **Track changes** – Who launched, deleted, or modified a resource.
- **Investigate incidents** – See exactly what actions were taken and by whom.
- **Audit compliance** – Satisfy regulatory requirements (PCI, HIPAA, SOC).
- **Security detection** – Find unusual or unauthorized behavior.
- **Automate alerting** – Route events to CloudWatch or EventBridge for response.

It’s foundational for any secure, well-managed AWS environment.

---

## When to use it

Use CloudTrail when:

- You need to audit AWS account activity.
- You want to detect unauthorized access or privilege escalation.
- You're responding to a security event or outage.
- You're implementing a compliance program.
- You need to trigger automation based on sensitive API actions.

---

## Key features

- **Event history** – View the last 90 days of management events in the console.
- **Trails** – Configure multi-region or single-region delivery to S3.
- **Data events** – Track access to S3 objects, Lambda invocations, DynamoDB reads/writes, etc.
- **Insights** – Detect unusual API activity (e.g., spikes in access or errors).
- **Integration with CloudWatch Logs** – Stream events to logs for alerting or analysis.
- **EventBridge support** – Trigger automation based on specific API calls.
- **Org trails** – Apply trails across all accounts in an AWS Organization.

---

## Common use cases

- **Security auditing** – Detect root user logins, IAM policy changes, security group updates.
- **Operational troubleshooting** – Understand who terminated an EC2 instance or modified a load balancer.
- **Compliance enforcement** – Retain long-term logs in S3 with encryption and versioning.
- **Forensic analysis** – Respond to incidents with a full event timeline.
- **Automated response** – Trigger Lambda functions on sensitive actions (e.g., S3 policy changes).

---

## Integrations

- **Amazon S3** – Store logs durably and securely.
- **AWS Key Management Service (KMS)** – Encrypt CloudTrail logs.
- **CloudWatch Logs** – Send logs for alerting and pattern analysis.
- **Amazon Athena** – Query logs using SQL directly from S3.
- **AWS Lake Formation / Glue** – Catalog and analyze CloudTrail data at scale.
- **AWS Organizations** – Enable organizational trails for centralized governance.

---

## Pricing

- **Management events**: First copy is free for 90 days in Event history.
- **Trails to S3**: Free for management events (1 copy per region); charges for additional copies, data events, and insights.
- **Data events**: Charged per event recorded (e.g., S3 object-level actions).
- **Insights**: Additional cost based on anomaly detection usage.

[Pricing details →](https://aws.amazon.com/cloudtrail/pricing/)

---

## Learn More

- [CloudTrail Documentation](https://docs.aws.amazon.com/cloudtrail/)
- [Viewing Event History](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events.html)
- [Creating a Trail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-create-and-update-a-trail.html)
- [CloudTrail Insights](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-insights.html)
- [EventBridge + CloudTrail](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-cloudtrail.html)
