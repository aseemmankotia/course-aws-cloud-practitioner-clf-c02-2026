# Practice Test 1: AWS Cloud Practitioner CLF-C02: Exam-Focused Prep

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A retail company purchases enough on-premises servers each year to handle its projected Black Friday traffic, based on capacity estimates made months in advance. In years when actual demand is lower than projected, the expensive hardware sits idle and depreciates. Which AWS Cloud advantage BEST addresses this problem?

A) Trade capital expense for variable expense
B) Stop guessing about capacity
C) Increase speed and agility
D) Go global in minutes

---

**Q2.** A company runs its entire customer-facing application on a single EC2 instance in one Availability Zone. When that instance experienced a hardware fault, the application became completely unavailable for several hours. Which design principle should the company apply to increase resilience against this type of failure?

A) Right-size the instance to a smaller instance type
B) Purchase a Reserved Instance for the workload
C) Design for failure by deploying redundant resources across multiple Availability Zones
D) Migrate from an operating expense model to a capital expense model

---

**Q3.** Which pillar of the AWS Well-Architected Framework focuses primarily on the ability to run and monitor systems to deliver business value, and to continuously improve supporting processes and procedures?

A) Performance Efficiency
B) Operational Excellence
C) Security
D) Cost Optimization

---

**Q4.** A company is beginning its cloud migration journey and wants structured guidance on organizational structure, staff skills, change management, and governance needed for a successful transition, not just technical architecture patterns. Which AWS resource is designed to address this?

A) AWS Well-Architected Framework
B) AWS Cloud Adoption Framework (CAF)
C) AWS Trusted Advisor
D) AWS Total Cost of Ownership (TCO) Calculator

---

**Q5.** A media company's website traffic increases 10 times during a live-streamed event and returns to normal immediately afterward. The company wants capacity to automatically increase during the spike and decrease afterward without manual intervention. Which cloud characteristic enables this?

A) Managed services
B) Total cost of ownership
C) Elasticity
D) Global infrastructure reach

---

**Q6.** A development team wants to release updates to the checkout microservice of an e-commerce application without requiring code changes to, or causing downtime in, the separate inventory microservice. Which architecture principle enables this independence between components?

A) Decoupling (loose coupling) between components
B) Vertical scaling
C) Designing a single point of failure
D) Manual capacity planning

---

**Q7.** A retail company experiences unpredictable traffic spikes during flash sales, with demand sometimes increasing 10x within minutes and dropping back to normal shortly after. Which cloud characteristic BEST addresses this business need?

A) Elasticity, allowing compute resources to scale automatically with demand
B) High availability through multiple Availability Zones
C) Global infrastructure reach to serve customers in multiple regions
D) Pay-as-you-go pricing to avoid long-term contracts

---

**Q8.** A company's on-premises data center requires large upfront capital expenditure (CapEx) for servers that are only used at 20% capacity most of the year, with occasional peaks reaching 90%. Moving to AWS shifts this cost model. Which statement BEST describes this economic benefit of cloud computing?

A) AWS eliminates all operational costs by removing the need for IT staff
B) AWS guarantees lower total costs than on-premises regardless of workload
C) AWS requires a multi-year reserved commitment to achieve any cost savings
D) AWS trades fixed capital expense for variable operational expense, so you pay only for what you use

---

**Q9.** According to the AWS Cloud Adoption Framework (CAF), which perspective is PRIMARILY responsible for ensuring that cloud migration aligns with an organization's business strategy and expected financial outcomes?

A) Security perspective
B) Operations perspective
C) Business perspective
D) Platform perspective

---

**Q10.** A monolithic application's checkout service fails whenever the inventory service becomes slow, causing the entire application to become unresponsive. Which cloud architecture design principle would BEST prevent this cascading failure?

A) Vertical scaling of the underlying EC2 instance
B) Increasing the instance's provisioned IOPS for faster disk access
C) Decoupling application components using a messaging service so they can operate and fail independently
D) Storing all application state in a single relational database

---

**Q11.** Which of the following is one of the AWS-stated six advantages of cloud computing?

