+++
aliases = ["nodejs-basics", "nestjs-basics"]
title = "NestJS - Basics"
weight = 1
+++

{{%bubble %}}

## Framework's Basics

**Points:** 2

**Description:** You can use the basic features of NestJS to deliver common features.

**Person who successfully completed requirement for given block can:**

- **deliver** simple and typical **functionalities** with **little to no additional help**,
- **present** the problem and explored **solutions clearly and in detail** when asking for help,
- **leverage** the most commonly used **standard library**'s capabilities,
- **use** known **packages and libraries**.

**Prerequisites:**

- [JavaScript's basics](../javascript/basics)
- [TypeScript's basics](../typescript/basics)
- [Persistence's basics](../../persistence/basics)

{{% /bubble%}}

## Areas

- Project setup
- Modules
- CRUD/Routing
- Dependency Injection
- Configuration
- Validation
- Authentication and Authorization
- Serialization
- Queueing

> **All katas listed below can be accomplished within scope of your sample NestJS application.**
>
> **You DO NOT need a separate code for that.**

---

## 📦 Project setup

Learn how to setup new NestJS application.

### 🎓 Learn

- 📗 [Setup NestJS Application](https://docs.nestjs.com/first-steps)
- 📗 [Performance](https://docs.nestjs.com/techniques/performance)

### 🎤 Interview

### 📝 Katas

- Setup fastify adapter for http server

---

## 📦 Modules

Learn about dividing applications into domain modules.

### 🎓 Learn

- 📗 [Modules](https://docs.nestjs.com/modules)
- 📗 [Dynamic Modules](https://docs.nestjs.com/fundamentals/dynamic-modules)
- 📗 [Circular Dependency](https://docs.nestjs.com/fundamentals/circular-dependency)

### 🎤 Interview

- Why is it useful to split application into modules?
- How to avoid `undefined` errors when dealing with circular dependencies (**Module A** importing **Module B** and vice versa)?
- What Dynamic Modules are useful for?

### 📝 Katas

- Create a module that:
  - depends on another module,
  - declares a controller,
  - declares a provider,
  - exports a provider.

---

## 📦 CRUD/Routing

Learn about routing and CRUD/REST.

### 🎓 Learn

- 📗 [Controllers](https://docs.nestjs.com/controllers)
- 📗 [Pipes](https://docs.nestjs.com/pipes)
- 📗 [Validation](https://docs.nestjs.com/techniques/validation)
- 📗 [Serialisation](https://docs.nestjs.com/techniques/serialization)

### 🎤 Interview

- What is a controller?
- What is Data Transfer Object (DTO) ?
- How can we receive DTO class instance instead of plain object?
- What is the difference between `PATCH` and `PUT` method (according to REST rules)?
- How would you access whole request body and single field from request body?
- How would you access all query params? What about single param?
- How would you access route paramteres?
- How to access library-specific request object?
- How to send a response using methods of underlying http library (express/fastify)?
- How to access library-specific response object without using it as a response to the request.
- What are pipes used for?
- What does it change to have `transform` option turned `on` in `ValidationPipe`

### 📝 Katas

- Create a controller contianing `GET`, `POST`, `PATCH` and `DELETE` actions
- Create a route that redirects user to another route. This can be simple alias for another route.
- Create a controller method that accepts a DTO in request body and validates it.
- Create a class represeting a response object (could be your database model) remove some of its fields (e.g. `password` field in `User` model) from response using `ClassSerializerInterceptor`
- Create a class represeting a response object and make it visible in a response for one controller, but remove it from response in another. (Hint: `@SerializeOptions()` decorator should help you)
- Create a DTO that accepts HTML input and sanitizes it.

---

## 📦 Dependency Injection

Learn about Inversion of Control and Dependency Injection.

### 🎓 Learn

- 📗 [Providers](https://docs.nestjs.com/providers)
- 📗 [Custom Providers](https://docs.nestjs.com/fundamentals/custom-providers)
- 📗 [Asynchronous Providers](https://docs.nestjs.com/fundamentals/async-providers)
- 📗 [Injecton Scopes](https://docs.nestjs.com/fundamentals/injection-scopes)

### 🎤 Interview

- How to create a custom provider?
- How to allow class to be injected to other services?
- What are use cases for following providers:
  - `useValue`
  - `useClass`
  - `useExisting`
  - `useFactory`
- What provider scopes do we have and how are they different?

### 📝 Katas

- Create an asynchronous provider that requires other services to be instantiated.
- Create a provider that uses `string` as a provider token and inject it in one of your providers.

---

## 📦 Configuration

Learn about accessing app configuration.

### 🎓 Learn

- 📗 [Configuration](https://docs.nestjs.com/techniques/configuration)

### 🎤 Interview

- What is the difference between `ConfigModule.forRoot` and `ConfigModule.forFeature`?
- Why would you use a partial registration for loading configuration for the application?
- How to access loaded env variables using `ConfigService`? How would you access them using partial config registartion?

### 📝 Katas

- Use partial config registration.
- Read config from `.env` file(s) and validate it.

---

## 📦 Authentication and Authorization

Learn about authenticating user and checking user access levels.

### 🎓 Learn

- 📗 [Guards](https://docs.nestjs.com/guards)
- 📗 [Authentication](https://docs.nestjs.com/security/authentication)
- 📗 [Authorization](https://docs.nestjs.com/security/authorization)
- 📗 [ExecutionContext](https://docs.nestjs.com/fundamentals/execution-context) - This chapter is optional except **Reflection and metadata** section (although other sections are highly recommended too!)

### 🎤 Interview

- What are guards in NestJS and what are they useful for?

### 📝 Katas

- Create a guard for username/password login.
- Create a guard for JWT login.
- Use guards that you created in different scopes (`globally` -> `in class` -> `in method`)
- Create a guard that can be disabled by marking route as public
- Create a guard that accepts only users with certain roles (for example `admin`)

---

## 📦 Queues and task scheduler

### 🎓 Learn

- 📗 [Queues](https://docs.nestjs.com/techniques/queues)
- 📗 [Task Scheduling](https://docs.nestjs.com/techniques/task-scheduling)

### 🎤 Interview

- What's the difference between queue and task scheduler?
- When should you use queue? When should you pick task scheduler?

### 📝 Katas

- Create a queue that sends welcome email to user after successful sign in.
- Create a task that runs every day.

---

## 📦 Testing

### 🎓 Learn

- 📗 [End-to-end testing](https://docs.nestjs.com/fundamentals/testing#end-to-end-testing)

### 🎤 Interview

- What is end-to-end test? What should this test cover?

### 📝 Katas

- Cover your application with end-to-end tests.

## 📝 Sample application

> Feel free to enhance/add new things in your application
>
> You can also create an application of your own which contains simillar functionalities (in terms of database relations and interactions with user).
>
> When in doubt, feel free to ask evaluator on this subject.

Create a **library** application consisting of following features:

- Authentication

  - User can register to application:
    - First name,
    - Last name,
    - Password,
    - Email.
  - Upon registration, user receives welcome email message.
  - User can log in to application using username/password.
  - User can see his account details (except password) when logged in.

- Authors

  - Only Admin can add author:
    - First name,
    - Last name,
    - Bio (short note about author).
  - Only Admin can edit author.
  - Only Admin can delete author.
  - Everyone can see author details (including **list of books**).
  - You can search through list of authors using his **first name** or **last name**.

- Books

  - Only Admin can add book:
    - Title,
    - Subtitle,
    - Description,
    - ISBN13,
    - Cover image,
    - Authors (at least one, can be multiple).
  - Only admin can edit book.
  - Only admin can delete book.
  - Everyone can see book details.
  - Everyone can search through list of books by **title**, **subtitle** and filter list of books by **authors**.

- Books supply

  - There can be multiple copies of one book.
  - Each copy must be uniquely identified.
  - Each copy must have it's status (**available**, **lost**, **borrowed**).
  - Only admin can change status of the book.

- Lending/Borrowing/Renting books

  - Anyone can borrow a book.
  - Each book copy should have its history of renting (when it was borrowed, by who, and when it was returned) - this history is only visible to admins.
  - After certain period (let's say 2 or 4 weeks) user who borrowed a book should be notified that he/she needs to return a copy soon.
  - Users cannot borrow copies that are **lost** or **borrowed**
  - Users can see history of their borrowing.

#### General requirements

- Use passport for authorization.
- Use queues library (like BullJS) to send emails.
- Use transactions to save records dependent on each other.
- Handle file upload and storage in application (filesystem, db, s3 - whatever you like).
- Write E2E tests for most crucial logic.

#### Glossary

- **Everyone** - every user and guest (someone that is not logged in)
- **User** - every logged in user (including admins)
- **Admin** - user with special, admin privileges
