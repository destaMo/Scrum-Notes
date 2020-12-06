# CodeDeploy

AWS CodeDeploy is a deployment service that automates application deployments to Amazon EC2 instances, on-premises instances, or serverless Lambda functions.

You can deploy a nearly unlimited variety of application content, such as code, serverless AWS Lambda functions, web and configuration files, executables, packages, scripts, multimedia files, and so on. AWS CodeDeploy can deploy application content that runs on a server and is stored in Amazon S3 buckets, GitHub repositories, or Bitbucket repositories. AWS CodeDeploy can also deploy a serverless Lambda function. You do not need to make changes to your existing code before you can use AWS CodeDeploy.

AWS CodeDeploy makes it easier for you to:

- Rapidly release new features.
- Update AWS Lambda function versions.
- Avoid downtime during application deployment.
- Handle the complexity of updating your applications, without many of the risks associated with error-prone manual deployments

CodeDeploy is able to deploy applications to two compute platforms:

- **EC2/On-Premises**: Describes instances of physical servers that can be Amazon EC2 cloud instances, on-premises servers, or both. Applications created using the EC2/On-Premises compute platform can be composed of executable files, configuration files, images, and more.

- **AWS Lambda**: Used to deploy applications that consist of updated versions of Lambda functions. AWS Lambda manages the Lambda functions in a serverless compute environment made up of a high-availability compute structure. All administration of the compute resources is performed by AWS Lambda. For more information, see [Serverless Computing and Applications](https://aws.amazon.com/serverless/). For more information about AWS Lambda and Lambda functions, see [AWS Lambda](#lambda).

> [CodeDeploy overview](https://aws.amazon.com/codedeploy/)
