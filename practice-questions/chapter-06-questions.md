## Chapter 6: Cloud Technology and Services: Global Infrastructure and Deployment Methods — Practice Questions

**Q1.** A financial services company must ensure that customer data never leaves the country due to local regulations. Which AWS concept directly addresses this requirement?

A) Using multiple Availability Zones
B) Deploying resources in a specific AWS Region
C) Enabling AWS CloudFront edge caching
D) Using AWS Direct Connect

<details>
<summary>Answer</summary>

**Correct: B**

AWS Regions are isolated geographic areas; choosing a Region located within the required country ensures data residency and does not replicate data outside it unless explicitly configured.

**Why the others are wrong:**
- Availability Zones are subdivisions within a Region, not a data residency control — they don't determine which country data resides in.
- CloudFront edge locations cache content globally at the network edge, which could actually cause data to be cached outside the country.
- Direct Connect is a private network connection to AWS, not a data residency or geographic control.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A media company wants to reduce latency for users streaming video content globally by caching content closer to end users. Which AWS service should they use?

A) AWS Direct Connect
B) AWS CloudFormation
C) AWS Site-to-Site VPN
D) Amazon CloudFront

<details>
<summary>Answer</summary>

**Correct: D**

Amazon CloudFront is AWS's content delivery network (CDN) that uses edge locations to cache content close to end users, reducing latency.

**Why the others are wrong:**
- Direct Connect provides a dedicated network link to AWS, not content caching or global distribution.
- CloudFormation is an Infrastructure as Code tool for provisioning resources, unrelated to content delivery.
- Site-to-Site VPN creates an encrypted tunnel between on-premises and AWS, not a caching or CDN solution.

</details>

---

**Q3.** A company needs a consistent, low-latency, high-bandwidth private connection between its data center and AWS that does not traverse the public internet. Which solution BEST meets this requirement?

A) AWS Site-to-Site VPN
B) Amazon CloudFront
C) Public internet with a NAT Gateway
D) AWS Direct Connect

<details>
<summary>Answer</summary>

**Correct: D**

AWS Direct Connect establishes a dedicated private network connection between on-premises infrastructure and AWS, bypassing the public internet and providing consistent, predictable low-latency, high-bandwidth performance.

**Why the others are wrong:**
- Site-to-Site VPN is encrypted but still travels over the public internet, so it cannot guarantee consistent bandwidth or latency.
- CloudFront is a content delivery network for caching, not a connectivity solution between a data center and AWS.
- Public internet with NAT Gateway does not provide a private, dedicated, or consistent-performance connection.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A DevOps team wants to define their entire AWS infrastructure in a text file so it can be version-controlled and deployed repeatedly in the same way. Which AWS service should they use?

A) AWS Management Console
B) AWS Direct Connect
C) AWS CloudFormation
D) AWS CLI

<details>
<summary>Answer</summary>

**Correct: C**

AWS CloudFormation allows infrastructure to be defined as code using JSON or YAML templates, enabling repeatable, version-controlled, automated deployments.

**Why the others are wrong:**
- The Management Console is a manual, GUI-based interface and does not support Infrastructure as Code by itself.
- Direct Connect is a networking connectivity service, unrelated to infrastructure provisioning.
- The AWS CLI can create resources via commands but does not provide declarative, version-controlled templates the way CloudFormation does.

</details>

---

**Q5.** A developer wants to programmatically integrate AWS service calls directly into a Python application's codebase. Which tool is the BEST fit?

A) AWS Management Console
B) AWS SDK
C) AWS CloudFormation
D) AWS Direct Connect

<details>
<summary>Answer</summary>

**Correct: B**

AWS SDKs (e.g., Boto3 for Python) provide language-specific libraries that let developers call AWS APIs directly within application code.

**Why the others are wrong:**
- The Management Console is a browser-based GUI, not something embedded into application code.
- CloudFormation provisions infrastructure via templates; it is not used for embedding calls in application logic.
- Direct Connect is a network connectivity service unrelated to application-level API integration.

</details>

---

**Q6.** A company wants to quickly connect its on-premises network to AWS using an encrypted tunnel over the existing internet connection, with minimal setup time and cost. Which option is BEST?

A) AWS Direct Connect
B) AWS Site-to-Site VPN
C) Amazon CloudFront
D) A new Availability Zone deployment

<details>
<summary>Answer</summary>

**Correct: B**

AWS Site-to-Site VPN creates an encrypted IPsec tunnel over the public internet, and can typically be provisioned within minutes to hours with no need for physical circuit installation.

**Why the others are wrong:**
- Direct Connect requires physical cross-connects and provisioning that can take weeks to months, making it unsuitable for a quick setup.
- CloudFront is a content delivery network and has no role in connecting a data center to AWS.
- Deploying to an Availability Zone does not establish network connectivity between on-premises and AWS at all.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which statement BEST describes an AWS Availability Zone?

A) A single data center shared across multiple AWS Regions
B) A physically separate, isolated data center (or group of data centers) within a Region, connected via low-latency links
C) A global point-of-presence used only for content caching
D) A logical partition within a single data center used for billing separation

<details>
<summary>Answer</summary>

**Correct: B**

An Availability Zone consists of one or more discrete data centers with redundant power, networking, and connectivity, physically separated from other AZs but connected via high-bandwidth, low-latency private links within the same Region.

**Why the others are wrong:**
- AZs belong to a single Region, not shared across multiple Regions.
- This describes an edge location used by CloudFront, not an Availability Zone.
- AZs are physically distinct facilities, not just logical/billing partitions within one data center.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A company runs a critical application and wants to protect it against the failure of an entire data center while keeping data within the same country. What is the BEST architecture approach?

A) Deploy the application across multiple Availability Zones within a single Region
B) Deploy the application across multiple Regions in different countries
C) Deploy the application using only CloudFront edge locations
D) Deploy the application in a single Availability Zone with automatic scaling

<details>
<summary>Answer</summary>

**Correct: A**

Deploying across multiple Availability Zones within one Region protects against a single data center failure while keeping all resources and data within the same country/Region, satisfying both resilience and residency needs.

**Why the others are wrong:**
- Deploying across multiple Regions in different countries would violate the requirement to keep data within the same country.
- CloudFront only caches static content at edge locations; it does not run application compute or provide data center-level failover.
- A single AZ with auto scaling still has a single point of failure at the data center level if that AZ goes down.

</details>

---

