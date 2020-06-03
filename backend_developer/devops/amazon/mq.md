# MQ

Amazon MQ is a managed message broker service for Apache ActiveMQ that makes it easy to set up and operate message brokers in the cloud. Message brokers allow different software systems–often using different programming languages, and on different platforms–to communicate and exchange information. Messaging is the communications backbone that connects and integrates the components of distributed applications, such as order processing, inventory management, and order fulfillment for e-commerce. Amazon MQ manages the administration and maintenance of ActiveMQ, a popular open-source message broker. The underlying infrastructure is automatically provisioned for high availability and message durability to support the reliability of your applications. With Amazon MQ, you get direct access to the ActiveMQ console and industry standard APIs and protocols for messaging, including JMS, NMS, AMQP, STOMP, MQTT, and WebSocket. You can easily move from any message broker that uses these standards to Amazon MQ because you don’t have to rewrite any messaging code in your applications.

Amazon MQ, Amazon SQS, and Amazon SNS are messaging services that are suitable for anyone from startups to enterprises. If you're using messaging with existing applications, and want to move your messaging to the cloud quickly and easily, we recommend you consider Amazon MQ. It supports industry-standard APIs and protocols so you can switch from any standards-based message broker to Amazon MQ without rewriting the messaging code in your applications. If you are building brand new applications in the cloud, we recommend you consider Amazon SQS and Amazon SNS. Amazon SQS and SNS are lightweight, fully managed message queue and topic services that scale almost infinitely and provide simple, easy-to-use APIs. You can use Amazon SQS and SNS to decouple and scale microservices, distributed systems, and serverless applications, and improve reliability.

Amazon MQ provides a managed message broker service that takes care of operating ActiveMQ, including broker set up, monitoring, maintenance, and provisioning the underlying infrastructure for high availability and durability. You may want to consider Amazon MQ when you want to offload operational overhead and associated costs. If you want greater control in order to customize features and configurations or to use custom ActiveMQ plugins, you may want to consider installing and running ActiveMQ on Amazon EC2 directly.

## Use scenarios

Any application that runs on an AWS compute service, such as Amazon EC2, Amazon ECS, or AWS Lambda, can use Amazon MQ. Amazon MQ is also integrated with the following AWS services:

- Amazon CloudWatch - monitor metrics and generate alarms
- Amazon CloudWatch Logs - publish logs from your Amazon MQ brokers to Amazon CloudWatch Logs
- AWS CloudTrail - log, continously monitor, and retain Amazon MQ API calls
- AWS CloudFormation - automate the process of creating, updating, and deleting message brokers
- AWS Identity and Access Management (IAM) - authentication and authorization of the service API

> [Amazon-MQ overview](https://aws.amazon.com/amazon-mq/)
