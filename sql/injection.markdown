# SQL Injection

* [Introduction](#introduction)
* [Malicious](#malicious)
* [Invalid Input](#invalid-input)
* [Parameterized Statements](#parameterized-statements)

## Introduction

SQL Injection is the "injection" of unexpected or malicious code into SQL statements.

* Best Case: this will cause unexpected or broken behavior
* Worst Case: this can be exploited to copy or destroy your database
* Every Case: it's bad. Anytime you hear SQL Injection, just know that it's something to avoid.

![Little Bobby Tables](../assets/little-bobby-tables.png "Little Bobby Tables")

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

## Parameterized Statements

Every language supports some version of [parameterized statements](https://en.wikipedia.org/wiki/Prepared_statement#C.23_ADO.NET), sometimes called prepared statements. Parameterized statements allow you to abstract your statement from your parameters.

Parameterized statements will sanitize your data by escaping any dangerous characters and performing any parsing or optimization necessary. Poor man's protection is just to do a `statement.Replace("'", "\'")` on the input, but if there is a more sophisticated attack, then this is not sufficient. It's better to use parameterized statements and sleep soundly.

Here's an example of a parameterized statement in C#:

```cs
SqlCommand command = sqlConnection.CreateCommand();
command.CommandText = "INSERT INTO Product (Name) VALUES (@name);";
command.Parameters.AddWithValue("@name", "Bicycle");

SqlDataReader dataReader = command.ExecuteReader();
// Handle data
```

The resulting SQL statement will be:

```sql
INSERT INTO Product (Name) VALUES ('Bicycle');
```

**Previous:** [Data](data.markdown) |
**Next:** [Joins](joins.markdown)
