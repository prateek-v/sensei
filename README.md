# EKS Terraform Pipeline

This repository provisions an Amazon EKS cluster using Terraform with automated GitHub Actions for validation and deployment.

## Features
- Validate Terraform code on PR
- Comment `terraform plan` output on PR
- Auto-deploy on merge to `main`
- Backup Terraform files to S3

## Prerequisites
- AWS credentials in GitHub Secrets
- S3 bucket + DynamoDB for backend state
- IAM permissions for GitHub Actions

## Usage
1. Create a PR to change Terraform code
2. On approval and merge, GitHub Action applies the changes
3. EKS cluster is created/updated# sensei
