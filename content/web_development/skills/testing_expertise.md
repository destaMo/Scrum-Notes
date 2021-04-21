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
- Tests preparation and setup (including CI)
- Contract testing
- Dealing with unusual situations

**Tooling**

- Test coverage
---

## 📦 API Contract testing

### 🎓 Learn

- 📗 [Contract testing](https://pactflow.io/blog/what-is-contract-testing/)
- 📗 [Contract testing with Pact](https://www.youtube.com/watch?v=-6x6XBDf9sQ)
- 📗 [Consumer driven contract testing](https://medium.com/better-practices/consumer-driven-contract-testing-using-postman-f3580dba5370)
- 📙 [CDC in postman](https://youtu.be/Ynfr-y_1WRs)
- 📙 [E2E vs Contract testing](https://techbeacon.com/app-dev-testing/end-end-vs-contract-based-testing-how-choose)

### 🎤 Interview
- What is contract testing, when to use it?
- What is consumer driven contract testing
- What are the pros and cons of using contract testing?
- How to automate contract tests?

### 📝 Katas
 - TBD

## 📦 E2E

### 🎓 Learn

- 📗 [Overview article](https://www.lambdatest.com/blog/all-you-need-to-know-about-end-to-end-testing/)
- 📙 [Cypress](https://www.cypress.io/)
- 📙 [Ember Testing guide](https://github.com/PoslinskiNet/ember-testing-guide) (acceptance section)

### 🎤  Interview

- What should we test and avoid in E2E?
- How to deal with authorization in E2E tests?
- What are pros and cons of using mocked data over real data, when would you use it and why?
- How to work with requests (waiting/reading data/overwriting)?
- How to debug test runs?
- How would you prepare your app to run E2E tests on it?
  - How to deal with env setup?
  - How to deal with desired DB state?
  - How to deal with test users?
- What are and how to deal with flaky tests?

### 📝 Katas

- Present several acceptance tests and elaborate about them
- tests should utilize mocked request/response, interctions like clicking/typing/drag and drop

## 📦 Tooling / Test coverage

### 🎓 Learn
- Elaborate on code coverage reliability and usefulness
- Code coverage in TDD

### 📝  Katas
- Setup code coverage monitoring tool on CI ensuring given coverage and no coverage drop

## 📦 Tooling / Continuous Integration/Deployment/Delivery

### 🎓 Learn
- 📗 [GH Actions](https://docs.github.com/en/actions)
- 📗 [Travis](https://docs.travis-ci.com/)
- 📗 [CircleCI](https://circleci.com/docs/)


### 🎤 Interview
- What should you consider when selecting CI for your test runs
- How could you speed up your test runs?


### 📝  Katas
- Setup and run your E2E and contract tests on CI of your choice
