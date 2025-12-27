# 🌐 Cross-Cloud Site-to-Site VPN: AWS ↔ Microsoft Azure

## 📌 Project Overview

<p>This project demonstrates the design and implementation of a secure Site-to-Site VPN connection between Amazon Web Services (AWS) and Microsoft Azure, enabling private, bi-directional communication between virtual machines hosted in two different cloud environments.

The solution follows cloud security best practices by hosting workloads in private subnets and eliminating direct public access. </p>

## 🎯 Objectives

- Enable secure private communication between AWS EC2 and Azure Virtual Machines
- Implement a multi-cloud networking architecture
- Apply network security controls and identity-based access
- Gain hands-on experience with VPN gateways and routing

## 🏗️ Architecture Overview

High-Level Design

- AWS VPC with Public & Private Subnets
- Azure Virtual Network with Gateway Subnet & Workload Subnet
- Site-to-Site IPSec VPN Tunnel between AWS and Azure
  
![image]()

## ☁️ AWS Architecture

- Amazon VPC
  - Public Subnet (NAT Gateway)
  - Private Subnet (EC2 Instance)
- NAT Gateway for controlled outbound internet access
- Virtual Private Gateway (VGW)
- Customer Gateway
- VPN Connection
- IAM Role + AWS Systems Manager
  - Secure VM access without SSH keys
