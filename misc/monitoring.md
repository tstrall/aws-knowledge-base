# Monitoring & Observability

**What it is:**
- Monitoring is the collection and analysis of system metrics to understand health and performance
- Observability is the broader discipline of understanding **what's happening inside a system** based on its external outputs (metrics, logs, traces)

---

## Core Pillars of Observability

| Pillar   | Description |
|----------|-------------|
| **Metrics** | Numeric time-series data (e.g., CPU, request latency) |
| **Logs**    | Structured/unstructured text output (e.g., errors, events) |
| **Traces**  | Distributed request tracking across services |

---

## Metrics: Prometheus + Grafana

**Prometheus**:
- Pull-based metrics scraping (via HTTP endpoint)
- Uses PromQL (query language)
- Stores time-series data in TSDB (time series DB)

```yaml
# Sample Prometheus scrape config
scrape_configs:
  - job_name: 'app'
    static_configs:
      - targets: ['localhost:9090']
```

**Grafana**:
- Visualization layer for Prometheus and other data sources
- Dashboards, alerts, panels

---

## Logs: Fluent Bit / CloudWatch / Loki / ELK

- **Fluent Bit**: Lightweight log forwarder
- **CloudWatch Logs**: AWS-native logging with retention and alerts
- **Loki**: Grafana’s log aggregation tool, designed to pair with Prometheus
- **ELK Stack**: Elasticsearch, Logstash, Kibana (popular log analysis stack)

Best practices:
- Use structured logs (JSON)
- Include request IDs and timestamps
- Log at appropriate levels (info, warn, error)

---

## Traces: OpenTelemetry + Jaeger / X-Ray

- **OpenTelemetry**: Open standard for distributed tracing
- **Jaeger**: Visualization and analysis UI for traces
- **AWS X-Ray**: AWS-native tracing and profiling tool

Trace fields:
- Trace ID, span ID, service name, duration, error status

---

## SaaS Observability Tools: Datadog vs Alternatives

| Tool       | Notes |
|------------|-------|
| **Datadog** | All-in-one SaaS (metrics, logs, traces, RUM, Synthetics); powerful but pricey |
| **New Relic** | Similar full-stack platform; strong APM features |
| **Dynatrace** | Enterprise-oriented; heavy on AI-driven anomaly detection |
| **Grafana Cloud** | Hosted Prometheus, Loki, and Tempo; cheaper, open-source focused |
| **Elastic Observability** | Based on ELK; self-host or Elastic Cloud |
| **Lightstep** | Strong tracing focus; good for microservices |
| **AWS-native** | CloudWatch, X-Ray, CloudTrail; tightly integrated but limited UX |

**Considerations:**
- **Cost scaling:** Datadog and New Relic get expensive fast at scale
- **Customization:** Prometheus/Grafana wins for control, but requires more setup
- **Compliance:** Some prefer managed solutions for audit or SOC2 compliance
- **Vendor lock-in:** Self-hosted tools can be swapped more easily

---

## Alerting Best Practices
- Avoid noisy alerts (focus on SLO/SLA violations)
- Group and route alerts by severity
- Integrate with Slack, PagerDuty, etc.
- Track alert history and suppression conditions

---

## Interview Tips
- Know the difference between monitoring and observability
- Explain how you'd monitor a microservice (app metrics, health checks, logs, traces)
- Be able to discuss Grafana dashboards, PromQL filters, or troubleshooting using traces
- Describe incident workflows and how monitoring helped
