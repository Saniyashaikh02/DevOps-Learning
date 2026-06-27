# ☁️ Cloud Infrastructure

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

Imagine you developed an amazing web application.

You tested it on your laptop, and everything works perfectly.

Now you want **10,000 users** to access it.

Can everyone connect to your laptop?

**No.**

Your laptop:

* Can be turned off
* Has limited CPU and RAM
* Uses a home internet connection
* Isn't designed to serve millions of users

This is why we need **Cloud Infrastructure**.

---

# What is Cloud Infrastructure?

Cloud Infrastructure means using computing resources such as servers, storage, networking, and databases over the internet instead of owning physical hardware.

Instead of buying your own servers, you **rent** them from cloud providers.

---

# Simple Definition

Cloud Infrastructure is a collection of virtual computing resources delivered over the internet on demand.

These resources include:

* Virtual Machines
* Storage
* Databases
* Networking
* Security
* Monitoring
* Load Balancers

---

# Traditional Infrastructure

Before cloud computing, companies bought physical servers.

```text
Company

↓

Buy Server

↓

Install Operating System

↓

Configure Network

↓

Install Software

↓

Deploy Application
```

Problems:

* Expensive
* Time-consuming
* Difficult to scale
* Requires maintenance

---

# Cloud Infrastructure

With cloud computing:

```text
Developer

↓

Cloud Provider

↓

Launch Server

↓

Deploy Application

↓

Users Access Website
```

You can create a server in minutes.

---

# Real-Life Example

Imagine you need a car.

### Traditional Way

Buy the car.

* Pay ₹10,00,000
* Insurance
* Maintenance
* Fuel

### Cloud Way

Use Uber.

Pay only when you need it.

Cloud computing works the same way.

---

# Why Do We Need Cloud?

Without Cloud:

* Buy servers
* Install hardware
* Replace failed disks
* Upgrade RAM
* Handle power failures

With Cloud:

Everything is managed by the provider.

---

# Benefits of Cloud Infrastructure

* Pay only for what you use
* High Availability
* Easy Scaling
* Global Access
* Better Security
* Automatic Backups
* Disaster Recovery

---

# Types of Cloud

## 1. Public Cloud

Infrastructure owned by cloud providers.

Examples:

* AWS
* Azure
* Google Cloud

Anyone can rent resources.

---

## 2. Private Cloud

Infrastructure used by only one organization.

Advantages:

* More control
* Better security

Disadvantages:

* Expensive

---

## 3. Hybrid Cloud

Combination of Public + Private Cloud.

Example:

Sensitive data stays in a private cloud.

Applications run in the public cloud.

---

# Popular Cloud Providers

## Amazon Web Services (AWS)

Largest cloud platform.

Services:

* EC2
* S3
* IAM
* VPC
* RDS
* Lambda

---

## Microsoft Azure

Popular among enterprise companies.

---

## Google Cloud Platform (GCP)

Known for:

* Kubernetes
* AI
* Big Data

---

# Core Cloud Services

## Compute

Virtual machines used to run applications.

AWS Service:

EC2 (Elastic Compute Cloud)

---

## Storage

Store files, images, videos, backups.

AWS Service:

S3 (Simple Storage Service)

---

## Database

Store application data.

AWS Services:

* RDS
* DynamoDB

---

## Networking

Connect servers securely.

AWS Service:

VPC (Virtual Private Cloud)

---

## Security

Manage users and permissions.

AWS Service:

IAM (Identity and Access Management)

---

## Load Balancer

Distributes traffic among multiple servers.

```text
Users

↓

Load Balancer

↓

Server 1

Server 2

Server 3
```

Benefits:

* Better performance
* High availability
* Fault tolerance

---

# Virtual Machine (VM)

A Virtual Machine is a software-based computer.

It behaves like a real computer but runs inside a physical server.

Example:

One physical server can host many VMs.

```text
Physical Server

│

├── VM1

├── VM2

├── VM3

└── VM4
```

---

# AWS EC2

EC2 stands for Elastic Compute Cloud.

It allows you to launch Linux or Windows virtual machines.

Common uses:

* Host websites
* Run applications
* Testing
* Development
* Databases

---

# AWS S3

S3 is object storage.

Used to store:

* Images
* Videos
* Documents
* Backups
* Static websites

Advantages:

* Highly Durable
* Scalable
* Secure

---

# AWS IAM

IAM controls:

* Users
* Groups
* Roles
* Permissions

Never share the Root Account.

Create IAM users for daily work.

---

# AWS VPC

VPC stands for Virtual Private Cloud.

Think of it as your private network inside AWS.

Inside a VPC you can create:

* Public Subnets
* Private Subnets
* Route Tables
* Internet Gateway

---

# AWS RDS

RDS stands for Relational Database Service.

Supported databases:

* MySQL
* PostgreSQL
* MariaDB
* SQL Server

Benefits:

* Automatic Backups
* High Availability
* Easy Scaling

---

# How Cloud Works

```text
Developer

↓

AWS Console

↓

Launch EC2

↓

Install Application

↓

Users Access Website
```

---

# Hands-on Practice

## Step 1

Create an AWS Free Tier account.

---

## Step 2

Launch an EC2 instance.

Choose:

* Ubuntu
* t2.micro
* Free Tier

---

## Step 3

Connect using SSH.

```bash
ssh ubuntu@your-server-ip
```

---

## Step 4

Update packages.

```bash
sudo apt update
```

---

## Step 5

Install Nginx.

```bash
sudo apt install nginx -y
```

---

## Step 6

Start Nginx.

```bash
sudo systemctl start nginx
```

---

## Step 7

Enable Nginx.

```bash
sudo systemctl enable nginx
```

---

## Step 8

Open Browser

```text
http://your-public-ip
```

You should see the Nginx welcome page.

Congratulations!

You deployed your first cloud server.

---

# Common Cloud Terms

| Term | Meaning          |
| ---- | ---------------- |
| EC2  | Virtual Machine  |
| S3   | Storage          |
| IAM  | User Management  |
| VPC  | Private Network  |
| RDS  | Managed Database |
| ALB  | Load Balancer    |

---

# Best Practices

* Never use Root User
* Enable MFA
* Use IAM Roles
* Delete unused resources
* Backup important data
* Monitor costs
* Keep Security Groups restricted

---

# Common Mistakes

❌ Leaving servers running

❌ Opening all ports (0.0.0.0/0)

❌ Using Root Account

❌ No backups

❌ Weak passwords

---

# Interview Questions

### What is Cloud Computing?

Cloud Computing is the delivery of computing resources over the internet.

---

### What is EC2?

EC2 is a virtual machine service provided by AWS.

---

### What is S3?

S3 is an object storage service.

---

### What is IAM?

IAM manages users and permissions.

---

### Difference between EC2 and S3?

EC2 runs applications.

S3 stores files.

---

# Summary

✔ Cloud replaces physical servers with virtual resources.

✔ AWS is the most popular cloud provider.

✔ Core AWS services:

* EC2
* S3
* IAM
* VPC
* RDS

✔ Cloud enables scalability, flexibility, and high availability.

✔ Every DevOps Engineer should understand cloud fundamentals before moving to CI/CD and Kubernetes.

