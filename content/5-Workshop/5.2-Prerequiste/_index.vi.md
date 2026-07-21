---
title: "Các bước chuẩn bị"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

#### 1. Phân quyền tài khoản (IAM Permissions)

Để triển khai được các tài nguyên trong bài workshop này, tài khoản AWS của bạn cần được cấp các quyền hạn thao tác cơ bản trên **Amazon S3**, **Amazon RDS** và **AWS IAM**.

Đoạn mã IAM Policy JSON mẫu dưới đây định nghĩa các quyền hạn tối thiểu cần thiết:

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