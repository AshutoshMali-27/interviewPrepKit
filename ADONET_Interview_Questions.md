# 🎯 ADO.NET Interview Questions — Part 4 (Questions Only)

> **Scope:** ADO.NET only — architecture, connections, connection pooling, commands, parameters, DataReader, DataSet/DataTable/DataAdapter, transactions, stored procedures, async ADO.NET, bulk operations, security, performance, plus tricky questions and predict-the-behavior code snippets.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks often still use ADO.NET heavily), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers modern .NET (`Microsoft.Data.SqlClient`) and legacy .NET Framework (`System.Data.SqlClient`).**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. ADO.NET Fundamentals & Architecture
2. Data Providers & Namespaces
3. Connections & Connection Strings
4. Connection Pooling
5. Command Object
6. Parameters & SQL Injection
7. DataReader
8. DataSet, DataTable, DataView & DataRelation
9. DataAdapter & CommandBuilder
10. Connected vs Disconnected Architecture
11. Stored Procedures & Functions
12. Transactions
13. Async ADO.NET
14. Bulk Operations & Table-Valued Parameters
15. Exception Handling & Resiliency
16. Data Types, NULL Handling & Conversions
17. Security
18. Performance & Optimization
19. Provider-Agnostic Code (DbProviderFactory)
20. Advanced Features (MARS, SqlDependency, XML, JSON)
21. ADO.NET vs Dapper vs EF Core
22. Design Patterns & Architecture with ADO.NET
23. Testing ADO.NET Code
24. Financial-Domain ADO.NET Questions 💰
25. Tricky ADO.NET Questions
26. Predict the Behavior (Code Snippets)
27. Coding & Hands-On Tasks
28. Scenario-Based & Debugging Questions
29. Rapid-Fire Round

---

## 1. ADO.NET Fundamentals & Architecture

1. 🟢 What is ADO.NET?
2. 🟢 What is the difference between ADO and ADO.NET?
3. 🟢 What are the main components of ADO.NET?
4. 🟢 Explain the architecture of ADO.NET (data providers and DataSet).
5. 🟢 What are the advantages of ADO.NET?
6. 🟢 What is the difference between connected and disconnected architecture?
7. 🟢 Which objects are part of the connected architecture?
8. 🟢 Which objects are part of the disconnected architecture?
9. 🟡 Is ADO.NET still used in modern .NET applications? Where and why?
10. 🟡 How do ORMs like EF Core and Dapper relate to ADO.NET internally?
11. 🟡 What is the role of the `System.Data` namespace?
12. 🟡 What are the base abstract classes in ADO.NET (`DbConnection`, `DbCommand`, `DbDataReader`, `DbParameter`, `DbTransaction`)?
13. 🟡 What are the interfaces `IDbConnection`, `IDbCommand`, `IDataReader`? How are they different from the abstract `Db*` classes?

---

## 2. Data Providers & Namespaces

14. 🟢 What is a .NET data provider?
15. 🟢 Name the commonly used data providers (SQL Server, Oracle, OLE DB, ODBC, MySQL, PostgreSQL, SQLite).
16. 🟢 What are the four core objects of a data provider (Connection, Command, DataReader, DataAdapter)?
17. 🟡 What is the difference between `System.Data.SqlClient` and `Microsoft.Data.SqlClient`?
18. 🟡 Why should new projects use `Microsoft.Data.SqlClient`?
19. 🟡 What breaking change did `Microsoft.Data.SqlClient` 4.0 introduce regarding `Encrypt=true` by default?
20. 🟡 What is the difference between the SqlClient, OLE DB and ODBC providers? When would you use OLE DB or ODBC?
21. 🟡 What are `Npgsql`, `MySqlConnector`, `Oracle.ManagedDataAccess` and `Microsoft.Data.Sqlite`?
22. 🟡 Why is `System.Data.OracleClient` deprecated?

---

## 3. Connections & Connection Strings

23. 🟢 What is a `SqlConnection`? What does it do?
24. 🟢 What is a connection string? What are its main parts?
25. 🟢 What is the difference between Windows Authentication and SQL Server Authentication in a connection string?
26. 🟢 What do `Data Source`, `Initial Catalog`, `Integrated Security`, `User ID`, `Password` mean?
27. 🟡 What do `Encrypt`, `TrustServerCertificate`, `Connect Timeout`, `Application Name`, `MultipleActiveResultSets` mean?
28. 🟢 What is the difference between `Open()` and `Close()`? Between `Close()` and `Dispose()`?
29. 🟢 Why should you open connections as late as possible and close them as early as possible?
30. 🟢 Why should you always wrap connections in a `using` block?
31. 🟡 What are the connection states (`ConnectionState`)? How do you check them?
32. 🟡 What happens if you call `Open()` on an already open connection?
33. 🟡 What is `SqlConnectionStringBuilder` and why use it?
34. 🟡 Where should connection strings be stored in .NET Framework vs .NET Core?
35. 🟡 How do you read a connection string from `appsettings.json` / `IConfiguration`?
36. 🟡 How do you secure connection strings (encrypting config sections, Key Vault, managed identity)?
37. 🟡 What is `Connect Timeout` vs `CommandTimeout`?
38. 🔴 What is `ConnectRetryCount` and `ConnectRetryInterval` (idle connection resiliency)?
39. 🔴 What is `Authentication=Active Directory Default` / Managed Identity in connection strings?
40. 🔴 What is `ApplicationIntent=ReadOnly` and `MultiSubnetFailover`?
41. 🟡 What is the `SqlConnection.InfoMessage` event? What is `StatisticsEnabled`?

---

## 4. Connection Pooling

