# Middle

---

## Areas

**Competence**

- Common table expressions aka CTE
- Generating series for different data types
- Window functions
- Indexing
- Query planner
- More joins
- Merge (aka upsert)
- Simple locking
- Triggers & generated-columns
- Text search

---

## 📦 Common table expressions aka CTE

### 🎓 Resources

- 📗 [queries-with](https://www.postgresql.org/docs/11/static/queries-with.html)
- 📗 [workshop-db-03](https://github.com/qbart/workshop-db-03)

---

## 📦 Generating series for different data types

### 🎓 Resources

- 📗 [functions-srf](https://www.postgresql.org/docs/11/static/functions-srf.html)

---

## 📦 Window functions

### 🎓 Resources

- 📗 [tutorial-window](https://www.postgresql.org/docs/11/static/tutorial-window.html)
- 📗 [sql-select](https://www.postgresql.org/docs/11/static/sql-select.html#SQL-WINDOW)
- 📗 [functions-window](https://www.postgresql.org/docs/11/static/functions-window.html)
- 📗 [workshop-db-03](https://github.com/qbart/workshop-db-03)

---

## 📦 Indexing

### 🎓 Resources

- 📗 [indexes](https://www.postgresql.org/docs/11/static/indexes.html)
- 📗 [heroku postgres indexes](https://devcenter.heroku.com/articles/postgresql-indexes)
- 📗 [principles-and-applications-of-the-index-types-supported-by-postgresql](https://medium.com/@Alibaba_Cloud/principles-and-applications-of-the-index-types-supported-by-postgresql-481f59bab67d)
- 📗 [tour-of-postgres-index-types](https://www.citusdata.com/blog/2017/10/17/tour-of-postgres-index-types/)
- 📗 [habr blog](https://habr.com/en/company/postgrespro/blog/441962/) (1-10)

---

## 📦 Query planner

### 🎓 Resources

- 📗 [performance-tips](https://www.postgresql.org/docs/11/performance-tips.html)
- 📗 [parallel-query](https://www.postgresql.org/docs/11/parallel-query.html)
- 📗 [performance-cheat-sheet-postgresql](https://severalnines.com/blog/performance-cheat-sheet-postgresql)
- 📗 [reading-an-explain-analyze-query-plan](https://robots.thoughtbot.com/reading-an-explain-analyze-query-plan)
- 📗 [reading-an-explain-analyze-query-plan](http://tatiyants.com/pev/#/plans)
- 📗 [explaining-the-unexplainable 1](https://www.depesz.com/2013/04/16/explaining-the-unexplainable/)
- 📗 [explaining-the-unexplainable 2](https://www.depesz.com/2013/04/27/explaining-the-unexplainable-part-2/)
- 📗 [explaining-the-unexplainable 3](https://www.depesz.com/2013/05/09/explaining-the-unexplainable-part-3/)
- 📗 [explaining-the-unexplainable 4](https://www.depesz.com/2013/05/19/explaining-the-unexplainable-part-4/)

---

## 📦 More joins

- FULL
- CROSS

### 🎓 Resources

- 📗 [queries-table-expressions](https://www.postgresql.org/docs/11/static/queries-table-expressions.html)

---

## 📦 Merge (aka upsert)

### 🎓 Resources

- 📗 [sql-insert](https://www.postgresql.org/docs/11/static/sql-insert.html)

---

## 📦 Simple locking

### 🎓 Resources

- 📗 [sql-for-update-share](https://www.postgresql.org/docs/current/sql-select.html#SQL-FOR-UPDATE-SHARE)
- 📗 [explicit-locking](https://www.postgresql.org/docs/11/static/explicit-locking.html)

---

## 📦 Triggers & generated-columns

### 🎓 Resources

- 📗 [generated-columns](https://www.postgresql.org/docs/12/ddl-generated-columns.html)
- 📗 [sql-createtrigger](https://www.postgresql.org/docs/11/static/sql-createtrigger.html)
- 📗 [plpgsql-trigger](https://www.postgresql.org/docs/11/static/plpgsql-trigger.html)
- 📗 [trigger-definition](https://www.postgresql.org/docs/11/static/trigger-definition.html)
- 📗 [functions-event-triggers](https://www.postgresql.org/docs/11/functions-event-triggers.html)

---

## 📦 Text search

As a general rule you understand differences and similiartites between two approaches and you know when to use Postgres or ElasticSearch.

### 🎓 Resources

- 📙 [datatype-textsearch](https://www.postgresql.org/docs/11/static/datatype-textsearch.html)
- 📙 [functions-textsearch](https://www.postgresql.org/docs/11/static/functions-textsearch.html)
- 📙 [textsearch](https://www.postgresql.org/docs/11/static/textsearch.html)

### 🎓 Elastic Search

Elasticsearch is a distributed, open source search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured.
Possible use cases:

* Application search
* Website search
* Logging and log analytics
* Infrastructure metrics and container monitoring
* Application performance monitoring
* Geospatial data analysis and visualization
* Security analytics
* Business analytics

- 📙 [es-intro](https://www.elastic.co/guide/en/elasticsearch/reference/current/elasticsearch-intro.html)
- 📙 [es-docs](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs.html)
- 📙 [es-indices](https://www.elastic.co/guide/en/elasticsearch/reference/current/indices.html)
- 📙 [es-mapping](https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping.html)
- 📙 [es-query-dsl](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html)

## Questions

1. Describe difference between `FULL JOIN` and `CROSS JOIN`.
2. In which situations `INSERT` command will trigger `ON CONFLICT` action that was specified in the upsert query?
3. How do database triggers work? 
4. How do generated columns work?
5. Compare PostgreSQL text-search capabilities with ElasticSearch.
- In which situations you would recommend customer using PostgreSQL FTS vs. ElasticSearch?
6. Describe locking. What is it for?
- Describe row-level, table-level, advisory locks.
- What is a deadlock?
7. Indexing:
- What are partial indexes?
- What are expressions indexes?
- What are include indexes?
- What is a index-only scan? How does it correlate to include indexes?
8. What is a query planner?
- Does it always generate fully optimal plan?
- Can you force query planner to choose different plan?


