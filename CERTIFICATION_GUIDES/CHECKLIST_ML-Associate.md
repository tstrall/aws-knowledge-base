# AWS Machine Learning – Associate Checklist

Track your ML – Associate exam coverage.  
Complete = ✅ To do = 🔲  
Each topic includes a short description so you can review quickly.

---

<details>
<summary><strong>Data Ingestion & Preparation</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| ✅ | [Amazon S3](../storage/s3.md) | Central object store for datasets and logs |
| ✅ | [AWS Glue](../data-analytics/glue.md) | Managed ETL and metadata catalog |
| ✅ | [Glue DataBrew](../data-analytics/databrew.md) | Visual tool for cleaning and transforming data |
| ✅ | [AWS Data Wrangler](../data-analytics/data-wrangler.md) | Python SDK for Pandas-based data workflows |
| ✅ | [Amazon Athena](../data-analytics/athena.md) | Query S3 using SQL (serverless) |
| ✅ | [Redshift Spectrum](../data-analytics/redshift-spectrum.md) | Query S3 from Redshift using external tables |

</details>

---

<details>
<summary><strong>ML Services & Model Building</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| ✅ | [SageMaker Studio](../ml/sagemaker-studio.md) | Full IDE for building, training, and deploying models |
| ✅ | [SageMaker Notebooks](../ml/sagemaker-notebooks.md) | Managed Jupyter environments for development |
| ✅ | [SageMaker Training Jobs](../ml/sagemaker-training.md) | Run distributed training jobs with tuning and logs |
| ✅ | [Hyperparameter Tuning](../ml/sagemaker-tuning.md) | Automatically search for best model configuration |
| ✅ | [Built-in Algorithms](../ml/sagemaker-built-in.md) | Pre-implemented models for fast experimentation |
| ✅ | [Amazon Forecast](../ml/forecast.md) | Managed time-series forecasting |
| ✅ | [Amazon Comprehend](../ml/comprehend.md) | NLP service for sentiment, entities, and classification |
| ✅ | [Amazon Rekognition](../ml/rekognition.md) | Image and video analysis (e.g., faces, labels) |

</details>

---

<details>
<summary><strong>Model Deployment</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| ✅ | [SageMaker Endpoints](../ml/sagemaker-endpoints.md) | Real-time hosted models for inference |
| ✅ | [Batch Transform](../ml/sagemaker-batch.md) | Run inference over entire datasets at once |
| ✅ | [Model Registry](../ml/sagemaker-model-registry.md) | Track model versions for production deployment |
| ✅ | [SageMaker Pipelines](../ml/sagemaker-pipelines.md) | Automate steps from data to deployment |

</details>

---

<details>
<summary><strong>Metrics & Evaluation</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| ✅ | [Classification Metrics](../ml/metrics-classification.md) | Accuracy, precision, recall, F1, AUC |
| ✅ | [Regression Metrics](../ml/metrics-regression.md) | MAE, RMSE, R² for continuous values |
| ✅ | [Confusion Matrix](../ml/metrics-confusion-matrix.md) | Visualizes classification performance |
| ✅ | [Bias/Variance & Overfitting](../ml/model-tuning-theory.md) | Understanding errors in training and testing |

</details>

---

<details>
<summary><strong>Security & Cost</strong></summary>

| Status | Topic | Description |
|--------|--------|-------------|
| ✅ | [KMS](../security/kms.md) | Encrypts training data, models, and outputs |
| ✅ | [IAM for SageMaker](../ml/sagemaker-iam.md) | Controls access to training and inference resources |
| ✅ | [VPC Access for SageMaker](../ml/sagemaker-vpc.md) | Isolate ML workloads in private networks |
| ✅ | [SageMaker Pricing Models](../ml/sagemaker-cost.md) | Billing by instance-hours, endpoints, and data I/O |
| ✅ | [Spot Training Jobs](../ml/sagemaker-spot.md) | Reduce cost using interruptible instances |

</details>

---

📘 See [Study Strategy](./STUDY_STRATEGY.md) to learn how this checklist fits into your exam prep process.