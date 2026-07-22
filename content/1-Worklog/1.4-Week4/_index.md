---
title: "Weekly WorkLog - Week 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
* Practice configuring advanced EC2 features (allocating Elastic IPs, creating external EBS volumes) and complete the first 4-week progress report.
* Learn the basics of Amazon VPC (Virtual Private Cloud) and how the two firewall layers, Security Groups and NACLs, work.

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Launched additional secondary EC2 instances for testing.<br>- Allocated and associated an Elastic IP to an EC2 instance to keep its IP static after restarts. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Created an independent Amazon EBS volume (gp3 type, 2 GiB size).<br>- Attached this volume to an EC2 instance and ran Linux commands to partition and mount it. | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Managed instances lifecycle and used basic AWS CLI commands to verify created resources.<br>- Summarized everything learned from Week 1 to Week 4 to complete the phase 1 progress report. | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Network Theory:** Read documentation about Amazon VPC (isolated virtual network).<br>- Learned about IP allocation (CIDR blocks from /16 to /28) to design a network that avoids overlap with home/office IPs. | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Security Theory:** Learned about Security Groups - a firewall layer acting directly at the instance level (Stateful - automatically tracks inbound/outbound return traffic). | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Explored Network ACLs (NACLs) - a second firewall layer protecting the entire Subnet (Stateless - requires manual rules for both inbound and outbound traffic). | 16/05/2026 | 16/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 4 Outcomes:
* Successfully allocated and associated an Elastic IP to an EC2 instance, securing a static public IP that won't change on reboot.
* Learned how to create an external EBS volume (gp3, 2 GiB), attach it to a Linux server, and use terminal commands to partition and mount it.
* Gathered screenshots and logs to complete and submit the first 4-week progress report.
* Got a solid grasp of Amazon VPC and understood how Security Groups (instance firewall) and NACLs (subnet firewall) work together.

![Nguyen Huu Tri](/images/tuan4,1.png)

![Nguyen Huu Tri](/images/tuan4,2.png)