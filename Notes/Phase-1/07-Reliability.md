# 🛡️ Reliability in DevOps

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

Imagine you own an online shopping website.

Today is **Diwali Sale**.

Millions of users are shopping at the same time.

Suddenly...

Your server crashes.

Customers cannot place orders.

The company loses money.

This is why **Reliability** is one of the most important goals in DevOps.

---

# What is Reliability?

Reliability is the ability of a system to perform its intended function continuously and correctly without failure.

A reliable system remains available, stable, and performs consistently even when something goes wrong.

---

# Simple Definition

**Reliability is the ability of an application or infrastructure to work correctly for a long period with minimal downtime and failures.**

---

# Why Reliability Matters

Imagine three websites.

Website A

```text
Works for 2 hours

↓

Crashes

↓

Restart
```

Website B

```text
Works for 8 hours

↓

Crashes
```

Website C

```text
Works 24×7

↓

Users Never Notice
```

Which one do users trust?

Obviously Website C.

---

# Goals of Reliability

A reliable system should provide:

* High Availability
* Fault Tolerance
* Fast Recovery
* Scalability
* Consistent Performance
* Data Protection

---

# High Availability (HA)

High Availability means your application remains available even if one server fails.

Example

```text
Users

↓

Load Balancer

↓

Server 1

Server 2

Server 3
```

If Server 2 crashes,

Traffic automatically moves to Server 1 and Server 3.

Users never notice.

---

# Fault Tolerance

Fault Tolerance means the system continues working even when hardware or software components fail.

Example

```text
Database 1

↓

Fails

↓

Database 2 Automatically Takes Over
```

---

# Redundancy

Redundancy means keeping extra resources ready.

Examples

* Extra Server
* Extra Database
* Extra Storage
* Extra Internet Connection

Purpose:

If one fails,

another immediately replaces it.

---

# Load Balancer

A Load Balancer distributes incoming traffic across multiple servers.

Example

```text
1000 Users

↓

Load Balancer

↓

Server 1

Server 2

Server 3
```

Benefits

* Better Performance
* No Single Server Overload
* High Availability

Popular Load Balancers

* AWS ALB
* AWS NLB
* NGINX
* HAProxy

---

# Auto Scaling

Traffic changes throughout the day.

Morning

```text
100 Users

↓

2 Servers
```

Festival Sale

```text
10000 Users

↓

20 Servers
```

Midnight

```text
200 Users

↓

2 Servers
```

Auto Scaling automatically increases or decreases servers.

Benefits

* Cost Saving
* Better Performance
* High Availability

---

# Disaster Recovery (DR)

Disaster Recovery is the process of restoring systems after a major failure.

Examples

* Fire
* Flood
* Power Failure
* Data Center Failure
* Cyber Attack

Recovery includes:

* Restore Backups
* Launch New Servers
* Recover Databases
* Resume Services

---

# Backup

Backup means creating copies of important data.

Example

```text
Production Database

↓

Daily Backup

↓

Cloud Storage
```

If data is deleted,

restore from backup.

---

# Health Checks

Health Checks continuously verify whether a server is working.

Example

```text
Health Check

↓

Server Responding?

↓

YES

↓

Keep Traffic

OR

↓

NO

↓

Remove From Load Balancer
```

---

# Monitoring and Reliability

Monitoring helps maintain reliability.

Monitor

* CPU
* Memory
* Disk
* Network
* Database
* API Response Time

Alerts allow engineers to act before users notice issues.

---

# Reliability Architecture

```text
Users

↓

Load Balancer

↓

Server 1

Server 2

Server 3

↓

Database Cluster

↓

Backup Storage

↓

Monitoring

↓

Alerts
```

---

# Real World Example

### Netflix

Millions of users watch movies simultaneously.

Netflix uses

* Multiple Data Centers
* Load Balancers
* Auto Scaling
* Monitoring
* Backups
* Disaster Recovery

If one server fails,

Users continue streaming without interruption.

---

# AWS Services for Reliability

## Elastic Load Balancer (ELB)

Distributes traffic across multiple EC2 instances.

---

## Auto Scaling Group (ASG)

Automatically launches or terminates EC2 instances based on demand.

---

## Amazon RDS Multi-AZ

Maintains standby databases for automatic failover.

---

## Amazon S3

Provides highly durable storage with multiple copies of data.

---

## Route 53

DNS service that can route traffic to healthy endpoints.

---

# Hands-on Practice

## Step 1

Launch two EC2 Ubuntu instances.

---

## Step 2

Install Nginx on both.

```bash
sudo apt update

sudo apt install nginx -y
```

---

## Step 3

Create different home pages.

Server 1

```text
Welcome from Server 1
```

Server 2

```text
Welcome from Server 2
```

---

## Step 4

Create an AWS Application Load Balancer.

---

## Step 5

Add both EC2 instances.

---

## Step 6

Open the Load Balancer DNS.

Refresh the browser multiple times.

Traffic will be distributed between servers.

---

## Step 7

Stop one EC2 instance.

Refresh again.

Website remains available.

Congratulations!

You built a highly available system.

---

# Reliability Metrics

Common metrics:

| Metric       | Meaning                    |
| ------------ | -------------------------- |
| Availability | System Uptime              |
| MTTR         | Mean Time To Recovery      |
| MTBF         | Mean Time Between Failures |
| Error Rate   | Failed Requests            |
| Latency      | Response Time              |

---

# Best Practices

* Use Load Balancers.
* Enable Auto Scaling.
* Take regular backups.
* Monitor everything.
* Use multiple Availability Zones.
* Test Disaster Recovery.
* Remove single points of failure.

---

# Common Mistakes

❌ One server for production

❌ No backups

❌ No monitoring

❌ No health checks

❌ Manual recovery

---

# Interview Questions

### What is Reliability?

Reliability is the ability of a system to operate correctly without failure over time.

---

### What is High Availability?

High Availability ensures applications remain available even if one component fails.

---

### What is Fault Tolerance?

Fault Tolerance allows systems to continue functioning despite failures.

---

### Difference between Backup and Disaster Recovery?

Backup is a copy of data.

Disaster Recovery is the complete process of restoring systems after failure.

---

### What is Auto Scaling?

Auto Scaling automatically adjusts the number of servers based on traffic.

---

# Summary

✔ Reliability ensures applications remain available and stable.

✔ Load Balancers distribute traffic.

✔ Auto Scaling handles changing workloads.

✔ Disaster Recovery restores systems after failures.

✔ Backups protect data.

✔ Monitoring improves reliability.

