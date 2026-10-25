# 🎯 Entity Framework Core Interview Questions — Part 3 (Questions Only)

> **Scope:** Entity Framework Core only — fundamentals, DbContext, modeling, relationships, querying, change tracking, saving, migrations, transactions, concurrency, performance, raw SQL, testing, plus a large set of tricky questions and predict-the-behavior code snippets.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers up to EF Core 10 (.NET 10).**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. ORM & EF Core Fundamentals
2. DbContext & DbSet
3. Approaches: Code-First, Database-First
4. Modeling & Configuration (Conventions, Data Annotations, Fluent API)
5. Keys, Indexes & Data Types
6. Relationships
7. Inheritance Mapping (TPH, TPT, TPC)
8. Owned Types, Complex Types, Value Objects & Value Conversions
9. Querying with LINQ
10. Loading Related Data (Eager, Explicit, Lazy)
11. Change Tracking
12. Saving Data (Insert, Update, Delete)
13. Bulk Operations
14. Migrations
15. Transactions
16. Concurrency Handling
17. Raw SQL, Stored Procedures, Views & Functions
18. Global Query Filters, Soft Delete & Multi-Tenancy
19. Interceptors, Events & Shadow Properties
20. Performance & Optimization
21. DbContext Lifetime, Pooling & Threading
22. Logging, Diagnostics & Debugging
23. Database Providers & Special Types
24. Testing with EF Core
25. EF Core vs EF6 vs Dapper vs ADO.NET
26. Design Patterns with EF Core (Repository, Unit of Work, CQRS)
27. Financial-Domain EF Core Questions 💰
28. Tricky EF Core Questions
29. Predict the Behavior (Code Snippets)
30. Coding & Hands-On Tasks
31. Scenario-Based & Debugging Questions
32. Rapid-Fire Round

---

## 1. ORM & EF Core Fundamentals

1. 🟢 What is an ORM? What problems does it solve?
2. 🟢 What is Entity Framework Core?
3. 🟢 What are the advantages and disadvantages of using an ORM?
4. 🟢 What is the difference between Entity Framework 6 and EF Core?
5. 🟢 What databases does EF Core support?
6. 🟢 What is a database provider in EF Core?
7. 🟢 What NuGet packages are needed to use EF Core with SQL Server?
8. 🟢 What is the EF Core model? How is it built?
9. 🟢 What is an entity? What makes a class an entity?
10. 🟢 What is a POCO class?
11. 🟡 What is the impedance mismatch between objects and relational tables?
12. 🟡 What happens internally when you run a LINQ query in EF Core (expression tree → SQL)?
13. 🟡 What are the main components of EF Core architecture (DbContext, model, change tracker, query pipeline, provider)?
14. 🟡 What is the EF Core release cadence? Which versions are LTS?
15. 🟡 What new features were introduced in EF Core 8, 9 and 10?

---

## 2. DbContext & DbSet

16. 🟢 What is `DbContext`? What are its responsibilities?
17. 🟢 What is `DbSet<T>`?
18. 🟢 How do you configure a `DbContext` (`OnConfiguring` vs `AddDbContext`)?
19. 🟢 What is `DbContextOptions` and `DbContextOptionsBuilder`?
20. 🟢 How do you register `DbContext` in ASP.NET Core DI?
21. 🟡 What is the default lifetime of `DbContext` when registered with `AddDbContext`? Why?
22. 🟡 Why is `DbContext` not thread-safe?
23. 🟡 What is `DbContext` pooling (`AddDbContextPool`)? What are its benefits and caveats?
24. 🟡 What is `IDbContextFactory<T>` (`AddDbContextFactory`)? When would you use it?
25. 🟡 Should `DbContext` be long-lived or short-lived? Why?
26. 🟡 Can you have multiple `DbContext` classes in one application? When would you?
27. 🟡 What is `Set<T>()` vs a `DbSet<T>` property?
28. 🟡 What does `OnModelCreating` do? When is it called?
29. 🟡 Is `OnModelCreating` called every time a `DbContext` is created? How is the model cached?
30. 🟡 What is `IEntityTypeConfiguration<T>` and `ApplyConfigurationsFromAssembly`?
31. 🟡 What is `ConfigureConventions` (pre-convention model configuration)?
32. 🟡 What is `Database.EnsureCreated()` vs `Database.Migrate()`?
33. 🟡 What is `DbContext.Database` (`DatabaseFacade`) used for?
34. 🔴 What is a compiled model (`dotnet ef dbcontext optimize`)? When does it help?
35. 🔴 What happens when you dispose a `DbContext`? What happens to tracked entities?

---

## 3. Approaches: Code-First, Database-First

36. 🟢 What is the Code-First approach?
37. 🟢 What is the Database-First approach in EF Core? How is it done (scaffolding)?
38. 🟢 Does EF Core support Model-First (EDMX)?
39. 🟡 What is `Scaffold-DbContext` / `dotnet ef dbcontext scaffold`? What options does it support?
40. 🟡 How do you re-scaffold without losing custom code (partial classes, T4 templates)?
41. 🟡 What are EF Core reverse engineering T4 templates?
42. 🟡 Which approach would you choose for a new project vs a legacy database? Why?
43. 🔴 How do you handle a database owned by a DBA team where you cannot run migrations?

---

## 4. Modeling & Configuration

44. 🟢 What are conventions in EF Core? Give examples.
45. 🟢 What are Data Annotations? Give examples (`[Key]`, `[Required]`, `[MaxLength]`, `[Table]`, `[Column]`, `[NotMapped]`, `[ForeignKey]`, `[InverseProperty]`).
46. 🟢 What is the Fluent API? Why is it more powerful than Data Annotations?
47. 🟡 What is the precedence order: conventions, Data Annotations, Fluent API?
48. 🟢 How do you exclude a property or entity from mapping?
49. 🟢 How do you map an entity to a different table name or schema?
50. 🟢 How do you set a column's data type, length and precision?
51. 🟡 How do you configure default values (`HasDefaultValue`, `HasDefaultValueSql`)?
52. 🟡 What are computed columns (`HasComputedColumnSql`)? Stored vs virtual?
53. 🟡 What is `ValueGeneratedOnAdd`, `ValueGeneratedOnAddOrUpdate` and `ValueGeneratedNever`?
54. 🟡 How do you map an entity to a view (`ToView`)?
55. 🟡 What are keyless entity types (`HasNoKey`)? When are they used?
56. 🟡 What are backing fields? How do you map private fields?
57. 🟡 How does EF Core work with constructors that have parameters?
58. 🟡 How do you map read-only collections (`IReadOnlyCollection<T>` with backing field)?
59. 🟡 How do nullable reference types affect EF Core's required/optional configuration?
60. 🟡 What are table splitting and entity splitting?
61. 🟡 What is a property bag / shared-type entity type (`Dictionary<string, object>`)?
62. 🟡 How do you configure column ordering (`HasColumnOrder`)?
63. 🟡 How do you add check constraints (`HasCheckConstraint` / `ToTable(t => t.HasCheckConstraint(...))`)?
64. 🟡 How do you add comments to tables and columns?
65. 🔴 How do you write a custom convention?
66. 🔴 How do you map private setters and encapsulated domain models (DDD) in EF Core?

