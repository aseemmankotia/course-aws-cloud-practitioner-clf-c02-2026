# Answer Key — Practice Test 1

**Q1. Correct: B**

The company's core problem is having to forecast future demand and provision hardware accordingly. AWS lets you scale resources up or down based on actual real-time demand, eliminating the need to guess capacity requirements in advance.

---

**Q2. Correct: C**

Designing for failure means assuming any individual component can fail and architecting redundancy, such as running instances across multiple Availability Zones, so a single failure does not cause an outage.

---

**Q3. Correct: B**

The Operational Excellence pillar covers running and monitoring systems to deliver business value and continually improving processes and procedures, including automation and learning from operational events.

---

**Q4. Correct: B**

The AWS Cloud Adoption Framework (CAF) provides guidance across business, people, governance, platform, security, and operations perspectives to help organizations manage the organizational change involved in cloud adoption.

---

**Q5. Correct: C**

Elasticity is the ability of a cloud environment to automatically scale computing resources up or down to match demand, which directly addresses handling a temporary traffic spike without manual provisioning.

---

**Q6. Correct: A**

Decoupling, often implemented with mechanisms like message queues or APIs, allows components such as microservices to be developed, deployed, and scaled independently, so a change to one component does not require changes to or downtime in another.

---

**Q7. Correct: A**

Elasticity is the ability to automatically scale resources up or down to match real-time demand, which directly solves the problem of rapid, unpredictable traffic spikes and drops.

---

**Q8. Correct: D**

One of the core cloud economic benefits is trading upfront fixed capital expenditure for variable operating expenditure, paying only for the compute capacity actually consumed instead of provisioning for peak capacity year-round.

---

**Q9. Correct: C**

The Business perspective in AWS CAF focuses on ensuring that IT aligns with business needs and that cloud investments deliver measurable business value and financial outcomes.

---

**Q10. Correct: C**

Decoupling components (for example, using a queue between services) allows each component to scale and fail independently, preventing a slowdown or failure in one service from cascading through the entire application. This is one of the foundational 'design for failure' principles taught at the Cloud Practitioner level.

---

**Q11. Correct: D**

Trading fixed capital expense (CapEx) for variable expense (OpEx) is explicitly listed among the AWS six advantages of cloud computing, alongside benefits of massive economies of scale, stopping guessing capacity, increasing speed and agility, no cost to run and maintain data centers, and going global in minutes.

---

**Q12. Correct: D**

For EC2, AWS manages security 'of' the cloud (physical hosts, hypervisor), but the customer is responsible for security 'in' the cloud, which includes guest OS patching, application software, and firewall/security group configuration.

---

**Q13. Correct: B**

Amazon Macie uses machine learning and pattern matching to automatically discover, classify, and protect sensitive data such as PII stored in Amazon S3.

---

**Q14. Correct: B**

With serverless services like Lambda, AWS's responsibility expands to include the operating system, runtime patching, and underlying infrastructure, while the customer remains responsible only for their function code, IAM permissions, and configuration.

---

**Q15. Correct: D**

AWS best practice is to enable MFA on the root user, secure its credentials, and avoid using the root user for routine tasks — instead creating IAM users/roles with least-privilege permissions for daily work.

---

**Q16. Correct: D**

AWS Shield provides protection against Distributed Denial of Service (DDoS) attacks, including automatic protection at no extra cost (Shield Standard) and advanced protections (Shield Advanced) for network and transport layer attacks.

---

**Q17. Correct: A**

AWS Artifact is a self-service portal that provides on-demand access to AWS compliance reports, such as ISO certifications and SOC reports, as well as agreements like the Business Associate Addendum (BAA).

---

**Q18. Correct: D**

For EC2 (IaaS), AWS secures the hardware, hypervisor, and physical infrastructure ('security OF the cloud'), while the customer is responsible for guest OS patching, application software, and network/firewall configuration ('security IN the cloud').

---

**Q19. Correct: C**

RDS is a managed service, so AWS takes on responsibility for patching the underlying OS and database engine, whereas on self-managed EC2 the customer had to handle this themselves. This illustrates how the responsibility line shifts toward AWS for managed services.

---

**Q20. Correct: C**

Amazon GuardDuty is a threat detection service that uses machine learning to continuously analyze VPC Flow Logs, CloudTrail logs, and DNS logs to identify anomalous or malicious activity without requiring the customer to deploy agents.

---

**Q21. Correct: B**

AWS recommends enabling MFA on the root user, securing its credentials, and avoiding routine use of the root account, instead creating an IAM administrator user or role for daily tasks.

---

**Q22. Correct: C**

AWS IAM Identity Center (formerly AWS SSO) provides centralized single sign-on access across multiple AWS accounts and business applications, integrating with AWS Organizations to eliminate the need for separate IAM users per account.

---

