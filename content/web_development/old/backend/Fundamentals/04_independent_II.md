# Independent - level II

## Areas

**Skills & practices**

- Error/Exception handling

**Misc**
- UUID
- Reflection
- Introspection

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
