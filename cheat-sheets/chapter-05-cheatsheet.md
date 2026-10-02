## Chapter 5 Cheat Sheet: Security & Compliance Services

### Compliance Documentation
| Service | Purpose | Cost |
|---|---|---|
| **AWS Artifact** | On-demand compliance reports (SOC 1/2/3, PCI DSS, ISO) + agreements (HIPAA BAA, NDA) | Free |

**Artifact Reports** = download audit docs. **Artifact Agreements** = accept legal agreements (e.g., BAA before storing PHI).

### Compliance Programs (know the scope)
| Program | Covers |
|---|---|
| HIPAA | US healthcare data (PHI) |
| PCI-DSS | Payment card data |
| GDPR | EU personal data / privacy |

### DDoS & Web Traffic Protection
| Service | Layer | Protects Against | Cost |
|---|---|---|---|
| **Shield Standard** | 3/4 (network/transport) | Common volumetric DDoS | Free, automatic |
| **Shield Advanced** | 3/4 | Advanced DDoS + cost protection + 24/7 DRT | ~$3,000/mo, 1-yr commit |
| **AWS WAF** | 7 (application) | SQL injection, XSS, bad bots, rate limiting | Pay per web ACL/rule/request |

**Exam rule:** Shield = network floods. WAF = malicious HTTP content. Use both together for layered defense. WAF attaches to CloudFront, ALB, API Gateway, AppSync — NOT to raw EC2 or NLB.

### Threat & Vulnerability Services — "GIM" Memory Trick
| Service | Detects | Scope | Data Source |
|---|---|---|---|
| **GuardDuty** | Threats/anomalous behavior | Account-wide | CloudTrail, VPC Flow Logs, DNS logs |
| **Inspector** | Vulnerabilities (CVEs), network exposure | EC2, ECR images, Lambda | Automated agentless/agent-based scans |
| **Macie** | Sensitive data (PII) | Amazon S3 only | ML + pattern matching |

**Exam trap:** These three are NEVER interchangeable. GuardDuty ≠ vulnerability scanner. Inspector ≠ data classifier. Macie ≠ threat detector.

### Quick Decision Guide
- "Need proof of AWS compliance for auditors" → **Artifact**
- "Detect malicious API calls / compromised credentials" → **GuardDuty**
- "Find unpatched CVEs on EC2/containers" → **Inspector**
- "Find PII in S3 buckets" → **Macie**
- "Block DDoS flood" → **Shield** (Standard=free, Advanced=paid+DRT)
- "Block SQL injection/XSS on web app" → **WAF**
- "Need HIPAA BAA before storing PHI" → **Artifact Agreements**

### Common Exam Traps
1. Choosing GuardDuty when the scenario is really about *scanning EC2 for vulnerabilities* (should be Inspector).
2. Choosing WAF when the attack described is a network-layer flood (should be Shield).
3. Forgetting Shield Standard is automatic and free for ALL AWS customers — no action needed to enable basic protection.
4. Assuming Macie scans EC2 or RDS — it only scans **S3**.
