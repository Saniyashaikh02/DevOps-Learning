# 🏗️ Build in DevOps

> **Level:** Beginner → Intermediate
> **Phase:** 1 - DevOps Fundamentals

---

# 📖 Introduction

One of the first stages in the DevOps lifecycle is **Build**.

Many beginners think writing code is enough. In reality, writing code is only the beginning.

Before users can use your application, your source code must be converted into a runnable application. This process is called **Build**.

---

# What is Build?

A **Build** is the process of converting source code into a runnable application or executable package.

Simply put,

```
Source Code
     │
     ▼
Build Process
     │
     ▼
Executable Application
```

---

# Real-Life Example

Imagine you want to build a house.

You don't just buy bricks and start living there.

You need:

* Cement
* Bricks
* Workers
* Electricity
* Plumbing
* Painting

Only after combining everything can you live in the house.

Software is similar.

Your project contains:

* Source code
* Images
* CSS
* JavaScript
* Libraries
* Configuration files

A build tool combines everything into one application.

---

# Why Do We Need Build?

Suppose you have:

```
My Project

│── 100 Java Files
│── 200 CSS Files
│── 500 Images
│── 40 JavaScript Files
│── Libraries
│── Configuration Files
```

Imagine copying and arranging all of these manually every time.

Impossible!

A build tool performs this automatically.

---

# Build Process

```
Developer Writes Code

        │

        ▼

Compile Source Code

        │

        ▼

Resolve Dependencies

        │

        ▼

Run Tests

        │

        ▼

Package Application

        │

        ▼

Ready for Deployment
```

---

# What Happens During Build?

A build tool usually performs these tasks:

## 1. Compile

Converts source code into machine-readable format.

Example

Java

```
Hello.java

↓

Compiler

↓

Hello.class
```

---

## 2. Resolve Dependencies

Modern applications depend on external libraries.

Example:

Node.js

```bash
npm install
```

Java

```
Maven downloads required libraries
```

Instead of downloading every library manually, build tools do it automatically.

---

## 3. Run Tests

Before deployment,

tests verify that your code works.

```
Build

↓

Run Tests

↓

Pass ✔

↓

Continue
```

If tests fail,

the build stops.

---

## 4. Package

After successful compilation,

the application is packaged.

Examples:

Java

```
.jar
```

Python

```
.whl
```

Node.js

```
Production Folder
```

Docker

```
Docker Image
```

---

# Build vs Compile

Many beginners confuse these terms.

## Compile

Converts source code into machine code.

Example

```
Hello.java

↓

Compiler

↓

Hello.class
```

---

## Build

Build is much larger.

It includes

* Compile
* Download dependencies
* Testing
* Packaging
* Optimization

Compilation is only one part of Build.

---

# Build Tools

Different programming languages use different build tools.

| Language   | Build Tool |
| ---------- | ---------- |
| Java       | Maven      |
| Java       | Gradle     |
| Node.js    | npm        |
| JavaScript | Webpack    |
| JavaScript | Vite       |
| .NET       | MSBuild    |
| C/C++      | Make       |

---

# Popular Build Tools

## Maven

Used mainly for Java applications.

Functions:

* Download libraries
* Compile code
* Run tests
* Create JAR files

---

## Gradle

Modern Java build tool.

Advantages:

* Faster than Maven
* Flexible
* Supports multiple languages

---

## npm

Node Package Manager.

Functions:

* Install packages
* Run scripts
* Build JavaScript applications

Example

```bash
npm install

npm run build
```

---

## Webpack

Bundles JavaScript applications.

```
100 JS Files

↓

Webpack

↓

Single Optimized Bundle
```

---

## Vite

Modern frontend build tool.

Advantages:

* Fast
* Lightweight
* Hot Reload

---

# Build Artifacts

After build,

an output file is created.

This output is called an **Artifact**.

Examples:

```
hello.jar

app.war

build/

dist/

Docker Image
```

Artifacts are deployed to production.

---

# Practical Example

## Step 1

Create a project

```bash
mkdir hello-app

cd hello-app
```

---

## Step 2

Initialize Node Project

```bash
npm init -y
```

This creates

```
package.json
```

---

## Step 3

Install Express

```bash
npm install express
```

---

## Step 4

Create index.js

```javascript
const express = require("express")

const app = express()

app.get("/", (req,res)=>{

res.send("Hello DevOps")

})

app.listen(3000)
```

---

## Step 5

Run

```bash
node index.js
```

Browser

```
http://localhost:3000
```

Output

```
Hello DevOps
```

Congratulations!

You built your first application.

---

# Build Lifecycle

```
Write Code

↓

Install Dependencies

↓

Compile

↓

Run Tests

↓

Package

↓

Artifact

↓

Deploy
```

---

# Common Build Errors

## Missing Dependency

```
Module Not Found
```

Solution

```bash
npm install
```

---

## Compilation Error

```
Syntax Error
```

Solution

Fix coding mistakes.

---

## Failed Tests

```
Tests Failed
```

Solution

Correct the application before deployment.

---

## Incorrect Configuration

```
package.json Missing
```

Solution

Create or fix configuration files.

---

# Best Practices

* Keep builds automated.
* Never build manually in production.
* Run tests before deployment.
* Keep dependencies updated.
* Version your artifacts.
* Use CI/CD pipelines for builds.

---

# Real-World Example

When you push code to GitHub,

GitHub Actions automatically performs:

```
Git Push

↓

Checkout Code

↓

Install Dependencies

↓

Compile

↓

Run Tests

↓

Build Artifact

↓

Deploy
```

No human intervention is required.

---

# Hands-on Practice

## Task 1

Create a Node.js application.

## Task 2

Install Express.

## Task 3

Run the application.

## Task 4

Stop the server.

## Task 5

Modify the message.

Example:

```
Hello DevOps

↓

Welcome to Build Phase
```

Run again and verify the change.

---

# Interview Questions

## What is Build?

Build is the process of converting source code into a deployable application.

---

## What is Compilation?

Compilation converts source code into machine-readable code.

---

## Name some Build Tools.

* Maven
* Gradle
* npm
* Webpack
* Vite
* MSBuild

---

## What is an Artifact?

An artifact is the final output generated after a successful build.

Examples:

* JAR
* WAR
* Docker Image
* dist Folder

---

# Summary

✔ Build converts source code into a deployable application.

✔ Build includes:

* Compilation
* Dependency Management
* Testing
* Packaging

✔ Build tools automate repetitive tasks.

✔ Every CI/CD pipeline starts with a successful build.

---

# What's Next?

In the next chapter (`03-Automation.md`), you'll learn:

* What is Automation?
* Why Automation is Important
* Bash Scripting
* PowerShell Basics
* Python Automation
* CI/CD Automation
* Real-World Examples
* Hands-on Automation Project
* Interview Questions
