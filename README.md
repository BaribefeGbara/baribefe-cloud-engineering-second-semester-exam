# Cloud Engineering Second Semester Examination Project

Deploy a Load-Balanced Website on AWS EC2 with Ansible Automation

## Project Overview

This project demonstrates the deployment of a highly available web application on AWS infrastructure using modern DevOps practices. The implementation includes automated configuration management, load balancing, and a comparison between compute-based (EC2) and storage-based (S3) hosting solutions.

## Architecture

```
Internet
    ↓
Classic Load Balancer
    ↓
┌─────────────────────┐
│                     │
EC2 Instance 1    EC2 Instance 2
(us-east-1a)      (us-east-1b)
    │                 │
    └─────────────────┘
         NGINX
```

## Features

- **High Availability**: Multi-AZ deployment with 2 EC2 instances
- **Load Balancing**: Classic Load Balancer for traffic distribution
- **Automation**: Ansible playbook for consistent server configuration
- **Dynamic Content**: Server-specific IP and hostname display
- **Security**: Properly configured security groups following least privilege principle
- **Comparison**: S3 static website hosting for cost/performance analysis

## Technologies Used

- **Cloud Provider**: AWS (EC2, VPC, Classic Load Balancer, S3)
- **Operating System**: Ubuntu 22.04 LTS
- **Web Server**: NGINX
- **Configuration Management**: Ansible
- **Version Control**: Git/GitHub
- **Infrastructure**: Custom VPC with multi-AZ architecture

## Project Structure

```
.
├── index.html              # HTML page with dynamic placeholders
├── ansible/
│   ├── inventory.ini       # Ansible inventory file
