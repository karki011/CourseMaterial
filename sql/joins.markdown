# SQL Joins

* [INNER JOIN](#inner-join)

Combining multiple tables is where the real power of SQL lives. SQL can combine multiple tables on criteria that match and report them as one result set. Here are several venn diagrams showing the visual representation of the different Joins available:

![SQL Joins](../assets/sql-joins.jpg "SQL Joins")

## INNER JOIN

The `INNER JOIN` statement in SQL gets only the records where a match occurs on both tables. It follows this syntax:

```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2 ON table1.column_name = table2.column_name;

-- Returns only records where the Orders.CustomerID matches the Customers.CustomerID
SELECT Orders.OrderID, Customers.CustomerName FROM Orders INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

So only the intersection of the tables is included in the result set:

![SQL INNER JOIN](../assets/sql-inner-join.png "SQL INNER JOIN")

**Previous:** [Injection](injection.markdown) |
**Next:** []()