A) Guaranteed 100% uptime for all workloads
B) Elimination of the shared responsibility model
C) Mandatory use of a single AWS Region for all resources
D) Trade capital expense for variable expense

---

**Q12.** A company runs its application on Amazon EC2 instances within its own VPC. Under the AWS Shared Responsibility Model, who is responsible for patching the guest operating system on these EC2 instances?

A) AWS is responsible, since EC2 is a managed service
B) AWS Support is responsible if the customer has a Business support plan
C) Responsibility is shared equally between AWS and the customer for every patch
D) The customer is responsible, since EC2 is treated as infrastructure the customer controls

---

**Q13.** A company stores customer data in Amazon S3 and wants to automatically discover and classify sensitive information such as personally identifiable information (PII) stored in those buckets. Which AWS service should they use?

A) Amazon GuardDuty
B) Amazon Macie
C) AWS Shield
D) AWS Config

---

**Q14.** A company deploys its backend logic entirely using AWS Lambda functions with no EC2 instances involved. Under the AWS Shared Responsibility Model, who is responsible for patching the underlying operating system and runtime environment that executes the Lambda function code?

A) The customer, because they wrote the function code
B) AWS, because Lambda is a serverless compute service
C) Both AWS and the customer equally, since Lambda uses a shared execution environment
D) AWS Trusted Advisor, since it monitors runtime security

---

**Q15.** A solutions architect is defining security best practices for a new AWS account's root user. Which action should be taken to best protect the root user?

A) Use the root user credentials for daily administrative tasks to simplify permissions management
B) Share the root user password with all administrators so anyone can perform emergency actions
C) Delete the root user account once the AWS account is created
D) Enable multi-factor authentication (MFA) on the root user and avoid using it for everyday tasks

---

**Q16.** A company's public-facing web application on AWS is experiencing volumetric network-layer attacks intended to overwhelm its infrastructure and cause downtime. Which AWS service is specifically designed to protect against this type of attack?

A) AWS Artifact
B) AWS IAM Identity Center
C) Amazon Inspector
D) AWS Shield

---

**Q17.** A compliance officer needs to download AWS's ISO 27001 certification and SOC 2 report to satisfy an internal audit requirement. Which AWS service provides on-demand access to these compliance reports?

A) AWS Artifact
B) AWS Trusted Advisor
C) AWS Config
D) AWS CloudTrail

---

**Q18.** A company runs its application on Amazon EC2 instances using Amazon EBS volumes. According to the AWS Shared Responsibility Model, who is responsible for applying security patches to the guest operating system running on these EC2 instances?

A) AWS, because it manages all patching for compute services
B) AWS Support, but only if the customer has a Business or Enterprise support plan
C) Neither party, since EC2 instances receive automatic patches by default
D) The customer, because EC2 is infrastructure as a service and OS-level maintenance is a customer task

---

**Q19.** A company migrates a self-managed MySQL database on EC2 to Amazon RDS to reduce operational overhead. Under the AWS Shared Responsibility Model, which task does AWS take over that the customer previously had to perform themselves?

A) Designing the database schema and writing application queries
B) Encrypting data within the application before sending it to the database
C) Patching the underlying database engine software
D) Managing IAM policies that control who can access the database

---

**Q20.** A company wants a service that continuously analyzes VPC Flow Logs, AWS CloudTrail event logs, and DNS logs using machine learning to automatically identify potentially unauthorized or malicious activity in their AWS account. Which service should they use?

A) AWS Config
B) Amazon Inspector
C) Amazon GuardDuty
D) AWS Trusted Advisor

---

**Q21.** Which action is the AWS-recommended best practice to protect the AWS account root user?

A) Share the root user credentials only with senior engineers on the team
B) Enable multi-factor authentication (MFA) on the root user and avoid using it for daily tasks
C) Rotate the root user's password every 24 hours using an automated script
D) Attach an IAM policy directly to the root user to limit its permissions

---

**Q22.** A company has 15 AWS accounts organized under AWS Organizations and wants employees to sign in once and access multiple accounts and applications without creating separate IAM users in each account. Which service should they use?

