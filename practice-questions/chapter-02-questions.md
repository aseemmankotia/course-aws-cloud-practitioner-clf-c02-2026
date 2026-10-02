## Chapter 2: Cloud Concepts: Cloud Economics and the Well-Architected Framework — Practice Questions

**Q1.** A startup is deciding between building its own data center or using AWS. The founders want to avoid large upfront investments and pay only for what they consume as the business grows. Which cost model BEST describes what AWS enables?

A) Converting variable OpEx into fixed CapEx
B) Eliminating both CapEx and OpEx entirely
C) Requiring a 3-year upfront hardware commitment
D) Converting fixed CapEx into variable OpEx

<details>
<summary>Answer</summary>

**Correct: D**

AWS shifts spending from large upfront capital expenditure (servers, data centers) to variable, pay-as-you-go operational expenditure.

**Why the others are wrong:**
- This reverses the actual direction of the shift — AWS moves away from fixed CapEx, not toward it.
- AWS still has operational costs (OpEx); it doesn't eliminate spending, it changes its structure.
- AWS pricing models like On-Demand require no upfront commitment; only Reserved/Savings Plans involve optional commitments.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company is comparing the cost of running an on-premises server farm versus migrating to AWS. Which factor MUST be included to produce an accurate Total Cost of Ownership (TCO) comparison?

A) Only the purchase price of the on-premises servers
B) Hardware, power, cooling, facility space, and IT staff costs for on-premises
C) Only the AWS On-Demand hourly compute rate
D) The number of AWS Regions available worldwide

<details>
<summary>Answer</summary>

**Correct: B**

TCO comparisons must account for all direct and indirect on-premises costs — hardware, power, cooling, real estate, and staffing — not just the sticker price of servers.

**Why the others are wrong:**
- Purchase price alone ignores ongoing operational costs like power and staffing.
- Compute rate alone ignores on-premises comparison costs, making the comparison meaningless.
- Number of Regions is unrelated to cost comparison; it's an availability/latency consideration.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An application's order-processing component occasionally fails under heavy load, causing the entire checkout system to go down. Which architectural change BEST applies the 'design for failure' and loose coupling principles to fix this?

A) Increase the EC2 instance size of the order-processing component
B) Move both components into a single larger EC2 instance
C) Schedule the order-processing component to run only during off-peak hours
D) Insert an Amazon SQS queue between the checkout system and the order-processing component

<details>
<summary>Answer</summary>

**Correct: D**

Adding a queue decouples the checkout system from the order-processing component, so a failure or slowdown in one doesn't cascade to the other — this is the core of loose coupling and designing for failure.

**Why the others are wrong:**
- Bigger instances (vertical scaling) don't address the tight coupling causing cascading failure.
- Combining components into one instance increases coupling, the opposite of the desired fix.
- Scheduling doesn't solve the architectural fragility; failures can still occur off-peak.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which AWS service provides real-time recommendations across cost optimization, security, fault tolerance, and performance to help align a workload with the Well-Architected Framework?

A) AWS Budgets
B) AWS Cost Explorer
C) AWS Config
D) AWS Trusted Advisor

<details>
<summary>Answer</summary>

**Correct: D**

AWS Trusted Advisor inspects your environment and gives recommendations across cost optimization, security, fault tolerance, performance, and service limits — mapping closely to Well-Architected pillars.

**Why the others are wrong:**
- AWS Budgets only tracks and alerts on cost/usage thresholds, not broad best-practice checks.
- Cost Explorer visualizes and analyzes spending trends but doesn't provide multi-pillar recommendations.
- AWS Config tracks resource configuration changes and compliance, not general best-practice guidance.

</details>

---

**Q5.** A company wants a tool that guides architects through structured questions to evaluate a workload against best practices for reliability, security, and cost, and produces an improvement plan. Which AWS offering should they use?

A) AWS Organizations
B) AWS Well-Architected Tool
C) AWS Service Catalog
D) AWS Systems Manager

<details>
<summary>Answer</summary>

**Correct: B**

The AWS Well-Architected Tool lets architects review workloads against the six pillars via structured questionnaires and generates an improvement plan.

**Why the others are wrong:**
- AWS Organizations manages multi-account governance, not workload architecture reviews.
- Service Catalog manages approved product/service deployment catalogs for teams, not architecture assessments.
- Systems Manager handles operational tasks like patching and automation, not architecture review.

</details>

---

**Q6.** Which pillar of the AWS Well-Architected Framework focuses specifically on minimizing the environmental impact of running cloud workloads?

A) Sustainability
B) Operational Excellence
C) Performance Efficiency
D) Reliability

<details>
<summary>Answer</summary>

**Correct: A**

The Sustainability pillar, added in December 2021, focuses on minimizing environmental impacts, including energy consumption and efficiency.

**Why the others are wrong:**
- Operational Excellence focuses on running and monitoring systems and improving processes, not environmental impact.
- Performance Efficiency is about using computing resources efficiently to meet requirements, not environmental focus specifically.
- Reliability focuses on recovery from failures and meeting demand, unrelated to environmental impact.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A company notices its EC2 instances are consistently running at 8% CPU utilization. According to cost optimization best practices, what should they do?

A) Purchase a 3-year All Upfront Reserved Instance for the same instance size
B) Enable detailed monitoring and take no further action
C) Migrate the workload to a larger instance type for headroom
D) Right-size to a smaller instance type that matches actual usage

<details>
<summary>Answer</summary>

**Correct: D**

Right-sizing means matching instance size to actual workload demand; consistently low utilization indicates over-provisioning and wasted spend.

**Why the others are wrong:**
- Committing long-term to an oversized instance locks in wasted spend rather than fixing it.
- Monitoring alone doesn't reduce cost; action is needed on the identified waste.
- Increasing instance size would increase costs further despite low utilization, the opposite of right-sizing.

</details>

---

**Q8.** What is the primary benefit of economies of scale as it relates to AWS pricing?

A) AWS guarantees fixed pricing for the lifetime of an account
B) Economies of scale only apply to customers using Reserved Instances
C) As AWS's aggregate customer usage grows, per-unit costs decrease and savings are passed to customers
D) Economies of scale eliminate the need for a pricing calculator

<details>
<summary>Answer</summary>

**Correct: C**

Because AWS aggregates demand from millions of customers, it achieves higher efficiency and lower costs per unit, which it has passed on through numerous price reductions over the years.

**Why the others are wrong:**
- AWS pricing changes over time (typically decreasing); it is not fixed for the account's lifetime.
- Economies of scale benefit all AWS customers via lowered list prices, not just Reserved Instance users.
- The AWS Pricing Calculator is a separate estimation tool unrelated to economies of scale.

</details>

---

