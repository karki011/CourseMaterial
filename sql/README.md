# SQL: Structured Query Language

* [Documentation and Resources](#documentation-and-resources)
* [Source Code Comments](#source-code-comments)
  * [Line Comment](#line-comment)
  * [Block Comment](#block-comment)
* [Source Code Line Termination](#source-code-line-termination)
* [Case Sensitivity](#case-sensitivity)
* [Material](#material)
* [Exercises](#exercises)

## Documentation and Resources

As we go into details of any programming tool, you'll find that documentation is your best friend for learning and improving your tool skill set:

* [W3 Schools](https://www.w3schools.com/sql/default.asp)
* [Wikipedia](https://en.wikipedia.org/wiki/SQL)

## Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by a compiler and are just there to help us programmers understand the code better.

You'll use comments for documentation and explanation of your code. Anytime you see comments, just know it's there for clarity.

### Line Comment

Also known as single-line comment, line comment syntax is prepended with `--`

```sql
-- Example line comment
```

### Block Comment

Also known as multi-line comment, block comment syntax is surrounded with `/* */`

```sql
/* Example
block
comment
*/
```

## Source Code Line Termination

Unless otherwise specified, each line of source code, called a statement, must be terminated with a `;`:

```sql
-- Here is a select statement
SELECT * FROM Customers;
```

## Case Sensitivity

Unless otherwise specified, SQL *IS NOT* case sensitive. For example, `select` is synonymous with `SELECT`.

However, SQL naming convention usually has keywords in ALL CAPS. We will do the same.

## Material

Awesome, let's get your [System Setup](system.markdown) and move onto our materials:

* [Introduction](introduction.markdown)
* [Statements](statements.markdown)
* [Modifiers](modifiers.markdown)
* [Data](data.markdown)
* [Injection](injection.markdown)
* [Joins](joins.markdown)

## Exercises

* [SqlIntro](https://github.com/truecodersio/SqlIntro)
