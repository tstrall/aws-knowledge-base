# Amazon CloudWatch

> Relevant for:  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ SysOps Administrator – Associate (SOA)  
> ✅ Developer – Associate (DVA)

---

## What is it?

Amazon CloudWatch is a **monitoring and observability service** for AWS resources and applications. It collects **metrics, logs, and events**, and lets you visualize data, trigger alarms, and respond to changes in your environment.

CloudWatch supports **real-time monitoring**, **dashboard creation**, and **automated responses** via alarms and EventBridge rules.

---

## Why should I care?

CloudWatch is essential for maintaining visibility into cloud infrastructure:

- **Detect issues quickly** using alarms and dashboards.
- **Automate responses** to state changes or anomalies.
- **Log everything centrally** (Lambda, EC2, VPC flow logs, RDS, custom apps).
- **Enable performance tuning** via detailed metrics and insights.
- **Foundation for DevOps and security operations**.

It’s a core service for AWS certifications, especially in high availability, monitoring, and automation scenarios.

---

## When to use it

Use CloudWatch when:

- You need to monitor performance or availability.
- You want to trigger alerts or automated actions based on metrics.
- You're debugging or auditing applications via logs.
- You’re building dashboards for system health or KPIs.
- You want to detect unusual behavior or forecast trends.

---

## Key features

- **Metrics** – Track usage, performance, and custom application data.
- **Logs** – Aggregate logs from Lambda, EC2, ECS, API Gateway, and more.
- **Alarms** – Trigger actions (SNS, Auto Scaling, EC2 reboot, etc.) on thresholds.
- **Dashboards** – Visualize system metrics and KPIs.
- **Log Insights** – Run structured queries on logs to troubleshoot and analyze trends.
- **Anomaly detection** – Learn baseline behavior and alert on outliers.
- **Composite alarms** – Combine multiple conditions into a single alert.
- **CloudWatch Agent** – Collect OS-level metrics and custom logs from EC2/on-prem servers.

---

## Common use cases

- **Lambda monitoring** – Duration, invocations, errors, throttles.
- **EC2 dashboards** – CPU, memory, disk usage (with agent).
- **Auto Scaling triggers** – Scale based on CPU, latency, queue depth, etc.
- **Security alerting** – Watch for unusual activity or brute-force attempts.
- **Application debugging** – Query logs with Log Insights during failures.
- **SLA enforcement** – Alert on performance degradation or downtime.

---

## Integrations

- **Amazon SNS** – Notify via email, SMS, Lambda, or webhook.
- **Auto Scaling / EC2** – Act on instance health or workload spikes.
- **EventBridge** – Route events to Lambda, Step Functions, SQS, etc.
- **AWS Lambda** – Send logs and metrics; trigger functions on alarms.
- **AWS Systems Manager** – Use metrics to trigger automation runbooks.
- **AWS X-Ray** – Correlate traces with logs for deep observability.

---

## Pricing

CloudWatch pricing is based on:

- **Metrics** (standard and high-resolution)
- **Log ingestion and retention**
- **Log Insights queries**
- **Dashboards (number of custom dashboards)**
- **Alarms and anomaly detection**

Some basic metrics (EC2, RDS, Lambda) are free; detailed and custom metrics incur charges.

[Pricing details →](https://aws.amazon.com/cloudwatch/pricing/)

---

## Learn More

- [Amazon CloudWatch Documentation](https://docs.aws.amazon.com/cloudwatch/index.html)
- [Using CloudWatch Alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)
- [CloudWatch Logs Insights Query Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html)
- [CloudWatch Agent Setup](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html)
- [Anomaly Detection](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Anomaly_Detection.html)
