## Chapter 7: Cloud Technology and Services: Compute Services — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | How much advance warning does AWS give before terminating a Spot Instance? | 2-minute interruption notice. Exam tip: Spot = deep discount, but must tolerate interruption; not for critical always-on workloads. |
| 2 | AWS Lambda maximum execution timeout per invocation? | 15 minutes. Exam tip: if a workload needs to run longer, Lambda is the wrong choice — consider EC2, ECS/Fargate, or Batch. |
| 3 | AWS Lambda maximum configurable memory? | 10,240 MB (10 GB). Exam tip: increasing memory also increases allocated CPU proportionally. |
| 4 | AWS Lambda /tmp ephemeral storage: default and maximum? | Default 512 MB, configurable up to 10,240 MB. Exam tip: this is temporary storage, wiped between invocations of a fresh execution environment. |
| 5 | Amazon ECS vs Amazon EKS — key difference? | ECS = AWS-proprietary container orchestrator, simpler to operate. EKS = managed Kubernetes, more operational overhead but Kubernetes-native/portable. Exam tip: 'need Kubernetes' = EKS; 'simplest AWS-native container option' = ECS. |
| 6 | What is AWS Fargate? | A serverless compute engine for containers — works with both ECS and EKS, removes the need to provision or manage EC2 instances. Exam tip: choose Fargate when the requirement is 'no server management' for containers. |
| 7 | Elastic Beanstalk vs raw EC2 — key difference? | Elastic Beanstalk is a PaaS that auto-provisions EC2, load balancer, and Auto Scaling for you, while still giving access to underlying resources. Raw EC2 requires manual provisioning of everything. Exam tip: 'quick deploy, less manual config, but still customizable' = Elastic Beanstalk. |
| 8 | List the main EC2 purchasing options. | On-Demand, Reserved Instances, Savings Plans, Spot Instances, Dedicated Hosts/Dedicated Instances. Exam tip: match scenario keywords — 'steady & long-term' = Reserved/Savings Plans, 'interruptible/flexible' = Spot, 'compliance/licensing' = Dedicated Hosts. |
| 9 | What three values define an Auto Scaling group's capacity? | Minimum, Maximum, and Desired capacity. Exam tip: ASG will always try to maintain the desired count between min and max, replacing unhealthy instances automatically. |
| 10 | Name the three Auto Scaling policy types. | Target tracking, Step scaling, and Scheduled scaling. Exam tip: 'maintain CPU at 50%' = target tracking; 'predictable traffic spike at 9am daily' = scheduled scaling. |
| 11 | Reserved Instance commitment terms available? | 1-year or 3-year terms. Exam tip: 3-year term = largest discount, best for long-term predictable workloads. |
| 12 | Rank AWS compute options from most to least operational overhead. | EC2 (most) > EKS > ECS > Elastic Beanstalk > Lambda (least). Exam tip: exam often frames questions around 'least management overhead' — the answer trends toward Lambda or Fargate-based options. |
