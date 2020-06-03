# Storage Gateway

AWS Storage Gateway is a hybrid storage service that enables your on-premises applications to seamlessly use AWS cloud storage. You can use the service for backup and archiving, disaster recovery, cloud data processing, storage tiering, and migration. Your applications connect to the service through a virtual machine or hardware gateway appliance using standard storage protocols, such as NFS, SMB and iSCSI. The gateway connects to AWS storage services, such as Amazon S3, Amazon Glacier, and Amazon EBS, providing storage for files, volumes, and virtual tapes in AWS. The service includes a highly-optimized data transfer mechanism, with bandwidth management, automated network resilience, and efficient data transfer, along with a local cache for low-latency on-premises access to your most active data.

## Storage Gateway Overview

- AWS Storage Gateway connects on-premises software appliance with cloud-based storage to provide seamless integration with data security features between the on-premises IT environment and the AWS storage infrastructure.
- Storage Gateway allows storage of data in the AWS cloud for scalable and cost-effective storage while maintaining data security.
- Exposes compatible iSCSI interface on the front end to easily integrate with existing backup applications and represents an other disk drive
- AWS Storage Gateway backs up the data in Amazon Storage as incremental EBS snapshots
- AWS Storage Gateway can run either on-premises, as a virtual machine (VM) appliance, or in AWS, as an EC2 instance. So if the on-premises data center goes offline and there is no available host, the gateway can be deployed on an EC2 instance.
- Gateways hosted on EC2 instances can be used for disaster recovery, data mirroring, and providing storage for applications hosted on EC2
- **AWS Storage Gateway, by default, uploads data using SSL and provides data encryption at rest when stored in S3 or Glacier using AES-256**
- AWS Storage Gateway performs compression of data in-transit and at-rest

### Storage Gateway Types

AWS Storage Gateway offers both volume-based and tape-based storage solutions

#### Volume gateways

Volume gateways provide cloud-backed storage volumes that you can mount as Internet Small Computer System Interface (iSCSI) devices from your on-premises application servers. For Volume gateways all data is securely stored in AWS, the approach differs with how much data is stored on-premises

#### Gateway-cached volumes

- Data is stored in S3 and acts as a Primary data storage
- Gateway retains a copy of recently read data locally for low latency access to the frequently accessed data
- Gateway-cached volumes offer a substantial cost savings on primary storage and minimize the need to scale your storage on-premises.
- Each gateway configured for gateway-cached volumes can support up to 32 volumes, with each volume ranging from 1GiB to 32TiB, for a total maximum storage volume of 1,024 TiB (1 PiB).
- Gateway-cached volumes can be attached as iSCSI devices from on-premises application servers
- Gateway-cached volumes can be backed up incrementally by taking snapshots which are stored as EBS snapshots in Amazon S3. These snapshots can be restored as gateway storage volume or used to create EBS volumes (if < 16TiB) to attached to an EC2 instance
- All gateway-cached volume data and snapshot data is stored in Amazon S3 encrypted at rest using server-side encryption (SSE) and it cannot be accessed with S3 API or any other tools
- Gateway VM can be allocate disks
  - Cache storage
    - Cache storage, acts as the on-premises durable storage, stores the data before uploading it to Amazon S3
    - Cache storage also stores recently read data for low-latency access
  - Upload buffer
    - Upload buffer acts as a staging area, before the data is uploaded to S3
    - Gateway uploads data over an encrypted Secure Sockets Layer (SSL) connection to AWS, where it is stored encrypted in Amazon S3

#### Gateway-stored volumes

- Gateway-stored volumes maintain the entire data set locally to provide low latency access
- Gateway asynchronously backs up point-in-time snapshots (in the form of EBS snapshots) of the data to S3 which provides durable off-site backups
- Gateway-cached volumes can be attached as iSCSI devices from on-premises application servers
- Each gateway configured for gateway-stored volumes can support up to 12 32 volumes, ranging from 1GiB to 16TiB, and a total volume storage of 192 TiB
- Gateway-stored volume configuration provides durable and inexpensive off-site backups that you can recover to your local data center or Amazon EC2. For example, if you need replacement capacity for disaster recovery, you can recover the backups to Amazon EC2.
- Gateway-stored volumes can be backed up incrementally by taking snapshots which are stored as EBS snapshots in Amazon S3. These snapshots can be restored as gateway storage volume or used to create EBS volumes (if < 16TiB) to attached to an EC2 instance
- Gateway VM can be allocate disks
  - Volume Storage
    - For storing the actual data
    - Can be mapped to on-premises direct-attached storage (DAS) or storage area network (SAN) disks
  - Upload buffer
    - Upload buffer acts as a staging area, before the data is uploaded to S3
    - Gateway uploads data over an encrypted Secure Sockets Layer (SSL) connection to AWS, where it is stored encrypted in Amazon S3