**Q23. Correct: C**

AWS Artifact is a self-service portal that gives customers on-demand access to AWS compliance reports (such as SOC and PCI DSS reports) and allows them to review and accept agreements like the Business Associate Addendum (BAA).

---

**Q24. Correct: A**

With Lambda, AWS manages the underlying infrastructure, operating system, and runtime patching (moving further into 'security of the cloud'), while the customer remains responsible for their function code, IAM permissions/roles, environment variables, and data ('security in the cloud').

---

**Q25. Correct: B**

Amazon GuardDuty is a threat detection service that uses machine learning and anomaly detection on VPC Flow Logs, DNS logs, and CloudTrail events to identify unauthorized behavior and potential threats.

---

**Q26. Correct: C**

AWS Direct Connect establishes a dedicated, private physical network connection between on-premises infrastructure and AWS, bypassing the public internet and providing consistent, low-latency, high-bandwidth throughput ideal for large data transfers.

---

**Q27. Correct: D**

AWS Fargate is a serverless compute engine for containers used with Amazon ECS or EKS that automatically provisions and scales the underlying infrastructure, removing the need to manage EC2 instances.

---

**Q28. Correct: A**

S3 Glacier Deep Archive offers the lowest per-GB storage cost in S3, making it ideal for long-term compliance data that is rarely accessed and where retrieval times of hours are acceptable.

---

**Q29. Correct: A**

An AWS Region is a geographic area that contains multiple, physically separated and isolated Availability Zones, each consisting of one or more data centers with independent power, cooling, and networking, enabling fault tolerance within the Region.

---

**Q30. Correct: A**

Amazon DynamoDB is a fully managed NoSQL key-value and document database built for consistent single-digit millisecond performance at virtually any scale, making it the standard choice for high-throughput session/key-value data.

---

**Q31. Correct: B**

AWS CloudFormation lets teams define AWS resources using declarative templates (JSON/YAML), enabling repeatable, version-controlled, automated provisioning of infrastructure as code across environments.

---

**Q32. Correct: D**

Amazon CloudFront is AWS's content delivery network (CDN) that caches content at edge locations worldwide, reducing latency for end users accessing static or dynamic content.

---

**Q33. Correct: D**

AWS Fargate is a serverless compute engine for containers that works with ECS or EKS, eliminating the need to provision or manage EC2 instances for running containers.

---

**Q34. Correct: D**

AWS CloudFormation supports templates written in either JSON or YAML format, giving users flexibility in how they define infrastructure as code.

---

**Q35. Correct: A**

An Availability Zone (AZ) consists of one or more discrete data centers with redundant power, networking, and connectivity, isolated from failures in other AZs, and each AWS Region contains multiple AZs.

---

**Q36. Correct: C**

Amazon DynamoDB is a fully managed NoSQL key-value and document database designed to deliver consistent single-digit millisecond performance at any scale, making it ideal for session data and high-throughput workloads.

---

**Q37. Correct: A**

AWS CloudFormation is an Infrastructure as Code (IaC) service that lets you define AWS resources in JSON or YAML templates, enabling consistent, repeatable, version-controlled deployments across multiple environments.

---

**Q38. Correct: D**

AWS Direct Connect establishes a dedicated, private physical network connection between on-premises infrastructure and AWS, bypassing the public internet and providing consistent low latency and high, predictable throughput ideal for large nightly data transfers.

---

**Q39. Correct: B**

An Availability Zone is one or more discrete data centers with redundant power, networking, and connectivity, physically separated from other AZs in the same Region to provide fault isolation while remaining connected by low-latency links.

---

**Q40. Correct: B**

Amazon DynamoDB is a fully managed NoSQL key-value and document database that delivers consistent single-digit millisecond performance at any scale and supports flexible, schema-less data models, making it ideal for variable player profile attributes.

---

**Q41. Correct: B**

Only the Enterprise Support plan guarantees a less-than-15-minute response time, and only for business-critical system down cases. It also includes a Technical Account Manager (TAM) for proactive guidance.

---

**Q42. Correct: A**

AWS Trusted Advisor inspects an AWS account and provides recommendations across exactly these five categories: cost optimization, performance, security, fault tolerance, and service limits.

---

**Q43. Correct: A**

The All Upfront payment option requires paying the full cost of the Reserved Instance term at the start and provides the largest discount of the three available payment options.

---

**Q44. Correct: A**

Compute Savings Plans provide the most flexibility: the discount automatically applies to usage across any EC2 instance family, size, OS, tenancy, or Region, and even to Fargate and Lambda usage. Standard Reserved Instances are locked to a specific instance type and Region.

---

**Q45. Correct: C**

Consolidated billing, a feature of AWS Organizations, combines usage from all member accounts to share volume pricing discounts and produces a single consolidated invoice for the entire organization.

---

