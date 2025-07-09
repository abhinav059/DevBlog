---
title: Welcome to my blog!
---
---
title: 🚀 From Code to Cloud: My DevOps & CI/CD Learning Journey
---

# 🚀 From Code to Cloud: My DevOps & CI/CD Learning Journey

> "You write code. But how does that code reach millions? Who ensures it runs reliably, securely, and consistently — every single day?"

Welcome to the world of **DevOps** and **CI/CD** — where code meets automation, speed meets quality, and software development turns into a high-speed relay race.

---

## 🧠 What is DevOps? Think of a Kitchen...

Imagine a busy restaurant kitchen 🍝.

- **Developers** are the chefs creating dishes (code).
- **Operations** are the servers delivering meals to tables (deploying software).
- If the kitchen and service team don’t communicate well, orders are delayed, messed up, or cold by the time they reach the customer.

**DevOps** is like a **super-efficient kitchen** where chefs and servers work together, share the same goal, and are backed by automation — ensuring food (software) reaches the customer hot, fast, and perfect.

> 🔁 DevOps = Development + Operations  
> 🎯 Goal: Shorter dev cycles, frequent delivery, and high software quality.

---

## 🔄 CI/CD: A Factory for Code Delivery

Think of a **car factory**. Every car (software feature) goes through:
1. Assembly (integration)
2. Testing
3. Painting (build)
4. Quality check
5. Delivery (deployment)

This is **CI/CD**:

### 🔧 Continuous Integration (CI)
- Automatically tests and integrates code on each push.

### 🚀 Continuous Delivery / Deployment (CD)
- Automatically delivers (or deploys) tested code to staging or production.

---

## 🛠️ My DevOps Toolkit

| Tool | Purpose |
|------|---------|
| **Git & GitHub** | Version control |
| **GitHub Actions** | CI/CD pipelines |
| **Docker** | Containerization |
| **Jenkins** | Build automation |
| **Terraform** | Infrastructure as code |
| **Prometheus + Grafana** | Monitoring & alerting |

---

## 🔁 My First CI Workflow with GitHub Actions

```yaml
# .github/workflows/test.yml
name: Run Python Tests

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    - name: Set up Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.9'

    - name: Install dependencies
      run: |
        pip install -r requirements.txt

    - name: Run tests
      run: |
        pytest