42. 🟢 What is connection pooling? Why is it important?
43. 🟢 Is connection pooling enabled by default in ADO.NET?
44. 🟡 How does ADO.NET decide which pool a connection belongs to?
45. 🟡 Why do two connection strings that differ only by whitespace or key order create different pools?
46. 🟡 What happens when you call `Close()` or `Dispose()` on a pooled connection?
47. 🟡 What are `Min Pool Size`, `Max Pool Size`, `Pooling`, `Connection Lifetime` / `Load Balance Timeout`?
48. 🟡 What is the default `Max Pool Size`?
49. 🟡 What happens when the pool is exhausted?
50. 🟡 What does the error "Timeout expired. The timeout period elapsed prior to obtaining a connection from the pool" mean? What causes it?
51. 🔴 What is connection leakage? How do you detect it?
52. 🔴 What is `SqlConnection.ClearPool()` and `ClearAllPools()`? When would you use them?
53. 🔴 How does Windows Authentication / integrated security affect pooling (pool per identity)?
54. 🔴 Why does impersonation or per-user connection strings hurt pooling?
55. 🔴 What is pool fragmentation? How do multiple databases cause it?
56. 🔴 What happens to a pooled connection if the database server restarts? How does ADO.NET detect broken connections?
57. 🔴 How does connection state (e.g., `SET` options, temp tables, transaction isolation level) leak between pooled connections? What is `sp_reset_connection`?
58. 🟡 How do you monitor connection pool usage (performance counters, event counters)?

---

## 5. Command Object

59. 🟢 What is a `SqlCommand`?
60. 🟢 What are the `CommandType` values (`Text`, `StoredProcedure`, `TableDirect`)?
61. 🟢 What is the difference between `ExecuteNonQuery()`, `ExecuteScalar()` and `ExecuteReader()`?
62. 🟢 What does `ExecuteNonQuery()` return? When does it return -1?
63. 🟢 What does `ExecuteScalar()` return if the query returns multiple rows or columns? No rows?
64. 🟡 What is `ExecuteXmlReader()`?
65. 🟡 What is `CommandTimeout`? What is the default value? What does 0 mean?
66. 🟡 How do you cancel a running command (`Cancel()`, `CancellationToken`)?
67. 🟡 What is `Prepare()`? Does it help with SQL Server?
68. 🟡 How do you execute multiple SQL statements in a single command?
69. 🟡 How do you get the newly inserted identity value (`SCOPE_IDENTITY()`, `OUTPUT INSERTED.Id`)?
70. 🟡 What is the difference between `SCOPE_IDENTITY()`, `@@IDENTITY` and `IDENT_CURRENT()`?
71. 🟡 How does `SET NOCOUNT ON` affect `ExecuteNonQuery()` return values?
72. 🟡 Can a `SqlCommand` be reused with different parameter values?
73. 🔴 Is `SqlCommand` thread-safe?
74. 🔴 What is `SqlCommand.StatementCompleted` event?

---

## 6. Parameters & SQL Injection

75. 🟢 What is SQL injection? Give an example.
76. 🟢 How do parameterized queries prevent SQL injection?
77. 🟢 How do you add parameters to a `SqlCommand`?
78. 🟡 What is the difference between `Parameters.Add()` and `Parameters.AddWithValue()`?
79. 🔴 Why can `AddWithValue()` cause performance problems (type inference, `nvarchar` vs `varchar`, implicit conversions, plan cache bloat)?
80. 🟡 Why should you specify `SqlDbType` and `Size` for parameters?
81. 🟡 What are parameter directions (`Input`, `Output`, `InputOutput`, `ReturnValue`)?
82. 🟡 How do you read an output parameter? When is its value available when using a DataReader?
83. 🟡 How do you pass `NULL` as a parameter value? Why is `null` different from `DBNull.Value`?
84. 🟡 How do you pass a list of values to an `IN` clause safely?
85. 🟡 How do you specify precision and scale for a `decimal` parameter? 💰
86. 🟡 Can you parameterize table names or column names? How do you safely build dynamic SQL in that case?
87. 🔴 Is a stored procedure always safe from SQL injection? When is it not (dynamic SQL with `EXEC`)?
88. 🔴 What is `sp_executesql` and how does ADO.NET use it for parameterized text commands?
89. 🔴 What is parameter sniffing? How can it affect ADO.NET queries?

---

## 7. DataReader

90. 🟢 What is a `SqlDataReader`?
91. 🟢 What are the characteristics of a DataReader (forward-only, read-only, connected)?
92. 🟢 How do you read data using `Read()`?
93. 🟢 What is the difference between `reader["Name"]`, `reader[0]` and `reader.GetString(0)`?
94. 🟡 What is `GetOrdinal()` and why should you call it outside the loop?
95. 🟡 How do you check for NULL values (`IsDBNull`, `DBNull.Value`)?
96. 🟡 What is `GetFieldValue<T>()` and `GetFieldValueAsync<T>()`?
97. 🟡 How do you read multiple result sets (`NextResult()`)?
98. 🟡 What is `HasRows`? What is `FieldCount`? What is `RecordsAffected`?
99. 🟡 What is `CommandBehavior`? Explain `CloseConnection`, `SingleRow`, `SingleResult`, `SequentialAccess`, `KeyInfo`, `SchemaOnly`.
100. 🟡 Why must you close a DataReader before reusing the connection?
101. 🟡 Can you have two open DataReaders on the same connection? What is MARS?
102. 🔴 What is `CommandBehavior.SequentialAccess` and when should you use it (large BLOB/text columns)?
103. 🔴 How do you stream large binary or text data (`GetStream()`, `GetTextReader()`)?
104. 🟡 What is `GetSchemaTable()`?
105. 🟡 How do you map a DataReader to a list of objects manually?
106. 🔴 What happens to output parameters if you don't fully read and close the DataReader?
107. 🔴 Is reading by column name slower than reading by ordinal? By how much and why?

---

## 8. DataSet, DataTable, DataView & DataRelation

