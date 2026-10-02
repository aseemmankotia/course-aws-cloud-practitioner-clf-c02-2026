# Answer Key — Practice Test 2

**Q1. Correct: D**

Stop guessing capacity lets the company use elasticity and auto scaling to match compute supply to actual demand in real time instead of over-provisioning hardware for a rare peak, eliminating the idle capacity described.

---

**Q2. Correct: C**

The People Perspective of the AWS CAF focuses on people development, training, staffing, and organizational change management needed to adopt cloud successfully.

---

**Q3. Correct: D**

TCO analysis must include indirect on-premises costs like power, cooling, real estate, and staff needed to maintain hardware, not just the sticker price of hardware compared to cloud rates.

---

**Q4. Correct: C**

Elasticity is the ability to automatically grow AND shrink resources in response to demand, matching capacity to load in near real time, as shown by both scaling up and back down.

---

**Q5. Correct: D**

Decoupling separates application components so they interact through queues or APIs rather than direct dependencies, allowing one component's failure or slowdown to not directly impact others — a core Well-Architected design principle.

---

**Q6. Correct: D**

The Reliability pillar focuses on a workload's ability to recover from infrastructure or service disruptions automatically, including failover across Availability Zones.

---

**Q7. Correct: C**

'Stop guessing capacity' refers specifically to eliminating the need to provision for peak load in advance by scaling resources to match actual demand in real time, which is exactly what Auto Scaling accomplishes here.

---

**Q8. Correct: C**

The Business Perspective of the CAF focuses on ensuring that cloud investments accelerate digital transformation goals, helping stakeholders build the business case and align IT strategy with business outcomes.

---

**Q9. Correct: B**

Introducing a queue (such as Amazon SQS) between the two services decouples them so that the inventory service can continue accepting requests even if the shipping service is temporarily unavailable or slow, which is a core 'design for failure' and loose-coupling principle.

---

**Q10. Correct: A**

Upfront hardware purchases are capital expenditures (CapEx); paying only for compute actually consumed on EC2 is a variable operational expense (OpEx), so this scenario describes converting CapEx into variable expense — one of the core AWS cloud economic value propositions.

---

**Q11. Correct: B**

The Cost Optimization pillar specifically covers practices such as right-sizing resources to eliminate unneeded capacity while still meeting workload requirements, directly matching the scenario described.

---

**Q12. Correct: C**

For serverless services like Lambda, AWS manages the entire underlying infrastructure, including the host OS, runtime patching, and hardware — this is part of AWS's 'security of the cloud' responsibility, which expands significantly for managed/serverless services compared to EC2.

---

**Q13. Correct: A**

Amazon Macie uses machine learning and pattern matching to automatically discover, classify, and protect sensitive data (like PII and credentials) stored in Amazon S3.

---

**Q14. Correct: A**

AWS IAM Identity Center (successor to AWS Single Sign-On) provides centralized, single sign-on access across multiple AWS accounts, integrating with existing identity providers like Active Directory, so employees don't need separate IAM users per account.

---

**Q15. Correct: A**

AWS best practice is to enable MFA on the root user immediately, secure its credentials, and avoid using the root user for everyday tasks — instead, create individual IAM users/roles with least-privilege permissions for daily operations.

---

**Q16. Correct: B**

AWS WAF (Web Application Firewall) lets customers create rules, including managed rule groups, that inspect HTTP/HTTPS requests and block patterns like SQL injection and cross-site scripting at Layer 7.

---

**Q17. Correct: B**

AWS Artifact is the self-service portal that provides on-demand access to AWS's compliance reports, certifications (such as ISO 27001), and agreements, supporting the customer's audit and compliance needs.

---

**Q18. Correct: B**

With serverless services like Lambda, AWS manages the underlying host OS, runtime patching, and infrastructure. The customer is only responsible for their function code, configuration, and IAM permissions assigned to the function.

---

**Q19. Correct: A**

AWS Artifact is the self-service portal for downloading AWS compliance reports, certifications (ISO, SOC, PCI), and for reviewing and accepting agreements like the Business Associate Addendum (BAA).

---

**Q20. Correct: B**

Amazon Macie uses machine learning and pattern matching to discover and classify sensitive data, including PII and financial information, stored in Amazon S3.

---

**Q21. Correct: A**

IAM Identity Center (formerly AWS SSO) provides centralized single sign-on across multiple AWS accounts managed in AWS Organizations, letting users log in once and assume permission sets in any assigned account.

---

**Q22. Correct: C**

Certain account-level actions, such as closing an AWS account, changing the account's support plan, or restoring IAM user permissions after a lockout, can only be performed by the root user and are not delegable to IAM identities.

---

**Q23. Correct: B**

AWS Shield Advanced is the paid tier that adds 24/7 access to the AWS DDoS Response Team (DRT), detailed attack diagnostics, and cost protection for scaling charges during a DDoS event — none of which are included in the free Shield Standard tier.

---

**Q24. Correct: A**

