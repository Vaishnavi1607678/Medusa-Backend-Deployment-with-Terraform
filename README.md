Medusa Backend Deployment with Terraform

📦 Project Overview
Feature	Description
Infrastructure as Code	Terraform manages AWS infrastructure (ECS, VPC, etc.)
CI/CD Automation	GitHub Actions pipeline automates provisioning
Platform	AWS ECS Fargate (serverless container hosting)

🛠️ Terraform Configuration
✅ Cloud Provider
AWS

📚 Core Resources
Resource	Description
🟩 VPC	Isolated network environment for resources
🟨 Subnet	Logical partition of the VPC
🔐 Security Group	Controls traffic to/from ECS containers
🔑 IAM Role	ECS task execution permissions
📦 ECS Cluster	Manages containers with AWS Fargate
📄 Task Definition	Defines container image & settings
🔁 ECS Service	Maintains desired running task count

🔧 Terraform Language
All infrastructure is defined using HCL (HashiCorp Configuration Language).
Easily reusable and modular for scalable deployments.

⚙️ CI/CD Pipeline with GitHub Actions
📋 Workflow Steps
Step	Description
🔁 Checkout Code	Gets latest code from the repo
⚙️ Setup Terraform	Installs specific Terraform version
🏗️ Terraform Init	Initializes Terraform working directory
🧠 Terraform Plan	Generates an execution plan
🚀 Terraform Apply	Provisions infrastructure on AWS

medusa-deploy/
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── terraform.tfvars
├── .github/workflows/
│   └── deploy.yml
└── medusa-backend/
    └── (your Medusa app)

Code ➝ GitHub Actions ➝ Terraform ➝ AWS ECS ➝ Medusa running
