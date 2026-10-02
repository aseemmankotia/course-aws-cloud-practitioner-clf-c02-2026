## Chapter 8: Cloud Technology and Services: Storage and Database Services — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Amazon S3 durability guarantee? | 99.999999999% (11 nines) durability for objects across multiple AZs. Exam tip: durability ≠ availability — availability varies by storage class. |
| 2 | Maximum size of a single S3 object? | 5 TB. Exam tip: uploads over 100 MB should use multipart upload for reliability and speed. |
| 3 | Can an EBS volume attach to multiple EC2 instances simultaneously? | Only with EBS Multi-Attach, and only within the same AZ, on select Nitro instance types with io1/io2 volumes. By default, EBS attaches to one instance only. |
| 4 | EFS vs EBS — which supports multi-AZ concurrent access? | EFS. It's a shared NFS file system mountable by thousands of instances across multiple AZs. EBS is single-instance, single-AZ by default. |
| 5 | S3 Glacier Instant Retrieval — access time? | Milliseconds, same as S3 Standard. Exam tip: use when data is accessed rarely (quarterly) but needs immediate access when requested. |
| 6 | S3 Glacier Flexible Retrieval — Expedited tier time? | 1-5 minutes. Exam tip: Flexible Retrieval also offers Standard (3-5 hours) and Bulk (5-12 hours) tiers. |
| 7 | S3 Glacier Deep Archive retrieval times? | Standard: ~12 hours. Bulk: ~48 hours. Exam tip: Deep Archive is the cheapest S3 class, for data accessed 1-2 times per year. |
| 8 | Amazon Aurora storage auto-scaling limit and replication? | Auto-scales up to 128 TiB; data is replicated 6 ways across 3 Availability Zones automatically for high durability. |
| 9 | RDS Multi-AZ vs Read Replica — purpose? | Multi-AZ = synchronous standby for high availability/failover (not for scaling reads). Read Replica = asynchronous copy for scaling read throughput. Exam commonly confuses these. |
| 10 | When to choose DynamoDB over RDS? | Choose DynamoDB for key-value/document workloads needing single-digit millisecond latency at massive, unpredictable scale with flexible schema. Choose RDS for structured relational data needing complex joins/transactions. |
| 11 | Primary use case for Amazon Redshift? | OLAP data warehousing — complex analytical queries over large, petabyte-scale structured datasets using columnar storage and MPP architecture. Not for transactional (OLTP) workloads. |
| 12 | S3 storage class for data accessed monthly needing millisecond access but lower storage cost than Standard? | S3 Standard-IA (Infrequent Access). Exam tip: charges a retrieval fee per GB, so it's only cost-effective if access is infrequent (not daily). |
