# Amazon SageMaker Batch Transform

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker Batch Transform** is a fully managed service that enables you to perform batch inference on large datasets using your trained machine learning models. It allows you to obtain predictions for multiple data records in a single request, making it suitable for scenarios where real-time inference is not required. Batch Transform manages the provisioning of resources, handles data loading and preprocessing, and scales automatically based on your workload. citeturn0search0

---

## Why should I care?

- **Efficient Processing**: Process large datasets in parallel without the need to manage infrastructure.
- **Cost-Effective**: Pay only for the resources used during the batch transform job, with automatic scaling to optimize costs.
- **Seamless Integration**: Integrates with other AWS services like S3 for data storage and SageMaker for model management.
- **Flexible Input Formats**: Supports various data formats, including CSV, JSON, and image files.

---

## When to use it

- When you need to generate predictions for large datasets and real-time responses are not necessary.
- For preprocessing data before training machine learning models.
- To perform inference on datasets that are too large to process in real-time.

---

## Key features

- **Automatic Resource Management**: SageMaker provisions and manages the necessary compute resources for the batch transform job.
- **Scalability**: Automatically scales to handle large datasets efficiently.
- **Data Sharding**: Distributes data across multiple instances to optimize processing time.
- **Input and Output Filtering**: Allows filtering of input data and joining of input attributes with predictions in the output. citeturn0search11

---

## Common use cases

- **Predictive Maintenance**: Analyzing historical sensor data to predict equipment failures.
- **Customer Segmentation**: Processing large customer datasets to identify segments for targeted marketing.
- **Fraud Detection**: Evaluating batches of transactions to identify potentially fraudulent activities.
- **Document Processing**: Extracting information from a large number of documents using natural language processing models.

---

## Integrations

- **Amazon S3**: Store input data and output results for batch transform jobs.
- **AWS Lambda**: Trigger batch transform jobs in response to events.
- **Amazon CloudWatch**: Monitor and log batch transform job metrics and logs.
- **AWS Step Functions**: Orchestrate batch transform jobs as part of larger workflows.

---

## Example: Running a Batch Transform Job with Boto3




```python
import boto3

# Create a SageMaker client
sagemaker = boto3.client('sagemaker')

# Define the batch transform job parameters
transform_job_name = 'my-batch-transform-job'
model_name = 'my-trained-model'
input_data_path = 's3://my-bucket/input-data/'
output_data_path = 's3://my-bucket/output-data/'

sagemaker.create_transform_job(
    TransformJobName=transform_job_name,
    ModelName=model_name,
    TransformInput={
        'DataSource': {
            'S3DataSource': {
                'S3DataType': 'S3Prefix',
                'S3Uri': input_data_path
            }
        },
        'ContentType': 'text/csv',
        'SplitType': 'Line'
    },
    TransformOutput={
        'S3OutputPath': output_data_path
    },
    TransformResources={
        'InstanceType': 'ml.m5.large',
        'InstanceCount': 1
    }
)

# Wait for the batch transform job to complete
sagemaker.get_waiter('transform_job_completed_or_stopped').wait(TransformJobName=transform_job_name)

# Print the status of the batch transform job
response = sagemaker.describe_transform_job(TransformJobName=transform_job_name)
print(f"Transform job status: {response['TransformJobStatus']}")
```




---

## Learn More

- [Batch Transform for Inference with Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/batch-transform.html)
- [Associating Prediction Results with Input Data Using Amazon SageMaker Batch Transform](https://aws.amazon.com/blogs/machine-learning/associating-prediction-results-with-input-data-using-amazon-sagemaker-batch-transform/)
- [Batch Inference at Scale with Amazon SageMaker](https://aws.amazon.com/blogs/architecture/batch-inference-at-scale-with-amazon-sagemaker/)
