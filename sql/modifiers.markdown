# SQL Modifiers

* [Operators](#operators)
* [WHERE: Filter Records](#where-filter-records)
* [AND, OR, NOT: Chaining Conditionals](#and-or-not-chaining-conditionals)
* [ORDER BY: Show Data Beautifully](#order-by-show-data-beautifully)
* [NULL: To Be or Not To Be](#null-to-be-or-not-to-be)
* [SELECT DISTINCT: Get Distinct Records](#select-distinct-get-distinct-records)

ANSI SQL provides additional statement keywords that can be used in tandem with the four CRUD statements to modify the results.

## Operators

In ANSI SQL, there are several operators that are used:

| Operator  | Definition                                                                    |
| --------- | ----------------------------------------------------------------------------- |
| `=`       | Equal                                                                         |
| `<>`      | Not equal. Note: In some versions of SQL this operator may be written as `!=` |
| `>`       | Greater than                                                                  |
| `<`       | Less than                                                                     |
| `>=`      | Greater than or equal                                                         |
| `<=`      | Less than or equal                                                            |

## WHERE: Filter Records

In SQL statements, the `WHERE` clause allows you to filter your data based on a certain conditional. The `SELECT`, `UPDATE`, and `DELETE` statements support adding the `WHERE` clause:

```sql
-- Select the Name and Address columns from the phone_book table where the id equals 42
SELECT Name, Address FROM phone_book WHERE id = 42;
```

## AND, OR, NOT: Chaining Conditionals

In SQL statements, you can chain conditionals together for the `WHERE` clause, allowing for logical operations with `AND`, `OR`, and `NOT`.

The `AND` operator displays a record if all the conditionals separated by `AND` are `TRUE`:

```sql
SELECT * FROM Customers WHERE Country='USA' AND City='Birmingham';
```

The `OR` operator displays a record if any of the conditionals separated by `OR` are `TRUE`:

```sql
SELECT * FROM Customers WHERE City='Birmingham' OR City='Atlanta';
```

The `NOT` operator displays a record if the condition(s) is `NOT TRUE`:

```sql
SELECT * FROM Customers WHERE NOT City='Atlanta';
```

You can also combine `AND`, `OR`, and `NOT` operators. Similar to mathematics, parens can be used to form complex expressions:

```sql
-- And Or combination
SELECT * FROM Customers
WHERE Country='USA' AND (City='Birmingham' OR City='Atlanta');

-- And Not combination
SELECT * FROM Customers
WHERE NOT Country='Germany' AND NOT Country='USA';
```

## ORDER BY: Show Data Beautifully

In SQL statements, the `ORDER BY` keyword can be used to sort the records returned by your `SELECT` statement. The `ORDER BY` follows this syntax:

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;

-- Select all from the Customers table
-- sorted ascending (the default sort) by the Country
SELECT * FROM Customers ORDER BY Country;

-- Select all from the Customers table
-- sorted ascending by the Country column and
-- descending by the CustomerName column
SELECT * FROM Customers ORDER BY Country ASC, CustomerName DESC;
```

## NULL: To Be or Not To Be

In SQL statements, the keyword `NULL` represents the absence of value:

```sql
-- Select where Address is absent of value
SELECT LastName, FirstName FROM Persons
WHERE Address IS NULL;

-- Select where Address isn't absent of value
SELECT LastName, FirstName, Address FROM Persons
WHERE Address IS NOT NULL;
```

## SELECT DISTINCT: Get Distinct Records

The `SELECT DISTINCT` statement will only return records with different values in the provided columns:

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;

-- Select the records that have a different Country value from the Customers table
SELECT DISTINCT Country FROM Customers;
```

**Previous:** [Statements](statements.markdown) |
**Next:** [Data](data.markdown)
