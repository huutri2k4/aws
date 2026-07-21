---
title: "Preparation Steps"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

#### 1. IAM Permissions

To deploy the resources used in this workshop, your AWS account must have the necessary permissions to manage **Amazon S3**, **Amazon RDS**, and **AWS IAM** resources.

The following sample IAM Policy JSON defines the minimum permissions required:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "WorkshopPermissions",
            "Effect": "Allow",
            "Action": [
                "s3:CreateBucket",
                "s3:DeleteBucket",
                "s3:PutObject",
                "s3:GetObject",
                "s3:DeleteObject",
                "s3:ListAllMyBuckets",
                "s3:ListBucket",
                "rds:CreateDBInstance",
                "rds:DeleteDBInstance",
                "rds:DescribeDBInstances",
                "rds:CreateDBSubnetGroup",
                "iam:CreateRole",
                "iam:CreatePolicy",
                "iam:AttachRolePolicy",
                "iam:PassRole"
            ],
            "Resource": "*"
        }
    ]
}
```



![Nguyen Huu Tri](/images/s3.png)



![Nguyen Huu Tri](/images/s3,1.png)



![Nguyen Huu Tri](/images/s3,2.png)



![Nguyen Huu Tri](/images/s3,3.png)