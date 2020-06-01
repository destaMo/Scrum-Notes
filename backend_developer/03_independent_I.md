# Indepedent - level I

## Areas

**Skills & practices**

- Uploading files
- Asynchronous processing
- Regular expressions
- Caching
- Authorization

**Misc**

- Extract Method
- Extract Class
- Introduce Explaining Variable
- Sanitization
- (non) Deterministic

**Tooling**
- CRON
- Git: bisect 

**Laws and principles**
- LSP 

**Patterns and Techniques**
- Policies
- Query Objects
- Presenters
- Single Table Inheritance (STI)
- Duck-typing

**DevOps**
- S3
- Linux
---

## 📦 Skills & practices / Uploading files

### 🎓 Learn

- Use cases: attachments and processing files
- Storage
  - Local (not possible on Heroku)
  - S3 or other cloud storage
  - Database any kind (not recommended)
- [RAILS] Benefits of Active Storage
  - Processing
  - Previews
  - Mirroring (i.e. multiple stores)
- Timeouts / performance problems mitigation
  - Direct uploads on S3
  - Using 3rd party storate providers

### Rails

- 📗 https://edgeguides.rubyonrails.org/active_storage_overview.html
- 📗 https://github.com/thoughtbot/paperclip
- 📗 https://github.com/carrierwaveuploader/carrierwave/

## 📦 Skills & practices / Asynchronous processing

### 🎓 Learn

- Processing tasks / requests asynchronously - the user does not have to wait for the result before resuming work
- Receiving information about task completion
  - Callbacks
  - Polling
- Use cases
  - UX performance optimisation
  - Mitigating timeouts
- [RAILS] Sidekiq
  - WebUI
  - Sidekiq CRON
  - Error handling
  - Unique Jobs
  - Scheduling
  - Cases for re-scheduling (i.e. intervals related to when the previous iteration completed)
  - Challenges
    - DB Connection pooling
    - Killing jobs during deployments (be prepared for restarts)
- Message Brokers (i.e. SQS / RabbitMQ)
  - For distributed processing (by different applications)
  - For processing that should be easy to scale

### Rails

