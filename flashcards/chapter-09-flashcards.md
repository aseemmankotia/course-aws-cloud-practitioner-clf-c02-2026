## Chapter 9: Cloud Technology and Services: Networking and AI/ML Awareness — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Security Group vs Network ACL: which is stateful? | Security Groups are stateful — return traffic is automatically allowed. NACLs are stateless — you must explicitly allow both inbound and outbound traffic. Exam tip: stateless NACLs need ephemeral port rules for return traffic. |
| 2 | Security Group vs Network ACL: allow/deny rules? | Security Groups: allow rules only (implicit deny). NACLs: support both explicit allow AND deny rules, evaluated in rule number order (lowest first). |
| 3 | Security Group vs Network ACL: scope of application? | Security Groups apply at the instance/ENI level. NACLs apply at the subnet level, affecting all resources in that subnet. |
| 4 | What makes a VPC subnet 'public'? | Its route table has a route to an Internet Gateway (IGW) attached to the VPC. Exam tip: NAT Gateway enables outbound-only internet access for PRIVATE subnets, it does not make a subnet public. |
| 5 | ALB operates at which OSI layer, and for what traffic? | Layer 7 (Application). Handles HTTP/HTTPS traffic with content-based routing (path, host, headers). Exam tip: choose ALB for microservices/container-based web apps. |
| 6 | NLB operates at which OSI layer, and for what traffic? | Layer 4 (Transport). Handles TCP/UDP traffic, supports static IPs and Elastic IPs, and delivers ultra-low latency at very high throughput. Exam tip: choose NLB for extreme performance or static IP requirements. |
| 7 | Classic Load Balancer (CLB) — exam relevance? | Legacy load balancer supporting basic Layer 4/7 features. AWS recommends ALB or NLB for new workloads. Exam tip: CLB is likely the 'wrong/deprecated' answer choice in scenario questions. |
| 8 | Route 53 — what does it provide? | A highly available, scalable DNS web service that also supports domain registration and health checks. Exam tip: Route 53 does NOT filter network traffic — that's NACLs/Security Groups. |
| 9 | Route 53 routing policies (list)? | Simple, Weighted, Latency-based, Failover, Geolocation, Geoproximity, Multivalue answer. Exam tip: Latency = fastest response; Geolocation = compliance/content restriction by region; Failover = active-passive DR. |
| 10 | Amazon API Gateway — primary purpose? | Fully managed service to create, publish, secure, and monitor REST and WebSocket APIs at scale, commonly integrated with AWS Lambda for serverless backends. |
| 11 | SageMaker vs Bedrock — key difference? | SageMaker: build, train, and deploy CUSTOM ML models with your own data (full ML lifecycle control). Bedrock: access PRE-TRAINED foundation models (e.g., Anthropic Claude, Amazon Titan/Nova, Meta Llama) via a single API with no infrastructure management. |
| 12 | NACL ephemeral port rule — common exam trap | Because NACLs are stateless, allowing inbound port 80 is not enough — you must also add an outbound rule allowing the ephemeral port range (1024–65535) for return traffic, or connections will fail. |
