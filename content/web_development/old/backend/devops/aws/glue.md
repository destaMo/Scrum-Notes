# Glue

AWS Glue is a fully managed **extract**, **transform**, and **load** (ETL) service that makes it easy for customers to prepare and load their data for analytics. You can create and run an ETL job with a few clicks in the AWS Management Console. You simply point AWS Glue to your data stored on AWS, and AWS Glue discovers your data and stores the associated metadata (e.g. table definition and schema) in the AWS Glue Data Catalog. Once cataloged, your data is immediately searchable, queryable, and available for ETL. AWS Glue generates the code to execute your data transformations and data loading processes.

AWS Glue is integrated across a wide range of AWS services, meaning less hassle for you when onboarding. AWS Glue natively supports data stored in Amazon Aurora and all other Amazon RDS engines, Amazon DynamoDB, Amazon Redshift, and Amazon S3, as well as MySQL, Oracle, Microsoft SQL Server, and PostgreSQL databases in your Virtual Private Cloud (Amazon VPC) running on Amazon EC2. AWS Glue provides out-of-the-box integration with Amazon Athena, Amazon EMR, Amazon Redshift Spectrum, and any Apache Hive Metastore-compatible application.

AWS Glue is serverless. There is no infrastructure to provision or manage. AWS Glue handles provisioning, configuration, and scaling of the resources required to run your ETL jobs on a fully managed, scale-out Apache Spark environment. You pay only for the resources used while your jobs are running.

AWS Glue generates ETL code that is customizable, reusable, and portable, using familiar technology - Scala, Python, and Apache Spark. You can also import custom readers, writers and transformations into your AWS Glue ETL code.

## Use scenarios

- Queries S3 data lakes are an increasingly popular way to store and analyze both structured and unstructured data. If you use an Amazon S3 data lake, AWS Glue can make all your data immediately available for analytics without moving the data.

- Analyze Log Data in Your Data Warehouse (e.g. Redshift)

- Event-driven ETL Pipelines with Glue can run your ETL jobs based on an event, such as getting a new data set. For example, you can use an AWS Lambda function to trigger your ETL jobs to run as soon as new data becomes available in Amazon S3. You can also register this new dataset in the AWS Glue Data Catalog as part of your ETL jobs.

> [Glue overview](https://aws.amazon.com/glue/)
