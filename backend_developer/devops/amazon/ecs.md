# ECS

Amazon Elastic Container Service (ECS) is a highly scalable, fast, container management service that makes it easy to run, stop, and manage Docker containers on a cluster of Amazon EC2 instances.

- ECS eliminates the need to install, operate, and scale the cluster management infrastructure.
- ECS is a **regional** service that simplifies running application containers in a highly available manner across multiple AZs within a region
- ECS helps schedule the placement of containers across the cluster based on the resource needs and availability requirements.
- ECS allows integration of your own custom scheduler or third-party schedulers to meet business or application specific requirements.
- **Containers and Images**
  - Applications deployed on ECS must be architected to run in **docker containers**, which is a standardized unit of software development, containing everything that the software application needs to run: code, runtime, system tools, system libraries, etc.
  - Containers are created from a read-only template called an **image**.
  - Images are typically built from a Dockerfile, and stored in a **registry** from which they can be downloaded and run on your container instances.
  - ECS can be configured to access a private Docker image registry within a VPC, Docker Hub or is integrated with EC2 Container Registry (ECR)
- **Clusters**
  - Cluster is a logical grouping of EC2 container instances to run tasks using ECS
  - ECS downloads the container images from the specified registry, and runs those images on the container instances within your cluster.
- **Task Definition**
  - Task definition is a description of an application that contains one or more docker containers
  - Task definition is needed to prepare application to run on ECS
  - Task definition is a text file in JSON format that describes one or more containers that form your application.
  - Task definitions specify various parameters for the application, such as containers to use, their repositories, ports to be opened, and data volumes
- **Task and Scheduling**
  - A task is the instantiation of a task definition on a container instance within the cluster.
  - After a task definition is created for the application within ECS, you can specify the number of tasks that will run on the cluster.
  - ECS task scheduler is responsible for placing tasks on container instances, with several different scheduling options available
- **ECS Service**
  - ECS Service helps to run and maintain a specified number of instances of a task definition simultaneously.
- **Container Agent**
  - Container agent runs on each instance within an ECS cluster
  - Container Agent sends information about the instance’s current running tasks and resource utilization to ECS, and starts and stops tasks whenever it receives a request from ECS

## Use cases

- [microservices](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/common_use_cases.html#microservices)
  - auto scaling
  - service discovery
  - authorization and secrets management
  - logging
  - continuous integration and continuous deployment
- [batch jobs](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/common_use_cases.html#batch)

> [ECS overview](https://aws.amazon.com/ecs/)
