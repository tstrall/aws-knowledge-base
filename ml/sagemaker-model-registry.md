# Amazon SageMaker Model Registry

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker Model Registry** is a fully managed service that enables you to catalog, manage, and deploy machine learning (ML) models in a centralized repository. It facilitates model versioning, approval workflows, metadata tracking, and deployment automation, streamlining the MLOps lifecycle from experimentation to production. citeturn0search0

---

## Why should I care?

- **Centralized Model Management**: Organize and track all your ML models and their versions in one place.
- **Version Control**: Maintain a history of model versions, enabling reproducibility and auditability.
- **Approval Workflows**: Implement governance by managing model approval statuses (e.g., Pending, Approved, Rejected).
- **Seamless Deployment**: Integrate with SageMaker endpoints for streamlined model deployment.
- **Metadata Association**: Attach training metrics, datasets, and other metadata to models for better traceability.

---

## When to use it

- Managing multiple versions of ML models across different stages (development, testing, production).
- Implementing MLOps practices with CI/CD pipelines for ML workflows.
- Collaborating across teams by providing a shared repository of models.
- Ensuring compliance and governance through model approval and metadata tracking.

---

## Key features

- **Model Groups**: Logical grouping of related model versions.
- **Model Versions**: Each registered model is versioned for tracking changes over time.
- **Approval Status**: Manage the deployment readiness of models with statuses like Approved, Pending, or Rejected.
- **Metadata Tracking**: Store training parameters, evaluation metrics, and other relevant information.
- **Integration with Model Cards**: Associate detailed documentation with models for transparency and governance. citeturn0search9
- **Collections**: Organize model groups into hierarchical structures for better discoverability. citeturn0search7

---

## Common use cases

- **Enterprise MLOps**: Standardize model management across large teams and projects.
- **Regulatory Compliance**: Maintain detailed records of model development and deployment for audits.
- **Cross-Account Collaboration**: Share models securely across different AWS accounts.
- **Automated Deployment Pipelines**: Integrate with CI/CD tools to automate model deployment upon approval.

---

## Integrations

- **Amazon SageMaker Pipelines**: Automate model registration and deployment workflows.
- **Amazon SageMaker Studio**: Visual interface for managing model registry components.
- **AWS Lambda & Step Functions**: Trigger actions based on model registry events.
- **Amazon CloudWatch**: Monitor model deployment metrics and logs.
- **AWS Identity and Access Management (IAM)**: Control access to model registry resources.

---

## Example: Registering a Model Version with Boto3




```python
import boto3

# Initialize SageMaker client
sm_client = boto3.client('sagemaker')

# Define model package group name
model_package_group_name = 'my-model-group'

# Define model data and image
model_url = 's3://my-bucket/model.tar.gz'
image_uri = '123456789012.dkr.ecr.us-west-2.amazonaws.com/my-image:latest'

# Create model package
response = sm_client.create_model_package(
    ModelPackageGroupName=model_package_group_name,
    ModelPackageDescription='My model version 1',
    InferenceSpecification={
        'Containers': [
            {
                'Image': image_uri,
                'ModelDataUrl': model_url
            }
        ],
        'SupportedContentTypes': ['text/csv'],
        'SupportedResponseMIMETypes': ['text/csv']
    },
    ModelApprovalStatus='PendingManualApproval'
)

print(f"Model Package ARN: {response['ModelPackageArn']}")
```




---

## Learn More

- [Amazon SageMaker Model Registry Documentation](https://docs.aws.amazon.com/sagemaker/latest/dg/model-registry.html)
- [Register a Model Version](https://docs.aws.amazon.com/sagemaker/latest/dg/model-registry-version.html)
- [Deploy a Model from the Registry with Python](https://docs.aws.amazon.com/sagemaker/latest/dg/model-registry-deploy.html)
- [Integrate Amazon SageMaker Model Cards with the Model Registry](https://aws.amazon.com/blogs/machine-learning/integrate-amazon-sagemaker-model-cards-with-the-model-registry/)