108. 🟢 What is a `DataSet`?
109. 🟢 What is a `DataTable`?
110. 🟢 What is the difference between `DataSet` and `DataTable`?
111. 🟢 What is the difference between `DataSet` and `DataReader`?
112. 🟢 What are `DataRow` and `DataColumn`?
113. 🟡 What is a `DataRelation`? How do you navigate parent/child rows?
114. 🟡 What are constraints in a DataTable (`UniqueConstraint`, `ForeignKeyConstraint`, `PrimaryKey`)?
115. 🟡 What is `DataRowState` (`Added`, `Modified`, `Deleted`, `Unchanged`, `Detached`)?
116. 🟡 What is `DataRowVersion` (`Original`, `Current`, `Proposed`, `Default`)?
117. 🟡 What do `AcceptChanges()` and `RejectChanges()` do?
118. 🟡 What does `GetChanges()` return?
119. 🟡 What is the difference between `Delete()` and `Remove()` on a DataRow?
120. 🟡 What is `Copy()` vs `Clone()` on a DataSet/DataTable?
121. 🟡 What is `Merge()` in a DataSet?
122. 🟡 What is a `DataView`? How do you filter and sort data with it?
123. 🟡 What is `DataTable.Select()` vs `DataView.RowFilter`?
124. 🟡 What is a computed / expression column in a DataTable?
125. 🟡 What is a typed DataSet vs an untyped DataSet?
126. 🟡 How do you convert a DataTable to a `List<T>` (manually, LINQ to DataSet, `Field<T>()`)?
127. 🟡 What is LINQ to DataSet (`AsEnumerable()`, `Field<T>()`, `CopyToDataTable()`)?
128. 🟡 How do you read and write XML with a DataSet (`ReadXml`, `WriteXml`, `WriteXmlSchema`)?
129. 🟡 How do you load a DataTable from a DataReader (`DataTable.Load()`)?
130. 🔴 What are the memory and performance costs of DataSet? Why is it rarely used in new Web APIs?
131. 🔴 Is DataSet/DataTable thread-safe?
132. 🔴 Why is deserializing DataSet/DataTable from untrusted input a security risk?

---

## 9. DataAdapter & CommandBuilder

133. 🟢 What is a `SqlDataAdapter`?
134. 🟢 What does `Fill()` do? Does it need an open connection?
135. 🟡 What happens to the connection state when `Fill()` is called on a closed vs open connection?
136. 🟡 What are `SelectCommand`, `InsertCommand`, `UpdateCommand`, `DeleteCommand`?
137. 🟡 What does `Update()` on a DataAdapter do? How does it decide which command to run per row?
138. 🟡 What is `SqlCommandBuilder`? What are its limitations?
139. 🟡 What is `FillSchema()` and `MissingSchemaAction`?
140. 🟡 What are `TableMappings` and `ColumnMappings`?
141. 🟡 What is `UpdateBatchSize` in a DataAdapter?
142. 🟡 How does a DataAdapter handle optimistic concurrency? What is `DBConcurrencyException`?
143. 🟡 What are `RowUpdating` and `RowUpdated` events?
144. 🟡 How do you fill a DataSet with multiple tables from one query?
145. 🔴 How do you get identity values back into the DataTable after `Update()`?
146. 🟡 How do you implement paging with a DataAdapter (`Fill(startRecord, maxRecords)`)? Why is it inefficient?

---

## 10. Connected vs Disconnected Architecture

147. 🟢 Explain connected architecture with an example.
148. 🟢 Explain disconnected architecture with an example.
149. 🟡 Compare DataReader and DataSet in terms of speed, memory, connection usage and functionality.
150. 🟡 When would you choose a DataReader over a DataSet and vice versa?
151. 🟡 Why was disconnected architecture popular in WinForms/Web Forms apps?
152. 🔴 Which approach is better for a high-traffic Web API and why?

---

## 11. Stored Procedures & Functions

153. 🟢 How do you call a stored procedure using ADO.NET?
154. 🟢 How do you pass input parameters to a stored procedure?
155. 🟡 How do you get output parameters from a stored procedure?
156. 🟡 How do you get the return value of a stored procedure?
157. 🟡 How do you call a stored procedure that returns multiple result sets?
158. 🟡 How do you call a scalar-valued function from ADO.NET?
159. 🟡 How do you call a table-valued function from ADO.NET?
160. 🟡 What are the advantages and disadvantages of stored procedures vs inline SQL?
161. 🟡 How do you handle `RAISERROR` / `THROW` from a stored procedure in C#?
162. 🟡 What is `SqlException.Number` and how do you map SQL error numbers to business errors?
163. 🔴 How do you discover stored procedure parameters at runtime (`SqlCommandBuilder.DeriveParameters`)? Why avoid it in hot paths?
164. 🔴 How do you call a stored procedure that takes a table-valued parameter?

---

## 12. Transactions

165. 🟢 What is a transaction? What are the ACID properties?
166. 🟢 How do you use `SqlTransaction` in ADO.NET?
167. 🟢 What happens if you don't call `Commit()` before disposing a transaction?
168. 🟡 Why must you assign the transaction to every command (`command.Transaction = tx`)? What error occurs if you don't?
169. 🟡 How do you roll back a transaction on error?
170. 🟡 What are savepoints (`Save()`, `Rollback(savepointName)`)?
171. 🟡 How do you set the isolation level (`BeginTransaction(IsolationLevel.Serializable)`)?
172. 🔴 Explain each isolation level and the anomalies it prevents (dirty read, non-repeatable read, phantom read).
173. 🔴 What is Snapshot isolation vs Read Committed Snapshot (RCSI)?
174. 🟡 What is `TransactionScope`? How is it different from `SqlTransaction`?
175. 🟡 What is the default isolation level of `TransactionScope`? Why can it cause problems?
176. 🔴 When does a `TransactionScope` escalate to a distributed transaction (MSDTC)? Is MSDTC supported in .NET Core/.NET 5+?
177. 🔴 Why must you use `TransactionScopeAsyncFlowOption.Enabled` with async code?
178. 🔴 What is the default timeout for `TransactionScope`?
179. 🔴 What happens to the isolation level of a pooled connection after a transaction ends?
180. 🔴 What is a deadlock in SQL Server? How do you handle error 1205 in ADO.NET?
181. 🟡💰 How do you implement a fund transfer (debit + credit) atomically with ADO.NET?
182. 🔴 How do you share a transaction between ADO.NET and Dapper / EF Core?

