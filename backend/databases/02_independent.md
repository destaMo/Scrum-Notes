# Independent

---

## Areas

**Competence**

- More joins
- Filtering out distinct rows
- Conditionals
- Text/math operations & formatting
- JSON / JSONB
- Foreign keys and referencial integrity
- Basic indexing
- Subqueries
- Transactions basics
- Views & materialized views
- Set operations

## 📦 More joins

- LEFT
- RIGHT

### 🎓 Resources

- 📗 [queries-table-expressions](https://www.postgresql.org/docs/11/static/queries-table-expressions.html)

---

## 📦 Filtering out distinct rows

- DISTINCT [ON]

### 🎓 Resources

- 📗 [sql-select](https://www.postgresql.org/docs/11/sql-select.html)

---

## 📦 Conditionals

- CASE
- COALESCE
- GREATEST
- LEAST

### 🎓 Resources

- 📗 [functions-conditional](https://www.postgresql.org/docs/11/static/functions-conditional.html)

---

## 📦 Text/math operations & formatting

Text:
- string concatenation (`||` / concat / concat_ws)
- length
- lower / upper
- quote_*

> Be aware of encoding/converting functions.

Math:
- operators
- round
- ceil
- floor
- sign
- trunc
- random
- div
- scale

### 🎓 Resources

- 📗 [functions-string](https://www.postgresql.org/docs/11/static/functions-string.html)
- 📗 [functions-formatting](https://www.postgresql.org/docs/11/static/functions-formatting.html)
- 📗 [functions-math](https://www.postgresql.org/docs/11/static/functions-math.html)

---

## 📦 JSON / JSONB 

### 🎓 Resources

- 📗 [datatype-json](https://www.postgresql.org/docs/11/static/datatype-json.html)
- 📗 [functions-json](https://www.postgresql.org/docs/11/static/functions-json.html)

---

## 📦 Foreign keys and referencial integrity

-  FOREIGN KEY

### 🎓 Resources

- 📗 [ddl-constraints](https://www.postgresql.org/docs/11/static/ddl-constraints.html)

---

## Basic indexing

- understand that there are different types that support different operations (no need for in-depth theory how it works)
- Unique
- Multicolumn

### 🎓 Resources

- 📗 [indexes](https://www.postgresql.org/docs/11/static/indexes.html)
- 📗 [types](https://www.postgresql.org/docs/11/indexes-types.html)
- 📗 [multicolumn](https://www.postgresql.org/docs/11/indexes-multicolumn.html)

## 📦 Subqueries

### 🎓 Resources

- 📗 [functions-subquery](https://www.postgresql.org/docs/11/static/functions-subquery.html)

---

## 📦 Transactions basics
### 🎓 Resources
- 📗 [sql-begin](https://www.postgresql.org/docs/11/static/sql-begin.html)
- 📗 [sql-commit](https://www.postgresql.org/docs/11/static/sql-commit.html)
- 📗 [sql-rollback](https://www.postgresql.org/docs/11/static/sql-rollback.html)

---

## 📦 Views & materialized views

### 🎓 Resources
- 📗 [sql-createview](https://www.postgresql.org/docs/11/static/sql-createview.html)
- 📗 [rules-materializedviews](https://www.postgresql.org/docs/11/static/rules-materializedviews.html)
- 📗 [sql-refreshmaterializedview](https://www.postgresql.org/docs/11/static/sql-refreshmaterializedview.html)

---

## 📦 Set operations

- UNION [ALL]
- INTERSECT [ALL]
- EXCEPT [ALL]

### 🎓 Resources
- 📗 [queries-union](https://www.postgresql.org/docs/11/static/queries-union.html)
- 📗 [sql-select](https://www.postgresql.org/docs/11/static/sql-select.html)

