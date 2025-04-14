# Terraform (Infrastructure as Code)

**What it is:**
- Open-source tool for declarative infrastructure management
- Created by HashiCorp, widely used for provisioning cloud resources

---

## Core Concepts

| Concept       | Description |
|---------------|-------------|
| **Provider**  | Plugin that interfaces with a cloud/service (e.g., AWS, GitHub) |
| **Resource**  | Infrastructure object (e.g., `aws_s3_bucket`, `aws_lambda_function`) |
| **Module**    | Reusable unit of configuration (can be local or remote) |
| **Variable**  | Input to parameterize modules and configs |
| **Output**    | Values returned after apply (e.g., endpoint, ARN) |
| **State**     | JSON file tracking what Terraform has deployed |

---

## Sample Structure
```
main.tf        # Resources and modules
variables.tf   # Input variables
outputs.tf     # Output values
provider.tf    # Provider config (e.g. AWS)
```

---

## Common Commands
```bash
terraform init       # Initialize working directory
terraform plan       # Preview changes
terraform apply      # Apply changes
terraform destroy    # Tear down infrastructure
```

---

## Remote State
- Store state in S3 with locking via DynamoDB (best practice)
```hcl
terraform {
  backend "s3" {
    bucket         = "my-tf-state"
    key            = "prod/network/terraform.tfstate"
    region         = "us-east-1"
    dynamodb_table = "my-tf-locks"
  }
}
```

---

## Modules
```hcl
module "vpc" {
  source  = "terraform-aws-modules/vpc/aws"
  version = "3.14.2"

  name = "my-vpc"
  cidr = "10.0.0.0/16"
  azs  = ["us-east-1a", "us-east-1b"]
  ...
}
```

---

## Best Practices
- Use remote state + locking
- Use modules for reuse and consistency
- Tag resources and support environments
- Store secrets in SSM/Secrets Manager, not variables
- Avoid hardcoded values

---

## Tools
- `tflint`, `terraform-docs`, `checkov`, `pre-commit` hooks
- `Terragrunt` (wrapper to simplify multi-env/module setups)

---

## Interview Tips
- Know how state works and how to debug drift
- Be able to explain module reuse and variable injection
- Understand how you'd structure environments (dev/stage/prod)
- Be ready to explain how secrets, tagging, and IAM are handled
