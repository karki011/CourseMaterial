# SQL CRUD: The Basics

* [SELECT: Read and Query Records](#select-read-and-query-records)
* [INSERT: Create New Records](#insert-create-new-records)
* [UPDATE: Modify Existing Records](#update-modify-existing-records)
* [DELETE: Remove Existing Records](#delete-remove-existing-records)

In the world of data manipulation, the acronym CRUD (Create, Read, Update, Delete) has become popular, since CRUD encapulates all the possible data manipulation actions:

* Create: The act of writing new data
* Read: The act of reading existing data
* Update: The act of modifying existing data
* Delete: The act of removing existing data

In the world of SQL, we also need the ability to manipulate data/records. We have CRUD in SQL with these commands:

## SELECT: Read and Query Records

The `SELECT` statement in SQL is used to query records in your database. It follows this syntax:

```sql
SELECT column1, column2, ...
FROM table_name;

-- Select the Name and Address columns from the phone_book table
SELECT Name, Address FROM phone_book;
```

You can also select from all columns by using `*`:

```sql
-- Select all available columns from the phone_book table
SELECT * FROM phone_book;
```

## INSERT: Create New Records

The `INSERT` statement in SQL is used to create a new record to your database. It follows this syntax:

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

-- Insert a record into our phone_book table with the provided key, value pairs
INSERT INTO phone_book (Name, Address) VALUES ('Cody Winton', '123 Main St.');
```

You can also insert a record for all available columns, as long as you provide values in the same order that the columns are in:

```sql
-- Insert a record into our phone_book table with the provided values
INSERT INTO phone_book VALUES ('Cody Winton', '123 Main St.', '205-555-1234');
```

**Note:** In SQL, single quotes are the string delimiter: `'Cody Winton'`

## UPDATE: Modify Existing Records

The `UPDATE` statement in SQL is used to modify existing records in your database. It follows this syntax:

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

/* Update all records from our phone_book table
with on the provided key, value pairs where the id equals 42 */
UPDATE phone_book SET Name = 'John Doe', Phone = '205-123-4567' WHERE id = 42


/* Update all records from our phone_book table
with on the provided key, value pairs where the Name equals "Cody Winton" */
UPDATE phone_book SET Name = 'John Doe', Phone = '205-123-4567' WHERE Name = 'Cody Winton'
```

**Note:** Without the `WHERE` clause in the `UPDATE` statement, every record in our table will be updated based on the key, value pairs provided.

## DELETE: Remove Existing Records

The `DELETE` statement in SQL is used to remove existing records in your database. It follows this syntax:

```sql
DELETE FROM table_name
WHERE condition;

-- Delete all records from our phone_book table where the id equals 42
DELETE FROM phone_book WHERE id = 42

-- Delete all records from our phone_book table where the Name equals "Cody Winton"
DELETE FROM phone_book WHERE Name = 'Cody Winton'
```

**Note:** Without the `WHERE` clause in the `DELETE` statement, every record in our table will be deleted.

**Previous:** [Introduction](introduction.markdown) |
**Next:** []()
