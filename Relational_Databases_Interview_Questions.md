# 🎯 Relational Database Interview Questions — Part 8 (Questions Only)
## MS SQL Server · MySQL · PostgreSQL · Oracle · YugabyteDB

> **Scope:** RDBMS fundamentals, SQL (DDL/DML/DQL/DCL/TCL), normalization, keys & constraints, joins, subqueries, CTEs, window functions, indexes, execution plans, transactions, isolation & locking, stored procedures, functions, triggers, cursors (including **REF CURSOR / SYS_REFCURSOR in Oracle** and **refcursor in PostgreSQL/pgAdmin**), exception handling, **PostgreSQL JSONB & JSON functions**, **bulk loading** (SQL Server **user-defined table types / TVPs**, `SqlBulkCopy`, MySQL loading lakhs of rows from Excel/CSV), connection pooling, performance tuning, security, backup/replication/HA, **YugabyteDB distributed SQL**, calling DB objects from .NET, query-writing questions and scenario-based questions.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks heavily use Oracle, SQL Server, PostgreSQL), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Tools referenced:** SSMS, pgAdmin, MySQL Workbench, Oracle SQL Developer, DBeaver, ysqlsh.

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies
**DB tags:** `[MSSQL]` `[MySQL]` `[PG]` `[Oracle]` `[YB]` `[All]`

---

## 📚 Table of Contents

**Part A — RDBMS & SQL Fundamentals (All Databases)**
1. RDBMS Fundamentals
2. Data Types
3. Keys & Constraints
4. Normalization & Denormalization
5. SQL Command Categories (DDL, DML, DQL, DCL, TCL)
6. SELECT, Filtering, Sorting & Aggregation
7. Joins
8. Subqueries, EXISTS & Set Operations
9. CTEs & Recursive Queries
10. Window (Analytic) Functions
11. Views & Materialized Views
12. Indexes
13. Query Execution Plans & Optimization
14. Transactions & ACID
15. Isolation Levels, Concurrency & MVCC
16. Locking & Deadlocks
17. Stored Procedures (General Concepts)
18. Functions (General Concepts)
19. Triggers (General Concepts)
20. Cursors (General Concepts)
21. Exception & Error Handling (General Concepts)
22. Temporary Tables, Table Variables & Sequences
23. Dynamic SQL & SQL Injection
24. Partitioning & Sharding
25. Connection Pooling
26. Security, Users, Roles & Privileges
27. Backup, Restore, Replication & High Availability

**Part B — Microsoft SQL Server**
28. SQL Server Architecture & Basics
29. T-SQL Programming
30. Stored Procedures, Functions & Triggers in SQL Server
31. Cursors in SQL Server
32. Error Handling — TRY/CATCH, THROW, RAISERROR
33. User-Defined Table Types & Table-Valued Parameters (Bulk Insert 10K–50K+ Rows)
34. Bulk Loading — BULK INSERT, BCP, SqlBulkCopy, OPENROWSET, SSIS
35. Indexing & Performance in SQL Server
36. Transactions, Isolation & Locking in SQL Server
37. JSON & XML in SQL Server
38. SQL Server HA/DR, Security & Administration

**Part C — MySQL**
39. MySQL Architecture & Storage Engines
40. MySQL Data Types & SQL Specifics
41. Stored Procedures, Functions, Triggers & Events in MySQL
42. Cursors & Error Handling (DECLARE HANDLER, SIGNAL) in MySQL
43. Bulk Loading Lakhs of Rows from Excel/CSV into MySQL
44. Indexing, Performance & EXPLAIN in MySQL
45. Transactions, Isolation & Locking in MySQL (InnoDB)
46. JSON in MySQL
47. MySQL Replication, HA & Administration

**Part D — PostgreSQL**
48. PostgreSQL Architecture & Basics
49. PostgreSQL Data Types & SQL Specifics
50. PL/pgSQL — Functions & Procedures
51. REF CURSOR (refcursor) in PostgreSQL & pgAdmin
52. Exception Handling in PL/pgSQL
53. Triggers in PostgreSQL
54. JSON & JSONB in PostgreSQL
55. Indexing in PostgreSQL (B-tree, GIN, GiST, BRIN, partial, expression)
56. MVCC, VACUUM, Autovacuum & Bloat
57. Performance & EXPLAIN ANALYZE in PostgreSQL
58. Bulk Loading in PostgreSQL (COPY, \copy, unnest, Npgsql binary import)
59. Connection Pooling in PostgreSQL (PgBouncer, Npgsql pooling)
60. Partitioning, Replication & HA in PostgreSQL
61. pgAdmin & PostgreSQL Tooling

**Part E — Oracle**
62. Oracle Architecture & Basics
63. Oracle Data Types & SQL Specifics
64. PL/SQL Fundamentals
65. Stored Procedures, Functions & Packages in Oracle
66. REF CURSOR & SYS_REFCURSOR in Oracle
67. Explicit & Implicit Cursors in Oracle
68. Exception Handling in PL/SQL
69. Triggers in Oracle
70. Bulk Processing — BULK COLLECT, FORALL, Collections
71. Indexing, Optimizer & Performance in Oracle
72. Transactions, Locking & Concurrency in Oracle
73. JSON in Oracle
74. Oracle HA, Backup & Administration

**Part F — YugabyteDB (Distributed SQL)**
75. YugabyteDB Fundamentals
76. YugabyteDB Architecture (YQL, DocDB, Tablets, Raft)
77. Sharding, Tablets & Colocation
78. YSQL vs PostgreSQL — Compatibility & Differences
79. Transactions & Consistency in YugabyteDB
80. Indexing & Performance in YugabyteDB
81. Stored Procedures, Functions, refcursor & JSONB in YugabyteDB
82. Connection Management, Smart Drivers & Pooling in YugabyteDB
83. Replication, Multi-Region, Backup & Operations in YugabyteDB
84. Migrating from PostgreSQL to YugabyteDB

**Part G — Cross-Database Comparisons & .NET Integration**
85. MSSQL vs MySQL vs PostgreSQL vs Oracle vs YugabyteDB
86. Calling Procedures, Functions, refcursors & Bulk Loads from .NET

**Part H — Practice**
87. Financial-Domain Database Questions 💰
88. SQL Query Writing Questions
89. Stored Procedure / Function / Cursor Writing Tasks
90. Tricky Questions
91. Predict the Output (SQL Snippets)
92. Scenario-Based Questions — Design & Development
93. Scenario-Based Questions — Performance & Production Issues
94. Scenario-Based Questions — Bulk Data & Migration
95. Rapid-Fire Round

---

# Part A — RDBMS & SQL Fundamentals

## 1. RDBMS Fundamentals

1. 🟢 `[All]` What is a database? What is a DBMS? What is an RDBMS?
2. 🟢 `[All]` What is the difference between DBMS and RDBMS?
3. 🟢 `[All]` What are tables, rows (tuples) and columns (attributes)?
4. 🟢 `[All]` What are Codd's rules (high level)?
5. 🟢 `[All]` What is a schema? What is the difference between a database and a schema in SQL Server, MySQL, PostgreSQL and Oracle?
6. 🟢 `[All]` What is an instance vs a database (especially in Oracle and PostgreSQL)?
7. 🟢 `[All]` What is metadata / the data dictionary / system catalog?
8. 🟢 `[All]` What is `INFORMATION_SCHEMA`? Which databases support it?
9. 🟡 `[All]` What is the difference between OLTP and OLAP?
10. 🟡 `[All]` What is the difference between SQL and NoSQL databases? When would you choose each?
11. 🟡 `[All]` What is distributed SQL / NewSQL? Where does YugabyteDB fit?
12. 🟡 `[All]` What is the difference between a row-store and a column-store?
13. 🟡 `[All]` What is ANSI SQL? How do vendor dialects (T-SQL, PL/SQL, PL/pgSQL, MySQL SQL) differ from it?
14. 🟡 `[All]` What is the logical order of execution of a SQL `SELECT` query?

---

## 2. Data Types

15. 🟢 `[All]` What are the main categories of data types (numeric, character, date/time, binary, boolean, JSON, UUID)?
16. 🟢 `[All]` What is the difference between `CHAR` and `VARCHAR`?
17. 🟢 `[MSSQL]` What is the difference between `VARCHAR` and `NVARCHAR`? When does Unicode matter?
18. 🟢 `[Oracle]` What is the difference between `VARCHAR2`, `NVARCHAR2` and `CHAR` in Oracle? Why not `VARCHAR`?
19. 🟡 `[All]` What is the difference between `DECIMAL/NUMERIC`, `FLOAT/REAL/DOUBLE` and `MONEY`? Which should you use for money? 💰
20. 🟡 `[Oracle]` How does Oracle's `NUMBER(p,s)` work?
21. 🟡 `[All]` What are the integer types and their ranges (`TINYINT`, `SMALLINT`, `INT`, `BIGINT`)?
22. 🟡 `[All]` What are the date/time types in each database (`DATE`, `DATETIME`, `DATETIME2`, `DATETIMEOFFSET`, `TIMESTAMP`, `TIMESTAMPTZ`, `TIMESTAMP WITH TIME ZONE`)?
23. 🟡 `[Oracle]` Why does Oracle's `DATE` include a time component?
24. 🟡 `[PG]` What is the difference between `timestamp` and `timestamptz` in PostgreSQL?
25. 🟡 `[MySQL]` What is the difference between `DATETIME` and `TIMESTAMP` in MySQL (time zone conversion, range, 2038 problem)?
26. 🟡 `[All]` How is boolean represented in each database (`BIT`, `TINYINT(1)`, `BOOLEAN`, Oracle 23ai `BOOLEAN`)?
27. 🟡 `[All]` How are large objects stored (`VARCHAR(MAX)`, `VARBINARY(MAX)`, `TEXT`, `BLOB`, `CLOB`, `BYTEA`)?
28. 🟡 `[All]` How are UUIDs/GUIDs stored (`UNIQUEIDENTIFIER`, `UUID`, `RAW(16)`, `BINARY(16)`)?
29. 🟡 `[MySQL]` What does `INT(11)` mean in MySQL? Does the number limit the value?
30. 🟡 `[MySQL]` What is the difference between `utf8` and `utf8mb4` in MySQL?
31. 🔴 `[All]` What problems arise from implicit data type conversions in WHERE clauses?

---

## 3. Keys & Constraints

32. 🟢 `[All]` What is a primary key?
33. 🟢 `[All]` What is a foreign key?
34. 🟢 `[All]` What is a unique key? Difference between primary key and unique key?
35. 🟢 `[All]` How many NULLs can a unique constraint allow in SQL Server vs PostgreSQL vs MySQL vs Oracle?
36. 🟢 `[All]` What is a candidate key, alternate key, composite key, super key?
37. 🟢 `[All]` What is a surrogate key vs a natural key? Pros and cons?
38. 🟢 `[All]` What are NOT NULL, CHECK and DEFAULT constraints?
39. 🟡 `[All]` What are referential actions (`ON DELETE CASCADE`, `SET NULL`, `NO ACTION`, `RESTRICT`)?
40. 🟡 `[All]` What is the difference between `NO ACTION` and `RESTRICT`?
41. 🟡 `[PG]` `[Oracle]` What are deferrable constraints? When are they useful?
42. 🟡 `[All]` How do you auto-generate keys (`IDENTITY`, `AUTO_INCREMENT`, `SERIAL`, `GENERATED AS IDENTITY`, sequences)?
43. 🟡 `[PG]` What is the difference between `SERIAL` and `GENERATED ALWAYS AS IDENTITY` in PostgreSQL?
44. 🟡 `[All]` Does a foreign key automatically create an index? In which databases?
45. 🔴 `[All]` What are the performance implications of foreign keys on large inserts and deletes?
46. 🔴 `[YB]` Why can sequential/auto-increment primary keys be a problem in distributed databases like YugabyteDB?

---

## 4. Normalization & Denormalization

47. 🟢 `[All]` What is normalization? Why is it needed?
48. 🟢 `[All]` What are insertion, update and deletion anomalies?
49. 🟢 `[All]` Explain 1NF, 2NF and 3NF with examples.
50. 🟡 `[All]` What is BCNF? How is it different from 3NF?
51. 🟡 `[All]` What are 4NF and 5NF (high level)?
52. 🟡 `[All]` What is functional dependency, partial dependency and transitive dependency?
53. 🟡 `[All]` What is denormalization? When is it appropriate?
54. 🟡 `[All]` What are star schema and snowflake schema?
55. 🟡 `[All]` What are fact tables and dimension tables? What is a slowly changing dimension (SCD Type 1/2)?
56. 🔴 `[All]` How do you design tables for a banking system (customers, accounts, transactions, ledger)? 💰

---

## 5. SQL Command Categories

57. 🟢 `[All]` What are DDL, DML, DQL, DCL and TCL? Give examples of each.
58. 🟢 `[All]` What is the difference between `DELETE`, `TRUNCATE` and `DROP`?
59. 🟡 `[All]` Can `TRUNCATE` be rolled back in SQL Server, PostgreSQL, MySQL and Oracle?
60. 🟡 `[All]` Does `TRUNCATE` reset identity/auto-increment values? Does it fire triggers?
61. 🟡 `[Oracle]` `[MySQL]` Why does DDL cause an implicit commit in Oracle and MySQL? Is DDL transactional in PostgreSQL and SQL Server?
62. 🟢 `[All]` What is the difference between `UPDATE` and `MERGE`/`UPSERT`?
63. 🟡 `[All]` How do you perform an upsert in each database (`MERGE`, `INSERT ... ON DUPLICATE KEY UPDATE`, `INSERT ... ON CONFLICT`)?
64. 🟡 `[All]` What is the `RETURNING` / `OUTPUT` clause? Which databases support it?
65. 🟡 `[All]` What are `GRANT` and `REVOKE`?
66. 🟡 `[All]` What are `COMMIT`, `ROLLBACK` and `SAVEPOINT`?

---

## 6. SELECT, Filtering, Sorting & Aggregation

67. 🟢 `[All]` What is the difference between `WHERE` and `HAVING`?
68. 🟢 `[All]` What is `GROUP BY`? Can you select a non-aggregated column not in `GROUP BY`? (MySQL `ONLY_FULL_GROUP_BY`)
69. 🟢 `[All]` What are aggregate functions? How do they treat NULLs?
70. 🟢 `[All]` What is the difference between `COUNT(*)`, `COUNT(1)` and `COUNT(column)`?
71. 🟢 `[All]` What is `DISTINCT`? Difference between `DISTINCT` and `GROUP BY`?
72. 🟢 `[All]` What are `LIKE`, `IN`, `BETWEEN`, `IS NULL` operators?
73. 🟢 `[All]` Why is `col = NULL` wrong? How does three-valued logic work?
74. 🟢 `[All]` What are `COALESCE`, `ISNULL`, `IFNULL`, `NVL`, `NVL2` and `NULLIF`?
75. 🟢 `[All]` How do you limit rows in each database (`TOP`, `LIMIT`, `FETCH FIRST`, `ROWNUM`, `OFFSET ... FETCH`)?
76. 🟡 `[All]` How do you implement pagination in each database? What is keyset (seek) pagination?
77. 🟡 `[All]` How are NULLs sorted in each database? What is `NULLS FIRST/LAST`?
78. 🟡 `[All]` What are `CASE` expressions? Simple vs searched CASE?
79. 🟡 `[All]` What are `GROUPING SETS`, `ROLLUP` and `CUBE`?
80. 🟡 `[All]` What is `PIVOT` / `UNPIVOT`? How do you pivot in PostgreSQL and MySQL (conditional aggregation, `crosstab`)?
81. 🟡 `[All]` How do you concatenate strings across rows (`STRING_AGG`, `GROUP_CONCAT`, `LISTAGG`)?
82. 🟡 `[All]` What are common string, date and conversion functions in each database?
83. 🟡 `[All]` What is collation? How does it affect comparisons and sorting (case and accent sensitivity)?

---

## 7. Joins

84. 🟢 `[All]` What are joins? Explain INNER, LEFT, RIGHT, FULL OUTER, CROSS and SELF joins.
85. 🟢 `[All]` What is the difference between a LEFT JOIN and an INNER JOIN in terms of results?
86. 🟡 `[All]` What happens when you put a condition on the right table in the `WHERE` clause vs the `ON` clause of a LEFT JOIN?
87. 🟡 `[MySQL]` Does MySQL support FULL OUTER JOIN? How do you emulate it?
88. 🟡 `[All]` What is a natural join? Why is it risky?
89. 🟡 `[All]` What are equi-joins and non-equi joins?
90. 🟡 `[All]` What is an anti-join and a semi-join?
91. 🟡 `[MSSQL]` `[Oracle]` `[PG]` What are `CROSS APPLY`/`OUTER APPLY` and `LATERAL` joins?
92. 🟡 `[Oracle]` What is the old Oracle `(+)` outer join syntax?
93. 🔴 `[All]` What join algorithms do databases use (nested loop, hash join, merge join)? When is each chosen?
94. 🔴 `[All]` How many rows are produced when joining tables with duplicate keys?

---

## 8. Subqueries, EXISTS & Set Operations

95. 🟢 `[All]` What is a subquery? What are scalar, row, table and correlated subqueries?
96. 🟡 `[All]` What is the difference between `IN` and `EXISTS`? Which is faster?
97. 🔴 `[All]` Why does `NOT IN` return no rows when the subquery contains NULL? Why is `NOT EXISTS` safer?
98. 🟢 `[All]` What are `UNION`, `UNION ALL`, `INTERSECT` and `EXCEPT`/`MINUS`?
99. 🟢 `[All]` What is the difference between `UNION` and `UNION ALL`? Which is faster?
100. 🟡 `[All]` What are `ANY`/`SOME` and `ALL` operators?
101. 🟡 `[All]` When should you rewrite a correlated subquery as a join?

