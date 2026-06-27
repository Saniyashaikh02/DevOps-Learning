# 🔍 Troubleshooting in DevOps

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

Imagine it's **2:00 AM**.

You receive a call.

> 🚨 **"Production website is down!"**

Millions of users cannot access the application.

The company is losing money every minute.

As a DevOps Engineer, your job is **not just to deploy applications**.

Your biggest responsibility is to **find the problem quickly, fix it, and prevent it from happening again.**

This process is called **Troubleshooting**.

---

# What is Troubleshooting?

Troubleshooting is the systematic process of identifying, analyzing, and resolving problems in applications, servers, networks, or infrastructure.

---

# Simple Definition

**Troubleshooting is the process of finding the root cause of a problem and fixing it as quickly as possible.**

---

# Why is Troubleshooting Important?

Imagine a website goes down.

Without troubleshooting:

```text
Website Down

↓

Nobody Knows Why

↓

Customers Leave

↓

Company Loses Money
```

With troubleshooting:

```text
Website Down

↓

Identify Problem

↓

Fix Problem

↓

Website Online
```

---

# Troubleshooting Process

Every DevOps Engineer should follow the same approach.

```text
Problem Reported

↓

Collect Information

↓

Identify Root Cause

↓

Fix Problem

↓

Verify Solution

↓

Document the Issue

↓

Prevent Future Problems
```

---

# Step 1 - Understand the Problem

Never start fixing immediately.

Ask questions.

Examples:

* Is the application down?
* Is only one page failing?
* Is everyone affected?
* When did it start?
* What changed recently?

---

# Step 2 - Check Server Status

Linux

```bash
uptime
```

Shows:

* Server Running Time
* Load Average

---

Check CPU

```bash
top
```

or

```bash
htop
```

Shows:

* Running Processes
* CPU Usage
* Memory Usage

---

# Step 3 - Check Memory

```bash
free -m
```

Example

```text
Total Memory

Used Memory

Free Memory
```

If memory is 100% used,

applications may crash.

---

# Step 4 - Check Disk Space

```bash
df -h
```

Example

```text
Filesystem

Used

Available

Use%
```

If disk becomes

```text
100%
```

Applications may stop working.

---

# Step 5 - Check Running Processes

```bash
ps -ef
```

Find specific process

```bash
ps -ef | grep nginx
```

Example

```text
nginx

running
```

---

# Step 6 - Check Services

Systemd

```bash
systemctl status nginx
```

Possible output

```text
Active (running)
```

or

```text
Failed
```

Restart service

```bash
sudo systemctl restart nginx
```

---

# Step 7 - Check Logs

Logs are the most valuable source of information.

System logs

```bash
journalctl
```

Specific service

```bash
journalctl -u nginx
```

Application logs

```text
/var/log/
```

Examples

```text
nginx.log

application.log

error.log
```

---

# Step 8 - Check Network

Ping server

```bash
ping google.com
```

Check connectivity

```bash
ping server-ip
```

---

Check listening ports

```bash
netstat -tulpn
```

or

```bash
ss -tulpn
```

Example

```text
Port 80

Listening
```

---

# Step 9 - Check Files

Example

```bash
ls

pwd

cat

less
```

Verify configuration files exist.

---

# Step 10 - Restart Application

Sometimes restarting fixes temporary problems.

```bash
sudo systemctl restart nginx
```

or

```bash
pm2 restart app
```

---

# Common Production Problems

## High CPU

Symptoms

* Website Slow
* API Slow

Check

```bash
top
```

---

## High Memory

Symptoms

* Server Crash
* OOM Killer

Check

```bash
free -m
```

---

## Disk Full

Symptoms

* Cannot write logs
* Application fails

Check

```bash
df -h
```

---

## Service Down

Symptoms

Website not opening

Check

```bash
systemctl status nginx
```

---

## Port Already Used

Check

```bash
netstat -tulpn
```

Find process

Kill process

```bash
kill -9 PID
```

---

# Real Troubleshooting Example

Problem

Website

```text
502 Bad Gateway
```

Checklist

```text
Check Nginx

↓

Check Application

↓

Check Logs

↓

Restart Application

↓

Verify
```

---

# Practical Example

Suppose Nginx stopped.

Check

```bash
systemctl status nginx
```

Restart

```bash
sudo systemctl restart nginx
```

Check

```bash
systemctl status nginx
```

Now website works.

---

# Linux Commands Every DevOps Engineer Must Know

| Command    | Purpose                |
| ---------- | ---------------------- |
| pwd        | Current Directory      |
| ls         | List Files             |
| cd         | Change Directory       |
| top        | CPU Usage              |
| htop       | Interactive Monitoring |
| free -m    | Memory                 |
| df -h      | Disk                   |
| ps -ef     | Running Processes      |
| journalctl | Logs                   |
| systemctl  | Services               |
| ping       | Network                |
| netstat    | Ports                  |
| ss         | Network Connections    |
| curl       | Test APIs              |
| wget       | Download Files         |

---

# Troubleshooting Workflow

```text
Problem

↓

Check Logs

↓

Check CPU

↓

Check Memory

↓

Check Disk

↓

Check Service

↓

Check Network

↓

Restart Service

↓

Verify
```

---

# Best Practices

* Never panic.
* Read logs carefully.
* Change only one thing at a time.
* Take backups before major changes.
* Document every issue.
* Monitor after fixing.

---

# Common Mistakes

❌ Restarting everything immediately

❌ Ignoring logs

❌ Deleting log files

❌ Not checking disk space

❌ Guessing instead of investigating

---

# Real World Example

Netflix detects an issue.

Monitoring sends an alert.

Engineers:

```text
Alert

↓

Logs

↓

Root Cause

↓

Fix

↓

Deploy

↓

Monitor Again
```

Entire process is automated.

---

# Interview Questions

### What is Troubleshooting?

Troubleshooting is the process of identifying, analyzing, and resolving technical problems.

---

### Which command checks disk usage?

```bash
df -h
```

---

### Which command checks memory?

```bash
free -m
```

---

### Which command checks running services?

```bash
systemctl status service-name
```

Example

```bash
systemctl status nginx
```

---

### Which command checks logs?

```bash
journalctl
```

---

### Which command checks CPU?

```bash
top
```

or

```bash
htop
```

---

# Mini Troubleshooting Checklist

Whenever a production issue occurs, ask yourself:

✅ Is the server reachable?

✅ Is the service running?

✅ Is CPU usage high?

✅ Is memory full?

✅ Is disk space available?

✅ Are logs showing errors?

✅ Is the network working?

✅ Is the application listening on the correct port?

---

# Summary

✔ Troubleshooting is one of the most important DevOps skills.

✔ Always follow a structured approach.

✔ Logs are your best friend.

✔ Monitor before users complain.

✔ Learn Linux commands—they are essential for troubleshooting.

✔ Practice debugging regularly to improve confidence.

