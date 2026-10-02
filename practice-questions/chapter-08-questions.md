## Chapter 8: Cloud Technology and Services: Storage and Database Services — Practice Questions

**Q1.** A media company runs a render farm of 50 Linux EC2 instances across three Availability Zones. All instances must read and write to the same shared project files concurrently. Which storage solution BEST meets this requirement?

A) Amazon EBS with Multi-Attach enabled
B) Amazon S3 with versioning
C) Instance store volumes
D) Amazon EFS

<details>
<summary>Answer</summary>

**Correct: D**

Amazon EFS is a fully managed NFS file system that can be mounted concurrently by thousands of EC2 instances across multiple AZs, making it ideal for shared, concurrent access patterns.

**Why the others are wrong:**
- EBS Multi-Attach only works within a single AZ and is limited to a small number of Nitro instances, and it requires a cluster-aware file system to avoid data corruption — not suited for 50 instances across 3 AZs.
- S3 is object storage, not a POSIX file system; applications expecting file-level read/write access cannot mount S3 directly.
- Instance store is ephemeral, local to a single instance, and data is lost on stop/terminate — it cannot be shared.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company has 500TB of video archives accessed roughly once a year. Retrieval times of up to 12 hours are acceptable, and cost minimization is the top priority. Which S3 storage class should they choose?

A) S3 Glacier Deep Archive
B) S3 Standard-IA
C) S3 Glacier Flexible Retrieval
D) S3 One Zone-IA

<details>
<summary>Answer</summary>

**Correct: A**

S3 Glacier Deep Archive is the lowest-cost S3 storage class, designed for data accessed once or twice a year, with a Standard retrieval tier of about 12 hours — matching both the access pattern and retrieval requirement.

**Why the others are wrong:**
- Standard-IA is meant for data accessed monthly, not yearly, and costs significantly more than Deep Archive for this pattern.
- Glacier Flexible Retrieval is cheaper than Standard-IA but more expensive than Deep Archive; its Standard retrieval (3-5 hours) is faster than needed, meaning the company is overpaying.
- One Zone-IA lacks multi-AZ resilience and is intended for infrequently accessed but easily reproducible data, not long-term archives — it's also costlier than Deep Archive.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A gaming startup is building a leaderboard feature that must return player rankings with single-digit millisecond latency, regardless of how many players are added. Which database service should they use?

A) Amazon RDS for MySQL
B) Amazon DynamoDB
C) Amazon Redshift
D) Amazon EFS

<details>
<summary>Answer</summary>

**Correct: B**

DynamoDB is a fully managed NoSQL key-value database purpose-built to deliver consistent single-digit millisecond performance at any scale, ideal for leaderboards and gaming workloads.

**Why the others are wrong:**
- RDS for MySQL is a relational database that scales vertically and requires read replicas to scale reads; it cannot guarantee consistent single-digit millisecond latency at massive scale as easily as DynamoDB.
- Redshift is a data warehouse optimized for analytical queries over large datasets, not low-latency transactional lookups.
- EFS is a file storage service, not a database, and is irrelevant to structured key-value lookups.

</details>

---

**Q4.** Which AWS database service is a MySQL- and PostgreSQL-compatible relational engine that AWS states can deliver up to five times the throughput of standard MySQL?

A) Amazon RDS for MySQL
B) Amazon DynamoDB
C) Amazon Aurora
D) Amazon Redshift

<details>
<summary>Answer</summary>

**Correct: C**

Amazon Aurora is AWS's proprietary relational engine, wire-compatible with MySQL and PostgreSQL, offering up to 5x the throughput of standard MySQL and 3x that of standard PostgreSQL.

**Why the others are wrong:**
- Standard RDS for MySQL runs open-source MySQL directly and does not include Aurora's performance enhancements.
- DynamoDB is a NoSQL service, not relational, and has no MySQL/PostgreSQL compatibility.
- Redshift is a columnar data warehouse for analytics, not a transactional MySQL/PostgreSQL-compatible engine.

</details>

---

**Q5.** A retail company wants to run complex analytical queries joining sales, inventory, and customer data spanning several petabytes to generate business intelligence reports. Which service is BEST suited for this workload?

A) Amazon DynamoDB
B) Amazon Redshift
C) Amazon RDS
D) Amazon EFS

<details>
<summary>Answer</summary>

**Correct: B**

Amazon Redshift is a petabyte-scale data warehouse that uses columnar storage and massively parallel processing, purpose-built for complex analytical (OLAP) queries across large datasets.

**Why the others are wrong:**
- DynamoDB is optimized for high-speed key-value lookups, not complex multi-table analytical joins.
- RDS is designed for transactional (OLTP) workloads and does not scale efficiently to petabyte-scale analytical queries.
- EFS is a file storage service and has no query engine or analytical capability.

</details>

---

**Q6.** You need to attach a general-purpose SSD volume to an EC2 instance that balances price and performance for most everyday workloads, and is now the default recommended volume type. Which EBS volume type should you select?

A) io2
B) st1
C) gp3
D) sc1

<details>
<summary>Answer</summary>

**Correct: C**

gp3 is AWS's current default general-purpose SSD volume, offering a baseline of 3,000 IOPS and 125 MiB/s throughput independent of volume size, with the ability to provision additional IOPS/throughput separately at lower cost than gp2.

**Why the others are wrong:**
- io2 is a provisioned IOPS SSD volume designed for mission-critical, latency-sensitive workloads that need very high and consistent IOPS — it costs more and is not the default general-purpose choice.
- st1 is a low-cost HDD volume optimized for large, sequential throughput workloads like big data and log processing, not general-purpose use.
- sc1 is a cold HDD volume for the lowest-cost, infrequently accessed workloads and has the lowest performance of all EBS types.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** An archive object is stored in S3 Glacier Deep Archive. You need it available within 12 hours. Which retrieval tier should you request?

A) Expedited
B) Bulk
C) Instant
D) Standard

<details>
<summary>Answer</summary>

**Correct: D**

S3 Glacier Deep Archive's Standard retrieval tier delivers objects within about 12 hours, which meets the stated requirement at a lower cost than requesting the fastest tier unnecessarily.

**Why the others are wrong:**
- Expedited retrieval is not offered for Deep Archive; it is only available for Glacier Flexible Retrieval, where it returns data in 1-5 minutes.
- Bulk retrieval for Deep Archive takes about 48 hours, exceeding the 12-hour requirement.
- Instant retrieval refers to S3 Glacier Instant Retrieval storage class (millisecond access), not a retrieval tier within Deep Archive.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the key architectural difference between Amazon EBS and Amazon EFS?

A) EBS is object storage while EFS is block storage
B) EBS attaches to a single EC2 instance within one Availability Zone, while EFS can be mounted concurrently by multiple instances across multiple Availability Zones
C) EBS scales automatically with no size limit, while EFS requires manual provisioning of storage size
D) EFS is only compatible with Windows instances, while EBS is only compatible with Linux instances

<details>
<summary>Answer</summary>

**Correct: B**

EBS is block storage tied to a single EC2 instance in a specific AZ (except limited Multi-Attach cases), whereas EFS is a shared, elastic NFS file system accessible by many instances simultaneously across AZs.

**Why the others are wrong:**
- This reverses the storage types — EBS is block storage, and EFS is file storage, not object storage.
- EFS actually scales automatically and elastically with no pre-provisioning needed, while EBS volumes must be sized and provisioned upfront (though they can be resized later).
- Both EBS and EFS support Linux; EFS does not support Windows at all, and this option misstates OS compatibility.

</details>

---

