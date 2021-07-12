+++
title = "Security"
+++

{{%bubble %}}

## Security

**Points:** 1

**Description:** You can explain the basic threats that every developer should keep in mind while developing a web application. You can apply all technics that prevents the most common security concerns.

**Person who successfully completed requirement for given block can:**

- Evaluate the state of the system from security perspective

{{% /bubble%}}

## Areas

**Security**

- OWASP
- Security Policies
- Security Protocols
- Workstation security

---


## 📦 Application Level Security

### 🎓 Learn
- 📗 [https://cve.mitre.org/](https://cve.mitre.org/)
- 📗 [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)
- 📗 [https://searchsecurity.techtarget.com/definition/two-factor-authentication](https://searchsecurity.techtarget.com/definition/two-factor-authentication)
- 📗 [https://www.synopsys.com/blogs/software-security/top-open-source-licenses/](https://www.synopsys.com/blogs/software-security/top-open-source-licenses/)
- 📗 [https://www.vaultproject.io/](https://www.vaultproject.io/)
- 📗 [https://www.cisco.com/c/en/us/solutions/small-business/resource-center/security/how-does-a-vpn-work.html](https://www.cisco.com/c/en/us/solutions/small-business/resource-center/security/how-does-a-vpn-work.html)
- 📗 [https://www.cloudflare.com/learning/ssl/how-does-ssl-work/](https://www.cloudflare.com/learning/ssl/how-does-ssl-work/)
- 📗 [https://frontendchecklist.io/](https://frontendchecklist.io/)


### 🎤 Interview

- What is OWASP?
- What are CVEs?
- Random questions about OWASP top 10 - be prepared ??
- What is 2FA, how it works and how we can leverage it our application?
- Why should we care about licenses?
- What kind of licenses can we use and which one should we avoid, what are the threats?
- How do you monitoring your application?
- How we can automaticly know if some of our dependencies is vulnarable?
- What is the policy of storing/managing secrets in your application?
- When would you consider using VPN in your architecture?
- What are the `.ignore` files and when we should use them?
- What is the SSL and how does it works?
- What are security checklists? How to use them?


### 📝 Katas
- Create examples form each of OWASP top 10 vulnarabilities in your framework/language of a choice, show the vulnarability and how to avoid it.
- Craete your secrets in [https://vault.selleo.dev/](https://vault.selleo.dev/ui/vault/secrets) show how you can safely use and manage them.

---

## 📦 Developer/Workstation Level Security

### 🎓 Learn

- 📗 [https://www.howtogeek.com/427982/how-to-encrypt-and-decrypt-files-with-gpg-on-linux/](https://www.howtogeek.com/427982/how-to-encrypt-and-decrypt-files-with-gpg-on-linux/)
- 📗 [https://www.csoonline.com/article/3247848/what-is-zero-trust-a-model-for-more-effective-security.html](https://www.csoonline.com/article/3247848/what-is-zero-trust-a-model-for-more-effective-security.html)
- 📗 [https://xkcd.com/936/](https://xkcd.com/936/)

### 🎤 Interview

- Should we use SSL for development environment?
- What is GPG and how we can use it in our daily job?
- What is your workflow when you finished the job for the client(the contract is fulfilled and you are moving to the next one)?
- How would you exchange critical data with your coworker?
- How can you validate the emails trustworthy?
- What is the way you access the internet? Do you have any policies?
- What is Zero Trust Policy?
- Do you have your own personal security checklist?
- Where do you store your backups, what they includes?
- How to create strong password?

### 📝 Katas

- Create selfsigned certificate for development purposes that is trusted on your local machine.
- Create a file with your name and share it with securely with GPG.
- Encrypt your disk on your workstation
- Enable 2FA authentication on most critical appcliations: GitHub, ZOHO, AWS, GCP, Heroku etc.
- Ensure there are no "dangling documet" with secret informations on your desk, office.

---

## 📦 Tools

- [https://www.vaultproject.io/](https://www.vaultproject.io/)
- [https://www.lastpass.com/](https://www.lastpass.com/)
- [https://1password.com/](https://1password.com/)
- [https://github.com/tfsec/tfsec](https://github.com/tfsec/tfsec)
- [https://github.com/aquasecurity/trivy](https://github.com/aquasecurity/trivy)
- [https://www.crowdstrike.com/](https://www.crowdstrike.com/)
- [https://www.fireeye.com/](https://www.fireeye.com/)
- [https://www.carbonblack.com](https://www.carbonblack.com/products-index/)
