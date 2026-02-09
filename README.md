#  Secure Azure Virtual Machine Lab (Junior Cloud Engineer)

##  Overview

This project demonstrates foundational cloud engineering skills using Microsoft Azure, focused on secure deployment, access control, and troubleshooting. The lab simulates a real-world junior cloud support scenario by deploying and securing a virtual machine within a controlled network environment.

**Goal:** Gain hands-on experience with Azure infrastructure while applying security best practices, least-privilege access, and structured troubleshooting techniques.

---

##  Architecture

The lab includes the following Azure resources:

* Resource Group
* Virtual Network (VNet)
* Subnet
* Network Security Group (NSG)
* Windows Virtual Machine
* Azure Active Directory (Azure AD) user
* Role-Based Access Control (RBAC)
* Azure Monitor (basic metrics & activity logs)

---

##  Technologies Used

* Microsoft Azure
* Azure Virtual Machines
* Azure Virtual Network (VNet)
* Network Security Groups (NSG)
* Azure Active Directory
* Role-Based Access Control (RBAC)
* Azure Monitor
* Windows Server / Windows OS

---

##  Lab Objectives

* Deploy a Windows virtual machine in Azure
* Configure network segmentation using VNets and subnets
* Secure inbound traffic using Network Security Groups
* Implement least-privilege access using Azure RBAC
* Monitor and troubleshoot VM availability and connectivity
* Practice safe configuration changes in a cloud environment

---

##  Implementation Steps

### 1. Resource Group

Created a dedicated resource group to logically organize all lab resources and simplify management and cleanup.

### 2. Virtual Network & Subnet

Configured a virtual network with a private address space and a subnet to isolate the virtual machine.

### 3. Network Security Group

Applied an NSG to restrict inbound traffic:

* Allowed RDP (port 3389) only from my public IP address
* Denied all other inbound traffic by default

This configuration follows least-privilege and zero-trust principles.

### 4. Virtual Machine Deployment

Deployed a Windows-based Azure virtual machine and validated connectivity using Remote Desktop Protocol (RDP).

### 5. Identity & Access Management

Created an Azure AD test user and assigned a Reader role at the resource group level using RBAC to demonstrate controlled access and separation of duties.

### 6. Monitoring & Troubleshooting

Enabled Azure Monitor to observe VM metrics and activity logs.
Performed basic troubleshooting by intentionally modifying NSG rules to simulate connectivity issues and then resolving them.

---

##  Security Considerations

* Restricted management access to a single trusted IP
* Used RBAC instead of shared credentials
* Avoided assigning Owner-level permissions unnecessarily
* Followed structured change and validation steps

---

##  What I Learned

* How Azure networking components work together
* How to secure cloud resources using NSGs and RBAC
* How to troubleshoot VM connectivity issues
* The importance of monitoring and documentation in cloud environments
* How cloud security differs from on-prem systems
