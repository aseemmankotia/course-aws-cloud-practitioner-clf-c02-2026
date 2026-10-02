# Chapter 6 Cheat Sheet: Global Infrastructure & Deployment Methods

## Global Infrastructure Hierarchy
| Component | Definition | Purpose | Exam Trigger Phrase |
|---|---|---|---|
| Region | Isolated geographic area containing multiple AZs | Data residency, compliance, latency to users | "data must stay in country X" |
| Availability Zone (AZ) | One or more discrete, physically separate data centers within a Region, min. 3 per Region, connected via low-latency links | High availability, fault tolerance within a Region | "protect against data center failure" |
| Edge Location | CloudFront caching point, far more numerous than Regions | Low-latency content delivery (CDN) | "reduce latency for global users", "cache static content" |

**Key rule:** Region ≠ AZ ≠ Edge Location. Region = where data lives (compliance). AZ = resilience within a Region. Edge Location = speed of delivery to users.

## Deployment Methods
| Method | What It Is | Best For | Exam Trigger |
|---|---|---|---|
| Management Console | Web GUI | Manual, one-off tasks, learning | "manually configure via browser" |
| CLI | Command-line tool | Scripting, automation, quick commands | "run commands from terminal" |
| SDK | Language libraries (Boto3, Java SDK, etc.) | Embedding AWS calls in application code | "call AWS API from within app code" |
| CloudFormation | Declarative IaC (JSON/YAML templates) | Repeatable, version-controlled infrastructure deployment | "deploy same infrastructure repeatedly", "version control infrastructure" |

## Connectivity Options
| Option | Path | Encryption | Setup Time | Performance | Exam Trigger |
|---|---|---|---|---|---|
| Public Internet | Public | No (unless app-layer TLS) | Immediate | Variable/unpredictable | Default/no special requirement |
| Site-to-Site VPN | Public internet, IPsec tunnel | Yes | Minutes–hours | Variable, internet-dependent | "encrypted connection quickly", "low cost secure tunnel" |
| Direct Connect | Dedicated private physical link | No (private, not internet) | Weeks–months | Consistent, high bandwidth, low latency | "bypass the internet", "consistent/dedicated bandwidth" |

## Quick Decision Rules
- **Compliance/data residency question** → Answer = Region selection.
- **"Data center outage" / HA within one country** → Answer = Multiple AZs.
- **"Global users, reduce latency, cache content"** → Answer = CloudFront (edge locations).
- **"Automate, repeatable, version-controlled infra"** → Answer = CloudFormation.
- **"Call AWS from my code"** → Answer = SDK.
- **"Quick, encrypted, low-cost connection to AWS"** → Answer = Site-to-Site VPN.
- **"Dedicated, consistent, high-bandwidth, bypass internet"** → Answer = Direct Connect.

## Common Traps
- Confusing **Region** (compliance) with **AZ** (availability) — they test different requirements.
- Assuming **VPN = Direct Connect** performance — VPN still uses public internet.
- Thinking **CloudFront** runs compute — it only caches/delivers content, not application logic.
- Forgetting **CloudFormation is free**; you only pay for the resources it provisions.
