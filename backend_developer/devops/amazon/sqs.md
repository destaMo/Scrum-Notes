# SQS

Amazon Simple Queue Service is a fully managed message queuing service that makes it easy to decouple and scale microservices, distributed systems, and serverless applications. Amazon SQS moves data between distributed application components and helps you decouple these components.

- extremely scalable queue service and potentially handles millions of messages
- helps build fault tolerant, distributed loosely coupled applications
- **stores copies of the messages on multiple servers** for redundancy and high availability
- guarantees **At-Least-Once Delivery**, but does notdd guarantee Exact One Time Delivery which might result in **duplicate** messages (Not true anymore with the introduction of FIFO queues)
- **does not maintain or guarantee message order**, and if needed sequencing information needs to be added to the message itself (Not true anymore with the introduction of FIFO queues)
- **supports multiple readers and writers** interacting with the same queue as the same time
- holds message for 4 days, by default, and can be changed from 1 min - 14 days after which the message is deleted
- message needs to be **explicitly deleted** by the consumer once processed
- allows send, receive and delete **batching** which helps club up to 10 messages in a single batch while charging price for a single message
- handles visibility of the message to multiple consumers using **Visibility Timeout**, where the message once read by a consumer is not visible to the other consumers till the timeout occurs
- can handle load and performance requirements by scaling the worker instances as the demand changes (**Job Observer pattern**)
- message sample allowing **short and long polling**
  - returns immediately **vs** waits for fixed time for e.g. 20 secs
  - might not return all messages as it samples a subset of servers **vs** returns all available messages
  - repetitive **vs** helps save cost with long connection
- supports **delay queues** to make messages available after a certain delay, can you used to differentiate from priority queues
- supports **dead letter queues**, to redirect messages which failed to process after certain attempts instead of being processed repeatedly
- **Design Patterns**
  - **Job Observer Pattern** can help coordinate number of EC2 instances with number of job requests (Queue Size) automatically thus Improving cost effectiveness and performance
  - **Priority Queue Pattern** can be used to setup different queues with different handling either by delayed queues or low scaling capacity for handling messages in lower priority queues

## Use scenarios

- [Standard Queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues.html)
  - Decouple live user requests from intensive background work - Let users upload media while resizing or encoding it.
  - Allocate tasks to multiple worker nodes - Process a high number of credit card validation requests.
  - Batch messages for future processing - Schedule multiple entries to be added to a database.
- [FIFO Queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html)
  - Ensure that user-entered commands are executed in the right order.
  - Display the correct product price by sending price modifications in the right order.
  - Prevent a student from enrolling in a course before registering for an account.
  - By default, FIFO queues support up to 3,000 messages per second with batching. To request a limit increase, file a support request.
  - FIFO queues support up to 300 messages per second (300 send, receive, or delete operations per second) without batching.

> [Service overview](https://aws.amazon.com/sqs/)