---

## 9. CTEs & Recursive Queries

102. 🟢 `[All]` What is a Common Table Expression (CTE)?
103. 🟡 `[All]` What is the difference between a CTE, a derived table, a temp table and a view?
104. 🟡 `[All]` What is a recursive CTE? Write one for an employee-manager hierarchy.
105. 🟡 `[MSSQL]` What is `MAXRECURSION`?
106. 🟡 `[Oracle]` What is `CONNECT BY` / `START WITH` / `LEVEL` / `SYS_CONNECT_BY_PATH` in Oracle?
107. 🟡 `[PG]` Are CTEs materialized in PostgreSQL? What changed in PostgreSQL 12 (`MATERIALIZED` / `NOT MATERIALIZED`)?
108. 🟡 `[MySQL]` Since which MySQL version are CTEs and window functions supported?
109. 🔴 `[All]` Can a CTE be used for DML (`UPDATE`/`DELETE` via CTE, data-modifying CTEs in PostgreSQL)?

---

## 10. Window (Analytic) Functions

110. 🟢 `[All]` What are window functions? How are they different from aggregate functions with `GROUP BY`?
111. 🟢 `[All]` What is the difference between `ROW_NUMBER()`, `RANK()` and `DENSE_RANK()`?
112. 🟡 `[All]` What are `PARTITION BY` and `ORDER BY` in the `OVER()` clause?
113. 🟡 `[All]` What are `LAG()` and `LEAD()`? Give a use case.
114. 🟡 `[All]` What are `FIRST_VALUE()`, `LAST_VALUE()` and `NTH_VALUE()`? Why does `LAST_VALUE` often give unexpected results?
115. 🟡 `[All]` What are window frames (`ROWS BETWEEN`, `RANGE BETWEEN`, `UNBOUNDED PRECEDING`, `CURRENT ROW`)?
116. 🟡 `[All]` What is `NTILE()`? `PERCENT_RANK()`? `CUME_DIST()`?
117. 🟡 `[All]` How do you compute a running total and a moving average with window functions? 💰
118. 🟡 `[All]` Can you use window functions in a `WHERE` clause? How do you filter on them?
119. 🔴 `[All]` How do you solve the "gaps and islands" problem with window functions?

---

## 11. Views & Materialized Views

120. 🟢 `[All]` What is a view? What are its advantages?
121. 🟡 `[All]` Can you insert/update through a view? What are updatable views?
122. 🟡 `[All]` What is `WITH CHECK OPTION`?
123. 🟡 `[MSSQL]` What is an indexed view in SQL Server? What are its requirements (`SCHEMABINDING`)?
124. 🟡 `[PG]` `[Oracle]` What is a materialized view? How do you refresh it (`REFRESH MATERIALIZED VIEW CONCURRENTLY`, Oracle fast refresh/MV logs)?
125. 🟡 `[MySQL]` Does MySQL support materialized views? How do you emulate them?
126. 🔴 `[All]` What are the performance implications of nested views?

---

## 12. Indexes

127. 🟢 `[All]` What is an index? Why does it speed up queries?
128. 🟢 `[All]` What is the difference between a clustered and a non-clustered index?
129. 🟢 `[All]` How many clustered indexes can a table have?
130. 🟡 `[All]` Which databases use clustered tables/index-organized tables (SQL Server clustered index, MySQL InnoDB primary key, Oracle IOT) vs heap tables (PostgreSQL)?
131. 🟡 `[All]` What is a B-tree index? How does it work?
132. 🟡 `[All]` What is a composite index? Why does column order matter (leftmost prefix rule)?
133. 🟡 `[All]` What is a covering index? What are included columns (`INCLUDE`)?
134. 🟡 `[All]` What is a unique index vs a unique constraint?
135. 🟡 `[All]` What is a filtered/partial index?
136. 🟡 `[All]` What is a function-based/expression index?
137. 🟡 `[All]` What are bitmap indexes (Oracle), hash indexes, full-text indexes, columnstore indexes?
138. 🟡 `[All]` What is index selectivity and cardinality?
139. 🟡 `[All]` What are the disadvantages of too many indexes?
140. 🟡 `[All]` What is index fragmentation? How do you rebuild/reorganize indexes?
141. 🟡 `[All]` What is an index seek vs an index scan vs a table scan?
142. 🟡 `[All]` What is a key lookup / bookmark lookup / heap fetch?
143. 🔴 `[All]` When will a database NOT use an index even if one exists (functions on columns, leading wildcard `LIKE '%x'`, implicit conversion, low selectivity, OR conditions)?
144. 🔴 `[All]` What is a SARGable predicate? Give examples of non-SARGable predicates and rewrite them.
145. 🔴 `[All]` How do you index a column used for `ORDER BY ... LIMIT`?
146. 🔴 `[All]` How do you find unused or missing indexes in each database?

---

## 13. Query Execution Plans & Optimization

147. 🟢 `[All]` What is an execution plan? How do you view it in each database (`EXPLAIN`, `EXPLAIN ANALYZE`, SSMS actual plan, `EXPLAIN PLAN FOR`, `DBMS_XPLAN`)?
148. 🟡 `[All]` What is the difference between an estimated and an actual execution plan?
149. 🟡 `[All]` What is a cost-based optimizer? What are statistics? Why do stale statistics cause bad plans?
150. 🟡 `[All]` How do you update statistics in each database (`UPDATE STATISTICS`, `ANALYZE`, `DBMS_STATS`)?
151. 🟡 `[All]` What is parameter sniffing / bind variable peeking? How do you handle it?
152. 🟡 `[All]` What is plan caching? Why do parameterized queries help?
153. 🟡 `[All]` What are query hints? When is it acceptable to use them?
154. 🟡 `[All]` What are the steps you follow to tune a slow query?
155. 🔴 `[All]` What is cardinality estimation and why do bad estimates cause bad joins?
156. 🔴 `[All]` How do you find the top resource-consuming queries in each database (Query Store/DMVs, `pg_stat_statements`, Performance Schema/slow query log, AWR/ASH)?

---

## 14. Transactions & ACID

157. 🟢 `[All]` What is a transaction?
158. 🟢 `[All]` Explain ACID properties with an example. 💰
159. 🟢 `[All]` What are autocommit mode and explicit transactions?
160. 🟡 `[All]` How is autocommit handled by default in SQL Server, MySQL, PostgreSQL and Oracle?
161. 🟡 `[All]` What is a savepoint?
162. 🟡 `[MSSQL]` What are nested transactions in SQL Server? What does `@@TRANCOUNT` show? Does an inner `COMMIT` really commit?
163. 🟡 `[Oracle]` What is an autonomous transaction (`PRAGMA AUTONOMOUS_TRANSACTION`)? Give a use case (audit logging).
164. 🟡 `[PG]` Can you commit inside a PostgreSQL function? What about procedures (PG 11+)?
165. 🔴 `[All]` What is a distributed transaction / two-phase commit? Which databases support it?
166. 🔴 `[All]` What is write-ahead logging (WAL / transaction log / redo log)?

---

## 15. Isolation Levels, Concurrency & MVCC

167. 🟢 `[All]` What are dirty reads, non-repeatable reads and phantom reads?
168. 🟢 `[All]` What are the four ANSI isolation levels?
169. 🟡 `[All]` What is the default isolation level in SQL Server, MySQL InnoDB, PostgreSQL, Oracle and YugabyteDB?
170. 🟡 `[All]` What is MVCC (Multi-Version Concurrency Control)? Which databases use it and how?
171. 🟡 `[MSSQL]` What are `SNAPSHOT` isolation and `READ_COMMITTED_SNAPSHOT` (RCSI) in SQL Server?
172. 🟡 `[MSSQL]` What is `NOLOCK` / `READ UNCOMMITTED`? Why is it dangerous? 💰
173. 🟡 `[Oracle]` Does Oracle support READ UNCOMMITTED? How does Oracle provide read consistency (undo)?
174. 🟡 `[PG]` How does PostgreSQL implement Repeatable Read (snapshot isolation) and Serializable (SSI)?
175. 🟡 `[MySQL]` How does InnoDB's Repeatable Read prevent phantoms (gap locks, next-key locks)?
176. 🔴 `[All]` What is write skew? Which isolation level prevents it?
177. 🔴 `[All]` What is the lost update problem? How do you prevent it (`SELECT ... FOR UPDATE`, optimistic concurrency, row versions)? 💰
178. 🔴 `[All]` What is serialization failure and why must the application retry?

---

## 16. Locking & Deadlocks

179. 🟢 `[All]` What is locking? Why is it needed?
180. 🟡 `[All]` What are shared, exclusive, update and intent locks?
181. 🟡 `[All]` What is lock granularity (row, page, table)? What is lock escalation (SQL Server)?
182. 🟡 `[All]` What is `SELECT ... FOR UPDATE`? What are `NOWAIT` and `SKIP LOCKED`?
183. 🟡 `[MSSQL]` What are `UPDLOCK`, `HOLDLOCK`, `ROWLOCK`, `READPAST` hints?
184. 🟡 `[All]` What is blocking? How do you find blocking sessions in each database?
185. 🟢 `[All]` What is a deadlock? Give an example.
186. 🟡 `[All]` How does each database detect and resolve deadlocks?
187. 🟡 `[All]` How do you capture and analyze deadlocks (SQL Server deadlock graph/Extended Events, `SHOW ENGINE INNODB STATUS`, PostgreSQL logs, Oracle trace files/ORA-00060)?
188. 🟡 `[All]` How do you prevent deadlocks (consistent ordering, short transactions, proper indexes)?
189. 🔴 `[All]` What are advisory locks (PostgreSQL `pg_advisory_lock`), `sp_getapplock` (SQL Server), `GET_LOCK` (MySQL), `DBMS_LOCK` (Oracle)?
190. 🔴 `[All]` How do you implement a job queue in a relational database safely (`FOR UPDATE SKIP LOCKED`)?

---

## 17. Stored Procedures (General Concepts)

191. 🟢 `[All]` What is a stored procedure?
192. 🟢 `[All]` What are the advantages and disadvantages of stored procedures?
193. 🟢 `[All]` What are IN, OUT and INOUT parameters?
194. 🟡 `[All]` Can a stored procedure return multiple result sets? How in each database?
195. 🟡 `[All]` Can a stored procedure call another stored procedure? Is recursion allowed?
196. 🟡 `[All]` How do you return a status code or error from a procedure?
197. 🟡 `[All]` How do you debug stored procedures in SSMS, pgAdmin, MySQL Workbench and SQL Developer?
198. 🟡 `[All]` How do you version-control and deploy stored procedures (migrations, Flyway, Liquibase, DbUp, SSDT)?
199. 🔴 `[All]` Business logic in stored procedures vs application code — what is your opinion and why?
200. 🔴 `[All]` How do you write a stored procedure that is safe to call concurrently?

---

## 18. Functions (General Concepts)

201. 🟢 `[All]` What is a user-defined function?
202. 🟢 `[All]` What is the difference between a stored procedure and a function? (asked in almost every interview)
203. 🟡 `[All]` What are scalar functions, inline table-valued functions and multi-statement table-valued functions?
204. 🟡 `[All]` Can a function modify data? In which databases?
205. 🟡 `[All]` Can a function use transactions or call stored procedures?
206. 🟡 `[All]` What are deterministic vs non-deterministic functions?
207. 🟡 `[PG]` What are `IMMUTABLE`, `STABLE` and `VOLATILE` function categories in PostgreSQL?
208. 🔴 `[All]` Why can scalar functions in a `SELECT` or `WHERE` hurt performance?

---

## 19. Triggers (General Concepts)

209. 🟢 `[All]` What is a trigger?
210. 🟢 `[All]` What are BEFORE, AFTER and INSTEAD OF triggers?
211. 🟡 `[All]` What are row-level vs statement-level triggers?
212. 🟡 `[All]` What are DDL triggers and logon triggers?
213. 🟡 `[All]` What are common use cases for triggers (auditing, validation, derived columns)?
214. 🟡 `[All]` What are the disadvantages of triggers (hidden logic, performance, recursion)?
215. 🟡 `[All]` What are recursive and nested triggers? How do you prevent infinite recursion?
216. 🔴 `[All]` How do triggers behave during bulk loads? How do you disable them temporarily?
217. 🔴 `[All]` Trigger-based auditing vs CDC vs temporal tables — which would you choose? 💰

---

## 20. Cursors (General Concepts)

218. 🟢 `[All]` What is a cursor?
219. 🟢 `[All]` What are the steps to use a cursor (DECLARE, OPEN, FETCH, CLOSE, DEALLOCATE)?
220. 🟡 `[All]` Why are cursors considered slow? What is the set-based alternative?
221. 🟡 `[All]` When is a cursor actually justified?
222. 🟡 `[All]` What are implicit vs explicit cursors?
223. 🟡 `[All]` What is a REF CURSOR / refcursor? Why is it used to return result sets from procedures?
224. 🟡 `[All]` What is the difference between a static cursor and a dynamic cursor?
225. 🔴 `[All]` What are the memory and locking implications of long-open cursors?

---

## 21. Exception & Error Handling (General Concepts)

226. 🟢 `[All]` How do you handle errors in stored procedures in each database?
227. 🟡 `[All]` What is the difference between raising a user-defined error and a system error?
228. 🟡 `[All]` How do you roll back a transaction when an error occurs inside a procedure?
229. 🟡 `[All]` How do you log errors to an error table without losing the log on rollback?
230. 🟡 `[All]` How do you re-throw an error after logging it?
231. 🔴 `[All]` What happens to an open transaction when an unhandled error occurs in each database?

---

## 22. Temporary Tables, Table Variables & Sequences

232. 🟢 `[All]` What are temporary tables? How do they work in each database?
233. 🟡 `[MSSQL]` What is the difference between `#temp`, `##temp` and `@table` variables?
234. 🟡 `[Oracle]` What are Global Temporary Tables (`ON COMMIT DELETE ROWS` / `PRESERVE ROWS`) and private temporary tables?
235. 🟡 `[PG]` How do temp tables work in PostgreSQL (`ON COMMIT DROP`)? What is the catalog bloat issue?
236. 🟡 `[MySQL]` What are the limitations of temporary tables in MySQL (cannot be referred to twice in the same query in older versions)?
237. 🟡 `[All]` What is a sequence? How is it different from identity?
238. 🟡 `[All]` What are sequence caching and gaps? Why are gaps normal?

---

## 23. Dynamic SQL & SQL Injection

239. 🟢 `[All]` What is dynamic SQL?
240. 🟡 `[MSSQL]` What is the difference between `EXEC()` and `sp_executesql`?
241. 🟡 `[PG]` How do you run dynamic SQL in PL/pgSQL (`EXECUTE ... USING`, `format()` with `%I` and `%L`)?
242. 🟡 `[Oracle]` What is `EXECUTE IMMEDIATE` and `DBMS_SQL`?
243. 🟡 `[MySQL]` How do you run dynamic SQL in MySQL (`PREPARE`, `EXECUTE`, `DEALLOCATE PREPARE`)?
244. 🟡 `[All]` What is SQL injection? How can it happen even inside stored procedures?
245. 🟡 `[All]` How do you safely use dynamic table or column names (`QUOTENAME`, `quote_ident`, `DBMS_ASSERT`)?

---

## 24. Partitioning & Sharding

246. 🟡 `[All]` What is table partitioning? What are its benefits?
247. 🟡 `[All]` What are range, list and hash partitioning?
248. 🟡 `[All]` How is partitioning implemented in each database (SQL Server partition functions/schemes, PostgreSQL declarative partitioning, MySQL partitioning, Oracle partitioning, YugabyteDB tablets + partitioning)?
249. 🟡 `[All]` What is partition pruning?
250. 🟡 `[All]` What is partition switching / attach / detach and how does it help archiving? 💰
251. 🟡 `[All]` What is the difference between partitioning and sharding?
252. 🔴 `[All]` How do you choose a partition key for a transactions table? 💰
253. 🔴 `[All]` What happens to queries that don't include the partition key?

---

## 25. Connection Pooling

254. 🟢 `[All]` What is connection pooling? Why is it important?
255. 🟡 `[All]` Where can pooling happen — client driver (ADO.NET, Npgsql, MySqlConnector, ODP.NET) vs server-side/proxy (PgBouncer, ProxySQL, Oracle DRCP, YSQL Connection Manager)?
256. 🟡 `[All]` What is the cost of opening a database connection in PostgreSQL (process per connection) vs SQL Server/MySQL (thread per connection)?
257. 🟡 `[All]` What are typical pool settings (min/max pool size, idle timeout, connection lifetime)?
258. 🟡 `[All]` What causes "connection pool exhausted" / "too many connections" errors?
259. 🟡 `[MySQL]` What is `max_connections` in MySQL and PostgreSQL? What happens when it's exceeded?
260. 🔴 `[All]` How do you size a connection pool? Why is "more connections" not always faster?
261. 🔴 `[All]` How does connection pooling interact with session state (temp tables, session variables, `SET` options, prepared statements)?

---

## 26. Security, Users, Roles & Privileges

