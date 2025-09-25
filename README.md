# Create a ready-to-use README.md file for the user's GitHub profile repository.
content = """<!-- Profile README for github.com/othiagorpantoja -->

<h1 align="center">Hi, I'm Thiago Pantoja — Principal Solutions Architect (Staff+)</h1>

<p align="center">
  <b>Business Strategy × Platform Engineering · Multi-cloud · Cloud Governance · Security by Design · FinOps</b>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/thiagorpantoja"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin"></a>
  <a href="mailto:thiago.pantoja@easynext.consulting"><img alt="Email" src="https://img.shields.io/badge/Email-thiago.pantoja%40easynext.consulting-informational?logo=minutemailer"></a>
  <a href="https://wa.me/5511988010667"><img alt="WhatsApp SP" src="https://img.shields.io/badge/WhatsApp-(11)%2098801-0667-25D366?logo=whatsapp&labelColor=202020"></a>
  <a href="https://wa.me/5592984561928"><img alt="WhatsApp AM" src="https://img.shields.io/badge/WhatsApp-(92)%2098456-1928-25D366?logo=whatsapp&labelColor=202020"></a>
  <img alt="Location" src="https://img.shields.io/badge/Manaus,%20BR-UTC−03-9cf?logo=google-maps">
  <img alt="Languages" src="https://img.shields.io/badge/EN%20%7C%20PT--BR%20%7C%20ES-orange">
</p>

---

## TL;DR

Principal Solutions Architect (Staff+) at the intersection of **business strategy** and **Platform Engineering**.  
I design **multi-account/region** architectures across **AWS, Azure, GCP, and OCI** with **Cloud Governance**, **Security by Design**, and **FinOps** at the core.  
I standardize the **SDLC** with **IaC** (Terraform/CDK/Ansible/CloudFormation), **Kubernetes** (EKS/AKS/GKE/OKE), and **CI/CD** — delivering **scale, reliability, and cost optimization** in complex multi-cloud environments.

### Quick links
- 🔭 [Pinned projects](#-selected-projects)
- 🧭 [What I do](#-what-i-do)
- 🧰 [Tech stack](#-tech-stack)
- 🧪 [Impact metrics](#-how-i-measure-impact)
- 🤝 [Work with me](#-work-with-me)

---

## 🧭 What I do
- **Modernization & Migrations:** landing zones, Organizations, **policy-as-code**; networking (**TGW/DX**); containers (**ECS/Fargate/EKS**); **API Gateway**; **event-driven** integrations (EventBridge/SQS/Step Functions/Lambda); **service mesh**.  
- **Security & Compliance:** **Zero Trust**, **IAM/KMS**, **WAF/ALB**, account segmentation, **DR/Backup** compliance — tying technical decisions to **risk, cost, and time-to-market**.  
- **DevEx & Platform:** **IDP/Backstage**, service catalog & **golden paths** (opinionated templates in Terraform/CDK/K8s), reusable pipelines (**GitHub Actions**), **PR previews**, and **self-service with guardrails**.  
- **Observability & Reliability:** Prometheus/Grafana/Loki/**OpenTelemetry**, **SLOs** from day one.

---

## 🧰 Tech stack

> The list below reflects the tools and languages I use most often in platform & cloud architecture, delivery, and operations.

### Languages & Runtimes
`Java` · `C#` · `.NET` · `Node.js` · `TypeScript` · `JavaScript` · `PHP` · `Python` · `Go` · `Kotlin` · `Bash` · `PowerShell`

### Backend & Frameworks
`Spring Boot` · `Quarkus` · `ASP.NET Core` · `Razor/Blazor` · `Express` · `NestJS` · `FastAPI` · `Laravel`

### Frontend & Mobile
`React` · `Next.js` · `Vue` · `Angular` · `React Native`

### Datastores & Caching
`PostgreSQL` · `MySQL` · `SQL Server` · `MongoDB` · `Redis/Valkey` · `DynamoDB`

### Messaging & Integration
`SQS` · `SNS` · `EventBridge` · `Kafka/MSK` · `Kinesis` · `Step Functions` · `API Gateway` · `Apigee Edge` · `Camunda`

### Cloud Providers
`AWS` · `Azure` · `GCP` · `Oracle Cloud (OCI)`

### Containers, Orchestration & Packaging
`Docker` · `Kubernetes` (`EKS`, `AKS`, `GKE`, `OKE`) · `Helm` · `Karpenter` · `HPA/PDB` · `Service Mesh`

### IaC & Policy
`Terraform` · `AWS CDK` · `CloudFormation` · `Ansible` · `OPA/Conftest` · `Policy as Code`

### CI/CD & GitOps
`GitHub Actions` · `GitLab CI` · `Azure DevOps` · `Jenkins` · `Argo CD` · `Flux` · Blue/Green & Canary

### Observability & AIOps
`OpenTelemetry` · `Prometheus` · `Grafana` · `Loki` · `CloudWatch` · `Azure Monitor` · `GCP Monitoring` · `Dynatrace` · `New Relic` · `Zabbix` · `Elasticsearch/Kibana` · `PagerDuty` · `incident.io`

### Security by Design
`Zero Trust` · `WAF/ALB` · `IAM` · `KMS` · `Secrets Manager/Parameter Store/Vault` · `TLS 1.2/1.3` · Supply-chain security (SBOM, image signing with cosign)

### Architecture & Practices
`Platform Engineering` · `Platform Architect` · `SRE` · `System Design` · `Well-Architected` · `DORA` · `FinOps` (CUR/Athena/Glue, tagging, rightsizing, Savings Plans) · `LGPD` · `DevSecOps`

---

## 🚀 Selected projects

<details>
  <summary><b>FinOps Automation — CUR + Athena + Glue + PDF Insights</b></summary>
  <br/>
  Automated cost ingestion (CUR), ETL with Glue, Athena queries, scheduled reports with serverless functions, and PDF/HTML insights for stakeholders.<br/>
  <b>Highlights:</b> cost allocation by tag/account, rightsizing suggestions, Savings Plans/RIs coverage, monthly deltas and KPIs.<br/><br/>
  🔗 Repo: <a href="https://github.com/thiagorpantoja/finops-automation">thiagorpantoja/finops-automation</a>
</details>

<details>
  <summary><b>Chatwoot on ECS Fargate — Multi-tenant + ALB + WAF</b></summary>
  <br/>
  Production-grade deployment on ECS Fargate with RDS/Redis, ALB rules per host, WAF, TLS 1.2/1.3, and IaC modules.<br/>
  <b>Highlights:</b> blue/green ready, autoscaling policies, least-privilege IAM, KMS, and observability pack.<br/><br/>
  🔗 Repo: <a href="https://github.com/thiagorpantoja/chatwoot-ecs">thiagorpantoja/chatwoot-ecs</a>
</details>

<details>
  <summary><b>EKS Blueprints + Karpenter — SLO-first Platform</b></summary>
  <br/>
  EKS with Karpenter, OTel, Prometheus, Grafana, Loki, and Golden Paths templates for app teams.<br/>
  <b>Highlights:</b> IDP/Backstage onboarding, PR env previews, guardrails, SLOs from day one.<br/><br/>
  🔗 Repo: <a href="https://github.com/thiagorpantoja/eks-blueprints-slo">thiagorpantoja/eks-blueprints-slo</a>
</details>

---

## 🧪 A tiny taste of my templates

```hcl
# Terraform: opinionated S3 bucket with FinOps tags & security defaults
resource "aws_s3_bucket" "app_bucket" {
  bucket = var.bucket_name
  tags = merge(var.common_tags, {
    "cost-center" = var.cost_center
    "owner"       = var.owner
    "env"         = var.env
  })
}

resource "aws_s3_bucket_versioning" "v" {
  bucket = aws_s3_bucket.app_bucket.id
  versioning_configuration { status = "Enabled" }
}

resource "aws_s3_bucket_server_side_encryption_configuration" "sse" {
  bucket = aws_s3_bucket.app_bucket.id
  rule { apply_server_side_encryption_by_default { sse_algorithm = "aws:kms" } }
}

resource "aws_s3_bucket_public_access_block" "pab" {
  bucket                  = aws_s3_bucket.app_bucket.id
  block_public_acls       = true
  block_public_policy     = true
  ignore_public_acls      = true
  restrict_public_buckets = true
}
