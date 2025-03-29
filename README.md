# terraform-eks-jagadesh
# Terraform EKS Cluster - Jagadesh

## Overview
This project sets up an **Amazon EKS (Elastic Kubernetes Service) cluster** using **Terraform**. The cluster is named **"jagadesh"** and is deployed on AWS.

## Prerequisites
Before proceeding, ensure you have the following installed:
- [Terraform](https://developer.hashicorp.com/terraform/downloads)
- [AWS CLI](https://aws.amazon.com/cli/)
- AWS Account with necessary IAM permissions
- Configured AWS credentials (`aws configure`)

## Project Structure
```
terraform-eks-jagadesh/
│── versions.tf          # Terraform and provider versions
│── variables.tf         # Input variables
│── vpc.tf               # VPC configuration
│── security-groups.tf   # Security groups for EKS
│── eks-cluster.tf       # EKS cluster definition
│── outputs.tf           # Outputs for reference
│── README.md            # Project documentation
```

## Deployment Steps
### 1. Clone the Repository
```bash
git clone https://github.com/jagadesh999/terraform-eks-jagadesh.git
cd terraform-eks-jagadesh
```

### 2. Initialize Terraform
```bash
terraform init
```

### 3. Plan the Deployment
```bash
terraform plan
```

### 4. Apply the Configuration
```bash
terraform apply -auto-approve
```

### 5. Verify EKS Cluster
```bash
aws eks --region us-east-1 describe-cluster --name jagadesh --query cluster.status
```

### 6. Destroy the Cluster (if needed)
To delete the cluster and all associated resources:
```bash
terraform destroy -auto-approve
```

## Notes
- The **cluster name** is set to `jagadesh`.
- Modify **variables.tf** if you need to change **region** or **cluster settings**.
- Ensure IAM roles have the correct permissions before applying Terraform.

## Commit Message Suggestion
When committing this project to GitHub, use a meaningful commit message:
```bash
git commit -m "Terraforming the future – EKS cluster ready!"
git push origin main
```

Now your **Terraform EKS cluster** is ready to use! 🚀

