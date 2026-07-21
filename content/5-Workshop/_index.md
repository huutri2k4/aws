---
title: "Workshop"
date: 2026-04-17
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Deploying S3 Storage, RDS Database, and IAM Access Management

#### Overview

In this hands-on workshop, I configured and integrated the core storage, database, and security services on AWS Cloud for the **Internship Management System**:

* **Amazon S3:** Provisioned S3 Buckets, configured access permissions, and handled media storage (profile avatars, student CVs, and weekly PDF report files).
* **Amazon RDS (MySQL):** Launched an AWS-managed relational database instance, configured DB Subnet Groups, and set up Security Group rules to allow secure database access on port 3306.
* **AWS IAM:** Authored custom JSON IAM Policies and created IAM Roles to enforce the Principle of Least Privilege, allowing backend applications to interact securely with S3 and RDS without hardcoding static Access Keys.

#### Lab Contents

1. [Introduction](5.1-Workshop-overview/)
2. [Prerequisites](5.2-Prerequiste/)
3. [Provisioning and Configuring Amazon S3 Bucket](5.3-S3-setup/)
4. [Provisioning and Connecting Amazon RDS MySQL](5.4-RDS-setup/)
5. [Configuring AWS IAM Policies & Roles](5.5-Policy/)
6. [Clean Up Resources](5.6-Cleanup/)