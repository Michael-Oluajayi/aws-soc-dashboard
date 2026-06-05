# AWS SOC Monitoring Dashboard

## Overview
This project deploys a Security Operations Center (SOC) monitoring setup on AWS using Terraform. It captures all account activity, stores logs securely, and sends real-time alerts when suspicious activity is detected.

## Architecture
- **CloudTrail** — Logs every API call and action taken in the AWS account
- **S3 Bucket** — Secure storage for all CloudTrail logs
- **CloudWatch Log Group** — 30 day log retention for analysis
- **CloudWatch Alarm** — Triggers on unauthorized API calls
- **SNS Topic** — Sends email alerts when threats are detected

## Security Features
- Full API activity logging across all regions
- Log file validation enabled — detects tampering
- Real-time alerting on unauthorized access attempts
- Logs stored in encrypted, public-access-blocked S3 bucket
- 30 day log retention for incident investigation

## Tools Used
- Terraform v1.15.5
- AWS CLI
- AWS Services: CloudTrail, CloudWatch, SNS, S3

## How to Deploy
1. Clone this repository
2. Configure AWS credentials: `aws configure`
3. Update your email in `main.tf` for SNS alerts
4. Initialize Terraform: `terraform init`
5. Preview changes: `terraform plan`
6. Deploy: `terraform apply`
7. Confirm your SNS email subscription

## What I Learned
This project taught me how to set up real-time security monitoring on AWS. I learned how CloudTrail captures every action in an account, how to route alerts through SNS, and how to build detection rules using CloudWatch alarms — skills directly used by SOC analysts every day.

## Author
Michael Olu-Ajayi — Aspiring Cloud Security Engineer