---

## 13. Async ADO.NET

183. 🟢 What async methods does ADO.NET provide (`OpenAsync`, `ExecuteReaderAsync`, `ExecuteNonQueryAsync`, `ExecuteScalarAsync`, `ReadAsync`)?
184. 🟡 Why should you use async ADO.NET in ASP.NET Core?
185. 🟡 Does async ADO.NET make a single query faster?
186. 🟡 How do you pass a `CancellationToken` to ADO.NET async methods?
187. 🟡 What is `await using` with `SqlConnection` and `SqlDataReader`?
188. 🔴 What are known performance issues with `ReadAsync` and large columns in `Microsoft.Data.SqlClient`? How do you mitigate them?
189. 🔴 What happens if you mix sync and async calls on the same connection?
190. 🔴 Can you run multiple async commands in parallel on the same connection?
191. 🔴 How do you stream rows to an API client using `IAsyncEnumerable<T>` with a DataReader?

---

## 14. Bulk Operations & Table-Valued Parameters

192. 🟡 What is `SqlBulkCopy`? When should you use it?
193. 🟡 What are `BatchSize`, `BulkCopyTimeout`, `ColumnMappings`, `NotifyAfter` in `SqlBulkCopy`?
194. 🟡 What are `SqlBulkCopyOptions` (`KeepIdentity`, `CheckConstraints`, `FireTriggers`, `TableLock`, `UseInternalTransaction`)?
195. 🟡 Can `SqlBulkCopy` take a `DataTable`, a `DataReader` and an `IEnumerable<T>`?
196. 🔴 How do you use `SqlBulkCopy` inside an existing transaction?
197. 🔴 How do you perform a bulk upsert (bulk copy into a staging table + `MERGE`)?
198. 🟡 What is a table-valued parameter (TVP)? How do you pass one from ADO.NET?
199. 🟡 What is `SqlDataRecord` and how is it used with TVPs?
200. 🟡 TVP vs `SqlBulkCopy` vs batching multiple inserts — when to use which?
201. 🟡 What is `SqlBatch` / `DbBatch` (.NET 6+)?
202. 🔴 How would you insert 10 million rows from a CSV file into SQL Server efficiently?

---

## 15. Exception Handling & Resiliency

203. 🟢 What is `SqlException`? What useful properties does it have (`Number`, `State`, `Class`, `LineNumber`, `Procedure`, `Errors`)?
204. 🟢 How do you handle database exceptions in ADO.NET?
205. 🟡 What are common SQL error numbers (2627/2601 unique violation, 547 FK violation, 1205 deadlock, -2 timeout, 4060 cannot open database, 18456 login failed)?
206. 🟡 What is the difference between `SqlException` and `InvalidOperationException` in ADO.NET?
207. 🟡 How do you detect a command timeout?
208. 🟡 What are transient errors? Which errors should be retried?
209. 🟡 How do you implement retry logic for transient failures (Polly, `SqlRetryLogicBaseProvider`)?
210. 🔴 What is the configurable retry logic in `Microsoft.Data.SqlClient` (`RetryLogicProvider`)?
211. 🔴 Why is retrying a non-idempotent command dangerous? 💰
212. 🟡 How do you make sure connections are closed when an exception occurs?

---

## 16. Data Types, NULL Handling & Conversions

213. 🟢 What is `DBNull.Value`? How is it different from `null`?
214. 🟢 How do you safely read a nullable column into a nullable C# type?
215. 🟡 What is `SqlDbType`? How do SQL Server types map to .NET types?
216. 🟡 What are `System.Data.SqlTypes` (`SqlInt32`, `SqlDecimal`, `SqlMoney`)? When would you use them?
217. 🟡💰 How do `decimal`, `money` and `float` SQL types map to .NET? Which should you use for money?
218. 🟡 How do you handle `datetime` vs `datetime2` vs `datetimeoffset` in ADO.NET?
219. 🟡 Why can `DateTime.MinValue` cause an error when inserting into a `datetime` column?
220. 🟡 How do you read and write `varbinary(max)` / BLOB data?
221. 🟡 How do you read and write `uniqueidentifier`?
222. 🔴 What is the precision loss risk when passing a `decimal` parameter without specifying precision/scale?
223. 🟡 How do you handle `varchar` vs `nvarchar` parameters and Unicode data?
224. 🟡 How do you map enums to database columns in ADO.NET?

---

## 17. Security

225. 🟢 How do you prevent SQL injection in ADO.NET?
226. 🟡 Why should you use least-privilege database accounts for applications?
227. 🟡 How do you protect sensitive data in connection strings?
228. 🟡 What is `Encrypt=True` and `TrustServerCertificate=False`? Why do they matter?
229. 🟡 What is Always Encrypted and how does ADO.NET support it (`Column Encryption Setting=Enabled`)? 💰
230. 🟡 What is `Persist Security Info=False`?
231. 🟡 Should you log full SQL queries with parameter values? Why not? 💰
232. 🔴 What is the risk of building dynamic `ORDER BY` clauses from user input? How do you whitelist safely?
233. 🔴 How do you use Azure AD / Managed Identity authentication instead of passwords?

---

## 18. Performance & Optimization

