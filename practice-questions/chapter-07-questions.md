## Chapter 7: Cloud Technology and Services: Compute Services — Practice Questions

**Q1.** A media company runs a nightly video-transcoding batch job that takes 4 hours. The job can be stopped and resumed without data loss, and cost is the top priority. Which EC2 purchasing option BEST meets these requirements?

A) On-Demand Instances
B) Spot Instances
C) Reserved Instances
D) Dedicated Hosts

<details>
<summary>Answer</summary>

**Correct: B**

Spot Instances offer up to 90% savings over On-Demand and are ideal for fault-tolerant, interruptible workloads like batch transcoding.

**Why the others are wrong:**
- On-Demand is the most expensive option and unnecessary since the workload tolerates interruption.
- Reserved Instances require a 1- or 3-year commitment, which doesn't fit a workload that runs nightly and isn't guaranteed to always need capacity.
- Dedicated Hosts are for licensing/compliance needs requiring physical server isolation, not cost optimization.

</details>

---

**Q2.** A company plans to run a steady-state web application for the next 3 years with predictable, constant EC2 usage. Which purchasing option provides the deepest discount for this scenario?

A) Spot Instances
B) On-Demand Instances
C) Compute Savings Plans with 1-month commitment
D) Reserved Instances

<details>
<summary>Answer</summary>

**Correct: D**

Reserved Instances with a 3-year term offer the largest discount for steady, predictable usage compared to Spot, On-Demand, or short-term Savings Plans.

**Why the others are wrong:**
- Spot Instances can be interrupted and are not suited for a steady-state production app.
- On-Demand offers no discount and costs the most for long-term steady usage.
- A 1-month Savings Plan commitment gives a much smaller discount than a 3-year Reserved Instance.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A developer wants to run code only in response to file uploads to Amazon S3, without provisioning or managing any servers, and pay only for the compute time used during execution. Which service should they choose?

A) Amazon EC2 Auto Scaling
B) AWS Lambda
C) AWS Elastic Beanstalk
D) Amazon ECS on EC2

<details>
<summary>Answer</summary>

**Correct: B**

AWS Lambda is a serverless compute service that runs code in response to events like S3 uploads and bills only for execution time, with no server management.

**Why the others are wrong:**
- EC2 Auto Scaling still requires managing EC2 instances, which contradicts 'no servers to manage'.
- Elastic Beanstalk deploys applications onto managed EC2 instances, not a pure event-driven serverless model.
- ECS on EC2 requires managing the underlying EC2 cluster capacity.

</details>

---

**Q4.** A company wants to run containerized workloads and needs full compatibility with open-source Kubernetes tooling and the ability to migrate the same configuration to another cloud provider in the future. Which AWS service should they choose?

A) Amazon ECS
B) AWS Elastic Beanstalk
C) Amazon EKS
D) AWS Lambda

<details>
<summary>Answer</summary>

**Correct: C**

Amazon EKS is a managed Kubernetes service, giving native compatibility with standard Kubernetes APIs and tooling, which supports portability across clouds.

**Why the others are wrong:**
- Amazon ECS is an AWS-proprietary container orchestrator and does not use the Kubernetes API, limiting portability.
- Elastic Beanstalk is a PaaS for deploying applications, not a container orchestration platform focused on Kubernetes.
- Lambda runs functions, not persistent containerized Kubernetes workloads.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A startup wants to deploy a web application quickly without manually configuring the load balancer, EC2 instances, or Auto Scaling group, but still wants the ability to access and modify these underlying resources later if needed. Which service fits this requirement?

A) AWS Lambda
B) Amazon EKS
C) Amazon EC2 with manual configuration
D) AWS Elastic Beanstalk

<details>
<summary>Answer</summary>

**Correct: D**

Elastic Beanstalk is a PaaS that automatically provisions EC2 instances, load balancers, and Auto Scaling groups, while still exposing the underlying resources for manual customization.

**Why the others are wrong:**
- Lambda does not use EC2 instances or load balancers in the traditional sense and doesn't fit the 'access underlying resources' requirement.
- EKS requires configuring a Kubernetes cluster manually, which is more operational overhead than the startup wants.
- Manually configuring EC2 is exactly what the startup wants to avoid.

</details>

---

**Q6.** An Auto Scaling group is configured with a minimum of 2, maximum of 10, and desired capacity of 4 instances. One instance fails its health check. What does the Auto Scaling group do?

A) It reduces the desired capacity to 3 and does nothing further
B) It scales out to the maximum capacity of 10 instances immediately
C) It terminates the unhealthy instance and launches a replacement to maintain the desired capacity
D) It stops the unhealthy instance but takes no other action

<details>
<summary>Answer</summary>

**Correct: C**

Auto Scaling groups automatically terminate instances that fail health checks and launch replacements to maintain the configured desired capacity.

**Why the others are wrong:**
- Auto Scaling does not permanently reduce desired capacity due to a failed health check; it replaces the instance instead.
- Scaling to maximum capacity only happens due to scaling policies triggered by metrics, not a single health check failure.
- Leaving the unhealthy instance running without replacement contradicts the core self-healing function of Auto Scaling.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** What is the maximum execution timeout for a single AWS Lambda function invocation?

A) 15 minutes
B) 5 minutes
C) 30 minutes
D) 60 minutes

<details>
<summary>Answer</summary>

**Correct: A**

AWS Lambda functions have a maximum execution timeout of 15 minutes per invocation.

**Why the others are wrong:**
- 5 minutes was an outdated earlier limit and is no longer the maximum.
- 30 minutes exceeds Lambda's actual maximum timeout.
- 60 minutes exceeds Lambda's actual maximum timeout and is often confused with other services' limits.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement BEST describes the difference in operational overhead between Amazon ECS and Amazon EKS?

A) EKS requires knowledge of Kubernetes and managing a Kubernetes control plane, while ECS uses a simpler AWS-proprietary orchestration model with less operational complexity
B) ECS requires managing a Kubernetes control plane while EKS does not require any cluster management
C) Both services have identical operational overhead since they are both container orchestrators
D) ECS and EKS both eliminate all infrastructure management regardless of the underlying compute type chosen

<details>
<summary>Answer</summary>

**Correct: A**

EKS is a managed Kubernetes service requiring Kubernetes expertise to configure and operate, while ECS uses AWS's own simpler orchestration model, generally resulting in lower operational overhead for teams unfamiliar with Kubernetes.

**Why the others are wrong:**
- This reverses the relationship — ECS does not use a Kubernetes control plane at all.
- The two services differ meaningfully in complexity and skill requirements, so overhead is not identical.
- Infrastructure management still depends on whether Fargate (serverless) or EC2 launch type is chosen, so overhead isn't automatically eliminated for both.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

