---
title: "Blog 3"
date: 2026-07-09
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# DEPLOY MODERN DATA PLATFORMS IN MINUTES WITH MODERN DATA ARCHITECTURE ACCELERATOR (MDAA)

Hello everyone in the AWS Study Group VN community.

In the process of learning about **AWS Big Data**, I read a very interesting blog post introducing the **Modern Data Architecture Accelerator (MDAA)** – an open-source framework developed by AWS to help enterprises deploy a Modern Data Platform faster and easier while strictly complying with **AWS Best Practices** for security, data governance, and scalability.

If you are researching **Data Lakes, Data Platforms, or AI Platforms on AWS**, this is a highly recommended solution to consider.

### Why Did AWS Develop MDAA?
A Modern Data Platform today is no longer just about creating an S3 Bucket to store data. A complete production system usually requires integrating numerous AWS services such as **Amazon S3** for storage, **AWS Glue** for ETL and metadata cataloging, **AWS Lake Formation** for data governance, **AWS IAM** for permission mapping, **AWS KMS** for data encryption, **CloudTrail** for audit logging, and **CloudWatch** for system monitoring, among other components.

This makes infrastructure construction highly complex. Besides understanding each individual service, the deployment team must ensure everything is configured properly regarding **Security, Governance, and Compliance**. According to AWS, this manual setup process typically consumes a significant amount of time and is highly prone to operational errors.

### How Does MDAA Work?
The most prominent highlight of MDAA is **revolutionizing infrastructure provisioning**. Instead of manually writing thousands of lines of Infrastructure as Code to create each AWS resource, users **only need to declare their desired configurations inside a single YAML file**.

**Example:**
* Set up a Data Lake.
* Enable data encryption.
* Govern access permissions.
* Capture Audit Logs.
* Deploy Data Quality controls.

MDAA then **automatically translates these declarations into a fully realized AWS architecture** utilizing the **AWS CDK and CloudFormation**. According to data published by AWS, in a typical governed Data Lake deployment example, the infrastructure code footprint can be **slashed from approximately 1,800 lines of CloudFormation down to just about 45 lines of YAML**, significantly simplifying the deployment cycle.

### MDAA Is Built on a Modular Architecture
An excellent point highlighted in the article is that MDAA is not a rigid single product but is built on a **modular architecture**. AWS currently provides **over 40 distinct modules**, each handling a specific function such as data storage, ETL pipelines, data governance, Machine Learning, or Generative AI.

These modules can be **combined together like LEGO blocks**. When an enterprise needs to scale out its platform, they can simply plug in additional modules instead of redesigning the entire system architecture. To allow seamless cross-module communication, MDAA utilizes **AWS Systems Manager Parameter Store** to share configuration metadata across components, avoiding the need to manually hardcode resource ARNs or resource IDs.

### Governance Integrated Right from Launch
In many real-world enterprise deployments, Data Governance is often treated as an afterthought, patched in only after system delivery. AWS chooses a completely different path.

Right from the initial deployment phase, MDAA comes **pre-configured with built-in data governance services** including **AWS Lake Formation, AWS Glue Data Catalog, AWS KMS, and CloudTrail**. This empowers enterprises to establish a robust, compliant data platform right from day one instead of dealing with structural refactoring down the line.

### Four Pre-Built Reference Architectures
To accommodate various institutional data requirements, AWS has pre-engineered **four reference architectures**:
* The first model is the **Basic Data Lake**, ideal for organizations looking to aggregate data from fragmented sources into a single, centralized repository.
* When advanced analytics or Machine Learning workflows are required, organizations can elastically expand into a **Data Science Platform**.
* If cross-functional teams such as Data Engineers, Data Analysts, and Data Scientists need to collaborate in a single environment, they can roll out **SageMaker Unified Studio**.
* For teams looking to build Generative AI applications on localized enterprise data, MDAA provides ready-made expansion paths utilizing **Amazon Bedrock and Retrieval-Augmented Generation (RAG)** without forcing a re-architecting of the data foundation.

**Real-World Case Study:**
The article highlights a practical deployment case involving a **university network with 17 campuses, managing roughly 7.2 TB of data and over 8,000 active dashboards**. Following the adoption of MDAA, **the deployment velocity for new features and analytical dashboards was accelerated by approximately 95%**, while successfully standardizing data governance across all branches and significantly minimizing dependency on third-party products. This example underscores that MDAA is optimized for large-scale enterprise data operations rather than simple apps.

### Is MDAA Suitable for Every Project?
According to the blog content, MDAA is explicitly engineered for enterprises building **Modern Data Platforms, Data Lakes, or high-volume analytical architectures**. The core strength of this framework lies not in provisioning more AWS services, but in its **ability to standardize entire architectures according to AWS Best Practices**, vastly shortening delivery timelines and enabling data teams to focus on data analytics rather than infrastructure management.

### Conclusion
In my opinion, MDAA represents a highly compelling approach by AWS toward modern data infrastructure engineering. Instead of forcing cloud engineers to configure individual siloed services, MDAA **automates near-total pipeline provisioning** while **embedding data governance, perimeter security, and horizontal scalability** from the ground up.

If you are currently exploring Data Lakes, Data Platforms, or scalable data grid designs on AWS, this is an incredibly valuable read to understand how AWS is standardizing complex, high-capacity enterprise data deployments.

**Reference Source:** <https://aws.amazon.com/blogs/big-data/deploy-modern-data-platforms-in-minutes-with-mdaa/>