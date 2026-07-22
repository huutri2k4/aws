---
title: "Weekly Work Log - Week 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:
* Deploy an Auto Scaling Group and test infrastructure Self-healing capabilities on AWS.
* Kick off the group project "Internship Management System": Define requirements, allocate tasks among 4 members, and design the UI on Figma.

### Weekly Tasks:
| Day | Task | Start Date | End Date | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **ASG Hands-on:** Provisioned and launched an Auto Scaling Group named `asg-tuan9` linked with the existing Launch template. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Testing Self-healing:** Manually terminated a running EC2 instance to verify if the ASG automatically triggers a replacement server. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Project Kickoff Meeting:** The 4-member team met to finalize the core features of the "Internship Management System" and sketch the user workflow. | 17/06/2026 | 17/06/2026 | Team Internal Docs |
| 4 | - **Task Allocation:** Divided system modules among the 4 members (Authentication, Internship tracking, and Reports) and discussed the design color scheme. | 18/06/2026 | 18/06/2026 | Team Internal Docs |
| 5 | - **UI/UX Design:** Collaborated on Figma to create basic wireframes and design high-fidelity layouts for the system's main dashboards. | 19/06/2026 | 19/06/2026 | Figma / Wireframe Tool |
| 6 | - **Project Setup:** Initialized the code repository structure, defined naming conventions, and established Git workflow rules for team collaboration. | 20/06/2026 | 20/06/2026 | Project Repository |

### Week 9 Outcomes:
* Successfully created the **Auto Scaling group (`asg-tuan9`)** with Min/Max/Desired operational parameters configured to 1.
* Validated the **Self-healing** infrastructure kpi; the system successfully auto-healed by generating a fresh instance after an unexpected termination.
* Finalized project specifications and established clear role definitions for the 4 team members on the Internship Management System.
* Completed wireframes and UI components on Figma, and established the baseline Git workspace ready for development.

![Nguyen Huu Tri](/aws/images/tuan9,1.png)