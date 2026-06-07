# aws-project-3...
# AWS VPC Creation
Name : Siggari Naga Teja

Code tech intern id : CITS802

## Overview

This project provisions an AWS Virtual Private Cloud (VPC) along with the essential networking components required to build a secure and scalable cloud environment.

## Resources Created

- VPC
- Public Subnet
- Private Subnet
- Internet Gateway
- Route Tables
- Route Table Associations
- Security Groups

## Architecture

```text
Internet
    |
    |
Internet Gateway
    |
+-----------------------+
|        VPC            |
|    10.0.0.0/16        |
|                       |
| +-------------------+ |
| | Public Subnet     | |
| | 10.0.1.0/24       | |
| +-------------------+ |
|                       |
| +-------------------+ |
| | Private Subnet    | |
| | 10.0.2.0/24       | |
| +-------------------+ |
+-----------------------+
```

## Prerequisites

- AWS Account
- AWS CLI configured
- Required IAM permissions
- Terraform installed

## Deployment

Initialize Terraform:

```bash
terraform init
```

Validate configuration:

```bash
terraform validate
```

Review execution plan:

```bash
terraform plan
```

Apply the configuration:

```bash
terraform apply
```

## Outputs

After successful deployment, the following outputs are available:

- VPC ID
- Public Subnet ID
- Private Subnet ID
- Internet Gateway ID

## Verification

Verify the created resources through:

- AWS Management Console
- AWS CLI commands

Example:

```bash
aws ec2 describe-vpcs
aws ec2 describe-subnets
```

## Cleanup

To delete all created resources:

```bash
terraform destroy
```

## Project Structure

```text
.
├── main.tf
├── variables.tf
├── outputs.tf
├── provider.tf
├── terraform.tfvars
└── README.md
```

## License

This project is licensed under the MIT License.
