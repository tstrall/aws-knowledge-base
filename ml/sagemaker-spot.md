# Amazon SageMaker Managed Spot Training

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Managed Spot Training** in Amazon SageMaker enables you to utilize Amazon EC2 Spot Instances for training machine learning models, offering cost savings of up to 90% compared to On-Demand Instances. SageMaker handles the provisioning and management of Spot Instances, including interruptions and resumptions, providing a seamless experience for training jobs. citeturn0search0

---

## Why should I care?

- **Significant Cost Savings**: Reduce training costs substantially by leveraging unused EC2 capacity.
- **Seamless Integration**: Easily enable Spot Instances in your training jobs with minimal configuration changes.
- **Fault Tolerance**: SageMaker manages interruptions and resumes training from the last checkpoint, minimizing loss.
- **Scalability**: Train large models efficiently without incurring high costs.

---

## Key Concepts

### Spot Instances

Spot Instances are spare EC2 compute capacities offered at discounted rates. They can be interrupted by AWS with a two-minute warning when the capacity is needed elsewhere. This makes them suitable for fault-tolerant and flexible applications like model training.

### Checkpointing

To handle potential interruptions, it's recommended to implement checkpointing in your training jobs. SageMaker can automatically save checkpoints to Amazon S3, allowing training to resume from the last saved state upon interruption. citeturn0search0

---

## How to Enable Managed Spot Training

When configuring your training job using the SageMaker Python SDK, set the following parameters in your Estimator:

- `use_spot_instances=True`: Enables the use of Spot Instances.
- `max_run`: Specifies the maximum duration of the training job in seconds.
- `max_wait`: Defines the total time SageMaker waits for Spot Instances to become available, which should be greater than `max_run`.
- `checkpoint_s3_uri`: (Optional) S3 URI where checkpoints are stored.

**Example:**


```python
from sagemaker.estimator import Estimator

estimator = Estimator(
    entry_point='train.py',
    role='SageMakerRole',
    instance_count=1,
    instance_type='ml.m5.xlarge',
    framework_version='1.8',
    py_version='py3',
    use_spot_instances=True,
    max_run=3600,
    max_wait=4000,
    checkpoint_s3_uri='s3://your-bucket/checkpoints/',
    ...
)
```


Ensure your training script is configured to save and load checkpoints from the specified S3 location.

---

## Best Practices

- **Implement Checkpointing**: Regularly save model states to S3 to resume training seamlessly after interruptions.
- **Set Appropriate Timeouts**: Configure `max_run` and `max_wait` to accommodate potential delays in Spot Instance availability.
- **Monitor Training Jobs**: Use Amazon CloudWatch to track training progress and handle any issues promptly.
- **Test for Fault Tolerance**: Simulate interruptions to ensure your training job can recover gracefully.

---

## Learn More

- [Managed Spot Training in Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/model-managed-spot-training.html)
- [Amazon SageMaker Managed Spot Training Examples](https://github.com/aws-samples/amazon-sagemaker-managed-spot-training)
- [Optimizing and Scaling Machine Learning Training with Managed Spot Training](https://aws.amazon.com/tutorials/managed-spot-training-sagemaker/)
