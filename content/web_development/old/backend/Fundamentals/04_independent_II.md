# Independent - level II

## Areas

**Skills & practices**

- Test driven development (TDD)
- Test doubles
- API Integration (patterns, recommendations and testing)
- Error/Exception handling

**Misc**
- UUID
- Reflection
- Introspection

**Tooling**
- Test coverage
- Continuous Integration/Deployment/Delivery
- Error reporting

**Laws and principles**
- Open-closed principle
- Composition over Inheritance
- Tell, don't ask principle

**Patterns and Techniques**
- Clients
- Wrappers / Facades
- Value object
- Factories (testing)
- State Machine
- Dependency Injection

## 📦 Skills & practices / Test driven development (TDD)

### 🎓 Learn

- "How to make the thing right" (TDD) vs "How to make the right thing" (BDD)
- Always see your test fail the right way
  - red/green/refactor loop
  - small development iterations
  - break code to ensure that "natural-greens" test the correct thing (limit false-positives)
- for every context prefer introducing counter-context
- benefits/costs of TDD
  - when not to TDD (i.e. one-off jobs, scripts, datafixes, migrations - code not used by main application)
  - 📗 [Tests-induced design damage](https://dhh.dk/2014/test-induced-design-damage.html) (when focusing on code testability results in overcomplicated solutions)
  - TDD often guides good architecture and helps ensuring long-term stability and extensibility (by keeping tech debt under control)
  - we add only what we need - not too much and not too little
- basic types of tests we use
    - unit tests
    - integration tests
    - feature tests
    - end-to-end tests
    - smoke tests
    - performance/load/stress/volume(...) tests (i.e. how system behave under some specific/maximum/peak load, lots of data, query count, code benchmarking)
- inside-out (pre-planned implementation architecture)
    - great for problems that need algorithmical solution where specification is unlikely to change much
    - results in highly optimised solution and tests
    - also results in soldified solution, that may be difficult to change or refactor for reuse
    - requires skills in planning implementation of solutions for complex problems
- outside-in (implementation architecture planned on-the-fly)
    - great for "simple" problems (process oriented) where specification may be likely to change
    - results in not overcomplicated, elastic-for-refactoring solution
    - does not require sophisticated skills in planning implementation architecture
    - applied to problem that requires algorithmical solution can result in ugly, complex, hard to understand and inefficient code
- going out of sync between tests and code during refactoring (or even implementation) phase vs keeping all units fully tested


## 📦 Skills & practices / Test doubles

### 🎓 Learn

- **Stubs**: these are used to replace a method call with a predefined return value. It’s the simplest use case;
- **Mocks**: responsible for the “real” magic of BDD, these are like stubs that can also record the interactions and messages received. Then, after the test runs, they can check whether the specified messages were received (including the number of times a message was received and the arguments passed in);
- **Spies**: these are like mocks, the difference here is that with mocks you write a expectation, then invoke the code that should (or should not) trigger it. With spies you keep the “normal” testing flow of invoking the code and then checking for the interactions (like the traditional assertions);
- **Fakes**: simpler versions of complex objects, generally “hand crafted” (not using a special tool or framework) and used when the real code would cause the tests to be too slow, cumbersome or unreliable.

#### Rails
📗 [Source](https://www.sitepoint.com/solid-ruby-dependency-inversion-principle/)

## 📦 Skills & practices / API Integration (patterns, recommendations and testing)

### 🎓 Learn

- Research the API
  - what API allows (capabilities)
  - look for patterns in API structure
  - does it adhere to any standard
  - completeness and quality of documentation
  - demo/sandbox accounts
  - limits (i.e. throttling)
  - how errors are returned
  - how pagination is handled
- Look for existing clients provided by vendor or community before rolling out your own
  - check how often it is updated/maintained so you are safe if/when API changes
- `Client` and `Facade` (`Wrapper`) patterns are useful in the context of integrating APIs (refer to their descriptions in this document)
- Testing API integrations
    - Mocking clients
        - Especially when we have implemented client library ourselves
    - mocking request
        - Webmock
            - especially for well documented APIs (copy&paste straight from documentation)
            - ...and testing API Client classes
        - VCR (recording responses)
            - for large responses (that would render tests unreadable)
            - for responses consisting of lots of irrelevant data (i.e. non-documented APIs, scraping)
            - smoke tests (especially when coupled with "expiring cassettes")
            - sequenced calls
    - using real connections to real services
        - useful in context of smoke specs
        - sandboxes can also be leveraged if available (need to be aware, that some sandboxes can go out-of-sync with their parent applications)
    - using real connections to fake services
        - i.e. locally set up servers, sandboxes or services mimicking original service behaviour
        - especially useful for frontend development

## 📦 Skills & practices / Error/Exception handling

### 🎓 Learn

- Ensuring code to be executed if exceptions was raised
  - i.e. to close critical connections to prevent memory leaks, connection saturation
- Consider re-raising rescuable exceptions in given context to prevent bubbling exception from lower-level libraries (to prevent discrete coupling)
- Leverage error names to allow for better targetting and/or grouping of specific errors
- Retry strategies
  - custom (i.e. new token retrieval or throttling handling)
  - delaying (i.e. for handling random errors like connection drop)
  - consider retry counter to prevent infinite-retry
- Transactional processes
  - "payment already sent" - idempotency handling (by key) / refunding
  - "notification already sent" - delaying/moving all notifications to the end of process
  - "objects already created" - leveraging 📙 [command pattern](https://refactoring.guru/design-patterns/command) to allow for reverting each of process stage
- Exceptions should not drive flow - exception are exceptions
- Services for error report aggregation: rollbar, sentry, airbrake, honeybadger...

#### Rails

  - `rescue nil` is forbidden ;)
  - never rescue from `Exception`
  - inherit from `StandardError`
  - leverage `rescue_from` in Controllers

## 📦 Misc / UUID

### 🎓 Learn

- Universally unique identifier
- Obfuscating sequenced ids
- Uniqueness between data stores
- Generating object id before it is persisted (i.e. for CQRS)
- 📗 [ULID](https://github.com/ulid/spec) - Lexicographically sortable

## 📦 Misc / Reflection

### 🎓 Learn
- Metaprogramming technique - reflecting textual class/methods representation to actual entity/message
- ex. State machine interaction by using UPDATE - Request "account" to "activate"
  - hey account what possible state changes do you support (introspection)
  - oh, you support activation... so I call `activate!` on you (reflection)

## 📦 Misc / Introspection

### 🎓 Learn
- Metaprogramming technique - Retrieving metadata of given code (i.e. hey, Product, what columns do you have)

## 📦 Tooling / Test coverage

- Does not reflect quality / quantity of test
- Does reflect how much code was executed during test execution
- TDD results in coverage is close to 100%
- SimpleCov as a tool of choice for Rails
- Test that may not be tested by choice (and may affect coverage)
  - Migrations
  - Data fixes
  - CLI Tools (rake tasks)
  - `/lib` that is outside of main app context - i.e. console tools / extensions
-  enforcing certain level, ensuring “no drop”

### Rails

- 📗 https://thoughtbot.com/upcase/videos/value-objects
- 📗 https://github.com/thoughtbot-upcase-exercises/extract-value-object

## 📦 Tooling / Continuous Integration/Deployment/Delivery

### 🎓 Learn
- Continuous integration
  - continuously integration with main branch
- Continuous delivery
  - deployment is manual
- Continuous deployment
  - continuously deploying application
- 📗 [Comparison](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)
- 📗 https://www.freecodecamp.org/news/the-real-difference-between-ci-and-cd/

### Tools

- TravisCI
- CircleCI

- Steps (examples)
  - Linting
  - Running tests
  - Smoke tests
  - Static code analysis
    - Security
    - Libraries are up to date

## 📦 Tooling / Error reporting

### 🎓 Learn

- Rollbar
- Sentry

## 📦 Laws and principles / Open-closed principle

### 🎓 Learn

- Opened for extension, closed for modification
- Ways to extend behavior
  - Monkey-patching
  - Instance based meta-programming
  - Inheritance
  - Dependency injection
    - Object
    - Anonymous functions / lambdas
- Is modification bad
  - private interface - ok
  - public interface - mostly ok, but your are still in control
  - published interface - additions are ok, modifications and removals are most likely not
- How to decide
  - Investigate your concrete dependencies
    - Make an educated guess about likelihood of change
    - Concrete dependencies can make total sense as effect of refactoring
  - Identify if you do base your logic on the type of dependency (it is open for modification this way)
- High "churn" may be indication of bad OCP violation
- Pure OCP
  - Plugin Architecture
  - DI Architecture

### Rails

- 📗 https://thoughtbot.com/upcase/videos/open-closed-principle

## 📦 Laws and principles / Composition over Inheritance

### 🎓 Learn

- Family (is a) vs friendship (has a)
- Inheritance
    - STI
    - Using full interface of parent class
    - **Shared** behaviour (module inclusion)
- Composition
  - High probability of logic differentiation
  - Changes in parent class may not be expected to affect child class
- Inheritance recommendations
    - Prefer delaying inheritance
    - Prefer flat inheritance
    - Prefer narrow inheritance
    - Both above increases chances of violating LSP (and hence polymorphism capability) and ISP (sort of security)

### Rails

- `include` is not composition
- 📗 https://thoughtbot.com/upcase/videos/composition-over-inheritance

## 📦 Laws and principles / Tell, don't ask principle

### 🎓 Learn

- Do not query an object and depend an action you perform on it based on this query result
- Patterns useful to counter that problem
  - Null object
  - Decorator / Presenter

### Examples

```ruby
  user.save if user.valid?
```

#### Rails

- 📗 https://thoughtbot.com/upcase/videos/tell-don-t-ask

## 📦 Patterns and Techniques / Clients

### 🎓 Learn

- Name after service/library we wrap
- Live close to the API of wrapped entity
- Methods reflect endpoint names
- Results should reflect responses of wrapped endpoints
  - Should not modify response to great extent
  - Light transformations are ok
- Provide references to wrapped endpoint (i.e. url to documentation page)
  - documentation can drive clients testing/implementation
  - it is a good idea to leverage request/response examples from documentation
- Keep Clients isolated from your main app
- Provide an instance Client users can work with
  - for reusing session/connection

### Rails
- 📗 [Selleo Way](https://medium.com/selleo/essential-rubyonrails-patterns-clients-and-wrappers-c19320bcda0)

## 📦 Patterns and Techniques / Wrappers / Facades

### 🎓 Learn
- Simplify interfaces of entities to facilitate wrapped entity usage within application
- Prefer wrapping other libraries
- Provide expressive naming for public methods
- Prefer using static methods
- Design responses in the useful way
- Keep Wrappers isolated from your main app
- Live close(r) to application (on conceptual level)

### Rails
- 📗 [Selleo Way](https://medium.com/selleo/essential-rubyonrails-patterns-clients-and-wrappers-c19320bcda0)

## 📦 Patterns and Techniques / Value object

### 🎓 Learn

- May be an answer to primitive obsession code smell
- Should be comparable
- Should be immutable
- examples: colors, currencies

## 📦 Patterns and Techniques / Factories (testing)

### 🎓 Learn

- Fixtures
  - used for large-scale data for used in integration testing
  - hard to find correlation between setup and assertion
  - may be difficult to maintain right correlations between tables and uniqueness
  - may be useful for testing large chunks of data (i.e. when testing views)
- Factories
  - easy to show correlation between setup and assertion
  - we can omit data irrelevant to test
  - factory by default should build minimal valid object (linting)
  - we should prefer building objects without persisting it (to conserve DB calls)
  - generating random data + factories can be used for seeding database

### Rails

- Factory Bot
    - 📗 [Defining](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#defining-factories) and [using](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#using-factories) factories (+ [building / creating multiple records](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#building-or-creating-multiple-records))
    - 📗 [Traits](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#traits)
    - 📗 [Dependent](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#dependent-attributes) and [transient](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#transient-attributes) attributes
    - 📗 [Sequences](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#sequences)
    - 📗 [Callbacks](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#callbacks)
    - 📗 [Custom construction](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#custom-construction) and [custom methods to persist objects](https://github.com/thoughtbot/factory_bot/blob/master/GETTING_STARTED.md#custom-methods-to-persist-objects)

## 📦 Patterns and Techniques / State Machine

### 🎓 Learn

- Example use case (orders, payments)
- Based on transition graph
- AASM in Rails
- Methods producing new types of objects
  - `NewUser` -> `ConfirmedUser` (https://www.youtube.com/watch?v=bwUueshN6Rw)
- Regular expression is built on top of transition graph

### Examples

- "3 days before checkin, 7 days before checkin"
- 📗 ["Dogs and robots"](https://www.youtube.com/watch?v=wfMtDGfHWpA)

## 📦 Patterns and Techniques / Dependency Injection

### 🎓 Learn

- Providing dependencies from outside
- To initialiser if an object makes no sense without dependency
- To method if a method makes no sense without dependency and dependency can change during object lifetime
