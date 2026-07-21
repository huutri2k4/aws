---
title: "Weekly Work Log - Week 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
* Focus on developing the front-end user interfaces (UI) for the group project modules based on team tasks allocation.
* Study core cloud concepts including Automated OS Patching, user authentication with AWS Cognito, and review foundational services (VPC, EC2, S3, EFS, Lambda).

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Patching Theory:** Explored automated OS Patching using EC2 Image Builder to securely generate clean base AMIs. | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Studied AWS CloudFormation rolling updates to safely replace older instances in an Auto Scaling Group with newly patched AMIs. | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Cognito Theory:** Researched AWS Cognito User Pools to understand Single Sign-On (SSO) integration across multiple applications. | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Cloud Review:** Refreshed knowledge on Custom VPC setups, including Route Tables, Internet Gateways, and public/private subnet architectures for deployment. | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Reviewed and compared core features and performance differences between block storage (EBS), shared network files (EFS), and object storage (S3). | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Group Project Development:** The 4-member team focused on implementing the front-end screen layouts; logic workflows and AWS configurations are currently in progress. | 04/07/2026 | 04/07/2026 | Project Repository |

### Weekly Group Project Status & Tasks Breakdown:
* **Member 1 (Auth & Profiles):** Completed UI layouts for Login, Forgot Password, User Profile, and Change Password pages. (Backend login logic, permissions mapping, and S3 CV uploads are still pending).
* **Member 2 (Internship Management):** Completed UI for the Admin Dashboard, Major lists, Position lists, Mentor lists, and Assignment screens. (Data linkage and workflow logic are in progress).
* **Member 3 (Tasks & Reports):** Finished front-end layouts for Tasks, Submit Report, Report History, Evaluations, and Goals pages. (S3 PDF upload handlers and PDF export functions are still in development).
* **Member 4 (Dashboards & AWS):** Completed UI dashboards for both corporate and student roles, alongside the Schedule and Notification views. (Real-time connection alerts, QR check-ins, and core AWS resource provisioning are pending).

### Week 11 Outcomes:
* The team successfully delivered all necessary front-end screen interfaces (UI) for the "Internship Management System".
* Gained a conceptual understanding of automated patch management workflows and central authentication using AWS Cognito.
* Reviewed and consolidated knowledge regarding custom VPC network path rules, EC2 compute configurations, and storage types to prepare for final deployment.