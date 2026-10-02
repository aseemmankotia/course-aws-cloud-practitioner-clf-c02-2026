## Chapter 5: Security and Compliance: Governance, Compliance, and Security Services — Practice Questions

**Q1.** A healthcare startup must give its auditors proof that AWS data centers meet HIPAA safeguards before signing a Business Associate Addendum. Which AWS service should they use to retrieve this documentation on demand?

A) AWS Artifact
B) AWS Config
C) AWS Trusted Advisor
D) AWS Audit Manager

<details>
<summary>Answer</summary>

**Correct: A**

AWS Artifact is the self-service portal for downloading AWS compliance reports (SOC, PCI DSS, ISO) and signing agreements like the HIPAA BAA (Business Associate Addendum).

**Why the others are wrong:**
- AWS Config tracks resource configuration compliance within your account, not AWS's own third-party audit reports.
- Trusted Advisor gives account-level best-practice checks, not compliance documentation.
- Audit Manager helps assess YOUR workload's compliance evidence, not download AWS's own certifications.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company wants continuous, automated detection of suspicious API calls and unusual network traffic across its AWS accounts without deploying any agents. Which service should they enable?

A) Amazon GuardDuty
B) Amazon Inspector
C) Amazon Macie
D) AWS Shield Advanced

<details>
<summary>Answer</summary>

**Correct: A**

GuardDuty is an intelligent, agentless threat detection service that continuously analyzes CloudTrail, VPC Flow Logs, and DNS logs using machine learning to find malicious activity.

**Why the others are wrong:**
- Inspector assesses vulnerabilities on EC2, ECR images, and Lambda — it does not monitor account-wide API/network threats.
- Macie focuses only on discovering sensitive data (PII) in S3, not threat detection.
- Shield Advanced protects against DDoS attacks, not general anomalous activity.

</details>

---

**Q3.** A public-facing web application behind an Application Load Balancer is being targeted with repeated SQL injection attempts. Which service should be configured to block these requests?

A) AWS Shield Standard
B) AWS WAF
C) Amazon GuardDuty
D) AWS Firewall Manager alone

<details>
<summary>Answer</summary>

**Correct: B**

AWS WAF filters HTTP/HTTPS (layer 7) traffic using rules that detect and block common web exploits like SQL injection and cross-site scripting.

**Why the others are wrong:**
- Shield Standard protects against network/transport layer (layer 3/4) DDoS attacks, not application-layer exploits like SQL injection.
- GuardDuty detects threats but does not actively block malicious HTTP requests in real time.
- Firewall Manager centrally manages WAF/Shield rules across accounts but is not itself the filtering engine — WAF is required.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which AWS service scans EC2 instances and container images for known software vulnerabilities (CVEs) and unintended network exposure?

A) Amazon Macie
B) AWS Artifact
C) Amazon GuardDuty
D) Amazon Inspector

<details>
<summary>Answer</summary>

**Correct: D**

Amazon Inspector automatically and continuously scans EC2 instances, container images in ECR, and Lambda functions for software vulnerabilities and network reachability issues.

**Why the others are wrong:**
- Macie discovers sensitive data (PII) in S3, not software vulnerabilities.
- Artifact provides compliance documentation, not vulnerability scanning.
- GuardDuty detects behavioral threats from logs, not CVE-based vulnerability scanning.

</details>

---

**Q5.** A company stores customer records in S3 and needs to automatically identify buckets containing unencrypted personally identifiable information (PII). Which service fits this requirement?

A) Amazon GuardDuty
B) Amazon Inspector
C) AWS Config
D) Amazon Macie

<details>
<summary>Answer</summary>

**Correct: D**

Amazon Macie uses machine learning and pattern matching to automatically discover, classify, and report on sensitive data such as PII stored in S3.

**Why the others are wrong:**
- GuardDuty detects threats and anomalous behavior, not data classification.
- Inspector scans for vulnerabilities on compute resources, not data sensitivity in S3.
- AWS Config tracks configuration compliance, not the content of stored data.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** An e-commerce company running behind an Elastic Load Balancer wants financial protection against DDoS-related scaling charges and 24/7 access to the AWS DDoS Response Team (DRT). Which option should they select?

A) AWS Shield Advanced
B) AWS Shield Standard
C) AWS WAF with rate-based rules
D) Amazon GuardDuty with DDoS findings enabled

<details>
<summary>Answer</summary>

**Correct: A**

AWS Shield Advanced is the paid tier that adds cost protection for DDoS-related scaling charges, advanced attack diagnostics, and 24/7 access to the DDoS Response Team (DRT).

**Why the others are wrong:**
- Shield Standard is free and automatic but offers no cost protection or DRT access.
- WAF rate-based rules help mitigate application-layer floods but provide no financial DDoS cost protection.
- GuardDuty does not offer DDoS cost protection or DRT access — it's a detection service, not a DDoS mitigation service.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A company needs to formally sign a Business Associate Addendum (BAA) with AWS before storing protected health information (PHI). Where do they complete this?

A) AWS Artifact Agreements
B) AWS Artifact Reports
C) AWS Organizations
D) AWS Config conformance packs

<details>
<summary>Answer</summary>

**Correct: A**

AWS Artifact Agreements is where customers review, accept, and manage agreements such as the HIPAA Business Associate Addendum (BAA) and NDAs.

**Why the others are wrong:**
- Artifact Reports provides downloadable compliance reports (SOC, PCI DSS) but not agreement signing.
- AWS Organizations manages multi-account structure, not compliance agreements.
- Config conformance packs check resource compliance rules, not legal agreements with AWS.

</details>

---

**Q8.** What is the key difference between AWS Shield and AWS WAF?

A) Shield filters HTTP request content; WAF blocks network-layer floods
B) Shield protects against DDoS at the network/transport layer; WAF filters malicious HTTP traffic at the application layer
C) Shield and WAF perform identical functions and are interchangeable
D) Shield only protects RDS; WAF only protects EC2

<details>
<summary>Answer</summary>

**Correct: B**

Shield defends against layer 3/4 DDoS attacks (volumetric/network floods), while WAF operates at layer 7, filtering HTTP/HTTPS requests for exploits like SQL injection and XSS.

**Why the others are wrong:**
- This reverses the actual roles of the two services.
- They serve different layers of the stack and are commonly used together, not interchangeably.
- Neither service is scoped to only RDS or only EC2 — both apply to internet-facing resources like CloudFront, ALB, and API Gateway.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

