# AWS Telemetry Platform Infrastructure (Terraform)

Modular Infrastructure as Code (IaC) provisioning resilient AWS architecture for high-throughput telemetry ingestion.

## Modules
- `modules/vpc`: Multi-AZ VPC with public and private subnets, NAT Gateway, and flow logs.
- `modules/ecs`: AWS ECS Fargate cluster with least-privilege IAM execution roles.
- `modules/s3`: Encrypted raw telemetry storage with KMS CMK and lifecycle rules.
- `modules/sqs`: Dead-letter queue (DLQ) backed FIFO ingestion pipeline.

## Usage
```bash
cd environments/dev
terraform init
terraform plan
```
