# Amazon SageMaker Pipelines

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker Pipelines** is a purpose-built, serverless workflow orchestration service designed to automate and manage end-to-end machine learning (ML) workflows. It enables you to define, deploy, and monitor ML pipelines composed of interconnected steps such as data preprocessing, model training, evaluation, and deployment. SageMaker Pipelines integrates seamlessly with other AWS services, providing a scalable and efficient solution for MLOps. citeturn0search0

---

## Why should I care?

- **Automation**: Streamlines the ML lifecycle by automating repetitive tasks, reducing manual intervention.
- **Scalability**: Automatically scales resources based on workload demands, ensuring efficient processing.
- **Integration**: Seamlessly integrates with AWS services like S3, Lambda, and SageMaker Model Registry for a cohesive ML workflow.
- **Monitoring and Logging**: Provides built-in tracking of pipeline executions, making it easier to monitor performance and debug issues.
- **Version Control**: Supports versioning of pipelines, facilitating reproducibility and auditability.

---

## When to use it

- Implementing continuous integration and continuous delivery (CI/CD) for ML models.
- Managing complex ML workflows that involve multiple interdependent steps.
- Ensuring consistent and repeatable ML processes across teams and projects.
- Automating model retraining and deployment in response to new data or performance metrics.

---

## Key features

- **Directed Acyclic Graph (DAG) Structure**: Defines pipelines as DAGs, ensuring clear dependencies and execution order.
- **Step Types**: Supports various step types including Processing, Training, Transform, and Condition steps.
- **Parameterization**: Allows dynamic input parameters for flexible pipeline executions.
- **Conditional Execution**: Enables branching logic within pipelines based on step outcomes.
- **Caching**: Avoids redundant computations by caching outputs of previous executions.
- **Integration with SageMaker Model Registry**: Facilitates model versioning and deployment workflows.

---

## Common use cases

- **Data Preprocessing**: Automating data cleaning and feature engineering steps.
- **Model Training and Evaluation**: Orchestrating training jobs and evaluating model performance.
- **Model Deployment**: Automating the deployment of models to production environments.
- **Monitoring and Retraining**: Setting up pipelines that monitor model performance and trigger retraining as needed.

---

## Integrations

- **Amazon S3**: Stores input data and model artifacts.
- **AWS Lambda**: Executes custom code within pipeline steps.
- **Amazon SageMaker Model Registry**: Manages model versions and approvals.
- **Amazon CloudWatch**: Monitors pipeline executions and logs.
- **AWS Step Functions**: Coordinates complex workflows that extend beyond ML tasks.

---

## Example: Defining a Simple Pipeline with Boto3




```python
import boto3
import sagemaker
from sagemaker.workflow.pipeline import Pipeline
from sagemaker.workflow.steps import ProcessingStep, TrainingStep
from sagemaker.processing import ScriptProcessor
from sagemaker.sklearn.estimator import SKLearn

# Initialize SageMaker session and role
sagemaker_session = sagemaker.session.Session()
role = sagemaker.get_execution_role()

# Define a processing step
script_processor = ScriptProcessor(
    image_uri='your-processing-image-uri',
    command=['python3'],
    role=role,
    instance_count=1,
    instance_type='ml.m5.xlarge'
)

processing_step = ProcessingStep(
    name='MyProcessingStep',
    processor=script_processor,
    inputs=[],
    outputs=[],
    code='processing_script.py'
)

# Define a training step
sklearn_estimator = SKLearn(
    entry_point='train_script.py',
    role=role,
    instance_type='ml.m5.xlarge',
    framework_version='0.23-1',
    sagemaker_session=sagemaker_session
)

training_step = TrainingStep(
    name='MyTrainingStep',
    estimator=sklearn_estimator,
    inputs={}
)

# Create the pipeline
pipeline = Pipeline(
    name='MyPipeline',
    steps=[processing_step, training_step],
    sagemaker_session=sagemaker_session
)

# Submit the pipeline
pipeline.upsert(role_arn=role)
execution = pipeline.start()
```

---

## Learn More

- [Amazon SageMaker Pipelines Documentation](https://docs.aws.amazon.com/sagemaker/latest/dg/pipelines.html)
- [Define a Pipeline](https://docs.aws.amazon.com/sagemaker/latest/dg/define-pipeline.html)
- [SageMaker Python SDK - Pipelines](https://sagemaker.readthedocs.io/en/stable/workflows/pipelines/sagemaker.workflow.pipelines.html)
- [SageMaker Pipelines Examples](https://sagemaker-examples.readthedocs.io/en/latest/sagemaker-pipelines/index.html)
