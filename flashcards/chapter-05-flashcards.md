## Chapter 5: Security and Compliance: Governance, Compliance, and Security Services — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | AWS Shield Advanced monthly cost and commitment? | $3,000/month per organization, 1-year subscription commitment. Exam tip: Shield Standard is free and automatic for all customers. |
| 2 | GuardDuty vs Inspector vs Macie — one-word purpose each? | GuardDuty = Threats (behavioral detection from logs). Inspector = Vulnerabilities (CVEs, network exposure). Macie = Data (PII discovery in S3). Memory trick: G-Threat, I-Issue, M-Mask(sensitive data). |
| 3 | AWS Shield vs AWS WAF — which OSI layer? | Shield = layer 3/4 (network/transport, DDoS floods). WAF = layer 7 (application, HTTP-based exploits like SQLi/XSS). Exam tip: they're complementary, often used together. |
| 4 | Where does WAF attach in an architecture? | CloudFront distributions, Application Load Balancer, API Gateway, and AppSync. Exam tip: WAF cannot be attached directly to EC2 instances or Network Load Balancers. |
| 5 | Is AWS Artifact a paid service? | No — AWS Artifact is free. It provides on-demand access to AWS compliance reports and agreements at no cost. |
| 6 | AWS Artifact Reports vs AWS Artifact Agreements — difference? | Reports = downloadable audit/compliance docs (SOC 1/2/3, PCI DSS, ISO). Agreements = legal documents to review/accept, e.g., HIPAA BAA, NDA. |
| 7 | What log sources does GuardDuty analyze? | CloudTrail management/data events, VPC Flow Logs, and DNS query logs — no agents required, fully managed ML-based detection. |
| 8 | What resource types does Amazon Inspector scan? | EC2 instances, container images in Amazon ECR, and AWS Lambda functions — for software vulnerabilities (CVEs) and network reachability issues. |
| 9 | What is Amazon Macie's scope of data scanning? | Amazon S3 only. It uses ML and pattern matching to find PII, credentials, and other sensitive data in S3 buckets and reports findings with severity levels. |
| 10 | Shield Standard vs Shield Advanced — key added benefits? | Standard: free, automatic, layer 3/4 protection for all customers. Advanced: paid, adds cost protection, advanced mitigation, near real-time visibility, and 24/7 DDoS Response Team (DRT) access. |
| 11 | Match compliance program to its primary domain: HIPAA, PCI-DSS, GDPR | HIPAA = US healthcare/PHI protection. PCI-DSS = payment card data security. GDPR = EU personal data protection/privacy rights. |
| 12 | Exam trap: 'Which service detects malicious S3 access AND classifies sensitive data?' | Trick question — no single service does both. GuardDuty detects malicious/anomalous S3 access behavior; Macie classifies sensitive data content. They are separate, complementary services. |
