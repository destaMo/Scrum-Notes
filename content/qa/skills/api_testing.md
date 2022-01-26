+++
title = "API testing"
+++

{{%bubble %}}

## API testing

**Points:** 2

**Description:** You can test API structure and therefore simulate situations that are not testable from the UI level

**Person who successfully completed requirement for given block can:**


{{% /bubble%}}

## **📦 API testing**

### **🎓 Learn**
- 📗 [API testing basics](https://www.katalon.com/resources-center/blog/api-testing-tips/)
- 📗 [basics2](https://blog.testproject.io/2021/07/28/rest-api-automation-from-scratch/)
- 📗 [JSON schema - basics](https://json-schema.org/learn/getting-started-step-by-step.html)
- 📗 [JSON to "JSON schema" converter](https://www.liquid-technologies.com/online-json-to-schema-converter)
- 📗 [Destructive testing](https://www.sisense.com/blog/rest-api-testing-strategy-what-exactly-should-you-test/)
- 📙 [curl converter](https://curlconverter.com/) 
- 📗 [Postman](https://www.postman.com/)
- 📗 [Postman - variables](https://learning.postman.com/docs/sending-requests/variables/#understanding-variables)
- 📗 [Postman - snippets](https://learning.postman.com/docs/writing-scripts/test-scripts/)
- 📙 [Overriding  the HTTP method](https://www.oreilly.com/library/view/building-a-restful/9781785285714/ch05s05.html)
- 📙 [Fuzz testing](https://www.guru99.com/fuzz-testing.html)
- 📙 [Fuzz testing - some more](https://www.freecodecamp.org/news/whats-fuzzing-fuzz-testing-explained/)
- 📙 [Fuzz testing - setup in Postman](https://medium.com/@Magii/fuzzing-with-postman-599dce6317c7)
- 📙 [Fuzz testing - "Big list of naughty strings"](https://github.com/minimaxir/big-list-of-naughty-strings/blob/master/blns.json)




### **🎤  Interview**
- When should we perform API testing? What are the pros and cons?
- What does a request consist of?
- How to begin? What do you need before writing the tests?
- Tell me how you plan tests for particular endpoint based on provided business and technical requirements

### **📝 Katas**
- Create a request
- Organize your requests within a collection
- Handle authentication, e.g. using Bearer token
- Use collection variables, e.g. to set baseUrl or particular JSON schema
- Use JSON schema to validate response's structure (test mandatory fields and input format)
- Write tests veryfing status code (positive and negative scenarios)
- Write tests for CRUD happy path
- Write some examples of destructive testing
<!-- - ???? Write tests for file upload - chyba nie -->
- Run whole collection and analyse the report
- Show me how to schedule a regular test run
