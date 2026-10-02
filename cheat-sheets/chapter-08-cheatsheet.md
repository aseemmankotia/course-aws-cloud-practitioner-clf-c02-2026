## Chapter 8 Cheat Sheet: Storage & Database Services

### Storage Comparison
| Service | Type | Scope | Use Case |
|---|---|---|---|
| S3 | Object | Regional, unlimited | Static assets, backups, data lakes |
| EBS | Block | Single EC2, single AZ | OS volumes, databases needing low-latency block storage |
| EFS | File (NFS) | Multi-instance, multi-AZ | Shared file access, content management, home directories |
| S3 Glacier | Object (archive) | Regional | Long-term archival, compliance data |

### S3 Storage Classes (cost: high → low)
| Class | Access Pattern | Retrieval |
|---|---|---|
| S3 Standard | Frequent | Milliseconds |
| S3 Intelligent-Tiering | Unknown/changing | Milliseconds (auto-tiers) |
| S3 Standard-IA | Infrequent (monthly) | Milliseconds + retrieval fee |
| S3 One Zone-IA | Infrequent, reproducible data | Milliseconds, single AZ |
| Glacier Instant Retrieval | Rare (quarterly) | Milliseconds |
| Glacier Flexible Retrieval | Rare (1-2x/yr) | Expedited: 1-5 min; Standard: 3-5 hr; Bulk: 5-12 hr |
| Glacier Deep Archive | Rarest (1-2x/yr) | Standard: ~12 hr; Bulk: ~48 hr |

### EBS Volume Types
| Type | Category | Best For |
|---|---|---|
| gp3 | General SSD (default) | Most workloads, balanced price/performance |
| io2 | Provisioned IOPS SSD | Mission-critical, high-IOPS databases |
| st1 | Throughput HDD | Big data, log processing (sequential) |
| sc1 | Cold HDD | Lowest cost, infrequent access |

### Database Comparison
| Service | Model | Best For |
|---|---|---|
| RDS | Relational (managed) | Traditional OLTP apps (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB) |
| Aurora | Relational (AWS-built) | High-throughput MySQL/PostgreSQL-compatible workloads; up to 5x MySQL throughput |
| DynamoDB | NoSQL key-value/document | Massive scale, single-digit ms latency, serverless |
| Redshift | Columnar data warehouse | Petabyte-scale analytics/BI (OLAP) |

### Key Numbers to Memorize
- S3 durability: 99.999999999% (11 nines)
- S3 max object size: 5 TB
- Aurora max storage: 128 TiB, 6 copies across 3 AZs
- Glacier Deep Archive minimum storage duration: 180 days (early deletion fee applies)
- Glacier Flexible Retrieval minimum storage duration: 90 days

### Exam Traps
- EBS is NOT shared across instances by default — EFS is.
- RDS Multi-AZ ≠ read scaling; it's for failover/HA only. Use Read Replicas for read scaling.
- Redshift ≠ OLTP database; it's for analytics (OLAP).
- Cheapest ≠ always correct — match retrieval time requirement to the tier before choosing based on price alone.
