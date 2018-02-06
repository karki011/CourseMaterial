# SQL Injection

* [Introduction](#introduction)
* [Malicious](#malicious)
* [Invalid Input](#invalid-input)

## Introduction

SQL Injection is the "injection" of unexpected or malicious code into SQL statements.

* Best Case: this will cause unexpected or broken behavior
* Worst Case: this can be exploited to copy or destroy your database
* Every Case: it's bad. Anytime you hear SQL Injection, just know that it's something to avoid.

![Little Bobby Tables](../assets/sql-1.png "Little Bobby Tables")

## Malicious

Here's an example of C# code that is vunerable to SQL Injection:

```cs
public void InsertProduct(string name)
{
    var sql = $"INSERT INTO Product (Name) VALUES ('{name}');";
    // Execute SQL here
}
```

If I call my method like so:

```cs
InsertProduct("Test'); DROP TABLE Product; --")
```

the resulting SQL statement will be:

```sql
INSERT INTO Product (Name) VALUES ('Test'); DROP TABLE Product; --');
```

This is a valid SQL statement that will add a product and then delete the `Product` table.

## Invalid Input

In addition to that, you will have lots of trouble with invalid input like "O'Henry". If I have this method:

```cs
public void InsertProduct(string name)
{
    var sql = $"INSERT INTO Product (Name) VALUES ('{name}');";
    // Execute SQL here
}
```

And I call it with "O'Henry" as the input:

```cs
InsertProduct("O'Henry")
```

the resulting SQL statement will be:

```sql
INSERT INTO Product (Name) VALUES ('O'Henry');
```

This is an invalid SQL statement that will fail because we have an open string delimiter, but no closed string delimiter. Not malicious code, but it will still fail.

**Previous:** [Data](data.markdown) |
**Next:** []()
