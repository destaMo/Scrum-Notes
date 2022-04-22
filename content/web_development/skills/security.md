+++
title = "Security"
+++

{{%bubble %}}

**Points:** 1

**Description:** You can explain the basic threats that every developer should keep in mind while developing a web application. You can apply all technics that prevent the most common security concerns.

**Person who completed requirement for the given block can:**

- Evaluate the state of the system from a security perspective

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
- Answer random questions around OWASP top 10
- What is 2FA, how it works and how we can leverage it in our applications?
- Why should we care about licenses?
- What kind of licenses can we use and which one should we avoid, what are the threats?
- How do you monitoring your application?
- How we can automatically know if some of our dependencies are vulnerable?
- What is the policy for storing/managing secrets in your application?
- When would you consider using VPN in your architecture?
- What are the `.ignore` files and when we should use them?
- What is the SSL and how does it work?
- What are security checklists? How to use them?


### 📝 Katas
- Create examples from each of OWASP's top 10 vulnerabilities in your framework/language of a choice, show the vulnerability and how to avoid it.
- Create your secrets in [https://vault.selleo.dev/](https://vault.selleo.dev/ui/vault/secrets) to show how you can safely use and manage them.

---

## 📦 Developer/Workstation Level Security

### 🎓 Learn

- 📗 [https://www.howtogeek.com/427982/how-to-encrypt-and-decrypt-files-with-gpg-on-linux/](https://www.howtogeek.com/427982/how-to-encrypt-and-decrypt-files-with-gpg-on-linux/)
- 📗 [https://www.csoonline.com/article/3247848/what-is-zero-trust-a-model-for-more-effective-security.html](https://www.csoonline.com/article/3247848/what-is-zero-trust-a-model-for-more-effective-security.html)
- 📗 [https://xkcd.com/936/](https://xkcd.com/936/)

### 🎤 Interview

- Should we use SSL for the development environment?
- What is GPG and how we can use it in our daily job?
- What is your workflow when you finished the job for the client(the contract is fulfilled and you are moving to the next one)?
- How would you exchange critical data with your coworker?
- How can you validate the email's trustworthiness?
- What is the way you access the internet? Do you have any policies?
- What is Zero Trust Policy?
- Do you have your security checklist?
- Where do you store your backups, what they include?
- How to create a strong password?

### 📝 Katas

- Create a self-signed certificate for development purposes that is trusted on your local machine.
- Create a file with your name and share it securely with GPG.
- Encrypt your disk on your workstation
- Enable 2FA authentication on most critical applications: GitHub, ZOHO, AWS, GCP, Heroku, etc.
- Ensure there are no "dangling documents" with secret information on your desk, office.

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
