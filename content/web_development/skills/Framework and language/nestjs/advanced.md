+++
aliases = ["nodejs-advanced", "nestjs-advanced"]
title = "NestJS - Advanced"
weight = 2
+++

{{%bubble %}}
**Points:** 2

**Description:** You can use advanced features of NestJS to deliver complex features.

**Person who successfully completed requirement for given block can:**

- Create complex NestJS applications with GraphQL support
- Understand dependency injection framework of NestJS
- Use external service providers with NestJS application
- Write unit tests for services

{{% /bubble%}}

## Areas

- Execution context and reflections
- Microservices
- Async Local Storage/Continuous Local Storage
- Validation
- Websockets
- Using cloud providers
- Lifecycle Events
- GraphQL
- Caching
- Unit testing

## 📦 Execution context and reflections

### 🎓 Learn

- 📗 [Exection context](https://docs.nestjs.com/fundamentals/execution-context) (this chapter includes reflections and metadata; please read it as well)

- What's the difference between `Reflector` methods: `get`, `getAllAndOverride`, `getAllAndMerge`?

### 📝 Katas

- Create a decorator that allows so store reflection metadata. Use that metadata later in one of your service, guard etc.

## 📦 Microservices

Create microservices with NestJS framework

### 🎓 Learn

- 📗 [Microservices](https://docs.nestjs.com/microservices/basics)
- 📗 [Monorepo Mode](https://docs.nestjs.com/cli/monorepo#monorepo-mode)

### 🎤 Interview

- What are benefits of monolithic architecture? What are downsides?
- Which transport service would you use to communicate with your service and why?
- When would you use microservice architecture? What are upsides and what are downsides?

### 📝 Katas

- Create an application that communicates with one external service you also created (for example: pdf generation service). Utilise monorepo structure.

## 📦 Async Local Storage/Continuous Local Storage

### 🎓 Learn

- 📗 [AsyncLocalStorage](https://nodejs.org/api/async_context.html#class-asynclocalstorage)
- 📗 [Accessing Request instance in non-nest providers](https://github.com/Papooch/nestjs-cls/blob/main/README.md)

### 🎤 Interview

- What are the use cases for Async Local Storage in NodeJS apps? Why do we sometimes need it for NestJS apps?

### 📝 Katas

- Using `NestJS-CLS` (or other similar tool) store information from the request (for example request id) and access it (even `console.log` will be enough) in one of your services.

## 📦 Validation

Use dependency injection in validator constraints

### 🎓 Learn

- 📗 [Custom validation with Database](https://dev.to/avantar/custom-validation-with-database-in-nestjs-gao)

### 📝 Katas

- Create a custom validator that checks against uniqueness of user email in database. Use dependency injection provided by NestJS.

## 📦 Websockets

### 🎓 Learn

- 📗 [A Beginner's Guide to WebSockets](https://www.youtube.com/watch?v=8ARodQ4Wlf4)
- 📗 [Websockets](https://docs.nestjs.com/websockets/gateways)
- 📗 [Using multiple nodes](https://socket.io/docs/v4/using-multiple-nodes)
- 📗 [Server-sent Events (NestJS)](https://docs.nestjs.com/techniques/server-sent-events)
- 📗 [Server-sent Events (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events)
- 📗 [Testing Socket.IO with jest](https://socket.io/docs/v4/testing/#example-with-jest)

### 🎤 Interview

- Why would you use WebSockets over HTTP? What are the advantages and what are the downsides?
- What is long polling? When would you use it as an alternative to websocket connection and why?
- What is sticky session? When do you need to apply it?
- What's the difference between WebSockets (WS) and Server-sent Events (SSE)?
- When would you use SSE and when WS?

## 📦 Using cloud providers

### 🎓 Learn

- 📗 [Uploading public files to S3](https://wanago.io/2020/08/03/api-nestjs-uploading-public-files-to-amazon-s3/)
- 📗 [Managing private files in S3](https://wanago.io/2020/08/10/api-nestjs-private-files-amazon-s3/)
- 📗 [Using Auth0 to manage user identity](https://auth0.com/blog/developing-a-secure-api-with-nestjs-adding-authorization/)

### 📝 Katas

- Create file uploader that stores files on `S3`. Allow user to access these files later (for example allow user to send album cover image and then when responding with album provide a link to this file in `S3`)
- Create an authorization flow using `AWS Cognito`, `Firebase`, `Supabase` or `Auth0`. If you need consultancy on how to solve managing users and relations on this, please don't hesitate to ask.
- What are upsides and downsides of verifying `JWT` using `JWT Secret` versus `JWKS`

## 📦 Lifecycle Events

Learn about lifecycle events in NestJS services

### 🎓 Learn

- 📗 [Lifecycle Events](https://docs.nestjs.com/fundamentals/lifecycle-events)

### 🎤 Interview

- Which events require you to enable shutdown hooks?
- For which kind of services a lifcecyle events are not being called?

### 📝 Katas

- Create a service that performs async operations upon service or application initialization.

## 📦 GraphQL

Learn to create GraphQL resolvers.

**When reading through following section please only consider Code-First approach!**

### 🎓 Learn

- 📗 [Resolvers](https://docs.nestjs.com/graphql/resolvers)
- 📗 [Mutations](https://docs.nestjs.com/graphql/mutations)
- 📗 [Subscriptions](https://docs.nestjs.com/graphql/subscriptions)
- 📗 [Unions and Enums](https://docs.nestjs.com/graphql/unions-and-enums)
- 📗 [Mapped Types](https://docs.nestjs.com/graphql/mapped-types)
- 📗 [Solving GraphQL n+1 problem](https://wanago.io/2021/02/08/api-nestjs-n-1-problem-graphql/)
- 📗 [Why you shouldn't use GrapHQL](https://blog.logrocket.com/why-you-shouldnt-use-graphql/)
- 📗 [GraphQL — Common Disadvantages Over REST and Solutions to Overcome them](https://levelup.gitconnected.com/graphql-common-disadvantages-over-rest-and-solutions-to-overcome-them-70cbaca42a44)

### 🎤 Interview

- What is `resolver`, `mutation` and `subscription`? How are they different?
- What are the limitations of GraphQL API (namely: downloading files and caching responses)? How would you work around them?

### 📝 Katas

> For all katas below try using code-first approach

- Create resolvers for two resources - both of these should be paginated.
  - As an additional excersise you can try using pagination with cursor instead of offset approach.
- Create a resolver with an extra field (using `ResolveField` decorator). Try avoiding `n+1` problem when fetching resources from database.
- Create a mutation for creating and updating a resource.
- Create a separate subscriptions that listen on creating any resource and updating/deleting particular resource (with specified id).
- Create an auth guard that can be used on GraphQL resolver/mutation.

## 📦 Caching

Familiarize yourself with response caching.

### 🎓 Learn

- 📗 [NestJS Caching](https://docs.nestjs.com/techniques/caching)

### 🎤 Interview

- What's the purpose of `caching`?

### 📝 Katas

- Implement at least one cached HTTP Route or Microservice/Websocket message response in your application.

## 📦 Unit Testing

Start writing unit tests for your services

### 🎓 Learn

- 📗 [Unit Testing](https://docs.nestjs.com/fundamentals/testing#unit-testing)
- 📗 [Testing Utilities](https://docs.nestjs.com/fundamentals/testing#testing-utilities)
- 📗 [Overriding globally registered enhancers#](https://docs.nestjs.com/fundamentals/testing#overriding-globally-registered-enhancers)
- 📗 [Testing request-scope instances](https://docs.nestjs.com/fundamentals/testing#testing-request-scoped-instances)
- 📗 [Testing NestJS with unit tests](https://wanago.io/2020/07/06/api-nestjs-unit-tests/)

### Interview

- What are `unit tests` useful for? When to use them, when to avoid them?

### Katas

- Write a unit tests for a service which:
  - depends on database Repository,
  - depends on config service/object,
  - depends on other service with mutliple dependencies.
