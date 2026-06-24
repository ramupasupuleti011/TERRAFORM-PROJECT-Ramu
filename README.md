# 🚀 AWS Infrastructure Automation using Terraform & Jenkins CI/CD

<p align="center">
<img src="./screenshots/architecture.png" width="900">
</p>

## 📌 Overview

Automated AWS infrastructure provisioning using **Terraform** and **Jenkins CI/CD**. The pipeline validates, plans, and deploys infrastructure resources on AWS using Infrastructure as Code (IaC).

## 🛠 Tech Stack

* AWS
* Terraform
* Jenkins
* GitHub
* Apache HTTP Server

## ☁ Resources Provisioned

* 4 EC2 Instances
* Classic Elastic Load Balancer
* Security Group
* S3 Bucket
* 4 IAM Users
* 40 GB EBS Volume

## 🔄 Jenkins Pipeline

```text
Checkout
   ↓
Terraform Init
   ↓
Terraform Validate
   ↓
Terraform Plan
   ↓
Terraform Apply / Destroy
```

### Deployment Commands

```bash
terraform init
terraform validate
terraform plan
terraform apply --auto-approve
```

Destroy Infrastructure

```bash
terraform destroy --auto-approve
```

## 🔐 Jenkins Credentials

| ID        | Type        |
| --------- | ----------- |
| accesskey | Secret Text |
| secretkey | Secret Text |

Environment Variables

```groovy
environment {
 AWS_ACCESS_KEY_ID = credentials('accesskey')
 AWS_SECRET_ACCESS_KEY = credentials('secretkey')
}
```

## 📂 Repository Structure

```text
terraform-project-ramu/
├── Jenkinsfile
├── main.tf
├── elb.tf
├── README.md
└── screenshots/
    └── architecture.png
```

## ✨ Key Features

* Infrastructure as Code (IaC)
* Jenkins CI/CD Automation
* Multi-AZ Architecture
* ELB Integration
* IAM User Management
* Secure AWS Credential Handling

## 👨‍💻 Author

**Ramu Pasupuleti**

AWS Cloud & DevOps Engineer

GitHub: https://github.com/ramupasupuleti011

LinkedIn: https://linkedin.com/in/ramu-pasupuleti-533272281