---

## 5. Keys, Indexes & Data Types

67. 🟢 What is a primary key in EF Core? What is the convention for detecting it?
68. 🟢 How do you configure a composite primary key?
69. 🟡 Can a composite key be configured with Data Annotations? (`[PrimaryKey]` in EF Core 7+)
70. 🟢 What is an alternate key (`HasAlternateKey`)? How is it different from a unique index?
71. 🟡 What key types are good choices: `int`, `long`, `Guid`, `string`? Pros and cons?
72. 🔴 What problems do random `Guid` primary keys cause for clustered indexes? What are sequential GUIDs / `Guid.CreateVersion7()`?
73. 🟡 What are identity columns vs sequences (`HasSequence`, `UseHiLo`)?
74. 🔴 What is the HiLo algorithm and when would you use it?
75. 🟢 How do you create an index (`HasIndex`, `[Index]`)?
76. 🟡 How do you create unique, composite, filtered and included-column indexes?
77. 🟡 What are descending indexes (EF Core 7+)?
78. 🟡💰 Why should you configure precision and scale for `decimal` properties? What happens if you don't?
79. 🟡 How is `string` mapped by default in SQL Server? How do you change it (`nvarchar(max)` vs `varchar(50)`)?
80. 🟡 How do you map `DateTime`, `DateTimeOffset`, `DateOnly` and `TimeOnly`?
81. 🟡 How do you map enums? As int or as string?
82. 🟡 How do you map `bool`, `byte[]`, `Guid`, `TimeSpan`?

---

## 6. Relationships

83. 🟢 What types of relationships does EF Core support?
84. 🟢 What are navigation properties? Reference navigation vs collection navigation?
85. 🟢 What is a foreign key property? Is it mandatory to declare one?
86. 🟢 How do you configure a one-to-one relationship?
87. 🟢 How do you configure a one-to-many relationship?
88. 🟢 How do you configure a many-to-many relationship? How did it change in EF Core 5?
89. 🟡 What is a skip navigation in many-to-many?
90. 🟡 When do you need an explicit join entity in many-to-many (payload columns)?
91. 🟡 What are principal entity and dependent entity?
92. 🟡 What is `HasOne`, `WithMany`, `HasMany`, `WithOne`, `HasForeignKey`, `HasPrincipalKey`?
93. 🟡 What is a required vs optional relationship? How does EF Core decide?
94. 🟡 What are cascade delete behaviors (`Cascade`, `Restrict`, `SetNull`, `NoAction`, `ClientSetNull`, `ClientCascade`)?
95. 🟡 What is the default delete behavior for required and optional relationships?
96. 🔴 What causes "may cause cycles or multiple cascade paths" error in SQL Server? How do you fix it?
97. 🟡 What is a self-referencing relationship (e.g., Employee-Manager, Category-Parent)?
98. 🟡 What are unidirectional relationships (navigation on one side only)?
99. 🟡 How do you configure two relationships between the same two entities (`[InverseProperty]`)?
100. 🟡 What is a shadow foreign key?
101. 🔴 What are orphaned entities? How does EF Core handle removing a child from a collection?
102. 🔴 What is relationship fix-up?

---

## 7. Inheritance Mapping

103. 🟢 What inheritance mapping strategies does EF Core support?
104. 🟡 What is Table-Per-Hierarchy (TPH)? What is a discriminator column?
105. 🟡 What is Table-Per-Type (TPT)? What are its performance implications?
106. 🟡 What is Table-Per-Concrete-Type (TPC)? When was it added?
107. 🟡 Compare TPH, TPT and TPC in terms of performance, storage and nullability.
108. 🟡 Which strategy is the default? Which one would you choose and why?
109. 🟡 How do you customise the discriminator column name and values?
110. 🔴 Why does TPC require special key generation strategies (sequences)?
111. 🔴 How do you query only a specific derived type (`OfType<T>()`)?

---

## 8. Owned Types, Complex Types, Value Objects & Value Conversions

112. 🟡 What are owned entity types (`OwnsOne`, `OwnsMany`)?
113. 🟡 How are owned types stored (same table vs separate table)?
114. 🟡 What are complex types (EF Core 8)? How are they different from owned types?
115. 🟡 How do you map a DDD value object (e.g., `Address`, `Money`) in EF Core?
116. 🟡 Can complex types be `struct`s or `record`s? Can they be null?
117. 🟡 What are value converters? Give examples.
118. 🟡 What built-in value converters exist (`EnumToStringConverter`, `BoolToZeroOneConverter`, etc.)?
119. 🟡 What are value comparers? Why are they needed for mutable types converted by value converters?
120. 🔴 What are the limitations of value converters in querying (translation of methods on converted properties)?
121. 🟡 How do you store a list of strings or a custom object in a single column?
122. 🟡 What is JSON column mapping (`ToJson()`)? How do you query inside JSON columns?
123. 🟡 What are primitive collections (EF Core 8) — storing `List<int>` / `string[]` directly?
124. 🔴 How do you encrypt a column using a value converter? What are the trade-offs? 💰

---

## 9. Querying with LINQ

