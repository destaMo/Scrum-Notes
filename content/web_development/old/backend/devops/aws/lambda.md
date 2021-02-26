# Lambda

AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume - there is no charge when your code is not running.

- *Serverless computing allows applications and services to be built and run without thinking about servers. With serverless computing, application still runs on servers, but all the server management is done by AWS.*
- Lambda is priced on a pay per use basis and there are no charges when the code is not running
- Lambda allows running of code for any type of application or backend service with zero administration
- Lambda performs all the operational and administrative activities on your behalf, including capacity provisioning, monitoring fleet health, applying security patches to the underlying compute resources, deploying code, running a web service front end, and monitoring and logging the code.
- Lambda does not provide access to the underlying compute infrastructure
- Scalability and availability
  - Lambda provides easy scaling and high availability to the code without additional effort on your part.
  - Lambda is designed to process events within milliseconds.
  - Latency will be higher immediately after a Lambda function is created, updated, or if it has not been used recently.
  - Lambda is designed to run many instances of the functions in parallel
  - Lambda is designed to use replication and redundancy to provide high availability for both the service and the Lambda functions it operates.
  - There are no maintenance windows or scheduled downtimes for either
  - For any Lambda function updates, there is a brief window of time, less then a minute, when requests would be served by both the versions
  - Lambda has a default safety throttle for number of concurrent executions per account per region
- Security
  - Lambda stores code in S3 and encrypts it at rest and performs additional integrity checks while the code is in use.
  - Each AWS Lambda function runs in its own isolated environment, with its own resources and file system view
- All calls made to AWS Lambda must complete execution within 300 seconds. Default timeout is 3 seconds. Timeout can be set the timeout to any value between 1 and 300 seconds.
- [AWS Step Functions](https://aws.amazon.com/step-functions/) can help coordinate a series of Lambda functions in a specific order. Multiple Lambda functions can be invoked sequentially, passing the output of one to the other, and/or in parallel, while the state is being maintain by Step Functions.
- [AWS X-Ray](https://aws.amazon.com/xray/) helps tracing for Lambda functions, which provides insights such as Lambda service overhead, function init time, and function execution time

## Use scenarios

- Using AWS Lambda with AWS services as event sources - _Event sources_ publish events that cause the Lambda function to be invoked. These can be AWS services such as Amazon S3. For more information and tutorials, see the following topics:
  - [Using AWS Lambda with Amazon S3](https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html)
  - [Using AWS Lambda with Kinesis](https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html)
  - [Using AWS Lambda with Amazon SQS](https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html)
  - [Using AWS Lambda with Amazon DynamoDB](https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html)
  - [Using AWS Lambda with AWS CloudTrail](https://docs.aws.amazon.com/lambda/latest/dg/with-cloudtrail.html)
  - [Using AWS Lambda with Amazon SNS from Different Accounts](https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html)
- On-demand Lambda function invocation over HTTPS (Amazon API Gateway) - In addition to invoking Lambda functions using event sources, you can also invoke your Lambda function over HTTPS. You can do this by defining a custom REST API and endpoint using API Gateway. For more information and a tutorial, see [Using AWS Lambda with Amazon API Gateway (On-Demand Over HTTPS)](https://docs.aws.amazon.com/lambda/latest/dg/with-on-demand-https.html).
- On-demand Lambda function invocation (build your own event sources using custom apps) - User applications such as client, mobile, or web applications can publish events and invoke Lambda functions using the AWS SDKs or AWS Mobile SDKs, such as the AWS Mobile SDK for Android. For more information and a tutorial, see [Getting Started](https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html) and [Using AWS Lambda as Mobile Application Backend (Custom Event Source: Android)](https://docs.aws.amazon.com/lambda/latest/dg/with-on-demand-custom-android.html)
- Scheduled events - You can also set up AWS Lambda to invoke your code on a regular, scheduled basis using the AWS Lambda console. You can specify a fixed rate (number of hours, days, or weeks) or you can specify a cron expression. For more information and a tutorial, see [Using AWS Lambda with Scheduled Events](https://docs.aws.amazon.com/lambda/latest/dg/with-scheduled-events.html).

> [Service overview](https://aws.amazon.com/lambda/)
