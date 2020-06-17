# SNS

Amazon Simple Notification Service is a web service that enables applications, end-users, and devices to instantly send and receive notifications from the cloud.

Pub/Sub messaging and mobile notifications for microservices, distributed systems, and serverless applications.

- delivery or sending of messages to subscribing endpoints or clients
- **publisher-subscriber** model
- Producers and Consumers communicate **asynchronously** with subscribers by producing and sending a message to a topic
- supports **Email (plain or JSON), HTTP/HTTPS, SMS, SQS**
- supports **Mobile Push Notifications** to push notifications directly to mobile devices with services like Amazon Device Messaging (ADM), Apple Push Notification Service (APNS), Google Cloud Messaging (GCM) etc. supported
- **order is not guaranteed** and **No recall** available
- **integrated with Lambda** to invoke functions on notifications
- **for Email notifications, use SNS or SES directly, SQS does not work**

## Use scenarios

- Fanout

The "fanout" scenario is when an Amazon SNS message is sent to a topic and then replicated and pushed to multiple Amazon SQS queues, HTTP endpoints, or email addresses. This allows for parallel asynchronous processing. For example, you could develop an application that sends an Amazon SNS message to a topic whenever an order is placed for a product. Then, the Amazon SQS queues that are subscribed to that topic would receive identical notifications for the new order. The Amazon EC2 server instance attached to one of the queues could handle the processing or fulfillment of the order while the other server instance could be attached to a data warehouse for analysis of all orders received.

![sns-fanout](https://docs.aws.amazon.com/sns/latest/dg/images/sns-fanout.png)

Another way to use "fanout" is to replicate data sent to your production environment with your development environment. Expanding upon the previous example, you could subscribe yet another queue to the same topic for new incoming orders. Then, by attaching this new queue to your development environment, you could continue to improve and test your application using data received from your production environment. For more information about sending Amazon SNS messages to Amazon SQS queues, see [Sending Amazon SNS Messages to Amazon SQS Queues](https://docs.aws.amazon.com/sns/latest/dg/SendMessageToSQS.html). For more information about sending Amazon SNS messages to HTTP/S endpoints, see [Sending Amazon SNS Messages to HTTP/HTTPS Endpoints](https://docs.aws.amazon.com/sns/latest/dg/SendMessageToHttp.html).

- Application and System Alerts

Application and system alerts are notifications, triggered by predefined thresholds, sent to specified users by SMS and/or email. For example, since many AWS services use Amazon SNS, you can receive immediate notification when an event occurs, such as a specific change to your AWS Auto Scaling group.

- Push Email and Text Messaging

Push email and text messaging are two ways to transmit messages to individuals or groups via email and/or SMS. For example, you could use Amazon SNS to push targeted news headlines to subscribers by email or SMS. Upon receiving the email or SMS text, interested readers could then choose to learn more by visiting a website or launching an application. For more information about using Amazon SNS to send SMS notifications, see [Sending SMS Messages with Amazon SNS](https://docs.aws.amazon.com/sns/latest/dg/SMSMessages.html).

- Mobile Push Notifications

Mobile push notifications enable you to send messages directly to mobile apps. For example, you could use Amazon SNS for sending notifications to an app, indicating that an update is available. The notification message can include a link to download and install the update. For more information about using Amazon SNS to send direct notification messages to mobile endpoints, see [Amazon SNS Mobile Push Notifications](https://docs.aws.amazon.com/sns/latest/dg/SNSMobilePush.html)

- Message Durability

Amazon SNS provides durable storage of all messages that it receives. When Amazon SNS receives your Publish request, it stores multiple copies of your message to disk. Before Amazon SNS confirms to you that it received your request, it stores the message in multiple isolated locations known as _Availability Zones_. The message is stored in Availability Zones that are located within your chosen AWS Region, such as the US East (N. Virginia) Region. Although rare, should a failure occur in one Availability Zone, Amazon SNS remains operational, and the durability of your messages persists.

> [Service overview](https://aws.amazon.com/sns/)
