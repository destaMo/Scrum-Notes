# EC2

Amazon Elastic Compute Cloud (EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers.

- provides **scalable computing capacity**
- **Features**
  - Virtual computing environments, known as **EC2 instances**
  - Preconfigured templates for EC2 instances, known as **Amazon Machine Images (AMIs)**, that package the bits needed for the server (including the operating system and additional software)
  - Various configurations of CPU, memory, storage, and networking capacity for your instances, known as **Instance types**
  - Secure login information for your instances using **key pairs** (public-private keys where private is kept by user)
  - Storage volumes for temporary data that’s deleted when you stop or terminate your instance, known as **Instance store volumes**
  - Persistent storage volumes for data using **Elastic Block Store (EBS)**
  - Multiple physical locations for your resources, such as instances and EBS volumes, known as **Regions and Availability Zones**
  - A firewall to specify the protocols, ports, and source IP ranges that can reach your instances using **Security Groups**
  - Static IP addresses, known as **Elastic IP addresses**
  - Metadata, known as **tags**, can be created and assigned to EC2 resources
  - Virtual networks that are logically isolated from the rest of the AWS cloud, and can optionally connect to on premises network, known as **Virtual private clouds (VPCs)**
- **Amazon Machine Image**
  - **template** from which EC2 instances can be launched quickly
  - **does NOT span across across regions**, and needs to be copied
  - **can be shared with other specific AWS accounts or made public**
- **Purchasing Option**
  - **On-Demand Instances**
    - pay for instances and compute capacity that you use by the hour
    - with **no long-term commitments** or **up-front payments**
  - **Reserved Instances**
    - provides **lower hourly running costs** by providing a billing discount
    - **capacity reservation** that is applied to instances
    - suited if **consistent, heavy, predictable usage**
    - **provides benefits with Consolidate Billing**
    - can be modified to **switch Availability Zones** or the **instance size within the same instance type**, given the instance size footprint (**Normalization factor**) remains the same
    - **pay for the entire term** regardless of the usage, so if the question targets cost effective solution and answer mentions reserved instances are purchased & unused, it can be ignored
  - **Spot Instances**
    - **cost-effective choice** but **does NOT guarantee availability**
    - **applications flexible in the timing** when they can run and also **able to handle interruption** by storing the state externally
    - AWS will give a **two minute warning** if the instance is to be terminated to save any unsaved work
  - **Dedicated Instances**, is a tenancy option which enables instances to run in VPC on hardware that’s isolated, dedicated to a single customer
  - **Light, Medium, and Heavy Utilization Reserved Instances are no longer available** for purchase and were part of the Previous Generation AWS EC2 purchasing model
- **Enhanced Networking**
  - results in **higher bandwidth, higher packet per second (PPS) performance, lower latency, consistency, scalability and lower jitter**
  - supported using **Single Root I/O Virtualization (SR-IOV)** only on supported instance types
  - is **supported only with an VPC (not EC2 Classic), HVM virtualization type** and available by default on Amazon AMI but can be installed on other AMIs as well
- **Placement Group**
  - provide **low latency, High Performance Computing** via 10Gbps network
  - is a logical grouping on instances within a Single AZ
  - **don’t span availability zones**, can span multiple subnets but subnets must be in the same AZ
  - **NOTE** - Spread Placement Groups can span multiple AZs.
  - **can span across peered VPCs** for the same Availability Zones
  - **existing instances cannot be moved into an existing placement group**
  - for **capacity errors, stop and start the instances** in the placement group
  - use **homogenous instance types** which support enhanced networking and **launch all the instances at once**

## Use scenarios

- hosting environments
- development and test environments
- backup and disaster recovery
- high performance computing

> [EC2 overview](https://aws.amazon.com/ec2/)