234. 🟢 How do you improve ADO.NET performance? List at least 10 techniques.
235. 🟢 Why is a DataReader faster than a DataSet?
236. 🟡 Why should you select only the columns you need instead of `SELECT *`?
237. 🟡 How does connection pooling improve performance?
238. 🟡 How does using `SqlDbType` and `Size` on parameters improve plan reuse?
239. 🟡 How do you reduce database roundtrips (batching, multiple result sets, TVPs)?
240. 🟡 How do you implement efficient paging (`OFFSET FETCH`, keyset paging)?
241. 🟡 Why should you use `ExecuteScalar` instead of `ExecuteReader` for a single value?
242. 🟡 How does `CommandBehavior.SequentialAccess` improve performance for large columns?
243. 🔴 How do you identify slow queries from your ADO.NET application (Query Store, Extended Events, `StatisticsEnabled`, `RetrieveStatistics`)?
244. 🔴 What is the cost of opening a physical connection vs a pooled one?
245. 🔴 How do you avoid allocations when reading large result sets?
246. 🔴 When would you use ADO.NET directly instead of an ORM for performance?

---

## 19. Provider-Agnostic Code (DbProviderFactory)

247. 🟡 What is `DbProviderFactory`? How do you write database-independent code?
248. 🟡 What is `DbProviderFactories.GetFactory()` and how do you register factories in .NET Core?
249. 🟡 What are the limitations of writing fully provider-agnostic SQL?
250. 🟡 What is `DbDataSource` (.NET 7) and why was it introduced?
251. 🔴 How would you design a data access layer that supports both SQL Server and PostgreSQL?

---

## 20. Advanced Features

252. 🟡 What is MARS (Multiple Active Result Sets)? How do you enable it? What are its drawbacks?
253. 🟡 What is `SqlDependency`? What is query notification? What are its limitations?
254. 🟡 How do you read XML data from SQL Server using ADO.NET (`ExecuteXmlReader`, `FOR XML`)?
255. 🟡 How do you read JSON data from SQL Server (`FOR JSON`) using ADO.NET?
256. 🟡 How do you get schema information (`GetSchema()`)?
257. 🟡 What is `SqlConnection.RetrieveStatistics()`?
258. 🔴 What is `SqlClientDiagnosticListener` / EventSource tracing in `Microsoft.Data.SqlClient`?
259. 🔴 What is `SqlCredential` and `SecureString` usage in SqlClient?
260. 🔴 How does ADO.NET support Always On availability groups and failover?

---

## 21. ADO.NET vs Dapper vs EF Core

261. 🟢 What is the difference between ADO.NET and Entity Framework?
262. 🟢 What is Dapper? How is it built on top of ADO.NET?
263. 🟡 Compare ADO.NET, Dapper and EF Core in terms of performance, productivity, control and maintainability.
264. 🟡 When would you choose raw ADO.NET over Dapper or EF Core?
265. 🟡 Can you use ADO.NET, Dapper and EF Core in the same project? How do you share connections and transactions?
266. 🔴 How would you migrate a legacy ADO.NET data layer to Dapper or EF Core?

---

## 22. Design Patterns & Architecture with ADO.NET

267. 🟡 How do you design a Data Access Layer (DAL) using ADO.NET?
268. 🟡 How do you implement the Repository pattern with ADO.NET?
269. 🟡 How do you implement Unit of Work with ADO.NET transactions?
270. 🟡 How do you write a reusable helper to execute queries and map results (generic `Query<T>` with a mapper delegate)?
271. 🟡 How do you register ADO.NET dependencies with DI in ASP.NET Core (connection factory)?
272. 🟡 Should `SqlConnection` be registered as singleton, scoped or transient in DI? Why?
273. 🔴 What is the problem with keeping a single static `SqlConnection` for the whole application?
274. 🔴 What is the old "SqlHelper" / Data Access Application Block and what problems did it have?

---

## 23. Testing ADO.NET Code

275. 🟡 How do you unit test code that uses ADO.NET?
276. 🟡 Why is it hard to mock `SqlConnection` and `SqlCommand`? How do interfaces (`IDbConnection`) help?
277. 🟡 How do you write integration tests against a real database (Testcontainers, LocalDB)?
278. 🟡 How do you keep tests isolated (transactions rolled back, test databases, Respawn)?
279. 🔴 How do you test stored procedures and transaction rollbacks?

---

## 24. Financial-Domain ADO.NET Questions 💰

280. 🟡💰 Why do many banks and financial systems still use ADO.NET and stored procedures?
281. 🟡💰 How do you pass and read monetary values safely (`decimal` with precision/scale, avoiding `float`)?
282. 🔴💰 How do you implement an atomic fund transfer with ADO.NET and a transaction?
283. 🔴💰 How do you prevent double debits under concurrent requests (`UPDLOCK`, `ROWLOCK`, conditional `UPDATE ... WHERE Balance >= @amount`, row version)?
284. 🔴💰 How do you check the rows affected to detect a failed conditional update?
285. 🔴💰 How do you implement idempotent payment inserts using a unique constraint and handling error 2627/2601?
286. 🔴💰 How do you implement an audit trail for every financial transaction?
287. 🔴💰 Which isolation level would you use for balance updates vs reporting queries?
288. 🔴💰 How do you process end-of-day batch jobs with millions of rows using ADO.NET?
289. 🔴💰 How do you handle deadlocks in high-volume transaction systems?
290. 🔴💰 How do you mask sensitive data (account number, card number) when logging SQL errors?
291. 🔴💰 How do you design a reconciliation job that compares two large datasets efficiently?

---

## 25. Tricky ADO.NET Questions

