## Chapter 9 Cheat Sheet: Networking & AI/ML Awareness

### VPC Core Components
| Component | Purpose |
|---|---|
| Subnet | Segment of VPC IP range in one AZ; public or private |
| Route Table | Determines where subnet traffic is directed |
| Internet Gateway (IGW) | Enables public subnet ↔ internet traffic (two-way) |
| NAT Gateway | Enables private subnet → internet outbound-only traffic |

**Public subnet = route table has route to IGW.** No IGW route = private subnet.

### Security Groups vs Network ACLs
| Feature | Security Group | Network ACL |
|---|---|---|
| Level | Instance (ENI) | Subnet |
| State | Stateful (auto-allows return traffic) | Stateless (must allow both directions) |
| Rules | Allow only | Allow AND Deny |
| Evaluation | All rules evaluated | Rule number order, lowest first |

**Exam trap:** Forgetting NACL needs an outbound rule for ephemeral ports (1024–65535) to allow return traffic.

### Elastic Load Balancing Types
| Type | OSI Layer | Protocol | Use Case |
|---|---|---|---|
| ALB | Layer 7 | HTTP/HTTPS | Content-based routing, microservices |
| NLB | Layer 4 | TCP/UDP | Ultra-low latency, static IP, high throughput |
| CLB | Layer 4/7 (legacy) | Basic | Legacy apps only — not recommended for new builds |

### Amazon Route 53
- Managed DNS + domain registration + health checks.
- Routing policies: **Simple, Weighted, Latency-based, Failover, Geolocation, Geoproximity, Multivalue answer.**
- Exam tip: Latency = speed; Geolocation = compliance/region restriction; Failover = DR.

### Amazon API Gateway
- Fully managed service to create, publish, secure, monitor REST/WebSocket APIs.
- Common pairing: API Gateway + Lambda = serverless API backend.

### SageMaker vs Bedrock
| Service | Purpose | Model Type |
|---|---|---|
| SageMaker | Build/train/deploy custom ML models | Your own trained models |
| Bedrock | Access to foundation models via API | Pre-trained FMs (Anthropic, Meta, Amazon Titan/Nova, etc.) |

**Exam tip:** "Custom model + your data" → SageMaker. "Quick generative AI, no infra" → Bedrock.

### Quick Decision Rules
- Block a specific IP → NACL (deny rule), not Security Group.
- Need static IP for load balancer → NLB.
- Need path/host-based routing → ALB.
- Need DR / regional performance routing for DNS → Route 53 (Failover / Latency).
