# 🚀 CI/CD (Continuous Integration & Continuous Delivery/Deployment)

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

Imagine a company has **100 developers** working on the same application.

Every day, each developer writes code and pushes it to GitHub.

Without an automated process:

* Developers manually merge code.
* Someone manually tests the application.
* Someone manually builds it.
* Someone manually deploys it.
* Bugs are discovered very late.

This is slow and error-prone.

CI/CD solves this problem.

---

# What is CI/CD?

CI/CD is a DevOps practice that automates the process of integrating, testing, building, and deploying software.

Instead of doing everything manually, the pipeline performs it automatically.

---

# What is Continuous Integration (CI)?

Continuous Integration means developers frequently merge their code into a shared repository.

Every time code is pushed:

* Code is downloaded.
* Dependencies are installed.
* Tests run automatically.
* Build starts automatically.
* If everything passes, the code is ready for deployment.

---

## CI Workflow

```text
Developer

↓

Git Push

↓

GitHub Repository

↓

CI Pipeline

↓

Build

↓

Test

↓

Ready for Deployment
```

---

# Why Do We Need CI?

Imagine three developers.

Developer A changes Login.

Developer B changes Payment.

Developer C changes Dashboard.

Without CI:

```text
Developer A

Developer B

Developer C

↓

Manual Merge

↓

Conflicts

↓

Application Breaks
```

With CI:

```text
Git Push

↓

Automatic Build

↓

Automatic Test

↓

Errors Found Immediately
```

---

# Benefits of CI

* Detect bugs early
* Faster development
* Better collaboration
* Better code quality
* Faster feedback

---

# What is Continuous Delivery (CD)?

Continuous Delivery means the application is automatically prepared for deployment.

After CI completes successfully:

```text
Code

↓

Build

↓

Tests

↓

Deploy to Staging

↓

Ready for Production
```

A human decides when to release it.

---

# What is Continuous Deployment?

Continuous Deployment goes one step further.

If all tests pass:

```text
Code

↓

Build

↓

Test

↓

Deploy Production

↓

Users
```

No manual approval.

Everything happens automatically.

---

# Continuous Delivery vs Continuous Deployment

| Continuous Delivery      | Continuous Deployment       |
| ------------------------ | --------------------------- |
| Manual Approval          | Automatic Release           |
| Safer                    | Faster                      |
| Human decides deployment | Pipeline decides deployment |

---

# CI/CD Pipeline

A pipeline is a sequence of automated steps.

```text
Developer

↓

Git Push

↓

Source Code

↓

Build

↓

Run Tests

↓

Create Artifact

↓

Deploy Staging

↓

Deploy Production

↓

Monitoring
```

---

# Pipeline Stages

## 1. Source

Developer writes code.

Pushes it to GitHub.

---

## 2. Build

Compile application.

Download dependencies.

Package application.

---

## 3. Test

Run:

* Unit Tests
* Integration Tests
* Security Tests

If tests fail,

pipeline stops.

---

## 4. Package

Create:

* Docker Image
* JAR
* WAR
* ZIP

This output is called an **Artifact**.

---

## 5. Deploy

Deploy application to:

* Development
* Staging
* Production

---

## 6. Monitor

Collect:

* Logs
* CPU
* RAM
* Errors

---

# CI/CD Tools

Popular tools:

| Tool           | Purpose |
| -------------- | ------- |
| GitHub Actions | CI/CD   |
| Jenkins        | CI/CD   |
| GitLab CI      | CI/CD   |
| CircleCI       | CI/CD   |
| Azure DevOps   | CI/CD   |

---

# GitHub Actions

GitHub Actions automatically runs workflows when events occur.

Example:

```text
Git Push

↓

GitHub Actions

↓

Build

↓

Test

↓

Deploy
```

---

# GitHub Actions Workflow

Location:

```text
.github/workflows/main.yml
```

Example:

```yaml
name: Build Project

on:
  push:

jobs:
  build:

    runs-on: ubuntu-latest

    steps:

    - uses: actions/checkout@v4

    - name: Install Dependencies
      run: npm install

    - name: Run Tests
      run: npm test

    - name: Build
      run: npm run build
```

Every push starts this workflow automatically.

---

# Jenkins

Jenkins is an automation server.

Functions:

* Build
* Test
* Deploy
* Notifications

Pipeline:

```text
GitHub

↓

Jenkins

↓

Build

↓

Test

↓

Deploy
```

---

# Practical Example

Imagine you have a Node.js application.

Developer updates code.

Runs:

```bash
git add .

git commit -m "Update Login"

git push origin main
```

Immediately:

GitHub Actions:

* Downloads code
* Installs packages
* Runs tests
* Builds project
* Creates artifact

Everything happens automatically.

---

# Hands-on Practice

## Step 1

Create GitHub Repository.

---

## Step 2

Create Node.js Project.

```bash
npm init -y
```

---

## Step 3

Push to GitHub.

---

## Step 4

Create folder

```text
.github/workflows
```

---

## Step 5

Create

```text
main.yml
```

Paste:

```yaml
name: Node CI

on:
  push:

jobs:

  build:

    runs-on: ubuntu-latest

    steps:

    - uses: actions/checkout@v4

    - run: npm install

    - run: npm test
```

Commit:

```bash
git add .

git commit -m "Add CI pipeline"

git push
```

Go to:

GitHub → Actions

You'll see the pipeline running automatically.

---

# Real World Example

Netflix developers push code hundreds of times every day.

Pipeline:

```text
Developer

↓

GitHub

↓

Build

↓

Test

↓

Docker Image

↓

Deploy Kubernetes

↓

Monitoring

↓

Users
```

No manual deployment.

---

# Benefits of CI/CD

* Faster Releases
* Automatic Testing
* Less Manual Work
* Better Quality
* Faster Recovery
* Better Collaboration

---

# Best Practices

* Keep builds fast
* Test every commit
* Never skip automated tests
* Store pipelines in Git
* Automate deployments
* Monitor after deployment

---

# Common Mistakes

❌ Manual deployment

❌ No testing

❌ Huge deployments

❌ No rollback strategy

❌ Ignoring failed pipelines

---

# Interview Questions

### What is CI?

Continuous Integration automatically builds and tests code whenever developers push changes.

---

### What is CD?

Continuous Delivery or Continuous Deployment automates software deployment.

---

### Difference between Continuous Delivery and Continuous Deployment?

Continuous Delivery requires manual approval.

Continuous Deployment automatically deploys after successful tests.

---

### Name some CI/CD tools.

* GitHub Actions
* Jenkins
* GitLab CI
* CircleCI
* Azure DevOps

---

### What is a Pipeline?

A pipeline is an automated sequence of steps used to build, test, and deploy software.

---

# Summary

✔ CI integrates code frequently.

✔ CD automates software delivery.

✔ Pipelines reduce manual work.

✔ GitHub Actions and Jenkins are popular CI/CD tools.

✔ Every modern DevOps project uses CI/CD.

