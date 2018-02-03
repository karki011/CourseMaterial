# SQL Data

* [Statement Data](#statement-data)
  * [String](#string)
  * [Numeric](#numeric)

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

**Previous:** [Introduction](introduction.markdown) |
**Next:** [Statements](statements.markdown)
