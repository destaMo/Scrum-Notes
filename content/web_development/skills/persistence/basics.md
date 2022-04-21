+++
title = "Persistence - Basics"
weight = 1
+++

{{%bubble %}}

**Points:** n/a (prerequisite for Backend Framework & Language basics)

**Description:** You can store & manipulate the data in one type of the database that is required to build an application with basic framework knowledge

**Person who successfully completed requirement for the given block:** 

- Knows how to read the data from transactional database
- Understands benefits & limitations of transactional database
- Can manipulate the structure and the data of the database
- Understands the difference between various database systems

{{% /bubble%}}

## Areas

**Competence**

- Filtering and projection
- Retrieving portions of data
- Simple joins
- Sorting data
- Basic data types
- Managing tables/schemas
- Basic constraints
- Managing data
- Grouping
- Basic aggregate functions

## 📦 Filtering and projection

- SELECT
- WHERE
- FROM

### 🎓 Resources

- 📗 [sql-select](https://www.postgresql.org/docs/11/sql-select.html)
- 📗 [queries-table-expressions](https://www.postgresql.org/docs/11/queries-table-expressions.html)
- 📗 [queries-select-lists](https://www.postgresql.org/docs/11/queries-select-lists.html)
- 📗 [queries-values](https://www.postgresql.org/docs/11/queries-values.html)
- 📗 [functions-comparison](https://www.postgresql.org/docs/11/functions-comparison.html)
- 📗 [functions-matching](https://www.postgresql.org/docs/11/functions-matching.html)

    ---

## 📦 Retrieving portions of data

- LIMIT
- OFFSET

### 🎓 Resources

- 📗 [queries-limit](https://www.postgresql.org/docs/11/queries-limit.html)

---

## 📦 Simple join

- INNER JOIN

### 🎓 Resources

- 📗 [queries-table-expressions](https://www.postgresql.org/docs/11/static/queries-table-expressions.html)

---

## 📦 Sorting data

- ORDER BY


### 🎓 Resources

- 📗 [queries-order](https://www.postgresql.org/docs/11/static/queries-order.html)

---

## 📦 Basic data types

### 🎓 Resources
- 📗 [datatype-numeric](https://www.postgresql.org/docs/11/static/datatype-numeric.html)
- 📗 [datatype-serial](https://www.postgresql.org/docs/current/datatype-numeric.html#DATATYPE-SERIAL)
- 📗 [datatype-character](https://www.postgresql.org/docs/11/static/datatype-character.html)
- 📗 [datatype-boolean](https://www.postgresql.org/docs/11/static/datatype-boolean.html)
- 📗 [datatype-datetime](https://www.postgresql.org/docs/11/static/datatype-datetime.html)
- 📗 [datatype-uuid](https://www.postgresql.org/docs/11/static/datatype-uuid.html)
- 📗 [uuid-ossp](https://www.postgresql.org/docs/11/static/uuid-ossp.html)
- 📙 [datatype-enum](https://www.postgresql.org/docs/11/static/datatype-enum.html)

---

## 📦 Managing tables/schemas

### 🎓 Resources
- 📗 [sql-createtable](https://www.postgresql.org/docs/11/static/sql-createtable.html)
- 📗 [sql-altertable](https://www.postgresql.org/docs/11/static/sql-altertable.html)
- 📗 [sql-droptable](https://www.postgresql.org/docs/11/static/sql-droptable.html)
- 📗 [ddl-schemas](https://www.postgresql.org/docs/11/static/ddl-schemas.html)

---

## 📦 Basic constraints

- DEFAULT
- UNIQUE
- NULL
- NOT NULL
- PRIMARY KEY

### 🎓 Resources
- 📗 [ddl-constraints](https://www.postgresql.org/docs/11/static/ddl-constraints.html)

---

## 📦 Managing data

- INSERT
- UPDATE
- DELETE
- TRUNCATE

### 🎓 Resources

- 📗 [sql-insert](https://www.postgresql.org/docs/11/static/sql-insert.html)
- 📗 [sql-update](https://www.postgresql.org/docs/11/static/sql-update.html)
- 📗 [sql-delete](https://www.postgresql.org/docs/11/static/sql-delete.html)
- 📗 [sql-truncate](https://www.postgresql.org/docs/11/sql-truncate.html)

---

## 📦 Grouping

- GROUP BY
- HAVING

### 🎓 Resources
- 📗 [querues-group](https://www.postgresql.org/docs/11/static/queries-table-expressions.html#QUERIES-GROUP)

---

## 📦 Basic aggregate functions

- SUM
- AVG
- COUNT
- MIN
- MAX

### 🎓 Resources

- 📗 [functions-aggregate](https://www.postgresql.org/docs/11/static/functions-aggregate.html)

## No-SQL

- 📗 [No-SQL wikipedia](https://en.wikipedia.org/wiki/NoSQL)
- 📗 [No-SQL db-engines](https://db-engines.com/en/article/NoSQL)

### Key-value stores

- 📗 [Key-value stores](https://db-engines.com/en/article/Key-value+Stores)
- 📙 [Redis](https://db-engines.com/en/system/Redis)

## Questions

1. What is a Primary Key?
2. Tell me about basic data types in PostgreSQL.
3. What's the difference between single quotes `'` and double quotes `"` in PostgreSQL?
4. How to perform type casting?
5. What `UNIQUE` constraint guarantees?
- Can it be used for multiple columns?
- How does `UNIQUE` behave in combination with `NULL` values? Why does it work this way?
6. What is the purpose of `INNER JOIN`? 
7. How do `LIMIT` and `OFFSET` work?
8. How to sort data?
9. Give an example of a query that uses `GROUP BY` and `HAVING`.
10. How would you define No-SQL?
11. Describe key-value store of your choice.
- Provide some use-cases of key-value stores.

### 📝 Katas

- [Learn SQL with simple, interactive exercises](https://sqlbolt.com/lesson/introduction)
