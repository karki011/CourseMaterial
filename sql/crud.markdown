# SQL CRUD: The Basics

* [CRUD: Create Read Update Delete](#crud-create-read-update-delete)
* [SELECT: Read and Query Data](#select-read-and-query-data)

## CRUD: Create Read Update Delete

In the world of data manipulation, the acronym CRUD (Create, Read, Update, Delete) has become popular, since CRUD encapulates all the possible data manipulation actions:

* Create: The act of writing new data
* Read: The act of reading existing data
* Update: The act of modifying existing data
* Delete: The act of removing existing data

In SQL, we have CRUD with these commands:

## SELECT: Read and Query Data

The `SELECT` statement in SQL is used to querying data in your database. It follows this syntax:

```sql
-- Select column1 and column2 from the table_name table
SELECT column1, column2 FROM table_name;

-- Select the name and address columns from the phone_book table
SELECT name, address FROM phone_book
```

You can also select data from all columns by using `*`:

```sql
-- Select all available columns from the phone_book table
SELECT * FROM phone_book;
```

**Previous:** [Introduction](introduction.markdown) |
**Next:** []()
