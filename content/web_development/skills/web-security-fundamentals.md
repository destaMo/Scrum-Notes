+++
title = "Web security fundamentals"
+++

{{%bubble %}}

## Fundamentals

**Description:** You understand *basic* security concepts around web development and the Web in general

**Rationale:**
You're at the beginning of your developer path. And you're here because you want to get better. Better at writting code. Better at finding programatic solutions to the business problems. But being better is not only quantified by being able to apply a programming pattern, writting performant code or a code that is easy to read and comperhend.

Being a good developer also means to be able to take additional perspectives while solving problems for your client. One of such perspective is to learn to write code that is not brittle when it comes to the security measures.

The skill we are talking about here is actually a combination of a know-how concerning the ways your code can be exploited by a hacker or a malicious user. And of course a proper mindset which allows you to avoid building solutions which are exploitable by (a flawed) design. 

**Person who successfully completed requirement for given block is:** 

A person who understands that the Internet is pretty much a wild world and there are bad guys out there. In the same time a person having conscience that with its craft, one can make that place better and safer for everyone.
Starting with not letting your client down, as a web developer. 

{{% /bubble%}}

## Areas

**Crash course to everything you should need to know about web security**

---

### 🎓 Learn (agnostic part)

- 📗 [OAuth in 6 minutes](https://www.youtube.com/watch?v=KT8ybowdyr0),
- 📗 [Three ways of storing data on the client side (for starters)](https://krishankantsinghal.medium.com/local-storage-vs-session-storage-vs-cookie-22655ff75a8)
- 📗 [HTTPS, TLS, SSL, and so on](https://kinsta.com/knowledgebase/tls-vs-ssl)
- 📗 [Oh, there is a padlock icon. I'm safe... NOT!](https://niebezpiecznik.pl/post/przestan-sprawdzac-czy-strony-maja-klodki/)
- 📗 [Did you know that you can actually browse cookies?](https://www.troyhunt.com/how-to-build-and-how-not-to-build/)
- 📗 [A few words as to where put your trust](https://www.codebyamir.com/blog/never-trust-data-from-the-browser)
- 📗 [Become a hacker yourself or just stop being naive with your solutions. How to get get behind a paywall](https://medium.datadriveninvestor.com/how-to-bypass-any-paywall-for-free-df87832cbff7)
- 📗 [The importance of secrets management](https://www.ekransystem.com/en/blog/secrets-management)

### 🎤 Interview

- Can you provide some examples of a sensitive data found in a web or mobile application? What makes such data "sensitive"?
- What's the original, intended use of OAuth? What kind of challenges OAuth authors tried to solve in the first place?
- Please provide a list different approaches to client side data storage. By focusing on localStorage, sessionStorage and Cookies explain if any of them is suitable and safe for storing sensitive data (including user passwords)?
- What is Token-Based Authentication? Why we are including tokens in the request headers and not for example login + password in order to authenticate a request made by an user?
- What's plain authentication? Does it have any weak points?
- Is it okay to send unencrypted password (as a plain text) over SSL/TLS? Justify your answer.
- Does your web / mobile framework provides you with any conventions which act as a safety net, making it harder for a developer to do stupid things (as far as the security is concerned)?
- What are the pros of basing your authentication / authorisation logic on a well estabilished library, instead of rolling on your own and building something from scratch?
- Are all Cookies secure? Is there a way for a non developer to access local storage or browse a Cookie?
- What the default approach for data input by the user and why? Should you trust it or not and why?
- What does it actually mean, when a website has a padlock icon next to the domain?
- How to take care of your personal and customer sensitive data i.e. SSH keys, 3rd API keys for integrations, AWS keys and rules?
- Can you describe the challenges for storing exchanging customer sensitive data inside the team? Which challenges described in the [secret management article](https://www.ekransystem.com/en/blog/secrets-management) are being solved by the tool like [quickforget](https://quickforget.com/)? And what kind of challenges are addressed by [Vault](https://www.vaultproject.io/)?

 ### 📝 Katas

 ##### 📗 The web framework of my choice is awesome, because it acts as my safety net:
 - Depending on your future development path please pick either
     - [Backend](https://guides.rubyonrails.org/security.html)
     - Frontend
         - [1](https://snyk.io/blog/10-react-security-best-practices/)
         - [2](https://relevant.software/blog/react-js-security-guide/)
 - and tell me about one cool thing you've learnt there.
 
 ##### 📗 Protecting yourself and others sometimes means that you have to pose a threat by yourself.
 📗 Imagine that your friend recommended you an article, that is behind a paywall. You're broke and can't afford to honestly pay the author, but the information in that article are essential for your survival. What could you possibly do to obtain such information (and why it's possible? Bonus points for covering all the JS, HTML and CSS)

---