125. 🟢 How do you query data with EF Core?
126. 🟢 What is the difference between `IQueryable<T>` and `IEnumerable<T>` in EF Core?
127. 🟢 When is a LINQ-to-Entities query actually executed?
128. 🟢 What is deferred execution in EF Core?
129. 🟢 What is the difference between `First`, `FirstOrDefault`, `Single`, `SingleOrDefault` and `Find`?
130. 🟡 How does `Find()` differ from `FirstOrDefault()` in terms of database roundtrips?
131. 🟢 What is projection? Why use `Select` to DTOs?
132. 🟢 How do you write joins in EF Core LINQ (navigation vs `Join`)?
133. 🟡 How do you write a left outer join (`GroupJoin` + `SelectMany` + `DefaultIfEmpty`, `LeftJoin` in EF Core 10)?
134. 🟡 How does `GroupBy` translate to SQL? What are its limitations?
135. 🟡 How do you implement pagination (`Skip`/`Take`)? Why is `OrderBy` required?
136. 🔴 What is keyset (seek) pagination? Why is it better than offset pagination for large tables?
137. 🟡 What is client evaluation vs server evaluation?
138. 🟡 What changed in EF Core 3.0 regarding client evaluation?
139. 🟡 What happens if a LINQ method cannot be translated to SQL?
140. 🟡 What is `AsEnumerable()` and when would you use it in a query?
141. 🟡 How do you use `EF.Functions` (`Like`, `DateDiffDay`, `Collate`, `Contains` full-text)?
142. 🟡 How do you perform case-insensitive search in EF Core? How does database collation affect it?
143. 🟡 How does `Contains()` on a local list translate to SQL? What changed in EF Core 8 and 10?
144. 🟡 How do you check if any records exist efficiently (`AnyAsync` vs `CountAsync`)?
145. 🟡 What are `ToListAsync`, `FirstOrDefaultAsync`, `CountAsync` etc.? Why use async methods?
146. 🟡 What is `AsAsyncEnumerable()` / streaming results?
147. 🟡 What are compiled queries (`EF.CompileQuery`, `EF.CompileAsyncQuery`)? When do they help?
148. 🟡 What is query caching and parameterization in EF Core?
149. 🔴 Why can using constants instead of variables in queries cause query plan cache pollution?
150. 🟡 What are query tags (`TagWith`)?
151. 🟡 How do you see the SQL generated by a query (`ToQueryString`, logging)?
152. 🟡 What is a split query (`AsSplitQuery`)? What is a single query?
153. 🔴 What is the cartesian explosion problem? How does `AsSplitQuery` solve it? What are its trade-offs?
154. 🟡 How do you configure the default query splitting behavior globally?
155. 🟡 What are `Union`, `Concat`, `Intersect`, `Except` in EF Core?
156. 🟡 What is `ExecuteSqlRaw` vs `FromSqlRaw`?
157. 🔴 How do you build dynamic queries (dynamic filters, sorting) with `IQueryable`?
158. 🔴 How do you use `Expression<Func<T, bool>>` to build reusable query predicates?

---

## 10. Loading Related Data

159. 🟢 What are the three ways to load related data in EF Core?
160. 🟢 What is eager loading? How do you use `Include()` and `ThenInclude()`?
161. 🟡 What is filtered include (EF Core 5)?
162. 🟢 What is explicit loading (`Entry().Reference().Load()`, `Entry().Collection().Load()`)?
163. 🟢 What is lazy loading? How do you enable it in EF Core?
164. 🟡 What are lazy loading proxies vs `ILazyLoader` injection?
165. 🟡 Why must navigation properties be `virtual` for proxy-based lazy loading?
166. 🔴 What is the N+1 query problem? How does lazy loading cause it?
167. 🔴 Why is lazy loading considered dangerous in Web APIs (serialization, N+1, disposed context)?
168. 🟡 Which loading strategy would you choose and why?
169. 🟡 What is `AutoInclude()` configuration?
170. 🟡 What happens if you use `Include` and then `Select` to a DTO? Is `Include` needed?
171. 🔴 How do you load deep object graphs efficiently?

---

## 11. Change Tracking

172. 🟢 What is change tracking in EF Core?
173. 🟢 What are the entity states (`Added`, `Unchanged`, `Modified`, `Deleted`, `Detached`)?
174. 🟢 What is `AsNoTracking()`? When should you use it?
175. 🟡 What is `AsNoTrackingWithIdentityResolution()`?
176. 🟡 How do you set no-tracking as the default behavior (`UseQueryTrackingBehavior`)?
177. 🟡 What is snapshot change tracking? How does `DetectChanges()` work?
178. 🟡 When is `DetectChanges()` called automatically?
179. 🔴 What is `AutoDetectChangesEnabled`? When would you turn it off?
180. 🔴 What are change-tracking proxies and notification entities (`INotifyPropertyChanged`)?
181. 🟡 What is the identity map / identity resolution in EF Core?
182. 🟡 What is `ChangeTracker.Entries()`? How do you inspect tracked entities?
183. 🟡 What is `ChangeTracker.Clear()`?
184. 🟡 What does `Attach()` do? What state does the entity get?
185. 🟡 What is the difference between `Add`, `Attach`, `Update` and `Remove`?
186. 🔴 What does `Update()` do to the entire graph? Why can it cause unnecessary updates?
187. 🟡 What is `Entry(entity).State = EntityState.Modified`?
188. 🟡 How do you mark only specific properties as modified (`Property(x => x.Name).IsModified = true`)?
189. 🟡 What are `OriginalValues` and `CurrentValues`?
190. 🔴 What is `TrackGraph()`? When would you use it?
191. 🔴 How do you work with disconnected entities (e.g., entities coming from an API request)?
192. 🔴 How does EF Core decide whether a disconnected entity is new or existing (key value set or not)?
193. 🟡 What is `ChangeTracker.DebugView`?

---

## 12. Saving Data

194. 🟢 How do you insert, update and delete data in EF Core?
195. 🟢 What does `SaveChanges()` do? What does it return?
196. 🟢 What is the difference between `SaveChanges()` and `SaveChangesAsync()`?
197. 🟡 Is `SaveChanges()` transactional by default?
198. 🟡 How does EF Core batch multiple statements in one `SaveChanges()` call? What is `MaxBatchSize`?
199. 🟡 How do you insert a parent and children in one go?
200. 🟡 How does EF Core get the generated identity value back after insert?
201. 🟡 How do you update an entity without first loading it from the database?
202. 🟡 How do you delete an entity without loading it?
203. 🟡 What is `SaveChanges(acceptAllChangesOnSuccess: false)` and `AcceptAllChanges()`?
204. 🟡 What happens to the change tracker after a failed `SaveChanges()`?
205. 🟡 What exceptions can `SaveChanges()` throw (`DbUpdateException`, `DbUpdateConcurrencyException`)?
206. 🟡 How do you handle unique constraint violations from `SaveChanges()`?
207. 🟡 How do you implement "upsert" (insert or update) in EF Core?
208. 🔴 How do you override `SaveChanges` to set audit fields (`CreatedAt`, `ModifiedBy`) automatically?
209. 🔴 How does EF Core order INSERT/UPDATE/DELETE commands when saving a graph with dependencies?

---

## 13. Bulk Operations

210. 🟡 What are `ExecuteUpdate` and `ExecuteDelete` (EF Core 7)?
211. 🟡 How are `ExecuteUpdate`/`ExecuteDelete` different from loading entities and calling `SaveChanges()`?
212. 🔴 Do `ExecuteUpdate`/`ExecuteDelete` update the change tracker? Do they fire interceptors and `SaveChanges` overrides?
213. 🔴 Do `ExecuteUpdate`/`ExecuteDelete` respect global query filters and concurrency tokens?
214. 🟡 How do you insert 100,000 records efficiently?
215. 🟡 What are third-party bulk libraries (EFCore.BulkExtensions, Z.EntityFramework.Extensions)? Pros and cons?
216. 🟡 When would you use `SqlBulkCopy` instead of EF Core?
217. 🔴 How do you batch large updates to avoid long locks and log growth?
218. 🟡 What is `ExecuteUpdate` with non-expression lambda syntax in EF Core 10?

