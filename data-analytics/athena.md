# Amazon Athena

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)  
> ✅ Data Analytics – Specialty (DAS)

---

## What is it?

**Amazon Athena** is a serverless, interactive query service that allows you to analyze data directly in Amazon S3 using standard SQL. It eliminates the need to set up or manage infrastructure, enabling quick and cost-effective data analysis. Athena uses Presto (Trino) under the hood and supports various data formats, including CSV, JSON, ORC, Avro, and Parquet. citeturn0search0

---

## Why should I care?

- **Serverless**: No infrastructure to manage; start querying immediately.
- **Cost-Effective**: Pay only for the queries you run, based on the amount of data scanned.
- **Flexible**: Supports standard SQL and integrates with various AWS services.
- **Scalable**: Automatically scales to execute queries in parallel, providing fast results even on large datasets.

---

## When to use it

- Performing ad-hoc data analysis on data stored in Amazon S3.
- Running queries without setting up a data warehouse.
- Analyzing logs, clickstreams, or other semi-structured data.
- Integrating with business intelligence tools for reporting.

---

## Key features

- **Standard SQL Support**: Use familiar SQL syntax for querying data.
- **Integration with AWS Glue**: Utilize the AWS Glue Data Catalog for schema management.
- **Federated Queries**: Query data across various sources, including on-premises and other cloud services.
- **Machine Learning Integration**: Invoke Amazon SageMaker models directly from SQL queries.
- **Security**: Supports encryption at rest and in transit, and integrates with AWS IAM for access control.

---

## Common use cases

- **Data Lake Analytics**: Query structured and unstructured data in Amazon S3.
- **Log Analysis**: Analyze application and infrastructure logs stored in S3.
- **Business Intelligence**: Connect to BI tools like Amazon QuickSight for interactive dashboards.
- **Data Exploration**: Quickly explore large datasets without moving data.

---

## Integrations

- **Amazon S3**: Primary data source for Athena queries.
- **AWS Glue**: Manages metadata and schema information.
- **Amazon QuickSight**: Visualize query results through interactive dashboards.
- **Amazon SageMaker**: Run machine learning models within SQL queries.
- **AWS SDK for pandas (awswrangler)**: Interact with Athena using Python for data analysis workflows.

---

## Example: Querying Data in S3

1. **Create a Table**: Define a table schema that maps to your data in S3.
   ```sql
   CREATE EXTERNAL TABLE logs (
     id STRING,
     timestamp STRING,
     message STRING
   )
   ROW FORMAT DELIMITED
   FIELDS TERMINATED BY ','
   LOCATION 's3://your-bucket/path/to/data/';
   ```

2. **Run a Query**: Use standard SQL to analyze your data.
   ```sql
   SELECT COUNT(*) FROM logs WHERE message LIKE '%ERROR%';
   ```

3. **View Results**: Results are displayed in the Athena console and can be downloaded or integrated with BI tools.

---

## Learn More

- [Amazon Athena Documentation](https://docs.aws.amazon.com/athena/)
- [Getting Started with Amazon Athena](https://docs.aws.amazon.com/athena/latest/ug/getting-started.html)
- [AWS SDK for pandas Athena Tutorial](https://aws-sdk-pandas.readthedocs.io/en/3.3.0/tutorials/006%20-%20Amazon%20Athena.html)