Even with serverless services like Lambda, the customer is always responsible for identity and access management — specifically defining least-privilege IAM policies attached to the function's execution role. AWS abstracts away infrastructure, OS, and physical security in serverless models, but access control configuration remains a customer task under 'security IN the cloud.'

---

**Q25. Correct: C**

Amazon Macie uses machine learning and pattern matching to automatically discover, classify, and report on sensitive data such as PII stored in Amazon S3, making it the correct choice for this data-discovery use case.

---

**Q26. Correct: D**

AWS Direct Connect establishes a dedicated private network connection between on-premises infrastructure and AWS, bypassing the public internet and providing consistent, predictable latency and higher throughput.

---

**Q27. Correct: D**

AWS CloudFormation lets you define infrastructure as code using JSON or YAML templates, and it manages the creation, update, and deletion of all specified resources as a single stack.

---

**Q28. Correct: B**

Amazon EFS is a fully managed, POSIX-compliant elastic file system that can be mounted concurrently by multiple EC2 instances and automatically scales storage capacity up or down as files are added or removed.

---

**Q29. Correct: D**

Amazon CloudFront is a content delivery network (CDN) that caches content at edge locations around the world, reducing latency for end users and offloading requests from the origin S3 bucket.

---

**Q30. Correct: B**

Amazon Aurora is AWS's cloud-native relational database engine, compatible with MySQL and PostgreSQL, offering up to 5x the throughput of standard MySQL and a storage layer that automatically replicates 6 copies of data across 3 Availability Zones.

---

**Q31. Correct: A**

AWS designs every Region to contain a minimum of 3 Availability Zones, each consisting of one or more discrete data centers with independent power, cooling, and networking, enabling high availability architectures.

---

**Q32. Correct: D**

AWS Direct Connect establishes a dedicated, private physical network connection between on-premises infrastructure and AWS, bypassing the public internet entirely and providing consistent, predictable low-latency throughput.

---

**Q33. Correct: D**

Amazon ECS with the Fargate launch type is a serverless compute engine for containers, meaning AWS provisions and manages the underlying compute infrastructure and orchestration, so no EC2 instances need to be managed.

---

**Q34. Correct: C**

Latency-based routing uses continuously measured network latency data between users and AWS Regions to route requests to the Region that provides the fastest response time, which can differ from the user's geographic proximity.

---

**Q35. Correct: A**

Availability Zones are physically separate data centers within a Region that host full AWS compute, storage, and database services with high availability, while edge locations are smaller sites in the AWS global network used by CloudFront and Route 53 to cache and deliver content closer to end users.

---

**Q36. Correct: B**

Amazon EFS is a managed, elastic NFS file system that can be mounted concurrently by many EC2 instances across multiple Availability Zones, providing shared, simultaneous read/write access to the same files.

---

**Q37. Correct: D**

Amazon Aurora MySQL-Compatible Edition is wire-compatible with MySQL, delivers up to five times the throughput of standard MySQL, and uses a distributed, auto-scaling storage layer that grows automatically up to 128 TB.

---

**Q38. Correct: C**

Amazon EFS is a fully managed, elastic NFS file system that supports concurrent POSIX-compliant access from thousands of Linux instances simultaneously, and it scales storage automatically with no capacity planning required.

---

**Q39. Correct: D**

AWS Direct Connect provides a dedicated, private network connection from on-premises infrastructure to AWS, delivering consistent, predictable latency and bandwidth that is not shared with public internet traffic — ideal for large, regular data transfers.

---

**Q40. Correct: C**

Amazon Redshift is a fully managed, petabyte-scale data warehouse that uses columnar storage and massively parallel processing, purpose-built for complex analytical queries and BI tool integration over very large datasets.

---

**Q41. Correct: A**

Compute Savings Plans automatically apply the discounted rate to usage across any instance family, size, OS, tenancy, and even AWS Region, with no need to exchange or modify anything — ideal for workloads whose instance configuration may change over 3 years while still committing to steady usage.

---

**Q42. Correct: B**

The Cost and Usage Report is the most comprehensive and granular billing dataset AWS offers — it can include hourly line items, resource IDs, and cost allocation tags, and can be delivered automatically to an S3 bucket in CSV or Parquet format for downstream BI tools.

---

**Q43. Correct: A**

AWS Organizations enables RI (and Savings Plans) discount sharing by default across all linked accounts. The billing system automatically applies unused RI discounts to matching instance usage anywhere in the organization, on a first-come, first-served basis, unless discount sharing is explicitly turned off.

---

**Q44. Correct: C**

Only the Enterprise Support Plan includes a dedicated Technical Account Manager (TAM), proactive Infrastructure Event Management, and a guaranteed less-than-15-minute response time for business-critical system-down cases.

---

**Q45. Correct: A**

Basic and Developer support plans only surface a limited subset of Trusted Advisor checks (core security checks and service quota checks) at no cost. Business and Enterprise plans unlock the complete set of checks across all five categories: cost optimization, performance, security, fault tolerance, and service limits.

---

