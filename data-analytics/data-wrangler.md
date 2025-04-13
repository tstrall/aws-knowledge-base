# AWS SDK for pandas (awswrangler)

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Data Analytics – Specialty (DAS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**AWS SDK for pandas**, also known as **awswrangler**, is an open-source Python library that extends the functionality of pandas to integrate seamlessly with AWS services. It simplifies data processing and analytics workflows by providing high-level abstractions for reading from and writing to AWS data stores, such as Amazon S3, Athena, Redshift, and more. This allows data engineers and scientists to interact with AWS services using familiar pandas syntax.

---

## Why should I care?

- **Simplified AWS Integration**: Interact with AWS data services using pandas-like syntax, reducing the learning curve.
- **Efficient Data Processing**: Perform ETL operations without managing complex AWS SDK configurations.
- **Scalability**: Handle large datasets efficiently by leveraging AWS's scalable infrastructure.
- **Open Source**: Benefit from community contributions and transparency.

---

## When to use it

- Building data pipelines that interact with AWS services.
- Performing data analysis on large datasets stored in AWS.
- Automating ETL processes involving AWS data sources.
- Integrating AWS data services into machine learning workflows.

---

## Key features

- **Amazon S3 Integration**: Read from and write to S3 in various formats (CSV, Parquet, JSON, etc.).
- **Amazon Athena Support**: Execute SQL queries and retrieve results as pandas DataFrames.
- **Amazon Redshift Connectivity**: Load data into Redshift and perform queries seamlessly.
- **AWS Glue Catalog Access**: Interact with the Glue Data Catalog for metadata management.
- **Time Series Support**: Work with Amazon Timestream for time series data.
- **DataFrame Operations**: Perform standard pandas operations with AWS data sources.

---

## Common use cases

- **Data Lake Operations**: Manage and process data stored in Amazon S3.
- **Analytics Workflows**: Query data using Athena and process results in pandas.
- **Data Warehousing**: Load and extract data from Amazon Redshift for analysis.
- **Machine Learning Pipelines**: Prepare and process data for ML models using AWS services.

---

## Integrations

- **Amazon S3**: Storage and retrieval of various data formats.
- **Amazon Athena**: SQL querying of data stored in S3.
- **Amazon Redshift**: Data warehousing and analytics.
- **AWS Glue**: Metadata management and ETL operations.
- **Amazon Timestream**: Time series data storage and analysis.
- **Amazon DynamoDB**: NoSQL database interactions.

---

## Example: Reading from S3 and Writing to Redshift


```python
import awswrangler as wr
import pandas as pd

# Read data from S3
df = wr.s3.read_parquet(path='s3://my-bucket/my-data/')

# Transform data using pandas
df['new_column'] = df['existing_column'] * 2

# Write data to Redshift
wr.redshift.copy(
    df=df,
    path='s3://my-bucket/temp/',
    con=wr.redshift.connect('my-redshift-connection'),
    schema='public',
    table='my_table',
    mode='overwrite'
)
```

---

## Learn More

- [AWS SDK for pandas Documentation](https://aws-sdk-pandas.readthedocs.io/)
- [GitHub Repository](https://github.com/aws/aws-sdk-pandas)
- [Quick Start Guide](https://aws-sdk-pandas.readthedocs.io/en/stable/quick_start.html)
