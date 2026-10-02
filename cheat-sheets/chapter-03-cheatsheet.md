# Shared Responsibility Model — Cheat Sheet

## The Split
| Layer | Responsible Party |
|---|---|
| Physical data centers, hardware, hypervisor | **AWS** (security OF the cloud) |
| Network infrastructure (AWS backbone) | **AWS** |
| Guest OS, applications, data | **Customer** (security IN the cloud) |
| IAM configuration (policies, users, roles) | **Customer** — always, every service |
| Encryption in transit (TLS/HTTPS config) | **Customer** |
| Encryption at rest (enabling KMS/SSE) | **Customer** (some defaults exist, e.g., S3 SSE-S3) |

## Responsibility Shift by Service Type
| Task | EC2 (IaaS) | RDS (Managed) | Lambda (Serverless) |
|---|---|---|---|
| Guest OS patching | Customer | **AWS** | **AWS** |
| DB engine patching | N/A (self-managed) | **AWS** | N/A |
| Runtime patching | Customer | AWS (managed engine) | **AWS** |
| Security groups / network ACLs | Customer | Customer | Customer (via VPC config if used) |
| IAM policy configuration | Customer | Customer | Customer |
| Data encryption settings | Customer | Customer | Customer |
| Application/function code security | Customer | Customer (queries/app logic) | Customer |
| Physical hardware | AWS | AWS | AWS |

**Rule of thumb:** The more abstracted the service (IaaS → managed service → serverless), the more infrastructure responsibility shifts to AWS. Customer responsibility for **data, IAM, and app-level config never disappears** — it exists on every service.

## Exam Traps
- ❌ "AWS is responsible for guest OS patching on EC2" — **FALSE**, that's the customer's job.
- ❌ "RDS requires the customer to patch the database engine" — **FALSE**, AWS does this (customer picks the maintenance window).
- ❌ "Lambda still requires OS patching from the customer" — **FALSE**, AWS fully manages this.
- ❌ "AWS automatically encrypts everything in transit with no setup" — **FALSE**, customer must configure TLS.
- ❌ "IAM configuration responsibility shifts to AWS with managed services" — **FALSE**, IAM policy setup is ALWAYS the customer's job.

## Quick Memory Anchor
**"AWS secures the cloud itself. You secure what you put IN it — and how you control who gets in."**
- OF the cloud = physical + host + network (AWS)
- IN the cloud = OS + apps + data + IAM + encryption config (Customer)