262. 🟢 `[All]` What is the difference between a login, a user, a role and a schema?
263. 🟡 `[All]` How do you grant least-privilege access to an application account?
264. 🟡 `[All]` What is row-level security (SQL Server RLS, PostgreSQL RLS policies, Oracle VPD)? 💰
265. 🟡 `[All]` What is data masking (Dynamic Data Masking, Oracle Data Redaction)? 💰
266. 🟡 `[All]` What is Transparent Data Encryption (TDE)? 💰
267. 🟡 `[MSSQL]` What is Always Encrypted? 💰
268. 🟡 `[All]` How do you audit database access (SQL Server Audit, pgAudit, Oracle Unified Auditing, MySQL Enterprise Audit)? 💰
269. 🟡 `[All]` What is `SECURITY DEFINER` vs `SECURITY INVOKER` (PostgreSQL), `EXECUTE AS` (SQL Server), definer's rights vs invoker's rights (Oracle `AUTHID`)?
270. 🔴 `[All]` How do you secure stored procedures so that users can execute them but not access tables directly?

---

## 27. Backup, Restore, Replication & High Availability

271. 🟢 `[All]` What types of backups exist (full, differential, incremental, log)?
272. 🟡 `[All]` What are RPO and RTO? 💰
273. 🟡 `[All]` What is point-in-time recovery (PITR)?
274. 🟡 `[All]` What are the recovery models in SQL Server (Simple, Full, Bulk-Logged)?
275. 🟡 `[All]` What is replication? Synchronous vs asynchronous replication?
276. 🟡 `[All]` What is a read replica? What is replication lag?
277. 🟡 `[All]` What are HA options in each database (SQL Server Always On AG/FCI/log shipping, MySQL Group Replication/InnoDB Cluster, PostgreSQL streaming replication/Patroni, Oracle Data Guard/RAC, YugabyteDB Raft replication/xCluster)?
278. 🔴 `[All]` How do you test that backups can actually be restored?

---

# Part B — Microsoft SQL Server

## 28. SQL Server Architecture & Basics

279. 🟢 `[MSSQL]` What are the main components of SQL Server architecture (relational engine, storage engine, SQLOS)?
280. 🟢 `[MSSQL]` What are system databases (`master`, `model`, `msdb`, `tempdb`, `resource`)?
281. 🟡 `[MSSQL]` What are data files (`.mdf`, `.ndf`) and log files (`.ldf`)?
282. 🟡 `[MSSQL]` What are pages and extents?
283. 🟡 `[MSSQL]` What is `tempdb` used for? Why is it a common bottleneck?
284. 🟡 `[MSSQL]` What is the buffer pool?
285. 🟡 `[MSSQL]` What are DMVs (Dynamic Management Views)? Name useful ones.
286. 🟡 `[MSSQL]` What are SQL Server editions (Express, Standard, Enterprise, Developer) and Azure SQL options?
287. 🟡 `[MSSQL]` What is SQL Server Agent?
288. 🔴 `[MSSQL]` What is the transaction log and VLFs? Why does the log file grow?

---

## 29. T-SQL Programming

289. 🟢 `[MSSQL]` What is T-SQL?
290. 🟢 `[MSSQL]` How do you declare variables and use control-of-flow (`IF`, `WHILE`, `BEGIN...END`, `BREAK`, `CONTINUE`)?
291. 🟡 `[MSSQL]` What is `SET NOCOUNT ON` and why use it in procedures?
292. 🟡 `[MSSQL]` What is the difference between `SET` and `SELECT` for variable assignment?
293. 🟡 `[MSSQL]` What are `@@ROWCOUNT`, `@@ERROR`, `@@IDENTITY`, `SCOPE_IDENTITY()` and `IDENT_CURRENT()`?
294. 🟡 `[MSSQL]` What is the `OUTPUT` clause? How do you capture inserted IDs for multiple rows?
295. 🟡 `[MSSQL]` How does `MERGE` work? What are its known issues and race conditions?
296. 🟡 `[MSSQL]` What are `CROSS APPLY` and `OUTER APPLY`?
297. 🟡 `[MSSQL]` What are `TRY_CAST`, `TRY_CONVERT`, `TRY_PARSE`?
298. 🟡 `[MSSQL]` What is `STRING_SPLIT` and `STRING_AGG`?
299. 🟡 `[MSSQL]` What are synonyms?
300. 🟡 `[MSSQL]` What are temporal (system-versioned) tables? 💰
301. 🔴 `[MSSQL]` What is `SET XACT_ABORT ON` and why is it recommended in procedures with transactions?

---

## 30. Stored Procedures, Functions & Triggers in SQL Server

302. 🟢 `[MSSQL]` How do you create a stored procedure with input and output parameters?
303. 🟢 `[MSSQL]` How do you return a value using `RETURN` vs an `OUTPUT` parameter vs a result set?
304. 🟡 `[MSSQL]` What are scalar functions, inline TVFs and multi-statement TVFs? Which is fastest?
305. 🟡 `[MSSQL]` What is scalar UDF inlining (SQL Server 2019+)?
306. 🟡 `[MSSQL]` Can you call a stored procedure inside a function? Why not?
307. 🟡 `[MSSQL]` What are `WITH RECOMPILE`, `OPTION (RECOMPILE)` and `OPTIMIZE FOR`?
308. 🟡 `[MSSQL]` What is `WITH SCHEMABINDING`?
309. 🟡 `[MSSQL]` What are `inserted` and `deleted` tables in triggers?
310. 🟡 `[MSSQL]` Why must SQL Server triggers be written to handle multiple rows?
311. 🟡 `[MSSQL]` What is an `INSTEAD OF` trigger on a view?
312. 🟡 `[MSSQL]` What are DDL triggers and logon triggers?
313. 🔴 `[MSSQL]` What is a CLR stored procedure? When would you use it?
314. 🔴 `[MSSQL]` What is natively compiled stored procedure (In-Memory OLTP)?

---

## 31. Cursors in SQL Server

315. 🟢 `[MSSQL]` How do you write a cursor in T-SQL?
316. 🟡 `[MSSQL]` What are cursor types (`STATIC`, `DYNAMIC`, `KEYSET`, `FAST_FORWARD`, `FORWARD_ONLY`, `READ_ONLY`)?
317. 🟡 `[MSSQL]` What is `@@FETCH_STATUS`?
318. 🟡 `[MSSQL]` What is `LOCAL` vs `GLOBAL` cursor?
319. 🟡 `[MSSQL]` How do you replace a cursor with a set-based solution or a `WHILE` loop over a temp table?
320. 🔴 `[MSSQL]` Does SQL Server support REF CURSOR like Oracle? How do you return result sets instead (`CURSOR VARYING OUTPUT`, result sets)?

---

## 32. Error Handling — TRY/CATCH, THROW, RAISERROR

321. 🟢 `[MSSQL]` How does `TRY...CATCH` work in SQL Server?
322. 🟡 `[MSSQL]` What are `ERROR_NUMBER()`, `ERROR_MESSAGE()`, `ERROR_SEVERITY()`, `ERROR_STATE()`, `ERROR_LINE()`, `ERROR_PROCEDURE()`?
323. 🟡 `[MSSQL]` What is the difference between `RAISERROR` and `THROW`?
324. 🟡 `[MSSQL]` What is `XACT_STATE()`? How do you handle uncommittable transactions?
325. 🟡 `[MSSQL]` Which errors are not caught by `TRY...CATCH` (compile errors, severity ≥ 20, some object name resolution errors)?
326. 🟡 `[MSSQL]` How do you write a standard error-handling template for a procedure with a transaction?
327. 🔴 `[MSSQL]` How do you log errors to a table when the transaction is rolled back (table variables survive rollback)?

---

## 33. User-Defined Table Types & Table-Valued Parameters (Bulk Insert 10K–50K+ Rows)

328. 🟢 `[MSSQL]` What is a user-defined table type (`CREATE TYPE ... AS TABLE`)?
329. 🟢 `[MSSQL]` What is a table-valued parameter (TVP)?
330. 🟡 `[MSSQL]` How do you pass 10,000–50,000 rows from C# to a stored procedure using a TVP (`DataTable`, `IEnumerable<SqlDataRecord>`, `SqlDbType.Structured`, `TypeName`)?
331. 🟡 `[MSSQL]` Why must a TVP parameter be declared `READONLY`?
332. 🟡 `[MSSQL]` Can you add a primary key, unique constraint or index to a table type?
333. 🟡 `[MSSQL]` How do you insert from a TVP into a real table with validation and duplicate checks?
334. 🟡 `[MSSQL]` How do you upsert using a TVP and `MERGE` (or `UPDATE` + `INSERT ... WHERE NOT EXISTS`)?
335. 🟡 `[MSSQL]` How do you return validation errors per row from a TVP-based bulk insert?
336. 🟡 `[MSSQL]` How do you return generated identity values mapped to input rows (`MERGE ... OUTPUT`)?
337. 🟡 `[MSSQL]` Can you alter a user-defined table type? What must you do to change it?
338. 🔴 `[MSSQL]` TVP vs `SqlBulkCopy` vs batched `INSERT` vs JSON/XML parameter — which is best for 10K, 50K, 1 lakh and 10 lakh rows?
339. 🔴 `[MSSQL]` What are the performance characteristics of TVPs (cardinality estimation, table variable deferred compilation in SQL Server 2019)?
340. 🔴 `[MSSQL]` How do you split very large inputs into chunks and handle partial failures?
341. 🔴 `[MSSQL]` How do you insert a parent table and child table (e.g., orders and order items) in one call using two TVPs? 💰
342. 🔴 `[MSSQL]` How does a TVP behave inside a transaction and with triggers on the target table?

---

## 34. Bulk Loading — BULK INSERT, BCP, SqlBulkCopy, OPENROWSET, SSIS

