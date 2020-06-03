# API Gateway

Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. With a few clicks in the AWS Management Console, you can create an API that acts as a “front door” for applications to access data, business logic, or functionality from your back-end services, such as workloads running on Amazon Elastic Compute Cloud (Amazon EC2), code running on AWS Lambda, or any web application.

Amazon API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, authorization and access control, monitoring, and API version management. Amazon API Gateway has no minimum fees or startup costs. You pay only for the API calls you receive and the amount of data transferred out.

- **performance**
  - With Amazon CloudFront integration, API Gateway allows you to take advantage of the worldwide network of edge locations to provide your end users with the lowest possible latency for API requests and responses. Amazon API Gateway also helps you manage traffic through throttling, so that back-end operations can withstand traffic spikes
- **easy to monitor**
  - API Gateway provides you with a dashboard to visually monitor calls to your services using Amazon CloudWatch
- **streamline api development**
  - API Gateway lets you simultaneously run multiple versions of the same API, allowing you to quickly iterate, test, and release new versions
- **flexible security**
  - use AWS administration and security tools, such as AWS Identity and Access Management (IAM) and Amazon Cognito, to authorize access to your APIs. Amazon API Gateway can verify signed API calls on your behalf using the same technology AWS uses for its own APIs. If you already use OAuth tokens or other authorization mechanisms, Amazon API Gateway can use AWS Lambda to execute a Lambda authorizer to help you verify incoming requests
- **create restful api endpoints for existing services**
  - With Amazon API Gateway, you can create modern resource based APIs, and then use the dynamic and flexible data transformation capabilities to generate the requests in the language your target services expect. API Gateway also helps you protect your existing services by setting throttling rules to avoid overwhelming your back-end infrastructure during unpredictable traffic spikes
- **keys for thrid-part developers**
  - API Gateway helps you manage the ecosystem of third-party developers accessing your APIs. You can create API keys on Amazon API Gateway, set fine-grained access permissions on each API key, and distribute them to third-party developers to access your APIs. You can also define plans that set throttling and request quota limits for each individual API key. The use of API keys is completely optional and must be enabled on a per-method level.

> [API Gateway overview](https://aws.amazon.com/api-gateway/)
