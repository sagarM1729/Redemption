<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 🔥 Top 30 SQL Interview Questions for Freshers (Basic to Advanced) 💪

Alright, same deal here—SQL isn't just some "nice to have" skill, it's MANDATORY for any developer worth their salt. You can't hide behind frameworks or libraries when the interviewer asks you to write a JOIN. Know this stuff cold or watch better candidates take your job. 💀

## ⚡ Basic SQL Fundamentals (Questions 1-10)

**1. What is SQL and why is it important? 🗄️**

SQL (Structured Query Language) is a standardized programming language specifically designed for managing and manipulating relational databases. It's crucial because nearly every application needs to store, retrieve, and manage data efficiently in structured tables.

**2. What is the difference between SQL and MySQL? 🤔**

SQL is the standard language/syntax used to interact with databases. MySQL is a specific Relational Database Management System (RDBMS) that implements SQL. Other RDBMSs include PostgreSQL, Oracle, SQL Server—all use SQL but with slight variations.

**3. What are the different types of SQL commands? 📋**

DDL (Data Definition Language): CREATE, ALTER, DROP, TRUNCATE—structure definition. DML (Data Manipulation Language): SELECT, INSERT, UPDATE, DELETE—data manipulation. DCL (Data Control Language): GRANT, REVOKE—permissions. TCL (Transaction Control Language): COMMIT, ROLLBACK, SAVEPOINT—transaction management.

**4. What is a Primary Key vs Foreign Key? 🔑**

Primary Key uniquely identifies each record in a table (cannot be NULL, must be unique). Foreign Key is a field in one table that references the Primary Key of another table, establishing relationships between tables.

**5. What is the difference between DELETE, TRUNCATE, and DROP? 🗑️**

DELETE removes specific rows based on WHERE condition, can be rolled back, slower, triggers activate. TRUNCATE removes all rows, faster, minimal logging, cannot be rolled back (in most RDBMSs), resets auto-increment. DROP removes entire table structure and data permanently.

**6. What is normalization in SQL? 📐**

Process of organizing database to reduce redundancy and improve data integrity by dividing large tables into smaller, related tables. Forms: 1NF (atomic values), 2NF (no partial dependency), 3NF (no transitive dependency), BCNF (stricter 3NF).

**7. What are SQL Joins? Explain different types. 🔗**

Joins combine rows from two or more tables based on related columns. INNER JOIN (matching rows only), LEFT JOIN (all from left + matching from right), RIGHT JOIN (all from right + matching from left), FULL OUTER JOIN (all rows from both), CROSS JOIN (Cartesian product).

**8. What is the difference between WHERE and HAVING clauses? ⚖️**

WHERE filters rows before grouping (used with individual rows). HAVING filters groups after GROUP BY operation (used with aggregate functions). Example: WHERE filters employees, HAVING filters departments based on aggregate conditions like COUNT or AVG.

**9. What is a View in SQL? 👁️**

Virtual table based on a SQL query result set. Doesn't store data physically but shows data from underlying tables. Used for security (restrict access to certain columns), simplification (complex queries as simple views), and data abstraction.

**10. What is the difference between Clustered and Non-Clustered Indexes? 📑**

Clustered Index determines physical order of data in table (only one per table, faster for range queries). Non-Clustered Index creates separate structure with pointers to actual data (multiple allowed per table, faster for specific lookups).

## 🚀 Intermediate Concepts (Questions 11-20)

**11. What is a Transaction in SQL? Explain ACID properties. 💼**

