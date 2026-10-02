## Chapter 9: Cloud Technology and Services: Networking and AI/ML Awareness — Practice Questions

**Q1.** A company's web application in a VPC public subnet is receiving unexpected traffic from a single malicious IP address. The security team wants to explicitly block that IP at the subnet level, even though individual EC2 instances use security groups that only allow specific ports. Which service should they configure to add an explicit DENY rule for this IP?

A) Security Groups, because they can create deny rules for specific IPs
B) Route 53 health checks, because they can block malicious traffic sources
C) AWS API Gateway resource policies, because they filter traffic by IP
D) Network ACLs, because they support explicit allow and deny rules evaluated in order

<details>
<summary>Answer</summary>

**Correct: D**

Network ACLs operate at the subnet level and support both allow and deny rules, evaluated in numerical order, making them the correct tool for explicitly blocking a specific IP address.

**Why the others are wrong:**
- Security groups only support allow rules — there is no way to explicitly deny traffic with a security group.
- Route 53 handles DNS resolution and health checks for endpoints, not traffic filtering at the network layer.
- API Gateway resource policies control access to API endpoints, not general subnet-level network traffic.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company needs a load balancer for a gaming application that uses a custom TCP protocol on non-standard ports and requires extremely low latency with a static IP address. Which ELB type BEST meets these requirements?

A) Application Load Balancer (ALB)
B) Classic Load Balancer (CLB)
C) Network Load Balancer (NLB)
D) Gateway Load Balancer (GWLB) configured for HTTP

<details>
<summary>Answer</summary>

**Correct: C**

Network Load Balancer operates at Layer 4, handles TCP/UDP traffic on any port, supports static IP addresses, and is designed for ultra-low latency, high-throughput workloads.

**Why the others are wrong:**
- ALB operates at Layer 7 and is designed for HTTP/HTTPS traffic with content-based routing, not raw TCP performance.
- CLB is a legacy load balancer with limited features and is not recommended by AWS for new workloads.
- Gateway Load Balancer is used for deploying third-party virtual network appliances, not general application traffic, and doesn't apply here.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company wants to route users to the closest regional deployment of their application based on the geographic location of the user's DNS query, to minimize latency. Which Amazon Route 53 routing policy should they use?

A) Latency-based routing policy
B) Weighted routing policy
C) Failover routing policy
D) Simple routing policy

<details>
<summary>Answer</summary>

**Correct: A**

Latency-based routing directs users to the AWS Region that provides the lowest network latency, which is the most relevant policy for minimizing response time based on user location.

**Why the others are wrong:**
- Weighted routing distributes traffic based on assigned proportions, not latency or location.
- Failover routing is used for active-passive disaster recovery configurations, not general latency optimization.
- Simple routing does not support multiple values with health-based or performance-based logic.

</details>

---

**Q4.** A retail company wants to add a generative AI chatbot to their website quickly using a pre-trained foundation model, without provisioning or managing any ML infrastructure or training custom models. Which AWS service should they use?

A) Amazon Bedrock
B) Amazon SageMaker
C) Amazon Rekognition
D) Amazon EC2 with a custom AMI

<details>
<summary>Answer</summary>

**Correct: A**

Amazon Bedrock provides serverless access to pre-trained foundation models from multiple providers through a single API, requiring no infrastructure management, which fits a quick generative AI use case.

**Why the others are wrong:**
- SageMaker is designed for building, training, and deploying custom ML models — it requires more setup and is used when custom model development is needed.
- Rekognition is a computer vision service for image and video analysis, not generative text-based chatbots.
- EC2 with a custom AMI would require significant infrastructure management, which the requirement explicitly avoids.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A data science team needs to build, train, and fine-tune a custom fraud-detection ML model using their own historical transaction data, with full control over algorithms and hyperparameters. Which AWS service is BEST suited for this?

A) Amazon Bedrock
B) Amazon SageMaker
C) Amazon Comprehend
D) Amazon API Gateway

<details>
<summary>Answer</summary>

**Correct: B**

Amazon SageMaker is a fully managed service purpose-built for the entire ML lifecycle, including building, training, and tuning custom models with an organization's own data.

**Why the others are wrong:**
- Bedrock provides access to pre-trained foundation models and is not designed for training custom models from scratch on proprietary data.
- Comprehend is a pre-built NLP service for text analysis, not a platform for training custom fraud-detection models.
- API Gateway is used to expose and manage APIs, not to build or train machine learning models.

</details>

---

**Q6.** A company is designing a VPC and wants EC2 instances in a subnet to be reachable from the internet. Which combination of configurations is REQUIRED to make the subnet public?

A) Attach a NAT Gateway to the subnet and assign public IPs to instances
B) Configure a Network ACL to allow all inbound and outbound traffic
C) Attach an Internet Gateway to the VPC and add a route in the subnet's route table pointing to the Internet Gateway
D) Place the subnet in a Route 53 hosted zone

<details>
<summary>Answer</summary>

**Correct: C**

A subnet is considered public when its route table has a route to an Internet Gateway attached to the VPC, allowing traffic to flow to and from the internet.

**Why the others are wrong:**
- A NAT Gateway allows private subnet instances to initiate outbound internet traffic but does not make a subnet publicly reachable from the internet.
- NACL rules control traffic filtering but do not determine whether a subnet has internet routing; the route table configuration does.
- Route 53 hosted zones manage DNS records and have no relationship to VPC subnet routing.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A student configuring a Network ACL sets an inbound rule to allow HTTP traffic on port 80 but notices that responses from the web server are being blocked. What is the MOST likely cause?

A) The security group is blocking outbound traffic
B) The Internet Gateway is not attached to the VPC
C) The NACL is missing an outbound rule allowing the ephemeral port range for return traffic
D) Route 53 has not been configured with a health check

<details>
<summary>Answer</summary>

**Correct: C**

Because NACLs are stateless, return traffic must be explicitly allowed via a separate outbound rule, typically covering the ephemeral port range (1024-65535), unlike stateful security groups.

**Why the others are wrong:**
- Security groups are stateful, so if inbound traffic is allowed, the corresponding outbound response is automatically allowed — this wouldn't cause the issue described.
- If the Internet Gateway were missing, no traffic would reach the instance at all, not just responses.
- Route 53 health checks are unrelated to traffic being blocked at the network ACL level.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement correctly describes the fundamental difference between Security Groups and Network ACLs in Amazon VPC?

A) Security Groups operate at the subnet level while NACLs operate at the instance level
B) Security Groups are stateless and require explicit rules for both directions, while NACLs are stateful
C) Security Groups are stateful and only support allow rules, while NACLs are stateless and support both allow and deny rules
D) Security Groups and NACLs are functionally identical and interchangeable

<details>
<summary>Answer</summary>

**Correct: C**

Security groups are stateful (return traffic is automatically allowed) and only support allow rules; NACLs are stateless (requiring rules for both directions) and support both allow and deny rules.

**Why the others are wrong:**
- This reverses the actual scope — security groups operate at the instance (ENI) level, while NACLs operate at the subnet level.
- This reverses statefulness — security groups are stateful, not NACLs.
- They are not interchangeable; they serve different layers of defense and have distinct rule capabilities.

</details>

---

