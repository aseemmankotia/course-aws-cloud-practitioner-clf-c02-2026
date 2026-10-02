## Chapter 7 Cheat Sheet: Compute Services

### EC2 Purchasing Options
| Option | Best For | Notes |
|---|---|---|
| On-Demand | Short-term, unpredictable workloads | No commitment, highest per-hour cost |
| Reserved Instances | Steady, predictable, long-term (1 or 3 yr) | Deepest discount for committed usage |
| Savings Plans | Flexible compute usage across instance families | Commit to $/hr spend, not specific instance |
| Spot Instances | Fault-tolerant, interruptible workloads (batch, CI/CD) | Up to ~90% off; 2-min interruption notice |
| Dedicated Hosts/Instances | Compliance/licensing needing physical isolation | Most expensive, full/partial physical server control |

### AWS Lambda Key Limits
| Limit | Value |
|---|---|
| Max execution timeout | 15 minutes |
| Max memory | 10,240 MB |
| Ephemeral storage (/tmp) | 512 MB default, up to 10,240 MB |
| Billing model | Pay per invocation + duration (ms) |
| Trigger sources | S3, API Gateway, DynamoDB Streams, EventBridge, SQS, etc. |

**Exam Rule:** "No servers to manage, event-driven, short execution" → Lambda.

### Containers: ECS vs EKS vs Fargate
| Service | Type | Overhead | Best For |
|---|---|---|---|
| Amazon ECS | AWS-proprietary orchestrator | Lower | Simpler AWS-native container deployments |
| Amazon EKS | Managed Kubernetes | Higher | Kubernetes-native, portable, multi-cloud |
| AWS Fargate | Serverless compute engine | Lowest | No EC2 management; works with both ECS & EKS |

**Exam Rule:** "Need Kubernetes" → EKS. "Simplest AWS container option" → ECS. "No server management for containers" → Fargate.

### AWS Elastic Beanstalk (PaaS)
- Upload code → EB auto-provisions EC2, load balancer, Auto Scaling group, and monitoring.
- Underlying resources remain visible/accessible for manual tuning.
- Reduces operational overhead vs manually configuring EC2 + ELB + ASG separately.
- **Exam Rule:** "Fast deploy, don't want to manually configure infra, but want control if needed" → Elastic Beanstalk.

### Auto Scaling Groups (ASG)
- Core settings: **Min**, **Max**, **Desired** capacity.
- Failed health check → instance terminated & replaced automatically (self-healing).
- Scaling policy types: **Target Tracking**, **Step Scaling**, **Scheduled Scaling**.
- **Exam Rule:** ASG improves both availability (replaces unhealthy instances) and cost efficiency (scales down when demand drops).

### Operational Overhead Spectrum (High → Low)
EC2 (self-managed) → EKS → ECS → Elastic Beanstalk → Lambda/Fargate

**Exam Rule of Thumb:** More control = more operational overhead. More "serverless" = less control, less overhead.