Transaction is a logical unit of work containing one or more SQL statements that execute as a single unit. ACID: Atomicity (all or nothing), Consistency (valid state transitions), Isolation (concurrent transactions don't interfere), Durability (committed changes persist even after system failure).

**12. What are Constraints in SQL? 🛡️**

Rules enforced on table columns to ensure data accuracy and reliability. Types: NOT NULL (no null values), UNIQUE (distinct values), PRIMARY KEY (unique identifier), FOREIGN KEY (referential integrity), CHECK (custom condition), DEFAULT (default value if none provided).

**13. What are Stored Procedures? 🔄**

Pre-compiled SQL code stored in database that can be executed multiple times. Accepts parameters, improves performance (compiled once), enhances security (encapsulation), reduces network traffic, and enables code reusability.

**14. What are Triggers in SQL? ⚡**

Special stored procedures that automatically execute in response to specific events (INSERT, UPDATE, DELETE) on a table. Types: BEFORE triggers (execute before operation), AFTER triggers (execute after operation). Used for audit logging, validation, maintaining referential integrity.

**15. What is the difference between UNION and UNION ALL? ➕**

UNION combines result sets from multiple SELECT statements and removes duplicate rows (slower due to deduplication). UNION ALL combines all rows including duplicates (faster, no deduplication overhead). Both require same number of columns with compatible data types.

**16. What are Aggregate Functions in SQL? 📊**

Functions that perform calculations on multiple rows and return single value. Common ones: COUNT (number of rows), SUM (total), AVG (average), MIN (minimum), MAX (maximum). Used with GROUP BY to calculate values for each group.

**17. Explain GROUP BY and ORDER BY clauses. 📈**

GROUP BY groups rows with same values into summary rows (used with aggregate functions). ORDER BY sorts result set in ascending (ASC) or descending (DESC) order. You can GROUP BY department and ORDER BY average salary.

**18. What is denormalization? When would you use it? ⚡**

Intentionally introducing redundancy by merging tables to improve read performance at the cost of write performance and storage. Used in data warehousing, reporting systems, or high-read scenarios where query speed is critical and data updates are infrequent.

**19. What are SQL functions? Explain Scalar vs Aggregate. 🔧**

SQL functions perform operations and return values. Scalar functions return single value for each row (UPPER, LOWER, LEN, ROUND, NOW). Aggregate functions operate on multiple rows and return single summary value (COUNT, SUM, AVG, MIN, MAX).

**20. What is a Subquery? What are nested and correlated subqueries? 🎯**

Subquery is a query nested inside another query. Nested subquery executes once and passes result to outer query. Correlated subquery executes for each row of outer query, referencing outer query columns (slower, row-by-row execution).

## 💎 Advanced Topics (Questions 21-30)

**21. What are Window Functions? Explain with examples. 🪟**

Functions that perform calculations across a set of rows related to current row without collapsing results like GROUP BY. Examples: ROW_NUMBER() (assigns unique number), RANK() (ranking with gaps), DENSE_RANK() (ranking without gaps), LAG/LEAD (access previous/next rows), SUM() OVER() (running totals).

**22. What is indexing strategy? When to create indexes? 📚**

Systematic approach to creating indexes for optimal performance. Create indexes on: columns in WHERE clauses, JOIN conditions, ORDER BY columns, frequently searched columns. Avoid on: small tables, columns with frequent updates, low-cardinality columns (few distinct values). Too many indexes slow down INSERT/UPDATE/DELETE.

**23. What is query optimization? List techniques. ⚙️**

Process of improving query performance. Techniques: use indexes properly, avoid SELECT *, use WHERE instead of HAVING when possible, use JOINs instead of subqueries when appropriate, avoid functions on indexed columns in WHERE, use EXPLAIN/EXPLAIN ANALYZE to understand execution plans, partition large tables.

**24. What are Cursors in SQL? 🖱️**

Database objects that retrieve and process rows one at a time (row-by-row processing). Slower than set-based operations but useful when you need procedural logic for each row. Steps: DECLARE → OPEN → FETCH → CLOSE → DEALLOCATE. Avoid when set-based operations can achieve same result.

**25. What are the transaction isolation levels? 🔐**

Define how concurrent transactions interact. Levels (least to most strict): READ UNCOMMITTED (dirty reads possible), READ COMMITTED (only committed data visible), REPEATABLE READ (consistent reads within transaction), SERIALIZABLE (complete isolation, slowest). Higher isolation = more consistency, less concurrency.

**26. What are materialized views? 💎**

Pre-computed, physically stored query results that act like tables. Unlike regular views (virtual), materialized views store actual data, dramatically improving query performance for complex calculations or aggregations. Need periodic refresh to sync with source data.

**27. How do you handle NULL values in SQL? 🚫**

NULL represents missing or unknown data. Functions: IS NULL / IS NOT NULL (check for nulls), COALESCE(col1, col2, default) (return first non-null), IFNULL/ISNULL (replace null with value), NULLIF (return null if values equal). Remember: NULL != NULL, use IS NULL not = NULL.

**28. What are table partitions in SQL? 🔪**

Dividing large tables into smaller, manageable pieces (partitions) based on column values (range, list, hash). Benefits: improved query performance (partition pruning), easier maintenance (drop old partitions), better manageability. Example: partition sales table by year or region.

**29. How do you prevent SQL Injection attacks? 🛡️**

Security vulnerability where attackers insert malicious SQL code. Prevention: use parameterized queries/prepared statements (NEVER concatenate user input), use ORM frameworks, validate and sanitize input, apply principle of least privilege, use stored procedures, escape special characters.

**30. What is database replication? Explain types. 🔄**

Copying and maintaining database objects in multiple databases for redundancy, load distribution, and high availability. Types: Master-Slave (one-way replication), Master-Master (bidirectional), Snapshot (periodic full copy), Transactional (real-time changes), Merge (offline changes synchronized).

***

**💡 Brutal truth:** Knowing syntax isn't enough. You need to write queries that execute in milliseconds, not minutes. Understand execution plans, index usage, and when to denormalize. If you can't explain WHY your query is slow or HOW to fix it, you're not SQL-proficient—you're just copying from Stack Overflow. Practice on real datasets with millions of rows, not toy examples with 10 records. 🎯

<div align="center">⁂</div>


