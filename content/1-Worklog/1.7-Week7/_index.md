---
title: "Weekly Work Log - Week 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
* Learn and practice deploying relational databases with Amazon RDS (MySQL).
* Understand how to set up isolated networking for databases and monitor instance health using Amazon CloudWatch.

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Explored linking the Cloud9 IDE environment directly with a backend EC2 instance for computing power. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **RDS Theory:** Studied the basics of Amazon RDS, including core features like Multi-AZ deployment, Read Replicas, and DB Snapshots. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Database Networking:** Configured a DB Subnet Group named `subnet-group-tuan7` and set up Security Group rules for port 3306. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Deployment & Connection:** Launched an Amazon RDS MySQL database instance.<br>- Installed MySQL Client on an EC2 instance and connected to the RDS using the DB Endpoint. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Data Operations & Monitoring:** Executed basic SQL commands to create tables and insert data, then checked system metrics via the **Amazon CloudWatch Metrics** console. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Maintenance & Cleanup:** Practiced creating a manual DB Snapshot for backups, explored AWS DMS concepts, and deleted the test RDS/EC2 resources to save costs. | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 7 Outcomes:
* Successfully created a functional **DB Subnet Group (`subnet-group-tuan7`)** to ensure secure and isolated networking for database hosting.
* Gained hands-on experience in provisioning an Amazon RDS MySQL instance and establishing a secure connection from a web server via DB Endpoints.
* Capable of using **Amazon CloudWatch Metrics** to monitor performance indicators and check instance status logs (`StatusCheckFailed_AttachedEBS`) for the project server (`Web-Server-Nhom4`).
* Learned how to manage database backups through DB Snapshots and clean up environment resources efficiently.

![Nguyen Huu Tri](/aws/images/tuan7,1.png)

![Nguyen Huu Tri](/aws/images/tuan7,2.png)