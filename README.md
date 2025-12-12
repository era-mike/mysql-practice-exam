# ⭐ **Study Guide and Answer Key — MYSQL PRACTICE QUESTIONS**

## **Question 1**

**Q:** In MySQL, what best describes a view?

**Correct Answer:** A predefined query that displays results as a virtual table

**Explanation:**
A view in MySQL is a stored query that behaves like a virtual table. It doesn’t physically store the data, but instead retrieves it dynamically from the underlying tables whenever the view is queried. This makes views useful for simplifying complex queries, enhancing security, and providing a consistent way to present data.

---

## **Question 2**

**Q:** What is the key difference between a correlated subquery and a standard subquery in MySQL?

**Correct Answer:** It references columns from the outer query within its condition

**Explanation:**
A correlated subquery is executed once for each row evaluated by the outer query because it refers to columns from that outer query. A standard subquery, by contrast, runs independently and only once, with its result passed back to the main query.

---

## **Question 3**

**Q:** Which MySQL data type is most appropriate for storing variable-length text values, such as names or email addresses?

**Correct Answer:** VARCHAR(255)

**Explanation:**
VARCHAR is designed for variable-length text, making it ideal for storing strings such as names or email addresses. CHAR is fixed-length and wastes space if values vary in size, INT is for numbers only, and TEXT(10) is invalid since the TEXT type does not accept a length specifier.

---

## **Question 4**

**Q:** Which SQL constraint guarantees that every value in a column is distinct from all others?

**Correct Answer:** UNIQUE

**Explanation:**
The UNIQUE constraint ensures that all values in a column are different from each other. NOT NULL only ensures a column cannot contain NULL values. DEFAULT sets a predefined value when none is provided. FOREIGN KEY enforces referential integrity between two tables.

---

## **Question 5**

**Q:** Which SQL constraint is used to establish a link between two different tables?

**Correct Answer:** FOREIGN KEY

**Explanation:**
A foreign key is used to create a relationship between two tables by linking a column in one table to the primary key of another. UNIQUE ensures distinct values, PRIMARY KEY uniquely identifies each row, and CHECK enforces a rule on column values.

---

## **Question 6**

**Q:** Which MySQL data type is most suitable for storing Boolean values such as true or false?

**Correct Answer:** BOOLEAN

**Explanation:**
In MySQL, the BOOLEAN (or BOOL) data type is the most suitable for storing true/false values. Internally, BOOLEAN is treated as TINYINT(1) where 0 = FALSE and 1 = TRUE. VARCHAR(1) and CHAR(1) can store symbols like Y/N but aren't real Boolean types. BIT can store binary values but isn’t commonly used specifically for Boolean logic.

---

## **Question 7**

**Q:** Which SQL syntax correctly creates a column with both NOT NULL and DEFAULT constraints?

**Correct Answer:** `email VARCHAR(255) NOT NULL DEFAULT 'none'`

**Explanation:**
MySQL requires the column name and data type first, followed by NOT NULL, then the DEFAULT clause. TEXT generally cannot use default values, `= 'none'` is invalid syntax, and DEFAULT NULL conflicts with NOT NULL.

---

## **Question 8**

**Q:** What is the main purpose of the SHOW command in MySQL?

**Correct Answer:** To manage and display information about databases and their objects

**Explanation:**
SHOW is used to display metadata about databases, tables, columns, indexes, users, storage engines, and server status. It helps administrators quickly inspect the environment.

---

## **Question 9**

**Q:** On which platform is MySQL Workbench not supported?

**Correct Answer:** Android

**Explanation:**
MySQL Workbench is available for Windows, macOS, and Linux. It is not available for mobile platforms like Android.

---

## **Question 10**

**Q:** During installation, which component is required for MySQL Workbench to operate correctly?

**Correct Answer:** MySQL Server

**Explanation:**
Workbench is a graphical client—it requires a running MySQL Server instance to connect to. Without the server, it cannot manage or query databases.

---
## **Question 11**

**Q:** Which website is the official source for downloading MySQL Workbench?