292. 🟡 Why do I get "ExecuteReader requires an open and available Connection"?
293. 🟡 Why do I get "There is already an open DataReader associated with this Command which must be closed first"?
294. 🟡 Why do I get "ExecuteNonQuery requires the command to have a transaction when the connection assigned to the command is in a pending local transaction"?
295. 🟡 Why do I get "Timeout expired" when getting a connection from the pool?
296. 🟡 Why do I get "Procedure or function expects parameter which was not supplied" even though I added it?
297. 🟡 Why does `ExecuteNonQuery()` return -1 for my UPDATE statement?
298. 🟡 Why does `ExecuteScalar()` return `null` and not `DBNull.Value` (or vice versa)?
299. 🟡 Why is my output parameter `null` after `ExecuteReader()`?
300. 🟡 Why do I get an `InvalidCastException` when reading a column?
301. 🟡 Why does `reader.GetInt32()` throw when the value is NULL?
302. 🟡 Why does `(int)cmd.ExecuteScalar()` throw for `COUNT(*)` in some cases and `SUM()` in others?
303. 🟡 Why does passing `null` as a parameter value throw an error?
304. 🟡 Why are my `decimal` values rounded when saving to the database? 💰
305. 🟡 Why does my query using `AddWithValue` run slowly while the same query in SSMS is fast?
306. 🟡 Why is my query fast in SSMS but slow from the application (ARITHABORT, parameter sniffing)?
307. 🟡 Why does `SqlDataAdapter.Fill()` work even though I never opened the connection?
308. 🟡 Why does `Fill()` leave my connection open in one case and closed in another?
309. 🟡 Why does `DataAdapter.Update()` do nothing after I modified rows?
310. 🟡 Why does `AcceptChanges()` before `Update()` cause no database changes?
311. 🟡 Why does `SqlCommandBuilder` fail to generate commands for my query?
312. 🟡 Why does `DataTable.Select()` throw a syntax error for some filter strings?
313. 🟡 Why does a DataRow show `RowState = Detached`?
314. 🟡 Why does my transaction appear to commit even though I didn't call `Commit()` (or vice versa)?
315. 🟡 Why does `Dispose()` of the connection not throw even though the transaction was never committed? What happens to the data?
316. 🔴 Why do connection pool timeouts occur even though I always call `Close()`?
317. 🔴 Why does the pool keep growing when using Windows authentication with impersonation?
318. 🔴 Why does a pooled connection sometimes come back with a different isolation level?
319. 🔴 Why does a `TransactionScope` throw "MSDTC is unavailable" or "platform not supported" in .NET Core?
320. 🔴 Why does a `TransactionScope` with async code throw "A TransactionScope must be disposed on the same thread that it was created"?
321. 🔴 Why do I get error 1205 (deadlock victim)? How should the application respond?
322. 🔴 Why does `SqlBulkCopy` silently map columns by ordinal instead of name?
323. 🔴 Why does `SqlBulkCopy` fail with "The given value of type String from the data source cannot be converted to type decimal"?
324. 🔴 Why does `ReadAsync` with a huge `varbinary(max)` column perform much worse than `Read`?
325. 🔴 Why does enabling MARS cause unexpected performance or locking issues?
326. 🔴 Why does `@@IDENTITY` return a wrong ID when a trigger exists on the table?
327. 🔴 Why do I get "Login failed" / certificate errors after upgrading to `Microsoft.Data.SqlClient` 4+?
328. 🔴 Why is `SqlConnection` in a static field a bad idea in a web application?
329. 🔴 Why can a missed `using` on a DataReader with `CommandBehavior.CloseConnection` still leak connections?
330. 🔴 What happens if two threads use the same `SqlConnection` at the same time?

---

## 26. Predict the Behavior (Code Snippets)

> What happens when each snippet runs? If it fails, say why.

**331. 🟢 Command on closed connection**
```csharp
using var conn = new SqlConnection(cs);
using var cmd = new SqlCommand("SELECT COUNT(*) FROM Customers", conn);
var count = (int)cmd.ExecuteScalar();
```

**332. 🟡 Two DataReaders on one connection**
```csharp
using var conn = new SqlConnection(cs);
conn.Open();
using var r1 = new SqlCommand("SELECT * FROM Customers", conn).ExecuteReader();
using var r2 = new SqlCommand("SELECT * FROM Orders", conn).ExecuteReader();
```
What happens with and without `MultipleActiveResultSets=True`?

**333. 🟡 ExecuteScalar with no rows**
```csharp
var cmd = new SqlCommand("SELECT Name FROM Customers WHERE Id = -1", conn);
var result = cmd.ExecuteScalar();
Console.WriteLine(result == null);
Console.WriteLine(result == DBNull.Value);
```

**334. 🟡 ExecuteScalar with a NULL value**
```csharp
var cmd = new SqlCommand("SELECT SUM(Amount) FROM Payments WHERE 1 = 0", conn);
var result = cmd.ExecuteScalar();
decimal total = (decimal)result;
```

**335. 🟡 ExecuteNonQuery return value**
```csharp
var cmd = new SqlCommand("SET NOCOUNT ON; UPDATE Accounts SET Balance = Balance + 1 WHERE Id = 1", conn);
int rows = cmd.ExecuteNonQuery();
Console.WriteLine(rows);
```
What is printed? What if `SET NOCOUNT ON` is removed?

**336. 🟡 ExecuteNonQuery on a SELECT**
```csharp
var cmd = new SqlCommand("SELECT * FROM Customers", conn);
Console.WriteLine(cmd.ExecuteNonQuery());
```

**337. 🟡 Null parameter**
```csharp
cmd.Parameters.AddWithValue("@MiddleName", customer.MiddleName); // MiddleName is null
cmd.ExecuteNonQuery();
```

**338. 🟡 Output parameter with DataReader**
```csharp
var outParam = cmd.Parameters.Add("@Total", SqlDbType.Int);
outParam.Direction = ParameterDirection.Output;
using var reader = cmd.ExecuteReader();
Console.WriteLine(outParam.Value);
while (reader.Read()) { }
```
What is printed? When does the value become available?

**339. 🟡 Reading NULL**
```csharp
while (reader.Read())
{
    int age = reader.GetInt32(reader.GetOrdinal("Age")); // some rows have NULL Age
}
```