343. 🟡 `[MSSQL]` What is `BULK INSERT`? What are its options (`FIELDTERMINATOR`, `ROWTERMINATOR`, `FIRSTROW`, `BATCHSIZE`, `TABLOCK`, `FORMAT='CSV'`)?
344. 🟡 `[MSSQL]` What is the `bcp` utility?
345. 🟡 `[MSSQL]` What is `SqlBulkCopy` in .NET and how does it compare with TVPs?
346. 🟡 `[MSSQL]` How do you import an Excel file into SQL Server (Import Wizard, `OPENROWSET`/ACE OLEDB, SSIS, C# with ClosedXML/EPPlus + SqlBulkCopy)?
347. 🟡 `[MSSQL]` What is minimal logging? When does bulk load get minimally logged?
348. 🟡 `[MSSQL]` Why load into a staging table first and then merge into the target?
349. 🔴 `[MSSQL]` How do you load 10 million rows fast (disable/rebuild indexes, `TABLOCK`, batch size, bulk-logged recovery)?
350. 🔴 `[MSSQL]` How do you handle bad rows during bulk load (`ERRORFILE`, `MAXERRORS`)?
351. 🟡 `[MSSQL]` What is SSIS and when would you use it?

---

## 35. Indexing & Performance in SQL Server

352. 🟡 `[MSSQL]` What is a clustered index? Why choose a narrow, unique, ever-increasing key?
353. 🟡 `[MSSQL]` What are heaps and forwarded records?
354. 🟡 `[MSSQL]` What are included columns?
355. 🟡 `[MSSQL]` What are filtered indexes?
356. 🟡 `[MSSQL]` What are columnstore indexes? When are they useful?
357. 🟡 `[MSSQL]` What is fill factor and page splits?
358. 🟡 `[MSSQL]` How do you check index fragmentation (`sys.dm_db_index_physical_stats`)? Reorganize vs rebuild?
359. 🟡 `[MSSQL]` What is Query Store?
360. 🟡 `[MSSQL]` What are missing index DMVs and why shouldn't you blindly create them?
361. 🟡 `[MSSQL]` What are wait statistics? Name common wait types (`PAGEIOLATCH`, `LCK_M_X`, `CXPACKET`, `WRITELOG`, `ASYNC_NETWORK_IO`).
362. 🟡 `[MSSQL]` What is MAXDOP and Cost Threshold for Parallelism?
363. 🔴 `[MSSQL]` What is Intelligent Query Processing / Parameter Sensitive Plan optimization (SQL Server 2022)?
364. 🔴 `[MSSQL]` What causes tempdb contention and how do you fix it?

---

## 36. Transactions, Isolation & Locking in SQL Server

365. 🟡 `[MSSQL]` What is the default isolation level in SQL Server? In Azure SQL Database (RCSI on)?
366. 🟡 `[MSSQL]` What is the difference between `SNAPSHOT` and `READ_COMMITTED_SNAPSHOT`?
367. 🟡 `[MSSQL]` What is lock escalation? How do you control it?
368. 🟡 `[MSSQL]` How do you find blocking (`sp_who2`, `sys.dm_exec_requests`, `sp_WhoIsActive`)?
369. 🟡 `[MSSQL]` How do you capture deadlocks (system_health Extended Events)?
370. 🔴 `[MSSQL]` What is the "MERGE + HOLDLOCK" upsert pattern and why is it needed?
371. 🔴 `[MSSQL]` How do you implement a safe "check balance and debit" in T-SQL? 💰

---

## 37. JSON & XML in SQL Server

372. 🟡 `[MSSQL]` How do you store JSON in SQL Server (`NVARCHAR(MAX)`, native `json` type in SQL Server 2025/Azure)?
373. 🟡 `[MSSQL]` What are `JSON_VALUE`, `JSON_QUERY`, `OPENJSON`, `ISJSON`, `JSON_MODIFY`?
374. 🟡 `[MSSQL]` How do you return query results as JSON (`FOR JSON PATH`, `FOR JSON AUTO`)?
375. 🟡 `[MSSQL]` How do you index JSON properties (computed columns + index)?
376. 🟡 `[MSSQL]` How do you pass a JSON array from C# to a procedure and insert it with `OPENJSON` (alternative to TVP)?
377. 🟡 `[MSSQL]` What are `FOR XML` and the `xml` data type methods (`value`, `query`, `nodes`)?

---

## 38. SQL Server HA/DR, Security & Administration

378. 🟡 `[MSSQL]` What are Always On Availability Groups? Readable secondaries?
379. 🟡 `[MSSQL]` What is log shipping? Database mirroring (deprecated)?
380. 🟡 `[MSSQL]` What is a Failover Cluster Instance?
381. 🟡 `[MSSQL]` What are Windows authentication vs SQL authentication vs Entra ID authentication?
382. 🟡 `[MSSQL]` What are database roles (`db_owner`, `db_datareader`, `db_datawriter`)?
383. 🟡 `[MSSQL]` What are maintenance plans / Ola Hallengren scripts?
384. 🟡 `[MSSQL]` What is CDC (Change Data Capture) and Change Tracking in SQL Server?
385. 🔴 `[MSSQL]` What is the difference between Azure SQL Database, Azure SQL Managed Instance and SQL Server on VM?

---

# Part C — MySQL

## 39. MySQL Architecture & Storage Engines

386. 🟢 `[MySQL]` What is MySQL? What are its main components?
387. 🟢 `[MySQL]` What are storage engines? What is the difference between InnoDB and MyISAM?
388. 🟡 `[MySQL]` Why is InnoDB the default engine?
389. 🟡 `[MySQL]` What is the InnoDB buffer pool (`innodb_buffer_pool_size`)?
390. 🟡 `[MySQL]` What are the redo log, undo log and binary log (binlog)?
391. 🟡 `[MySQL]` What is the InnoDB clustered index (primary key) and secondary index structure?
392. 🟡 `[MySQL]` What happens if an InnoDB table has no primary key?
393. 🟡 `[MySQL]` What is `innodb_flush_log_at_trx_commit` and `sync_binlog`? Durability vs performance? 💰
394. 🟡 `[MySQL]` MySQL vs MariaDB vs Percona Server vs Amazon Aurora MySQL?
395. 🟡 `[MySQL]` What are SQL modes (`STRICT_TRANS_TABLES`, `ONLY_FULL_GROUP_BY`, `NO_ZERO_DATE`)?

---

## 40. MySQL Data Types & SQL Specifics

396. 🟡 `[MySQL]` What are `ENUM` and `SET` types? Pros and cons?
397. 🟡 `[MySQL]` What is `AUTO_INCREMENT`? What is `LAST_INSERT_ID()`?
398. 🟡 `[MySQL]` What is `INSERT ... ON DUPLICATE KEY UPDATE`? What is `REPLACE INTO` and why is it dangerous?
399. 🟡 `[MySQL]` What is `INSERT IGNORE`?
400. 🟡 `[MySQL]` What is `LIMIT offset, count`? Why is large offset slow?
401. 🟡 `[MySQL]` What are generated (virtual/stored) columns?
402. 🟡 `[MySQL]` How are case sensitivity of table names and string comparisons controlled (`lower_case_table_names`, collations)?
403. 🟡 `[MySQL]` What are MySQL user variables (`@var`) vs local variables (`DECLARE`)?

---

## 41. Stored Procedures, Functions, Triggers & Events in MySQL

404. 🟢 `[MySQL]` How do you create a stored procedure in MySQL? Why do you change the `DELIMITER`?
405. 🟢 `[MySQL]` What are IN, OUT and INOUT parameters in MySQL?
406. 🟡 `[MySQL]` How do you return multiple result sets from a MySQL procedure?
407. 🟡 `[MySQL]` How do you create a function in MySQL? What are `DETERMINISTIC`, `READS SQL DATA`, `NO SQL`?
408. 🟡 `[MySQL]` Why might function creation fail with binary logging enabled (`log_bin_trust_function_creators`)?
409. 🟡 `[MySQL]` What triggers does MySQL support (BEFORE/AFTER INSERT/UPDATE/DELETE, row-level only)? What are `NEW` and `OLD`?
410. 🟡 `[MySQL]` Can a MySQL trigger modify the same table that fired it?
411. 🟡 `[MySQL]` What is the MySQL Event Scheduler?
412. 🟡 `[MySQL]` How do you loop in MySQL procedures (`LOOP`, `WHILE`, `REPEAT`, `LEAVE`, `ITERATE`)?
413. 🔴 `[MySQL]` What is the `DEFINER` clause and what problems does it cause during migration?

---

## 42. Cursors & Error Handling in MySQL

414. 🟢 `[MySQL]` How do you write a cursor in MySQL?
415. 🟡 `[MySQL]` What is `DECLARE CONTINUE HANDLER FOR NOT FOUND` and why is it needed with cursors?
416. 🟡 `[MySQL]` What is the required order of declarations (variables, conditions, cursors, handlers)?
417. 🟡 `[MySQL]` What are MySQL cursor limitations (read-only, non-scrollable, asensitive)?
418. 🟡 `[MySQL]` Does MySQL support REF CURSOR? How do you return result sets instead?
419. 🟡 `[MySQL]` What are `DECLARE ... HANDLER` types (`CONTINUE`, `EXIT`) and conditions (`SQLEXCEPTION`, `SQLWARNING`, `NOT FOUND`, SQLSTATE values)?
420. 🟡 `[MySQL]` What are `SIGNAL` and `RESIGNAL`?
421. 🟡 `[MySQL]` What is `GET DIAGNOSTICS`?
422. 🟡 `[MySQL]` How do you write a procedure that rolls back a transaction on any error?

---

## 43. Bulk Loading Lakhs of Rows from Excel/CSV into MySQL

423. 🟢 `[MySQL]` How do you import an Excel file into MySQL? Why do you usually convert it to CSV first?
424. 🟡 `[MySQL]` What is `LOAD DATA INFILE` vs `LOAD DATA LOCAL INFILE`?
425. 🟡 `[MySQL]` What are the important `LOAD DATA` options (`FIELDS TERMINATED BY`, `ENCLOSED BY`, `LINES TERMINATED BY`, `IGNORE 1 LINES`, column list, `SET` clause)?
426. 🟡 `[MySQL]` What is `secure_file_priv` and `local_infile`? Why does `LOAD DATA` fail with "The MySQL server is running with the --secure-file-priv option"?
427. 🟡 `[MySQL]` How do you transform values (dates like `dd/MM/yyyy`, empty strings to NULL, trimming) during `LOAD DATA` using user variables and `SET`?
428. 🟡 `[MySQL]` How do you handle Excel issues — date serial numbers, leading zeros in account/mobile numbers, scientific notation, commas in amounts, Unicode/BOM? 💰
429. 🟡 `[MySQL]` How do you handle duplicates during load (`IGNORE`, `REPLACE`, staging table + `INSERT ... ON DUPLICATE KEY UPDATE`)?
430. 🟡 `[MySQL]` How do you import using MySQL Workbench Table Data Import Wizard? Why is it slow for lakhs of rows?
431. 🟡 `[MySQL]` How do you bulk insert from C# (multi-row `INSERT ... VALUES (...),(...)`, `MySqlBulkLoader`, `MySqlBulkCopy` in MySqlConnector)?
432. 🟡 `[MySQL]` What is the optimal batch size for multi-row inserts? What is `max_allowed_packet`?
433. 🟡 `[MySQL]` How do you read Excel files in .NET (EPPlus, ClosedXML, ExcelDataReader, NPOI) and stream rows without loading everything into memory?
434. 🔴 `[MySQL]` How do you speed up loading 10 lakh+ rows (disable unique/foreign key checks, `autocommit=0`, load into a table without secondary indexes, add indexes later)?
435. 🔴 `[MySQL]` How do you validate data and report bad rows back to the user after a bulk upload?
436. 🔴 `[MySQL]` How do you make a bulk upload idempotent (re-upload of the same file should not duplicate data)?
437. 🔴 `[MySQL]` How do you design an "upload Excel → validate → preview → commit" feature for business users?

---

## 44. Indexing, Performance & EXPLAIN in MySQL

438. 🟡 `[MySQL]` How do you read `EXPLAIN` output (`type`, `possible_keys`, `key`, `rows`, `filtered`, `Extra`)?
439. 🟡 `[MySQL]` What are access types (`ALL`, `index`, `range`, `ref`, `eq_ref`, `const`)?
440. 🟡 `[MySQL]` What do `Using filesort`, `Using temporary`, `Using index` mean?
441. 🟡 `[MySQL]` What is `EXPLAIN ANALYZE` (MySQL 8.0.18+)?
442. 🟡 `[MySQL]` What is the slow query log? How do you analyze it (`pt-query-digest`)?
443. 🟡 `[MySQL]` What is the Performance Schema and `sys` schema?
444. 🟡 `[MySQL]` What are invisible indexes and descending indexes in MySQL 8?
445. 🟡 `[MySQL]` What is index condition pushdown and covering index in InnoDB?
446. 🟡 `[MySQL]` Why does a UUID primary key hurt InnoDB performance?
447. 🔴 `[MySQL]` How do you optimize `LIMIT 100000, 20` style pagination?

---

## 45. Transactions, Isolation & Locking in MySQL (InnoDB)

448. 🟡 `[MySQL]` What is the default isolation level in MySQL InnoDB?
449. 🟡 `[MySQL]` What are record locks, gap locks and next-key locks?
450. 🟡 `[MySQL]` Why can an UPDATE without an index lock the entire table in InnoDB?
451. 🟡 `[MySQL]` What is `SELECT ... FOR UPDATE` and `SELECT ... FOR SHARE` / `LOCK IN SHARE MODE`?
452. 🟡 `[MySQL]` How do you view deadlocks in MySQL (`SHOW ENGINE INNODB STATUS`, `innodb_print_all_deadlocks`)?
453. 🟡 `[MySQL]` What is `innodb_lock_wait_timeout`?
454. 🔴 `[MySQL]` Why do MyISAM tables not support transactions, and what happens if you mix MyISAM and InnoDB in a transaction?

---

## 46. JSON in MySQL

455. 🟡 `[MySQL]` What is the `JSON` data type in MySQL?
456. 🟡 `[MySQL]` What are `JSON_EXTRACT`, `->`, `->>`, `JSON_SET`, `JSON_OBJECT`, `JSON_ARRAYAGG`, `JSON_TABLE`?
457. 🟡 `[MySQL]` How do you index JSON fields in MySQL (generated columns, multi-valued indexes)?
458. 🟡 `[MySQL]` How do you return nested JSON from a MySQL query?

---

## 47. MySQL Replication, HA & Administration

459. 🟡 `[MySQL]` How does MySQL replication work (binlog, relay log, source/replica)?
460. 🟡 `[MySQL]` What are statement-based, row-based and mixed binlog formats?
461. 🟡 `[MySQL]` What is GTID-based replication?
462. 🟡 `[MySQL]` What is semi-synchronous replication?
463. 🟡 `[MySQL]` What are Group Replication and InnoDB Cluster?
464. 🟡 `[MySQL]` What is ProxySQL / MySQL Router?
465. 🟡 `[MySQL]` How do you back up MySQL (`mysqldump`, `mysqlpump`, MySQL Shell dump, Percona XtraBackup)?
466. 🔴 `[MySQL]` How do you handle replication lag for read-after-write consistency?

---

# Part D — PostgreSQL

## 48. PostgreSQL Architecture & Basics

467. 🟢 `[PG]` What is PostgreSQL? What are its key features?
468. 🟢 `[PG]` What is the process-based architecture of PostgreSQL (postmaster, backend processes, background workers)?
469. 🟡 `[PG]` What are shared buffers, WAL buffers, work_mem and maintenance_work_mem?
470. 🟡 `[PG]` What is WAL (Write-Ahead Log)? What are checkpoints?
471. 🟡 `[PG]` What is the difference between a cluster, database, schema and tablespace in PostgreSQL?
472. 🟡 `[PG]` What is the `public` schema and `search_path`? What changed in PostgreSQL 15 regarding `public` permissions?
473. 🟡 `[PG]` What are extensions? Name popular ones (`pg_stat_statements`, `pgcrypto`, `uuid-ossp`, `postgis`, `pg_trgm`, `hstore`, `pgvector`, `pg_partman`, `pg_cron`).
474. 🟡 `[PG]` What are system catalogs (`pg_class`, `pg_attribute`, `pg_stat_activity`, `pg_locks`)?
475. 🟡 `[PG]` What is TOAST?
476. 🟡 `[PG]` What is `ctid` and `xmin`/`xmax`?
477. 🔴 `[PG]` What is transaction ID wraparound and why is it dangerous?

---

## 49. PostgreSQL Data Types & SQL Specifics

478. 🟡 `[PG]` What are PostgreSQL-specific data types (arrays, `jsonb`, `uuid`, `inet`, `cidr`, `hstore`, range types, `interval`, enum, composite types, domains)?
479. 🟡 `[PG]` How do you work with arrays (`ANY`, `ARRAY_AGG`, `unnest`)?
480. 🟡 `[PG]` What are composite types and domains? (Can be used like "types" for parameters.)
481. 🟡 `[PG]` What is `INSERT ... ON CONFLICT DO UPDATE / DO NOTHING`?
482. 🟡 `[PG]` What is `RETURNING`?
483. 🟡 `[PG]` What is `DISTINCT ON`?
484. 🟡 `[PG]` What is `ILIKE`? What are `SIMILAR TO` and regex operators (`~`, `~*`)?
485. 🟡 `[PG]` What is `generate_series()`?
486. 🟡 `[PG]` What is `MERGE` in PostgreSQL 15+? How is it different from `ON CONFLICT`?
487. 🟡 `[PG]` How does case sensitivity of identifiers work (quoted vs unquoted names)?
488. 🟡 `[PG]` What is the `::` cast operator?

---

## 50. PL/pgSQL — Functions & Procedures

489. 🟢 `[PG]` What is PL/pgSQL?
490. 🟢 `[PG]` How do you create a function in PostgreSQL (`CREATE OR REPLACE FUNCTION ... RETURNS ... LANGUAGE plpgsql`)?
491. 🟢 `[PG]` What is the difference between a function and a procedure in PostgreSQL (PG 11+ `CREATE PROCEDURE`, `CALL`, transaction control)?
492. 🟡 `[PG]` What is dollar quoting (`$$`)?
493. 🟡 `[PG]` What are the block structure parts (`DECLARE`, `BEGIN`, `EXCEPTION`, `END`)?
494. 🟡 `[PG]` How do you return a single value, a row, a set of rows (`RETURNS SETOF`, `RETURNS TABLE`), and a refcursor?
495. 🟡 `[PG]` What are `RETURN QUERY`, `RETURN NEXT` and `RETURN`?
496. 🟡 `[PG]` What are `%TYPE` and `%ROWTYPE` in PL/pgSQL?
497. 🟡 `[PG]` What are `IN`, `OUT`, `INOUT` and `VARIADIC` parameters?
498. 🟡 `[PG]` What is function overloading in PostgreSQL? What problems does it cause when dropping functions?
499. 🟡 `[PG]` What are `FOUND`, `GET DIAGNOSTICS ... ROW_COUNT`?
500. 🟡 `[PG]` What are `PERFORM` and `SELECT INTO` (`STRICT`)?
501. 🟡 `[PG]` How do you loop (`FOR rec IN query LOOP`, `FOREACH ... IN ARRAY`, `WHILE`, `LOOP ... EXIT WHEN`)?
502. 🟡 `[PG]` What are `IMMUTABLE`, `STABLE`, `VOLATILE`, `STRICT`, `PARALLEL SAFE`, `SECURITY DEFINER`?
503. 🟡 `[PG]` What are SQL-language functions vs PL/pgSQL functions? Which can be inlined?
504. 🟡 `[PG]` How do you call a procedure with OUT parameters?
505. 🔴 `[PG]` Can a function `COMMIT` or `ROLLBACK`? Can a procedure? When can't a procedure commit (called inside a transaction block)?
506. 🔴 `[PG]` How do you pass an array or a JSON array of rows into a function for bulk insert?

---

## 51. REF CURSOR (refcursor) in PostgreSQL & pgAdmin

507. 🟢 `[PG]` What is a `refcursor` in PostgreSQL?
508. 🟡 `[PG]` How do you write a function that returns a `refcursor`?
509. 🟡 `[PG]` How do you write a procedure with an `INOUT refcursor` parameter?
510. 🟡 `[PG]` How do you return multiple result sets from one function/procedure using multiple refcursors?
511. 🟡 `[PG]` What is a bound vs unbound cursor variable (`CURSOR FOR query` vs `refcursor`)?
512. 🟡 `[PG]` What are `OPEN ... FOR`, `OPEN ... FOR EXECUTE`, `FETCH`, `MOVE`, `CLOSE`?
513. 🟡 `[PG]` Why must a refcursor be fetched inside the same transaction? What happens after `COMMIT`?
514. 🟡 `[PG]` How do you fetch data from a refcursor in pgAdmin / psql (`BEGIN; SELECT func('mycur'); FETCH ALL IN "mycur"; COMMIT;`)?
515. 🟡 `[PG]` Why does pgAdmin show only `<unnamed portal 1>` when you call a refcursor function?
516. 🟡 `[PG]` How do you name the cursor (portal) explicitly instead of getting `<unnamed portal N>`?
517. 🟡 `[PG]` What is `WITH HOLD` cursor? When would you use it?
518. 🟡 `[PG]` What are `SCROLL` and `NO SCROLL` cursors?
519. 🟡 `[PG]` How do you read refcursor results from .NET using Npgsql (transaction + `FETCH ALL`)? What changed in Npgsql regarding automatic refcursor dereferencing?
520. 🔴 `[PG]` refcursor vs `RETURNS TABLE` vs `RETURNS SETOF` vs returning JSON — which would you choose and why?
521. 🔴 `[PG]` What are the performance and connection-pooling implications of refcursors (open portal ties up the connection, PgBouncer transaction mode)?
522. 🔴 `[PG]` How do you migrate Oracle procedures that return `SYS_REFCURSOR` to PostgreSQL?

---

## 52. Exception Handling in PL/pgSQL

523. 🟢 `[PG]` How do you handle exceptions in PL/pgSQL (`EXCEPTION WHEN ... THEN`)?
524. 🟡 `[PG]` What are common condition names (`unique_violation`, `foreign_key_violation`, `no_data_found`, `too_many_rows`, `division_by_zero`, `others`)?
525. 🟡 `[PG]` What is SQLSTATE? How do you catch errors by SQLSTATE code?
526. 🟡 `[PG]` What are `SQLERRM` and `GET STACKED DIAGNOSTICS` (`MESSAGE_TEXT`, `PG_EXCEPTION_DETAIL`, `PG_EXCEPTION_CONTEXT`)?
527. 🟡 `[PG]` How do you raise errors and messages (`RAISE NOTICE`, `RAISE WARNING`, `RAISE EXCEPTION ... USING ERRCODE, DETAIL, HINT`)?
528. 🟡 `[PG]` What happens to changes made inside a `BEGIN ... EXCEPTION` block when an exception is caught (implicit savepoint rollback)?
529. 🔴 `[PG]` What is the performance cost of `EXCEPTION` blocks (subtransactions) inside loops?
530. 🔴 `[PG]` How do you log errors to a table even if the main transaction rolls back (dblink / `pg_background` / logging from the application)?
531. 🟡 `[PG]` What is `ASSERT` in PL/pgSQL?
532. 🟡 `[PG]` How do PostgreSQL errors appear in .NET (`PostgresException`, `SqlState`)?

---

## 53. Triggers in PostgreSQL

533. 🟡 `[PG]` How do you create a trigger in PostgreSQL (trigger function returning `trigger` + `CREATE TRIGGER`)?
534. 🟡 `[PG]` What are `NEW`, `OLD`, `TG_OP`, `TG_TABLE_NAME`, `TG_WHEN`, `TG_LEVEL`?
535. 🟡 `[PG]` What should a BEFORE row trigger return? What happens if it returns NULL?
536. 🟡 `[PG]` What are statement-level triggers with transition tables (`REFERENCING NEW TABLE AS`)?
537. 🟡 `[PG]` What are `INSTEAD OF` triggers on views?
538. 🟡 `[PG]` What are constraint triggers and deferred triggers?
539. 🟡 `[PG]` What are event triggers (DDL)?
540. 🟡 `[PG]` How do you write a generic audit trigger that stores old/new rows as JSONB? 💰
541. 🟡 `[PG]` How do you auto-update an `updated_at` column with a trigger?

---

## 54. JSON & JSONB in PostgreSQL

542. 🟢 `[PG]` What is the difference between `json` and `jsonb`?
543. 🟢 `[PG]` When should you use `jsonb` instead of relational columns? When not?
544. 🟡 `[PG]` What are the JSON operators `->`, `->>`, `#>`, `#>>`?
545. 🟡 `[PG]` What are the JSONB operators `@>`, `<@`, `?`, `?|`, `?&`, `||`, `-`, `#-`?
546. 🟡 `[PG]` How do you build JSON objects and arrays (`json_build_object`, `jsonb_build_object`, `json_agg`, `jsonb_agg`, `row_to_json`, `to_jsonb`, `json_object_agg`)?
547. 🟡 `[PG]` How do you return nested JSON (e.g., customer with list of orders) from a single query/function?
548. 🟡 `[PG]` How do you expand JSON into rows (`jsonb_array_elements`, `jsonb_each`, `jsonb_to_record`, `jsonb_to_recordset`, `jsonb_populate_recordset`)?
549. 🟡 `[PG]` How do you update a value inside JSONB (`jsonb_set`, `jsonb_insert`, `||`, subscripting in PG 14+ `data['key'] = ...`)?
550. 🟡 `[PG]` How do you remove a key from JSONB?
551. 🟡 `[PG]` What is SQL/JSON path (`jsonb_path_query`, `@?`, `@@`)?
552. 🟡 `[PG]` What are the SQL/JSON standard functions in PostgreSQL 16/17 (`JSON_TABLE`, `JSON_VALUE`, `JSON_QUERY`, `JSON_EXISTS`, `IS JSON`)?
553. 🟡 `[PG]` How do you index JSONB (GIN with `jsonb_ops` vs `jsonb_path_ops`, expression B-tree index on `data->>'key'`)?
554. 🟡 `[PG]` Which queries can use a GIN index on JSONB and which cannot?
555. 🟡 `[PG]` How do you pass a JSON array from C# to a PostgreSQL function and bulk insert it (`jsonb_to_recordset` / `jsonb_populate_recordset`)?
556. 🟡 `[PG]` How do you write a function that accepts a JSON object as input and returns a JSON object as output (API-style function)?
557. 🟡 `[PG]` How do you validate JSON structure in PostgreSQL (CHECK constraints, `jsonb_typeof`, `IS JSON`)?
558. 🔴 `[PG]` What are the performance pitfalls of large JSONB documents (TOAST, full rewrite on update)?
559. 🔴 `[PG]` How do you map JSONB columns in .NET (Npgsql, EF Core `ToJson`, `JsonDocument`, POCO mapping)?
560. 🔴 `[PG]` How do you query "all customers whose JSON address city is Pune and who have a tag 'premium'" efficiently?

---

## 55. Indexing in PostgreSQL

561. 🟡 `[PG]` What index types does PostgreSQL support (B-tree, Hash, GIN, GiST, SP-GiST, BRIN)?
562. 🟡 `[PG]` When would you use GIN? GiST? BRIN?
563. 🟡 `[PG]` What are partial indexes? Give an example (`WHERE is_active`).
564. 🟡 `[PG]` What are expression indexes (`lower(email)`)?
565. 🟡 `[PG]` What are covering indexes (`INCLUDE`) and index-only scans? What role does the visibility map play?
566. 🟡 `[PG]` What is `CREATE INDEX CONCURRENTLY`? What are its caveats?
567. 🟡 `[PG]` What is `pg_trgm` and how does it speed up `LIKE '%text%'` searches?
568. 🟡 `[PG]` What is full-text search in PostgreSQL (`tsvector`, `tsquery`, GIN)?
569. 🟡 `[PG]` Why does PostgreSQL not have clustered indexes like SQL Server? What does `CLUSTER` do?
570. 🔴 `[PG]` How do you find unused and duplicate indexes (`pg_stat_user_indexes`)?
571. 🔴 `[PG]` What is index bloat and how do you fix it (`REINDEX CONCURRENTLY`, `pg_repack`)?

---

## 56. MVCC, VACUUM, Autovacuum & Bloat

572. 🟡 `[PG]` How does MVCC work in PostgreSQL (tuple versions, `xmin`, `xmax`)?
573. 🟡 `[PG]` Why does an `UPDATE` in PostgreSQL create a new row version?
574. 🟡 `[PG]` What are dead tuples?
575. 🟡 `[PG]` What does `VACUUM` do? What is `VACUUM FULL`? Why is `VACUUM FULL` dangerous in production?
576. 🟡 `[PG]` What is autovacuum? How do you tune it?
577. 🟡 `[PG]` What is `ANALYZE`?
578. 🟡 `[PG]` What is table bloat? How do you detect and fix it?
579. 🟡 `[PG]` What are HOT updates (Heap-Only Tuples)? How does fillfactor help?
580. 🔴 `[PG]` How can a long-running transaction or idle-in-transaction session prevent vacuum and cause bloat?
581. 🔴 `[PG]` What is `idle_in_transaction_session_timeout` and `statement_timeout`?

---

## 57. Performance & EXPLAIN ANALYZE in PostgreSQL

582. 🟡 `[PG]` How do you read `EXPLAIN (ANALYZE, BUFFERS)` output?
583. 🟡 `[PG]` What are Seq Scan, Index Scan, Index Only Scan, Bitmap Heap Scan?
584. 🟡 `[PG]` What are Nested Loop, Hash Join and Merge Join nodes?
585. 🟡 `[PG]` What do "rows=" estimate vs actual differences tell you?
586. 🟡 `[PG]` What is `pg_stat_statements`? How do you find the slowest queries?
587. 🟡 `[PG]` How do you find blocking queries (`pg_stat_activity`, `pg_locks`, `pg_blocking_pids`)?
588. 🟡 `[PG]` How do you kill a query or session (`pg_cancel_backend`, `pg_terminate_backend`)?
589. 🟡 `[PG]` What is `work_mem` and how does it affect sorts and hash joins?
590. 🟡 `[PG]` What is `random_page_cost` and `effective_cache_size`?
591. 🟡 `[PG]` What is parallel query in PostgreSQL?
592. 🔴 `[PG]` What are generic vs custom plans for prepared statements (`plan_cache_mode`)?
593. 🔴 `[PG]` How do you tune PostgreSQL for an OLTP banking workload? 💰

---

## 58. Bulk Loading in PostgreSQL

594. 🟢 `[PG]` What is `COPY` in PostgreSQL? How is it different from `\copy` in psql?
595. 🟡 `[PG]` How do you load a CSV exported from Excel using `COPY ... FROM ... WITH (FORMAT csv, HEADER true, DELIMITER ',', NULL '')`?
596. 🟡 `[PG]` How do you import CSV using pgAdmin's Import/Export dialog?
597. 🟡 `[PG]` How do you bulk insert from .NET using Npgsql binary COPY (`BeginBinaryImport`)?
598. 🟡 `[PG]` How do you bulk insert using arrays and `unnest()` in a single statement?
599. 🟡 `[PG]` How do you bulk insert using a JSON array and `jsonb_to_recordset`?
600. 🟡 `[PG]` How do you do a bulk upsert (COPY into staging/temp table, then `INSERT ... ON CONFLICT`)?
601. 🟡 `[PG]` What are unlogged tables and when are they useful for staging?
602. 🔴 `[PG]` How do you load 1 crore rows quickly (drop/disable indexes, `COPY`, larger `maintenance_work_mem`, `ANALYZE` after load)?
603. 🔴 `[PG]` How do you handle bad rows in `COPY` (PostgreSQL 17 `ON_ERROR ignore`, staging with text columns)?

---

## 59. Connection Pooling in PostgreSQL

604. 🟡 `[PG]` Why is connection pooling especially important in PostgreSQL?
605. 🟡 `[PG]` How does Npgsql connection pooling work (`Pooling`, `Minimum Pool Size`, `Maximum Pool Size`, `Connection Idle Lifetime`)?
606. 🟡 `[PG]` What is PgBouncer? What are session, transaction and statement pooling modes?
607. 🟡 `[PG]` Which features break in PgBouncer transaction mode (session variables, prepared statements in older versions, advisory locks, `LISTEN/NOTIFY`, `WITH HOLD` cursors, temp tables)?
608. 🟡 `[PG]` What is `No Reset On Close` / `DISCARD ALL`?
609. 🟡 `[PG]` What are alternatives to PgBouncer (Pgpool-II, Odyssey, PgCat, Supavisor, RDS Proxy)?
610. 🔴 `[PG]` How do you size `max_connections` and pool sizes for 20 microservices each with multiple pods?

---

## 60. Partitioning, Replication & HA in PostgreSQL

611. 🟡 `[PG]` What is declarative partitioning (range, list, hash) in PostgreSQL?
612. 🟡 `[PG]` How do you create monthly partitions for a transactions table and automate them (`pg_partman`)? 💰
613. 🟡 `[PG]` What are the limitations of partitioned tables (unique constraints must include partition key)?
614. 🟡 `[PG]` What is streaming replication? Physical vs logical replication?
615. 🟡 `[PG]` What are replication slots? What risk do inactive slots create?
616. 🟡 `[PG]` What is a hot standby?
617. 🟡 `[PG]` What is Patroni? How is automatic failover done?
618. 🟡 `[PG]` How do you back up PostgreSQL (`pg_dump`, `pg_dumpall`, `pg_basebackup`, pgBackRest, Barman)?
619. 🟡 `[PG]` What is PITR in PostgreSQL (WAL archiving)?
620. 🔴 `[PG]` What is `LISTEN/NOTIFY` and when would you use it?

---

## 61. pgAdmin & PostgreSQL Tooling

621. 🟢 `[PG]` What is pgAdmin? What can you do with it?
622. 🟡 `[PG]` How do you view the execution plan graphically in pgAdmin?
623. 🟡 `[PG]` How do you debug a PL/pgSQL function in pgAdmin (pldbgapi extension)?
624. 🟡 `[PG]` How do you view server activity, locks and kill sessions in pgAdmin's dashboard?
625. 🟡 `[PG]` How do you back up and restore a database using pgAdmin (custom/tar/plain formats)?
626. 🟡 `[PG]` What is the Query Tool's auto-commit setting in pgAdmin and why does it matter for refcursors?
627. 🟡 `[PG]` What other tools are used (psql, DBeaver, DataGrip, Azure Data Studio)?
628. 🟡 `[PG]` What are useful psql meta-commands (`\d`, `\dt`, `\df`, `\x`, `\timing`, `\copy`, `\i`)?

---

# Part E — Oracle

## 62. Oracle Architecture & Basics

629. 🟢 `[Oracle]` What is the architecture of Oracle (instance = memory + background processes; database = files)?
630. 🟡 `[Oracle]` What are the SGA and PGA? Name SGA components (buffer cache, shared pool, redo log buffer, large pool).
631. 🟡 `[Oracle]` What are background processes (DBWn, LGWR, CKPT, SMON, PMON, ARCn)?
632. 🟡 `[Oracle]` What are datafiles, control files, redo log files and archive logs?
633. 🟡 `[Oracle]` What are tablespaces, segments, extents and blocks?
634. 🟡 `[Oracle]` What is the undo tablespace? What is ORA-01555 "snapshot too old"?
635. 🟡 `[Oracle]` What is a schema in Oracle and how is it related to a user?
636. 🟡 `[Oracle]` What are CDB and PDB (multitenant architecture)?
637. 🟡 `[Oracle]` What is the `DUAL` table?
638. 🟡 `[Oracle]` What are `ROWID` and `ROWNUM`?
639. 🟡 `[Oracle]` What is the listener and `tnsnames.ora`?
640. 🔴 `[Oracle]` What is the shared pool and hard parse vs soft parse? Why do bind variables matter?

---

## 63. Oracle Data Types & SQL Specifics

641. 🟡 `[Oracle]` What is the difference between `ROWNUM` and `ROW_NUMBER()`? Why does `WHERE ROWNUM > 1` return no rows?
642. 🟡 `[Oracle]` How do you paginate in Oracle (12c `OFFSET ... FETCH`, older `ROWNUM` nested query)?
643. 🟡 `[Oracle]` What are sequences (`NEXTVAL`, `CURRVAL`) and identity columns (12c+)?
644. 🟡 `[Oracle]` What is `MERGE` in Oracle?
645. 🟡 `[Oracle]` What are `DECODE`, `NVL`, `NVL2`, `COALESCE`, `NULLIF`?
646. 🟡 `[Oracle]` Why is an empty string treated as NULL in Oracle?
647. 🟡 `[Oracle]` What are `LISTAGG`, `PIVOT`, `UNPIVOT` in Oracle?
648. 🟡 `[Oracle]` What are synonyms (private/public) and database links?
649. 🟡 `[Oracle]` What is flashback query (`AS OF TIMESTAMP`)? 💰
650. 🟡 `[Oracle]` What is `RETURNING INTO`?

---

## 64. PL/SQL Fundamentals

651. 🟢 `[Oracle]` What is PL/SQL? What are its advantages?
652. 🟢 `[Oracle]` What is the structure of a PL/SQL block (DECLARE, BEGIN, EXCEPTION, END)?
653. 🟢 `[Oracle]` What are anonymous blocks vs named blocks?
654. 🟡 `[Oracle]` What are `%TYPE` and `%ROWTYPE`?
655. 🟡 `[Oracle]` What are PL/SQL records?
656. 🟡 `[Oracle]` What are control structures (`IF`, `CASE`, `LOOP`, `WHILE`, `FOR`)?
657. 🟡 `[Oracle]` What is `DBMS_OUTPUT.PUT_LINE`? Why don't you see output in some tools?
658. 🟡 `[Oracle]` What is `SELECT ... INTO`? What exceptions can it raise?
659. 🟡 `[Oracle]` What is context switching between SQL and PL/SQL engines? Why does it matter?
660. 🔴 `[Oracle]` What is `PRAGMA` and name common pragmas (`AUTONOMOUS_TRANSACTION`, `EXCEPTION_INIT`, `SERIALLY_REUSABLE`, `UDF`)?

---

## 65. Stored Procedures, Functions & Packages in Oracle

661. 🟢 `[Oracle]` How do you create a procedure in Oracle with IN, OUT and IN OUT parameters?
662. 🟢 `[Oracle]` How do you create a function in Oracle?
663. 🟡 `[Oracle]` Can an Oracle function perform DML? Can it be called from SQL if it does?
664. 🟡 `[Oracle]` What is a package? What are the package specification and body?
665. 🟡 `[Oracle]` What are the advantages of packages (encapsulation, overloading, state, performance)?
666. 🟡 `[Oracle]` What are package variables and package state? What is ORA-04068 "existing state of packages has been discarded"?
667. 🟡 `[Oracle]` What is overloading in packages?
668. 🟡 `[Oracle]` What is `NOCOPY` hint?
669. 🟡 `[Oracle]` What are pipelined table functions?
670. 🟡 `[Oracle]` What is `DETERMINISTIC` and `RESULT_CACHE` for functions?
671. 🟡 `[Oracle]` What are invalid objects and how do you recompile them?
672. 🔴 `[Oracle]` What are definer's rights vs invoker's rights (`AUTHID CURRENT_USER`)?

---

## 66. REF CURSOR & SYS_REFCURSOR in Oracle

673. 🟢 `[Oracle]` What is a REF CURSOR?
674. 🟢 `[Oracle]` What is `SYS_REFCURSOR`?
675. 🟡 `[Oracle]` What is the difference between a strong REF CURSOR and a weak REF CURSOR?
676. 🟡 `[Oracle]` What is the difference between `SYS_REFCURSOR` and a user-defined `TYPE ... IS REF CURSOR`?
677. 🟡 `[Oracle]` How do you write a procedure that returns a result set using an `OUT SYS_REFCURSOR` parameter?
678. 🟡 `[Oracle]` How do you write a function that returns `SYS_REFCURSOR`?
679. 🟡 `[Oracle]` How do you return multiple result sets using multiple `SYS_REFCURSOR` OUT parameters?
680. 🟡 `[Oracle]` How do you open a REF CURSOR with dynamic SQL (`OPEN cur FOR v_sql USING ...`)?
681. 🟡 `[Oracle]` How do you test a REF CURSOR procedure in SQL Developer / SQL*Plus (`VARIABLE rc REFCURSOR; EXEC proc(:rc); PRINT rc;`)?
682. 🟡 `[Oracle]` How do you consume a REF CURSOR inside another PL/SQL block (`FETCH ... INTO`, `BULK COLLECT`)?
683. 🟡 `[Oracle]` Who should close a REF CURSOR returned to a client? What is ORA-01000 "maximum open cursors exceeded"?
684. 🟡 `[Oracle]` How do you read a REF CURSOR from .NET using ODP.NET (`OracleDbType.RefCursor`, `ParameterDirection.Output`, `ExecuteReader`)?
685. 🔴 `[Oracle]` What is implicit statement results (`DBMS_SQL.RETURN_RESULT`, 12c) and how is it different from REF CURSOR OUT parameters?
686. 🔴 `[Oracle]` REF CURSOR vs pipelined function vs returning a collection — when to use which?
687. 🔴 `[Oracle]` How do you map Oracle `SYS_REFCURSOR` procedures to PostgreSQL `refcursor` during migration (Ora2Pg)?

---

## 67. Explicit & Implicit Cursors in Oracle

688. 🟢 `[Oracle]` What is an implicit cursor? What are `SQL%ROWCOUNT`, `SQL%FOUND`, `SQL%NOTFOUND`, `SQL%ISOPEN`?
689. 🟢 `[Oracle]` What is an explicit cursor? Write the OPEN-FETCH-CLOSE pattern.
690. 🟡 `[Oracle]` What are explicit cursor attributes (`%FOUND`, `%NOTFOUND`, `%ROWCOUNT`, `%ISOPEN`)?
691. 🟡 `[Oracle]` What is a cursor FOR loop? Why is it preferred?
692. 🟡 `[Oracle]` What are parameterized cursors?
693. 🟡 `[Oracle]` What is `SELECT ... FOR UPDATE` cursor with `WHERE CURRENT OF`?
694. 🟡 `[Oracle]` What is a cursor variable vs a cursor?
695. 🔴 `[Oracle]` Why does row-by-row cursor processing perform badly ("slow-by-slow") and how do you fix it with bulk operations?

---

## 68. Exception Handling in PL/SQL

696. 🟢 `[Oracle]` How does exception handling work in PL/SQL?
697. 🟢 `[Oracle]` What are predefined exceptions (`NO_DATA_FOUND`, `TOO_MANY_ROWS`, `ZERO_DIVIDE`, `DUP_VAL_ON_INDEX`, `VALUE_ERROR`, `INVALID_CURSOR`, `CURSOR_ALREADY_OPEN`)?
698. 🟡 `[Oracle]` How do you declare and raise a user-defined exception?
699. 🟡 `[Oracle]` What is `RAISE_APPLICATION_ERROR`? What error number range is allowed (-20000 to -20999)?
700. 🟡 `[Oracle]` What is `PRAGMA EXCEPTION_INIT`?
701. 🟡 `[Oracle]` What are `SQLCODE` and `SQLERRM`? What is `DBMS_UTILITY.FORMAT_ERROR_BACKTRACE`?
702. 🟡 `[Oracle]` What is `WHEN OTHERS` and why is `WHEN OTHERS THEN NULL` considered a bug?
703. 🟡 `[Oracle]` How do exceptions propagate through nested blocks?
704. 🟡 `[Oracle]` What happens to the transaction when an unhandled exception leaves a procedure (statement-level rollback)?
705. 🔴 `[Oracle]` How do you log errors in an autonomous transaction so the log survives rollback? 💰
706. 🔴 `[Oracle]` What is `SAVE EXCEPTIONS` with `FORALL` and `SQL%BULK_EXCEPTIONS`?
707. 🔴 `[Oracle]` What is DML error logging (`LOG ERRORS INTO`)?

---

## 69. Triggers in Oracle

708. 🟡 `[Oracle]` What types of triggers exist in Oracle (row/statement, BEFORE/AFTER, INSTEAD OF, compound, DDL, database event/logon)?
709. 🟡 `[Oracle]` What are `:NEW` and `:OLD`? What is the `REFERENCING` clause?
710. 🟡 `[Oracle]` What is the mutating table error (ORA-04091)? How do you fix it (compound triggers)?
711. 🟡 `[Oracle]` What is a compound trigger?
712. 🟡 `[Oracle]` How do you use a trigger with a sequence to generate IDs (pre-12c)?
713. 🟡 `[Oracle]` How do you enable/disable triggers?
714. 🔴 `[Oracle]` What is trigger firing order (`FOLLOWS`/`PRECEDES`)?

---

## 70. Bulk Processing — BULK COLLECT, FORALL, Collections

715. 🟡 `[Oracle]` What are PL/SQL collections (associative arrays, nested tables, VARRAYs)?
716. 🟡 `[Oracle]` What is `BULK COLLECT`? Why use `LIMIT` with it?
717. 🟡 `[Oracle]` What is `FORALL`? How is it different from a `FOR` loop?
718. 🟡 `[Oracle]` How do you insert 1 lakh rows from a collection using `FORALL`?
719. 🟡 `[Oracle]` What are `INDICES OF` and `VALUES OF` in `FORALL`?
720. 🟡 `[Oracle]` How do you pass an array from .NET to an Oracle procedure (ODP.NET array binding, associative arrays, `ArrayBindCount`)?
721. 🟡 `[Oracle]` What are SQL object types and `TABLE()` operator for passing collections (Oracle's equivalent of TVP)?
722. 🟡 `[Oracle]` What is `INSERT /*+ APPEND */` and direct-path insert?
723. 🟡 `[Oracle]` What is SQL*Loader? What are external tables? How do you load CSV/Excel data into Oracle?
724. 🔴 `[Oracle]` What is the optimal `LIMIT` size for `BULK COLLECT`? What are PGA memory concerns?

---

## 71. Indexing, Optimizer & Performance in Oracle

725. 🟡 `[Oracle]` What index types exist in Oracle (B-tree, bitmap, function-based, reverse key, composite, IOT, invisible)?
726. 🟡 `[Oracle]` When should you use bitmap indexes? Why are they bad for OLTP?
727. 🟡 `[Oracle]` What is a reverse key index and when does it help?
728. 🟡 `[Oracle]` How do you view execution plans (`EXPLAIN PLAN`, `DBMS_XPLAN.DISPLAY`, `DISPLAY_CURSOR`)?
729. 🟡 `[Oracle]` What are AWR, ASH and ADDM reports?
730. 🟡 `[Oracle]` What is `DBMS_STATS.GATHER_TABLE_STATS`?
731. 🟡 `[Oracle]` What are optimizer hints (`/*+ INDEX */`, `/*+ PARALLEL */`, `/*+ LEADING */`)?
732. 🟡 `[Oracle]` What are bind variables and bind peeking / adaptive cursor sharing?
733. 🟡 `[Oracle]` What is the result cache?
734. 🔴 `[Oracle]` What are SQL profiles, SQL plan baselines and SQL Tuning Advisor?

---

## 72. Transactions, Locking & Concurrency in Oracle

735. 🟡 `[Oracle]` What is the default isolation level in Oracle?
736. 🟡 `[Oracle]` How does Oracle achieve "readers don't block writers and writers don't block readers"?
737. 🟡 `[Oracle]` What is `SELECT ... FOR UPDATE NOWAIT / WAIT n / SKIP LOCKED`?
738. 🟡 `[Oracle]` What is ORA-00060 deadlock detected?
739. 🟡 `[Oracle]` How do you find blocking sessions (`v$session`, `v$lock`)?
740. 🟡 `[Oracle]` Does Oracle escalate locks?
741. 🔴 `[Oracle]` What is ORA-08177 "can't serialize access for this transaction"?

---

## 73. JSON in Oracle

742. 🟡 `[Oracle]` How do you store JSON in Oracle (`VARCHAR2`/`CLOB` with `IS JSON`, native `JSON` type in 21c+)?
743. 🟡 `[Oracle]` What are `JSON_VALUE`, `JSON_QUERY`, `JSON_TABLE`, `JSON_EXISTS`, `JSON_OBJECT`, `JSON_ARRAYAGG`?
744. 🟡 `[Oracle]` What are JSON Relational Duality Views (23ai)?
745. 🟡 `[Oracle]` How do you parse JSON in PL/SQL (`JSON_OBJECT_T`, `JSON_ARRAY_T`)?

---

## 74. Oracle HA, Backup & Administration

746. 🟡 `[Oracle]` What is RMAN?
747. 🟡 `[Oracle]` What is Data Guard? Physical vs logical standby?
748. 🟡 `[Oracle]` What is Oracle RAC?
749. 🟡 `[Oracle]` What is ARCHIVELOG mode?
750. 🟡 `[Oracle]` What is Flashback Database / Flashback Table?
751. 🟡 `[Oracle]` What is Data Pump (`expdp`/`impdp`)?
752. 🟡 `[Oracle]` What is Oracle DRCP (Database Resident Connection Pooling)?
753. 🔴 `[Oracle]` What is GoldenGate?

---

# Part F — YugabyteDB (Distributed SQL)

## 75. YugabyteDB Fundamentals

754. 🟢 `[YB]` What is YugabyteDB?
755. 🟢 `[YB]` What is distributed SQL? How is it different from a traditional single-node RDBMS?
756. 🟢 `[YB]` What APIs does YugabyteDB provide (YSQL — PostgreSQL-compatible, YCQL — Cassandra-compatible)?
757. 🟡 `[YB]` Why would an organization move from PostgreSQL to YugabyteDB (horizontal scaling, HA, geo-distribution)?
758. 🟡 `[YB]` What are the trade-offs of YugabyteDB compared to PostgreSQL (latency, compatibility, operational complexity)?
759. 🟡 `[YB]` How does YugabyteDB compare with CockroachDB, Google Spanner, Aurora PostgreSQL and Citus?
760. 🟡 `[YB]` What is YugabyteDB Anywhere and YugabyteDB Aeon (managed)?

---

## 76. YugabyteDB Architecture

761. 🟡 `[YB]` What are the two layers of YugabyteDB (Yugabyte Query Layer — YQL, and DocDB storage layer)?
762. 🟡 `[YB]` What are YB-Master and YB-TServer? What does each do?
763. 🟡 `[YB]` What is DocDB? How does it use RocksDB?
764. 🟡 `[YB]` What is a tablet? What is a tablet leader and tablet follower?
765. 🟡 `[YB]` How does Raft consensus work for replication in YugabyteDB?
766. 🟡 `[YB]` What is the replication factor (RF=3, RF=5)? How many node failures can each tolerate?
767. 🟡 `[YB]` What is Hybrid Logical Clock (HLC) and why is it needed?
768. 🔴 `[YB]` What is a leader lease and how does it give consistent reads?
769. 🔴 `[YB]` How does YSQL reuse the PostgreSQL query layer code?

---

## 77. Sharding, Tablets & Colocation

770. 🟡 `[YB]` What is automatic sharding in YugabyteDB?
771. 🟡 `[YB]` What is hash sharding vs range sharding? How do you declare each (`PRIMARY KEY (id HASH)` vs `PRIMARY KEY (id ASC)`)?
772. 🟡 `[YB]` What is the default sharding strategy for the first primary key column in YSQL?
773. 🟡 `[YB]` When should you choose range sharding (range scans, ordering) vs hash sharding (even distribution)?
774. 🟡 `[YB]` What is tablet splitting (automatic and manual)? What is `SPLIT INTO n TABLETS`?
775. 🟡 `[YB]` What are hot spots and how do monotonically increasing keys (timestamps, sequences) cause them with range sharding?
776. 🟡 `[YB]` What is colocation? When should small tables be colocated?
777. 🟡 `[YB]` What are tablespaces in YugabyteDB used for (geo-placement of data)?
778. 🔴 `[YB]` How do you design primary keys for a high-insert transactions table in YugabyteDB? 💰
779. 🔴 `[YB]` What is table partitioning + tablespaces for geo-partitioning (data residency)? 💰

---

## 78. YSQL vs PostgreSQL — Compatibility & Differences

780. 🟡 `[YB]` Which PostgreSQL version is YSQL based on (PG 11 compatibility, newer releases on PG 15)?
781. 🟡 `[YB]` Which PostgreSQL features work the same in YSQL (stored procedures, functions, triggers, JSONB, refcursor, CTEs, window functions, extensions)?
782. 🟡 `[YB]` Which PostgreSQL features behave differently or have limitations in YugabyteDB (some extensions, `VACUUM` not needed, `CLUSTER`, `LISTEN/NOTIFY`, certain index types, sequences caching, foreign key performance)?
783. 🟡 `[YB]` Why is `VACUUM` not needed in YugabyteDB?
784. 🟡 `[YB]` How do sequences work in YugabyteDB and why should you increase sequence cache (`ysql_sequence_cache_minval`)?
785. 🟡 `[YB]` Why do `SERIAL` primary keys with range sharding create hot spots? What are alternatives (UUID, hash sharding)?
786. 🟡 `[YB]` Can you use pgAdmin, psql, DBeaver and Npgsql with YugabyteDB? What is `ysqlsh`?
787. 🟡 `[YB]` What are the default port numbers (YSQL 5433, YCQL 9042) and why does YSQL use 5433 instead of 5432?
788. 🔴 `[YB]` Why can a query that is fast in PostgreSQL be slow in YugabyteDB (network round trips, distributed joins, foreign key checks, missing index on distributed table)?
789. 🔴 `[YB]` What is the "N+1 RPC" problem in distributed SQL and how do batching (`yb_bnl_batch_size`, batched nested loop) help?

---

## 79. Transactions & Consistency in YugabyteDB

790. 🟡 `[YB]` Does YugabyteDB support ACID transactions across shards/nodes?
791. 🟡 `[YB]` What isolation levels does YugabyteDB support (Serializable, Snapshot/Repeatable Read, Read Committed)?
792. 🟡 `[YB]` What is the default isolation level in YSQL and how do you enable Read Committed (`yb_enable_read_committed_isolation`)?
793. 🟡 `[YB]` What are single-shard (fast-path) vs distributed transactions?
794. 🟡 `[YB]` What is the transaction status tablet?
795. 🟡 `[YB]` What are provisional records / intents?
796. 🟡 `[YB]` What are optimistic vs pessimistic concurrency control (wait-on-conflict) in YugabyteDB?
797. 🟡 `[YB]` What is a transaction conflict / restart read error (40001)? Why must applications implement retries?
798. 🔴 `[YB]` What is clock skew and how does YugabyteDB handle it (max clock skew, read restart)?
799. 🔴 `[YB]` What are follower reads and when would you use them (stale reads allowed, `yb_read_from_followers`)?
800. 🔴💰 How do you implement a fund transfer in YugabyteDB with retries on serialization failures?

---

## 80. Indexing & Performance in YugabyteDB

801. 🟡 `[YB]` How do secondary indexes work in YugabyteDB (stored as separate distributed tables)?
802. 🟡 `[YB]` What are covering indexes (`INCLUDE`) and why are they more important in YugabyteDB?
803. 🟡 `[YB]` What are partial and expression indexes in YugabyteDB?
804. 🟡 `[YB]` Does YugabyteDB support GIN indexes on JSONB? What are the limitations?
805. 🟡 `[YB]` What is `CREATE INDEX` backfill and `NONCONCURRENTLY`?
806. 🟡 `[YB]` How do you read `EXPLAIN (ANALYZE, DIST)` in YugabyteDB (storage read requests, RPCs)?
807. 🟡 `[YB]` What is `yb_stat_statements` / `pg_stat_statements` in YugabyteDB?
808. 🟡 `[YB]` What is the cost-based optimizer in YugabyteDB and why must you run `ANALYZE`?
809. 🔴 `[YB]` How do you optimize joins and foreign key checks in YugabyteDB?
810. 🔴 `[YB]` How do you bulk load data into YugabyteDB efficiently (`COPY` with `ROWS_PER_TRANSACTION`, `yb_disable_transactional_writes`, YugabyteDB Voyager, parallel loaders)?

---

## 81. Stored Procedures, Functions, refcursor & JSONB in YugabyteDB

811. 🟡 `[YB]` Are PL/pgSQL functions and procedures supported in YugabyteDB? Any differences from PostgreSQL?
812. 🟡 `[YB]` Does `refcursor` work in YugabyteDB the same way as in PostgreSQL? What do you need to watch for (transactions, connection managers)?
813. 🟡 `[YB]` Are triggers supported in YugabyteDB? What is the performance impact in a distributed system?
814. 🟡 `[YB]` How do JSONB functions and operators behave in YugabyteDB?
815. 🟡 `[YB]` What should you watch for when a stored procedure performs many single-row statements in a loop in YugabyteDB (each is a network round trip)?
816. 🔴 `[YB]` How do you rewrite row-by-row PL/pgSQL logic into set-based or batched operations for YugabyteDB?

---

## 82. Connection Management, Smart Drivers & Pooling in YugabyteDB

817. 🟡 `[YB]` What are YugabyteDB smart drivers (e.g., Npgsql-based YugabyteDB .NET driver)? What is cluster-aware and topology-aware load balancing?
818. 🟡 `[YB]` Can you use the standard Npgsql driver with YugabyteDB? What do you lose?
819. 🟡 `[YB]` What is the YSQL Connection Manager (built-in pooling)?
820. 🟡 `[YB]` Can you use PgBouncer with YugabyteDB?
821. 🟡 `[YB]` Why is connection count per node important in YugabyteDB?
822. 🔴 `[YB]` How do you configure connection pooling for microservices connecting to a 3-node YugabyteDB cluster?

---

## 83. Replication, Multi-Region, Backup & Operations in YugabyteDB

823. 🟡 `[YB]` How does synchronous replication within a cluster work?
824. 🟡 `[YB]` What is xCluster replication (asynchronous between clusters)? What are its consistency trade-offs?
825. 🟡 `[YB]` What are read replicas in YugabyteDB?
826. 🟡 `[YB]` What deployment topologies exist (single-region multi-zone, multi-region synchronous, xCluster, geo-partitioned)? 💰
827. 🟡 `[YB]` What is preferred leader region and why does it matter for latency?
828. 🟡 `[YB]` How do you back up and restore YugabyteDB (distributed snapshots, `ysql_dump`, PITR)?
829. 🟡 `[YB]` How do you add or remove nodes (rebalancing tablets)?
830. 🟡 `[YB]` What is CDC in YugabyteDB (gRPC / logical replication connector) for Kafka/Debezium?
831. 🔴 `[YB]` What happens when a node fails? When a full zone fails? When a region fails?
832. 🔴 `[YB]` How do you perform a rolling upgrade without downtime?

---

## 84. Migrating from PostgreSQL to YugabyteDB

833. 🟡 `[YB]` What is YugabyteDB Voyager? What does it do (assess, export schema/data, import, verify)?
834. 🟡 `[YB]` What schema changes are commonly needed when migrating from PostgreSQL (primary key sharding choices, sequences, unsupported extensions)?
835. 🟡 `[YB]` How do you migrate from Oracle or MySQL to YugabyteDB?
836. 🟡 `[YB]` How do you test application compatibility after migration (stored procedures, refcursors, JSONB queries)?
837. 🔴 `[YB]` How do you migrate with minimal downtime (live migration, CDC, fall-back)?
838. 🔴 `[YB]` What application code changes are needed (retry logic for 40001, connection settings, smart driver)?

---

# Part G — Cross-Database Comparisons & .NET Integration

## 85. MSSQL vs MySQL vs PostgreSQL vs Oracle vs YugabyteDB

839. 🟡 `[All]` Compare the five databases on licensing, scalability, features, procedural language and typical use cases.
840. 🟡 `[All]` How do procedural languages compare (T-SQL, PL/SQL, PL/pgSQL, MySQL stored program language)?
841. 🟡 `[All]` How do you return result sets from procedures in each database (result set, `SYS_REFCURSOR`, `refcursor`/`RETURNS TABLE`, result set)?
842. 🟡 `[All]` How do you pass a list of rows into a procedure in each database (TVP, collections/object types/array binding, arrays/JSON/composite types, JSON/temp table)?
843. 🟡 `[All]` How do you implement auto-increment in each database?
844. 🟡 `[All]` How do you implement upsert in each database?
845. 🟡 `[All]` How do you limit/paginate in each database?
846. 🟡 `[All]` How does exception handling syntax differ across the five databases?
847. 🟡 `[All]` What are the string concatenation operators/functions in each (`+`, `CONCAT`, `||`)?
848. 🟡 `[All]` How do default isolation levels and MVCC implementations differ?
849. 🟡 `[All]` How does each database handle empty strings vs NULL?
850. 🔴 `[All]` What are common pitfalls when migrating from Oracle to PostgreSQL (empty string = NULL, `NUMBER`, `DUAL`, `ROWNUM`, packages, `SYS_REFCURSOR`, `CONNECT BY`, autonomous transactions, `DATE` with time)?
851. 🔴 `[All]` What are common pitfalls when migrating from SQL Server to PostgreSQL (case sensitivity, `TOP`, `IDENTITY`, `ISNULL`, `#temp`, T-SQL procedures returning result sets)?
852. 🔴 `[All]` What are common pitfalls when migrating from MySQL to PostgreSQL (backticks, `AUTO_INCREMENT`, zero dates, `GROUP BY` leniency, `ON DUPLICATE KEY`)?
853. 🔴 `[All]` How do you write an application that supports multiple databases (abstractions, Dapper/EF Core providers, avoiding vendor-specific SQL)?

---

## 86. Calling Procedures, Functions, refcursors & Bulk Loads from .NET

854. 🟡 `[MSSQL]` How do you call a SQL Server procedure with input/output parameters and read multiple result sets in C#?
855. 🟡 `[MSSQL]` How do you pass a TVP from C# (`SqlParameter` with `SqlDbType.Structured` and `TypeName = "dbo.MyTableType"`)?
856. 🟡 `[MySQL]` How do you call a MySQL procedure from C# (`MySqlConnector`, `CommandType.StoredProcedure`)?
857. 🟡 `[MySQL]` How do you bulk insert into MySQL from C# (`MySqlBulkCopy`, `MySqlBulkLoader`, multi-row insert)?
858. 🟡 `[PG]` How do you call a PostgreSQL function vs a procedure from C# with Npgsql (`SELECT * FROM func()` vs `CALL proc()`)?
859. 🟡 `[PG]` How do you read a refcursor returned by a PostgreSQL function/procedure in C# (transaction + `FETCH ALL FROM "cursor_name"`)?
860. 🟡 `[PG]` How do you pass a JSONB parameter and read JSONB results in Npgsql (`NpgsqlDbType.Jsonb`)?
861. 🟡 `[PG]` How do you pass arrays and composite types to PostgreSQL functions from Npgsql?
862. 🟡 `[PG]` How do you use binary COPY from C# to load lakhs of rows?
863. 🟡 `[Oracle]` How do you call an Oracle procedure with `SYS_REFCURSOR` OUT parameter using ODP.NET?
864. 🟡 `[Oracle]` How do you use array binding in ODP.NET to insert 50,000 rows in one round trip?
865. 🟡 `[YB]` How do you connect to YugabyteDB from .NET (Npgsql or YugabyteDB smart driver, port 5433, load balance settings)?
866. 🟡 `[All]` How do you handle database-specific exceptions in .NET (`SqlException.Number`, `MySqlException.Number`, `PostgresException.SqlState`, `OracleException.Number`)?
867. 🔴 `[All]` How do you call stored procedures from Dapper and EF Core in each database?
868. 🔴 `[All]` How do you implement retry logic for transient errors and serialization failures across these databases?

---

# Part H — Practice

## 87. Financial-Domain Database Questions 💰

869. 🟡💰 `[All]` Which data type should be used for money in each database?
870. 🟡💰 `[All]` How do you design an accounts and transactions schema with double-entry bookkeeping?
871. 🔴💰 `[All]` How do you implement a fund transfer procedure that is atomic and safe under concurrency in each database?
872. 🔴💰 `[All]` How do you prevent negative balances under concurrent withdrawals (`SELECT ... FOR UPDATE`, conditional update, check constraints, row versioning)?
873. 🔴💰 `[All]` How do you implement idempotent transaction posting using a unique reference number?
874. 🔴💰 `[All]` How do you design an immutable ledger table (no UPDATE/DELETE, corrections as new entries)?
875. 🔴💰 `[All]` How do you implement an audit trail (triggers with JSONB, temporal tables, CDC, flashback)?
876. 🔴💰 `[All]` How do you generate a customer account statement with opening balance, transactions and running balance using SQL?
877. 🔴💰 `[All]` How do you implement end-of-day interest calculation for lakhs of accounts efficiently (set-based vs cursor)?
878. 🔴💰 `[All]` How do you archive old transactions (partitioning, partition switching/detach)?
879. 🔴💰 `[All]` How do you reconcile two large tables (bank statement vs internal ledger) and find mismatches?
880. 🔴💰 `[All]` How do you mask PAN, Aadhaar, card and account numbers in non-production databases?
881. 🔴💰 `[All]` How do you meet data retention and RBI/PCI requirements at the database level?
882. 🔴💰 `[YB]` Why might a bank choose YugabyteDB for a payments system (HA, multi-region, no single point of failure)?

---

## 88. SQL Query Writing Questions

> Write the query in ANSI SQL and mention the differences for SQL Server, MySQL, PostgreSQL and Oracle where relevant.

883. 🟢 Find the second highest salary from the `Employees` table.
884. 🟢 Find the Nth highest salary (using `DENSE_RANK`, `LIMIT/OFFSET`, `TOP`, correlated subquery).
885. 🟢 Find the highest salary in each department.
886. 🟢 Find employees who earn more than their manager.
887. 🟢 Find duplicate records in a table based on email.
888. 🟢 Delete duplicate records but keep one (using `ROW_NUMBER()`, `ctid` in PostgreSQL, `ROWID` in Oracle, self-join in MySQL).
889. 🟢 Count employees in each department, including departments with zero employees.
890. 🟢 Find departments with more than 5 employees.
891. 🟢 Find customers who have never placed an order (LEFT JOIN, `NOT EXISTS`, `NOT IN` — and the NULL trap).
892. 🟢 Find the top 3 highest-paid employees in each department.
893. 🟡 Find employees who joined in the last 6 months.
894. 🟡 Find the total sales per month for the current year.
895. 🟡 Find month-over-month growth percentage of revenue using `LAG()`.
896. 🟡 Calculate the running total of transactions per account ordered by date. 💰
897. 🟡 Calculate the running balance for an account statement (credits positive, debits negative). 💰
898. 🟡 Find the first and last transaction of each customer.
899. 🟡 Find customers who made transactions on three consecutive days.
900. 🟡 Find gaps in a sequence of invoice numbers.
901. 🟡 Find islands of consecutive login dates per user (gaps and islands).
902. 🟡 Find the employee hierarchy (all reports under a given manager) using a recursive CTE / `CONNECT BY`.
903. 🟡 Pivot monthly sales into columns (Jan, Feb, Mar...) per product.
904. 🟡 Unpivot columns into rows.
905. 🟡 Swap gender values 'M' and 'F' in a single UPDATE.
906. 🟡 Find the median salary.
907. 🟡 Find products that were never sold.
908. 🟡 Find the most frequently purchased product per customer.
909. 🟡 Find customers whose total purchases exceed the average customer purchase.
910. 🟡 Find accounts whose balance dropped below zero at any point in time. 💰
911. 🟡 Find transactions above ₹50,000 made by the same card within 10 minutes of each other. 💰
912. 🟡 Find dormant accounts (no transaction in the last 12 months). 💰
913. 🟡 Get the latest record per group (latest address per customer) — at least 3 approaches.
914. 🟡 Concatenate all product names per order into a comma-separated string (`STRING_AGG` / `GROUP_CONCAT` / `LISTAGG`).
915. 🟡 Find the cumulative percentage contribution of each product to total sales (Pareto / 80-20).
916. 🟡 Write a query to paginate orders 20 per page sorted by date, page 5 (offset and keyset).
917. 🟡 Find all pairs of employees in the same department (self-join without duplicates).
918. 🟡 Find the day with the highest number of transactions for each branch.
919. 🔴 Write an upsert that inserts new customers and updates existing ones from a staging table in all four databases.
920. 🔴 Write a query to find the top 5 customers by transaction value for each month in the last year.
921. 🔴 Write a query that returns each customer with their orders as a nested JSON array (PostgreSQL `json_agg`, SQL Server `FOR JSON`, MySQL `JSON_ARRAYAGG`, Oracle `JSON_ARRAYAGG`).
922. 🔴 Query a JSONB column to find orders where `items` contains a product with `sku = 'ABC'` and `qty > 2`.
923. 🔴 Calculate the age of each loan in days, months and years. 💰
924. 🔴 Find overlapping date ranges (e.g., overlapping bookings or leave requests).
925. 🔴 Write a query to calculate EMI schedule rows using a recursive CTE. 💰
926. 🔴 Detect circular references in a parent-child table.

---

## 89. Stored Procedure / Function / Cursor Writing Tasks

927. 🟢 `[MSSQL]` Write a stored procedure to insert a customer and return the new ID using an OUTPUT parameter.
928. 🟢 `[MySQL]` Write a stored procedure with IN and OUT parameters that returns the total orders for a customer.
929. 🟢 `[PG]` Write a PL/pgSQL function that returns a table of employees for a given department (`RETURNS TABLE`).
930. 🟢 `[Oracle]` Write a PL/SQL procedure that returns employees of a department via `OUT SYS_REFCURSOR`.
931. 🟡 `[PG]` Write a PostgreSQL function that returns a `refcursor` and show how to fetch it in pgAdmin.
932. 🟡 `[PG]` Write a PostgreSQL procedure with two `INOUT refcursor` parameters returning customers and orders.
933. 🟡 `[Oracle]` Write a package with a procedure returning two `SYS_REFCURSOR`s (header and details).
934. 🟡 `[PG]` Write a function that accepts a JSONB array of orders and inserts them into a table, returning the count.
935. 🟡 `[PG]` Write a function that returns customer details with their last 5 transactions as a single JSONB object.
936. 🟡 `[MSSQL]` Create a user-defined table type and a procedure that inserts 50,000 rows from it with duplicate checks.
937. 🟡 `[MSSQL]` Write a procedure using TVP that upserts products and returns which rows were inserted vs updated.
938. 🟡 `[MySQL]` Write a `LOAD DATA LOCAL INFILE` statement to load a CSV exported from Excel with date conversion and NULL handling.
939. 🟡 `[MySQL]` Write a procedure that moves validated rows from a staging table to the main table and logs invalid rows.
940. 🟡 `[All]` Write a cursor in each database that loops through accounts and applies monthly interest — then rewrite it as a single set-based UPDATE. 💰
941. 🟡 `[MSSQL]` Write a procedure with `TRY...CATCH`, transaction and `THROW` that transfers funds between accounts. 💰
942. 🟡 `[Oracle]` Write a procedure with user-defined exceptions and `RAISE_APPLICATION_ERROR` for insufficient balance. 💰
943. 🟡 `[PG]` Write a procedure with `EXCEPTION` handling that rolls back and raises a custom error with `ERRCODE`.
944. 🟡 `[MySQL]` Write a procedure with `DECLARE EXIT HANDLER FOR SQLEXCEPTION` that rolls back and re-signals.
945. 🟡 `[All]` Write an audit trigger in each database that logs old and new values on UPDATE.
946. 🟡 `[PG]` Write a generic audit trigger function that stores `to_jsonb(OLD)` and `to_jsonb(NEW)`.
947. 🟡 `[Oracle]` Write a compound trigger to avoid the mutating table error.
948. 🟡 `[Oracle]` Write a `BULK COLLECT ... LIMIT` + `FORALL` procedure to copy 10 lakh rows with `SAVE EXCEPTIONS`.
949. 🔴 `[All]` Write a job-queue "dequeue" procedure using `FOR UPDATE SKIP LOCKED` (and `READPAST` in SQL Server).
950. 🔴 `[YB]` Write a fund transfer function for YugabyteDB and describe the retry logic required in the application.
951. 🔴 `[PG]` Write a dynamic search function with optional filters using `format()` and `EXECUTE ... USING` safely, returning a refcursor.

---

## 90. Tricky Questions

952. 🟡 `[All]` Why does `SELECT * FROM t WHERE col = NULL` return no rows?
953. 🟡 `[All]` Why does `NOT IN (subquery)` return no rows when the subquery has a NULL?
954. 🟡 `[All]` Is `COUNT(*)` faster than `COUNT(1)`?
955. 🟡 `[All]` Does `ORDER BY` in a view or subquery guarantee order of the final result?
956. 🟡 `[All]` Without `ORDER BY`, is the order of rows guaranteed?
957. 🟡 `[All]` Can a table have a primary key with NULL values?
958. 🟡 `[All]` Can you create a unique index on a column that has multiple NULLs?
959. 🟡 `[All]` Why does an index on `created_at` not help `WHERE YEAR(created_at) = 2025`?
960. 🟡 `[All]` Why does `WHERE name LIKE '%kumar'` not use an index?
961. 🟡 `[All]` Why does adding an index sometimes make a query slower?
962. 🟡 `[All]` Why does the same query run fast in SSMS/pgAdmin but slow from the application?
963. 🟡 `[All]` Why does `TRUNCATE` fail on a table referenced by a foreign key?
964. 🟡 `[All]` Why is there a gap in my identity/sequence values?
965. 🟡 `[All]` Can `DELETE` without `WHERE` be rolled back? Can `TRUNCATE`?
966. 🟡 `[All]` What is the result of `NULL = NULL`, `NULL <> NULL`, `NULL + 1`, `'a' || NULL` in each database?
967. 🟡 `[Oracle]` Why does `WHERE ROWNUM = 2` return no rows?
968. 🟡 `[Oracle]` Why is `''` equal to NULL in Oracle but not in PostgreSQL/SQL Server/MySQL?
969. 🟡 `[MSSQL]` Why can `NOLOCK` return the same row twice or skip rows?
970. 🟡 `[MSSQL]` Why does `@@IDENTITY` return the wrong value when a trigger exists?
971. 🟡 `[MSSQL]` Why does an inner `COMMIT TRANSACTION` not actually commit when `@@TRANCOUNT > 1`?
972. 🟡 `[MSSQL]` Why can a TVP-based insert be slow for very large inputs (cardinality estimate of 1 row)?
973. 🟡 `[MySQL]` Why does MySQL allow selecting non-grouped columns in some versions/configs?
974. 🟡 `[MySQL]` Why does `LOAD DATA LOCAL INFILE` fail with "Loading local data is disabled"?
975. 🟡 `[MySQL]` Why do leading zeros disappear from account numbers when importing from Excel? 💰
976. 🟡 `[MySQL]` Why does an `UPDATE ... WHERE non_indexed_col = x` lock many rows in InnoDB?
977. 🟡 `[PG]` Why does pgAdmin show `<unnamed portal 1>` instead of data when calling a refcursor function?
978. 🟡 `[PG]` Why do I get "cursor does not exist" when fetching a refcursor?
979. 🟡 `[PG]` Why does a refcursor function work in pgAdmin but return nothing in my .NET app?
980. 🟡 `[PG]` Why does my table keep growing in size even though I delete rows?
981. 🟡 `[PG]` Why can't I `COMMIT` inside a function?
982. 🟡 `[PG]` Why does `CREATE INDEX` lock writes, and why use `CONCURRENTLY`?
983. 🟡 `[PG]` Why is `jsonb` slower to insert but faster to query than `json`?
984. 🟡 `[PG]` Why doesn't my GIN index get used for `data->>'city' = 'Pune'`?
985. 🟡 `[PG]` Why does `SELECT "Name" FROM Customer` fail but `SELECT name FROM customer` works?
986. 🟡 `[Oracle]` Why do I get ORA-01422 "exact fetch returns more than requested number of rows"?
987. 🟡 `[Oracle]` Why do I get ORA-01403 "no data found" inside a function called from SQL?
988. 🟡 `[Oracle]` Why do I get ORA-04091 mutating table error in a trigger?
989. 🟡 `[Oracle]` Why do I get ORA-01000 maximum open cursors exceeded from my .NET app?
990. 🟡 `[Oracle]` Why does `WHEN OTHERS THEN NULL` hide production bugs?
991. 🟡 `[YB]` Why does an auto-increment primary key create a hot spot in YugabyteDB?
992. 🟡 `[YB]` Why do I get "Restart read required" / serialization errors in YugabyteDB that I never saw in PostgreSQL?
993. 🟡 `[YB]` Why is a stored procedure that loops over 10,000 rows much slower in YugabyteDB than in PostgreSQL?
994. 🔴 `[All]` Is a stored procedure always faster than inline SQL?
995. 🔴 `[All]` Is a cursor always slower than a set-based query?
996. 🔴 `[All]` Can a deadlock happen with only one table?
997. 🔴 `[All]` Can two transactions both read a balance of ₹1,000 and both withdraw ₹800 successfully? Under which isolation level? 💰
998. 🔴 `[All]` Can `SELECT` statements cause blocking?
999. 🔴 `[All]` What happens if a transaction is left open by an application for hours?

---

## 91. Predict the Output (SQL Snippets)

> What is the result of each snippet? If it errors, say why. Mention database-specific differences.

**1000. 🟢 NULL comparison**
```sql
SELECT COUNT(*) FROM (VALUES (1),(NULL),(3)) AS t(x) WHERE x <> 1;
```

**1001. 🟡 NOT IN with NULL**
```sql
SELECT * FROM customers WHERE id NOT IN (SELECT customer_id FROM orders);
-- orders.customer_id contains one NULL value
```

**1002. 🟢 COUNT variants**
```sql
-- t(x): 1, NULL, 2, NULL
SELECT COUNT(*), COUNT(x), COUNT(DISTINCT x), SUM(x), AVG(x) FROM t;
```

**1003. 🟡 LEFT JOIN with WHERE**
```sql
SELECT c.id, o.id
FROM customers c LEFT JOIN orders o ON o.customer_id = c.id
WHERE o.status = 'PAID';
```
Is this still a left join? How do you keep customers without orders?

**1004. 🟡 RANK vs DENSE_RANK vs ROW_NUMBER**
```sql
-- salaries: 100, 200, 200, 300
SELECT salary,
       ROW_NUMBER() OVER (ORDER BY salary DESC) rn,
       RANK()       OVER (ORDER BY salary DESC) rk,
       DENSE_RANK() OVER (ORDER BY salary DESC) drk
FROM emp;
```

**1005. 🟡 Integer division**
```sql
SELECT 5/2, 5/2.0, CAST(5 AS DECIMAL)/2;
```
What is returned in SQL Server, PostgreSQL, MySQL and Oracle?

**1006. 🟡 String concatenation with NULL**
```sql
SELECT 'Hello ' || NULL;     -- PostgreSQL / Oracle
SELECT 'Hello ' + NULL;      -- SQL Server
SELECT CONCAT('Hello ', NULL); -- MySQL / SQL Server / PostgreSQL
```

**1007. 🟡 Oracle empty string**
```sql
SELECT CASE WHEN '' IS NULL THEN 'NULL' ELSE 'NOT NULL' END FROM dual;
```
What about the same check in PostgreSQL and SQL Server?

**1008. 🟡 ROWNUM**
```sql
SELECT * FROM employees WHERE ROWNUM > 1;
SELECT * FROM (SELECT * FROM employees ORDER BY salary DESC) WHERE ROWNUM <= 3;
```

**1009. 🟡 UNION vs UNION ALL**
```sql
SELECT 1 UNION SELECT 1 UNION ALL SELECT 1;
```

**1010. 🟡 Transaction rollback with TRUNCATE**
```sql
BEGIN;
TRUNCATE TABLE logs;
ROLLBACK;
SELECT COUNT(*) FROM logs;
```
What happens in PostgreSQL, SQL Server, MySQL and Oracle?

**1011. 🟡 Nested transactions in SQL Server**
```sql
BEGIN TRAN;
  INSERT INTO t VALUES (1);
  BEGIN TRAN;
    INSERT INTO t VALUES (2);
  COMMIT;
ROLLBACK;
SELECT COUNT(*) FROM t;
```

**1012. 🔴 TRY/CATCH without XACT_ABORT**
```sql
BEGIN TRY
  BEGIN TRAN;
    UPDATE accounts SET balance = balance - 100 WHERE id = 1;
    UPDATE accounts SET balance = balance + 100 WHERE id = 999; -- id 999 doesn't exist
  COMMIT;
END TRY
BEGIN CATCH
  ROLLBACK;
END CATCH;
```
Does the CATCH block run? Is money lost? 💰

**1013. 🔴 PostgreSQL refcursor in autocommit**
```sql
CREATE FUNCTION get_emps() RETURNS refcursor AS $$
DECLARE c refcursor := 'emp_cur';
BEGIN OPEN c FOR SELECT * FROM emp; RETURN c; END; $$ LANGUAGE plpgsql;

SELECT get_emps();
FETCH ALL IN emp_cur;   -- run as a separate statement with autocommit ON
```

**1014. 🔴 PL/pgSQL exception rollback**
```sql
DO $$
BEGIN
  INSERT INTO t VALUES (1);
  BEGIN
    INSERT INTO t VALUES (2);
    PERFORM 1/0;
  EXCEPTION WHEN division_by_zero THEN
    RAISE NOTICE 'caught';
  END;
  INSERT INTO t VALUES (3);
END $$;
SELECT * FROM t;
```

**1015. 🔴 Oracle SELECT INTO**
```sql
DECLARE v_name VARCHAR2(50);
BEGIN
  SELECT name INTO v_name FROM employees WHERE dept_id = 10;  -- 0 rows in some cases, 5 rows in others
END;
```
What exceptions are raised in each case?

**1016. 🔴 MySQL cursor without handler**
```sql
DECLARE cur CURSOR FOR SELECT id FROM accounts;
OPEN cur;
read_loop: LOOP
  FETCH cur INTO v_id;
  -- no NOT FOUND handler declared
END LOOP;
```

**1017. 🟡 JSONB operators**
```sql
SELECT '{"a":{"b":5}}'::jsonb -> 'a' -> 'b',
       '{"a":{"b":5}}'::jsonb -> 'a' ->> 'b',
       '{"a":{"b":5}}'::jsonb #>> '{a,b}',
       '{"tags":["x","y"]}'::jsonb @> '{"tags":["x"]}';
```
What type and value does each return?

**1018. 🟡 jsonb vs json**
```sql
SELECT '{"a":1,"a":2, "b":3}'::json, '{"a":1,"a":2, "b":3}'::jsonb;
```

**1019. 🟡 Upsert**
```sql
INSERT INTO accounts(id, balance) VALUES (1, 500)
ON CONFLICT (id) DO UPDATE SET balance = accounts.balance + EXCLUDED.balance;
```
Account 1 already has balance 1000. What is the new balance? 💰

**1020. 🔴 Lost update**
```sql
-- Session A and B both at READ COMMITTED:
-- A: SELECT balance FROM accounts WHERE id=1;   -- 1000
-- B: SELECT balance FROM accounts WHERE id=1;   -- 1000
-- A: UPDATE accounts SET balance = 1000 - 800 WHERE id=1; COMMIT;
-- B: UPDATE accounts SET balance = 1000 - 800 WHERE id=1; COMMIT;
```
What is the final balance? How do you fix it? 💰

**1021. 🔴 Deadlock**
```sql
-- Session A: UPDATE accounts SET ... WHERE id = 1;  then  UPDATE accounts SET ... WHERE id = 2;
-- Session B: UPDATE accounts SET ... WHERE id = 2;  then  UPDATE accounts SET ... WHERE id = 1;
```
What happens? How does each database resolve it?

**1022. 🟡 TVP READONLY**
```sql
CREATE PROCEDURE dbo.ImportOrders @Orders dbo.OrderType READONLY AS
BEGIN
  UPDATE @Orders SET Amount = Amount * 1.18;
END
```

**1023. 🟡 LOAD DATA with dates**
```sql
LOAD DATA LOCAL INFILE 'txn.csv' INTO TABLE txn
FIELDS TERMINATED BY ',' IGNORE 1 LINES
(txn_id, txn_date, amount);
-- CSV dates are in dd/mm/yyyy format, strict mode ON
```

**1024. 🟡 Window frame**
```sql
SELECT amount,
       LAST_VALUE(amount) OVER (ORDER BY txn_date) AS last_val
FROM txn;
```
Why does `last_val` equal the current row's amount? How do you fix it?

**1025. 🔴 YugabyteDB hash vs range**
```sql
CREATE TABLE txn (id BIGSERIAL, created_at TIMESTAMPTZ, PRIMARY KEY (created_at ASC, id));
-- 50,000 inserts per second with current timestamps
```
What problem will occur? How do you redesign the key?

---

## 92. Scenario-Based Questions — Design & Development

1026. 🟡 `[All]` Design tables for customers, accounts, transactions and beneficiaries for a banking app. Which constraints and indexes would you add? 💰
1027. 🟡 `[All]` You must return a customer profile, their accounts and last 10 transactions from one database call. How do you do it in SQL Server, Oracle and PostgreSQL (multiple result sets / refcursors / JSON)?
1028. 🟡 `[PG]` Your API needs flexible attributes per product category. Would you use JSONB or EAV tables? Why?
1029. 🟡 `[PG]` You need to store KYC documents' metadata which varies by document type. Design using JSONB with validation and indexes. 💰
1030. 🟡 `[MSSQL]` The UI sends 30,000 rows of salary data to save. Design the procedure using a table type, including validation and error reporting.
1031. 🟡 `[MySQL]` Business users upload an Excel file with 3 lakh beneficiary records every week. Design the end-to-end import process. 💰
1032. 🟡 `[Oracle]` A legacy Oracle package returns 4 `SYS_REFCURSOR`s to a .NET application. How do you consume them and what should you watch for?
1033. 🟡 `[PG]` A procedure in PostgreSQL must return two result sets to .NET. refcursor or JSON? Explain the trade-offs.
1034. 🟡 `[All]` You need an audit log of every change to the `accounts` table. Trigger, CDC, temporal table or application-level logging? 💰
1035. 🟡 `[All]` How do you implement soft delete and still keep unique constraints working?
1036. 🟡 `[All]` How do you generate unique, human-readable transaction reference numbers safely under concurrency? 💰
1037. 🟡 `[All]` How do you implement a maker-checker workflow for payments at the database level? 💰
1038. 🔴 `[All]` You need to support the same application on SQL Server and PostgreSQL. How do you structure stored procedures and data access?
1039. 🔴 `[YB]` You are designing a new payments table in YugabyteDB with 10,000 inserts per second. Design the primary key, indexes and partitioning. 💰
1040. 🔴 `[YB]` Your application uses refcursors and JSONB heavily in PostgreSQL. What do you validate before moving to YugabyteDB?
1041. 🔴 `[All]` How do you design a multi-tenant database (shared schema with tenant_id + RLS, schema per tenant, database per tenant)?

---

## 93. Scenario-Based Questions — Performance & Production Issues

1042. 🟡 `[All]` A report query that used to take 2 seconds now takes 2 minutes. How do you investigate?
1043. 🟡 `[All]` The application is getting timeouts during month-end processing. What do you check? 💰
1044. 🟡 `[All]` The database CPU is at 100%. How do you find the cause in each database?
1045. 🟡 `[All]` Users report the application "hangs" — you suspect blocking. How do you find the blocking session and what do you do?
1046. 🟡 `[All]` Deadlocks are occurring frequently in the payment module. How do you capture, analyze and fix them? 💰
1047. 🟡 `[MSSQL]` A stored procedure is fast for some parameters and very slow for others. What is happening and how do you fix it?
1048. 🟡 `[MSSQL]` `tempdb` is full and growing. What could cause it?
1049. 🟡 `[MSSQL]` The transaction log file has grown to 500 GB. Why, and how do you fix it safely?
1050. 🟡 `[MySQL]` MySQL shows "Too many connections". What do you do immediately and long term?
1051. 🟡 `[MySQL]` A query with `LIMIT 500000, 50` is very slow. How do you fix it?
1052. 🟡 `[PG]` A PostgreSQL table's size keeps increasing and queries get slower even though row count is stable. What is happening?
1053. 🟡 `[PG]` You see many `idle in transaction` sessions in `pg_stat_activity`. Why is this bad and how do you fix it?
1054. 🟡 `[PG]` PostgreSQL warns about transaction ID wraparound. What do you do?
1055. 🟡 `[PG]` A JSONB search query on 50 lakh rows is slow. How do you index and rewrite it?
1056. 🟡 `[PG]` Your .NET app opens 500 connections to PostgreSQL and the server runs out of memory. How do you fix it?
1057. 🟡 `[Oracle]` The app gets ORA-01000 maximum open cursors exceeded. How do you find the leak?
1058. 🟡 `[Oracle]` A batch job gets ORA-01555 snapshot too old. What causes it and how do you fix it?
1059. 🟡 `[Oracle]` A PL/SQL procedure processing 10 lakh rows with a cursor loop takes 3 hours. How do you speed it up?
1060. 🟡 `[YB]` After moving from PostgreSQL to YugabyteDB, some APIs became 5x slower. How do you investigate?
1061. 🟡 `[YB]` One node in the YugabyteDB cluster shows much higher CPU than others. What could be the cause (hot tablet, leader imbalance)?
1062. 🔴 `[All]` A new index was added and suddenly inserts became slow. Why?
1063. 🔴 `[All]` The same query plan suddenly changed after statistics were updated and performance degraded. How do you stabilize it?
1064. 🔴 `[All]` A production database restore is needed to a point 10 minutes before a wrong UPDATE. Walk through the process in each database. 💰

---

## 94. Scenario-Based Questions — Bulk Data & Migration

1065. 🟡 `[MSSQL]` You need to insert 50,000 rows from a .NET API in under 2 seconds. Compare TVP, `SqlBulkCopy` and batched inserts and pick one.
1066. 🟡 `[MSSQL]` A TVP-based import of 1 lakh rows times out. How do you redesign it?
1067. 🟡 `[MySQL]` An Excel upload of 5 lakh rows using row-by-row inserts takes 40 minutes. How do you bring it under 1 minute?
1068. 🟡 `[MySQL]` After importing from Excel, dates and amounts are wrong. How do you identify and fix the root causes?
1069. 🟡 `[MySQL]` The same Excel file was uploaded twice and created duplicate records. How do you prevent and clean this?
1070. 🟡 `[PG]` You need to load a 5 GB CSV into PostgreSQL daily. Design the process (COPY, staging, upsert, indexes, ANALYZE).
1071. 🟡 `[PG]` A bulk insert through a PL/pgSQL loop with `EXCEPTION` blocks is extremely slow. Why, and how do you fix it?
1072. 🟡 `[Oracle]` You need to load 1 crore records from CSV into Oracle. SQL*Loader, external tables, or BULK COLLECT/FORALL — which and why?
1073. 🟡 `[All]` During bulk load, some rows fail validation. How do you continue loading valid rows and report invalid ones?
1074. 🔴 `[All]` You must migrate a database from Oracle to PostgreSQL including packages and `SYS_REFCURSOR` procedures. What is your plan and tooling (Ora2Pg, AWS SCT)?
1075. 🔴 `[All]` You must migrate from SQL Server to PostgreSQL for licensing cost reasons. What are the main risks?
1076. 🔴 `[YB]` You must migrate a 2 TB PostgreSQL database to YugabyteDB with less than 30 minutes downtime. How do you plan it?
1077. 🔴 `[All]` How do you validate that migrated data matches source data (row counts, checksums, sample comparison)?
1078. 🔴 `[All]` How do you purge 5 crore old rows from a live production table without locking it for hours?

---

## 95. Rapid-Fire Round

1079. 🟢 `[All]` Which clause filters groups?
1080. 🟢 `[All]` Which join returns all rows from both tables?
1081. 🟢 `[All]` What does ACID stand for?
1082. 🟢 `[All]` Which is faster: `UNION` or `UNION ALL`?
1083. 🟢 `[All]` How many clustered indexes can a SQL Server table have?
1084. 🟢 `[MSSQL]` Which function returns the last identity value in the current scope?
1085. 🟢 `[MySQL]` Which function returns the last auto-increment value?
1086. 🟢 `[PG]` Which clause returns inserted values in PostgreSQL?
1087. 🟢 `[Oracle]` What is the dummy table in Oracle?
1088. 🟢 `[PG]` Which data type stores binary JSON in PostgreSQL?
1089. 🟢 `[Oracle]` What is the built-in weak REF CURSOR type?
1090. 🟢 `[MSSQL]` What keyword must a TVP parameter have?
1091. 🟢 `[MySQL]` Which statement loads a CSV file fastest in MySQL?
1092. 🟢 `[PG]` Which command loads a CSV fastest in PostgreSQL?
1093. 🟡 `[MSSQL]` `RAISERROR` or `THROW` — which re-throws the original error?
1094. 🟡 `[MySQL]` Which statement raises a custom error in MySQL?
1095. 🟡 `[PG]` Which statement raises a custom error in PL/pgSQL?
1096. 🟡 `[Oracle]` Which procedure raises a custom error in PL/SQL?
1097. 🟡 `[PG]` Which JSONB operator checks containment?
1098. 🟡 `[PG]` Which index type is best for JSONB containment queries?
1099. 🟡 `[PG]` Which index type is best for very large append-only time-series tables?
1100. 🟡 `[All]` What is the default isolation level in PostgreSQL? In MySQL InnoDB? In Oracle? In SQL Server?
1101. 🟡 `[Oracle]` What is the error number range for `RAISE_APPLICATION_ERROR`?
1102. 🟡 `[Oracle]` Which keyword fetches many rows into a collection at once?
1103. 🟡 `[Oracle]` Which keyword performs bulk DML from a collection?
1104. 🟡 `[PG]` Which pooler is most commonly used with PostgreSQL?
1105. 🟡 `[YB]` What is the default YSQL port?
1106. 🟡 `[YB]` What consensus protocol does YugabyteDB use?
1107. 🟡 `[YB]` What is a unit of data distribution in YugabyteDB called?
1108. 🟡 `[YB]` Which sharding type is the default for the first primary key column in YSQL?
1109. 🟡 `[YB]` What SQLSTATE indicates a serialization failure that should be retried?
1110. 🔴 `[PG]` What is the difference between `VACUUM` and `VACUUM FULL` in one line?
1111. 🔴 `[MSSQL]` What is the difference between `SNAPSHOT` and `RCSI` in one line?
1112. 🔴 `[Oracle]` What is the difference between strong and weak REF CURSOR in one line?
1113. 🔴 `[PG]` What is the difference between `json` and `jsonb` in one line?
1114. 🔴 `[YB]` What is the difference between hash and range sharding in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases (MSSQL, MySQL, PostgreSQL, Oracle, YugabyteDB).
