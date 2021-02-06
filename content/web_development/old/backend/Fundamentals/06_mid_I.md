# Mid - level I

## Areas

**Open discussion topics**

**Skills & practices**

- Code Benchmarking
- Optimistic / Pessimistic / Distributed locking
- Message Brokers
- (Micro)Service Oriented Architecture

**Misc**

- CQRS
- Idempotency (term)
- Hashing / checksums
- base64
- JSON Web Tokens
- Eventual Consistency (term)
- Deployment strategies
- HTTP

**Tooling**
- Tunneling
- Webhooks testing

**Patterns and Techniques**
- Data structures

## 📦 Open discussion topics

**A selection of topics from the list below will be discussed during verification session**

* What is your opinion about monolithic vs microservice based architecture? :poodle:
* How would you ensure reliability of microservice architecture?
* How do you deal with database related performance issues (when processing tens of millions of records)?
* If you are asked to implement an interface that should work with live (realtime) data feed, how would you approach implementing it?
* How would you handle very intense traffic (i.e. from IoT) in [framework] application?
* How would you ensure stability of public (published) API in application that is under active and rapid development?
* What do you think about / where do you find application for SOA :poodle:
* What do you think about / where do you find application for CQRS :poodle:
* What do you think about / where do you find application for DDD :poodle:
* What do you think about / where do you find application for Event Sourcing :poodle:
* What do you think about / where do you find application for Reporting Databases

---

## 📦 Pair programming

- Complex problem solving skills will be verified during pair programming session
- Problems are of algorithmic yet pragmatic/practical nature
- Pairing session can take between 120 and 240 minutes, depending on developer efficiency
  - Complete problem solution may not necessarily be expected
