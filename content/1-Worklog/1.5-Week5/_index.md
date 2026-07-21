---
title: "Weekly Work Log - Week 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
* Learn the basics of AWS IAM permissions and practice writing custom JSON policies for application access control.
* Understand VPC network flow fundamentals, focusing on the differences between Public and Private Subnets.

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **IAM Theory:** Explored core IAM concepts: Users, Groups, Roles, and Policies. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **VPC Theory:** Learned about Route Tables, Internet Gateways (IGW), and NAT Gateways for managing subnet internet access. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **IAM Users:** Practiced creating a new IAM User and managing permissions centrally by adding them to an IAM Group. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Writing Policies:** Used the JSON Policy Editor to write basic access rules for viewing and reading S3 bucket data. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **IAM Roles:** Successfully created an IAM Role named `EC2-S3-ReadOnly-Role` for EC2 to securely access S3 without storing permanent Access Keys. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Resource Cleanup:** Reviewed and removed unused lab resources (test instances, users, and roles) to prevent unnecessary charges. | 23/05/2026 | 23/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 5 Outcomes:
* Capable of writing a functional JSON policy statement in the Policy Editor to restrict actions (`ListAllMyBuckets`, `GetBucketLocation`, `GetObject`).
* Successfully created `EC2-S3-ReadOnly-Role` to attach directly to EC2 instances for safer cross-service integration.
* Understand when to use Public Subnets for web apps and Private Subnets for backend/databases, along with basic Route Table configurations.
* Cleaned up all temporary lab resources to maintain a cost-efficient and secure cloud environment.

![Nguyen Huu Tri](images/tuan5,1.png)

![Nguyen Huu Tri](images/tuan5,2.png)