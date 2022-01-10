+++
title = "API testing"
+++

{{%bubble %}}

## API testing

**Points:** 2

**Description:** You can test API structure and therefore simulate situations that are not testable from the UI level (coming on September 2021)

**Person who successfully completed requirement for given block can:**


{{% /bubble%}}

## **📦 API testing**

### **🎓 Learn**
- 📗 [API testing basics](https://www.katalon.com/resources-center/blog/api-testing-tips/)
- 📗 [basics2](https://blog.testproject.io/2021/07/28/rest-api-automation-from-scratch/)
- 📗 []()
- 📗 []()
- 📗 []()
- 📗 [devpath Selleo ??](https://selleo.com/devpath/web_development/skills/api_expertise/)
- 📙 [curl converter](https://curlconverter.com/) 
- JSON schema
- CI ??

### **🎤  Interview**
- When should we perform API testing? What are the pros and cons?
- What does a request contain?

### **📝 Katas**
- Create a request
- Organize your requests within a collection
- 


<!-- ------------------------ -->
* create requesta (import curl)
* Bearer token (firstly POST /login and set authToken in collection variable)
* 4 requests - CRUD
* set baseUrl
* JSON schema - empty URL with collectionVariable.set (generator https://www.liquid-technologies.com/online-json-to-schema-converter)
* then adjust generated schema to your needs, create GET and check how it works
* plan what needs to be tested in particular requests (check status, schema, what validations etc.)
* implement those tests
* run collection
