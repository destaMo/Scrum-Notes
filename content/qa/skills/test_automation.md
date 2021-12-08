+++
title = "Test automation"
+++

{{%bubble %}}

## Test automation

**Points:** 2

**Description:** You understand the value of test automation and can cover critical paths with automated scripts.

**Person who successfully completed requirement for given block can:**
- Compare manual and automated testing and differentiate in what cases each of them should be used
- Set up Cypress on a project from scratch
- Write executable automation tests that give a valuable information about state of particular features
- Create useful custom functions in terms of test automation
- Support grabbing website elements with CSS selectors
- Improve written tests by using requests and authentication token

{{% /bubble%}}

## **📦 Test automation**

### **🎓 Learn**

- 📗 [pros and cons of automating the tests](https://sumatosoft.com/blog-post/automation-testing-pros-cons)
- 📗 [manual vs automated tests](https://www.qamadness.com/manual-testing-vs-automated-testing/)
- 📗 [Cypress - get started](https://selleo.com/blog/how-to-get-started-with-cypress-a-simple-guide)
- 📗 [Cypress - writing your first test](https://docs.cypress.io/guides/getting-started/writing-your-first-test.html)
- 📗 [Cypress - custom commands](https://docs.cypress.io/api/cypress-api/custom-commands.html)
- 📙 [Cypress - querying elements](https://docs.cypress.io/guides/core-concepts/introduction-to-cypress.html#Querying-Elements)
- 📗 [Cypress - localStorage commands](https://www.npmjs.com/package/cypress-localstorage-commands)
- 📗 [Mocha snippets](https://marketplace.visualstudio.com/items?itemName=spoonscen.es6-mocha-snippets)
- 📗 [basic CSS selectors](https://docs.google.com/document/d/1VDdFmbDlmCj7N0mLGpgkX4rFkeNSxrG7DaQziCAt1U8/edit#heading=h.er22qrcb665g)
- 📙 [advanced CSS selectors](https://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048)
- 📙 [jQuery form selectors](https://api.jquery.com/category/selectors/form-selectors/)
- 📙 [jQuery tree traversal - children, closest, find, parent, parents, siblings](https://api.jquery.com/category/traversing/tree-traversal/)
- 📙 [jQuery filtering](https://api.jquery.com/category/traversing/filtering/)
- 📗 [Cypress - setting a token in localStorage](https://newbedev.com/in-cypress-set-a-token-in-localstorage-before-test)
- 📗 [Cypress - intercepting a request](https://egghead.io/blog/intercepting-network-requests-in-cypress)
- 📗 [Cypress - ignore uncaught exceptions](https://stackoverflow.com/questions/53845493/cypress-uncaught-assertion-error-despite-cy-onuncaughtexception)

### **🎤 Interview**

- What are the most important advantages and disadvantages of automated tests?
- Is manual or automated testing more important/efficient than the other one? Compare those two approaches
- What are some configurable options in Cypress?
- When should you create custom commands or functions? Provide some examples

### **📝 Katas**

- Set up Cypress or some other test automation framework from scratch
- Write and run a basic test case (e.g. logging in and some navigation)
- Write an example custom command (e.g. generating a unique ID, selecting filters)
- Use CSS selectors to refer to proper elements on a website
- Improve authentication so that Cypress does not need to login manually each time
- Solve a problem of creating an object with name that already exists
- Get authentication token and use it in created request (for example login)
- Show me what snippets you use
- Make sure that data you need to be loaded is actually loaded by intercepting a request and waiting for its response
- Show me how to ignore uncaught exceptions