**340. 🟡 Transaction not assigned to command**
```csharp
conn.Open();
using var tx = conn.BeginTransaction();
var cmd = new SqlCommand("INSERT INTO Logs(Msg) VALUES('x')", conn);
cmd.ExecuteNonQuery();
tx.Commit();
```

**341. 🟡 Transaction without Commit**
```csharp
using (var conn = new SqlConnection(cs))
{
    conn.Open();
    using var tx = conn.BeginTransaction();
    var cmd = new SqlCommand("INSERT INTO Logs(Msg) VALUES('x')", conn, tx);
    cmd.ExecuteNonQuery();
}
```
Is the row saved?

**342. 🔴 Partial failure inside a transaction**
```csharp
using var tx = conn.BeginTransaction();
try
{
    new SqlCommand("UPDATE Accounts SET Balance = Balance - 100 WHERE Id = 1", conn, tx).ExecuteNonQuery();
    new SqlCommand("UPDATE Accounts SET Balance = Balance + 100 WHERE Id = 999", conn, tx).ExecuteNonQuery(); // Id 999 doesn't exist
    tx.Commit();
}
catch { tx.Rollback(); }
```
Is money lost? Is an exception thrown? What should be checked? 💰

**343. 🟡 Fill on a closed connection**
```csharp
var conn = new SqlConnection(cs);
var adapter = new SqlDataAdapter("SELECT * FROM Customers", conn);
var table = new DataTable();
adapter.Fill(table);
Console.WriteLine(conn.State);
```
What is printed? What if `conn.Open()` is called before `Fill()`?

**344. 🟡 AcceptChanges before Update**
```csharp
table.Rows[0]["Name"] = "Updated";
table.AcceptChanges();
adapter.Update(table);
```
Is the database updated?

**345. 🟡 Delete vs Remove**
```csharp
table.Rows[0].Delete();
table.Rows.Remove(table.Rows[1]);
adapter.Update(table);
```
Which rows are deleted in the database?

**346. 🟡 DataRowState**
```csharp
var row = table.NewRow();
Console.WriteLine(row.RowState);
table.Rows.Add(row);
Console.WriteLine(row.RowState);
table.AcceptChanges();
row["Name"] = "A";
Console.WriteLine(row.RowState);
```

**347. 🔴 Connection leak**
```csharp
public SqlDataReader GetCustomers()
{
    var conn = new SqlConnection(cs);
    conn.Open();
    var cmd = new SqlCommand("SELECT * FROM Customers", conn);
    return cmd.ExecuteReader();
}
```
What happens when this is called 200 times without closing the reader? How do you fix it?

**348. 🔴 Pool fragmentation**
```csharp
var cs1 = "Server=db;Database=Bank;User Id=app;Password=x;";
var cs2 = "Server=db; Database=Bank; User Id=app; Password=x;";
```
Do connections opened with `cs1` and `cs2` share the same pool?

**349. 🔴 AddWithValue type inference**
```csharp
// Column AccountNo is varchar(20) with an index
cmd.CommandText = "SELECT * FROM Accounts WHERE AccountNo = @acc";
cmd.Parameters.AddWithValue("@acc", "ACC123");
```
What type is the parameter sent as? What is the performance impact?

**350. 🔴 Decimal parameter precision**
```csharp
var p = cmd.Parameters.Add("@Amount", SqlDbType.Decimal);
p.Value = 1234.5678m;
// Column is decimal(18,2)
```
What is stored? What if `p.Precision` and `p.Scale` are not set and the column is `decimal(18,4)`? 💰

**351. 🔴 SQL injection**
```csharp
var sql = "SELECT * FROM Users WHERE Name = '" + txtName.Text + "'";
var cmd = new SqlCommand(sql, conn);
```
What happens if the user enters `' OR 1=1 --`? How do you fix it?

**352. 🔴 Dynamic ORDER BY**
```csharp
cmd.CommandText = "SELECT * FROM Trades ORDER BY @sortColumn";
cmd.Parameters.AddWithValue("@sortColumn", "TradeDate");
```
Does the result get sorted by `TradeDate`? Why or why not?

**353. 🔴 TransactionScope with async**
```csharp
using (var scope = new TransactionScope())
{
    await conn.OpenAsync();
    await cmd.ExecuteNonQueryAsync();
    scope.Complete();
}
```

**354. 🔴 TransactionScope with two connections**
```csharp
using (var scope = new TransactionScope())
{
    using (var c1 = new SqlConnection(cs)) { c1.Open(); /* insert */ }
    using (var c2 = new SqlConnection(cs)) { c2.Open(); /* insert */ }
    scope.Complete();
}
```
Does the transaction escalate to a distributed transaction? What happens on .NET Core?

**355. 🔴 Static connection in a web app**
```csharp
public static class Db
{
    public static SqlConnection Conn = new SqlConnection(cs);
}
// Every request does: Db.Conn.Open(); ... Db.Conn.Close();
```
What happens under concurrent requests?

**356. 🟡 SqlBulkCopy column mappings**
```csharp
// DataTable columns: Name, Amount     | Table columns: Id (identity), Amount, Name
using var bulk = new SqlBulkCopy(conn) { DestinationTableName = "Payments" };
bulk.WriteToServer(dataTable);
```
What happens? How do you fix it?

**357. 🟡 Multiple result sets**
```csharp
cmd.CommandText = "SELECT * FROM Customers; SELECT * FROM Orders;";
using var reader = cmd.ExecuteReader();
while (reader.Read()) { /* customers */ }
// orders are never read
```
How do you read the second result set? What happens if you skip `NextResult()`?

**358. 🟡 CommandBehavior.CloseConnection**
```csharp
var reader = cmd.ExecuteReader(CommandBehavior.CloseConnection);
reader.Close();
Console.WriteLine(conn.State);
```

