---
title: "Introduction"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Introduction to S3, RDS, and IAM in the Project

In the **Internship Management System** web application, organizing data storage and maintaining strict security controls are top priorities:

* **Amazon S3 (Simple Storage Service):** Acts as a scalable Object Storage repository, holding static assets such as student avatars, PDF CV documents, and weekly internship report files.
* **Amazon RDS MySQL (Relational Database Service):** Serves as the primary relational database management system, handling structured data including user accounts, internship terms, academic majors, task assignments, and evaluation records.
* **AWS IAM (Identity and Access Management):** Functions as the central security mechanism, defining precisely which backend services or users are granted permission to perform actions (`s3:PutObject`, `s3:GetObject`, RDS queries) following least privilege principles.

#### Workshop Workflow Overview

This workshop focuses on provisioning infrastructure and establishing secure connectivity across these three core services:

1. **Amazon S3 Bucket Setup:** Creating the storage bucket, enabling static media upload capabilities, and verifying object path URLs.
2. **Amazon RDS MySQL Provisioning:** Deploying a managed MySQL DB instance, placing it inside a secure DB Subnet Group, and configuring inbound rules for port 3306 on the Security Group.
3. **IAM Access Control Configuration:** Drafting JSON IAM Policy statements and creating IAM Roles to grant temporary, secure service-level permissions to S3 and RDS.

> **Note:** All configurations in this workshop strictly follow AWS security best practices, eliminating the need to embed static Access Keys inside application source code.

![Nguyen Huu Tri](/images/s3.png)