- Developer can use any language/framework, but need to come prepared with a testing framework, database, application scaffolding etc. in place
- Potential tasks can be found 📗 [here](https://gist.github.com/stevo/80aa460769fc4b90543994e0bc58ccc9#file-requirements_part_6-md)
  - Task requirements can be **slightly** changed for individual sessions
- All skills acquired during development path will be verified, including
  - Requirements analysis
  - Design Patterns
  - Applying principles
  - Debugging skills
  - Test Driven Development

## 📦 Skills & practices / Code Benchmarking

### 🎓 Learn

- Benchmarking significant code change on systems with expected high-load
- Practical knowledge: benchmark a snippet of code
- General concept of load/stress testing (JMeter, Apache Bench)
  - Distributed AWS instances + monitoring and graphs analysis
  - Testing in context of one process
- Monitoring / Profiling

## 📦 Skills & practices / Optimistic / Pessimistic / Distributed locking

### 🎓 Learn

- Optimistic - comparing a know (retrieved) value (i.e. version, timestamp)
  - Concept of resolving conflicts (i.e. comparing actual changes)
- Pessimistic - lock resource for updating until lock is released
  - Database level
    - We can lock individual record, table...
    - We can lock read, write, both etc.
  - Implementation level
    - Mutexes
- Distributed locking https://redis.io/topics/distlock
- Rollbacks / Transactions in external systems that do not support it
  - Command pattern
  - "Test driving" (to_sql vs to_a on relation)

## 📦 Skills & practices / Message Brokers

### 🎓 Learn

- Examples: RabbitMQ, KAFKA, SQS
- Why?
  - Scaling / Stream processing (parallel processing)
  - Message delivery / Event bus (cross system communication)
  - Ensure some additional functionalities
    - At least once delivery / at most once delivery etc.
    - Streams / Channels
    - Active acknowledging of processing a message
- Advantages
  - Decoupling
  - Fault tolerance
  - Scaling

## 📦 Skills & practices / (Micro)Service Oriented Architecture

### 🎓 Learn

- Communication (brokers)
- Discovery (switching replicas, RPC)
- Identifying domains for purpose of
  - scaling
  - availability
- **SOA**
  - używa enterprise service bus (esb)
  - korzysta zazwyczaj z jednego storage
  - zazwyczaj jest to szereg usług zależnych od siebie i komunikujących sie pomiędzy sobą
- **MS**
  - używa prostszych kanalow komunikacji jak message brokers
  - każdy serwis posiada swoj własny data store
  - niezależne byty realizujące jakieś konkretne zadania
  - "dumb pipes" - nie powinniśmy całkowicie polegać na infrastrukturze

- 📗 https://martinfowler.com/microservices/#what
- 📗 https://blog.arkency.com/soa-microservices-ruby-eventide-scott-bellware-interview/
- 📗 https://www.techapeek.com/2019/07/18/what-is-the-difference-between-soa-and-microservices/
- 📗 https://blog.arkency.com/2014/07/microservices-72-resources/
- 📗 [Microservices vs. SOA](https://youtu.be/Xjm6y8rs8u4)

## 📦 Misc / CQRS

### 🎓 Learn

- Rozdzielenie odczytu od zapisu
  - Nie tylko na poziomie metod, ale na poziomie klas
  - Decouple response from DB
- Problemy
  - Frontend / Eventual Consistency
  - Failures
- Optimistic UI
- Denormalizing data

## 📦 Misc / Idempotency (term)

### 🎓 Learn

- https://stackoverflow.com/questions/1077412/what-is-an-idempotent-operation
- 📗 [Concept of idempotency key in Stripe](https://github.com/stripe/stripe-ruby/blob/b13fc8465f0a43ea4e7de8fe85c1cafdd5ea59d7/lib/stripe/api_operations/delete.rb#L15)
- https://aws.amazon.com/premiumsupport/knowledge-center/lambda-function-idempotent/
- "Calling same thing with same arguments should not cause any adverse side effects"
  - i.e. idempotency key added to message (uuid during creation as example)
  - silently handling specific classes of errors

### 📦 Misc / Hashing / checksums

### 🎓 Learn

- Hashing == funkcja skrótu - na podstawie inputu generowanie "unikalnego" ciągu znaków
- Application
    - Generating key for caching (i.e. assets)
    - Data corruption on any kind of transport, tampering prevention (i.e. MD5)
    - Comparison, indexing (SHA) (i.e. binary data duplicates, bit-torrent)

## 📦 Misc / base64

### 🎓 Learn

- encryption vs encoding
- used for encoding binary data to text, where binary can't be used (email attachments, small binary files in json)

## 📦 Misc / JSON Web Tokens

### 🎓 Learn

- 3 segments
  - header
  - payload
  - signature (header + payload) - prevents payload tampering
- Use long secrets for signing
- For stateless systems
  - whitelisting (sign-out removes JWT ID from some store)
  - payload can stores useful session-oriented data
  - standard for JWT
- Disadvantages
  - Need to be securely designed (especially in relation to claims)
  - Size
- Claims https://www.iana.org/assignments/jwt/jwt.xhtml
- Has to be used when it makes sense

## 📦 Misc / Eventual Consistency (term)

### 🎓 Learn
- 📗 [Eventual Consistency](https://en.wikipedia.org/wiki/Eventual_consistency)

### Takeaways

- State of the system has to become consistent at some point in time, but may not be consistent in given point in time
- Introduced significant complexity but can allow high scalability
- E.g.
  - DNS
  - Bank transfer (your balance is reduced, but other party balance has not increased)

### 🎤 Interview

- Teach me what is the eventual consistency
- Tell me what can be the consequences of the eventual consistency?

## 📦 Misc / Deployment strategies

### 🎓 Learn

- Heroku / Capistrano = deploy + restart - Rolling deployments (you can revert)
- Blue/Green deployment / 0-downtime
  - Routing part of traffic to newly deployed instance
  - Problems with
    - migrations
    - DNS
  - Needs extra monitoring and control to get advantages out of Blue/Green
- Canary Release (Incremental Rollout, Phased Rollout) - automated Blue/Green
- 📗 [12 Factor App](https://12factor.net/pl/)
  - wszystkie zewnętrzne rzeczy dostarczać przez envy (not in DB, not harcoded)
  - nie opierać się na state maszyny (np. filesystem, tmp)
  - be close to your production environment

### 🎤 Interview

- Tech me about Blue/Green deployment / Canary Release (Incremental Rollout, Phased Rollout) / 0-downtime
  - Routing part of traffic to newly deployed instance
  - Problems with: migrations & DNS
- Tell me about 12-factor app methodology

## 📦 Misc / HTTP

### 🎓 Learn

- https://developer.mozilla.org/en-US/docs/Web/HTTP
- Stateless
  - Mitigated with Cookies (stays in place when tab closes)
    - cookies are scope to domain
  - and sessions (ends when tab closes)
- Not encrypted
  - HTTPS is encrypted
- Standard of data transmission based on TCP in Client/Server architecture
- Request/Response cycle (at least in version 1)
- IP / DNS
- Headers
    - Method: POST / GET / PUT / DELETE/ HEAD...
        - HEAD - no response body, only headers. I.e. for health-check
        - OPTIONS - what methods given path handles
        - PATCH (subset of attributes) vs PUT (all attributes)
    - Content-Type
- Basic authentication support
- 1.1 supports sending multiple request in one connection
- 📗 [Caching](https://pl.wikipedia.org/wiki/Lista_nag%C5%82%C3%B3wk%C3%B3w_HTTP#Cache-Control)
- 📗 [FE HTTP](https://github.com/Selleo/DevPath/blob/master/frontend_developer/01_junior_I.md#-networking--http)

## 📦 Tooling / Tunneling

### 🎓 Learn

- ngrok (exposing local address/port to WAN)
- VPN (for security, masking location)
- SSH

## 📦 Tooling / Webhooks testing

### 🎓 Learn

- 📗 [requestbin](https://requestbin.com)
- ngrok

## 📦 Patterns and Techniques / Data structures

### 🎓 Learn

- 📗 [Data structures](https://en.wikipedia.org/wiki/Data_structure)
- 📗 [The top data structures you should know](https://www.freecodecamp.org/news/the-top-data-structures-you-should-know-for-your-next-coding-interview-36af0831f5e3/)
- 📗 [Intro to decision trees](https://medium.com/greyatom/decision-trees-a-simple-way-to-visualize-a-decision-dc506a403aeb)

### 🎤 Interview

Teach me how you understand:
- Queue (FIFO)
- Stack (LIFO)
- Linked Lists
- Set (array with unique contents)
- Tuple (array with constant size)
- Dictionary / Map / Hash
- Binary tree (in context of Decision trees)
- Graph (where vectors have values)
