# AWS EKS Platform Automation

## Overview

This project demonstrates the implementation of a production-ready cloud platform on AWS using Infrastructure as Code (IaC), Kubernetes, and CI/CD automation.

The platform is designed to automate infrastructure provisioning, application deployment, monitoring, and operational management using modern DevOps practices.

## Technologies Used

* AWS
* Amazon EKS
* Terraform
* Docker
* Kubernetes
* GitHub Actions
* Helm
* Prometheus
* Grafana
* AWS CloudWatch
* IAM
* VPC
* Route53

## Architecture

The solution includes:

* Terraform modules for infrastructure provisioning
* Amazon EKS cluster deployment
* Containerized applications running on Kubernetes
* Automated CI/CD pipelines
* Monitoring and alerting
* Secure IAM-based access controls
* High availability and scalability

## Project Structure

```text
.
├── terraform/
│   ├── modules/
│   ├── networking/
│   ├── eks/
│   └── security/
├── kubernetes/
│   ├── deployments/
│   ├── services/
│   └── ingress/
├── helm/
├── scripts/
├── monitoring/
├── .github/workflows/
└── README.md
```

## Prerequisites

Before getting started, install:

* Git
* Docker
* Terraform
* AWS CLI
* kubectl
* Helm

## Clone Repository

```bash
git clone https://github.com/yourusername/aws-eks-platform-automation.git

cd aws-eks-platform-automation
```

## Configure AWS Access

```bash
aws configure
```

Verify access:

```bash
aws sts get-caller-identity
```

## Deploy Infrastructure

Initialize Terraform:

```bash
terraform init
```

Validate configuration:

```bash
terraform validate
```

Review deployment plan:

```bash
terraform plan
```

Deploy infrastructure:

```bash
terraform apply
```

## Configure Kubernetes

Connect to EKS:

```bash
aws eks update-kubeconfig \
--region us-east-1 \
--name production-eks-cluster
```

Verify connectivity:

```bash
kubectl get nodes
```

## Deploy Applications

```bash
kubectl apply -f kubernetes/
```

Verify deployments:

```bash
kubectl get pods -A
```

## CI/CD Pipeline

The GitHub Actions pipeline performs:

* Source code validation
* Terraform validation
* Security scanning
* Docker image build
* Container image push
* Kubernetes deployment
* Post-deployment verification

## Monitoring & Observability

Monitoring stack includes:

* Prometheus
* Grafana
* CloudWatch
* Kubernetes Metrics Server

Key metrics monitored:

* CPU utilization
* Memory utilization
* Pod health
* Node health
* Application availability
* Infrastructure performance

## Security

Security controls implemented:

* IAM Roles and Policies
* Least Privilege Access
* Kubernetes RBAC
* Secrets Management
* Infrastructure Scanning
* Container Security Validation

## Future Enhancements

* ArgoCD GitOps Integration
* Service Mesh Implementation
* Multi-Region Deployment
* Disaster Recovery Automation
* Cost Optimization Dashboard

## Author

Komlavi Gidi

DevOps Engineer | Platform Engineer | Cloud Engineer

LinkedIn:
https://www.linkedin.com/in/komlavi-gidi-580455368

GitHub:
https://github.com/amenvi18-tech