A) Amazon Cognito
B) AWS Directory Service
C) AWS IAM Identity Center
D) AWS Organizations Service Control Policies

---

**Q23.** What is the primary purpose of AWS Artifact?

A) To automatically remediate non-compliant AWS resources
B) To scan source code repositories for security vulnerabilities before deployment
C) To provide on-demand access to AWS compliance reports and agreements such as SOC and PCI DSS documentation
D) To generate a real-time inventory of all security groups across an AWS account

---

**Q24.** A company is migrating from Amazon EC2 instances to AWS Lambda for a new application component. Under the AWS shared responsibility model, how does the customer's security responsibility change when moving to Lambda?

A) The customer is relieved of managing the underlying operating system and server patching, but still manages function code, IAM permissions, and data security
B) The customer must now patch the guest operating system and hypervisor for the Lambda service
C) The customer no longer needs to manage IAM permissions because Lambda is fully managed by AWS
D) The customer becomes responsible for the physical security of the data center running Lambda

---

**Q25.** A company wants an AWS service that uses machine learning to continuously analyze VPC Flow Logs, DNS logs, and CloudTrail events to automatically detect unusual API calls and potentially unauthorized or malicious activity in their AWS account. Which service should they use?

A) AWS WAF
B) Amazon GuardDuty
C) Amazon Macie
D) AWS Shield

---

**Q26.** A financial services company needs a dedicated, private network connection between its on-premises data center and AWS to support large, consistent data transfers with predictable, low-latency performance. The connection must not traverse the public internet. Which solution BEST meets these requirements?

A) AWS Site-to-Site VPN
B) AWS Transit Gateway
C) AWS Direct Connect
D) Internet Gateway

---

**Q27.** A company wants to run several containerized microservices continuously without provisioning, patching, or managing any underlying EC2 instances. Which AWS service BEST meets this requirement?

A) AWS Lambda
B) Amazon EC2
C) Amazon EMR
D) AWS Fargate

---

**Q28.** A company must retain compliance log data for 7 years. The data is accessed frequently during the first 30 days, then rarely afterward, and a retrieval time of several hours is acceptable for archived data. Which S3 storage class should be applied via a lifecycle policy for the long-term archival phase to minimize cost?

A) S3 Glacier Deep Archive
B) S3 One Zone-IA
C) S3 Standard
D) S3 Intelligent-Tiering

---

**Q29.** Which statement correctly describes the relationship between AWS Regions and Availability Zones?

A) A Region consists of multiple, isolated Availability Zones located within the same geographic area
B) An Availability Zone contains multiple Regions to provide fault tolerance
C) A Region is a single data center, while an Availability Zone spans multiple geographic areas
D) Availability Zones and Regions are interchangeable terms for the same infrastructure component

---

**Q30.** A gaming company needs a fully managed NoSQL database capable of handling millions of requests per second with consistent single-digit millisecond latency at any scale, storing player session data as simple key-value pairs. Which AWS service BEST meets this requirement?

A) Amazon DynamoDB
B) Amazon Aurora
C) Amazon RDS
D) Amazon Redshift

---

**Q31.** A DevOps team wants to define their AWS infrastructure — including a VPC, EC2 instances, and security groups — as code so that deployments are repeatable and version-controlled across multiple environments. Which AWS service should they use?

A) AWS Trusted Advisor
B) AWS CloudFormation
C) AWS Systems Manager
D) AWS Config

---

**Q32.** A media company stores video thumbnails and static assets in an S3 bucket and wants viewers around the world to experience low-latency access to this content by caching copies at locations close to users. Which AWS service BEST meets this requirement?

A) AWS Direct Connect
B) AWS Global Accelerator
C) Amazon Route 53
D) Amazon CloudFront

---

**Q33.** A development team needs to run containerized applications on AWS but does not want to provision, patch, or manage any underlying EC2 instances. Which compute option should they choose?

A) Amazon EC2 Auto Scaling
B) AWS Elastic Beanstalk
C) Amazon EMR
D) AWS Fargate

---

