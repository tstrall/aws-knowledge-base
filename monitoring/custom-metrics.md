# Custom CloudWatch Metrics

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Custom CloudWatch metrics** allow you to publish application- or business-specific data to Amazon CloudWatch. This enables monitoring of metrics not provided by AWS services, such as memory usage, disk space, or custom application KPIs.

---

## Why should I care?

AWS services emit standard metrics (e.g., CPUUtilization for EC2), but they don't cover everything. Custom metrics let you:

- Monitor internal application states (e.g., queue length, user signups).
- Track on-premises or hybrid workloads.
- Create fine-grained dashboards and alarms tailored to your business.

This is especially useful for observability in serverless, containerized, or hybrid environments.

---

## When to use it

Use custom metrics when:

- You need to monitor metrics not available by default (e.g., memory, disk usage).
- You're tracking business KPIs like revenue, conversion rate, or user engagement.
- You want to set alarms on application-specific thresholds.
- You're integrating monitoring across hybrid or multi-cloud environments.

---

## Key features

- **Namespace**: Logical container for your metrics (e.g., `MyApp/Metrics`).
- **Dimensions**: Key-value pairs to filter and categorize metrics (e.g., `InstanceId`, `Environment`).
- **Resolution**:
  - **Standard**: 1-minute granularity.
  - **High-resolution**: 1-second granularity (higher cost).
- **Units**: Specify units like `Count`, `Percent`, `Seconds`, etc.
- **Statistic Sets**: Aggregate multiple data points into a single submission to reduce API calls.

---

## Common use cases

- **EC2 Monitoring**: Track memory and disk usage using the CloudWatch Agent.
- **Application Metrics**: Monitor custom KPIs like transaction counts or error rates.
- **On-Premises Systems**: Integrate metrics from non-AWS environments.
- **Business Analytics**: Track metrics like revenue, user engagement, or conversion rates.

---

## Integrations

- **CloudWatch Agent**: Collect system-level metrics from EC2 or on-premises servers.
- **AWS SDKs/CLI**: Programmatically publish metrics using `PutMetricData`.
- **Lambda Functions**: Emit metrics during function execution.
- **Third-Party Tools**: Integrate with monitoring tools like Datadog, Prometheus, or custom scripts.

---

## Example: Publishing a Custom Metric via AWS CLI

```bash
aws cloudwatch put-metric-data \
  --namespace "MyApp/Metrics" \
  --metric-name "PageLoadTime" \
  --dimensions "Page=Home" \
  --unit "Milliseconds" \
  --value 350
```


This command publishes a `PageLoadTime` metric under the `MyApp/Metrics` namespace with a value of 350 milliseconds for the "Home" page.

---

## Pricing

Custom metrics are charged per metric per month. As of the latest pricing:

- $0.30 per metric per month for the first 10,000 metrics.
- Volume discounts apply beyond 10,000 metrics.

High-resolution metrics (1-second granularity) incur additional charges.

For detailed pricing, refer to the [Amazon CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/) page.

---

## Learn More

- [Publishing Custom Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html)
- [CloudWatch Agent Configuration](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html)
- [AWS CLI put-metric-data Command](https://docs.aws.amazon.com/cli/latest/reference/cloudwatch/put-metric-data.html)
- [CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/)
