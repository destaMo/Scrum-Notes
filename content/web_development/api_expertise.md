+++
title = "API Expertise"
+++

{{%bubble %}}

## API Expertise

**Points:** 2 

**Description:** You can build (or mock) & use standarized APIs as well as document your own API.

**Person which succesfully completed requirement for given block can:** 

- Compare, choose and confidently justify the right API building standard for given use case
- Evaluate, recommend and implement the right tooling and way of documenting the API
- Deliver mocked APIs meeting given specification using the adequate tooling
- Design and apply (enforce / lint) API contracts 
- Name, explain, compare and apply a wide range of typically used API authentication/authorization strategies, including OAuth and JWT

{{% /bubble%}}

## Areas

**API Expertise**

- Types of APIs
- JSON API
- GraphQL
- Documentation
- Versioning
- Authorization
- Authentication

---

{{%todo %}}
## 📦 Types of APIs

### 🎓 Learn

### 🎤 Interview

### 📝 Katas
{{% /todo%}}

## 📦 JSON API

### 🎓 Learn

- 📗 [Documentation](https://jsonapi.org/)

### 🎤 Interview

- Explain role of `links`, `data`, `included`, `errors`
- Explain default structure of entity payload (`type`, `id`, `attributes` etc.)
- How to deal with pagination?
- How to deal with search?
- How to deal with sort?
- How to deal with includes?
- How to deal with errors?
- How to create/update/delete resource?
- What is the role of sparse fieldsets?
- What is the default valid header in JSON API spec?

### 📝 Katas

- Provide sample usage of `data` attribute

---

## 📦 GraphQL

### 🎓 Learn

- 📗 [Documentation](https://graphql.org/)
- 📗 [Spec](https://graphql.github.io/graphql-spec/)

### 🎤 Interview

- Explain the differences between REST-like APIs and GraphQL
- When GraphQL is a good fit for the application?

### 📝 Katas

- Show me and explain GraphQL consumer code in your application

---

## 📦 Authentication

## 📦 Skills & practices / Authorization

### 🎓 Learn

- 📗 [OAuth](https://oauth.net/)
- 📗 [JWT](https://jwt.io/)
- Authorization is a process of confirming if given identity (already authenticated) should have access to given resource
- Roles implementation
  - flags - simple, straight-forward, require extra column for each role (difficult to extend), easy to search and read. Nice when there are only two roles in the system.
  - enum - simple, straight-forward, quite easy to extend, easy to search and read. Nice when you have many roles and each user has only one.
  - relation based - i.e. rolify. Less performing (more complex SQL queries). More to difficult to filter read. Nice when you have many roles and each user can have many of those and you would like to configure and introduce new roles from UI level.
  - STI - Easy to search and read. Provide contextual place for role-based code out of the box. Hard to extend, as you need to introduce new class to handle it. Nice when you have limited number of roles and each user can have only one. Also when you need to contextualize some of your code per role.
  - Bit encoded - Works similarly to permission setting mechanism in UNIX systems. Each bit represents one role and roles are encoded as integer on DB level. Not easy to read and search, but very efficient to query for. Moderately difficult to extend (just add a new bit, still those need to be in order). Nice when you have many roles and each user can have many of those and you do not need to introduce new ones from UI.

### 🎤 Interview

- Explain JWT
- Should you use cookies for authentication and if yes then when?
- Explain the concept of expired token
- Explain basics of OAuth

### 📝 Katas

- Show me your sample usage of OAuth

---

## 📦 Authorization

### 🎓 Learn

- 📗 [RBAC example in React](https://auth0.com/blog/role-based-access-control-rbac-and-react-apps/)
- 📗 [RBAC example in Ember](https://github.com/minutebase/ember-can)

### 🎤 Interview

- What authorization strategy are you using in your apps?

### 📝 Katas

- Present sample usage of yours RBAC-driven app

---