# Practice Test 2: AWS Cloud Practitioner CLF-C02: Exam-Focused Prep

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A media company owns physical servers sized for its historical peak holiday traffic. For the other eleven months of the year, those servers run at roughly 15% utilization, yet the company still pays for 100% of the hardware, power, and floor space. Which AWS Cloud advantage MOST directly addresses this specific inefficiency?

A) Trade capital expense for variable expense
B) Go global in minutes
C) Increase speed and agility
D) Stop guessing capacity

---

**Q2.** During a cloud adoption assessment, a company identifies a gap: employees lack the cloud skills needed to operate new workloads, and there is no formal training or organizational change management plan in place. According to the AWS Cloud Adoption Framework (CAF), which perspective is this gap MOST associated with?

A) Governance Perspective
B) Platform Perspective
C) People Perspective
D) Security Perspective

---

**Q3.** A finance team compares an on-premises deployment to AWS by looking only at the purchase price of servers versus AWS On-Demand hourly rates, and concludes on-premises is cheaper. Which factor is this analysis MOST likely failing to include that a proper Total Cost of Ownership (TCO) comparison requires?

A) The AWS Free Tier eligibility period
B) The AWS Well-Architected Framework review cost
C) The Amazon EC2 Reserved Instance discount percentage
D) Indirect costs such as power, cooling, facility space, and IT labor for on-premises infrastructure

---

**Q4.** An online ticket retailer's application automatically adds compute capacity in the minutes before a popular concert's tickets go on sale, then automatically removes that capacity a few hours later once demand drops. Which cloud characteristic does this BEST demonstrate?

A) Scalability
B) High availability
C) Elasticity
D) Fault tolerance

---

**Q5.** A development team redesigns a monolithic order-processing application into separate services connected by Amazon SQS queues, so that if the inventory service fails temporarily, the order-intake service can continue accepting orders without being blocked. Which cloud architecture design principle does this redesign demonstrate?

A) Vertical scaling
B) Server consolidation
C) Single point of failure elimination through hardware redundancy
D) Decoupling components

---

**Q6.** A company designs its workload so that if an Availability Zone becomes unavailable, automated processes detect the failure and route traffic to healthy resources in another Availability Zone without manual intervention. This design decision primarily supports which AWS Well-Architected Framework pillar?

A) Cost Optimization
B) Performance Efficiency
C) Operational Excellence
D) Reliability

---

**Q7.** A retail company experiences highly unpredictable traffic spikes during flash sales. In their on-premises data center, they provision servers for peak load year-round, resulting in idle capacity 80% of the time. After migrating to AWS, they configure Auto Scaling to automatically add and remove EC2 instances based on real-time demand. Which advantage of cloud computing does this scenario BEST illustrate?

A) Trade capital expense for variable expense
B) Go global in minutes
C) Stop guessing capacity
D) Increase speed and agility

---

**Q8.** A CIO wants to launch an AWS cloud migration initiative and needs to build a business case, define target business outcomes, and align the migration roadmap with overall corporate strategy before any technical work begins. Which AWS Cloud Adoption Framework (CAF) perspective addresses this need?

A) Platform Perspective
B) Operations Perspective
C) Business Perspective
D) Governance Perspective

---

**Q9.** An order-processing application has an inventory service that calls a shipping service directly via synchronous API calls. When the shipping service becomes temporarily overloaded, the inventory service also fails, and the entire application goes down. Which architectural principle should be applied to prevent this cascading failure?

A) Enable Multi-Factor Authentication on both services
B) Introduce a message queue to decouple the two services
C) Move both services into the same Availability Zone
D) Increase the instance size of the shipping service

---

**Q10.** A company currently spends $600,000 every three years purchasing physical servers upfront, regardless of how much compute capacity is actually used. After migrating workloads to Amazon EC2, this large upfront purchase is replaced by hourly or per-second charges based on actual instance usage. This scenario BEST illustrates converting which type of cost into which type of cost?

A) Capital expense into variable expense
B) Variable expense into fixed expense
C) Operational expense into capital expense
D) Fixed expense into unpredictable revenue

---

**Q11.** A company running a fleet of EC2 instances notices that several instances are consistently utilized at only 10-15% CPU. They want to reduce spend by matching instance types and sizes to actual workload requirements while continuing to meet performance needs. Which pillar of the AWS Well-Architected Framework MOST directly addresses this practice?

