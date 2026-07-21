---
title: "Weekly Work Log - Week 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:
* Learn the basics of EC2 Auto Scaling Groups (ASG) and load distribution with Elastic Load Balancing (ELB).
* Practice creating launch blueprints and target groups to set up a multi-server high-availability architecture.

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Auto Scaling Theory:** Explored Amazon EC2 Auto Scaling Group concepts, including manual, dynamic, scheduled, and predictive scaling policies. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Load Balancing Theory:** Studied Elastic Load Balancing types and differentiated between ALB (Application), NLB (Network), and GWLB (Gateway). | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Creating Launch Template:** Configured and created a Launch Template named `template-tuan8-tri` to save instance configuration specs for automated deployment. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Creating Target Group:** Provisioned a Target Group named `tg-tuan8-nhom4` working on HTTP port 80 to manage target backend instances. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **ALB Deployment:** Set up an Application Load Balancer linked with the Target Group and verified traffic distribution using the balancer's DNS endpoint. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **ASG Configurations:** Set up Min/Max/Desired capacity values for the ASG and explored using Amazon SNS for email notifications during scaling activities. | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 8 Outcomes:
* Successfully generated a **Launch Template (`template-tuan8-tri`)** to automate standard instance configurations for scaling purposes.
* Created a functional **Target Group (`tg-tuan8-nhom4`)** on HTTP port 80 within the custom VPC environment, ready for health monitoring.
* Gained a clear understanding of combining ALBs for traffic distribution and Auto Scaling Groups for handling traffic spikes.
* Capable of configuring operational limits (Min/Max/Desired) and integrating Amazon SNS for automatic status alerts.

![Nguyen Huu Tri](/images/tuan8,1.png)

![Nguyen Huu Tri](/images/tuan8,2.png)