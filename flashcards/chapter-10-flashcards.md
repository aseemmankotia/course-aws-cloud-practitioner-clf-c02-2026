## Chapter 10: Billing, Pricing, and Support: Pricing Models and Account Structure — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Spot Instance interruption notice — how much warning time? | 2 minutes, delivered via EC2 instance metadata or EventBridge. Exam tip: Spot = up to 90% off On-Demand, but can be reclaimed anytime with only 2 minutes warning. |
| 2 | AWS Free Tier: EC2 t2.micro/t3.micro allowance | 750 hours/month free for 12 months from account creation. Exam tip: this is a 12-month offer, NOT always-free. |
| 3 | AWS Lambda Always Free tier limits | 1 million requests/month + 400,000 GB-seconds of compute/month — never expires. Exam tip: Lambda's free tier is 'Always Free', not the 12-month type. |
| 4 | Standard RI vs Convertible RI: max discount and flexibility | Standard RI: up to 72% off, NO changes to instance family/OS/tenancy. Convertible RI: up to 66% off, CAN exchange for different family/OS/tenancy during term. |
| 5 | Reserved Instances vs Savings Plans — key difference | RIs commit to a specific instance configuration in a region (capacity reservation available). Savings Plans commit to $/hour spend and apply flexibly across instance families and even Fargate/Lambda. |
| 6 | Reserved Instance term lengths and payment options | Terms: 1-year or 3-year. Payment options: All Upfront, Partial Upfront, No Upfront. Exam tip: longer term + more upfront payment = bigger discount. |
| 7 | EC2 Instance Savings Plans vs Compute Savings Plans — discount tradeoff | EC2 Instance SP: up to 72% off but locked to one instance family/region. Compute SP: up to 66% off but most flexible (any family, region, OS, tenancy, or compute service). |
| 8 | Best pricing model for fault-tolerant, interruptible, flexible-schedule workloads | Spot Instances. Use for batch processing, big data, CI/CD, and containerized/stateless workloads. Exam tip: never use Spot for workloads that can't tolerate sudden termination. |
| 9 | What does AWS Organizations consolidated billing combine? | Merges all linked/member account invoices into one bill under the management account, and aggregates usage to reach volume discount tiers (e.g., S3) faster. |
| 10 | AWS Organizations default account limit | 10 accounts by default (soft limit) — can be increased via a Service Quotas request. Exam tip: this is a default limit, not a hard cap. |
| 11 | On-Demand Instance pricing model | Pay per second (Linux) or per hour (some OS) with no upfront commitment. Best for unpredictable, short-term, or testing workloads. Exam tip: most expensive per-hour rate of all EC2 purchase options. |
| 12 | CLI command to list your Reserved Instances | `aws ec2 describe-reserved-instances` — returns purchased RIs, their state, term, and offering class (Standard/Convertible). Exam tip: know this exists conceptually, not memorize full syntax. |
