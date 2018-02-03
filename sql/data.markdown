# SQL Data

* [Statement Data](#statement-data)
  * [String](#string)
  * [Numeric](#numeric)
* [Null](#null)

## Statement Data

Data is often included in [SQL Statements](statements.markdown) like `SELECT` and almost always included in `INSERT`, `UPDATE`, and `DELETE` statements. Here's the data you'll use:

### String

A string is a sequence of zero or more unicode characters. In SQL statements, a String is surrounded by single quotes, referred to as the string delimiter:

```sql
SELECT * FROM Customers WHERE Country = 'USA';
```

### Numeric

In SQL statements, a numeric value is used without modification:

```sql
SELECT * FROM Customers WHERE Id = 42;
```

## Null

In SQL statements, the keyword `NULL` represents the absence of value:

```sql
-- Select where column is null
SELECT column_names
FROM table_name
WHERE column_name IS NULL;

-- Select where column isn't null
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
```

**Note:** `NULL` is not the same as `0` or an empty string: `''`

* `0` and `''` are actual values, stored in your database as `0` or `''`
* `NULL` represents the absence of value: nothing is stored in your database

**Previous:** [Introduction](introduction.markdown) |
**Next:** [Statements](statements.markdown)