---

## 14. Migrations

219. 🟢 What are migrations in EF Core?
220. 🟢 How do you add a migration and update the database (`Add-Migration`, `Update-Database`, `dotnet ef`)?
221. 🟢 What files are generated by a migration (`Up`, `Down`, Designer, ModelSnapshot)?
222. 🟡 What is the `ModelSnapshot` file and why is it important?
223. 🟡 What is the `__EFMigrationsHistory` table?
224. 🟡 How do you remove the last migration? How do you revert a migration that was already applied?
225. 🟡 How do you generate a SQL script from migrations (`Script-Migration`, idempotent scripts)?
226. 🟡 What is an idempotent migration script? Why use it in production deployments?
227. 🟡 What are migration bundles (`dotnet ef migrations bundle`)?
228. 🟡 Should you call `Database.Migrate()` at application startup in production? Why or why not?
229. 🟡 How do you add custom SQL to a migration (`migrationBuilder.Sql()`)?
230. 🟡 How do you seed data (`HasData`, `UseSeeding`/`UseAsyncSeeding` in EF Core 9)?
231. 🟡 What are the limitations of `HasData` seeding?
232. 🔴 How do you rename a column without losing data? Why might EF Core generate drop + add instead?
233. 🔴 How do you handle migrations when multiple developers create migrations in parallel (merge conflicts)?
234. 🔴 How do you split a migration into multiple deployment steps for zero-downtime changes?
235. 🔴 How do you manage migrations for multiple database providers?
236. 🔴 How do you keep migrations in a separate assembly?
237. 🟡 What is `IDesignTimeDbContextFactory<T>` and when is it needed?
238. 🔴 How do you squash/reset migrations in a long-running project?
239. 🟡 What does the "pending model changes" warning/error in EF Core 9 mean?

---

## 15. Transactions

240. 🟢 How does EF Core handle transactions by default?
241. 🟡 How do you use explicit transactions (`Database.BeginTransaction()`)?
242. 🟡 How do you share a transaction across multiple `SaveChanges()` calls?
243. 🟡 How do you share a transaction across multiple `DbContext` instances?
244. 🟡 How do you use `TransactionScope` with EF Core? What are the async caveats (`TransactionScopeAsyncFlowOption`)?
245. 🔴 Does EF Core support distributed transactions? What are the limitations?
246. 🟡 What are savepoints in EF Core (`CreateSavepoint`, `RollbackToSavepoint`)?
247. 🟡 How do you set the isolation level of a transaction?
248. 🔴 Explain isolation levels (Read Uncommitted, Read Committed, Repeatable Read, Serializable, Snapshot) and their effect on EF Core queries.
249. 🔴 How do execution strategies (retry on failure) interact with user-initiated transactions?
250. 🔴 Why do you get "The configured execution strategy does not support user-initiated transactions"? How do you fix it?
251. 🟡💰 Why must a fund transfer (debit + credit) be in a single transaction?

---

## 16. Concurrency Handling

252. 🟢 What is concurrency conflict? What is the "lost update" problem?
253. 🟢 What is optimistic concurrency vs pessimistic concurrency?
254. 🟡 How does EF Core implement optimistic concurrency?
255. 🟡 What is a concurrency token (`[ConcurrencyCheck]`, `IsConcurrencyToken()`)?
256. 🟡 What is a row version / timestamp column (`[Timestamp]`, `IsRowVersion()`)?
257. 🟡 What SQL does EF Core generate when a concurrency token is configured?
258. 🟡 What is `DbUpdateConcurrencyException`? How do you handle it?
259. 🟡 What are the resolution strategies: client wins, database wins, merge?
260. 🔴 How do you implement pessimistic locking with EF Core (`UPDLOCK`, `FOR UPDATE` via raw SQL)?
261. 🔴 How do you handle concurrency for disconnected entities in a Web API (passing row version to client)?
262. 🔴 How do you implement optimistic concurrency on PostgreSQL (`xmin`)?
263. 🔴💰 How would you prevent double withdrawal from an account under high concurrency?

---

## 17. Raw SQL, Stored Procedures, Views & Functions

264. 🟢 How do you execute raw SQL queries in EF Core?
265. 🟡 What is the difference between `FromSql`, `FromSqlRaw` and `FromSqlInterpolated`?
266. 🔴 How can `FromSqlRaw` lead to SQL injection? How does `FromSql` with interpolated strings prevent it?
267. 🟡 What is `SqlQuery<T>` (EF Core 7/8) for unmapped types and scalar values?
268. 🟡 How do you execute non-query SQL (`ExecuteSql`, `ExecuteSqlRaw`)?
269. 🟡 How do you call a stored procedure that returns entities?
270. 🟡 How do you call a stored procedure with output parameters?
271. 🟡 How do you map insert/update/delete to stored procedures (`InsertUsingStoredProcedure`, EF Core 7)?
272. 🟡 Can you compose LINQ on top of `FromSql`? When can't you?
273. 🟡 How do you map a database view?
274. 🟡 How do you map scalar and table-valued functions (`HasDbFunction`)?
275. 🟡 How do you get access to the underlying `DbConnection` for ADO.NET or Dapper?
276. 🔴 When would you choose raw SQL or stored procedures over LINQ?

---

## 18. Global Query Filters, Soft Delete & Multi-Tenancy

277. 🟡 What are global query filters (`HasQueryFilter`)?
278. 🟡 How do you implement soft delete with EF Core?
279. 🟡 How do you bypass a global query filter (`IgnoreQueryFilters`)?
280. 🟡 What are named query filters (EF Core 10) and how do you disable one filter selectively?
281. 🟡 How do you implement multi-tenancy using global query filters?
282. 🔴 What are the pitfalls of global query filters with required navigations and `Include`?
283. 🔴 Why is the value used in a query filter referenced from a `DbContext` field instead of a constant?
284. 🔴 What multi-tenancy strategies exist (shared table with TenantId, schema per tenant, database per tenant) and how does EF Core support each?
285. 🔴 How do you make sure a unique index works correctly with soft delete (filtered indexes)?

---

## 19. Interceptors, Events & Shadow Properties