**359. 🔴 IDENTITY retrieval with trigger**
```csharp
cmd.CommandText = "INSERT INTO Orders(CustomerId) VALUES(@c); SELECT @@IDENTITY;";
var id = cmd.ExecuteScalar();
// A trigger on Orders inserts into an AuditLog table that also has an identity column
```
Which ID is returned? How do you fix it?

---

## 27. Coding & Hands-On Tasks

360. 🟢 Write code to connect to SQL Server and print all rows from a `Customers` table using a DataReader.
361. 🟢 Write CRUD methods (Insert, Select, Update, Delete) for `Product` using parameterized queries.
362. 🟢 Write code to get a single value (e.g., total customers) using `ExecuteScalar`.
363. 🟡 Insert a record and return the newly generated identity using `OUTPUT INSERTED.Id`.
364. 🟡 Call a stored procedure with input, output and return value parameters.
365. 🟡 Read multiple result sets from a stored procedure into two lists.
366. 🟡 Fill a DataSet with two tables and create a DataRelation between them.
367. 🟡 Use a DataAdapter with `SqlCommandBuilder` to update modified rows in a DataTable.
368. 🟡 Convert a `DataTable` to `List<T>` using a generic method.
369. 🟡 Write a generic `Query<T>(sql, parameters, mapper)` helper method using ADO.NET.
370. 🟡 Implement paging using `OFFSET ... FETCH` with parameters.
371. 🟡 Implement a safe search with optional filters (dynamic WHERE with parameters).
372. 🟡 Implement a whitelist-based dynamic `ORDER BY`.
373. 🟡 Write async versions of CRUD methods with `CancellationToken` support.
374. 🟡 Implement a repository using ADO.NET registered in ASP.NET Core DI.
375. 🟡 Implement a transaction that inserts an order and its order items atomically.
376. 🔴 Implement an atomic fund transfer with `SqlTransaction`, checking rows affected and rolling back on failure. 💰
377. 🔴 Implement a conditional debit (`UPDATE ... WHERE Balance >= @amount`) and handle insufficient funds. 💰
378. 🔴 Implement idempotent payment insertion by catching unique constraint violations (2627/2601). 💰
379. 🔴 Implement retry logic for deadlocks (1205) and transient errors with exponential backoff.
380. 🔴 Bulk insert 1 million rows using `SqlBulkCopy` from a streaming `IDataReader`.
381. 🔴 Pass a list of IDs to a stored procedure using a table-valued parameter.
382. 🔴 Implement a bulk upsert using a staging table and `MERGE`.
383. 🔴 Stream rows from a DataReader as `IAsyncEnumerable<T>` to an API endpoint.
384. 🔴 Implement a provider-agnostic DAL using `DbProviderFactory` / `DbDataSource`.
385. 🔴 Write an audit-logging wrapper that records every command executed with masked parameters. 💰

---

## 28. Scenario-Based & Debugging Questions

386. 🟡 Your application throws "connection pool timeout" errors under load. How do you investigate?
387. 🟡 A query is fast in SSMS but slow from your C# code. How do you investigate?
388. 🟡 Your app intermittently fails with deadlock errors. How do you diagnose and fix them?
389. 🟡 Users report that some updates are not saved. How do you debug the ADO.NET code?
390. 🟡 After upgrading to `Microsoft.Data.SqlClient`, connections fail with certificate errors. What do you do?
391. 🟡 Memory usage is high when loading a large report into a DataSet. How do you reduce it?
392. 🟡 A batch job that inserts rows one by one takes hours. How do you speed it up?
393. 🔴 A fund transfer sometimes debits one account but doesn't credit the other. How do you find and fix the bug? 💰
394. 🔴 Duplicate payments appear when a client retries a request after a timeout. How do you prevent this? 💰
395. 🔴 The database CPU spikes because of thousands of different query plans for the same query. What is the cause?
396. 🔴 You need to migrate a legacy ADO.NET + DataSet application to modern .NET. How do you plan it?
397. 🔴 How would you review a pull request containing ADO.NET code? What would you look for?
398. 🔴 How do you design a high-throughput data access layer for a trading system? 💰

---

## 29. Rapid-Fire Round

399. 🟢 Which namespace contains `SqlConnection` in modern .NET?
400. 🟢 Which method is used for INSERT/UPDATE/DELETE?
401. 🟢 Which method returns a single value?
402. 🟢 Which method returns a DataReader?
403. 🟢 Is a DataReader connected or disconnected?
404. 🟢 Is a DataSet connected or disconnected?
405. 🟢 Which object fills a DataSet?
406. 🟢 What does `DBNull.Value` represent?
407. 🟢 Is connection pooling enabled by default?
408. 🟢 What is the default `Max Pool Size`?
409. 🟢 What is the default `CommandTimeout`?
410. 🟢 What is the default `Connect Timeout`?
411. 🟡 Can a DataReader move backward?
412. 🟡 Can a DataSet contain multiple tables?
413. 🟡 Does `Fill()` require an open connection?
414. 🟡 Does `Close()` on a pooled connection close the physical connection?
415. 🟡 Can you use a transaction across two different connections without `TransactionScope`?
416. 🟡 Is `SqlConnection` thread-safe?
417. 🟡 What does `CommandType.StoredProcedure` do?
418. 🟡 What does `CommandBehavior.CloseConnection` do?
419. 🟡 What does `AcceptChanges()` do?
420. 🟡 What does `SET NOCOUNT ON` change for ADO.NET?
421. 🔴 What is the SQL error number for a deadlock?
422. 🔴 What is the SQL error number for a unique key violation?
423. 🔴 What is the SQL error number for a command timeout in SqlClient?
424. 🔴 What is `sp_reset_connection`?
425. 🔴 What is the difference between `SCOPE_IDENTITY()` and `@@IDENTITY` in one line?
426. 🔴 What is `DbDataSource` in one line?

---

> **Next part (optional):** Microservices, Authentication/Authorization.