**Correct Answer:** [www.mysql.com](http://www.mysql.com)

**Explanation:**
The official source for MySQL Workbench is the MySQL website, maintained by Oracle. Downloading from unofficial sources may risk outdated or unsafe software.

---

## **Question 12**

**Q:** In MySQL Workbench, what does the term *schema* represent?

**Correct Answer:** A database

**Explanation:**
In MySQL, *schema* is synonymous with *database*. It represents a logical container for tables, views, procedures, and other database objects.

---

## **Question 13**

**Q:** What is the correct SQL command to create a new schema?

**Correct Answer:** `CREATE SCHEMA myDatabase;`

**Explanation:**
CREATE SCHEMA defines a new database environment. Commands like NEW, MAKE, or ADD SCHEMA do not exist in standard SQL.

---

## **Question 14**

**Q:** What SQL command is used to create a new table in a database?

**Correct Answer:** `CREATE TABLE users`

**Explanation:**
`CREATE TABLE` defines a new table, including its columns and constraints. Other listed options are not valid SQL.

---

## **Question 15**

**Q:** Which SQL command correctly adds a new column named *phone_number* to the *customers* table?

**Correct Answer:** `ALTER TABLE customers ADD phone_number VARCHAR(15);`

**Explanation:**
`ALTER TABLE … ADD` is the valid syntax for adding columns. UPDATE modifies row values, and the other options are invalid SQL statements.

---

## **Question 16**

**Q:** Which SQL command removes the *email* column from the *employees* table?

**Correct Answer:** `ALTER TABLE employees DROP COLUMN email;`

**Explanation:**
`DROP COLUMN` permanently removes the column definition. DELETE removes rows, UPDATE … SET email=NULL clears data, and REMOVE COLUMN is invalid SQL.

---

## **Question 17**

**Q:** Which SQL query retrieves only the *first_name* and *last_name* of customers who live in Texas?

**Correct Answer:**
`SELECT first_name, last_name FROM customers WHERE state = 'TX';`

**Explanation:**
The query selects only the desired columns and applies a filter on the state. Queries using AND in place of column lists or GET syntax are invalid.

---

## **Question 18**

**Q:** What is the correct SQL syntax to insert a new record into a products table with columns *name*, *price*, and *stock*?

**Correct Answer:**
`INSERT INTO products (name, price, stock) VALUES ('TV', 399.99, 20);`

**Explanation:**
Explicitly listing columns ensures values match the correct fields. INSERT … VALUES without column names only works if all columns are supplied in order. Other commands listed are invalid.

---

## **Question 19**

**Q:** Which SQL command correctly increases the price of all products in the *products* table where the stock is less than 10?

**Correct Answer:**
`UPDATE products SET price = price + 10 WHERE stock < 10;`

**Explanation:**
UPDATE modifies existing rows. MODIFY and CHANGE are not SQL commands for altering data, and the incorrect UPDATE syntax attempts to modify a column directly.

---

## **Question 20**

**Q:** Which SQL command deletes all records from the *orders* table where the status is 'cancelled'?

**Correct Answer:**
`DELETE FROM orders WHERE status = 'cancelled';`

**Explanation:**
DELETE … WHERE removes only matching rows. ERASE, REMOVE, and DROP FROM are not valid SQL commands for row deletion.


## **Question 21**

**Q:** Which SQL clause is used to combine rows from two tables based on a related column?

**Correct Answer:** JOIN

**Explanation:**
JOIN merges rows across tables using a related column, such as a primary/foreign key relationship. Options like MERGE, LINK, or UNITE are not SQL operations in MySQL.

---

## **Question 22**

**Q:** Which SQL query correctly joins the *orders* and *customers* tables by matching the customer ID?

**Correct Answer:**
`SELECT * FROM orders JOIN customers ON orders.customer_id = customers.id;`

**Explanation:**
This is proper ANSI JOIN syntax. The implicit join using a comma is outdated. The MERGE and SELECT … AND syntax given in the other options are invalid.

---

## **Question 23**

**Q:** What happens if you attempt to insert a record that violates a table’s NOT NULL constraint?

**Correct Answer:** An error is returned and the record is not inserted

**Explanation:**
A NOT NULL constraint requires a value. MySQL rejects inserts missing required values unless a default is provided. It does *not* silently insert NULL or issue a mere warning.

---

## **Question 24**

**Q:** What is the primary goal of database normalization?

**Correct Answer:** Reduce data redundancy and improve data integrity

**Explanation:**
Normalization organizes tables to eliminate unnecessary duplication and maintain consistent data. Performance gains are secondary and not guaranteed.

---

## **Question 25**

**Q:** In an ER (Entity-Relationship) diagram, what does a rectangle typically represent?

**Correct Answer:** A table (entity)

**Explanation:**
A rectangle represents an *entity*, which translates to a table in a relational database. Attributes are ovals, relationships are diamonds.

---

## **Question 26**

**Q:** What is the purpose of MySQL authentication?

**Correct Answer:** To verify a user’s identity before granting access

**Explanation:**
Authentication verifies *who* a user is. Authorization (separate concept) controls what they can do. Backup and encryption are unrelated tasks.

---

## **Question 27**

**Q:** What does authorization control in MySQL?

**Correct Answer:** What operations a user can perform on specific objects

**Explanation:**
Authorization governs privileges like SELECT, INSERT, UPDATE, etc., on databases, tables, or columns. It does not control programming languages or performance.

---

## **Question 28**

**Q:** Which MySQL statement is used to assign specific privileges to a user?

**Correct Answer:** GRANT

**Explanation:**
GRANT assigns privileges such as SELECT or INSERT. ALLOW, GIVE, or ADD PRIVILEGE are not valid SQL keywords.

---

## **Question 29**

**Q:** Which of the following is a recommended technique for preventing SQL injection attacks?

**Correct Answer:** Using parameterized queries (prepared statements)

**Explanation:**
Prepared statements separate SQL code from data, preventing user input from altering query structure. Concatenation is dangerous, and full database access increases risk.

---

## **Question 30**

**Q:** What is a prepared statement in MySQL?

**Correct Answer:** A query in which the SQL engine separates code from data inputs

**Explanation:**
Prepared statements are parsed once and executed repeatedly with different values, improving safety (protecting against SQL injection) and performance.

## **Question 31**

**Q:** Which MySQL function is used to encrypt data with AES encryption?

**Correct Answer:** `AES_ENCRYPT()`

**Explanation:**
`AES_ENCRYPT()` encrypts data using the AES algorithm.
`SHA256()` creates a one-way hash,
`ENCODE()` performs reversible encoding (not encryption),
and `PROTECT_DATA()` is not a MySQL function.

---

## **Question 32**

**Q:** What is the correct SQL command to create a new user in MySQL?

**Correct Answer:** `CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';`

**Explanation:**
`CREATE USER` is the proper syntax and requires specifying the username and host.
`NEW USER` and `ADD USER` are invalid SQL.
`CREATE NEWUSER` is not a recognized command.

---

## **Question 33**

**Q:** Which SQL command is used to grant privileges to a MySQL user?

**Correct Answer:** GRANT

**Explanation:**
The GRANT command assigns permissions such as SELECT or INSERT.
ALLOW, GIVE, and ENABLE are not valid MySQL privilege commands.

---

## **Question 34**

**Q:** What does the following command do?
`GRANT SELECT, INSERT ON sales.* TO 'dataentry'@'localhost';`

**Correct Answer:** Grants SELECT and INSERT permissions on all tables in the *sales* database

**Explanation:**
`sales.*` means "every table within the sales schema."
It does *not* apply server-wide and does not delete or modify privileges beyond those listed.

---

## **Question 35**

**Q:** How can you remove all privileges from a MySQL user *without deleting the user account*?

**Correct Answer:** `REVOKE ALL PRIVILEGES ON *.* FROM 'username'@'localhost';`

**Explanation:**
REVOKE removes permissions but leaves the account intact.
`DROP USER` deletes the account,
`DELETE PRIVILEGES` is not a valid command,
and `RESET PASSWORD` changes only authentication.

---

## **Question 36**

**Q:** Which MySQL command displays the privileges that have been granted to a specific user?

**Correct Answer:** `SHOW GRANTS FOR 'username'@'localhost';`

**Explanation:**
SHOW GRANTS lists all privileges assigned to a user.
`SHOW PRIVILEGES` only lists *possible* privilege types.
Directly querying the mysql system database is not standard practice.

---

## **Question 37**

**Q:** What is the main benefit of creating a role in MySQL?

**Correct Answer:** It allows centralized permission management for multiple users

**Explanation:**
A role bundles privileges together. Assigning a role to users is easier than maintaining privileges individually. Roles do not replace passwords or speed up databases.

---

## **Question 38**

**Q:** Which tool in MySQL Workbench is commonly used to back up a database?

**Correct Answer:** Data Export Utility

**Explanation:**
The Data Export Utility creates SQL dump files for backup.
Performance Dashboard monitors activity,
Query Builder creates SELECT statements,
and Event Scheduler automates tasks.

---

## **Question 39**

**Q:** How does an incremental backup differ from a full backup in MySQL?

**Correct Answer:**
An incremental backup stores only the changes since the last backup, while a full backup captures the entire database

**Explanation:**
Incremental backups are faster and smaller.
Full backups recreate the database from scratch.
Full backups can contain everything—data and structure—while incremental backups require the previous full backup plus all increments.

---

## **Question 40**

**Q:** Which MySQL feature can be used to automate database backups on a schedule?

**Correct Answer:** MySQL Event Scheduler

**Explanation:**
MySQL’s internal Event Scheduler runs recurring SQL tasks.
AUTO BACKUP and RESTORE MANAGER are nonexistent commands.
CRON exists at the OS level, not within MySQL.

---

## **Question 41**

**Q:** In MySQL, what is the main purpose of performing a point-in-time recovery?

**Correct Answer:** To return (restore) the database to the exact condition it was in before a failure or mistake occurred

**Explanation:**
Point-in-time recovery uses a full backup plus binary logs to recreate the precise state the database was in at a specific moment.
It is used for accidental deletes, failed updates, corruption, or system crashes.

---

## **Question 42**

**Q:** Which command is used to restore a MySQL database from a `.sql` backup file?

**Correct Answer:** `mysql -u root -p < backup.sql`

**Explanation:**
Using the `mysql` client with input redirection loads the SQL statements into the server.
`mysqldump` performs backups—not restores.
`SELECT * FROM backup.sql` is invalid.
`restore database` is not a MySQL command.

---

## **Question 43**

**Q:** What is the correct syntax to create a stored procedure in MySQL that accepts an input parameter?

**Correct Answer:**
`CREATE PROCEDURE myProc(IN param1 INT) BEGIN ... END;`

**Explanation:**
Stored procedures use the CREATE PROCEDURE syntax and parameters must be declared as IN, OUT, or INOUT.
`CREATE FUNCTION` requires a return type.
DECLARE PROCEDURE is not valid SQL.
NEW PROCEDURE does not exist.

---

## **Question 44**

**Q:** Which SQL statement is used to execute a stored procedure in MySQL?

**Correct Answer:** `CALL procedureName();`

**Explanation:**
`CALL` is the required keyword to invoke stored procedures.
`EXEC` is used in SQL Server, not MySQL.
RUN and DO do not execute stored procedures.

---

## **Question 45**

**Q:** Which statement clause must be used in a stored function to return a value in MySQL?

**Correct Answer:** RETURN

**Explanation:**
Stored functions *must* use RETURN to send back a single value.
RETURNS defines the return type but not the returned value itself.
OUTPUT, YIELD, RETURN VALUE are not MySQL syntax.

---

## **Question 46**

**Q:** Which statement correctly describes the difference between a stored procedure and a stored function in MySQL?

**Correct Answer:** Functions return a single value, procedures may not return any

**Explanation:**
Functions must return one value and can be used in expressions.
Procedures may return zero or multiple result sets, and cannot be used inline within queries.

---

## **Question 47**

**Q:** Which SQL keyword sequence is used to create a trigger that runs after an INSERT on a table in MySQL?

**Correct Answer:** AFTER INSERT ON table_name

**Explanation:**
Triggers must declare timing (BEFORE/AFTER) and event (INSERT/UPDATE/DELETE).
The other options include invalid trigger syntax.

---

## **Question 48**

**Q:** Which MySQL feature allows you to schedule and run automated recurring tasks?

**Correct Answer:** Events

**Corrected Note:**
Your course marked “Triggers” as correct, but **Events** is actually the correct MySQL feature for scheduled recurring tasks. Triggers respond to table actions, not time-based events.

**Explanation:**
The MySQL Event Scheduler lets you run recurring tasks like backups, cleanup jobs, or data updates at scheduled intervals.

---

## **Question 49**

**Q:** Which MySQL Workbench tool is used to monitor real-time server performance such as memory, connections, and queries?

**Correct Answer:** Performance Dashboard

**Explanation:**
The Performance Dashboard visualizes server resource usage.
Performance Schema is an internal engine tool,
SQL Editor is for writing queries,
Admin Dashboard is not a Workbench component.

---

## **Question 50**

**Q:** What is the primary advantage of creating indexes on columns in a MySQL table?

**Correct Answer:** They improve query performance by speeding up search operations

**Explanation:**
Indexes create fast lookup paths and reduce the time needed to search through large tables.
They do not compress data or remove NULLs.
Unique indexes can enforce distinctness, but that is not the primary purpose.

---

## **Question 51**

**Q:** Which SQL clause can significantly improve query performance when filtering large datasets?

**Correct Answer:** WHERE

**Explanation:**
The WHERE clause filters rows *before* grouping or sorting, reducing the workload for later stages of query execution.
HAVING filters after grouping, which is slower.
GROUP BY and ORDER BY organize results, not filter them.