286. 🟡 What are interceptors in EF Core? Name the types (command, connection, transaction, SaveChanges, materialization, query expression).
287. 🟡 How do you write a `SaveChangesInterceptor` for auditing?
288. 🟡 How do you write a `DbCommandInterceptor` to log or modify SQL?
289. 🟡 What are EF Core events (`SavingChanges`, `SavedChanges`, `ChangeTracker.Tracked`, `StateChanged`)?
290. 🟡 What are shadow properties? How do you define and read them?
291. 🟡 How do you use shadow properties for audit fields (`CreatedAt`, `UpdatedBy`)?
292. 🔴 How do you implement an audit trail that stores old and new values for every change? 💰
293. 🔴 What is `IMaterializationInterceptor` used for?
294. 🔴 How do you implement temporal tables (SQL Server) with EF Core? How do you query history (`TemporalAsOf`)?

---

## 20. Performance & Optimization

295. 🟢 How do you improve EF Core query performance? List at least 10 techniques.
296. 🟢 Why should you use `AsNoTracking()` for read-only queries?
297. 🟢 Why should you select only the columns you need?
298. 🟡 Why should you avoid `ToList()` before `Where()`?
299. 🟡 How do you detect and fix N+1 queries?
300. 🟡 How do you detect slow queries in EF Core?
301. 🟡 What is the impact of loading large object graphs?
302. 🟡 When should you use compiled queries?
303. 🟡 When should you use `DbContext` pooling?
304. 🟡 What is the cost of `DbContext` creation?
305. 🟡 How do indexes affect EF Core performance? How do you identify missing indexes?
306. 🟡 Why is `Count()` on a large table slow? Alternatives?
307. 🔴 What is parameter sniffing and how can it affect EF Core queries?
308. 🔴 How do you handle queries that return millions of rows (streaming, `AsAsyncEnumerable`, batching)?
309. 🔴 What is the cost of `Include` with multiple collections? Single vs split queries?
310. 🔴 How does EF Core handle `IN` clauses with large lists? What changed with `OPENJSON` and parameter translation modes?
311. 🔴 What is connection pooling and how does EF Core use it?
312. 🔴 What is `EnableRetryOnFailure()` and connection resiliency?
313. 🔴 How do you benchmark EF Core queries?
314. 🔴 When would you bypass EF Core for performance-critical paths?

---

## 21. DbContext Lifetime, Pooling & Threading

315. 🟡 Why must you not use the same `DbContext` instance concurrently from multiple threads?
316. 🟡 What does "A second operation was started on this context instance before a previous operation completed" mean?
317. 🟡 How do you run multiple queries in parallel with EF Core?
318. 🟡 How do you use `DbContext` in a `BackgroundService` or singleton?
319. 🟡 How do you use `DbContext` in Blazor Server? Why is `IDbContextFactory` recommended?
320. 🔴 What state is reset when a pooled `DbContext` is returned to the pool?
321. 🔴 Why can't you put per-request state in a pooled `DbContext` constructor? How do you work around it?
322. 🟡 What happens if you register `DbContext` as a singleton?
323. 🟡 What happens if you forget to `await` an async EF Core call?

---

## 22. Logging, Diagnostics & Debugging

324. 🟢 How do you log SQL queries generated by EF Core?
325. 🟡 What is `LogTo()`? What is `EnableSensitiveDataLogging()` and why is it dangerous in production?
326. 🟡 What is `EnableDetailedErrors()`?
327. 🟡 How do you use `ToQueryString()` for debugging?
328. 🟡 How do you view the EF Core model (`Model.ToDebugString()`)?
329. 🟡 How do you use SQL Server Profiler / Extended Events / Query Store with EF Core?
330. 🟡 What EF Core event counters / metrics are available?
331. 🟡 How do you configure warnings as errors (`ConfigureWarnings`)?
332. 🟡 What is the "multiple collection include" warning and how do you resolve it?

---

## 23. Database Providers & Special Types

333. 🟡 What providers are officially supported (SQL Server, SQLite, Cosmos DB, In-Memory) and which popular third-party ones exist (Npgsql, Pomelo MySQL, Oracle)?
334. 🟡 How does EF Core with Cosmos DB differ from relational providers?
335. 🟡 What are the limitations of SQLite in EF Core (migrations, ALTER TABLE)?
336. 🟡 What are provider-specific features (SQL Server: memory-optimized tables, temporal tables; PostgreSQL: arrays, JSONB)?
337. 🟡 How do you store and query spatial data (NetTopologySuite)?
338. 🟡 How do you use hierarchyid in SQL Server with EF Core?
339. 🔴 How do you support multiple databases from the same model?
340. 🟡 What is vector search support in EF Core 10 (SQL Server vector type) at a high level?

---

## 24. Testing with EF Core

341. 🟢 How do you unit test code that uses EF Core?
342. 🟡 What is the In-Memory provider? Why is it not recommended for testing?
343. 🟡 What are the differences between In-Memory provider and SQLite in-memory mode?
344. 🟡 Why is testing against a real database (Testcontainers) recommended?
345. 🟡 How do you mock `DbContext` and `DbSet`? Why is it hard?
346. 🟡 How does the Repository pattern help (or not help) with testing?
347. 🔴 How do you isolate tests that share a database (transactions rolled back, Respawn)?
348. 🔴 How do you test migrations?
349. 🔴 How do you test concurrency handling?

---

## 25. EF Core vs EF6 vs Dapper vs ADO.NET

350. 🟢 What is the difference between EF Core and ADO.NET?
351. 🟢 What is Dapper? How is it different from EF Core?
352. 🟡 When would you choose Dapper over EF Core?
353. 🟡 Can you use EF Core and Dapper together in the same project? How do you share a transaction?
354. 🟡 What EF6 features are missing or different in EF Core?
355. 🟡 How do you migrate an EF6 application to EF Core?
356. 🔴 What is the performance difference between EF Core (tracking, no-tracking) and Dapper today?

---

## 26. Design Patterns with EF Core

357. 🟡 What is the Repository pattern? Is `DbSet<T>` already a repository?
358. 🟡 What is the Unit of Work pattern? Is `DbContext` already a unit of work?
359. 🟡 Should you use a generic repository on top of EF Core? Pros and cons?
360. 🟡 Why can returning `IQueryable<T>` from a repository be considered a leaky abstraction?
361. 🟡 What is the Specification pattern? How does it work with EF Core?
362. 🟡 How does CQRS work with EF Core (EF Core for writes, Dapper/no-tracking for reads)?
363. 🔴 How do you map DDD aggregates with EF Core (aggregate roots, private collections, value objects)?
364. 🔴 How do you implement domain events with EF Core (dispatch on `SaveChanges`)?
365. 🔴 What is the Outbox pattern and how do you implement it with EF Core?

---

## 27. Financial-Domain EF Core Questions 💰

