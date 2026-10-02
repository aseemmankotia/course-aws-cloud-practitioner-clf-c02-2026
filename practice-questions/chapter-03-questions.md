## Chapter 3: Security and Compliance: The Shared Responsibility Model — Practice Questions

**Q1.** A company runs a fleet of Amazon EC2 instances hosting a custom Java application. Six months after launch, an auditor finds the guest operating system is missing critical security patches. Who is responsible for this gap?

A) The customer, because guest OS patching is a customer responsibility for EC2
B) AWS, because it owns all infrastructure supporting EC2
C) AWS, because EC2 is a managed service
D) Neither party, since AWS Config would have patched it automatically

<details>
<summary>Answer</summary>

**Correct: A**

EC2 is IaaS — AWS manages the physical host and hypervisor, but the customer owns everything above the hypervisor, including guest OS patching.

**Why the others are wrong:**
- AWS only secures the infrastructure OF the cloud (hardware, hypervisor, physical security), not the guest OS running inside an instance.
- EC2 is not a fully managed service like RDS or Lambda — it is unmanaged compute, so OS-level maintenance falls to the customer.
- AWS Config only audits and reports configuration compliance; it does not automatically patch systems.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company migrates its database from self-managed MySQL on EC2 to Amazon RDS for MySQL. Which task moves from the customer's responsibility to AWS's responsibility as a result of this migration?

A) Configuring the database's IAM authentication policies
B) Patching the underlying operating system and database engine
C) Managing security group rules for the database
D) Encrypting sensitive data before it is written to the database

<details>
<summary>Answer</summary>

**Correct: B**

RDS is a managed service — AWS handles OS patching and database engine patching (within the customer's chosen maintenance window), whereas on EC2 the customer would patch both manually.

**Why the others are wrong:**
- IAM policy configuration remains a customer responsibility regardless of whether the database is self-managed or on RDS.
- Network access control via security groups is always configured by the customer, on both EC2 and RDS.
- Data encryption choices and key management remain the customer's responsibility even with RDS.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A developer deploys business logic using AWS Lambda triggered by API Gateway. Under the shared responsibility model, what is the developer still responsible for?

A) Writing secure function code and configuring least-privilege IAM permissions for the function
B) Patching the operating system that runs the Lambda execution environment
C) Provisioning and maintaining the underlying compute servers
D) Managing the physical hardware hosting the Lambda service

<details>
<summary>Answer</summary>

**Correct: A**

With Lambda (serverless), AWS manages the entire infrastructure stack including OS and runtime patching. The customer's responsibility narrows to their function code, dependencies, and IAM configuration.

**Why the others are wrong:**
- AWS fully manages OS patching for the Lambda execution environment — this is a defining benefit of serverless.
- AWS provisions and maintains all underlying servers for Lambda; the customer never manages servers.
- Physical hardware is always AWS's responsibility across every compute service, not just Lambda.

</details>

---

**Q4.** A company needs a compute service where AWS is fully responsible for both guest OS patching and runtime patching, requiring zero server management from the customer.

A) AWS Lambda
B) Amazon EC2
C) Amazon EC2 with Auto Scaling
D) Amazon RDS

<details>
<summary>Answer</summary>

**Correct: A**

Lambda is serverless — AWS owns the entire OS and runtime layer, leaving the customer responsible only for code and configuration.

**Why the others are wrong:**
- EC2 requires the customer to patch the guest OS themselves.
- Auto Scaling only manages instance count; the customer still must patch the guest OS on each EC2 instance.
- RDS shifts OS/engine patching to AWS but is a database service, not general-purpose compute, and still requires customer-managed network/IAM settings.

</details>

---

**Q5.** A company stores sensitive customer records in Amazon S3 and must ensure the data is encrypted at rest using AWS Key Management Service (KMS). Who is responsible for enabling this encryption?

A) AWS automatically encrypts all data at rest with KMS by default, with no customer action required
B) AWS Support enables encryption upon customer request via a support ticket
C) Encryption at rest is not available for S3 and must be handled at the application layer
D) The customer must configure and enable server-side encryption with KMS on the bucket or objects

<details>
<summary>Answer</summary>

**Correct: D**

While S3 encrypts new objects by default using SSE-S3, using SSE-KMS with customer-managed keys requires the customer to explicitly configure the bucket policy or object settings.

**Why the others are wrong:**
- Default S3 encryption uses SSE-S3, not SSE-KMS; customer-managed KMS keys must be explicitly configured.
- AWS Support does not configure encryption settings on behalf of customers as part of standard operations.
- S3 does support at-rest encryption natively; it does not need to be built into the application layer.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which action is the customer's responsibility when protecting data in transit between an application and an AWS service?

A) AWS automatically encrypts all traffic across the public internet with no configuration needed
B) AWS Trusted Advisor enforces TLS on all customer traffic automatically
C) The customer must configure the application to use HTTPS/TLS endpoints
D) Data in transit is only relevant for on-premises networks, not AWS

<details>
<summary>Answer</summary>

**Correct: C**

Encryption in transit is a customer responsibility — the customer must configure applications and clients to use TLS/HTTPS endpoints when communicating with AWS services.

**Why the others are wrong:**
- AWS provides TLS endpoints but does not force all customer application traffic to use them automatically.
- Trusted Advisor provides recommendations and checks; it does not enforce encryption configurations.
- Data in transit protection is equally relevant for traffic within AWS and between AWS and on-premises systems.

</details>

---

**Q7.** A startup wants to minimize its security operations workload by choosing services where AWS assumes the most infrastructure responsibility, while still requiring the customer to manage IAM policies and data protection settings.

A) Self-managed database on EC2
B) On-premises data center with a VPN to AWS
C) Amazon RDS or AWS Lambda
D) Amazon EC2 with manually configured security groups only

<details>
<summary>Answer</summary>

**Correct: C**

Managed services like RDS and serverless services like Lambda shift infrastructure maintenance (OS/engine patching) to AWS, reducing customer operational burden while customer still configures IAM and data protection.

**Why the others are wrong:**
- Running a database on EC2 requires the customer to patch both OS and database engine, increasing operational burden.
- An on-premises data center places all infrastructure responsibility on the customer, the opposite of the goal.
- Plain EC2 still requires guest OS management from the customer, unlike managed or serverless services.

</details>

---

**Q8.** What does the phrase 'security OF the cloud' refer to in the AWS shared responsibility model?

A) The customer's responsibility to secure their applications and data
B) A joint effort between AWS and the customer for all layers of security
C) AWS's responsibility to protect the physical infrastructure that runs all AWS services
D) The compliance certifications AWS obtains for its own internal software teams

<details>
<summary>Answer</summary>

**Correct: C**

‘Security OF the cloud’ specifically refers to AWS protecting the infrastructure — hardware, software, networking, and facilities — that runs AWS Cloud services.

**Why the others are wrong:**
- Protecting applications and data is described as 'security IN the cloud,' which is the customer's responsibility.
- The model splits responsibility by boundary — it is not a fully joint effort at every layer.
- Compliance certifications support the 'security of the cloud' concept but the phrase itself refers to infrastructure protection, not certification scope.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

