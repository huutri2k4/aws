---
title: "Blog 2"
date: 2026-07-09
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Automatically Trigger CI/CD for Each Project in a GitHub Monorepo with AWS CodePipeline

In the process of learning about **CI/CD on AWS**, I read a quite interesting blog post from AWS about **integrating a GitHub Monorepo with AWS CodePipeline**.

### The Problem of Monorepo in CI/CD
**Monorepo** is a way of organizing source code where **multiple applications or services reside within a single repository**.

**Example:**
repo/
├── frontend/
├── backend/
├── auth-service/
├── internship-service/
└── docs/

This approach helps **manage source code centrally**, makes it easy to share common libraries, and simplifies repository management. However, when deploying CI/CD, a problem arises: **If each service has its own AWS CodePipeline, any commit in the repository can trigger all pipelines.**

**Example:**
* Only modifying `docs/README.md`
* Only updating `frontend/`

**But:**
* Frontend Pipeline runs
* Backend Pipeline runs
* Auth Service Pipeline runs

While in reality, **only one specific pipeline needs to be activated**. This increases **build time, consumes resources, and incurs unnecessary costs**.

### The Solution Idea
After reading the AWS blog post, I realized that the problem does not lie within CodePipeline itself, but in **how events from GitHub are handled**. Instead of letting CodePipeline automatically listen to the entire repository, we can **create an intermediate layer to decide which pipeline should run**.

**General Architecture:**
Developer ➔ GitHub Monorepo ➔ Webhook ➔ API Gateway ➔ Lambda ➔ Decision Engine ➔ Corresponding CodePipeline

**Lambda will read the payload from the GitHub Webhook** to determine:
* **Which files were changed**
* **Which directories are affected**
* **Whether it is an important file or not**

Only then does it decide whether to trigger the pipeline.

### How It Works
Suppose the repository has the following structure:
repo/
├── frontend/
├── backend/
├── internship-service/
└── docs/

If a commit is made to: `frontend/src/App.jsx`
➔ **Lambda will analyze the GitHub payload** and recognize that the change is located inside the frontend directory.
* **Result:** Runs Frontend Pipeline; Does not run Backend Pipeline; Does not run Internship Service Pipeline.

Conversely, if a commit is made to: `docs/README.md`
➔ The system can **completely ignore it**. No pipeline is activated.

### What I Learned

#### 1. Event-Driven CI/CD is More Efficient Than Polling
Initially, I thought that having the pipeline just monitor the repository was enough. However, the **Event-Driven approach makes the system much smarter**.
Instead of: *"Repository changes ➔ Run everything"*
We shift to: ***"Repository changes ➔ Analyze ➔ Run exactly what needs to run"***

#### 2. Lambda Can Act as a Decision Engine
Previously, I usually viewed Lambda as a simple processing function. In this model, **Lambda becomes the central orchestrator**. It can: **Analyze commits, Check branches, Ignore non-important files, and Trigger multiple different pipelines**.

#### 3. Saving AWS Costs
This is especially useful when using: **AWS CodeBuild, AWS CodePipeline, and ECS Deployment**. Each build consumes resources. If the repository contains dozens of microservices, **building only the specific service that changed will save a significant amount of cost**.

### Conclusion
This is a **simple, cost-effective solution** but highly suitable for Monorepo systems or Microservices architectures on AWS.

![Nguyen Huu Tri](/aws/images/VA.jpg)

**Reference Source:** <https://aws.amazon.com/vi/blogs/devops/integrate-github-monorepo-with-aws-codepipeline-to-run-project-specific-ci-cd-pipelines/>