366. 🟡💰 How do you map `decimal` for money (precision, scale)? What happens if precision is not configured?
367. 🟡💰 What is the risk of storing money as `float`/`double` columns?
368. 🟡💰 How do you map a `Money` value object (amount + currency) in EF Core?
369. 🔴💰 How do you implement a fund transfer with EF Core that is atomic and concurrency-safe?
370. 🔴💰 How do you prevent two concurrent requests from overdrawing an account (row version, conditional update, `UPDLOCK`)?
371. 🔴💰 How would you use `ExecuteUpdate` for an atomic balance decrement with a condition (`WHERE Balance >= amount`)?
372. 🔴💰 How do you implement an immutable ledger table (append-only) with EF Core?
373. 🔴💰 How do you implement an audit trail for every change to financial records?
374. 🔴💰 How do you implement idempotent transaction processing with a unique constraint?
375. 🟡💰 How do you store timestamps for trades (UTC, `DateTimeOffset`, `datetime2` precision)?
376. 🔴💰 How do you handle end-of-day batch processing of millions of records with EF Core?
377. 🔴💰 How would you implement data retention / archival of old transactions?
378. 🔴💰 How do you encrypt sensitive columns (account number, PAN) — Always Encrypted vs value converters?
379. 🔴💰 Which isolation level would you use for financial reports vs transactional operations?

---

## 28. Tricky EF Core Questions

380. 🟡 Why does my query return stale data even though the database was updated?
381. 🟡 Why does `SaveChanges()` update all columns instead of just the changed one?
382. 🟡 Why does `SaveChanges()` not save anything even though I modified the entity?
383. 🟡 Why do I get "The instance of entity type cannot be tracked because another instance with the same key value is already being tracked"?
384. 🟡 Why do I get "A second operation was started on this context instance before a previous operation completed"?
385. 🟡 Why do I get "Cannot access a disposed context instance"?
386. 🟡 Why is my navigation property `null` even though data exists in the database?
387. 🟡 Why does a navigation property get populated even though I didn't use `Include`?
388. 🟡 Why does JSON serialization of my entity throw "A possible object cycle was detected"?
389. 🟡 Why does my LINQ query throw "could not be translated"?
390. 🟡 Why does calling a custom C# method inside `Where()` fail, but works inside the final `Select()`?
391. 🟡 Why does `Where(x => x.Name.ToLower() == input.ToLower())` hurt performance?
392. 🟡 Why does `ToList().Where(...)` give correct results but load the whole table?
393. 🟡 Why does `Count()` and then `ToList()` hit the database twice?
394. 🟡 Why does iterating an `IQueryable` twice run the query twice?
395. 🟡 Why does `Include` get ignored when I project with `Select`?
396. 🟡 Why does `Find()` sometimes not hit the database?
397. 🟡 Why does `Remove()` of a child from a collection delete it in one case and only null the FK in another?
398. 🟡 Why do I get a cascade delete error when deleting a parent?
399. 🟡 Why are my `decimal` values truncated in the database? 💰
400. 🟡 Why does EF Core create a `nvarchar(max)` column for my string?
401. 🟡 Why does a `bool` property with a database default always insert `false`?
402. 🟡 Why does EF Core generate a shadow foreign key column like `CustomerId1`?
403. 🟡 Why does a migration drop and recreate a column instead of renaming it?
404. 🟡 Why does `EnsureCreated()` break migrations later?
405. 🟡 Why does `Update()` on a detached entity also mark all related entities as modified?
406. 🟡 Why does `Attach()` followed by `SaveChanges()` do nothing?
407. 🟡 Why are records missing from query results when they exist in the table (global query filters)?
408. 🟡 Why doesn't `ExecuteDelete` trigger my `SaveChanges` audit logic?
409. 🟡 After `ExecuteUpdate`, why does a tracked entity still show the old value?
410. 🔴 Why does an `async` EF Core query block the thread pool if used with `.Result`?
411. 🔴 Why does `AsNoTracking()` return duplicate object instances for the same row in a join?
412. 🔴 Why does adding one more `Include` make the query 100x slower?
413. 🔴 Why does `AsSplitQuery()` return inconsistent data under concurrent writes?
414. 🔴 Why does `Skip/Take` without `OrderBy` return unpredictable pages?
415. 🔴 Why does `Contains()` with a huge list throw or perform badly?
416. 🔴 Why do queries with different constant values create many cached query plans?
417. 🔴 Why does a pooled `DbContext` keep state from a previous request?
418. 🔴 Why does `DbUpdateConcurrencyException` occur even though no one else updated the row (triggers, row count)?
419. 🔴 Why can lazy loading proxies cause exceptions after the `DbContext` is disposed?
420. 🔴 Why does a `TransactionScope` with async code throw "A TransactionScope must be disposed on the same thread that it was created"?
421. 🔴 Why does `GroupBy` followed by selecting entire groups fail to translate?
422. 🔴 Why does comparing a value-converted property in `Where` not translate?
423. 🔴 Why does `First()` on an ordered query generate `TOP(1)` but `Last()` throws?
424. 🔴 Why does `DateTime.Now` inside a query get evaluated on the server vs client differently?
425. 🔴 Is `DbContext` a unit of work AND a repository? Then why do people wrap it?
426. 🔴 Can two different `DbContext` instances track the same entity? What happens when both save?
427. 🔴 What happens when you call `SaveChanges()` inside a loop for 10,000 records?
428. 🔴 What happens if you never call `Dispose()` on a `DbContext`?
429. 🔴 How many database roundtrips does `context.Orders.Include(o => o.Items).Include(o => o.Payments).ToList()` make with single vs split query?
430. 🔴 What happens if two migrations from different branches have the same timestamp order?

---

## 29. Predict the Behavior (Code Snippets)

> What happens when each snippet runs? How many SQL queries are executed? If it fails, say why.

**431. 🟡 Deferred execution**
```csharp
var query = context.Products.Where(p => p.Price > 100);
var count = query.Count();
var list = query.ToList();
```
How many SQL queries run?

**432. 🟡 Client vs server filtering**
```csharp
var products = context.Products.ToList().Where(p => p.Price > 100).ToList();
```
What SQL is generated? What is the problem?

**433. 🟡 IEnumerable vs IQueryable**
```csharp
IEnumerable<Product> products = context.Products;
var expensive = products.Where(p => p.Price > 100).Take(10).ToList();
```
Is the filter applied in SQL or in memory?

**434. 🟡 Untranslatable method**
```csharp
bool IsPremium(Product p) => p.Price > 1000;
var premium = context.Products.Where(p => IsPremium(p)).ToList();
```

**435. 🟡 Method in final projection**
```csharp
string Format(decimal price) => $"₹{price:N2}";
var list = context.Products.Select(p => new { p.Name, Price = Format(p.Price) }).ToList();
```
Does this work? Why is it different from the previous snippet?

**436. 🟡 Find vs FirstOrDefault**
```csharp
var p1 = context.Products.Find(1);
var p2 = context.Products.Find(1);
var p3 = context.Products.FirstOrDefault(p => p.Id == 1);
```
How many SQL queries run? Are `p1`, `p2`, `p3` the same instance?

