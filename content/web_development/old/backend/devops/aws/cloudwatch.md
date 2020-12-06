# CloudWatch

Amazon CloudWatch is a monitoring and management service built for developers, system operators.

- allows monitoring of AWS resources and applications in real time, collect and track pre configured or custom metrics and configure alarms to send notification or make resource changes based on defined rules
- **does not aggregate data across regions**
- **stores the log data indefinitely**, and the retention can be changed for each log group at any time
- **alarm history is stored for only 14 days**
- can be used an **alternative to S3 to store logs** with the ability to configure Alarms and generate metrics, however logs **cannot be made public**
- Alarms exist only in the created region and the Alarm actions must reside in the same region as well

## Use scenarios

- monitor EC2 instances
- monitor other AWS resources (EBS volumes, RDS, SQS, SNS)
- monitor custom metrics (e.g. performance of a simple API call)
- create CloudWatch alters
- monitor, store and access to a log file for EC2, Route53 and other resources

> [CloudWatch overview](https://aws.amazon.com/cloudwatch/)
