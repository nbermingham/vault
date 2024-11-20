## Overview
SQL (Structured Query Language) is the standard language for interacting with relational databases. It is used to query, manipulate, and manage data stored in structured formats like tables.

---

## Key Concepts

### SQL Basics
- Data Manipulation Language (DML): Includes commands to query, insert, update, and delete data.
- Data Definition Language (DDL): Used to define the structure of the database, including creating and modifying tables.
- Data Control Language (DCL): Manages access control to the database with commands like granting or revoking permissions.

### Relational Databases
- Data is organized into tables consisting of rows (records) and columns (attributes).
- Relationships between tables include:
  - One-to-One: Each record in one table corresponds to one record in another table.
  - One-to-Many: One record in one table links to multiple records in another.
  - Many-to-Many: Records in both tables link to each other through a junction table.

---

## Common SQL Commands

### [[SELECT Statement]]
The SELECT statement is used to retrieve specific data from a database table. It supports filtering, grouping, and sorting through various clauses.

### [[INSERT Statement]]
The INSERT statement is used to add new records to a database table. Values for specific columns are specified.

### [[UPDATE Statement]]
The UPDATE statement is used to modify existing records in a database table. It allows specifying conditions to target particular rows.

### [[DELETE Statement]]
The DELETE statement is used to remove records from a database table. Conditions can be applied to target specific rows.

---

## [[JOIN Operations]]
SQL JOIN operations combine data from two or more tables based on relationships between them.

- [[INNER JOIN]]: Returns rows with matching values in both tables.
- [[LEFT JOIN]]: Returns all rows from the left table and matching rows from the right table.
- [[RIGHT JOIN]]: Returns all rows from the right table and matching rows from the left table.

---

## [[Aggregate Functions]]
Aggregate functions perform calculations on grouped data. Common functions include:
- COUNT: Counts rows.
- SUM: Calculates the sum of numeric values.
- AVG: Calculates the average of numeric values.
- MIN and MAX: Find the minimum and maximum values, respectively.

---

## [[Subqueries]]
Subqueries are nested queries that appear inside another SQL statement. They are used to perform operations that depend on the results of the inner query.

---

## [[Window Functions]]
Window functions perform calculations across rows related to the current row without collapsing them into a single output. Common window functions include:
- [[ROW_NUMBER]]: Assigns a unique number to each row within a partition.
- [[RANK]]: Assigns a rank to rows, allowing ties.
- [[OVER]]: Defines the partitioning and ordering of the window.

---

## Indexing
Indexes improve data retrieval speed but can slow down data modification operations like inserts, updates, and deletes. Indexes are typically created on frequently queried columns.

---

## Transactions
Transactions ensure data integrity by grouping SQL operations into a single unit of work. They support commands like BEGIN, COMMIT, and ROLLBACK to manage changes atomically.

---

## Tools and Databases
- SQL Tools: Examples include MySQL Workbench, DBeaver, and pgAdmin.
- Popular SQL Databases: MySQL, PostgreSQL, SQLite, Microsoft SQL Server, and Oracle Database.

---

## Best Practices
- Use aliases to improve query readability.
- Avoid selecting all columns; specify the required ones explicitly.
- Normalize databases to reduce redundancy and improve data integrity.
- Create indexes on frequently queried columns to improve performance.
- Use transactions to ensure atomicity and prevent partial updates.

---

## Resources
- Books:
  - *SQL in 10 Minutes, Sams Teach Yourself* by Ben Forta.
  - *Learning SQL* by Alan Beaulieu.
- Courses:
  - *The Complete SQL Bootcamp* on Udemy.
  - *Introduction to Databases* by Stanford Online.

---

## Related Topics
- Data Science: SQL forms the backbone of data analysis workflows.
- Big Data: SQL concepts are used in querying large-scale datasets.
- Database Design: Techniques for structuring relational databases.

---

## Tags
#SQL #databases #datascience #querylanguage #relationaldatabases