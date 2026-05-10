# PayShield
Secure Payment Processing System Architecture on AWS

![AWS Architecture](./assets/architecture-preview.png)

## Live Demo

🔗 https://tannu610.github.io/PayShield/

---

## Overview

PayShield is an interactive AWS cloud architecture visualization that demonstrates how a secure, production-style payment processing system can be designed using modern cloud infrastructure principles.

The project focuses on:

- High Availability
- Secure Network Design
- Multi-AZ Deployment
- Private Subnet Isolation
- Load Balancing
- Database Failover
- Monitoring and Observability

---

## Architecture Components

### Networking
- Amazon VPC
- Internet Gateway
- Public & Private Subnets
- Multi-AZ Architecture

### Compute
- EC2 Backend Instances
- Bastion Host
- Auto Scaling Ready Design

### Traffic Management
- Application Load Balancer (ALB)
- HTTPS Request Handling

### Database
- Amazon RDS
- Multi-AZ Replication
- Private DB Subnets

### Monitoring
- Amazon CloudWatch
- Logs, Metrics, and Alarms

### Security
- Security Groups
- Least-Privilege Access
- Private Application Layer
- Restricted SSH Access

---

## Request Flow

### 1. User Request
Users send HTTPS requests through the Internet Gateway to the Application Load Balancer.

### 2. Load Balancing
The ALB distributes traffic across backend EC2 instances running in private subnets.

### 3. Database Communication
Application servers securely communicate with Amazon RDS inside isolated database subnets.

### 4. Response Flow
Responses are securely returned back to users through the ALB over HTTPS.

---

## Security Design

- EC2 instances are not publicly accessible
- Database instances remain isolated in private DB subnets
- Security Groups enforce least-privilege communication
- SSH access is restricted through a Bastion Host
- Only ALB can communicate with backend EC2 instances
- Only backend servers can access the database

---

## Features

- Interactive request flow visualization
- Step-by-step traffic tracing
- Multi-AZ infrastructure representation
- Production-style AWS architecture
- Modern responsive UI
- Security-focused infrastructure design

---

## Technologies Used

- HTML5
- CSS3
- JavaScript
- AWS Architecture Concepts
- GitHub Pages

---

## Local Setup

Clone the repository:

```bash
git clone https://github.com/tannu610/PayShield.git
