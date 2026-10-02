## Chapter 6: Cloud Technology and Services: Global Infrastructure and Deployment Methods — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Minimum number of Availability Zones per AWS Region? | 3 (minimum). Exam tip: high availability architectures should span at least 2, ideally all available AZs in a Region. |
| 2 | AWS Region vs Availability Zone vs Edge Location — what's the difference? | Region = geographic area with multiple AZs (data residency/compliance). AZ = physically separate data center within a Region (high availability). Edge Location = CloudFront caching point close to users (low latency content delivery). Exam tests choosing the right one per scenario. |
| 3 | Site-to-Site VPN vs Direct Connect — key exam difference? | VPN: encrypted tunnel over public internet, fast to set up, variable performance. Direct Connect: dedicated private physical connection, consistent low latency/high bandwidth, longer provisioning time (weeks+). Exam tip: 'consistent bandwidth' or 'bypass internet' = Direct Connect. |
| 4 | What deploys infrastructure using declarative JSON/YAML templates on AWS? | AWS CloudFormation. Exam tip: enables Infrastructure as Code — repeatable, version-controlled deployments. |
| 5 | Which AWS access method is best for embedding AWS calls directly into application code? | AWS SDK (e.g., Boto3 for Python, AWS SDK for Java/.NET/JS). Exam tip: SDK = code-level integration; CLI = terminal commands; Console = GUI. |
| 6 | What is the AWS Management Console? | The web-based graphical user interface (GUI) for manually managing AWS resources. Exam tip: not suited for automation or Infrastructure as Code. |
| 7 | What is the AWS CLI used for? | Command Line Interface for managing AWS resources via terminal commands and scripts. Exam tip: good for automation/scripting but not declarative IaC like CloudFormation. |
| 8 | What service does Amazon CloudFront provide? | A global Content Delivery Network (CDN) that caches content at edge locations to reduce latency for end users. Exam tip: 'reduce latency for global users' → CloudFront. |
| 9 | How are Availability Zones within a Region connected? | Via high-bandwidth, low-latency, redundant private networking links. Exam tip: AZs are far enough apart to avoid correlated disaster impact, but close enough for low-latency synchronous replication. |
| 10 | What determines data residency/compliance for stored AWS data? | The AWS Region selected for deployment. Data does not automatically replicate outside the chosen Region unless configured. Exam tip: Region choice = compliance/data residency answer. |
| 11 | Which connectivity option is fastest to provision: VPN or Direct Connect? | Site-to-Site VPN — can be set up in minutes/hours since it uses existing internet connectivity. Direct Connect requires physical circuit installation, taking weeks to months. |
| 12 | Are edge locations the same as Regions? | No. Edge locations are CloudFront caching endpoints, far more numerous than Regions, and do not host EC2/compute resources — they only cache/deliver content closer to users. |
