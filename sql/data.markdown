# SQL Data

* [Statement Data](#statement-data)
  * [String](#string)
  * [Numeric](#numeric)
  * [Null](#null)
* [Table Data](#table-data)
  * [Primary Keys](#primary-keys)
  * [Other Data Types](#other-data-types)

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

### Null

In SQL statements, the keyword `NULL` represents the absence of value:

```sql
-- Select where Address is null
SELECT LastName, FirstName FROM Persons
WHERE Address IS NULL;

-- Select where Address isn't null
SELECT LastName, FirstName, Address FROM Persons
WHERE Address IS NOT NULL;
```

**Note:** `NULL` is not the same as `0` or an empty string: `''`

* `0` and `''` are actual values, stored in your database as `0` or `''`
* `NULL` represents the absence of value: nothing is stored in your database

## Table Data

In ANSI SQL, data tends to resolve to 1 of 4 data types:

* Primary Keys
* Text Types
* Numeric Types
* Date Types

### Primary Keys

While not technically required for a table, best practice demands a primary key. Your best two options are:

* `INT` or `LONGINT`: an integer that increments for you as you insert your data
* `GUID` (Globally Unique IDentifier): a generated value that is extremely mathematically likely to be unique in the universe

### Other Data Types

Here is a list of [SQL Data Types](https://www.w3schools.com/sql/sql_datatypes.asp) available to you in ANSI SQL.

**Previous:** [Modifiers](modifiers.markdown) |
**Next:** [Injection](injection.markdown)
