## Chapter 10 Cheat Sheet: Pricing Models & Account Structure

### EC2 Purchasing Options
| Model | Commitment | Max Discount | Flexibility | Best For |
|---|---|---|---|---|
| On-Demand | None | 0% | Full | Unpredictable, short-term, testing |
| Standard RI | 1 or 3 yr | ~72% | None (fixed instance/family/region) | Steady, predictable, known config |
| Convertible RI | 1 or 3 yr | ~66% | Can exchange family/OS/tenancy | Steady but config may change |
| Spot | None | up to 90% | Can be reclaimed anytime (2-min notice) | Fault-tolerant, flexible workloads |
| EC2 Instance Savings Plan | 1 or 3 yr ($/hr commit) | ~72% | Flexible size/OS/tenancy, fixed family+region | Steady EC2 usage |
| Compute Savings Plan | 1 or 3 yr ($/hr commit) | ~66% | Any family/region/OS/tenancy + Fargate/Lambda | Mixed or evolving compute usage |

**Exam rule of thumb:** More flexibility = lower max discount. Standard RI > EC2 Instance SP > Convertible RI > Compute SP in terms of discount, inverse order for flexibility.

### Spot Instances
- Interruption notice: **2 minutes** (via metadata / EventBridge)
- Use for: batch jobs, CI/CD, big data, containers, stateless apps
- Never use for: databases, workloads that can't tolerate abrupt termination

### AWS Free Tier
| Type | Duration | Example |
|---|---|---|
| 12-Months Free | 12 months from account creation | EC2 t2.micro/t3.micro — 750 hrs/month |
| Always Free | No expiration | Lambda — 1M requests + 400,000 GB-seconds/month |
| Trials | Short fixed period | Varies by service |

### AWS Organizations & Consolidated Billing
- Single **management account** invites/creates **member accounts**
- **Consolidated billing**: one invoice for all accounts
- **Volume discount aggregation**: combined usage reaches pricing tiers faster (e.g., S3 storage tiers)
- RI and Savings Plan discounts can be **shared** across accounts in the org
- Default account limit: **10 accounts** (soft limit, increasable via Service Quotas)
- No extra cost to use AWS Organizations itself

### Common Exam Traps
- Confusing Standard RI (no exchange) with Convertible RI (can exchange)
- Assuming Spot has no interruption warning — it's always 2 minutes
- Thinking Free Tier is unlimited or permanent — most offers are 12-month, only some are Always Free
- Believing consolidated billing merges security/IAM permissions — it does NOT, billing only
- Choosing Reserved Instances for short-term/unpredictable workloads instead of On-Demand or Spot