**Q34.** In which file format(s) can an AWS CloudFormation template be written?

A) XML only
B) YAML only
C) JSON only
D) JSON or YAML

---

**Q35.** Which statement correctly describes an AWS Availability Zone?

A) One or more discrete data centers with redundant power, networking, and connectivity, located within an AWS Region
B) A city that contains multiple AWS Regions
C) A single data center that makes up an entire AWS Region
D) A global network of caching servers used to deliver content closer to users

---

**Q36.** A gaming company needs a fully managed NoSQL database that delivers consistent single-digit millisecond latency at any scale for storing player session data. Which AWS service should they use?

A) Amazon RDS
B) Amazon Redshift
C) Amazon DynamoDB
D) Amazon Aurora

---

**Q37.** A company wants to define its entire cloud infrastructure — VPCs, subnets, EC2 instances, and security groups — as version-controlled code that can be repeatably deployed across development, test, and production environments. Which AWS service is BEST suited for this?

A) AWS CloudFormation
B) AWS Management Console
C) AWS CLI
D) AWS Systems Manager

---

**Q38.** A company runs a hybrid workload with an on-premises data center that must transfer large data sets to AWS every night for analytics processing. The connection needs consistent, low-latency, high-throughput performance and must bypass the public internet entirely. Which connectivity option BEST meets these requirements?

A) Site-to-Site VPN over the public internet
B) AWS Client VPN
C) Amazon CloudFront with an origin access identity
D) AWS Direct Connect

---

**Q39.** According to AWS global infrastructure design, what does a single Availability Zone consist of?

A) A single data center located at the geographic center of an AWS Region
B) One or more discrete data centers with redundant power, networking, and connectivity, isolated from failures in other Availability Zones
C) A collection of edge locations used to cache content close to end users
D) A virtual boundary within a VPC used to isolate subnets for security purposes

---

**Q40.** A mobile gaming company needs a database to store player profile and session data. The application requires single-digit millisecond response times at massive scale, with a flexible schema since player attributes vary by game mode. Which AWS service BEST fits this requirement?

A) Amazon Redshift
B) Amazon DynamoDB
C) Amazon RDS for PostgreSQL
D) Amazon EFS

---

**Q41.** A retail company runs a business-critical e-commerce workload on AWS and requires a guaranteed response time of less than 15 minutes when that workload is completely down. Which AWS Support plan is the minimum required to meet this requirement?

A) Business
B) Enterprise
C) Developer
D) Basic

---

**Q42.** A company wants a single AWS tool that automatically inspects their AWS environment and provides real-time recommendations across five categories: cost optimization, performance, security, fault tolerance, and service limits. Which AWS service provides this?

A) AWS Trusted Advisor
B) AWS Cost Explorer
C) AWS Budgets
D) AWS Health Dashboard

---

**Q43.** A company purchasing a 1-year Standard Reserved Instance wants to maximize their discount compared to On-Demand pricing and is willing to pay the entire cost of the reservation immediately. Which payment option should they choose?

A) All Upfront
B) No Upfront
C) Partial Upfront
D) Monthly Upfront

---

**Q44.** How does an AWS Compute Savings Plan differ from a Standard Reserved Instance?

A) A Compute Savings Plan applies its discount regardless of instance family, size, OS, tenancy, or AWS Region, while a Standard Reserved Instance is tied to a specific instance configuration and Region
B) A Compute Savings Plan can only be purchased with a 3-year commitment, while Reserved Instances support both 1-year and 3-year terms
C) A Compute Savings Plan does not require any usage commitment, while a Standard Reserved Instance requires a fixed hourly commitment
D) A Compute Savings Plan can only be used with Amazon EC2, while a Standard Reserved Instance can be used with EC2, Fargate, and Lambda

---

**Q45.** A company has 12 separate AWS accounts for different departments and wants to receive a single monthly invoice while also qualifying for volume pricing discounts based on the combined usage across all accounts. Which AWS feature should they use?

A) AWS Cost and Usage Report
B) AWS Budgets
C) Consolidated billing in AWS Organizations
D) AWS Pricing Calculator

---

