# Multi-Cloud Network Foundations (Azure + AWS)

## Overview
This project demonstrates foundational cloud networking concepts by building equivalent architectures in both Microsoft Azure and AWS.

The goal is to understand how core networking components translate across cloud providers.

---

##  Azure Implementation
- Created Virtual Network (VNet)
- Configured subnets (subnet-a, subnet-b)
- Associated Network Security Group (NSG)
- Managed IP addressing and segmentation

---

##  AWS Implementation
- Created VPC with CIDR block (10.0.0.0/16)
- Configured public subnet (10.0.10.0/24)
- Attached Internet Gateway
- Updated route tables for internet access
- Launched EC2 instance inside subnet
- Configured Security Group (SSH + HTTP)
- Installed Apache web server
- Validated connectivity via public IP

---

##  Architecture Comparison

| Azure | AWS |
|------|-----|
| VNet | VPC |
| Subnet | Subnet |
| NSG | Security Group |
| Routing | Route Tables |
| Public Access | Internet Gateway |

---

##  Key Learnings
- Network design is critical for security and scalability
- Proper CIDR planning prevents IP conflicts
- Security groups should follow least privilege principle
- Routing determines how traffic flows in/out of cloud environments

---

## Relevance to AWS SAA
This project reinforces:
- VPC design best practices
- Public vs Private subnet concepts
- Internet Gateway and routing
- EC2 networking
- Security group configurations

---

##  Next Steps
- Add private subnet + NAT Gateway
- Deploy multi-tier architecture
- Add Load Balancer
- Automate infrastructure with Terraform
