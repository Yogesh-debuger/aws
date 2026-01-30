# CloudShield: Secure AWS VPC with EC2

## 📌 Project Overview

This project demonstrates the design and implementation of a **secure, production-style AWS Virtual Private Cloud (VPC)** with EC2 instances deployed across public and private subnets. The focus is on **network security, routing, access control, and cost-aware cloud practices**.

The project reflects a real-world cloud infrastructure scenario where applications are securely exposed to the internet while backend resources remain isolated.

---

## 🏗️ Architecture Summary

* Custom VPC with defined CIDR block
* Public and private subnets
* Internet Gateway for public access
* NAT Gateway / NAT Instance for private subnet outbound access
* EC2 instances deployed in both subnets
* Security Groups and Network ACLs for traffic control
* IAM Roles for secure instance permissions

(Refer to `architecture-diagram.png` for visual representation)

---

## 🧰 Tech Stack & Services Used

* **Amazon VPC**
* **Amazon EC2**
* **Internet Gateway (IGW)**
* **NAT Gateway / NAT Instance**
* **Route Tables**
* **Security Groups**
* **Network ACLs**
* **AWS IAM (Roles & Policies)**
* **Linux (Amazon Linux)**
* **SSH Key Pair Authentication**
* **python3 for hosting ec2 instance**
---

## 🔐 Security Implementation

* Configured **Security Groups** to allow only required ports (SSH, HTTP/HTTPS)
* Implemented **Network ACLs** for subnet-level traffic filtering
* Used **IAM Roles** instead of hardcoded credentials
* SSH access restricted via **key-pair authentication only**

---

## 🚀 EC2 Provisioning Details

* EC2 instance launched in **public subnet** for internet-facing access
* EC2 instance launched in **private subnet** for internal communication
* Instances configured with appropriate security groups
* IAM roles attached to manage AWS resource access securely

---

## 🌐 Networking & Routing

* Internet Gateway attached to VPC for public subnet access
* NAT Gateway / NAT Instance configured for private subnet outbound traffic
* Separate route tables created and associated with respective subnets

---

## 🔑 Access Control

* SSH key pair generated and private key securely stored
* SSH access tested using key-based authentication
* IAM policies applied following least-privilege principle

---

## 🧪 Testing & Validation

* Verified SSH access to EC2 instances
* Tested internet connectivity from public subnet
* Validated outbound internet access from private subnet via NAT
* Confirmed security group and NACL rules functionality

---

## 📸 Screenshots & Proof of Work

Screenshots are provided in the `screenshots/` directory:

* EC2 instance running
* Website/application successfully launched on EC2 instances

---

## 💰 Cost Optimization Note

To avoid unnecessary AWS charges, all resources were **stopped after successful validation**. The infrastructure can be redeployed at any time using the same configuration.

---

## 🎯 Learning Outcomes

* Practical understanding of AWS VPC architecture
* Hands-on experience with secure networking and routing
* Improved knowledge of IAM roles and access control
* Awareness of AWS cost management best practices

---
