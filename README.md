# Multi-Cloud Network Architecture (AWS + Azure) 🌐

## Overview

This project explores how foundational cloud networking concepts translate across AWS and Microsoft Azure by designing equivalent network architectures in both environments.

The goal is to understand not just how to build networks, but how design decisions impact security, scalability, and connectivity across cloud platforms.

---

## Architecture

**Azure:**
VNet → Subnets → NSG → Public Access

**AWS:**
VPC → Subnet → Route Table → Internet Gateway → EC2

---

## Key Components

### Azure
- Virtual Network (VNet) for isolated networking
- Subnet segmentation for workload separation
- Network Security Groups (NSGs) for traffic control

### AWS
- VPC with CIDR block (10.0.0.0/16)
- Public subnet (10.0.10.0/24)
- Internet Gateway for external connectivity
- Route tables to control traffic flow
- Security Groups for instance-level access control
- EC2 instance deployed and validated via HTTP

---

## Architecture Mapping

| Concept            | Azure             | AWS               |
|------------------|------------------|------------------|
| Network          | VNet             | VPC              |
| Subnet           | Subnet           | Subnet           |
| Security         | NSG              | Security Group   |
| Routing          | System/User Routes | Route Tables    |
| Internet Access  | Public IP / Gateway | Internet Gateway |

---

## Security Design

- Controlled inbound traffic using NSG / Security Groups
- Limited exposure to only required ports (SSH, HTTP)
- Segmentation using subnets
- Applied principle of least privilege

---

## Business Impact

Understanding multi-cloud networking enables organizations to:

- **Maintain flexibility** across cloud providers (avoid vendor lock-in)
- **Standardize architecture patterns** across platforms
- **Improve security posture** through consistent network design principles
- **Accelerate cloud adoption** by reducing learning curve across environments
- **Design resilient systems** that can scale across regions and providers

---

## Trade-offs & Design Decisions

- Used **public subnet for simplicity**:
  - Easier validation and testing
  - Not production-ready (would require private subnets + NAT)

- Separate security controls (NSG vs Security Groups):
  - Azure provides subnet-level control
  - AWS focuses more on instance-level control

- CIDR planning:
  - Ensures scalability and prevents IP conflicts in larger environments

---

## Key Learnings

- Core networking concepts remain consistent across cloud providers
- Security and routing are critical to system reliability
- Network design directly impacts scalability and cost
- Multi-cloud knowledge improves architectural flexibility

---

## Next Steps

- Implement private subnets + NAT Gateway
- Add Load Balancer for high availability
- Build multi-tier architecture (web + app + DB)
- Automate infrastructure using Terraform
- Compare cost and performance between AWS and Azure

---

## Author

Jesus Velasquez  
Cloud Learner | Focused on Cloud Architecture, Networking, and System Design