**437. 🟡 Tracking and stale data**
```csharp
var p = context.Products.First(x => x.Id == 1);   // Price = 100
// Another process updates Price to 200 in the database
var again = context.Products.First(x => x.Id == 1);
Console.WriteLine(again.Price);
```

**438. 🟡 AsNoTracking modifications**
```csharp
var p = context.Products.AsNoTracking().First(x => x.Id == 1);
p.Price = 500;
context.SaveChanges();
```
Is the price updated in the database?

**439. 🟡 Duplicate tracking**
```csharp
var p = context.Products.First(x => x.Id == 1);
var detached = new Product { Id = 1, Name = "New" };
context.Products.Update(detached);
```

**440. 🟡 Attach and save**
```csharp
var product = new Product { Id = 5, Name = "Pen", Price = 10 };
context.Attach(product);
context.SaveChanges();
```
What SQL runs? What if `product.Price = 20;` is added after `Attach`?

**441. 🟡 Update on disconnected entity**
```csharp
var product = new Product { Id = 5, Name = "Pen" };   // Price not set
context.Update(product);
context.SaveChanges();
```
What happens to the `Price` column in the database?

**442. 🟡 Navigation without Include**
```csharp
var order = context.Orders.First(o => o.Id == 1);
Console.WriteLine(order.Customer?.Name);
```
With no lazy loading configured, what is printed?

**443. 🟡 Relationship fix-up**
```csharp
var customer = context.Customers.First(c => c.Id == 1);
var order = context.Orders.First(o => o.CustomerId == 1);
Console.WriteLine(order.Customer?.Name);
```
What is printed now? Why?

**444. 🔴 N+1 with lazy loading**
```csharp
var orders = context.Orders.ToList();     // 100 orders, lazy loading enabled
foreach (var o in orders)
    Console.WriteLine(o.Customer.Name);
```
How many SQL queries run?

**445. 🟡 Include with projection**
```csharp
var data = context.Orders
    .Include(o => o.Items)
    .Select(o => new { o.Id, o.Total })
    .ToList();
```
Are `Items` loaded? Is `Include` used?

**446. 🔴 Cartesian explosion**
```csharp
var blogs = context.Blogs
    .Include(b => b.Posts)
    .Include(b => b.Contributors)
    .ToList();
```
One blog has 100 posts and 50 contributors. How many rows does a single query return? What does `AsSplitQuery()` change?

**447. 🟡 Count with Any**
```csharp
if (context.Orders.Count(o => o.Status == "Pending") > 0) { }
if (context.Orders.Any(o => o.Status == "Pending")) { }
```
What is the SQL difference?

**448. 🟡 Pagination without OrderBy**
```csharp
var page2 = context.Products.Skip(10).Take(10).ToList();
```

**449. 🔴 Concurrent use of one context**
```csharp
var t1 = context.Products.ToListAsync();
var t2 = context.Orders.ToListAsync();
await Task.WhenAll(t1, t2);
```

**450. 🔴 Disposed context**
```csharp
IQueryable<Product> GetProducts()
{
    using var ctx = new AppDbContext();
    return ctx.Products.Where(p => p.IsActive);
}
var list = GetProducts().ToList();
```

**451. 🔴 SaveChanges in a loop**
```csharp
foreach (var item in items)     // 10,000 items
{
    context.Products.Add(item);
    context.SaveChanges();
}
```
How many roundtrips and transactions? How do you fix it?

**452. 🔴 ExecuteUpdate and the change tracker**
```csharp
var p = context.Products.First(x => x.Id == 1);   // Price = 100
await context.Products.Where(x => x.Id == 1).ExecuteUpdateAsync(s => s.SetProperty(x => x.Price, 200));
Console.WriteLine(p.Price);
context.SaveChanges();
```
What is printed? Does `SaveChanges()` overwrite the price back to 100?

**453. 🔴 ExecuteDelete with soft delete**
```csharp
// SaveChanges is overridden to convert deletes into IsDeleted = true
await context.Customers.Where(c => c.Id == 7).ExecuteDeleteAsync();
```
Is the row soft-deleted or physically deleted?

**454. 🔴 Global query filter**
```csharp
modelBuilder.Entity<Customer>().HasQueryFilter(c => !c.IsDeleted);
var all = context.Customers.Count();
var withDeleted = context.Customers.IgnoreQueryFilters().Count();
```
What is the SQL for each?

**455. 🔴 Concurrency token**
```csharp
// Account has [Timestamp] public byte[] RowVersion
var a1 = ctx1.Accounts.First(a => a.Id == 1);
var a2 = ctx2.Accounts.First(a => a.Id == 1);
a1.Balance -= 100; ctx1.SaveChanges();
a2.Balance -= 200; ctx2.SaveChanges();
```
What happens on the second `SaveChanges()`? 💰

**456. 🟡 Remove from collection**
```csharp
var order = context.Orders.Include(o => o.Items).First(o => o.Id == 1);
order.Items.Remove(order.Items.First());
context.SaveChanges();
```
Is the item deleted or is its foreign key set to null? What decides it?

**457. 🟡 Cascade delete**
```csharp
var customer = context.Customers.First(c => c.Id == 1);   // has orders, Restrict delete behavior
context.Customers.Remove(customer);
context.SaveChanges();
```

**458. 🔴 SQL injection**
```csharp
var name = Request.Query["name"];
var r1 = context.Products.FromSqlRaw($"SELECT * FROM Products WHERE Name = '{name}'").ToList();
var r2 = context.Products.FromSql($"SELECT * FROM Products WHERE Name = {name}").ToList();
```
Which one is vulnerable? Why?

**459. 🟡 Decimal precision**
```csharp
public class Payment { public int Id { get; set; } public decimal Amount { get; set; } }
// No precision configured; SQL Server provider
context.Payments.Add(new Payment { Amount = 1234.56789m });
context.SaveChanges();
```
What is stored? What warning does EF Core give? 💰

**460. 🔴 Contains with a local list**
```csharp
var ids = new List<int> { 1, 2, 3 };
var products = context.Products.Where(p => ids.Contains(p.Id)).ToList();
```
What SQL is generated in older EF Core vs EF Core 8+?

**461. 🔴 Execution strategy with manual transaction**
```csharp
// options.UseSqlServer(cs, o => o.EnableRetryOnFailure());
using var tx = context.Database.BeginTransaction();
context.Accounts.Add(a);
context.SaveChanges();
tx.Commit();
```
What happens? How do you fix it?

**462. 🟡 AsNoTracking with identity resolution**
```csharp
var orders = context.Orders.AsNoTracking().Include(o => o.Customer).ToList();
// Two orders belong to the same customer
Console.WriteLine(ReferenceEquals(orders[0].Customer, orders[1].Customer));
```
What is printed? What changes with `AsNoTrackingWithIdentityResolution()`?

