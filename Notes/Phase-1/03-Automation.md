# 🤖 Automation in DevOps

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

Imagine you work as a DevOps Engineer.

Every morning you have to:

* Login to the server
* Pull the latest code
* Install dependencies
* Build the application
* Restart the server
* Check logs
* Notify your team

Now imagine doing this **every single day**.

It is:

* Time-consuming
* Repetitive
* Error-prone

This is where **Automation** comes in.

---

# What is Automation?

Automation means using scripts, software, or tools to perform repetitive tasks **without manual intervention**.

Instead of doing tasks yourself every day, you let a computer execute them.

---

# Simple Definition

**Automation is the process of performing repetitive tasks automatically using scripts or software, reducing manual effort, increasing speed, and minimizing human errors.**

---

# Real-Life Example

Imagine switching on your home lights manually every evening.

Now imagine installing a smart light that turns on automatically at sunset.

That is automation.

Software systems work the same way.

---

# Before Automation

```text
Developer Pushes Code

↓

Login Server

↓

Copy Files

↓

Install Packages

↓

Restart Server

↓

Check Logs

↓

Inform Team
```

Time Taken:

20–30 minutes

---

# After Automation

```text
Developer Pushes Code

↓

Automation Script

↓

Everything Happens Automatically
```

Time Taken:

2–3 minutes

---

# Why Do We Need Automation?

Without automation:

* Repetitive work
* Human errors
* Slow deployments
* Inconsistent environments
* More downtime

With automation:

* Faster deployments
* Consistent results
* Fewer mistakes
* Increased productivity
* Better reliability

---

# Benefits of Automation

* Saves Time
* Reduces Human Errors
* Faster Software Delivery
* Improves Reliability
* Better Productivity
* Easy Scaling
* Consistency

---

# Where is Automation Used?

Automation is used almost everywhere in DevOps.

Examples:

* Code Deployment
* Testing
* Build Process
* Infrastructure Provisioning
* Server Configuration
* Monitoring
* Backups
* Security Scanning

---

# Automation Workflow

```text
Developer

↓

Git Push

↓

GitHub Actions

↓

Build

↓

Test

↓

Deploy

↓

Notify Team
```

---

# Types of Automation

## 1. Build Automation

Automatically compile source code.

Example:

```text
Git Push

↓

Compile

↓

Package
```

---

## 2. Testing Automation

Automatically run unit tests.

```text
Code

↓

Tests

↓

Report
```

---

## 3. Deployment Automation

Automatically deploy applications.

Example:

```text
Git Push

↓

Server Updated Automatically
```

---

## 4. Infrastructure Automation

Create servers automatically.

Instead of clicking buttons,

write code.

Tools:

* Terraform
* AWS CloudFormation

---

## 5. Configuration Automation

Install software automatically.

Tools:

* Ansible
* Puppet
* Chef

---

# Automation Tools

Popular DevOps Automation Tools:

| Tool           | Purpose                   |
| -------------- | ------------------------- |
| Bash           | Linux Automation          |
| PowerShell     | Windows Automation        |
| Python         | General Automation        |
| GitHub Actions | CI/CD Automation          |
| Jenkins        | Pipeline Automation       |
| Terraform      | Infrastructure Automation |
| Ansible        | Configuration Automation  |

---

# Bash Automation

Example:

Create

```text
deploy.sh
```

Content:

```bash
#!/bin/bash

echo "Updating Code..."

git pull

echo "Installing Packages..."

npm install

echo "Running Tests..."

npm test

echo "Building Project..."

npm run build

echo "Restarting Application..."

pm2 restart app

echo "Deployment Completed Successfully!"
```

Run:

```bash
chmod +x deploy.sh

./deploy.sh
```

---

# PowerShell Automation

Windows Example:

```powershell
Write-Host "Hello DevOps"

Get-Date

Get-Process
```

---

# Python Automation

Example:

```python
import os

print("Updating project...")

os.system("git pull")

os.system("npm install")

os.system("npm test")
```

---

# Real-World Scenario

Imagine Netflix has:

* 20,000 servers
* Millions of users

Do you think engineers manually update each server?

No.

Automation handles everything.

---

# CI/CD Automation

Developer pushes code.

```text
Git Push

↓

GitHub Actions

↓

Build

↓

Tests

↓

Docker Image

↓

Deploy

↓

Users
```

Everything happens automatically.

---

# Hands-on Practice

## Step 1

Create a folder.

```bash
mkdir automation-demo

cd automation-demo
```

---

## Step 2

Create a Bash script.

```text
deploy.sh
```

Content:

```bash
#!/bin/bash

echo "Hello DevOps"

echo "Today's Date"

date

echo "Current Directory"

pwd
```

Run:

```bash
chmod +x deploy.sh

./deploy.sh
```

---

## Step 3

PowerShell Practice

Create:

```text
hello.ps1
```

Content:

```powershell
Write-Host "Hello DevOps"

Get-Date

Get-Location
```

Run:

```powershell
.\hello.ps1
```

---

# Practical DevOps Example

Without Automation

```text
Developer

↓

Login Server

↓

Install Packages

↓

Restart Server

↓

Check Logs

↓

Deployment Complete
```

With Automation

```text
Developer

↓

Git Push

↓

GitHub Actions

↓

Everything Automatic

↓

Deployment Complete
```

---

# Advantages

* Faster Releases
* Better Consistency
* Lower Costs
* Less Human Error
* Easier Maintenance
* Improved Reliability

---

# Disadvantages

* Initial Setup Takes Time
* Requires Learning Scripts
* Incorrect Automation Can Cause Problems
* Needs Regular Maintenance

---

# Best Practices

* Automate repetitive tasks only.
* Test automation scripts before production.
* Store scripts in Git.
* Keep scripts simple.
* Add comments.
* Avoid hardcoded passwords.
* Log every action.

---

# Common Mistakes

❌ Writing huge scripts

❌ No error handling

❌ No backups

❌ Hardcoded passwords

❌ No testing

---

# Real Company Example

When a developer pushes code to GitHub,

GitHub Actions automatically:

```text
Checkout Code

↓

Install Dependencies

↓

Run Tests

↓

Build Project

↓

Create Docker Image

↓

Deploy to Server

↓

Notify Slack
```

No engineer needs to manually deploy.

---

# Interview Questions

## What is Automation?

Automation is the process of performing repetitive tasks automatically using scripts or software.

---

## Why is Automation important?

* Saves Time
* Reduces Human Errors
* Improves Reliability
* Faster Deployments

---

## Name Automation Tools.

* Bash
* PowerShell
* Python
* Jenkins
* GitHub Actions
* Terraform
* Ansible

---

## What is a Script?

A script is a file containing commands executed automatically.

Example:

```bash
deploy.sh
```

---

# Summary

✔ Automation removes repetitive manual work.

✔ Scripts execute tasks automatically.

✔ DevOps heavily depends on automation.

✔ Automation increases speed, consistency, and reliability.

✔ Tools like Bash, PowerShell, Python, Jenkins, GitHub Actions, Terraform, and Ansible are widely used.