- 📗 [ActiveJob and Sidekiq](https://gist.github.com/stevo/2769d7d9f30b237ea5c0b0b4c43c15bf#active-job-and-sidekiq)
- 📗 [Sidekiq queue priorities explained](https://github.com/mperham/sidekiq/issues/1543)

## 📦 Skills  & practices / Regular expressions

### 🎓 Learn

- [PAIR] Write a regular expressions to match given requirements
  - Non-capturing groups
  - Named captures
- Syntax for describing rules/expectations against textual content (i.e. email validation)
- Use cases
  - validating
  - searching
  - filtering
  - sanitizing
- Tooling
  - http://www.crystular.org/
  - https://rubular.com/
- Regular expressions are to be used with caution (due to possible introduction of performance / security problems)

### 📝 Katas

- Write a regular expressions to match given requirements

## 📦 Skills & practices / Caching

### 🎓 Learn

- Page caching for "static" content with no authorization
  - Pre-generated but still served by HTTP server
  - Varnish
- Action caching for "static" content behind authentication or other filters
- Fragment caching for dynamic pages that contain cacheable fragments
  - Russian doll caching - expiring deep nested fragments should expire higher level fragments. Can be achieved by properly constructing cache key.
  - [RAILS] Partial and collection caching
    - collection caching requires one call to cache store
- Cache invalidation
  - cache-key based
    - if planned properly it allows for selectively expiring cache on multiple levels (i.e. company scoped, user scoped, resource scoped)
  - expire_in (relative time based)
  - active (external process)
- Low level caching
  - [RAILS] Rails.cache.fetch
- Storage
  - File system (tmp/cache)
  - Redis, Consul
  - Memcached (very fast, but not very flexible when it comes to managing cache keys)
  - Relational database (i.e. counter_cache)
- ETag
  - Server generates checksum for content generated
  - Client sends this back on next request
  - Server generates new output and checks if the checksum matches
  - If it does, it return HTTP 304 Not Modified
- SQL Caching
  - Caching consecutive, same calls to DB (for free in Rails)
  - Materialized views
- Caching in rails development is disabled by default
  - [There is a task to toggle it](https://blog.bigbinary.com/2016/01/25/caching-in-development-environment-in-rails5.html)
- Use cases, risks and costs
  - Performance issues that affect UX or costs significantly and in important parts of the system
  - Improper cache invalidation can be a source of hard to track errors
  - Adding caching can introduce another layer of complexity to application, and requires extra testing effort


### Rails

- https://guides.rubyonrails.org/caching_with_rails.html
- https://blog.appsignal.com/2018/08/14/rails-collection-caching.html

## 📦 Skills & practices / Authorization

### 🎓 Learn

- Authorization is a process of confirming if given identity (already authenticated) should have access to given resource
- Roles implementation
  - flags - simple, straight-forward, require extra column for each role (difficult to extend), easy to search and read. Nice when there are only two roles in the system.
  - enum - simple, straight-forward, quite easy to extend, easy to search and read. Nice when you have many roles and each user has only one.
  - relation based - i.e. rolify. Less performing (more complex SQL queries). More to difficult to filter read. Nice when you have many roles and each user can have many of those and you would like to configure and introduce new roles from UI level.
  - STI - Easy to search and read. Provide contextual place for role-based code out of the box. Hard to extend, as you need to introduce new class to handle it. Nice when you have limited number of roles and each user can have only one. Also when you need to contextualize some of your code per role.
  - Bit encoded - Works similarly to permission setting mechanism in UNIX systems. Each bit represents one role and roles are encoded as integer on DB level. Not easy to read and search, but very efficient to query for. Moderately difficult to extend (just add a new bit, still those need to be in order). Nice when you have many roles and each user can have many of those and you do not need to introduce new ones from UI.

### Rails

- 📗 [CanCan](https://github.com/ryanb/cancan)
- 📗 [Pundit](https://github.com/varvet/pundit)

## 📦 Misc / Extract Method

### 🎓 Learn

- Reduce complexity of given method by breaking it into pieces
- Improves on method readability / comprehendability
- Usually new methods introduced should be added to private interface
- If it requires passing extra arguments into method, it might indicate that `Extract Class`refactoring might be introduced instead (so those arguments will be kept as state of extracted class/object)

### Rails

- 📗 https://thoughtbot.com/upcase/videos/ruby-science-extract-method

## 📦 Misc / Extract Class

### 🎓 Learn

- Reduces complexity of given class by breaking it into pieces
- Improves on SRP, testability and code re-use / modularity
- Increases indirection, might introduce test-code mismatch (code is tested indirectly) - which is not inherently bad

### Rails

- 📗 https://thoughtbot.com/upcase/videos/ruby-science-extract-class
- 📗 https://thoughtbot.com/upcase/videos/extract-class

## 📦 Misc / Introduce explaining variable

### 🎓 Learn

- Giving a name to value that would otherwise be cryptic
  - 📗 [example](https://selleo.com/til/posts/wfafr3yngs-extract-explaining-variable-by-example)
- Simplifying expressions (i.e dividing complex equations or logical expressions to smaller pieces, but not by exposing new methods)
- Giving non-keyword method arguments a name
  - i.e. `SendOrder.call(order, 4.days.from_now)` -> `deliver_at = 4.days.from_now; SendOrder.call(order, deliver_at)`

### Rails

- 📗 https://github.com/thoughtbot-upcase-exercises/explaining-variable

## 📦 Misc / Sanitization

### 🎓 Learn

- Filtering content (i.e. text) from things we do not want
- Usually refered to in context of HTML and other markup languages and in context of security (i.e. XSS prevention, exposing sensitive data in logs etc.) or design (i.e. limiting what user can change in terms of styling)
  - XSS - remove all JS from HTML
  - Styling - filter out all tags beside `<b>` and `<i>`

## 📦 Misc / (not) Deterministic

### 🎓 Learn

- A deterministic function/method is a method that called in the same environment multiple times will always return the same value or behave the same way
- An example of non-deterministic code is flakey-spec
- A non deterministic code is a code, that react to change in environment it should not react to (i.e. time, order of execution)
- I.e. API calls that fails when called once, but succeed when called again

## 📦 Tooling / CRON

### 🎓 Learn

- Tool/daemon/utility that allows specifying intervals in which certain task/job/script should be executed
- Crontab - syntax for defining the interval pattern
- Use Cases
	- "on every 1st day of month generate and send invoice for coworking space"
	- backups
- https://crontab.guru/
- [RAILS] Cron in Sidekiq

## 📦 Tooling / Git: bisect

### 🎓 Learn

- Allows to find which commit affected a code in a given way (in most cases - broke the build)

## 📦 Laws and principles / LSP

### 🎓 Learn

- Liskov Substitution Principle
- Strong LSP - interface is exactly the same (you could apply parent level tests to subclass test and those should go green), not very applicable, probably only in "proxy" like approaches or decorating methods
- Weak LSP - original behaviour is not maintained
- Methods matches LSP when
  - accepts (can be called with) the same arguments lists
  - object returned are of the same type or matching the same interface (NullObject pattern is useful to achieve that)
- LSP improves on code comprehendability and working with polymorphism, especially when working with collections of polymorphic objects (limits risk of unexpected exceptions)
- It is worth to consider calling original implementation (`super`)
- 📗 https://thoughtbot.com/upcase/videos/liskov-substitution-principle

## 📦 Patterns and Techniques / Policies

### 🎓 Learn

- Pattern for describing auhtorization rules
- Should be kept simple and build logic around (subject (user) and object (resource))
- Renders testing authorization easy
  - As long as you ensure that policy is actually used

### Rails

- Pundit as a library of choice
  - Authorizes actions on controller level
  - Provides helpers for view layer
  - Can enforce/ensure authorization for all actions
  - Provides scoping capabilites (i.e. allow to destroy only own posts)

## 📦 Patterns and Techniques / Query Objects

### 🎓 Learn

- A pattern dedicated to wrapping logic related to querying data store
- Should be applied when
  - Logic is complex (in terms of LOC)
  - Logic is complex (actual complexity, pure SQL with many cases to be tested)
  - Logic is higly contextual (i.e. used for specific purpose in very limited amount of cases)
  - Logic breaks "SQL coupling" (when joining other tables)
  - Logic is based on conditions
- We prefer queries to not be chainable and return iterable collections instead (due to ISP issues)
  - We can expose additional scopes on the object instead
  - It results in much higher testability (very hard to mock relations)

### Rails
- 📗 https://medium.com/selleo/essential-rubyonrails-patterns-part-2-query-objects-4b253f4f4539
- 📗 https://github.com/Selleo/pattern#query

## 📦 Patterns and Techniques / Presenters

### 🎓 Learn

- Presenters in our context acts as a grouping pattern, that expose a certain interface for presentation purposes (i.e. template). It differs from decorator in a sense, that it does not necesarilly have to wrap single, individual object as context. It wraps a specific "concept" instead, i.e. `DashboardPresenter`

## 📦 Patterns and Techniques / Single Table Inheritance (STI)

### 🎓 Learn

- Single Table Inheritance
- Allow for single table to acts as a source for many model classes
- Useful when all columns are shared by all models
- Capabilities
  - Allow for overriding methods for each model (i.e. `#compress` or `#url`)
  - [RAILS] Automatic filtering by type column (i.e. `Avatar.all`)
- Beware of LSP in this context
- Example Use cases
  - Roles (`Admin`/`User`)
  - Attachments (`Avatar`, `ProductPhoto`, `Pdf`)
- STI should be used with caution and well thought through, due to risk of introducing lots of contextual code (breaking LSP)

## 📦 Patterns and Techniques / Duck-typing

### 🎓 Learn

- Two classes / objects / modules share the same interface / API
- "If it walks like a duck, quacks like a duck, then it has to be a duck"
- TODO: Upcase quote

## 📦 DevOps / S3

### 🎓 Learn
- 📗 [service description](/service_delivery_paths/backend_developer/devops/amazon/s3.md)

📝 Katas

- Create a bucket, make it private (access key and secret required to access)
- Generate expiring link to given resource
- Create a public read-only bucket

## 📦 DevOps / Linux

### 🎓 Learn

- 📗 [commands](/service_delivery_paths/backend_developer/devops/linux.md#independent-i)
- 📗 [ssh](/service_delivery_paths/backend_developer/devops/linux.md#ssh)
- 📗 [file permissions](/service_delivery_paths/backend_developer/devops/linux.md#permissions)
- 📗 [file ownership](/service_delivery_paths/backend_developer/devops/linux.md#ownership)