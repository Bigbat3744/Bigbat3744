# Hi, I'm Olaitan Soyoye 👋

**AWS Certified Solutions Architect – Associate** · Cloud engineer (AWS, Terraform, Python) · Scotland, UK · Open to Cloud, Platform and DevOps Engineer roles

I build and run cloud infrastructure in my own AWS account, and I work the way teams do: everything in Terraform, every change through a pull request with automated checks, least-privilege IAM, monitoring with real alarms, and honest write-ups of what broke and how I fixed it.

---

## ⭐ Featured project

### ☁️ [CloudOps Insight Hub](https://github.com/Bigbat3744/cloudops-insight-hub)
Serverless AWS cost monitoring. A scheduled Lambda collects spend by service from Cost Explorer into DynamoDB, and a separate read-only Lambda serves it through a throttled API Gateway HTTP API.

- **Security:** separate collector and reader roles scoped to exact ARNs, proven with `iam simulate-principal-policy`; input validation and safe error responses
- **Monitoring:** 5 CloudWatch alarms → SNS email, including one that detects a missed daily run; a dashboard, access logs and X-Ray
- **CI/CD:** GitHub Actions signs in to AWS with **OIDC (no stored keys)**; `fmt`, `validate`, `tflint`, a blocking Checkov scan and `terraform plan` on every PR
- **Troubleshooting:** load-test 503s diagnosed from metrics as the Lambda concurrency limit; incidents documented in the README

`Terraform` `Lambda` `DynamoDB` `API Gateway` `EventBridge` `CloudWatch` `SNS` `X-Ray` `IAM` `GitHub Actions` `Python`

---

## 🧱 More projects

### 🌐 [Terraform VPC Lab](https://github.com/Bigbat3744/terraform-vpc-lab)
A two-tier AWS network in Terraform: public and private subnets with a bastion pattern. SSH and HTTP are restricted to a single IP, the private tier only accepts traffic from the web tier's security group, outbound rules are explicit and IMDSv2 is required. It uses no NAT gateway to keep cost low, and `terraform destroy` removes everything.

`Terraform` `VPC` `EC2` `Security Groups` `IAM`

### 🔀 [Multi-Cloud Job Aggregator](https://github.com/Bigbat3744/multi-cloud-devops-job-aggregator)
A FastAPI backend on Azure Container Apps with DynamoDB storage and an S3 frontend, deployed through a GitHub Actions pipeline with a staging → health check → production gate. The Azure backend was decommissioned when the trial credits expired, and the full stack runs locally.

`Azure Container Apps` `Docker` `FastAPI` `DynamoDB` `S3` `GitHub Actions`

### 🧠 [Daily Challenge Generator](https://github.com/Bigbat3744/daily-challenge-generator)
A serverless coding-challenge API (API Gateway REST API, Lambda, DynamoDB) with an S3-hosted frontend, built with Terraform. The README documents the IAM, CORS and state-management problems I hit and how I solved them.

`Lambda` `API Gateway` `DynamoDB` `S3` `Terraform`

---

## 🛠️ Tools I use

| Cloud | IaC & CI | Observability | Languages |
|---|---|---|---|
| AWS (primary), Azure | Terraform, GitHub Actions, OIDC, tflint, Checkov | CloudWatch, X-Ray, SNS | Python, Bash |

---

## 📫 Connect

- 💼 [LinkedIn](https://www.linkedin.com/in/olaitan-soyoye-5a91b6b9)
- 📧 soyoyeolaitan@yahoo.com
