# Amazon SageMaker Endpoints

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker Endpoints** are fully managed, scalable interfaces that allow you to deploy machine learning models for inference. They support various deployment options, including real-time, asynchronous, serverless, and multi-model endpoints, catering to different latency, throughput, and cost requirements.

---

## Why should I care?

- **Flexible Deployment Options**: Choose from real-time, asynchronous, serverless, or multi-model endpoints based on your application's needs.
- **Scalability**: Endpoints can automatically scale to handle varying traffic patterns.
- **Cost Efficiency**: Optimize costs by selecting the appropriate endpoint type and scaling strategy.
- **Integration**: Seamlessly integrates with other AWS services like Lambda, S3, and CloudWatch.

---

## When to use it

- Deploying models that require real-time predictions with low latency.
- Handling large payloads or long-running inference tasks asynchronously.
- Serving multiple models through a single endpoint to optimize resource utilization.
- Implementing cost-effective solutions for intermittent or unpredictable traffic patterns.

---

## Key features

- **Real-Time Inference**: Deploy models that provide immediate predictions.
- **Asynchronous Inference**: Handle large or long-running inference requests without blocking.
- **Serverless Inference**: Automatically scale compute resources based on demand, eliminating the need to manage infrastructure.
- **Multi-Model Endpoints**: Host multiple models on a single endpoint, dynamically loading them as needed.
- **Auto Scaling**: Automatically adjust the number of instances based on traffic.
- **Monitoring and Logging**: Integrate with Amazon CloudWatch for metrics and logs to monitor endpoint performance.

---

## Common use cases

- **E-commerce**: Providing personalized product recommendations in real-time.
- **Healthcare**: Analyzing medical images or records asynchronously.
- **Finance**: Detecting fraudulent transactions with low latency.
- **Manufacturing**: Predictive maintenance by analyzing sensor data in real-time.

---

## Integrations

- **Amazon S3**: Store and retrieve model artifacts and inference data.
- **AWS Lambda**: Trigger inference requests or process results.
- **Amazon CloudWatch**: Monitor endpoint metrics and logs.
- **AWS Step Functions**: Orchestrate complex inference workflows.
- **Amazon API Gateway**: Expose endpoints as RESTful APIs.

---

## Example: Deploying a Model to a Real-Time Endpoint Using Boto3



```python
import boto3

# Create a SageMaker client
sagemaker = boto3.client('sagemaker')

# Define model parameters
model_name = 'my-model'
model_artifact = 's3://my-bucket/model.tar.gz'
container_image = '123456789012.dkr.ecr.us-west-2.amazonaws.com/my-container:latest'
role_arn = 'arn:aws:iam::123456789012:role/SageMakerExecutionRole'

# Create the model
sagemaker.create_model(
    ModelName=model_name,
    PrimaryContainer={
        'Image': container_image,
        'ModelDataUrl': model_artifact
    },
    ExecutionRoleArn=role_arn
)

# Create endpoint configuration
endpoint_config_name = 'my-endpoint-config'
sagemaker.create_endpoint_config(
    EndpointConfigName=endpoint_config_name,
    ProductionVariants=[
        {
            'VariantName': 'AllTraffic',
            'ModelName': model_name,
            'InstanceType': 'ml.m5.large',
            'InitialInstanceCount': 1
        }
    ]
)

# Deploy the endpoint
endpoint_name = 'my-endpoint'
sagemaker.create_endpoint(
    EndpointName=endpoint_name,
    EndpointConfigName=endpoint_config_name
)
```



---

## Learn More

- [Deploy models for real-time inference](https://docs.aws.amazon.com/sagemaker/latest/dg/realtime-endpoints.html)
- [Deploy models with Amazon SageMaker Serverless Inference](https://docs.aws.amazon.com/sagemaker/latest/dg/serverless-endpoints.html)
- [Multi-model endpoints](https://docs.aws.amazon.com/sagemaker/latest/dg/multi-model-endpoints.html)
- [AWS::SageMaker::Endpoint - AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpoint.html)
