# 🚀 Ansible + Terraform Multi-Node Infrastructure Automation

This project demonstrates how to automate **infrastructure provisioning using Terraform** and **server configuration using Ansible** in a real-world DevOps setup.

---

## 📌 Project Overview

- Provisioned AWS EC2 instances using **Terraform**
- Configured servers using **Ansible Playbooks and Roles**
- Set up a **multi-node environment** with different Linux distributions
- Automated **Docker installation across all nodes**
- Used **Dynamic Inventory** to fetch infrastructure details automatically
- Generated Ansible inventory dynamically using **Terraform template**

---

## 🏗️ Infrastructure Setup

Using Terraform, the following infrastructure was created:

- 🖥️ **1 Control Plane Node**
- 🖥️ **3 Worker Nodes**

### 🐧 Operating Systems Used:
- Ubuntu  
- Amazon Linux  
- Red Hat Enterprise Linux (RHEL)

This setup simulates a **real-world heterogeneous environment**.

---

## ⚙️ Configuration Management (Ansible)

Ansible was used to automate server configuration:

### ✅ Key Features:
- Used **Ansible Roles** for modular and reusable configuration
- Created **Playbooks** to manage multiple nodes
- Installed and configured **Docker** on all servers
- Ensured consistency across different OS environments

---

## 🔄 Dynamic Inventory (Terraform + Template)

- Used **Terraform `templatefile` function** with `inventory.tpl`
- Generated Ansible inventory dynamically using `generate_inventory.tf`
- Automatically populated:
  - Public IPs
  - Private IPs
  - Host groups (control-plane, workers)
- Eliminated manual inventory file management

---

## 📂 Project Structure
ansible-for-devops/
│
├── inventories/
├── playbooks/
├── roles/
│ └── docker/
│ ├── tasks/
│ ├── handlers/
│ └── defaults/
│
├── terraform/
│ ├── ec2.tf
│ ├── key_pair.tf
│ ├── security_group.tf
│ ├── variables.tf
│ ├── generate_inventory.tf
│ ├── templates/
│ │ └── inventory.tpl
│ ├── outputs.tf
│
└── README.md
---
