# ENTERPRISE-WEB
Deploying and enterprise web in huawei cloud lab 
# 🌐 Deploying an Enterprise Web on Huawei Cloud

## 📌 Project Overview
This mini project demonstrates the deployment of a cloud-based enterprise web solution on **Huawei Cloud** using the following key components:
- **Elastic Cloud Server (ECS)**
- **Relational Database Service (RDS)**
- **Elastic Load Balancer (ELB)**
- **Auto Scaling (AS)**
- **WordPress CMS (via LAMP stack)**

---

## 🛠 Technologies Used
- Huawei Cloud VPC, ECS, RDS, ELB, Auto Scaling
- CentOS 7.6
- LAMP Stack: Linux, Apache, MySQL, PHP
- WordPress 4.9.10
- GitHub, LinkedIn (for publishing and showcasing)

---

## ✅ Step-by-Step Deployment

### 1. **Create a VPC**
- Region: AP-Singapore
- Created a VPC `vpc-mp` with default subnet

### 2. **Configure Security Group**
- Created a security group `sg-mp`
- Added inbound rule: Allow All (0.0.0.0/0) temporarily for easy access

### 3. **Launch ECS Instance**
- ECS Name: `ecs-mp`
- Image: CentOS 7.6 (40 GB)
- Specs: 1 vCPU, 1 GB RAM
- Public EIP attached
- Used for Apache + PHP setup

### 4. **Install LAMP Stack**
```bash
yum install -y httpd php php-fpm php-mysql mysql
systemctl start httpd
systemctl start php-fpm
systemctl enable httpd
systemctl enable php-fpm
