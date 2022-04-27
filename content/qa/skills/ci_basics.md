+++
title = "CI basics"
+++

{{%bubble %}}

**Points:** 1

**Description:** You can include your end-to-end tests in a CI pipeline which you can prepare by yourself

**Person who successfully completed requirement for given block can:**
- Prepare a basic CI setup that runs their end-to-end tests
- Deal with encountered issues while implementing needed configuration
- Configure integration between repository and CI
- CircleCI is just a suggestion, you can use any other tool

{{% /bubble%}}

## **📦 CI basics**

### **🎓 Learn**
- 📙 [CircleCI - Cypress orb](https://circleci.com/developer/orbs/orb/cypress-io/cypress)
- 📙 [CircleCI - enabling GitHub checks](https://circleci.com/docs/2.0/enable-checks/)
- 📙 [Useful docker images](https://github.com/cypress-io/cypress-docker-images/tree/master/base)

### **🎤 Interview**
 - What is continuous integration? How does it help with the process of maintaining a good quality?
 - What are benefits of having CI setup, especially if any E2E tests exist?
 - What are some configurable options in Cypress orb?

### **📝 Katas**
 - Create a setup for CircleCI (e.g. on a forked repository with a simple E2E test)
 - Perform a success run on CircieCI
 - Perform a run on CircleCI with failing tests and show me how you can debug the issue (logs, screenshots, videos)
 - Enable GitHub checks and configure branch protection (set the CircleCI runs required before merge)
