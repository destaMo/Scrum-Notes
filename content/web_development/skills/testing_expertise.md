+++
title = "Testing Expertise"
+++

{{%bubble %}}

## Testing Expertise

**Points:** 2

**Description:** You can use testing automation tools in critical area of the system, to increase the overall stability of the solution in terms of business requirements.

**Person who successfully completed requirement for given block can:**

- write maintainable, readable tests of all types
- utilize E2E & API Testing to maintain high stability
- propose a proper testing strategy for the project
- automate the testing process via CI tools

{{% /bubble%}}

## Areas

**Skills & practices**

- E2E
- Contract testing
- Tests preparation and setup
- Dealing with unusual situations

**Tooling**

- Test coverage
- Continuous Integration/Deployment/Delivery

<<<<<<< HEAD
<<<<<<< HEAD
---

## 📦 Test driven development (TDD)

### 🎓 Learn

- Always see your test fail the right way
  - red/green/refactor loop
  - small development iterations
  - break code to ensure that "natural-greens" test the correct thing (limit false-positives)
- for every context prefer introducing counter-context
- benefits/costs of TDD
  - when not to TDD (i.e. one-off jobs, scripts, data fixes, migrations - code not used by main application)
  - 📗 [Tests-induced design damage](https://dhh.dk/2014/test-induced-design-damage.html) (when focusing on code testability results in overcomplicated solutions)
  - TDD often guides good architecture and helps ensuring long-term stability and extensibility (by keeping tech debt under control)
  - we add only what we need - not too much and not too little
- inside-out (pre-planned implementation architecture)
  - great for problems that need algorithmic solution where specification is unlikely to change much
  - results in highly optimised solution and tests
  - also results in solidified solution, that may be difficult to change or refactor for reuse
  - requires skills in planning implementation of solutions for complex problems
- outside-in (implementation architecture planned on-the-fly)
  - great for "simple" problems (process oriented) where specification may be likely to change
  - results in not overcomplicated, elastic-for-refactoring solution
  - does not require sophisticated skills in planning implementation architecture
  - applied to problem that requires algorithmic solution can result in ugly, complex, hard to understand and inefficient code
- going out of sync between tests and code during refactoring (or even implementation) phase vs keeping all units fully tested

=======
>>>>>>> Cleanup
=======
## 📦 E2E

### 🎓 Learn

- 📗 [Overview article](https://www.lambdatest.com/blog/all-you-need-to-know-about-end-to-end-testing/)
- 📙 [Cypress](https://www.cypress.io/)
- 📙 [Ember Testing guide](https://github.com/PoslinskiNet/ember-testing-guide) (acceptance section)
- 📙 [E2E vs Contract testing](https://techbeacon.com/app-dev-testing/end-end-vs-contract-based-testing-how-choose)

### 🎤 Interview

- How to deal with auth/JWT?
- What should we test and avoid in E2E?
- What is conditional testing and when is it helpful?
- What are pros and cons of using mocked data over real data, when would you use it and why?
- How to work with requests in tests (waiting/reading data/overwriting)?
- How to debug test runs?
- How would you prepare your app to run E2E tests on it?
- What are and how to deal with flaky tests?

### 📝 Katas

- Present several acceptance tests and elaborate about them
- ideally tests should utilize mocked request/response, interctions like clicking/typing/drag and drop

>>>>>>> WIP
## 📦 API Contract testing

### 🎓 Learn

- 📗 [Postman automated tests](https://medium.com/better-practices/from-manual-to-automated-testing-the-roadblocks-and-the-journey-6333dfacc5ae)
- 📗 [What is contract testing](https://pactflow.io/blog/what-is-contract-testing/)
- 📗 [Introduction to contract testing](https://blog.scottlogic.com/2019/01/07/introduction-to-contract-testing-part-1.html)

### 🎤 Interview

- What is consumer-driven contract testing?
- What tools would you use to automate contract testing?
- What is OpenApi 3.0 and how it can help you in tests?

<!-- - Research the API
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
<<<<<<< HEAD
    - especially useful for frontend development

## 📦 E2E

### 🎓 Learn

- 📗 [Overview article](https://www.lambdatest.com/blog/all-you-need-to-know-about-end-to-end-testing/)
- 📙 [Cypress](https://www.cypress.io/)
- 📙 [Ember Testing guide](https://github.com/PoslinskiNet/ember-testing-guide) (acceptance section)

### 🎤 Interview

- What should we test and avoid in E2E?
- What is conditional testing and when is it helpful?
- What are pros and cons of using mocked data over real data, when would you use it and why?
- How to work with requests (waiting/reading data/overwriting)?
- How to debug test runs?
- How would you prepare your app to run E2E tests on it?
- What are and how to deal with flaky tests?

### 📝 Katas

<<<<<<< HEAD
- Present your sample acceptance test and elaborate about it (it could be a test for the exercise from Local storage section)
=======
- Present several acceptance tests and elaborate about them
- ideally tests should utilize mocked request/response, interctions like clicking/typing/drag and drop
>>>>>>> Cleanup
=======
    - especially useful for frontend development -->
>>>>>>> WIP

<!-- ## 📦 Tooling / Test coverage

- Does not reflect quality / quantity of test
- Does reflect how much code was executed during test execution
- TDD results in coverage is close to 100%
- SimpleCov as a tool of choice for Rails
- Test that may not be tested by choice (and may affect coverage)
  - Migrations
  - Data fixes
  - CLI Tools (rake tasks)
  - `/lib` that is outside of main app context - i.e. console tools / extensions
- enforcing certain level, ensuring “no drop”

### Rails

- 📗 https://thoughtbot.com/upcase/videos/value-objects
- 📗 https://github.com/thoughtbot-upcase-exercises/extract-value-object -->

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
