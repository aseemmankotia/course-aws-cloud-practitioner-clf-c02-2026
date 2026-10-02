## Chapter 1: Cloud Concepts: The AWS Cloud Value Proposition — Practice Questions

**Q1.** A finance manager notices the company spends millions upfront on servers every three years, and much of that capacity sits idle outside of peak season. Which AWS Cloud advantage BEST addresses this problem?

A) Increase speed and agility
B) Go global in minutes
C) Stop spending money running and maintaining data centers
D) Trade capital expense for variable expense

<details>
<summary>Answer</summary>

**Correct: D**

Paying only for compute/storage consumed instead of large upfront hardware purchases directly converts CapEx into pay-as-you-go OpEx — the exact scenario described.

**Why the others are wrong:**
- Agility refers to speed of provisioning/launching resources, not the spending model.
- Global reach is about deploying in new regions, unrelated to idle capacity spend.
- This advantage is about not managing physical data centers, which is a side effect but not the direct answer to the CapEx problem described.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During a flash sale, a retailer's web application automatically adds EC2 instances as traffic spikes and removes them within minutes once traffic drops. Which term does AWS use for this specific capability?

A) Elasticity
B) Scalability
C) High availability
D) Fault tolerance

<details>
<summary>Answer</summary>

**Correct: A**

Elasticity is the automatic, real-time addition and removal of capacity to match current demand — both scaling out and back in.

**Why the others are wrong:**
- Scalability is the broader ability to increase capacity to meet demand, but doesn't necessarily imply automatic scale-in.
- High availability refers to system uptime across failures, not capacity matching.
- Fault tolerance means continuing to operate despite component failure, unrelated to demand-based capacity changes.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company's leadership wants a structured way to plan their cloud migration, covering business justification, staff readiness, governance risk, technical architecture, security posture, and day-to-day operations. Which AWS framework should they use?

A) AWS Cloud Adoption Framework (CAF)
B) AWS Well-Architected Framework
C) AWS Total Cost of Ownership (TCO) Calculator
D) AWS Trusted Advisor

<details>
<summary>Answer</summary>

**Correct: A**

CAF provides six perspectives — Business, People, Governance, Platform, Security, Operations — exactly matching the areas described for organizing a cloud transformation.

**Why the others are wrong:**
- The Well-Architected Framework evaluates workload architecture design (six pillars), not organizational transformation.
- The TCO Calculator compares on-premises vs. AWS costs, not organizational readiness.
- Trusted Advisor gives account-level recommendations on cost, security, and performance, not a transformation framework.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A US-based startup wants to launch its application to customers in Japan and Australia without building physical infrastructure in those countries. Which AWS Cloud advantage does this scenario demonstrate?

A) Economies of scale
B) Go global in minutes
C) Increase speed and agility
D) Trade capital expense for variable expense

<details>
<summary>Answer</summary>

**Correct: B**

Deploying to AWS Regions in Japan and Australia within minutes, instead of years building data centers, is the definition of 'go global in minutes,' directly reducing time to market.

**Why the others are wrong:**
- Economies of scale is about AWS lowering prices through aggregated demand, not geographic deployment speed.
- Agility refers to speed of resource provisioning for development/testing, not international expansion specifically.
- This advantage concerns the spending model (CapEx vs OpEx), not geographic reach.

</details>

---

**Q5.** A company decides not to hire two additional IT staff members it would have needed to manage an on-premises data center refresh, because it migrated to AWS instead. How should this be classified?

A) Cost savings
B) Capital expenditure
C) Cost avoidance
D) Economies of scale

<details>
<summary>Answer</summary>

**Correct: C**

Cost avoidance means preventing a future cost the company would otherwise have incurred (hiring staff for a refresh it no longer needs to perform).

**Why the others are wrong:**
- Cost savings refers to a reduction in actual current spending, not a prevented future expense.
- Capital expenditure is the upfront spending model itself, not a cost classification outcome.
- Economies of scale describes AWS's pricing benefit from aggregated customer demand, unrelated to staffing decisions.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which AWS service is the BEST example of enabling elasticity for a fleet of EC2 instances based on real-time demand?

A) AWS Organizations
B) AWS Auto Scaling
C) AWS CloudFormation
D) Amazon CloudWatch Logs

<details>
<summary>Answer</summary>

**Correct: B**

AWS Auto Scaling automatically adds or removes EC2 capacity based on demand or defined policies, which is the core exam example of elasticity.

**Why the others are wrong:**
- AWS Organizations manages multi-account governance, not capacity scaling.
- CloudFormation provisions infrastructure as code but does not automatically scale resources based on demand by itself.
- CloudWatch Logs collects and stores log data; it doesn't scale infrastructure.

</details>

---

**Q7.** Which AWS Cloud Adoption Framework (CAF) perspective is primarily concerned with staff skills, organizational structure, and change management during cloud adoption?

A) Governance
B) Operations
C) People
D) Platform

<details>
<summary>Answer</summary>

**Correct: C**

The People perspective in CAF addresses culture, staff readiness, training, and organizational change management.

**Why the others are wrong:**
- Governance focuses on skills needed to manage risk, compliance, and cloud strategy alignment, not general staff readiness.
- Operations focuses on day-to-day service delivery and reliability of workloads once running.
- Platform focuses on principles and patterns for architecting solutions on AWS, a technical perspective.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A company migrating to AWS wants its billing model to reflect actual resource consumption instead of fixed upfront hardware purchases. Which pricing characteristic BEST supports this goal?

A) Reserved Instance three-year all-upfront pricing
B) Purchasing a Savings Plan requiring a one-year term
C) On-Demand, pay-as-you-go pricing with no upfront commitment
D) Buying physical servers with a depreciation schedule

<details>
<summary>Answer</summary>

**Correct: C**

On-Demand pricing charges only for resources actually consumed with no upfront payment, directly reflecting the variable expense model.

**Why the others are wrong:**
- All-upfront Reserved Instances require a large upfront payment, similar to CapEx, contradicting the goal.
- Savings Plans still require a term commitment, which reduces (but doesn't eliminate) the variable expense benefit compared to On-Demand.
- Buying physical servers is the traditional CapEx on-premises model the company is trying to move away from.

</details>

---

