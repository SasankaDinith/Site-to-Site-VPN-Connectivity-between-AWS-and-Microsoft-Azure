# 🌐 Cross-Cloud Site-to-Site VPN: AWS ↔ Microsoft Azure

## Project Overview

<p>This project demonstrates the design and implementation of a secure Site-to-Site VPN connection between Amazon Web Services (AWS) and Microsoft Azure, enabling private, bi-directional communication between virtual machines hosted in two different cloud environments.

The solution follows cloud security best practices by hosting workloads in private subnets and eliminating direct public access. </p>
---
## Objectives

- Enable secure private communication between AWS EC2 and Azure Virtual Machines
- Implement a multi-cloud networking architecture
- Apply network security controls and identity-based access
- Gain hands-on experience with VPN gateways and routing
---
## Architecture Overview

High-Level Design

- AWS VPC with Public & Private Subnets
- Azure Virtual Network with Gateway Subnet & Workload Subnet
- Site-to-Site IPSec VPN Tunnel between AWS and Azure
  
![image](https://github.com/SasankaDinith/Site-to-Site-VPN-Connectivity-between-AWS-and-Microsoft-Azure/blob/5eed4c3cc8f47030a7365c6f3cd885ff9bdfdf31/Project%20Diagram.jpeg)

---

## AWS Architecture

- Amazon VPC
  - Public Subnet (NAT Gateway)
  - Private Subnet (EC2 Instance)
- NAT Gateway for controlled outbound internet access
- Virtual Private Gateway (VGW)
- Customer Gateway
- VPN Connection
- IAM Role + AWS Systems Manager
  - Secure VM access without SSH keys

 ---

## Azure Architecture

- Resource Group
- Virtual Network (VNet)
  - GatewaySubnet
  - Workload Subnet
- Azure Virtual Network Gateway
- Local Network Gateway
- Network Security Group (NSG)
  - Traffic filtering (Allow/Deny rules)
- Azure Virtual Machine in Workload Subnet

---
## Security Features

- No public IP assigned to AWS EC2 or Azure VM
- Private IP communication over IPSec VPN
- Controlled outbound access via NAT Gateway
- IAM-based access using AWS Systems Manager
- NSG rules to restrict Azure network traffic
---

## Network Flow

- AWS EC2 instance (private subnet) initiates traffic
- Traffic routed through AWS VPN Gateway
- Encrypted IPSec tunnel established to Azure Virtual Network Gateway
- Azure VM receives traffic via private IP
- Bi-directional communication enabled

---

## Technologies Used

#### AWS

Amazon VPC | EC2 | NAT Gateway | VPC | Customer Gateway | VPN Connection | IAM | AWS System Manager 

#### Azure

Virtual Network (VNet) | Virtual Network Gateway | Local Network Gateway | Network Security Group (NSG) | Azure Virtual Machine 


---

## Key Outcomes

- 100% private cross-cloud communication
- Zero public IP exposure
- Secure and reliable multi-cloud connectivity
- Hands-on experience in hybrid cloud networking
---

## Licence
This project is licensed under the MIT License.





