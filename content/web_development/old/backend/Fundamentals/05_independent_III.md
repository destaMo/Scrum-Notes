# Indepedent - level III

## Areas

**Open discussion topics**

**Skills & practices**
- BDD
- Websockets
- FullText Search

**Misc**
- REST

**Tooling**
- SCA - Complexity / Security / Performance

**Laws and principles**
- ISP - Interfaces segregation principle
- Dependency Inversion Principle

**Patterns and Techniques**
- Pub/Sub
- Repository
- Null Object
- Proxy
- Builder
- Polymorphism

## 📦 Open discussion topics

**A selection of topics from the list below will be discussed during verification session**

* What is your list of top things/techniques to ensure high code quality and why?
* What do you think about metaprogramming?
* What patterns do you consider useful when writing backend MVC apps?
* What full-text search solution are you familiar with? In what cases would you use those solutions?
* What do you miss in [framework]? Where do you think [framework] is not the good fit?
* What do you think about project documentation?
* What are the anti-patterns when writing [framework] apps in your opinion?
* How would you deal with complex, legacy project that you need to work with, if it does not have adequate tests coverage?
* Are you familiar with concept of Test Induced Design Damage? What is your opinion on that? :poodle:
* How do you often deal with long running requests (i.e. generating documents)
* How would you describe “maintainable code”?
* If I was to write API only application in [language], what would be your recommendations / hints in relation to this task?
* What kinds of caching do you feel are the most useful when developing [framework] applications?
* If there is an information you need deep inside your code, but it is only accessible on top level (i.e. in controller), how would you approach propagating it (think “current_user”, but it can be anything else)
* What do you think about / where do you find application for JWT :poodle:
* What do you think about / where do you find application for Pub / Sub :poodle:
* What do you think about / where do you find application for UUIDs :poodle:
* What do you think about / where do you find application for WebSockets :poodle:
* Where do you find use for so-called "monorepo"s :poodle:

---

## 📦 Skills & practices / BDD

### 🎓 Learn

- "How to make the right thing"
- Behaviour Driven Development
- Focused on business logic / behaviour
  - In majority of cases on series on steps, instead of individual step
- Basically those can be treated as E2E Integration tests
  - Starts from UI/API/Scripts etc.
  - Ends on UI/API calls/Database/API Responses etc.
- Tools
  - Cucumber
  - Cypress
  - RSpec / Capybara
- Tend to be slow and a chore to build and update
  - Prefer testing primarily happy paths
  - Hard to test all side effects / edge cases
- Are (should be) usually readable for business people
- Consider writing after implementing a features, but before integrating (due to high cost)

## 📦 Pair programming

- Competence in TDD will be verified during pair programming session based on following requirements: https://gist.github.com/stevo/80aa460769fc4b90543994e0bc58ccc9
- Pairing session can take between 90 and 180 minutes, depending on developer efficiency.
- Developer can use any language/framework, but need to come prepared with a testing framework, database, application scaffolding etc. in place
- Aspects to be verified
    - Test driving implementation steps in small iterations
    - Building solution with Outside-in approach
    - Red-Green-Refactor cycle
    - Applying right design patterns to solve the problem defined
    - **Patterns to use may be imposed**
- Competence in BDD **may** be verified during pair programming session
    - Driving implementation by E2E testing
    - Iterative approach to building tests and implementation
    - Planning code without driving it with unit test (keeping tech debt under control)
    - Skills related to mocking/seeding entities on application boundaries (HTTP, Message Brokers, Database etc.)
    - Applying right techniques to keep the tests readability very high (even for non-technical people)
        - helpers around building application context (seeding, mocking)
        - custom matchers
    - Choosing which supplemental tests are necessary beside core e2e test to keep solution stable

### Typical task

- Drive implementation of following requirements BDD style (e2e tests).
- Assume application is integrated with "WhatADay" service.

1. Student creates a lesson for time when tutor is not available
1. Student sees, that lesson was rejected
1. Student creates a lesson for time when tutor is available
1. Student sees, that lesson was accepted
1. Tutor sees a new lesson created for him
1. Tutor cancels that lesson
1. Tutor no longer sees that lesson

### Resources