### Tape-based storage solutions

#### Gateway–virtual tape library (VTL)

- Gateway-VTL provides cost-effective and durable archival of backup data in Amazon Glacier.
- Gateway-VTL provides a virtual tape infrastructure that scales seamlessly with the business needs and eliminates the operational burden of provisioning, scaling, and maintaining a physical tape infrastructure.
- VTL interface lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your gateway-VTL.
- Each gateway-VTL is preconfigured with a media changer and tape drives, which are available to the existing client backup applications as iSCSI devices. Tape cartridges can be added as needed to archive your data.
- Gateway VTL has the following components :-
  - Virtual tape
    - Virtual tape are similar to the physical tape cartridge, except that the data is stored in the AWS storage solution
    - Each gateway can contain 1500 tapes or up to 150 TiB of total tape data, with each tape ranging from 100 GiB to 2.5 TiB
  - **Virtual tape library**
    - Virtual tape library is similar to the physical tape library with tape drives (replaced with VTL tape drive) and robotic arms (replaced with Media changer)
    - Tapes in the Virtual tape library are backup in Amazon **S3**
    - Backup software writes data to the gateway, the gateway stores data locally and then asynchronously uploads it to virtual tapes in Amazon S3.
  - **Virtual tape shelf**
    - Virtual tape shelf is similar to the offsite tape holding facility
    - Tapes in the Virtual tape library are backup in Amazon ****Glacier**** providing an extremely low-cost storage service for data archiving and backup
    - VTS is located in the same region where the gateway was created and every region would have a single VTS irrespective of the number of gateways
  - Archiving tapes
    - When the backup software ejects a tape, the gateway moves the tape to the VTS for long term storage
  - Retrieving tapes
    - Tape can be retrieved from VTS only by first retrieving the tapes first to VTL and would be available in the VTL in about 24 hours
- Gateway VM can be allocate disks
  - Cache storage
    - Cache storage, acts as the on-premises durable storage, stores the data before uploading it to Amazon S3
    - Cache storage also stores recently read data for low-latency access
  - Upload buffer
    - Upload buffer acts as a staging area, before the data is uploaded to the Virtual tape
    - Gateway uploads data over an encrypted Secure Sockets Layer (SSL) connection to AWS, where it is stored encrypted in Amazon S3

## Use cases

- hybrid cloud workloads

  Big data analytics, data processing, machine learning or cloud data migration workloads with on-premises applications or data sources require architectures that require both local access and a connection to a central cloud object storage repository -- Amazon S3. The File Gateway helps you manage hybrid file and object workloads that run across both your organization and the AWS Cloud.

- Backup and restore

  The Tape Gateway configuration is a cloud-based virtual tape library (VTL) that serves as a drop-in replacement for tape backup systems, and integrates with leading industry backup software tools. Get the performance of local disk backups, and low-cost, highly scalable and durable cloud back-ups without disrupting current tape-based processes.

- Disaster recovery on AWS

  With a Volume Gateway configuration, you can take snapshots of your local volumes and store those snapshots in Amazon EBS. Those snapshots can be the starting point for an Amazon EBS volume, which you can then attach to an Amazon EC2 instance. In the event of a local site disaster simply set up your applications in the cloud or in a different datacenter, and restore your snapshot to keep running.

- Tiered storage for files & volumes

  Expanding on-premises NAS and SAN storage arrays consumes time, capital, and rack space. Configuring the service as a File Gateway or a Volume gives you a flexible buffer for application file data, or block volume storage that can grow as needed, extending the life of your investments and helping your organization gracefully manage capacity fluctuations.

> [Service overview](https://aws.amazon.com/storagegatewas/)
