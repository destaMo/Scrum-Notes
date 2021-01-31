+++
aliases = ["backend", "ror", "ruby", "rails", "junior"]
title = "Ruby/Ruby On Rails - Advanced"
weight = 2
+++

# Ruby on Rails - LEVEL 2

---

## Areas:

### Ruby On Rails:

- Framework Advanced Topics
- Testing Advanced Topics

---

## Ruby On Rails/ Framework Advanced Topics

In this section we will build more advanced features in our Rails application and learn how to answer more demanding technical interview questions.

### Learn

- [APIs comparison](https://dri.es/headless-cms-rest-vs-jsonapi-vs-graphql)
- [Rails Guides - caching](https://guides.rubyonrails.org/caching_with_rails.html)
- [Rails Guides - polymorphic-associations](https://guides.rubyonrails.org/association_basics.html#polymorphic-associations)
- [STI vs Polymorphic Associations](https://www.freecodecamp.org/news/single-table-inheritance-vs-polymorphic-associations-in-rails-af3a07a204f2/)
- [Thoughtbot - Polymorphism](https://thoughtbot.com/blog/back-to-basics-polymorphism-and-ruby)
- [sidekiq](https://github.com/mperham/sidekiq)
- [crontab](https://crontab.guru/)
- [Clients and Wrappers](https://medium.com/selleo/essential-rubyonrails-patterns-clients-and-wrappers-c19320bcda0)
- [Value Object](https://revs.runtime-revolution.com/value-objects-in-ruby-on-rails-9df64bc8db34)
- [Thoughtbot - Null Object](https://thoughtbot.com/blog/handling-associations-on-null-objects)
- [Pattern Matching](https://womanonrails.com/ruby-pattern-matching)
- [Ruby Data Structures](https://www.rubyguides.com/2019/04/ruby-data-structures/)
- [Refactoring - code smells](https://refactoring.guru/pl/refactoring/smells)
- [Design Patterns - Creational Patterns](https://refactoring.guru/design-patterns/creational-patterns)
- [Design Patterns - Structural Patterns](https://refactoring.guru/design-patterns/structural-patterns)
- [Design Patterns - Behavioral Patterns](https://refactoring.guru/design-patterns/behavioral-patterns)

### Interview

**IMPORTANT TOPICS FOR DISCUSSION:**

- "Composition over Inheritance" - explain what is it and what can happen when you neglect this principle?
- "Single-Table Inheritance vs. Polymorphic Associations" - explain when to use each of them, what kind of problems will they help you solve and what problems they can cause if you select wrong thing
- "Asynchronous processing" - what is it? What tools can you use to implement it? What are pros and cons of introducing asynchronous processing in your application? When to use it?
- "Caching" - what is it? Compare page/action/fragment/partial/low level caching? What are pros and cons of using caching in your application? When to use it?
- "JSON API vs GraphQL API vs REST API" - what are the pros and cons of using them? When will you suggest one over another?

**OTHER QUESTIONS:**

- How cache invalidation works in Rails?
- Where to store cache in rails? compare different solutions?
- What is ETag?
- List Sidekiq features that can be useful for you. How to get information that a task has been completed?
- What is CRON? Explain crontab syntax and its limitations.
- Compare Client and Wrapper.
- What is an Iterator? when should we use it, what problems does it solve for us?
- What is a Value Object? when should we use it, what problems does it solve for us?
- What is a Null Object, when should we use it, what problems does it solve for us?
- What is Sanitization? When can it be useful?
- What is pattern matching? When can it be useful?
- What does it mean that method is Deterministic?
- What is the difference between Continuous Delivery/Integration/Deployment?
- What is Dependency Injection?
- What are Websockets? For what types of features are they great?


- List and explain creational patterns. Which of them have you used?
- List and explain structural patterns. Which of them have you used?
- List and explain behavioral patterns. Which of them have you used?
- List code smells you know.


- Discuss tools you can use for test coverage and point advantages they can bring to the project?
- Discuss tools you can use for error reporting and point advantages they can bring to the project?
- Discuss tools you can use for static code analysis that are related to security?
- Discuss tools you can use for static code analysis that are related to complexity?


- What do you know about Microservices Oriented Architecture?
- Explain Optimistic / Pessimistic / Distributed locking
- What is Pub/Sub?
- What is a Message Broker?
- What is Idempotency?
- What is Eventual Consistency?
- What is Command/Query Responsibility Segregation? What advantages does it give?
- What is Domain-Driven Design? What advantages does it give? For what kind of projects it can/should be used?
- When to use JSON Web Tokens (JWT)?

### Katas

In all below steps use Test Driven Development. You can use an application from LEVEL 1 or add those features somewhere else.
Please DO NOT use any gems like active admin.
Please DO NOT waste your time on any styling :)
Important: use correct patterns when applicable!

- implement JSON API for resource that has has_many association
- implement simple GraphQL API for resource that has has_many association with simple mutations and queries
- implement 4 different types of caching
- use Polymorphism in your application
- use Single-Table Inheritance
- implement sidekiq in your application
- use third party API with the usage of Client and Wrapper
- use webhooks
- use websockets
- implement Iterator
- implement Value Object
- implement Null Object

---

## Ruby On Rails / Testing Advanced Topics

In this section we will understand BDD and learn how to test external and internal API.

### Learn

- [Applying BDD](https://medium.flatstack.com/applying-behavior-driven-development-to-ruby-on-rails-web-applications-using-rspec-cucumber-and-2c893c3ab7eb)
- [The BDD Story](https://medium.com/@blazejkosmowski/the-bdd-story-fe82d6d4b24f)
- [cucumber](https://cucumber.io/)
- [webmock](https://github.com/bblimke/webmock)
- [vcr](https://github.com/vcr/vcr)

### Interview

- Explain Behaviour Driven Development (BDD) and compare it to TDD
- Explain difference between inside-out and outside-in testing. Describe scenarios in which each is better than the other one?
- What is Cucumber?
- How to test internal API?
- How to test external API? What are the helpful gems that you can use?
- How to test webhooks?
