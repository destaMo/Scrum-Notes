# Junior - level I

## 📦 GIT CLI
* [GIT](/common/git.md)

## 📦 Authentication

- Authentication is NOT Authorization
- Basic methods
  - SSO (just a concept)
  - Simple Token
  - User / Password (HTTP Basic Authentication)
    - Base64 encoded and sent between requests
  - User / Password (Session based)
  - Libraries of choice

### 🎓 Resources

- 📗 https://blog.risingstack.com/web-authentication-methods-explained/
- 📗 [JWT Introduction](https://blog.risingstack.com/web-authentication-methods-explained)
- 📗 [SSO](https://auth0.com/blog/what-is-and-how-does-single-sign-on-work/)

#### Rails

- 📙 [Devise](https://github.com/plataformatec/devise)

#### NodeJS

- 📙 [PassportJs](http://www.passportjs.org)

## 📦 Pagination

### 🎓 Resources

- 📗 https://www.jackmarchant.com/articles/offset-and-cursor-pagination-explained

#### Rails

- 📙 [kaminari](https://github.com/kaminari/kaminari), [will_paginate](https://github.com/mislav/will_paginate), [pagy](https://github.com/ddnexus/pagy)

#### NodeJS

- 📙 [findAndCountAll](https://sequelize.org/master/class/lib/model.js~Model.html#static-method-findAndCountAll)

### 🎤 Interview

- What is it for (what problems does it solve)?
  1. Performance (DB Engine)
  1. UX
  1. Saving bandwidth
  1. Saving memory (server / client)
- Types
  - Limit / Offset
  - Cursor

## 📦 Filtering

### 🎓 Resources

- 📗 https://www.joshgraham.com/full-text-search-explained/

### Rails

- 📙 https://github.com/Casecommons/pg_search
- 📙 [Ransack](https://github.com/activerecord-hackery/ransack/) ([Demo](http://ransack-demo.herokuapp.com/))

### NodeJS

- 📙 https://medium.com/riipen-engineering/full-text-search-with-sequelize-and-postgresql-3572cb3093e7

### 🎤 Interview

- What is it for (what problems does it solve)?
  - UX driven (find what you are interested it)
- Using DB Engine vs using language
  - Performance (memory and CPU)
  - Complexity/Readability vs Performance
- Library of choice (how does it work and what does it offer?)
- Basics of what framework provides (ECTO, AREL, AR etc.)

## 📦 Sessions & Cookies

### 🎓 Resources

- 📗 https://blog.webf.zone/ultimate-guide-to-http-cookies-2aa3e083dbae

#### Rails

- 📙 https://www.theodinproject.com/courses/ruby-on-rails/lessons/sessions-cookies-and-authentication

#### NodeJS

- 📙 https://expressjs.com/en/resources/middleware/cookie-parser.html

### 🎤 Interview

- Cookies (client)
  - When does it expire?
  - Scoped (domain)
  - HTTP Only (non retrievable from JS)
  - Uses (settings scoped per machine/browser, tracking, session reference)
  - Size limit - 4KB
- Sessions (client or server)
  - What do we use it for?
    - Keeping resource authenticated
  - Storage options (redis, DB, cache. cookies, tempfile...)

## 📦 Single Responsibility Principle (SRP)

### 🎓 Resources

- 📗 https://thoughtbot.com/upcase/videos/single-responsibility-principle
- 📗 https://vimeo.com/157708450
- 📗 http://rcardin.github.io/solid/srp/programming/2017/12/31/srp-done-right.html

### 🎤 Interview

- Why?
  - Maintainable (easier to read, easier to modify, easier to test, less coupled)
  - Reusable (fragmented)
  - Do not overdo it! (cost of indirection)
- Measure SRP and decide if you accept what you have?
- Simply list what a class/object do - make sure it fits the encapsulating pattern
- 3-5 responsibilities is ok
  - REPL - 4 responsibilities
- Cohesion vs Adhesion
  - Cohesion - everything couple together (state)
  - Adhesion - it can be pulled from its scopes without affecting its other responsibilities
- Single (class of) reason to change

## 📦 Request / Response lifecycle

### 🎓 Resources

- 📗 https://www.rubypigeon.com/posts/examining-internals-of-rails-request-response-cycle/

#### Rails

- 📙 https://thoughtbot.com/upcase/videos/rack
- 📙 https://guides.rubyonrails.org/rails_on_rack.html
- 📙 https://www.railstutorial.org/book/beginning#sec-mvc

#### NodeJS

- 📙 https://itnext.io/a-new-and-better-mvc-pattern-for-node-express-478a95b09155
- 📙 https://medium.com/@TaylorAckley/simple-and-minimalist-mvc-architecture-pattern-for-node-express-cb542287a144

### 🎤 Interview

- What are the layers that requests travel through before you handle it and build response?
- What are the layers that response travels before it reaches browser?
- What is MVC?

## 📦 Form objects

- Form is basically oriented around
  - storing (logic)
  - attributes (types, defaults, validation)
- Representing abstract resources (i.e. contact form, search form, login screen)
- Simplified storing of many objects as one (custom persistence logic)
  - Good replacement for "nested attributes"
  - Not good for objects from multiple domains (using different stores)
- Place for conditional / contextualized validation logic
- Place for interface usable by actual forms (i.e. contextualized contents of dropdowns)
- Form is NOT good place for callbacks
  - Aggregate callbacks in Service Objects
- Replacement for strong attributes (in rails)

### 🎓 Resources

- 📗 https://medium.com/selleo/essential-rubyonrails-patterns-form-objects-b199aada6ec9
- 📗 https://thoughtbot.com/upcase/videos/form_objects

#### Rails

- 📙 https://github.com/Selleo/pattern#form
- 📙 https://dry-rb.org

#### NodeJS

- 📙 Write a form object from scratch

### 🎤 Interview

- What is a form object?
- Why would you use a form object?

## 📦 ActiveRecord

### 🎓 Resources

- 📗 [Martin Fowler on ActiveRecord pattern](https://www.martinfowler.com/eaaCatalog/activeRecord.html)
- 📗 [ORM - Wikipedia](https://en.wikipedia.org/wiki/Object-relational_mapping)
- 📗 [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)

#### Rails

- 📙 [ActiveRecord Basics](https://guides.rubyonrails.org/active_record_basics.html)

#### NodeJS

- 📙 [Sequelize ORM](https://sequelize.org/v5/)

### 🎤 Interview

- What is the difference between ORM and ActiveRecord?
    - ORM
        - Maps classes to tables
        - Maps object to records
        - Maps attributes to columns
- How do you understand CRUD?

## 📦 DRY

### 🎓 Resources

- 📗 Ruby examples - https://www.youtube.com/watch?v=lhXrO_ojc4k
- 📗 DRY principle explained - https://thevaluable.dev/dry-principle-cost-benefit-example/

### 🎤 Interview

- DRY (don't repeat yourself) How to decided if we should follow it?
  - If the likeliness of code change is high and if the likeliness of the SAME change in many place is high - prevents "shotgun surgery"
  - Can increase complexity and indirection (do not overdo it)
    - 2-3 times repetition might be ok
  - Techniques (selection)
    - Extract method
    - Pulling methods up (inheritance)
    - Mixins
    - Extending base classes
- WET (write everything twice)
  - If the likeliness of code change is high and if the likeliness of the DIFFERENT change in many place is high - prevents method pull-down when code diverges (accidental similarity)
  - Can increase readability and comprehensibility
  - Very useful in tests setup

## 📦 HTML

### 🎓 Resources

- 📗 https://devdocs.io/html/

### 🎤 Interview

- Explain/show examples of some of the tags:
    - `html`, `head`, `body`
    - `div`, `span`, tables (`table`, `thead`, `tbody`, `th`, `tr`, `td`), lists (`ul`, `ol`, `li`), headers, links, paragraphs + text formatting, forms, `class`/`id`/`data`

## 📦 Templating languages

### 🎓 Resources

#### Rails

- 📙 [ERB](https://apidock.com/ruby/ERB)
- 📙 [HAML](http://haml.info/)
- 📙 [SLIM](http://slim-lang.com/)
- 📙 [Liquid (templating language for users)](https://github.com/Shopify/liquid)
- 📙 [Handlebars](http://handlebarsjs.com/)

#### NodeJS

- 📙 [Pug](https://pugjs.org/api/getting-started.html)
- 📙 [Handlebars](http://handlebarsjs.com/)
- 📙 [LiquidJS](https://github.com/harttle/liquidjs)

#### Elixir

- 📙 [EEx](https://hexdocs.pm/eex/EEx.html)

### 🎤 Interview

- Discuss basics characteristics of some of the template languages that you know of

### 📝 Katas

- Use one of the template languages for displaying some interpolated data, e.g., customer info

## 📦 Indirection

### 🎓 Resources

- 📗 [Virtual Memory, Video 2: Indirection](https://www.youtube.com/watch?v=NMBdeP1thCA)
- 📗 ["Indirection" is using something that uses something else, in its broadest sense."](https://stackoverflow.com/questions/18003544/what-does-level-of-indirection-mean-in-david-wheelers-aphorism) / delegation

### 🎤 Interview

- What is indirection?
- What do you understand by that: *"Indirection" is using something that uses something else, in its broadest sense.*?

---

## 📦 Heroku

### 🎓 Resources

- 📗 https://devcenter.heroku.com/categories/reference

### 🎤 Interview

- What are the benefits
  - Easy of use and scale
  - Easy to add services
  - Pipelines
  - Stateless
  - Little configuration
- Disadvanteges
  - Pricey / Expensive
  - Stateless
- **[Independent 1]** Buildpacks

### 📝 Katas

- Setup your own app
- Explore resources from marketplace

## 📦 Debugging

### 🎓 Resources

#### Rails

- 📙 [pry-rails](https://github.com/rweng/pry-rails)

#### NodeJs

- 📙 [NDB](https://www.npmjs.com/package/ndb)
- 📙 [--inspect](https://nodejs.org/de/docs/guides/debugging-getting-started/#enable-inspector)

### 🎤 Interview

- Show your approach to debug a webapp

## 📦 PosgreSQL

### Filtering and projection

This is limited to basic usage of SELECT, WHERE and FROM.

#### 🎓 Resources

- 📗 https://www.postgresql.org/docs/11/sql-select.html
- 📗 https://www.postgresql.org/docs/11/queries-table-expressions.html
- 📗 https://www.postgresql.org/docs/11/queries-select-lists.html
- 📗 https://www.postgresql.org/docs/11/queries-values.html
- 📗 https://www.postgresql.org/docs/11/functions-comparison.html
- 📗 https://www.postgresql.org/docs/11/functions-matching.html

#### 🎤 Interview

- Tell me how do you use SELECT, WHERE and FROM.

### Retrieving portions of data

This is limited to the usage of LIMIT and OFFSET.

#### 🎓 Resources
- 📗 https://www.postgresql.org/docs/11/queries-limit.html

#### 🎤 Interview

- Tell me about LIMIT and OFFSET when querying the database.

### Simple joins

This is limited to the usage of INNER JOIN.

#### 🎓 Resources

- 📗 https://www.postgresql.org/docs/11/static/queries-table-expressions.html

#### 🎤 Interview

- Tell me why and how would I use INNER JOIN in the query.

### Sorting data

This is limited to ORDER BY.

#### 🎓 Resources

- 📗 https://www.postgresql.org/docs/11/static/queries-order.html

#### 🎤 Interview

- Teach me about "ORDER BY" for specifying order of queried data.

### Basic data types

This is limited to numeric, character, boolean and date time types.

#### 🎓 Resources

- 📗 https://www.postgresql.org/docs/11/static/datatype-numeric.html
- 📗 https://www.postgresql.org/docs/11/static/datatype-character.html
- 📗 https://www.postgresql.org/docs/11/static/datatype-boolean.html
- 📗 https://www.postgresql.org/docs/11/static/datatype-datetime.html

#### 🎤 Interview

- Tell me about the basic data types in PostgreSQL.
