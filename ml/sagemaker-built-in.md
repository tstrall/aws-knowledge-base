# Amazon SageMaker Built-in Algorithms

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker** offers a suite of built-in algorithms optimized for large-scale machine learning tasks. These algorithms are pre-packaged and can be used directly within SageMaker, eliminating the need to develop and maintain custom training code. They support various problem types, including classification, regression, clustering, anomaly detection, and more, across different data modalities such as tabular, text, and image data.

---

## Why should I care?

- **Ease of Use**: Quickly deploy models without writing custom training code.
- **Scalability**: Efficiently handle large datasets with optimized performance.
- **Integration**: Seamlessly integrates with other AWS services like S3, CloudWatch, and SageMaker Pipelines.
- **Cost-Effective**: Utilize managed infrastructure to reduce operational overhead.

---

## When to use it

- When you need to rapidly develop and deploy ML models without extensive coding.
- For standard ML tasks where built-in algorithms suffice.
- To leverage optimized and scalable solutions for large datasets.

---

## Key features

- **Pre-optimized**: Algorithms are tuned for performance and scalability.
- **Versatile**: Support for various ML tasks and data types.
- **Managed**: AWS handles the underlying infrastructure and maintenance.
- **Customizable**: Configure hyperparameters to tailor models to specific needs.

---

## Common use cases

- **Classification**: Spam detection, sentiment analysis, image recognition.
- **Regression**: Price prediction, demand forecasting.
- **Clustering**: Customer segmentation, topic modeling.
- **Anomaly Detection**: Fraud detection, fault monitoring.
- **Recommendation Systems**: Product or content recommendations.

---

## Integrations

- **Amazon S3**: For storing and retrieving training data.
- **Amazon CloudWatch**: Monitoring and logging of training jobs.
- **Amazon SageMaker Pipelines**: Automate and manage ML workflows.
- **Amazon SageMaker Studio**: Interactive development environment for ML.

---

## Example: Using the XGBoost Built-in Algorithm



```python
import sagemaker
from sagemaker import get_execution_role
from sagemaker.inputs import TrainingInput
from sagemaker.estimator import Estimator

# Define the SageMaker session and role
sagemaker_session = sagemaker.Session()
role = get_execution_role()

# Specify the S3 path for training data
s3_input_train = TrainingInput(s3_data='s3://your-bucket/train/', content_type='csv')

# Define the XGBoost estimator
xgboost_estimator = Estimator(
    image_uri=sagemaker.image_uris.retrieve('xgboost', sagemaker_session.boto_region_name),
    role=role,
    instance_count=1,
    instance_type='ml.m5.large',
    output_path='s3://your-bucket/output',
    sagemaker_session=sagemaker_session
)

# Set hyperparameters
xgboost_estimator.set_hyperparameters(
    max_depth=5,
    eta=0.2,
    gamma=4,
    min_child_weight=6,
    subsample=0.8,
    objective='binary:logistic',
    num_round=100
)

# Start the training job
xgboost_estimator.fit({'train': s3_input_train})
```

---

## Learn More

- [Amazon SageMaker Built-in Algorithms Documentation](https://docs.aws.amazon.com/sagemaker/latest/dg/algos.html)
- [SageMaker Python SDK - Built-in Algorithms](https://sagemaker.readthedocs.io/en/stable/algorithms/index.html)
- [SageMaker Example Notebooks](https://sagemaker-examples.readthedocs.io/en/latest/training/algorithms.html)