- [The BDD story](https://medium.com/p/the-bdd-story-fe82d6d4b24f)
- https://www.codecademy.com/articles/tdd-outside-in
- https://thoughtbot.com/blog/testing-from-the-outsidein
- https://iamalivingcontradiction.wordpress.com/2015/02/17/a-tale-of-two-approaches-inside-out-vs-outside-in-testing/
- https://www.toptal.com/freelance/your-boss-won-t-appreciate-tdd-try-bdd

## 📦 Skills & practices / Websockets

### 🎓 Learn

- Client-server communication protocol
  - Allows two-way (full-duplex) communication through established connection
  - Needs one HTTP request to establish connection / authenticate it
  - Each message integrity is ensured
  - WS/WSS
- Great for
  - Great alternative for polling
  - Real-time synchronisation (i.e. collaborative calendars, spreadsheets, documents)
  - Live feeds / Notifications
  - Games
  - Chats

### Resources

- https://blog.teamtreehouse.com/an-introduction-to-websockets
- https://www.youtube.com/watch?v=vQjiN8Qgs3c

## 📦 Skills & practices / FullText Search

### 🎓 Learn

- Effective searching data for text in large data stores through fine-grained indexing
- Engines
  - PGSearch
  - ElasticSearch
  - SOLR
- Capabilities
  - Scoring / Relevance sorting
  - Fuzzy-search
  - Spell-check
  - Type-ahead
  - Suggesters
  - Higlighting
- Refs
  - https://www.elastic.co/products/elasticsearch/features
  - https://www.joshgraham.com/full-text-search-explained/

## 📦 Misc / REST

### 🎓 Learn

- REpresenational State Transfer
- Set of constraints
  - Client-Server architecture (decoupled, stateless)
  - Resources identified by URL
  - Use nouns as resource name
  - Use verbs as manipulation

## 📦 Tooling / SCA - Complexity / Security / Performance

### Rails

- Brakeman
- RubyCritic
  - Nice to score between A and B
  - Churn vs Complexity may suggest violating SRP
- overcommit
- fasterer
- reek
- rubocop
- rails best practices
- bullet (n+1)
- CodeClimate

## 📦 Laws and principles / ISP - Interfaces segregation principle

### 🎓 Learn

- Consider exposing narrow interfaces
	- Can be violated by inheritance
	  - exposing dangerous methods
	- Composition over inheritance
	- Case for QueryObject returning relation
		- breaking output

### Resources

- https://thoughtbot.com/upcase/videos/interface-segregation-principle

## 📦 Laws and principles / Dependency Inversion Principle

### 🎓 Learn

- High level classes should not depend on low level classes, should depend abstractions (interfaces) instead.

- Dependency Injection / DIP / Inversion of control
  - DI into constructor - when the object makes no sense without dependency
  - DI into method - when dependency is only meaningful in context of given method

### Resources

- https://thoughtbot.com/upcase/videos/dependency-inversion-principle
- https://martinfowler.com/articles/dipInTheWild.html#YouMeanDependencyInversionRight
- https://thoughtbot.com/upcase/videos/invert-control

## 📦 Patterns and Techniques / Pub/Sub

### 🎓 Learn

- 📗 https://docs.google.com/document/d/1FVvYL4a2kH9Y9HE6wCyO4D3VRdmVdK5V-Mx8h_dVTwk/edit?usp=sharing
- 📗 https://hackernoon.com/observer-vs-pub-sub-pattern-50d3b27f838c

## 📦 Patterns and Techniques / Repository

### 🎓 Learn

- Layer separating object and its business logic from persistence layer
- `Repository.save(object)` vs `object.save`
- TODO: Todoist case, KAFKA/ES case
- Keeping clean interfaces and conventions is important when using repository

## 📦 Patterns and Techniques / Null Object

### 🎓 Learn

- Should match more or less interface object it represents
- `Guest` is an example of NullObject for user
- Can be helpful in maintaining LSP
  - `Receipt`
- Prevents conditional logic in some cases

### Resources

- https://github.com/thoughtbot-upcase-exercises/null-object-part-one
- https://github.com/thoughtbot-upcase-exercises/null-object-part-two
- https://sourcemaking.com/design_patterns/null_object

## 📦 Patterns and Techniques / Adapter

### 🎓 Learn

- Standardises / Changes interface to adapt them to different interface
  - Multiple clients / adapter / wrapper case

### Resources

- https://medium.com/@dljerome/design-patterns-in-ruby-adapter-89a482c26d8c
- https://refactoring.guru/design-patterns/adapter
- https://refactoring.guru/design-patterns/adapter/ruby/example
- https://sourcemaking.com/design_patterns/adapter

## 📦 Patterns and Techniques / Proxy

### 🎓 Learn

- Exposes same interface, but can add additional logic as caching/access control/logging

### Resources

- https://refactoring.guru/design-patterns/proxy
- https://refactoring.guru/design-patterns/proxy/ruby/example
- https://sourcemaking.com/design_patterns/proxy

## 📦 Patterns and Techniques / Builder

### 🎓 Learn

- Builder methods have to return `self` (object itself)
- Useseful as a object configuration mean
  - i.e. AREL, Mail builder
- Can replace long parameter lists
  - useful when arguments are based on conditional logic
- Correlated: Director pattern

### Resources

- https://refactoring.guru/design-patterns/builder
- https://refactoring.guru/design-patterns/builder/ruby/example
- https://medium.com/kkempin/builder-design-pattern-in-ruby-dfa2d557ff1b
- https://sourcemaking.com/design_patterns/builder

## 📦 Patterns and Techniques / Polymorphism

### 🎓 Learn

- Duck-typing in Ruby
- Generally - not caring about entity identity, but rather entity interface / API
- Polymorphism in Rails relations
