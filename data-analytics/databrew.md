# AWS Glue DataBrew

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Data Analytics – Specialty (DAS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**AWS Glue DataBrew** is a visual data preparation tool that enables users to clean and normalize data without writing code. With over 250 prebuilt transformations, it simplifies tasks such as filtering anomalies, converting data formats, and correcting invalid values. DataBrew is serverless, requiring no infrastructure management, and integrates seamlessly with various AWS services. citeturn0search1

---

## Why should I care?

- **No-Code Interface**: Empowers analysts and data scientists to prepare data without programming skills.
- **Time Efficiency**: Reduces data preparation time by up to 80% compared to manual coding.
- **Scalability**: Handles large datasets without the need to manage servers or clusters.
- **Integration**: Works with AWS services like S3, Redshift, RDS, and more.

---

## When to use it

- Preparing data for analytics or machine learning.
- Cleaning and transforming datasets from various sources.
- Collaborating across teams with varying technical expertise.
- Automating repetitive data preparation tasks.

---

## Key features

- **Projects**: Workspaces for data preparation activities.
- **Datasets**: Connections to data sources like S3, Redshift, and RDS.
- **Recipes**: Sequences of transformation steps that can be applied to datasets.
- **Jobs**: Scheduled or on-demand executions of recipes on full datasets.
- **Data Profiling**: Automatic generation of statistics to understand data quality.
- **Data Lineage**: Visualization of data transformations and flow.

---

## Common use cases

- **Data Cleaning**: Removing duplicates, handling missing values, and correcting errors.
- **Data Transformation**: Changing data formats, aggregating data, and deriving new columns.
- **Data Normalization**: Standardizing data to a common format or scale.
- **Data Enrichment**: Combining data from multiple sources to enhance datasets.

---

## Integrations

- **Amazon S3**: Input and output storage for datasets.
- **Amazon Redshift**: Data warehousing and analytics.
- **Amazon RDS**: Relational database services.
- **AWS Glue**: Orchestration of ETL workflows.
- **Amazon Athena**: Querying data in S3 using SQL.

---

## Example: Creating a DataBrew Project

1. **Access DataBrew Console**: Navigate to the AWS Glue DataBrew console.
2. **Create Project**: Click on "Projects" and then "Create project".
3. **Configure Project**:
   - **Name**: Enter a unique project name.
   - **Recipe**: Create a new recipe or select an existing one.
   - **Dataset**: Choose an existing dataset or create a new one by specifying the data source (e.g., S3 bucket).
   - **IAM Role**: Assign an IAM role with necessary permissions.
4. **Data Sampling**: Select sampling options (e.g., first N rows or random sampling) and sample size.
5. **Create Project**: Click "Create project" to launch the interactive session.

---

## Learn More

- [AWS Glue DataBrew Documentation](https://docs.aws.amazon.com/databrew/latest/dg/what-is.html)
- [Getting Started with DataBrew](https://docs.aws.amazon.com/databrew/latest/dg/getting-started.html)
- [AWS Glue DataBrew Features](https://aws.amazon.com/glue/features/databrew/)
- [AWS Glue DataBrew – AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/serverless-etl-aws-glue/databrew.html)
