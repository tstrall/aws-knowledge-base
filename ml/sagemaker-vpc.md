# Amazon SageMaker and VPC Integration

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

Integrating **Amazon SageMaker** with **Amazon Virtual Private Cloud (VPC)** allows you to securely run machine learning workloads within a private, isolated network. This setup ensures that your data and models remain within your controlled environment, enhancing security and compliance. By configuring SageMaker to use your VPC, you can control network access, monitor traffic, and connect to other AWS services without traversing the public internet.

---

## Why should I care?

- **Enhanced Security**: Keep your data and model artifacts within a private network, reducing exposure to external threats.
- **Compliance**: Meet organizational and regulatory requirements by controlling network boundaries and access.
- **Controlled Access**: Define fine-grained access controls using security groups and network ACLs.
- **Private Connectivity**: Use AWS PrivateLink to connect to AWS services privately, without using public IPs.

---

## Key Concepts

### VPC Configuration for SageMaker

When you configure SageMaker to use your VPC, you specify:

- **Subnets**: Private subnets where SageMaker resources will be deployed.
- **Security Groups**: Define inbound and outbound traffic rules for your resources.

This configuration allows SageMaker to create Elastic Network Interfaces (ENIs) in your VPC, enabling secure communication with other resources.

### Interface VPC Endpoints (AWS PrivateLink)

To enable private connectivity between your VPC and SageMaker APIs, you can create interface VPC endpoints:

- **SageMaker API**: `com.amazonaws.<region>.sagemaker.api`
- **SageMaker Runtime**: `com.amazonaws.<region>.sagemaker.runtime`

These endpoints allow you to invoke SageMaker APIs without traversing the public internet. citeturn0search0

---

## Common Use Cases

- **Secure Training and Inference**: Run training jobs and host models within your VPC to ensure data privacy.
- **SageMaker Studio in VPC Only Mode**: Launch SageMaker Studio with no internet access, requiring all traffic to go through your VPC. citeturn0search9
- **Accessing Private Resources**: Allow SageMaker to access databases, file systems, or other services within your VPC.

---

## Best Practices

- **Use Private Subnets**: Deploy SageMaker resources in private subnets without direct internet access.
- **Configure Security Groups Carefully**: Apply the principle of least privilege to control traffic.
- **Set Up VPC Endpoints**: Create interface VPC endpoints for services like SageMaker API, SageMaker Runtime, and Amazon S3 to enable private connectivity.
- **Monitor Network Traffic**: Use VPC Flow Logs to monitor and troubleshoot network traffic.

---

## Learn More

- [Connect to SageMaker AI Within your VPC](https://docs.aws.amazon.com/sagemaker/latest/dg/interface-vpc-endpoint.html)
- [Connect Amazon SageMaker Studio in a VPC to External Resources](https://docs.aws.amazon.com/sagemaker/latest/dg/studio-updated-and-internet-access.html)
- [Give SageMaker AI Training Jobs Access to Resources in Your Amazon VPC](https://docs.aws.amazon.com/sagemaker/latest/dg/train-vpc.html)
