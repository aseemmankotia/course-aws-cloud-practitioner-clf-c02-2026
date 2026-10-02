## Chapter 10: Billing, Pricing, and Support: Pricing Models and Account Structure — Practice Questions

**Q1.** A company runs a steady-state database workload it knows will run for exactly one year but wants the option to later swap the instance family, OS, or tenancy without losing its discount. Which purchasing option BEST fits this requirement?

A) Standard Reserved Instance
B) Spot Instance
C) On-Demand Instance
D) Convertible Reserved Instance

<details>
<summary>Answer</summary>

**Correct: D**

Convertible RIs allow exchanging the reservation for one with different instance families, OS, or tenancy during the term, at the cost of a lower max discount (~66%) than Standard.

**Why the others are wrong:**
- Standard RIs lock in instance family/type — no exchange for family/OS changes, only offers higher discount (~72%)
- Spot Instances have no commitment discount structure and can be interrupted at any time
- On-Demand has no commitment discount at all, defeating the purpose of a known 1-year workload

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A batch image-processing job can tolerate being stopped and restarted at any time, has no fixed deadline, and the company wants the lowest possible compute cost. Which pricing model should they choose?

A) On-Demand Instances
B) Standard Reserved Instances
C) Savings Plans
D) Spot Instances

<details>
<summary>Answer</summary>

**Correct: D**

Spot Instances offer up to 90% off On-Demand pricing and are ideal for fault-tolerant, flexible workloads that can handle a 2-minute interruption notice.

**Why the others are wrong:**
- On-Demand is the most expensive option and doesn't optimize cost for flexible workloads
- Standard RIs require a 1- or 3-year commitment, unsuitable for unpredictable batch jobs
- Savings Plans require committed hourly spend and don't offer the deepest discount for interruptible workloads

</details>

---

**Q3.** A company has separate AWS accounts for Finance, Engineering, and Marketing. It wants a single monthly invoice and to combine usage across accounts to reach volume pricing tiers faster. What should it implement?

A) IAM cross-account roles
B) AWS Organizations with consolidated billing
C) AWS Budgets with linked alerts
D) Separate Reserved Instance purchases in each account

<details>
<summary>Answer</summary>

**Correct: B**

AWS Organizations consolidated billing combines usage from all member accounts into one bill and aggregates usage to reach volume discount tiers (e.g., S3 storage) faster.

**Why the others are wrong:**
- IAM cross-account roles manage access permissions, not billing
- AWS Budgets only monitors and alerts on spend, it does not combine billing or discounts
- Purchasing RIs separately per account does not aggregate usage for volume discounts

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which pricing model provides the MOST flexibility by automatically applying a committed hourly spend discount across EC2 instance families, AWS Fargate, and AWS Lambda usage, regardless of region?

A) Compute Savings Plans
B) EC2 Instance Savings Plans
C) Standard Reserved Instances
D) Convertible Reserved Instances

<details>
<summary>Answer</summary>

**Correct: A**

Compute Savings Plans are the most flexible option, applying to any instance family, size, OS, tenancy, region, and even Fargate/Lambda usage, in exchange for a slightly lower discount (up to ~66%).

**Why the others are wrong:**
- EC2 Instance Savings Plans are locked to a specific instance family within a region, less flexible
- Standard RIs are locked to a specific instance type/family and region
- Convertible RIs allow family changes but are still limited to EC2 only, not Fargate or Lambda

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A startup needs to run a short-term proof-of-concept workload for two weeks with completely unpredictable usage patterns and no upfront commitment. Which pricing model is MOST appropriate?

A) Savings Plans
B) On-Demand Instances
C) Reserved Instances
D) Spot Instances

<details>
<summary>Answer</summary>

**Correct: B**

On-Demand pricing requires no upfront commitment and charges per second/hour of use, ideal for short-term, unpredictable workloads like a two-week PoC.

**Why the others are wrong:**
- Savings Plans require a 1- or 3-year committed spend, unsuitable for a 2-week project
- Reserved Instances require long-term commitment, not appropriate for a short PoC
- Spot Instances could be interrupted at any time, risky for a time-sensitive PoC without fault tolerance

</details>

---

**Q6.** How much advance notice does AWS provide before reclaiming a Spot Instance?

A) 2 minutes
B) 5 minutes
C) 30 seconds
D) No notice is given

<details>
<summary>Answer</summary>

**Correct: A**

AWS issues a Spot interruption notice 2 minutes before reclaiming the instance capacity, via EC2 instance metadata or an EventBridge event.

**Why the others are wrong:**
- 5 minutes is not the AWS-defined interruption warning period
- 30 seconds is too short and not the documented value
- AWS does provide a notice — it does not reclaim Spot Instances silently

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A developer launches a t2.micro EC2 instance and an AWS Lambda function in a new AWS account to test a personal project. Which statement about AWS Free Tier usage is correct?

A) Both the EC2 instance and Lambda usage are free forever with no limits
B) Only Lambda is covered by Free Tier; EC2 always incurs charges
C) The EC2 t2.micro hours are free for 12 months up to a monthly limit, while Lambda includes an always-free monthly allowance
D) Free Tier only applies to accounts created before 2020

<details>
<summary>Answer</summary>

**Correct: C**

EC2 t2.micro/t3.micro usage (750 hrs/month) is part of the 12-month Free Tier, while Lambda's 1M requests and 400,000 GB-seconds/month are part of the Always Free offers that don't expire.

**Why the others are wrong:**
- Free Tier has specific monthly limits and time windows, it is not unlimited or forever for EC2
- EC2 does have Free Tier coverage for the first 12 months, this option is factually wrong
- Free Tier is available to any new or eligible AWS account regardless of creation year, not date-restricted like this

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the PRIMARY billing benefit an organization gains by enabling consolidated billing in AWS Organizations?

A) Automatic encryption of all data across linked accounts
B) A single bill for all accounts plus combined usage to reach volume pricing discounts sooner
C) Free Reserved Instances for every linked account
D) Automatic IAM permission sharing across accounts

<details>
<summary>Answer</summary>

**Correct: B**

Consolidated billing merges invoices from all member accounts into a single bill for the management account and aggregates usage to hit volume discount tiers faster (e.g., S3 storage pricing tiers).

**Why the others are wrong:**
- Consolidated billing has nothing to do with encryption; that's a security service concern
- RIs are not free — consolidated billing only allows RI discount sharing across accounts within the organization, not free RIs
- IAM permissions are not automatically shared through consolidated billing; that requires separate IAM/SCP configuration

</details>

---

