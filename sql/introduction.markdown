# SQL Introduction

* [Introduction](#introduction)
* [SQL Implementations](#sql-implementations)
* [ANSI SQL](#ansi-sql)

## Introduction

SQL, pronounced "Sequel", stands for Structured Query Languange. From [Wikipedia's](https://en.wikipedia.org/wiki/SQL) article on SQL:

> SQL was initially developed at IBM by Donald D. Chamberlin and Raymond F. Boyce in the early 1970s. This version, initially called SEQUEL (Structured English Query Language), was designed to manipulate and retrieve data stored in IBM's original quasi-relational database management system, System R, which a group at IBM San Jose Research Laboratory had developed during the 1970s. The acronym SEQUEL was later changed to SQL because "SEQUEL" was a trademark of the UK-based Hawker Siddeley aircraft company.
>
> In the late 1970s, Relational Software, Inc. (now Oracle Corporation) saw the potential of the concepts described by Codd, Chamberlin, and Boyce, and developed their own SQL-based RDBMS with aspirations of selling it to the U.S. Navy, Central Intelligence Agency, and other U.S. government agencies. In June 1979, Relational Software, Inc. introduced the first commercially available implementation of SQL, Oracle V2 (Version2) for VAX computers.

## SQL Implementations

There are a many different flavors of SQL, such as:

* MySQL by Oracle
* Microsoft SQL
* PostgreSQL
* SQLite

## ANSI SQL

SQL is **NOT** guaranteed to be portable between systems, but many SQL flavors comply with the ANSI standard. To be compliant with the ANSI standard, a flavor of SQL must support at least the major commands (such as SELECT, UPDATE, DELETE, INSERT, WHERE) in a similar manner.

Since the introduction of ANSI SQL, the standard has been revised to include a larger set of features. This is the skillset we'll be focusing on so that you'll have the most portable base of knowledge across all platforms and be able to pick up new ones with ease.

**Previous:** [System Setup](system.markdown) |
**Next:** [Operators](operators.markdown)