A) Reliability
B) Cost Optimization
C) Security
D) Performance Efficiency

---

**Q12.** A company runs its entire application on AWS Lambda, using function code that processes customer orders. Under the AWS shared responsibility model, which task is AWS responsible for?

A) Managing IAM permissions assigned to the Lambda function
B) Writing secure, vulnerability-free application code
C) Patching and maintaining the underlying operating system and runtime infrastructure
D) Configuring environment variables and function-level settings

---

**Q13.** A company needs to automatically discover, classify, and alert on sensitive data such as personally identifiable information (PII) stored in Amazon S3 buckets. Which AWS service should they use?

A) Amazon Macie
B) Amazon GuardDuty
C) Amazon Inspector
D) AWS Shield

---

**Q14.** A company wants its employees to sign in once using their existing corporate directory credentials and then access multiple AWS accounts without creating separate IAM users in each account. Which AWS service should they use?

A) IAM Identity Center
B) AWS Organizations
C) IAM user groups
D) IAM roles assigned per employee

---

**Q15.** A security team wants to apply the strongest recommended protection to the AWS account root user immediately after creating a new AWS account. Which action should they take?

A) Enable multi-factor authentication (MFA) on the root user and avoid using it for daily tasks
B) Delete the root user after account setup
C) Add the root user to an IAM group with read-only permissions
D) Create an IAM role that assumes the root user's permissions

---

**Q16.** An e-commerce company's web application is being targeted by an attack that sends malicious HTTP requests containing SQL injection patterns to exploit its login form. Which AWS service should the company configure with rules to detect and block this specific type of application-layer attack?

A) AWS Shield Standard
B) AWS WAF
C) Amazon GuardDuty
D) AWS Shield Advanced

---

**Q17.** A company's compliance team needs to download AWS's ISO 27001 certification report on demand to satisfy an internal audit requirement. Which AWS service provides access to this type of compliance documentation?

A) AWS Config
B) AWS Artifact
C) AWS CloudTrail
D) AWS Trusted Advisor

---

**Q18.** A company runs a data-processing workload entirely on AWS Lambda functions triggered by S3 events. Under the AWS shared responsibility model, who is responsible for patching the operating system and runtime environment that executes the Lambda code?

A) The customer, because they wrote the function code
B) AWS, because Lambda is a serverless compute service
C) Both AWS and the customer share this task equally
D) A third-party AWS Partner selected during Lambda setup

---

**Q19.** An auditor requires a formal copy of AWS's ISO 27001 certification and SOC 2 report to complete a compliance review. Which AWS service provides on-demand access to these compliance documents?

A) AWS Artifact
B) AWS Trusted Advisor
C) AWS Config
D) Amazon Inspector

---

**Q20.** A security team wants a service that automatically scans the contents of S3 buckets to identify and alert on sensitive data such as credit card numbers and personally identifiable information (PII). Which AWS service should they enable?

A) Amazon GuardDuty
B) Amazon Macie
C) AWS WAF
D) Amazon Inspector

---

**Q21.** A company manages 15 separate AWS accounts under AWS Organizations and wants employees to sign in once with centralized credentials to access any of these accounts without creating separate IAM users in each one. Which service BEST meets this requirement?

A) IAM Identity Center
B) IAM users with the AdministratorAccess policy
C) Service control policies (SCPs)
D) IAM access keys shared across accounts

---

**Q22.** A company follows AWS best practices for root user protection. Which of the following tasks requires signing in as the AWS account root user rather than an IAM identity?

A) Launching a new EC2 instance
B) Creating an IAM policy for a development team
C) Closing the AWS account
D) Creating an S3 bucket for log storage

---

**Q23.** A company running a public-facing web application on AWS wants proactive DDoS response support, real-time attack visibility, and cost protection against scaling charges incurred during a large-scale DDoS event. Which offering should they subscribe to?

A) AWS WAF with default managed rule groups only
B) AWS Shield Advanced
C) AWS Shield Standard
D) Amazon GuardDuty with S3 protection enabled

---

**Q24.** A company runs a data-processing workload entirely on AWS Lambda, using S3 as the event source. Under the AWS shared responsibility model, which of the following security tasks is the CUSTOMER's responsibility?

