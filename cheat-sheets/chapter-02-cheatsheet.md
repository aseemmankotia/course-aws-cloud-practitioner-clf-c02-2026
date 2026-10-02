# Chapter 2 Cheat Sheet: Cloud Economics & Well-Architected Framework

## CapEx vs OpEx
| Model | Description | Example |
|---|---|---|
| CapEx (Fixed) | Large upfront investment, paid regardless of usage | Buying servers, building a data center |
| OpEx (Variable) | Pay-as-you-go, scales with actual usage | AWS On-Demand compute/storage billing |

**Exam rule:** AWS converts CapEx into OpEx — no upfront hardware purchase required.

## Total Cost of Ownership (TCO)
Must include for on-premises comparison:
- Hardware purchase & refresh cycles
- Power & cooling
- Facility/real estate space
- IT staff & maintenance labor
- Networking equipment

**Exam trap:** Comparing only server purchase price to AWS hourly rate — ignores indirect costs, making TCO incomplete.

## Economies of Scale & Right-Sizing
- **Economies of scale:** AWS aggregates demand from millions of customers → lower per-unit cost → passed to customers via price cuts.
- **Right-sizing:** Match instance/storage size to actual workload needs. Tools: AWS Compute Optimizer, AWS Trusted Advisor.

## Managed vs Self-Managed
| Self-Managed (e.g., DB on EC2) | Managed Service (e.g., RDS) |
|---|---|
| You patch, back up, scale manually | AWS handles patching, backups, scaling |
| More operational overhead | Less operational overhead — focus on differentiation |

## The Six Pillars of AWS Well-Architected Framework
| Pillar | Focus |
|---|---|
| Operational Excellence | Run & monitor systems, automate, improve processes |
| Security | Protect data, systems, and assets |
| Reliability | Recover from failures, meet demand dynamically |
| Performance Efficiency | Use compute resources efficiently as demand changes |
| Cost Optimization | Avoid unnecessary costs, right-size resources |
| Sustainability | Minimize environmental impact (added Dec 2021) |

**Exam tip:** Sustainability is the newest pillar — commonly tested as an outlier answer choice.

## Design for Failure & Loose Coupling
- **Design for failure:** Assume components will fail; build redundancy across Availability Zones/Regions.
- **Loose coupling:** Decouple components so failure in one doesn't cascade. Achieved via:
  - Amazon SQS (queue-based decoupling)
  - Amazon SNS (pub/sub decoupling)
  - Load balancers to abstract backend instances

**Exam trap:** Choosing to scale up (vertical scaling) an instance instead of decoupling tightly-coupled components — doesn't fix architectural fragility.

## Key Tools
| Tool | Purpose |
|---|---|
| AWS Well-Architected Tool | Self-service review against the 6 pillars with improvement plan |
| AWS Trusted Advisor | Real-time best-practice checks: cost, security, performance, fault tolerance, limits |
| AWS Pricing Calculator | Estimate AWS costs, build TCO comparisons |
| AWS Cost Explorer | Visualize and analyze historical cost/usage trends |
