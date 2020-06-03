# RDS

Amazon Relational Database Service is a web service that makes it easier to set up, operate, and scale a relational database in the cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks.

- supports MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL Server, and the new, MySQL-compatible Amazon Aurora DB engine
- as it is a managed service, shell (root ssh) access is not provided
- manages backups, software patching, automatic failure detection, and recovery
- supports use initiated manual backups and snapshots
- **daily automated backups with database transaction logs** enables **Point in Time recovery** up to the last five minutes of database usage
- **snapshots** are user-initiated storage volume snapshot of DB instance, backing up the **entire DB instance and not just individual databases** that can be restored as a independent RDS instance
- support encryption at rest using KMS as well as encryption in transit using SSL endpoints
- for encrypted database
  - logs, snapshots, backups, read replicas are all encrypted as well
  - cross region replicas and snapshots does not work across region (Note - this is possible now with latest AWS [enhancement])
- Multi-AZ deployment
  - provides **high availability and automatic failover support and is NOT a scaling solution**
  - maintains a **synchronous standby replica in a different AZ**
  - **transaction success is returned only if the commit is successful both on the primary and the standby DB**
  - Oracle, PostgreSQL, MySQL, and MariaDB DB instances use **Amazon technology**, while SQL Server DB instances use SQL **Server Mirroring**
  - **snapshots and backups are taken from standby & eliminate I/O freezes**
  - during automatic failover, its seamless and **RDS switches to the standby instance** and **updates the DNS record to point to standby**
  - failover can be **forced** with the Reboot with failover option
- Read Replicas
  - uses the PostgreSQL, MySQL, and MariaDB DB engines’ built-in replication functionality to create a separate Read Only instance
  - updates are **asynchronously** copied to the Read Replica, and data might be stale
  - can help **scale applications** and **reduce read only load **
  - **requires automatic backups enabled**
  - **replicates all databases** in the source DB instance
  - for disaster recovery, can be **promoted to a full fledged database**
  - can be **created in a different region** for MySQL, Postgres and MariaDB, for disaster recovery, migration and low latency across regions
- RDS does not support all the features of underlying databases, and if required the database instance can be launched on an EC2 instance
- RMAN (Recovery Manager) can be used for Oracles backup and recovery when running on an EC2 instance

[enhancement]: https://aws.amazon.com/about-aws/whats-new/2017/01/amazon-rds-now-supports-read-replicas-of-encrypted-database-instances-across-regions/

> [Service overview](https://aws.amazon.com/rds/)
