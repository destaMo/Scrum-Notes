+++
title = "AWS Services Basics"
+++

{{%bubble %}}

## AWS Services Basics

**Points:** X

**Description:** You understand AWS services that allow you to solve basic issues and implement most common requests.

**Person which succesfully completed requirement for given block can:**

- Work with most common AWS services
- Understand key features of AWS services
- Evaluate which service should be used for given scenario
- Use and configure AWS services based on requirements

{{% /bubble%}}

### 🎓 Learn
### 📝 Katas
**For this challange use configure it using terraform as described in the [IaaC Fundamentals](/iaac_fundamentals)**

Create a small AWS infrastructure for a simple Rails/Node app with simple frontend that can be found [here](). The following resources should be used and setup as in the following diagram:
- VPC and subnets
- ECS with EC2
- Elastic Cache (Redis)
- RDS - PostgreSQL
- S3 for files storage
- CloudFront for the front-end app
- Route53 for DNS setup
- AWS Cert Manager
- ALB
- NAT Gateway
- SQS
### 🎤 Interview
- When is the purpose of EBS?
- What is the general idea behind CloudFront?
- S3 events and file processing - describe a potential flow.
- Explain briefly S3 lifecycle and what can you achieve with it?
- How to spawn instances in two availability zones?
- What is the purpose of EC2 keys?
- AMI - pros and cons.
- Explain when would you use custom AMI and when user-data?
- Describe the difference between EC2 instance types across regions.
- Describe metrics in CloudWatch for a running service.


