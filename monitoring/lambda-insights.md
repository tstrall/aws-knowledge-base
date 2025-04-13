# Lambda Insights

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)

---

## What is it?

**Lambda Insights** is a feature of Amazon CloudWatch that provides enhanced monitoring and troubleshooting for AWS Lambda functions. It collects and aggregates system-level metrics such as CPU time, memory usage, disk, and network activity. Additionally, it gathers diagnostic information like cold starts and Lambda worker shutdowns, helping you isolate and resolve issues with your Lambda functions efficiently. citeturn0search0

---

## Why should I care?

While AWS Lambda provides basic metrics like invocation count and duration, Lambda Insights offers deeper visibility into your functions' performance. It enables you to:

- Monitor resource utilization (CPU, memory, disk, network) to optimize function performance.
- Identify and troubleshoot issues such as cold starts and execution bottlenecks.
- Gain insights into function behavior over time, facilitating better scaling and cost management decisions.

---

## When to use it

Consider using Lambda Insights when:

- You require detailed performance metrics beyond standard Lambda monitoring.
- You're troubleshooting complex issues or performance anomalies in your serverless applications.
- You need to optimize resource allocation for cost efficiency.
- You're monitoring functions with variable workloads and want to ensure consistent performance.

---

## Key features

- **System-level metrics**: CPU time, memory usage, disk I/O, and network activity.
- **Diagnostic information**: Cold starts, Lambda worker shutdowns, and other execution details.
- **Enhanced dashboards**: Multi-function and single-function views in CloudWatch for comprehensive monitoring.
- **Integration with CloudWatch Logs**: Embedded metric formatting allows for detailed log analysis.
- **Support for various runtimes**: Compatible with runtimes that support Lambda extensions. citeturn0search0

---

## Common use cases

- **Performance optimization**: Analyze resource usage to fine-tune function configurations.
- **Issue diagnosis**: Identify causes of increased latency or errors in function execution.
- **Capacity planning**: Understand usage patterns to plan for scaling and resource allocation.
- **Compliance and auditing**: Maintain detailed logs and metrics for regulatory requirements.

---

## Integrations

- **AWS Lambda**: Direct integration for enhanced monitoring.
- **Amazon CloudWatch**: Utilizes CloudWatch dashboards and Logs for visualization and analysis.
- **AWS X-Ray**: Provides trace data for in-depth performance analysis.
- **Infrastructure as Code tools**: Enable Lambda Insights via AWS CLI, CloudFormation, AWS SAM, or AWS CDK. citeturn0search2

---

## Example: Enabling Lambda Insights via AWS CLI

To enable Lambda Insights on an existing function:

```bash
aws lambda update-function-configuration \
  --function-name my-function \
  --layers arn:aws:lambda:<region>:580247275435:layer:LambdaInsightsExtension:<version> \
  --role arn:aws:iam::<account-id>:role/<execution-role>
```


Ensure that the execution role has the `CloudWatchLambdaInsightsExecutionRolePolicy` attached.

---

## Pricing

Lambda Insights charges are based on the metrics and logs collected:

- **Metrics**: Standard CloudWatch pricing applies.
- **Logs**: Charges are based on the volume of log data ingested and stored.

For detailed pricing information, refer to the [Amazon CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/) page.

---

## Learn More

- [CloudWatch Lambda Insights Overview](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Lambda-Insights.html)
- [Enabling Lambda Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Lambda-Insights-Getting-Started.html)
- [Lambda Insights Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Lambda-Insights-view-metrics.html)
