## Chapter 11: Billing, Pricing, and Support: Cost Management Tools and Support Plans — Practice Questions

**Q1.** A retail company wants to be automatically notified via email whenever their forecasted monthly AWS spend is projected to exceed $10,000, even before the month ends. Which service should they configure?

A) AWS Cost Explorer
B) AWS Cost and Usage Report
C) AWS Budgets
D) AWS Trusted Advisor

<details>
<summary>Answer</summary>

**Correct: C**

AWS Budgets lets you set cost thresholds and sends alerts based on actual OR forecasted spend via SNS/email before the threshold is hit.

**Why the others are wrong:**
- Cost Explorer visualizes and forecasts spend but does not send proactive alerts.
- Cost and Usage Report provides raw detailed billing data for analysis, not real-time alerting.
- Trusted Advisor flags cost optimization opportunities (e.g., idle resources) but doesn't monitor budget thresholds.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company's production website goes down and they need a guaranteed response time of under 1 hour from AWS Support, but the workload is not classified as business-critical. What is the MINIMUM AWS Support plan that meets this requirement?

A) Developer
B) Enterprise On-Ramp
C) Enterprise
D) Business

<details>
<summary>Answer</summary>

**Correct: D**

Business Support guarantees under 1 hour response time for 'production system down' cases, which is the minimum tier offering this SLA.

**Why the others are wrong:**
- Developer Support only guarantees under 12 business hours for system impaired issues — no 1-hour SLA exists.
- Enterprise On-Ramp meets the requirement but is more than the minimum needed; it adds business-critical (<30 min) SLA not required here.
- Enterprise Support also exceeds the requirement and costs significantly more; it's needed only for business-critical (<15 min) SLAs.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A finance team needs the most granular, line-item-level billing data — broken down hourly by resource, tag, and usage type — to feed into a third-party BI tool for chargeback reporting. Which AWS tool should they use?

A) AWS Cost Explorer
B) AWS Budgets
C) AWS Trusted Advisor
D) AWS Cost and Usage Report

<details>
<summary>Answer</summary>

**Correct: D**

AWS Cost and Usage Report (CUR) provides the most comprehensive and granular billing dataset, delivered to S3, with hourly/daily/monthly line items suitable for external BI ingestion.

**Why the others are wrong:**
- Cost Explorer is a visualization and forecasting tool with limited granularity, not raw exportable line-item data.
- Budgets only tracks spend against thresholds and sends alerts; it does not provide detailed usage data.
- Trusted Advisor provides recommendations, not billing/usage line-item data.

</details>

---

**Q4.** Which AWS tool provides automated recommendations across cost optimization, performance, security, fault tolerance, and service limits?

A) AWS Trusted Advisor
B) AWS Cost Explorer
C) AWS Health Dashboard
D) AWS Budgets

<details>
<summary>Answer</summary>

**Correct: A**

Trusted Advisor evaluates your account against five check categories (cost optimization, performance, security, fault tolerance, service limits) and gives actionable recommendations.

**Why the others are wrong:**
- Cost Explorer only addresses cost visualization and forecasting.
- Health Dashboard reports on service and account-specific operational issues/events, not best-practice recommendations.
- Budgets only manages spend thresholds and alerts.

</details>

---

**Q5.** Which is the MINIMUM AWS Support plan required to receive a single, designated Technical Account Manager (TAM) for an account?

A) Business
B) Enterprise On-Ramp
C) Enterprise
D) Developer

<details>
<summary>Answer</summary>

**Correct: C**

Enterprise Support is the only plan that includes a designated (named) TAM assigned specifically to the account.

**Why the others are wrong:**
- Business Support does not include a TAM at all.
- Enterprise On-Ramp provides access to a pool of TAMs, not a single designated TAM.
- Developer Support has no TAM access.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** You want AWS Budgets to send an alert when your ACTUAL spend crosses 80% of a defined monthly limit. Which budget type should you configure?

A) Usage budget
B) Cost budget
C) Savings Plans budget
D) RI utilization budget

<details>
<summary>Answer</summary>

**Correct: B**

A Cost budget tracks actual (or forecasted) spend against a defined dollar threshold and triggers alerts at set percentages.

**Why the others are wrong:**
- Usage budgets track service usage amounts (e.g., hours, GB), not dollar spend.
- Savings Plans budgets track utilization/coverage of Savings Plans commitments, not general spend.
- RI utilization budgets track how effectively Reserved Instances are used, not overall cost.

</details>

---

**Q7.** How far into the future can AWS Cost Explorer forecast your AWS spend by default?

A) 3 months
B) 6 months
C) 12 months
D) 24 months

<details>
<summary>Answer</summary>

**Correct: C**

AWS Cost Explorer can forecast spend up to 12 months into the future based on historical usage patterns.

**Why the others are wrong:**
- 3 months is too short — well under the actual supported forecast window.
- 6 months is also below the actual maximum forecast range.
- 24 months exceeds the documented forecast limit of Cost Explorer.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A Cloud Practitioner wants to check whether any AWS service events are actively impacting the specific resources in their own account, rather than viewing general AWS infrastructure status. Which tool should they use?

A) AWS Service Health Dashboard
B) AWS re:Post
C) AWS Health Dashboard (Personal Health Dashboard)
D) AWS Trusted Advisor

<details>
<summary>Answer</summary>

**Correct: C**

The Personal Health Dashboard (part of AWS Health Dashboard) shows account-specific events and how they affect your resources.

**Why the others are wrong:**
- The Service Health Dashboard shows the general public status of AWS services, not personalized account impact.
- re:Post is a community Q&A forum, unrelated to real-time account health events.
- Trusted Advisor gives best-practice recommendations, not real-time service event impact.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

