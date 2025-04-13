# Amazon SageMaker Notebooks

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon SageMaker Notebooks** are fully managed Jupyter notebook instances that provide an integrated environment for machine learning (ML) development. They come pre-installed with popular data science and ML libraries, enabling you to build, train, and deploy models without managing the underlying infrastructure. SageMaker Notebooks support various instance types, including those optimized for compute or GPU-intensive tasks, and offer features like lifecycle configurations for automated setup.

---

## Why should I care?

- **Fully Managed**: Eliminates the need to set up and manage your own Jupyter servers.
- **Scalable**: Choose from a range of instance types to match your workload requirements.
- **Integrated with AWS Services**: Seamlessly access data in Amazon S3, train models with SageMaker, and deploy endpoints.
- **Secure**: Leverage AWS Identity and Access Management (IAM) for fine-grained access control.
- **Customizable**: Use lifecycle configurations to automate the installation of packages and setup of environments.

---

## When to use it

- Developing and testing ML models in an interactive environment.
- Collaborating with team members on data science projects.
- Running data exploration and preprocessing tasks.
- Integrating with other AWS services for end-to-end ML workflows.

---

## Key features

- **Pre-installed Libraries**: Includes popular ML and data science libraries like TensorFlow, PyTorch, scikit-learn, and more.
- **Lifecycle Configurations**: Automate the setup of your notebook environment with scripts that run on start-up.
- **Elastic Inference**: Attach elastic inference accelerators to reduce the cost of inference workloads.
- **Multiple Kernel Support**: Run notebooks with different kernels, such as Python 3, R, or Julia.
- **Git Integration**: Clone repositories directly into your notebook instance for version control.

---

## Common use cases

- **Data Exploration**: Analyze and visualize datasets stored in Amazon S3.
- **Model Development**: Build and train ML models using built-in libraries and frameworks.
- **Experiment Tracking**: Keep track of different model versions and parameters.
- **Education and Training**: Use as a teaching tool for ML courses and workshops.

---

## Integrations

- **Amazon S3**: Store and retrieve datasets for training and evaluation.
- **Amazon SageMaker**: Train and deploy models directly from the notebook interface.
- **AWS Glue**: Access and process data catalogs for ETL operations.
- **Amazon CloudWatch**: Monitor notebook instance metrics and logs.
- **AWS CodeCommit**: Version control your notebooks and code.

---

## Example: Creating a SageMaker Notebook Instance

1. **Navigate to SageMaker in the AWS Console**: Open the Amazon SageMaker console at [https://console.aws.amazon.com/sagemaker/](https://console.aws.amazon.com/sagemaker/).
2. **Create a Notebook Instance**: Click on "Notebook instances" and then "Create notebook instance".
3. **Configure the Instance**: Provide a name, select an instance type (e.g., `ml.t2.medium`), and assign an IAM role with the necessary permissions.
4. **(Optional) Add Lifecycle Configuration**: Attach a lifecycle configuration script to automate setup tasks.
5. **Create and Launch**: Click "Create notebook instance". Once the status changes to "InService", click "Open Jupyter" to start using the notebook.

---

## Learn More

- [Amazon SageMaker Notebook Instances Documentation](https://docs.aws.amazon.com/sagemaker/latest/dg/nbi.html)
- [Getting Started with Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/gs.html)
- [SageMaker Example Notebooks](https://github.com/aws/amazon-sagemaker-examples)
