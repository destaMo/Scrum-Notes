# Data Pipeline

AWS Data Pipeline is a web service that helps you reliably process and move data between different AWS compute and storage services, as well as on-premises data sources, at specified intervals. With AWS Data Pipeline, you can regularly access your data where it’s stored, transform and process it at scale, and efficiently transfer the results to AWS services such as Amazon S3, Amazon RDS, Amazon DynamoDB, and Amazon EMR.

AWS Data Pipeline helps you easily create complex data processing workloads that are fault tolerant, repeatable, and highly available. You don’t have to worry about ensuring resource availability, managing inter-task dependencies, retrying transient failures or timeouts in individual tasks, or creating a failure notification system. AWS Data Pipeline also allows you to move and process data that was previously locked up in on-premises data silos.

- AWS Data Pipeline is a web service that makes it easy to automate and schedule regular data movement and data processing activities in AWS
- AWS Data Pipeline help define data-driven workflows
- AWS Data Pipeline integrates with on-premises and cloud-based storage systems to allow developers to use their data when they need it, where they want it, and in the required format.
- AWS Data Pipeline allows you to quickly define a pipeline, which defines a dependent chain of data sources, destinations, and predefined or custom data processing activities
- Based on a defined schedule, the pipeline regularly performs processing activities such as distributed data copy, SQL transforms, EMR applications, or custom scripts against destinations such as S3, RDS, or DynamoDB.
- By executing the scheduling, retry, and failure logic for the workflows as a highly scalable and fully managed service, Data Pipeline ensures that the pipelines are robust and highly available.

## AWS Data Pipeline features

- Distributed, fault-tolerant and highly available
- Managed workflow orchestration service for data-driven workflows
- Infrastructure management service, will provision and terminate resources as required
- Provides dependency resolution
- Can be scheduled
- Grants control over retries, including frequency and number
- Native integration with S3, DynamoDB, RDS, EMR, EC2 and Redshift
- Support for both AWS based and external on-premise resources

## AWS Data Pipeline Concepts

### Pipeline Definition

- Pipeline definition helps the business logic to be communicated to the AWS Data Pipeline
- Pipeline definition defines the location of data (Data Nodes), activities to be performed, the schedule, resources to run the activities, per-conditions and actions to be performed

### Pipeline Components, Instances, and Attempts

- Pipeline components represent the business logic of the pipeline and are represented by the different sections of a pipeline definition.
- Pipeline components specify the data sources, activities, schedule, and preconditions of the workflow
- When AWS Data Pipeline runs a pipeline, it compiles the pipeline components to create a set of actionable instances and contains all the information needed to perform a specific task
- Data Pipeline provides a durable and robust data management as it retries a failed operation depending on frequency & defined number for retries

### Task Runners

- A task runner is an application that polls AWS Data Pipeline for tasks and then performs those tasks
- When Task Runner is installed and configured,
  - it polls AWS Data Pipeline for tasks associated with activated pipelines
  - after a task is assigned to Task Runner, it performs that task and reports its status back to AWS Data Pipeline.
- A task is a discreet unit of work that the Data Pipeline service shares with a task runner and differs from a pipeline, which defines activities and resources that usually yields several tasks
- Tasks can be executed either on the AWS Data Pipeline managed or user managed resources

### Data Nodes

- Data Node defines the location and type of data that a pipeline activity uses as source (input) or destination (output)
- Data pipeline supports S3, Redshift, DynamoDB and SQL data nodes

### Databases

- Data Pipeline supports JDBC, RDS and Redshift database

### Activities

- An activity is a pipeline component that defines the work to perform
- Data Pipeline provides pre defined activities for common scenarios like sql transformation, data movement, hive queries etc
- Activities are extensible and can be used to run own custom scripts to support endless combinations

### Preconditions

- Precondition is a pipeline component containing conditional statements that must be satisfied (evaluated to True) before an activity can run
- A pipeline supports
  - System-managed preconditions
    - are run by the AWS Data Pipeline web service on your behalf and do not require a computational resource
    - Includes source data and keys check _for e.g. DynamoDB data, table exists or S3 key exists or prefix not empty_
  - User-managed preconditions
    - run on user defined and managed computational resources
    - Can be defined as Exists check or Shell command

### Resources

- A resource is the computational resource that performs the work that a pipeline activity specifies
- Data Pipeline supports AWS Data Pipeline-managed and self-managed resources
- AWS Data Pipeline-managed resources include EC2 and EMR, which are launched by the Data Pipeline service only when they’re needed
- Self managed on-premises resources can also be used, where a Task Runner package is installed which  continuously polls the AWS Data Pipeline service for work to perform
- Resources can run in the same region as their working data set or even on a region different than AWS Data Pipeline
- Resources launched by AWS Data Pipeline are counted within the resource limits and should be taken into account

### Actions

- Actions are steps that a pipeline takes when a certain event like success, failure occurs.
- Pipeline supports SNS notifications and termination action on resources

![GumGum](https://d1.awsstatic.com/architecture-diagrams/customers/gumgum-arch-diag.18a0f53f28019e7bab994c8e6dd28ff6eadf2e56.png)

> [Data Pipeline overview](https://aws.amazon.com/datapipeline/)
