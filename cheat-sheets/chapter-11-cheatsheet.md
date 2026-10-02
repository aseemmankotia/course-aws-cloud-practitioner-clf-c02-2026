## Chapter 11 Cheat Sheet: Billing, Pricing & Support

### Cost Management Tools
| Tool | Purpose | Key Detail |
|---|---|---|
| Cost Explorer | Visualize & forecast spend | Up to 12 months history + 12 months forecast; graphs, not raw exports |
| AWS Budgets | Set thresholds & get alerts | Types: Cost, Usage, RI utilization/coverage, Savings Plans; alerts on actual OR forecasted spend |
| Cost and Usage Report (CUR) | Most granular billing data | Hourly/daily/monthly line items delivered to S3; feeds BI tools |
| Trusted Advisor | Best-practice recommendations | 5 categories: Cost Optimization, Performance, Security, Fault Tolerance, Service Limits |

**Exam trap:** Cost Explorer = *analyze/forecast*; Budgets = *alert*; CUR = *raw detailed data export*. Don't confuse them.

### AWS Support Plan Comparison
| Plan | Cost | Response Time (worst-case) | TAM |
|---|---|---|---|
| Basic | Free | No technical support cases | None |
| Developer | From $29/mo | System impaired: <12 business hrs | None |
| Business | From $100/mo (or % of usage) | Production down: <1 hr; 24/7 phone/chat/email | None |
| Enterprise On-Ramp | % of usage | Business-critical down: <30 min | Pool of TAMs |
| Enterprise | % of usage | Business-critical down: <15 min | Dedicated TAM |

**Exam trap:** Only Business, Enterprise On-Ramp, and Enterprise get FULL Trusted Advisor checks (all 5 categories). Basic/Developer get only 7 core checks (mostly security + service limits).

### Support & Info Resources
| Resource | What it does |
|---|---|
| AWS Health Dashboard (Personal) | Account-specific service events/impacts |
| Service Health Dashboard | Public, general AWS service status |
| AWS re:Post | Free community Q&A (replaced AWS Forums) |
| Knowledge Center | FAQ-style articles for common issues |

### Quick Response Time Table (by case severity)
| Severity | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |
|---|---|---|---|---|---|
| General guidance | — | <24h | <24h | <24h | <24h |
| System impaired | — | <12h | <12h | <12h | <12h |
| Production impaired | — | — | <4h | <4h | <4h |
| Production down | — | — | <1h | <1h | <1h |
| Business-critical down | — | — | — | <30min | <15min |

**Memory trick:** "Basic = billing only, Developer = business hours, Business = 24/7 & 1-hour, Enterprise = minutes & TAM."

### Common Exam Traps
1. Assuming Cost Explorer can send alerts — it can't; that's Budgets.
2. Choosing Enterprise when Business already meets the SLA requirement (over-provisioning cost).
3. Confusing Enterprise On-Ramp's *pooled* TAMs with Enterprise's *dedicated* TAM.
4. Forgetting cost allocation tags must be manually activated before appearing in CUR/Cost Explorer.
