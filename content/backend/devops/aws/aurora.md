# Aurora

Amazon Aurora is a MySQL and PostgreSQL compatible relational database built for the cloud, that combines the performance and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases.

It provides the security, availability, and reliability of commercial-grade databases at 1/10th the cost. Aurora is fully managed by Amazon Relational Database Service (RDS), which automates time-consuming administration tasks like hardware provisioning, database setup, patching, and backups.

Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance. Aurora delivers high performance and availability with up to 15 low-latency read replicas, point-in-time recovery, continuous backup to Amazon S3, and replication across three Availability Zones.

- AWS Aurora is a relational database engine that combines the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases.
- Amazon Aurora (Aurora) is a fully managed, MySQL- and PostgreSQL-compatible, relational database engine i.e. applications developed with MySQL can switch to Aurora with little or no changes
- Aurora delivers up to 5x performance of MySQL without requiring any changes to most MySQL applications
- Aurora PostgreSQL delivers up to 3x performance of PostgreSQL.
- RDS manages the Aurora databases, handling time-consuming tasks such as provisioning, patching, backup, recovery, failure detection and repair.
- Based on the database usage, Aurora storage will automatically grow, from **10GB to 64TB** in 10GB increments with no impact to database performance

#### High Availability and Replication

- Aurora provides data durability and reliability by replicating the database volume six ways **across three Availability Zones in a single region**
  - Aurora automatically divides the database volume into 10GB segments spread across many disks.
  - Each 10GB chunk of your database volume is replicated six ways, across three Availability Zones
- RDS databases _for e.g. MySQL, Oracle etc._ have the data in a single AZ
- Aurora is designed to transparently handle the loss of up to two copies of data without affecting database write availability and up to three copies without affecting read availability.
- Aurora storage is also self-healing. Data blocks and disks are continuously scanned for errors and repaired automatically.
- Aurora Replicas share the same underlying volume as the primary instance. Updates made by the primary are visible to all Aurora Replicas
- As Aurora Replicas share the same data volume as the primary instance, there is virtually no replication lag
- Any Aurora Replica can be promoted to become primary without any data loss and therefore can be used for enhancing fault tolerance in the event of a primary DB Instance failure.
- To increase database availability, 1 to 15 replicas can be created in any of 3 AZs, and RDS will automatically include them in failover primary selection in the event of a database outage.

#### Security

- Aurora uses SSL (AES-256) to secure the connection between the database instance and the application
- Aurora allows database encryption using keys managed through AWS Key Management Service (KMS).
- Encryption and decryption are handled seamlessly.
- With Aurora encryption, data stored at rest in the underlying storage is encrypted, as are its automated backups, snapshots, and replicas in the same cluster.
- Encryption of existing unencrypted Aurora instance is not supported. Create a new encrypted Aurora instance and migrate the data

#### Backup and Restore

- Automated backups are always enabled on Aurora DB Instances.
- Backups do not impact database performance.
- Aurora also allows creation of manual snapshots
- Aurora automatically maintains 6 copies of your data across 3 AZs and will automatically attempt to recover your database in a healthy AZ with no data loss.
- If in any case the data is unavailable within Aurora storage,
  - DB Snapshot can be restored or
  - point-in-time restore operation can be performed to a new instance. Latest restorable time for a point-in-time restore operation can be up to 5 minutes in the past.
- Restoring a snapshot creates a new Aurora DB instance
- Deleting Aurora database deletes all the automated backups (with an option to create a final snapshot), but would not remove the manual snapshots.
- Snapshots (including encrypted ones) can be shared with another AWS accounts

> [Service overview](https://aws.amazon.com/cloudfront/)
