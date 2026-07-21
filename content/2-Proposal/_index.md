---
title: "Proposal"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

In this section, the team summarizes the bootcamp/internship activities that were **planned** and **executed** for the project.

# Internship Management System (IMS)
## Internship Management Solution Integrated with AWS Services (S3, RDS, IAM)

### 1. Executive Summary
The **Internship Management System (IMS)** was developed by a team of 4 members to streamline, track progress, submit reports, and evaluate interns for enterprises and academic institutions. The system utilizes core **AWS Cloud services (Singapore Region `ap-southeast-1`)**, including **Amazon S3** for media/document storage, **Amazon RDS (MySQL)** for centralized database management, and **AWS IAM** for identity and access control.

### 2. Problem Statement
*Current Challenges*
* Traditional internship management relies heavily on manual processes using Excel files, leading to lost weekly reports, fragmented task assignments, and inefficient performance evaluations.
* Storing PDF reports, CV documents, and profile avatars on local server drives poses security risks, lacks distributed storage, and quickly consumes local disk capacity.
* Self-hosted databases on local machines lack robust security controls, flexible backup options, and high-performance querying capabilities.

*Proposed Solution*
* Build a modern web application adhering to RESTful API Service architecture.
* Integrate **Amazon S3** to manage cloud storage for all student profile avatars, CV documents, and submitted weekly PDF reports.
* Deploy an **Amazon RDS MySQL** relational database to securely and efficiently store user data, internship terms, task assignments, and evaluations.
* Utilize **AWS IAM** to define granular permission policies (IAM Roles/Policies), ensuring the backend application interacts with S3 and RDS under the principle of least privilege.

*Benefits and Return on Investment (ROI)*
* Digitizes 100% of task assignments, report submissions, and evaluations, reducing manual administrative workloads for Mentors and Admins by 80%.
* Offloads local storage requirements entirely by shifting all static assets to secure, low-cost Amazon S3 storage.
* Ensures data integrity and seamless management via a fully managed Amazon RDS database instance.

### 3. Solution Architecture
The system employs a web application model directly connected to storage and database services on AWS Cloud:

![Nguyen Huu Tri](images/sodoaws.jpg)

*AWS Services Utilized*
- *Amazon S3*: Object storage dedicated to storing profile avatars, CV files, and weekly PDF reports.
- *Amazon RDS (MySQL)*: Relational database storing user accounts, internship batches, tasks, and evaluation results.
- *AWS IAM*: Identity and access management securing backend interactions with S3 buckets and RDS instances.

*Component Design*
- *Frontend & Service Tier*: Users interact with the Web Frontend, which sends asynchronous requests to the Backend (RESTful API Service).
- *File Storage Tier*: When uploading avatars or submitting PDF reports, the application uses the AWS SDK to push files directly to an **Amazon S3 Bucket**.
- *Database Tier*: All queries regarding user accounts, internship assignments, and grading are executed against the **Amazon RDS MySQL Database**.
- *Security & Access Tier*: **AWS IAM** provides IAM Roles and Policies to restrict actions (`s3:PutObject`, `s3:GetObject`), securing cloud assets.

### 4. Technical Implementation
*Implementation Stages*
Executed by a 4-member team over 12 weeks across 4 key phases:
1. *Research & Architecture Design*: Analyzed business requirements, finalized core modules (Auth, Management, Reports, Dashboard), created Figma wireframes/UIs, and drafted system architecture (Weeks 1–4).
2. *Frontend & Service Layer Development*: Standardized team Git Flow practices on GitLab, split frontend components, and built RESTful API Service Patterns (Weeks 5–8).
3. *AWS Infrastructure & Integration*: Provisioned Amazon RDS MySQL, created S3 Buckets, defined IAM Policies/Roles, and integrated image/PDF upload APIs targeting S3 (Weeks 9–11).
4. *Testing & Final Review*: Tested S3 file upload workflows, verified RDS queries, reviewed IAM permissions, and compiled final reports (Week 12).

*Technical Requirements*
- *Collaborative Environment*: Managed codebase via GitLab adopting Git Flow branching strategies.
- *Frontend & Backend*: Built modular component-driven frontends connected to asynchronous RESTful API backend service layers.
- *AWS Integration*: Mastered AWS SDK integration within the backend to handle Amazon S3 file uploads, Amazon RDS MySQL Endpoint connections, and IAM JSON policy configurations.

### 5. Milestones & Timeline
- *Phase 1 (Weeks 1–4)*: Learned AWS fundamentals (EC2, S3, IAM) and submitted Phase 1 Progress Report.
- *Phase 2 (Weeks 5–8)*: Hands-on practice with IAM Roles, S3 Versioning, provisioning, and connecting Amazon RDS MySQL.
- *Phase 3 (Weeks 9–11)*: Kicked off the "Internship Management System" group project, designed Figma mockups, allocated tasks among 4 members, provisioned RDS Database, and submitted architecture diagrams for Admin review.
- *Phase 4 (Week 12)*: Finalized image/PDF upload features to Amazon S3, integrated data with Amazon RDS MySQL, conducted system testing, and submitted final reports.

### 6. Budget Estimation
*Estimated Monthly Infrastructure Cost (For Testing / Academic Scale)*
- *Amazon RDS MySQL (db.t3.micro)*: ~$15.00/month (Covered under AWS Free Tier).
- *Amazon S3 (Media & PDF Storage - ~5-10 GB)*: ~$0.15 – $0.25/month.
- *AWS IAM*: Completely Free.

*Total Infrastructure Cost*: ~$15.25/month (Can be reduced to **$0.00/month** by utilizing AWS 12-Month Free Tier allocations).

### 7. Risk Assessment
*Risk Matrix*
- Database Connection Timeout (RDS): High impact, low probability.
- S3 Upload Failure due to incorrect IAM Policy: Medium impact, medium probability.
- Exposure of Database Credentials / Secret Keys: Very high impact, low probability.

*Mitigation Strategies*
- RDS Timeout: Configure RDS Security Groups properly to allow inbound traffic on port 3306 from the backend application server.
- S3 / IAM Errors: Precisely define allowed actions (`s3:PutObject`, `s3:GetObject`) in IAM Policies and assign IAM Roles directly instead of hardcoding access keys.
- Credential Security: Use environment variables (`.env`) to safely isolate RDS connection strings and S3 configurations.

### 8. Expected Outcomes
*Technical Enhancements*: Successfully built an internship management web application seamlessly integrated with core AWS Cloud services (S3, RDS, IAM).
*Practical Value*: Enabled team members to master practical AWS cloud services, improved 4-member group project management workflows (Git Flow, Figma, RESTful APIs), and delivered a complete project ready for academic evaluation.