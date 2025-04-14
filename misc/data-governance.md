# Data Governance

**What it is:**
- A discipline that ensures high data quality, consistency, security, and usability across systems
- Involves people, processes, and tools to manage data assets effectively

---

## Key Pillars of Data Governance

| Pillar               | Description |
|----------------------|-------------|
| **Data Quality**     | Accuracy, completeness, consistency, validity of data |
| **Data Lineage**     | Track where data originates, how it transforms, and where it goes |
| **Metadata Management** | Manage business and technical context about data assets |
| **Access Control**   | Who can see or change what data, enforced by IAM, roles, policies |
| **Compliance**       | Legal and regulatory adherence (e.g., HIPAA, GDPR, FedRAMP) |
| **Data Stewardship** | Assigning accountability and responsibility for data |

---

## Common Practices

- **Schema Evolution Control**: Track changes to table or record formats
- **Data Contracts**: Formalized interfaces between producer and consumer teams
- **Validation Checks**: Pre-load, in-pipeline, and post-load integrity tests
- **Column-level Lineage**: Tooling to trace transformations on individual fields
- **Data Catalogs**: Tools like Amundsen, DataHub, Alation for discoverability

---

## Governance in Modern Data Stacks

| Component            | Role in Governance |
|----------------------|--------------------|
| **dbt**              | Documented models + source freshness checks |
| **Great Expectations / Deequ** | Data validation and testing |
| **Apache Atlas**     | Lineage, classification, and audit trail tooling |
| **AWS Glue Data Catalog** | Centralized metadata in AWS |
| **SSM / Secrets Manager** | Secure config and secret distribution |

---

## Governance Challenges
- Balancing agility vs control in data pipelines
- Maintaining lineage and traceability in distributed systems
- Managing schema drift in semi-structured sources (e.g., JSON logs)
- Scaling policies across business units

---

## Interview Tips
- Explain how you manage schema changes and notify downstream consumers
- Know the difference between data ownership and data stewardship
- Be able to talk about data validation in ETL/ELT workflows
- Highlight tools you’ve used for auditing, cataloging, or policy enforcement

Let me know if you'd like to expand with specific tools (e.g., DataHub setup, dbt contracts) or compliance-specific examples (HIPAA/GDPR handling).

