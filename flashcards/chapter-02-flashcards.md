## Chapter 2: Cloud Concepts: Cloud Economics and the Well-Architected Framework — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | CapEx vs OpEx: which model does AWS shift customers toward? | OpEx (variable, pay-as-you-go). Exam tip: AWS eliminates large upfront CapEx (data centers, hardware) and replaces it with usage-based operational spending. |
| 2 | Name the six pillars of the AWS Well-Architected Framework. | Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability. Exam tip: Sustainability was added in Dec 2021 — often tested as 'the newest pillar.' |
| 3 | Which Well-Architected pillar covers minimizing environmental impact? | Sustainability. Exam tip: focuses on energy efficiency and reducing resource waste in cloud workloads. |
| 4 | What does 'design for failure' mean in AWS architecture? | Assume any component can fail; build redundancy (multi-AZ, multi-Region) so failures don't cause full outages. Exam tip: tied directly to the Reliability pillar. |
| 5 | Which AWS services are commonly used to achieve loose coupling between application components? | Amazon SQS (queuing) and Amazon SNS (pub/sub). Exam tip: decoupling prevents one component's failure from cascading to others. |
| 6 | What causes AWS economies of scale? | AWS aggregates usage across millions of customers, lowering per-unit infrastructure costs, and passes savings on via price cuts. Exam tip: AWS has reduced prices many times since 2006. |
| 7 | What does 'right-sizing' mean for cost optimization? | Matching compute/storage capacity to actual workload demand instead of over-provisioning. Exam tip: use AWS Compute Optimizer or Trusted Advisor to identify underutilized resources. |
| 8 | What costs must a proper TCO (Total Cost of Ownership) comparison include for on-premises infrastructure? | Hardware, power, cooling, facility/real estate, and IT staff costs — not just purchase price. Exam tip: TCO tools compare these against AWS's all-in usage-based pricing. |
| 9 | What is the key benefit of a managed service (e.g., Amazon RDS) vs self-managed infrastructure (e.g., database on EC2)? | AWS handles undifferentiated heavy lifting — patching, backups, scaling — reducing operational burden. Exam tip: 'less operational overhead' is the exam's preferred phrasing for managed service benefits. |
| 10 | Which Well-Architected pillar covers monitoring, automation, and continuous improvement of operations? | Operational Excellence. Exam tip: includes running workloads via Infrastructure as Code and using runbooks/automation. |
| 11 | Which Well-Architected pillar covers the ability to recover from failures and scale to meet demand? | Reliability. Exam tip: includes design for failure, automated recovery, and testing recovery procedures. |
| 12 | Give an example of a fixed (CapEx) cost in traditional on-premises IT. | Purchasing servers and building/leasing data center facilities upfront. Exam tip: contrast with AWS's variable OpEx model billed by actual usage. |