**463. 🟡 Default value trap**
```csharp
modelBuilder.Entity<User>().Property(u => u.IsActive).HasDefaultValue(true);
context.Users.Add(new User { Name = "A", IsActive = false });
context.SaveChanges();
```
What value ends up in the database?

**464. 🔴 GroupBy translation**
```csharp
var groups = context.Orders.GroupBy(o => o.CustomerId).ToList();
var totals = context.Orders.GroupBy(o => o.CustomerId)
    .Select(g => new { g.Key, Total = g.Sum(o => o.Amount) }).ToList();
```
Which query is translated efficiently to SQL?

---

## 30. Coding & Hands-On Tasks

465. 🟢 Create a `DbContext` with `Customer` and `Order` entities and a one-to-many relationship using Fluent API.
466. 🟢 Write CRUD operations for `Product` using async EF Core methods.
467. 🟡 Configure a many-to-many relationship between `Student` and `Course` with a payload column (`EnrolledOn`).
468. 🟡 Write a query to get the top 5 customers by total order amount.
469. 🟡 Write a query to get customers who have never placed an order.
470. 🟡 Write a query to find the second highest salary per department.
471. 🟡 Write a query that returns paginated, filtered and sorted products with total count.
472. 🟡 Implement keyset pagination for an `Orders` table.
473. 🟡 Implement soft delete using a global query filter and override `SaveChanges`.
474. 🟡 Implement automatic `CreatedAt`/`UpdatedAt` auditing using a `SaveChangesInterceptor`.
475. 🟡 Configure a value converter to store an enum as a string.
476. 🟡 Map an `Address` value object using owned types or complex types.
477. 🟡 Map a JSON column and query a property inside it.
478. 🟡 Seed initial data using `HasData` and `UseSeeding`.
479. 🟡 Write a migration that renames a column without data loss.
480. 🟡 Call a stored procedure that returns a result set and one with an output parameter.
481. 🟡 Use `ExecuteUpdate` to increase prices of all products in a category by 10%.
482. 🟡 Use `ExecuteDelete` to delete records older than 1 year in batches.
483. 🔴 Implement optimistic concurrency with a row version and handle `DbUpdateConcurrencyException` with a retry/merge strategy.
484. 🔴 Implement a fund transfer between two accounts using a transaction and concurrency checks. 💰
485. 🔴 Implement an atomic conditional balance debit using `ExecuteUpdate` (`WHERE Balance >= @amount`). 💰
486. 🔴 Implement an audit trail table that stores entity name, key, old values, new values, user and timestamp. 💰
487. 🔴 Implement multi-tenancy with a tenant ID query filter resolved per request.
488. 🔴 Implement the Outbox pattern with EF Core.
489. 🔴 Implement a generic repository and a Specification pattern on top of EF Core.
490. 🔴 Write integration tests for a repository using Testcontainers (SQL Server/PostgreSQL).
491. 🔴 Import 1 million rows from a CSV efficiently into the database.
492. 🔴 Implement temporal table support and query the state of a record at a past point in time.

---

## 31. Scenario-Based & Debugging Questions

493. 🟡 An API endpoint that lists orders is very slow. How do you investigate the EF Core part?
494. 🟡 You see hundreds of identical SQL queries per request in the logs. What is the likely cause and fix?
495. 🟡 Memory usage grows when processing a large batch with one `DbContext`. Why, and how do you fix it?
496. 🟡 After deployment, the app fails because the database schema doesn't match the model. How do you prevent this?
497. 🟡 Two developers' migrations conflict after merging. How do you resolve it?
498. 🟡 Users report that their edits are sometimes silently overwritten. How do you fix it?
499. 🟡 A query works in development (SQLite/In-Memory) but fails in production (SQL Server). Why?
500. 🟡 A report query times out in production. What do you check (indexes, query plan, command timeout)?
501. 🔴 A nightly job processing millions of records takes 6 hours with EF Core. How would you make it faster?
502. 🔴 You get deadlocks in the database during high load. How do you investigate and reduce them?
503. 🔴 Duplicate rows appear in a table when the client retries requests. How do you fix it at the database and EF Core level? 💰
504. 🔴 Account balances become negative under concurrent withdrawals. How do you fix it? 💰
505. 🔴 You need to add a NOT NULL column to a table with 500 million rows with zero downtime. How do you do it?
506. 🔴 You need to split one large table into two without downtime. How would you plan the migrations?
507. 🔴 The team wants to replace EF Core with Dapper "for performance". How do you evaluate this decision?
508. 🔴 How would you review a pull request that contains EF Core code? What would you look for?

---

## 32. Rapid-Fire Round

509. 🟢 What is the default lifetime of `DbContext` in ASP.NET Core?
510. 🟢 Is `DbContext` thread-safe?
511. 🟢 What method saves changes to the database?
512. 🟢 What method disables tracking for a query?
513. 🟢 What method loads related data eagerly?
514. 🟢 What command creates a migration?
515. 🟢 What command applies migrations?
516. 🟢 What is the name of the table that stores applied migrations?
517. 🟢 What is the default primary key convention?
518. 🟢 What is the default inheritance mapping strategy?
519. 🟢 What attribute excludes a property from mapping?
520. 🟢 What attribute marks a row version column?
521. 🟡 Does `SaveChanges()` use a transaction by default?
522. 🟡 Does `Find()` always hit the database?
523. 🟡 Does `AsNoTracking()` return entities that can be updated with `SaveChanges()`?
524. 🟡 Does `ExecuteUpdate` require `SaveChanges()`?
525. 🟡 Does `ExecuteDelete` respect global query filters?
526. 🟡 Is lazy loading enabled by default in EF Core?
527. 🟡 Can EF Core map private fields?
528. 🟡 Can EF Core map entities without a primary key?
529. 🟡 Can you use EF Core without migrations?
530. 🟡 Can you use multiple providers in one `DbContext`?
531. 🟡 What is the default cascade behavior for a required relationship?
532. 🟡 What exception is thrown on a concurrency conflict?
533. 🟡 What is the default `MaxBatchSize` for SQL Server?
534. 🟡 What is the default command timeout?
535. 🔴 What does `ChangeTracker.Clear()` do?
536. 🔴 What does `AsSplitQuery()` do?
537. 🔴 What is the difference between `FromSql` and `SqlQuery`?
538. 🔴 What is the difference between owned types and complex types in one line?
539. 🔴 What is `IDesignTimeDbContextFactory` used for in one line?
540. 🔴 What is `EF.Constant()` / `EF.Parameter()` used for?

---

> **Next part (optional):** Microservices, Authentication/Authorization.
