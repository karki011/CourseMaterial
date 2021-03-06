# SQL Joins

* [INNER JOIN](#inner-join)
* [LEFT JOIN](#left-join)
* [Other JOINs](#other-joins)
  * [RIGHT JOIN](#right-join)
  * [FULL OUTER JOIN](#full-outer-join)
  * [LEFT EXCLUDING JOIN](#left-excluding-join)
  * [RIGHT EXCLUDING JOIN](#right-excluding-join)
  * [FULL OUTER EXCLUDING JOIN](#full-outer-excluding-join)

Combining multiple tables is where the real power of SQL lives. SQL can combine multiple tables on criteria that match and report them as one result set. That is where a JOIN clause comes in.

A JOIN clause is used to combine rows from two or more tables, based on a related column between them. Here are several Venn diagrams showing the visual representation of the different Joins available:

![SQL Joins](../assets/sql-joins.jpg "SQL Joins")

## INNER JOIN

The `INNER JOIN` statement in SQL gets only the records where a match occurs on both tables. The result set looks like this:

![SQL INNER JOIN](../assets/sql-inner-join.png "SQL INNER JOIN")

The `INNER JOIN` statement follows this syntax:

```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2 ON table1.column_name = table2.column_name;

-- Returns only records where the Orders.CustomerID matches the Customers.CustomerID
SELECT Orders.OrderID, Customers.CustomerName FROM Orders INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

## LEFT JOIN

The `LEFT JOIN` statement in SQL gets all the records from the left table and only records from the right table where a match occurs. The result set looks like this:

![SQL LEFT JOIN](../assets/sql-left-join.png "SQL LEFT JOIN")

The `LEFT JOIN` statement follows this syntax:

```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2 ON table1.column_name = table2.column_name;

-- Returns all customers and includes the order ID record
-- where the Orders.CustomerID matches the Customers.CustomerID
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```

## Other JOINs

While the majority of your joins will tend to be `INNER` or `LEFT` join statements, there are several other joins available to you:

### RIGHT JOIN

![SQL RIGHT JOIN](../assets/sql-right-join.png "SQL RIGHT JOIN")

### FULL OUTER JOIN

![SQL FULL OUTER JOIN](../assets/sql-full-outer-join.png "SQL FULL OUTER JOIN")

### LEFT EXCLUDING JOIN

![SQL LEFT EXCLUDING JOIN](../assets/sql-left-excluding-join.png "SQL LEFT EXCLUDING JOIN")

### RIGHT EXCLUDING JOIN

![SQL RIGHT EXCLUDING JOIN](../assets/sql-right-excluding-join.png "SQL RIGHT EXCLUDING JOIN")

### FULL OUTER EXCLUDING JOIN

![SQL FULL OUTER EXCLUDING JOIN](../assets/sql-full-outer-excluding-join.png "SQL FULL OUTER EXCLUDING JOIN")

**Previous:** [Injection](injection.markdown) |
**Next:** []()