A) Configuring the IAM permissions granted to the function's execution role
B) Applying firmware updates to the host hardware running the Lambda service
C) Maintaining physical security of the data centers hosting the Lambda execution environment
D) Patching the operating system of the underlying Lambda execution environment

---

**Q25.** A company stores several million documents in Amazon S3 and needs to automatically scan the objects to discover and classify sensitive data, such as personally identifiable information (PII) and financial account numbers. Which AWS service is PURPOSE-BUILT for this requirement?

A) Amazon GuardDuty
B) Amazon Inspector
C) Amazon Macie
D) AWS WAF

---

**Q26.** A financial services company needs a private, dedicated network connection from its on-premises data center to AWS that provides consistent low latency and higher bandwidth than an internet-based connection, and does not traverse the public internet. Which AWS service BEST meets this requirement?

A) AWS Site-to-Site VPN
B) Internet Gateway
C) AWS Transit Gateway
D) AWS Direct Connect

---

**Q27.** A DevOps team wants to define their entire AWS infrastructure — VPCs, EC2 instances, security groups, and RDS databases — in version-controlled template files that can be repeatably deployed and updated as a single unit. Which AWS service is designed for this?

A) AWS Elastic Beanstalk
B) AWS OpsWorks
C) AWS Systems Manager
D) AWS CloudFormation

---

**Q28.** A media company runs a rendering application on multiple EC2 instances that all need simultaneous read/write access to the same shared file system, with automatic scaling of storage capacity as files are added. Which storage service should they use?

A) Amazon EBS
B) Amazon EFS
C) Amazon S3
D) EC2 Instance Store

---

**Q29.** A company hosts a static website on Amazon S3 and wants to reduce latency for users worldwide by caching content at locations physically closer to them, while also reducing direct load on the S3 bucket. Which AWS service should they add in front of S3?

A) Amazon Route 53
B) AWS Global Accelerator
C) AWS Direct Connect
D) Amazon CloudFront

---

**Q30.** A company needs a relational database that is compatible with MySQL, provides up to 5 times the throughput of standard MySQL on the same hardware, and automatically replicates 6 copies of data across 3 Availability Zones for high durability. Which service should they choose?

A) Amazon RDS for MySQL
B) Amazon Aurora
C) Amazon DynamoDB
D) Amazon Redshift

---

**Q31.** According to AWS global infrastructure design, what is the minimum number of Availability Zones that AWS provisions within each Region?

A) 3
B) 1
C) 2
D) 4

---

**Q32.** A financial services company needs a network connection between its on-premises data center and AWS that provides consistent, low-latency throughput and does not traverse the public internet at all. Which connectivity option BEST meets this requirement?

A) AWS Site-to-Site VPN
B) An Internet Gateway attached to the VPC
C) AWS Transit Gateway
D) AWS Direct Connect

---

**Q33.** A company wants to deploy a multi-container application without provisioning or managing any underlying EC2 instances, while AWS fully handles the container orchestration infrastructure. Which option BEST meets this requirement?

A) Amazon EKS with self-managed EC2 worker nodes
B) Amazon EC2 Auto Scaling group running Docker manually installed on each instance
C) AWS Lambda functions packaged as container images
D) Amazon ECS with the AWS Fargate launch type

---

**Q34.** A global web application has backend servers deployed in us-east-1, eu-west-1, and ap-southeast-1. The company wants Amazon Route 53 to direct each user's request to whichever region currently provides the fastest response time based on measured network performance, rather than the user's physical location. Which routing policy should be configured?

A) Geolocation routing
B) Weighted routing
C) Latency-based routing
D) Failover routing

---

**Q35.** Which statement correctly distinguishes an AWS Availability Zone from a CloudFront edge location?

A) An Availability Zone consists of one or more discrete data centers with redundant power and networking used to run full AWS services, while an edge location is a site used by CloudFront and Route 53 to cache content and reduce latency for end users.
B) An Availability Zone is a single data center used only for CloudFront caching, while an edge location contains multiple full AWS Regions.
C) Availability Zones and edge locations are the same infrastructure component, just named differently depending on the service being used.
D) An edge location is used to host EC2 instances for general compute workloads, while an Availability Zone is used only for content caching.

---

