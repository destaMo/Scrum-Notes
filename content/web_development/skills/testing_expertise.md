+++
title = "Testing Expertise"
+++

{{%bubble %}}

## Testing Expertise

**Points:** 2

**Description:** You can use testing automation tools in critical area of the system, to increase the overall stability of the solution in terms of business requirements.

**Person who successfully completed requirements for given block can:**

- write maintainable, readable tests of all types
- utilize E2E & API Testing to maintain high stability
- propose a proper testing strategy for a given project
- automate the testing process via CI tools

{{% /bubble%}}

## Areas

**Skills & practices**

- Deep general knowledge about testing
- Contract testing
- E2E
- Tests preparation and setup (including CI)

**Tooling**

- Test coverage
- Test mutators

---

## 📦 Testing in general

### 🎤 Interview

- Explain extensively all the "what's" and "why's" in automated testing to a junior developer. (5-10mins of discussion)

## 📦 API Contract testing

### 🎓 Learn

- 📗 [Contract testing](https://pactflow.io/blog/what-is-contract-testing/)
- 📗 [Contract testing with Pact](https://www.youtube.com/watch?v=-6x6XBDf9sQ)
- 📗 [Consumer driven contract testing](https://medium.com/better-practices/consumer-driven-contract-testing-using-postman-f3580dba5370)
- 📙 [CDC in postman](https://youtu.be/Ynfr-y_1WRs)
- 📙 [E2E vs Contract testing](https://techbeacon.com/app-dev-testing/end-end-vs-contract-based-testing-how-choose)

### 🎤 Interview

- What problems does contract testing solves?
- When would you suggest using contract testing?
- Describe consumer driven contract testing and compare it with regular contract testing.
- What are the ways of automating contract testing?
- What are chellanges with testing versioned API in contract tests?

### 📝 Katas

- Write a contract test when consumer and provider is controlled by you
- Write a contract test when consumer is controlled by you but provider is controlled by 3rd party (it should provide documentation allowing to describe a contract)

## 📦 E2E

### 🎓 Learn

- 📗 [Overview article](https://www.lambdatest.com/blog/all-you-need-to-know-about-end-to-end-testing/)
- 📙 [Cypress](https://www.cypress.io/)
- 📙 [Ember Testing guide](https://github.com/PoslinskiNet/ember-testing-guide) (acceptance section)

### 🎤 Interview

- List some cases which you dont want to test in E2E
- How would you ensure the same database state before every test run?
- Why and in which cases you would want to use mocked data in E2E tests?
- Name several cases where you would want to intercept requests/responses
- How do you debug test runs?
- What are the typical reasons behind flakiness and how to deal with it?

### 📝 Katas

- Write E2E test dealing with authorization programmatically (without using UI)
- Cover a non trivial form (multiple inputs, validation, interdependent inputs) with e2e tests
- Cover a funtionality in app (may be your project) using real data with e2e tests

## 📦 Tooling / Test mutators and coverage

### 🎓 Learn

- 📗 [Stryker Mutator](https://stryker-mutator.io/docs/)
- 📗 [Mutant](https://github.com/mbj/mutant)
- 📗 [Instambul](https://istanbul.js.org/)

### 🎤 Interview

- Elaborate on code coverage reliability and usefulness
- How mutation tests can help with improving stability of the app?

### 📝 Katas

- Setup code coverage monitoring tool on CI ensuring given coverage and no coverage drop
- Show usage of a mutation test using library of your choice

## 📦 Tooling / Continuous Integration/Deployment/Delivery

### 🎓 Learn

- 📗 [GH Actions](https://docs.github.com/en/actions)
- 📗 [Travis](https://docs.travis-ci.com/)
- 📗 [CircleCI](https://circleci.com/docs/)

### 🎤 Interview

- What should you consider when selecting CI for your test runs?
- How could you speed up your test runs?

### 📝 Katas

- Setup and run your E2E and contract tests on CI of your choice
