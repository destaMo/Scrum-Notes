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

- Contract testing
- E2E
- Tests preparation and setup (including CI)

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

- What problems does contract testing solve?
- When would you suggest using contract testing?
- Describe consumer driven contract testing and compare it with regular contract testing.
- Is there any way to automate contract testing?
- How to deal with contract tests for versioned API?

### 📝 Katas

- Write a contract test when consumer and provider is controlled by you
- Write a contract test when consumer is controlled by you but provider is controlled by 3rd party (it should provide documentation allowing to describe a contract)

## 📦 E2E

### 🎓 Learn

- 📗 [Overview article](https://www.lambdatest.com/blog/all-you-need-to-know-about-end-to-end-testing/)
- 📙 [Cypress](https://www.cypress.io/)
- 📙 [Ember Testing guide](https://github.com/PoslinskiNet/ember-testing-guide) (acceptance section)

### 🎤 Interview

- List some cases which you dont want to tests in E2E
- What should you consider when setting up your E2E tests?
- Why and in which cases you would want to use mocked data in E2E tests?
- Name several cases where you would want to intercept requests/responses
- How to debug test runs?
- What are flaky tests and how to deal with them?

### 📝 Katas

- Write E2E test dealing with authorization programmatically (without using UI)
- Write a test for non-trivial form
- Write a test of app using real data

## 📦 Tooling / Test coverage

### 🎓 Learn

- 📗 [Stryker Mutator](https://stryker-mutator.io/docs/)
- 📗 [Mutant](https://github.com/mbj/mutant)

### 🎤 Interview

- Elaborate on code coverage reliability and usefulness - Code coverage in TDD
- How mutation tests can help to improve stability of the app

### 📝 Katas

- Setup code coverage monitoring tool on CI ensuring given coverage and no coverage drop
- Show usage of a mutation test using library of your choice

## 📦 Tooling / Continuous Integration/Deployment/Delivery

### 🎓 Learn

- 📗 [GH Actions](https://docs.github.com/en/actions)
- 📗 [Travis](https://docs.travis-ci.com/)
- 📗 [CircleCI](https://circleci.com/docs/)

### 🎤 Interview

- What should you consider when selecting CI for your test runs
- How could you speed up your test runs?

### 📝 Katas

- Setup and run your E2E and contract tests on CI of your choice