**Q36.** A media processing application runs on multiple EC2 instances spread across three Availability Zones within the same VPC. All instances must concurrently read and write to the same set of files. Which storage solution BEST meets this requirement?

A) Amazon EBS Multi-Attach volume
B) Amazon EFS
C) Amazon S3 Standard
D) An Amazon EBS Provisioned IOPS volume attached separately to each instance

---

**Q37.** A company needs a fully managed relational database that is compatible with its existing MySQL applications, delivers up to five times the throughput of standard MySQL running on comparable hardware, and automatically scales storage up to 128 TB as data grows. Which AWS service meets these requirements?

A) Amazon RDS for MySQL
B) Amazon DynamoDB
C) Amazon Redshift
D) Amazon Aurora MySQL-Compatible Edition

---

**Q38.** A media company runs a rendering farm of 50 Linux EC2 instances that must all read and write to the same file system concurrently, with POSIX file permissions and automatic capacity scaling as files are added. Which AWS service BEST meets these requirements?

A) Amazon EBS with Multi-Attach enabled across all 50 instances
B) Amazon S3 with an EC2 instance profile mounted via s3fs
C) Amazon EFS mounted on all 50 instances via the NFS client
D) Amazon FSx for Windows File Server joined to AWS Managed Microsoft AD

---

**Q39.** A financial services firm must transfer 20TB of data daily between its on-premises data center and AWS with consistent low latency and bandwidth that does not compete with regular internet traffic. Which connectivity option BEST satisfies this requirement?

A) AWS Site-to-Site VPN over the public internet
B) An internet gateway attached to the VPC
C) AWS Transit Gateway with no additional connectivity configured
D) AWS Direct Connect with a dedicated connection

---

**Q40.** A retail analytics team needs to run complex SQL joins and aggregations across 5 petabytes of historical sales data using standard business intelligence tools, with columnar storage optimized for large-scale analytical queries. Which AWS service is the BEST fit?

A) Amazon DynamoDB
B) Amazon RDS for MySQL
C) Amazon Redshift
D) Amazon Aurora Serverless

---

**Q41.** A company runs a fleet of EC2 instances for a production workload that must run continuously for the next 3 years. Over that period, the team expects to change instance families, sizes, operating systems, and tenancy multiple times as the application evolves, but wants the maximum possible discount for committing to steady usage. Which purchasing option BEST meets these requirements?

A) Compute Savings Plans (3-year term)
B) Standard Reserved Instances (3-year term)
C) Convertible Reserved Instances (3-year term)
D) Spot Instances

---

**Q42.** A finance team needs a detailed, hourly line-item report of all AWS costs and usage, broken down by individual resource ID and cost allocation tag, delivered automatically to an S3 bucket for ingestion into a third-party BI tool. Which AWS service should they use?

A) AWS Cost Explorer
B) AWS Cost and Usage Report (CUR)
C) AWS Budgets
D) AWS Pricing Calculator

---

**Q43.** A company uses AWS Organizations with consolidated billing across 12 member accounts. One member account purchases a Reserved Instance for an m5.large instance in us-east-1. By default, how is the RI discount applied across the organization?

A) The discount is automatically shared with any account in the organization that has matching, unused instance usage
B) The Reserved Instance discount must be manually transferred between accounts
C) The discount applies only to the member account that purchased the RI
D) The management (payer) account always receives the full discount regardless of which account uses matching instances

---

**Q44.** A company running mission-critical workloads needs a guaranteed less-than-15-minute response time for business-critical system-down cases, along with a dedicated Technical Account Manager and proactive Infrastructure Event Management. Which AWS Support plan meets these requirements?

A) AWS Developer Support Plan
B) AWS Business Support Plan
C) AWS Enterprise Support Plan
D) AWS Enterprise On-Ramp Support Plan

---

**Q45.** Which statement accurately differentiates AWS Trusted Advisor access between the Business/Enterprise support plans and the Basic/Developer support plans?

A) Business and Enterprise plans unlock the full set of Trusted Advisor checks across all categories, while Basic and Developer plans only see a limited set of core security and service-limit checks
B) Basic and Developer plans include every Trusted Advisor check but without email notifications
C) Trusted Advisor is exclusively available to customers on the Enterprise Support plan
D) Trusted Advisor provides the identical set of checks on every support plan, and only the response SLA changes

---

