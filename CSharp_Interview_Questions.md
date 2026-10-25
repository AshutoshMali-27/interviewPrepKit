# 🎯 C# Interview Questions — Complete Question Bank (Questions Only)

> **Scope:** Pure C# language — theory, tricky output, and coding questions. (.NET / ASP.NET Core / EF Core will come in the next part.)
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks, trading, payments, fintech), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers C# up to C# 14 (.NET 10).**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. Language Fundamentals & Type System
2. Strings
3. Object-Oriented Programming
4. Classes, Structs, Records & Properties
5. Memory Management & Garbage Collection
6. Generics
7. Delegates, Events & Lambdas
8. Collections
9. LINQ
10. Exception Handling
11. Multithreading & Synchronization
12. Async / Await & Tasks
13. Advanced C# (Equality, Reflection, Attributes, Pattern Matching, Performance)
14. Modern C# Features (C# 6 → C# 14)
15. Financial-Domain C# Questions 💰
16. SOLID & Design Patterns in C#
17. Predict the Output (Code Snippets)
18. Coding Problems — Strings
19. Coding Problems — Arrays & Numbers
20. Coding Problems — Collections, LINQ & Data Structures
21. Coding Problems — OOP & Low-Level Design
22. Coding Problems — Multithreading & Async
23. Coding Problems — Financial Domain 💰
24. Scenario-Based & Debugging Questions
25. Rapid-Fire Round

---

## 1. Language Fundamentals & Type System

1. 🟢 What is C#? What are its main features?
2. 🟢 What is the difference between C# and .NET?
3. 🟢 What happens when you compile a C# program? What is IL/CIL?
4. 🟢 What is the difference between value types and reference types?
5. 🟡 Are value types always stored on the stack? Explain with examples.
6. 🟢 What is the stack and what is the heap? What is stored where?
7. 🟢 What is boxing and unboxing? Why is it considered expensive?
8. 🟡 Can you unbox an `int` that was boxed directly into a `long`? Why or why not?
9. 🟡 List situations where boxing happens implicitly without you noticing.
10. 🟢 What are the built-in data types in C#? What are their sizes?
11. 🟢 What is the difference between `int`, `Int32` and `Int64`?
12. 🟢 What is the difference between implicit and explicit conversion?
13. 🟢 What is the difference between `Convert.ToInt32()`, `int.Parse()` and `int.TryParse()`?
14. 🟢 What is the difference between `is` and `as` operators?
15. 🟢 What is the difference between a direct cast and the `as` operator?
16. 🟢 What is the difference between `const` and `readonly`?
17. 🟡 What is the difference between `readonly` and `static readonly`?
18. 🔴 Why can changing a `public const` in a library cause bugs in consuming assemblies?
19. 🟢 What is the difference between `var`, `dynamic` and `object`?
20. 🟡 When would you actually use `dynamic`?
21. 🟢 What are `ref`, `out` and `in` parameters? How do they differ?
22. 🟡 What is `ref readonly` parameter (C# 12) and how is it different from `in`?
23. 🟡 Why can't you use `ref`/`out` parameters in async methods?
24. 🟢 What is the `params` keyword? What changed for `params` in C# 13?
25. 🟢 What are optional parameters and named arguments?
26. 🟡 What is the hidden problem with default values of optional parameters across assemblies?
27. 🟢 What are nullable value types? How is `int?` implemented?
28. 🟡 What are nullable reference types (NRT)? Do they give runtime protection?
29. 🟢 Explain `?.`, `??`, `??=` and `!` operators.
30. 🟢 What are access modifiers in C#? Explain each one.
31. 🟡 What is the difference between `protected internal` and `private protected`?
32. 🟡 What is the `file` access modifier (C# 11)?
33. 🟢 What are the default access modifiers for classes, members, interfaces and enums?
34. 🟢 What is the `static` keyword? What can be static?
35. 🟢 What is a static class? Can it have a constructor? Can it be inherited?
36. 🟢 What is a static constructor? When is it called? Is it thread-safe?
37. 🟡 What is `beforefieldinit` and how does it affect static initialization?
38. 🟢 What is an `enum`? What is the default underlying type?
39. 🟡 What is a `[Flags]` enum? How do you check if a flag is set?
40. 🟡 Can you assign an undefined integer value to an enum variable? How do you validate it?
41. 🟢 What is the difference between `==`, `Equals()` and `ReferenceEquals()`?
42. 🟡 Is `==` resolved at compile time or runtime? Why does it matter?
43. 🟢 What is the difference between `Array`, `ArrayList` and `List<T>`?
44. 🟢 What are jagged arrays vs multi-dimensional arrays?
45. 🟢 What is the difference between shallow copy and deep copy? How do you implement each?
46. 🟡 What does `MemberwiseClone()` do?
47. 🟢 What are partial classes and partial methods? Where are they used?
48. 🟢 What is the difference between `System.Tuple` and `ValueTuple`?
49. 🟢 What is deconstruction? How do you make your own class deconstructable?
50. 🟢 What are indexers? How are they different from properties?
51. 🟡 What are `checked` and `unchecked` contexts?
52. 🟢 What is the difference between `break`, `continue`, `return` and `goto`?
53. 🟢 Does C# allow fall-through in `switch` statements?
54. 🟢 What is the difference between `for`, `foreach`, `while` and `do-while`?
55. 🟡 How does `foreach` work internally? Does a type need to implement `IEnumerable` to be used in `foreach`?
56. 🟢 What is the difference between `&` and `&&`, `|` and `||`?
57. 🟢 What is the conditional (ternary) operator? What type does it return when branches differ?
58. 🟢 What are namespaces? What is the difference between a namespace and an assembly?
59. 🟢 What are `using` directives, `using static`, global usings and type aliases?
60. 🟢 What are top-level statements? What does the compiler generate for them?
61. 🟢 What is the `Main` method? Can it be async? Can there be more than one?
62. 🟡 What is the `default` keyword / `default` literal?
63. 🟡 What are discards (`_`) and where can you use them?
64. 🟢 What are comments and XML documentation comments in C#?
65. 🟡 What are preprocessor directives (`#if`, `#region`, `#nullable`, `#pragma`)?

---

## 2. Strings

66. 🟢 Why are strings immutable in C#? What are the benefits?
67. 🟢 What is the difference between `string` and `String`?
68. 🟢 What is the difference between `string` and `StringBuilder`? When should you use each?
69. 🟡 How does `StringBuilder` work internally?
70. 🟡 Does `a + b + c` with strings create multiple intermediate strings?
71. 🟡 What is string interning? When are strings interned automatically?
72. 🟢 What is the difference between `string.Empty`, `""` and `null`?
73. 🟢 What is the difference between `IsNullOrEmpty` and `IsNullOrWhiteSpace`?
74. 🟢 What is string interpolation? How is it compiled?
75. 🟡 What are interpolated string handlers (C# 10)?
76. 🟡 What are verbatim strings (`@""`) and raw string literals (`"""`)?
77. 🟡 What is the difference between `string.Compare`, `CompareTo`, `Equals` and `==` for strings?
78. 🟡 What is `StringComparison.Ordinal` vs `OrdinalIgnoreCase` vs `CurrentCulture` vs `InvariantCulture`?
79. 🔴 What is the "Turkish I" problem and why does culture matter in string comparison?
80. 🟡 Why should you not lock on a string?
81. 🟡 What are UTF-8 string literals (`"abc"u8`)?
82. 🟡 How do you avoid allocations when slicing strings?

---

## 3. Object-Oriented Programming

83. 🟢 What are the four pillars of OOP? Explain each with a C# example.
84. 🟢 What is encapsulation? How is it achieved in C#?
85. 🟢 What is abstraction? How is it different from encapsulation?
86. 🟢 What is inheritance? What types of inheritance does C# support?
87. 🟢 Why doesn't C# support multiple class inheritance? What is the diamond problem?
88. 🟢 What is polymorphism? Compile-time vs runtime polymorphism?
89. 🟢 What is the difference between method overloading and method overriding?
90. 🟢 Can you overload a method by changing only its return type?
91. 🟢 What is the difference between an abstract class and an interface?
92. 🟡 After default interface methods (C# 8), why do we still need abstract classes?
93. 🟢 Can an abstract class have a constructor? Can you instantiate it?
94. 🟢 Can an abstract class have non-abstract methods? Can it have fields?
95. 🟢 Can an interface have fields, constructors or static members?
96. 🟡 What are default interface methods? What problem do they solve?
97. 🟡 What happens when two interfaces have the same default method and a class implements both?
98. 🟡 What are static abstract members in interfaces?
99. 🟢 What is the difference between `virtual`, `override`, `abstract` and `new` keywords?
100. 🟡 What is method hiding? How is it different from overriding?
101. 🟢 What is a `sealed` class? What is a `sealed` method? Why use them?
102. 🟡 What performance benefit does sealing a class give?
103. 🟢 What types of constructors exist in C#?
104. 🟢 What is constructor chaining? Explain `this()` and `base()`.
105. 🟡 What is the order of execution of static constructors, field initializers and constructors in an inheritance hierarchy?
106. 🔴 Why is calling a virtual method from a constructor dangerous?
107. 🟢 What is a private constructor? Where is it used?
108. 🟢 What is a destructor/finalizer in C#?
109. 🟡 What is explicit interface implementation? Why is it used?
110. 🟢 What is the difference between `this` and `base`?
111. 🟡 What are extension methods? What are their limitations?
112. 🟡 Can an extension method be called on a null object?
113. 🟡 What are extension members / extension blocks in C# 14?
114. 🟡 What is operator overloading? Which operators can't be overloaded?
115. 🟡 What are implicit and explicit user-defined conversion operators?
116. 🟢 What is composition vs aggregation vs association?
117. 🟡 Composition vs inheritance — which would you prefer and why?
118. 🟡 What are covariant return types (C# 9)?
119. 🟢 What is the `object` class? Which methods does every class inherit from it?
120. 🟡 Can a struct inherit from a class? Can it implement an interface?
121. 🟢 What are nested classes? When would you use them?
122. 🟡 What is an anonymous type? What are its limitations?

---

## 4. Classes, Structs, Records & Properties

123. 🟢 What is the difference between a class and a struct?
124. 🟡 When should you choose a struct over a class?
125. 🟡 Why should structs ideally be immutable?
126. 🟡 What is a `readonly struct`? What is a `readonly` member of a struct?
127. 🔴 What is a defensive copy? When does the compiler create one?
128. 🟡 Can a struct have a parameterless constructor?
129. 🟢 What is a record? What does the compiler generate for a record?
130. 🟡 What is the difference between `record class` and `record struct`?
131. 🟡 What is the difference between `record struct` and `readonly record struct`?
132. 🟡 What is a `with` expression? Is it a deep or shallow copy?
133. 🟡 Can records be inherited? How does equality work with inherited records?
134. 🟡 How do you customize the `ToString()` output of a record?
135. 🟢 What is the difference between a field and a property?
136. 🟢 What are auto-implemented properties?
137. 🟢 What is the `init` accessor?
138. 🟢 What is the `required` modifier (C# 11)?
139. 🟡 What is the `field` keyword in C# 14?
140. 🟡 What are primary constructors (C# 12)? How are they different for records vs classes?
141. 🟡 Are primary constructor parameters properties? Are they mutable?
142. 🟢 What are object initializers and collection initializers?
143. 🟡 What is an `init`-only property vs a `readonly` field vs a get-only property?
144. 🟡 What are partial properties (C# 13)?

---

## 5. Memory Management & Garbage Collection

145. 🟢 What is garbage collection? How does it work in C#?
146. 🟢 What are GC roots?
147. 🟡 What are Gen 0, Gen 1 and Gen 2? Why is GC generational?
148. 🟡 What is the Large Object Heap? What size threshold puts an object there?
149. 🔴 What is the Pinned Object Heap?
150. 🟡 What is the difference between workstation GC and server GC?
151. 🟡 What is background/concurrent GC?
152. 🟢 What is `IDisposable`? Why do we need it if GC exists?
153. 🟢 What does the `using` statement compile into?
154. 🟢 What is a `using` declaration (C# 8)?
155. 🟡 What is `IAsyncDisposable` and `await using`?
156. 🔴 Explain the full Dispose pattern. Why `Dispose(bool disposing)`?
157. 🟡 What does `GC.SuppressFinalize` do?
158. 🟡 What is the difference between `Dispose()`, `Finalize()` and `Close()`?
159. 🔴 Why are finalizers expensive? When do you actually need one?
160. 🔴 What is `SafeHandle` and why is it preferred over finalizers?
161. 🟡 Can memory leaks happen in C#? Give at least five examples.
162. 🟡 How can events cause memory leaks? How do you prevent it?
163. 🟡 What is a `WeakReference`? Where is it used?
164. 🟡 Should you call `GC.Collect()`? When is it acceptable?
165. 🔴 What are `Span<T>` and `ReadOnlySpan<T>`? Why were they introduced?
166. 🔴 What is the difference between `Span<T>` and `Memory<T>`?
167. 🔴 What is a `ref struct`? What restrictions apply and why?
168. 🔴 What is `stackalloc`? What are its risks?
169. 🔴 What is `ArrayPool<T>`? What are common mistakes when using it?
170. 🔴 What is object pooling? When does it help?
171. 🟡 What is pinning? What does the `fixed` keyword do?
172. 🔴 How would you diagnose high memory usage in a C# application? Which tools?
173. 🔴 What is `GCSettings.LatencyMode`? What is a no-GC region?

---

## 6. Generics

174. 🟢 What are generics? What are their advantages?
175. 🟢 How do generics avoid boxing?
176. 🟡 What generic constraints are available in C#? List all of them.
177. 🟡 What is the difference between `where T : class` and `where T : notnull`?
178. 🟡 What is the `unmanaged` constraint?
179. 🟡 What is the `new()` constraint?
180. 🟡 Can you have a generic method inside a non-generic class?
181. 🟡 Do static fields in a generic class get shared across `MyClass<int>` and `MyClass<string>`?
182. 🔴 How does the CLR implement generics for reference types vs value types?
183. 🔴 What are covariance and contravariance? Explain `in` and `out` keywords.
184. 🔴 Why is `List<string>` not assignable to `List<object>` but `IEnumerable<string>` is assignable to `IEnumerable<object>`?
185. 🔴 What is array covariance and why is it considered unsafe?
186. 🔴 What is generic math (`INumber<T>`) in C# 11?
187. 🟡 What is `default(T)` and when is it useful?
188. 🟡 Can you overload methods based only on generic constraints?
189. 🔴 What is the `allows ref struct` anti-constraint (C# 13)?

---

## 7. Delegates, Events & Lambdas

190. 🟢 What is a delegate? Why is it called type-safe?
191. 🟢 What are `Func`, `Action` and `Predicate`?
192. 🟡 What is a multicast delegate? What does it return if multiple methods return values?
193. 🟡 What happens if one method in a multicast delegate throws an exception?
194. 🟢 What is an event? What is the difference between a delegate and an event?
195. 🟡 What is the standard event pattern (`EventHandler<TEventArgs>`)?
196. 🟡 How do you raise an event in a thread-safe way?
197. 🟡 What are custom event accessors (`add`/`remove`)?
198. 🟢 What are anonymous methods and lambda expressions?
199. 🟡 What is a closure? How does the compiler implement captured variables?
200. 🟡 What is the problem with capturing loop variables in lambdas? Is `for` different from `foreach`?
201. 🟡 What are static lambdas (C# 9)? Why use them?
202. 🟡 What are local functions? Local function vs lambda — differences?
203. 🔴 What are expression trees? Where are they used?
204. 🔴 What is the difference between `Func<T, bool>` and `Expression<Func<T, bool>>`?
205. 🟡 What is a natural type of a lambda (C# 10)?
206. 🟡 Can lambdas have default parameter values (C# 12)?
207. 🔴 What are function pointers (`delegate*`) in C# 9?
208. 🟡 What is the Observer pattern and how do events implement it?

---

## 8. Collections

209. 🟢 What collections are available in C#? When would you use each?
210. 🟢 What is the difference between `List<T>` and `LinkedList<T>`?
211. 🟡 How does `List<T>` grow internally? What is its time complexity for add/insert/remove?
212. 🟢 What is the difference between `Dictionary` and `Hashtable`?
213. 🟡 How does `Dictionary<TKey,TValue>` work internally? How are collisions handled?
214. 🟡 What happens if you mutate an object after using it as a dictionary key?
215. 🟡 What is the difference between `Dictionary`, `SortedDictionary` and `SortedList`?
216. 🟢 What is a `HashSet<T>`? How is it different from `List<T>`?
217. 🟢 What is the difference between `Queue<T>` and `Stack<T>`?
218. 🟡 What is `PriorityQueue<TElement, TPriority>`? Is it a min-heap or max-heap?
219. 🟢 What is the difference between `IEnumerable`, `ICollection`, `IList` and `IReadOnlyList`?
220. 🟡 Why should methods return `IReadOnlyList<T>` or `IEnumerable<T>` instead of `List<T>`?
221. 🟡 What is the difference between read-only collections and immutable collections?
222. 🟡 What are `ImmutableList`, `ImmutableDictionary` and `ImmutableArray`?
223. 🟡 What are `FrozenDictionary` and `FrozenSet` (.NET 8)? When should you use them?
224. 🟢 What happens if you modify a collection while iterating over it with `foreach`?
225. 🟢 What is the difference between `IEnumerable` and `IEnumerator`?
226. 🟢 What does `yield return` do? What does `yield break` do?
227. 🔴 What does the compiler generate for an iterator method?
228. 🟡 What sorting algorithm does `Array.Sort` / `List.Sort` use? Is it stable?
229. 🟡 What is the difference between `IComparable<T>` and `IComparer<T>`?
230. 🟡 What is `IEqualityComparer<T>`? Give a use case.
231. 🟡 Which collections are thread-safe? List the concurrent collections.
232. 🔴 How does `ConcurrentDictionary` achieve thread safety?
233. 🔴 Can the value factory in `ConcurrentDictionary.GetOrAdd` run more than once? How do you avoid side effects?
234. 🟡 What is `BlockingCollection<T>`?
235. 🟡 What is `ConcurrentBag<T>` and when is it suitable?
236. 🔴 What is `CollectionsMarshal` and why would you use it?
237. 🟡 What are collection expressions (C# 12) and the spread operator?

---

## 9. LINQ

238. 🟢 What is LINQ? What are its advantages?
239. 🟢 What is the difference between query syntax and method syntax?
240. 🟢 What is deferred execution? Which operators are deferred and which are immediate?
241. 🟡 What is the problem of multiple enumeration? How do you avoid it?
242. 🟢 What is the difference between `IEnumerable` and `IQueryable`?
243. 🟢 What is the difference between `First`, `FirstOrDefault`, `Single` and `SingleOrDefault`?
244. 🟢 What is the difference between `Select` and `SelectMany`?
245. 🟢 What is the difference between `Where` and `TakeWhile`/`SkipWhile`?
246. 🟢 Why is `Any()` preferred over `Count() > 0`?
247. 🟡 What is the difference between `GroupBy` and `ToLookup`?
248. 🟡 What is the difference between `OrderBy().OrderBy()` and `OrderBy().ThenBy()`?
249. 🟡 How do you perform inner join, left join and group join in LINQ?
250. 🟡 What is the difference between `Distinct` and `DistinctBy`?
251. 🟡 What are `MinBy`, `MaxBy`, `Chunk`, `CountBy`, `AggregateBy`, `Index` (newer LINQ methods)?
252. 🟡 What is `Aggregate` and when would you use it?
253. 🟡 What is `Zip`?
254. 🟡 What are `Cast<T>()` and `OfType<T>()`? How do they differ?
255. 🟡 What does `AsEnumerable()` do on an `IQueryable`?
256. 🔴 How would you write your own LINQ operator like `Where` or `Select`?
257. 🔴 What is PLINQ? When can it hurt performance?
258. 🟡 What are the performance pitfalls of LINQ in hot paths?
259. 🟡 What is `let` in query syntax?
260. 🟡 Does `OrderBy` sort stably?

---

## 10. Exception Handling

261. 🟢 What is an exception? How does try/catch/finally work?
262. 🟢 Can you have a `try` without a `catch`? A `try` without a `finally`?
263. 🟢 When does a `finally` block not execute?
264. 🟢 What is the difference between `throw` and `throw ex`?
265. 🟡 How do you rethrow an exception later while preserving its stack trace?
266. 🟢 Why does the order of catch blocks matter?
267. 🟡 What are exception filters (`when`)? What advantage do they have over catching and rethrowing?
268. 🟢 How do you create a custom exception? What are the best practices?
269. 🟢 What is an inner exception?
270. 🟡 What is `AggregateException`? When is it thrown?
271. 🟡 Which exceptions cannot be caught?
272. 🟡 What is the difference between `ArgumentException`, `ArgumentNullException`, `InvalidOperationException` and `NotSupportedException`?
273. 🟡 What is `ArgumentNullException.ThrowIfNull` and the guard-clause helpers?
274. 🟡 What is the cost of throwing exceptions? Should exceptions be used for flow control?
275. 🟡 What is the `Try` pattern (`TryParse`, `TryGetValue`)?
276. 🟡 Is `finally` executed if there is a `return` inside `try`? Can you `return` from `finally`?
277. 🟡 How are exceptions handled in async methods?
278. 🔴 What happens to an exception thrown in a fire-and-forget task?
279. 🔴 What are global exception handlers (`AppDomain.UnhandledException`, `TaskScheduler.UnobservedTaskException`)?
280. 🟡 What is the difference between checked exceptions (Java) and C# exceptions?

---
## 11. Multithreading & Synchronization

281. 🟢 What is the difference between a process and a thread?
282. 🟢 What is multithreading? What are its advantages and risks?
283. 🟢 How do you create a thread in C#?
284. 🟢 What is the difference between foreground and background threads?
285. 🟢 What is the ThreadPool? Why use it instead of creating threads?
286. 🟡 What is thread pool starvation? What causes it?
287. 🟢 What is a race condition? Give an example.
288. 🟢 What is a deadlock? What are the four conditions for a deadlock?
289. 🟡 How do you prevent deadlocks?
290. 🟡 What is a livelock? What is starvation?
291. 🟢 How does the `lock` statement work internally?
292. 🟡 What object should you lock on? Why not `this`, `typeof(X)` or a string?
293. 🟡 What is the new `System.Threading.Lock` type (C# 13 / .NET 9)?
294. 🟡 Why can't you use `await` inside a `lock` block? What is the alternative?
295. 🟡 What is the difference between `Monitor`, `Mutex`, `Semaphore` and `SemaphoreSlim`?
296. 🟡 What is `ReaderWriterLockSlim`? When is it useful?
297. 🟡 What is `SpinLock` / `SpinWait`?
298. 🟡 What are `AutoResetEvent`, `ManualResetEvent(Slim)`, `CountdownEvent` and `Barrier`?
299. 🟡 What is `Monitor.Wait` and `Monitor.Pulse`?
300. 🟡 What is the `Interlocked` class? Which operations does it provide?
301. 🔴 What is compare-and-swap (CAS)? How would you implement a lock-free counter?
302. 🔴 What does the `volatile` keyword do? Does it make `count++` thread-safe?
303. 🔴 What are memory barriers? What is instruction reordering?
304. 🟡 What is a reentrant lock? Is `lock` reentrant?
305. 🟡 What is `ThreadLocal<T>` vs `[ThreadStatic]` vs `AsyncLocal<T>`?
306. 🟡 What is the difference between `Thread.Sleep`, `Task.Delay`, `Thread.Yield` and `Thread.SpinWait`?
307. 🟡 Why is `Thread.Abort` not supported in .NET Core? How do you stop a thread?
308. 🟡 What is `Parallel.For` / `Parallel.ForEach`? How is it different from `Task.WhenAll`?
309. 🟡 What is `Parallel.ForEachAsync`?
310. 🟡 What is `MaxDegreeOfParallelism`?
311. 🔴 What is false sharing?
312. 🟡 Is `Dictionary<TKey,TValue>` safe for concurrent reads? For reads and writes?
313. 🟡 What is a thread-safe class? How do you make a class thread-safe?
314. 🟡 What is immutability's role in concurrency?
315. 🔴 What is the producer-consumer problem? How do you solve it in C#?
316. 🔴 What are `System.Threading.Channels`? Bounded vs unbounded channels?
317. 🔴 What is back-pressure?

---

## 12. Async / Await & Tasks

318. 🟢 What is asynchronous programming? Why is it needed?
319. 🟢 What is the difference between synchronous, asynchronous and parallel programming?
320. 🟢 What is a `Task`? Is a Task the same as a thread?
321. 🟢 What is the difference between `Task` and `Thread`?
322. 🟢 How do `async` and `await` work?
323. 🔴 What does the compiler generate for an async method (state machine)?
324. 🟡 Does marking a method `async` make it run on a background thread?
325. 🟡 What is the difference between CPU-bound and I/O-bound work? Which APIs should you use for each?
326. 🟢 What is the difference between `Task` and `Task<T>`?
327. 🟡 Why should you avoid `async void`? When is it acceptable?
328. 🟡 What is `ConfigureAwait(false)`? When should you use it?
329. 🔴 Explain the classic async deadlock with `.Result` / `.Wait()`. Does it happen in ASP.NET Core?
330. 🟡 What is a `SynchronizationContext`?
331. 🟡 What is the difference between `.Result`, `.Wait()` and `.GetAwaiter().GetResult()`?
332. 🟡 What is the difference between `Task.WhenAll`, `Task.WhenAny`, `Task.WaitAll` and `Task.WhenEach`?
333. 🟡 When `Task.WhenAll` fails, which exception do you get? How do you see all of them?
334. 🟡 What is the difference between `Task.Run`, `Task.Factory.StartNew` and `new Task().Start()`?
335. 🟡 What is `Task.FromResult` and `Task.CompletedTask`?
336. 🔴 What is `ValueTask`? When should you use it and what are its rules?
337. 🟡 How does cancellation work? What are `CancellationTokenSource` and `CancellationToken`?
338. 🟡 How do you implement a timeout for an async operation?
339. 🟡 What are linked cancellation tokens?
340. 🟡 What is `IAsyncEnumerable<T>` and `await foreach`?
341. 🔴 What is `[EnumeratorCancellation]`?
342. 🔴 What is `TaskCompletionSource<T>`? Give a use case.
343. 🔴 Why use `TaskCreationOptions.RunContinuationsAsynchronously`?
344. 🟡 How do you run multiple async calls in parallel but limit concurrency?
345. 🟡 What is "async all the way"? What is sync-over-async and async-over-sync?
346. 🟡 What is `Task.Yield()`?
347. 🔴 What happens to an async method's local variables across `await`?
348. 🔴 What are `ConfigureAwaitOptions` (.NET 8)?
349. 🟡 How do you call an async method from a constructor?
350. 🟡 How do you handle exceptions in fire-and-forget tasks?
351. 🔴 How does `async`/`await` behave inside `lock`, `foreach`, `using` and `finally`?
352. 🟡 What is `Progress<T>` / `IProgress<T>`?
353. 🔴 What is `TimeProvider` (.NET 8) and why does it help in testing async/time-based code?

---

## 13. Advanced C#

354. 🔴 What is the contract between `Equals()` and `GetHashCode()`?
355. 🟡 How do you correctly override `Equals` and `GetHashCode`? What is `HashCode.Combine`?
356. 🟡 Why implement `IEquatable<T>`, especially for structs?
357. 🟡 What happens if `GetHashCode` changes while the object is in a `HashSet`?
358. 🟡 What is reflection? What are its use cases and costs?
359. 🟡 How do you get all properties of a type and read their values using reflection?
360. 🟡 How do you create an instance of a type at runtime?
361. 🔴 What is the `UnsafeAccessor` attribute (.NET 8)?
362. 🟡 What are attributes? How do you create and read a custom attribute?
363. 🟡 What are generic attributes (C# 11)?
364. 🟡 What are caller info attributes (`CallerMemberName`, `CallerArgumentExpression`)?
365. 🔴 What are source generators? Why are they preferred over reflection?
366. 🔴 What are Roslyn analyzers?
367. 🟡 What is pattern matching? List all pattern types in C#.
368. 🟡 What is the difference between a switch statement and a switch expression?
369. 🟡 What are property patterns and extended property patterns?
370. 🟡 What are relational and logical patterns (`and`, `or`, `not`)?
371. 🟡 What are list patterns (C# 11)?
372. 🟡 What is the difference between `x == null` and `x is null`?
373. 🟢 What are `nameof`, `typeof`, `GetType()` and `sizeof`?
374. 🔴 What is `unsafe` code? When would you use pointers in C#?
375. 🔴 What are `ref` returns and `ref` locals?
376. 🟡 What is `Lazy<T>`? Is it thread-safe? What are its thread-safety modes?
377. 🟡 How do you make a type immutable in C#?
378. 🔴 What is double dispatch? How does the Visitor pattern achieve it in C#?
379. 🟡 What is the difference between early binding and late binding?
380. 🟡 What is JIT compilation? What is tiered compilation?
381. 🔴 What is Native AOT? What C# features are restricted with it?
382. 🔴 What is Dynamic PGO?
383. 🟡 What is `InternalsVisibleTo`?
384. 🔴 What is `[MethodImpl(MethodImplOptions.AggressiveInlining)]`?
385. 🔴 What are inline arrays (C# 12)?
386. 🔴 What is `OverloadResolutionPriority` (C# 13)?
387. 🔴 How do you benchmark C# code correctly? What is BenchmarkDotNet?
388. 🟡 What is serialization? What is the difference between `System.Text.Json` and Newtonsoft.Json from a C# perspective?
389. 🟡 What is the difference between `Regex` with and without `[GeneratedRegex]`?
390. 🟡 What is the `IFormattable` / `ISpanFormattable` interface?

---

## 14. Modern C# Features (C# 6 → C# 14)

391. 🟢 What are the major features introduced in C# 6?
392. 🟢 What are the major features introduced in C# 7.x?
393. 🟡 What are the major features introduced in C# 8?
394. 🟡 What are the major features introduced in C# 9?
395. 🟡 What are the major features introduced in C# 10?
396. 🟡 What are the major features introduced in C# 11?
397. 🟡 What are the major features introduced in C# 12?
398. 🟡 What are the major features introduced in C# 13?
399. 🟡 What are the major features introduced in C# 14?
400. 🟢 What are ranges and indices (`^1`, `..`)?
401. 🟢 What is target-typed `new()`?
402. 🟢 What are file-scoped namespaces and global usings?
403. 🟡 What is the null-conditional assignment (`a?.B = value`) in C# 14?
404. 🟡 What are implicit span conversions in C# 14?
405. 🟡 What are user-defined compound assignment operators in C# 14?
406. 🟡 What is `using` alias for any type (C# 12)?
407. 🟡 Which recent C# feature have you used in a real project and why?

---

## 15. Financial-Domain C# Questions 💰

408. 🟢💰 Why should you use `decimal` instead of `double` or `float` for money?
409. 🟢💰 Why does `0.1 + 0.2 == 0.3` return false for `double`?
410. 🟡💰 What are the size, precision and range differences between `float`, `double` and `decimal`?
411. 🟡💰 When would a financial system still use `double`?
412. 🟡💰 What is banker's rounding? What does `Math.Round(2.5)` return?
413. 🟡💰 Explain all `MidpointRounding` modes.
414. 🔴💰 How would you design a `Money` type in C#?
415. 🔴💰 How do you split an amount into N parts without losing a paisa/cent (allocation problem)?
416. 🟡💰 Why do some trading systems store amounts as `long` in minor units?
417. 🟡💰 How do you detect integer overflow in financial calculations?
418. 🟡💰 What is `BigInteger`? What are `Int128`/`UInt128`?
419. 🟡💰 What is the difference between `DateTime`, `DateTimeOffset`, `DateOnly` and `TimeOnly`?
420. 🔴💰 How do you handle time zones and daylight saving in trade timestamps and end-of-day processing?
421. 🟡💰 Why should you store timestamps in UTC?
422. 🟡💰 How do culture settings affect parsing amounts like "1,234.50"? How do you parse safely?
423. 🔴💰 How do you make account balance updates thread-safe?
424. 🔴💰 How would you implement a fund transfer between two accounts without deadlocks?
425. 🔴💰 What is idempotency? How would you implement idempotent payment processing in C#?
426. 🔴💰 What is optimistic vs pessimistic concurrency? How would you implement each in C#?
427. 🟡💰 Why is immutability important in financial systems?
428. 🔴💰 How do you reduce GC pauses in a low-latency trading application?
429. 🟡💰 How would you mask sensitive data (card numbers, account numbers) in logs and `ToString()`?
430. 🟡💰 Is `SecureString` recommended for new code? Why or why not?
431. 🔴💰 How would you design an audit trail using C# types?
432. 🔴💰 How would you implement a rate limiter for an API that places orders?
433. 🔴💰 How would you implement retry with exponential backoff without double-processing a payment?
434. 🔴💰 How would you process millions of transactions from a file efficiently in C#?
435. 🔴💰 How would you calculate interest/EMI precisely when `decimal` has no `Pow` method?

---

## 16. SOLID & Design Patterns in C#

436. 🟢 Explain each SOLID principle with a C# example.
437. 🟡 Give an example of a Single Responsibility Principle violation and fix it.
438. 🟡 How does the Open/Closed Principle apply to a discount or tax calculation module?
439. 🟡 Give a C# example of a Liskov Substitution violation.
440. 🟡 What is Interface Segregation? Give an example of a "fat" interface.
441. 🟡 What is Dependency Inversion vs Dependency Injection vs Inversion of Control?
442. 🟢 What is the Singleton pattern? Write a thread-safe singleton in multiple ways.
443. 🟡 What are the drawbacks of the Singleton pattern?
444. 🟡 Singleton vs static class — differences?
445. 🟡 What is the Factory Method pattern? Abstract Factory?
446. 🟡 What is the Strategy pattern? Implement it for payment fees.
447. 🟡 What is the Decorator pattern? Implement caching or logging around a service.
448. 🟡 What is the Builder pattern?
449. 🟡 What is the Adapter pattern?
450. 🟡 What is the Repository and Unit of Work pattern?
451. 🟡 What is the Template Method pattern?
452. 🟡 What is the Chain of Responsibility pattern?
453. 🟡 What is the Command pattern?
454. 🟡 What is the Observer pattern?
455. 🟡 What is the Prototype pattern? How do records relate to it?
456. 🟡 What is the Facade pattern?
457. 🟡 What is the Proxy pattern?
458. 🔴 What is the State pattern? Implement an order state machine.
459. 🔴 What are anti-patterns you have seen in C# codebases?
460. 🟡 What are DRY, KISS and YAGNI?

---
## 17. Predict the Output (Code Snippets)

> What is the output of each snippet? If it doesn't compile or throws, say why.

**461. 🟡 Closures in a loop**
```csharp
var actions = new List<Action>();
for (int i = 0; i < 3; i++) actions.Add(() => Console.Write(i + " "));
foreach (var a in actions) a();
```

**462. 🟢 String immutability**
```csharp
string s = "hello";
s.ToUpper();
Console.WriteLine(s);
```

**463. 🔴 Virtual call from base constructor**
```csharp
class A
{
    public A() => Print();
    public virtual void Print() => Console.WriteLine("A");
}
class B : A
{
    private int x = 5;
    public B() => x = 10;
    public override void Print() => Console.WriteLine(x);
}
new B();
```

**464. 🟢 `new` vs `override`**
```csharp
class P { public virtual string Who() => "P"; public string Name() => "P"; }
class C : P { public override string Who() => "C"; public new string Name() => "C"; }
P obj = new C();
Console.WriteLine(obj.Who() + obj.Name());
```

**465. 🟡 Boxed equality**
```csharp
object a = 1, b = 1;
Console.WriteLine(a == b);
Console.WriteLine(a.Equals(b));
```

**466. 🟡 String reference equality**
```csharp
string a = "hello";
string b = "hel" + "lo";
string c = new string("hello".ToCharArray());
Console.WriteLine(ReferenceEquals(a, b));
Console.WriteLine(ReferenceEquals(a, c));
Console.WriteLine(a == c);
object x = a, y = c;
Console.WriteLine(x == y);
```

**467. 🟡 Deferred execution**
```csharp
var list = new List<int> { 1, 2, 3 };
var query = list.Where(x => x > 1);
list.Add(4);
Console.WriteLine(query.Count());
```

**468. 🟡 `return` and `finally`**
```csharp
static int F()
{
    int x = 1;
    try { return x; }
    finally { x = 2; }
}
Console.WriteLine(F());
```

**469. 🟢 Integer overflow**
```csharp
int max = int.MaxValue;
Console.WriteLine(max + 1);
Console.WriteLine(checked(max + 1));
```

**470. 🟡💰 Rounding**
```csharp
Console.WriteLine(Math.Round(2.5));
Console.WriteLine(Math.Round(3.5));
Console.WriteLine(Math.Round(-2.5));
Console.WriteLine(Math.Round(2.345m, 2));
Console.WriteLine(Math.Round(2.345m, 2, MidpointRounding.AwayFromZero));
```

**471. 🟢💰 Floating point**
```csharp
Console.WriteLine(0.1 + 0.2 == 0.3);
Console.WriteLine(0.1m + 0.2m == 0.3m);
```

**472. 🟢 Concatenation order**
```csharp
Console.WriteLine(1 + 2 + "3" + 4 + 5);
```

**473. 🟢 Char arithmetic**
```csharp
Console.WriteLine('a' + 'b');
Console.WriteLine("" + 'a' + 'b');
Console.WriteLine('a' + 1);
Console.WriteLine((char)('a' + 1));
```

**474. 🟡 Increment operators**
```csharp
int x = 5;
int y = x++ + ++x;
Console.WriteLine($"{x} {y}");
```

**475. 🟡 Division and modulo**
```csharp
Console.WriteLine(5 / 2);
Console.WriteLine(5 / 2.0);
Console.WriteLine(-5 / 2);
Console.WriteLine(-5 % 2);
Console.WriteLine(5.0 / 0);
Console.WriteLine(5 / 0);
```

**476. 🟡 Nullable comparisons**
```csharp
int? a = null, b = null;
Console.WriteLine(a == b);
Console.WriteLine(a >= b);
Console.WriteLine(a < 5);
Console.WriteLine((a + 1) == null);
```

**477. 🔴 Ternary type**
```csharp
object o = true ? 1 : 2.0;
Console.WriteLine(o.GetType());
Console.WriteLine(o);
```

**478. 🟡 Mutable struct in a List**
```csharp
struct Counter { public int Value; public void Inc() => Value++; }

var list = new List<Counter> { new Counter() };
var c = list[0];
c.Inc();
Console.WriteLine(list[0].Value);

var arr = new Counter[1];
arr[0].Inc();
Console.WriteLine(arr[0].Value);
```

**479. 🔴 Readonly struct field**
```csharp
struct Counter { public int Value; public void Inc() => Value++; }
class Holder
{
    public readonly Counter C;
    public void Bump() { C.Inc(); C.Inc(); Console.WriteLine(C.Value); }
}
new Holder().Bump();
```

**480. 🟡 Lazy iterator**
```csharp
static IEnumerable<int> Get(int n)
{
    if (n < 0) throw new ArgumentException("negative");
    yield return n;
}
var seq = Get(-1);
Console.WriteLine("Created");
foreach (var x in seq) Console.WriteLine(x);
```

**481. 🟡 Async order**
```csharp
static async Task Main()
{
    Console.WriteLine("1");
    var t = DoAsync();
    Console.WriteLine("3");
    await t;
    Console.WriteLine("5");
}
static async Task DoAsync()
{
    Console.WriteLine("2");
    await Task.Delay(100);
    Console.WriteLine("4");
}
```

**482. 🟡 Static initialization cycle**
```csharp
class A { public static int X = B.Y + 1; }
class B { public static int Y = A.X + 1; }
Console.WriteLine(A.X);
Console.WriteLine(B.Y);
```

**483. 🟢 Null strings**
```csharp
string s = null;
Console.WriteLine(s + "x" + null);
Console.WriteLine(s?.Length ?? -1);
Console.WriteLine(s.Length);
```

**484. 🟢 Record equality**
```csharp
record Person(string Name, int Age);
var p1 = new Person("Asha", 30);
var p2 = new Person("Asha", 30);
Console.WriteLine(p1 == p2);
Console.WriteLine(ReferenceEquals(p1, p2));
Console.WriteLine(p1);
```

**485. 🟡 `with` expression and shared references**
```csharp
record Order(string Id, List<string> Items);
var o1 = new Order("1", new List<string> { "A" });
var o2 = o1 with { Id = "2" };
o2.Items.Add("B");
Console.WriteLine(o1.Items.Count);
Console.WriteLine(o1 == o2);
```

**486. 🟡 Array covariance**
```csharp
object[] arr = new string[3];
arr[0] = "ok";
arr[1] = 42;
Console.WriteLine("done");
```

**487. 🟡 Enum defaults**
```csharp
enum Status { Active = 1, Closed = 2 }
Status s = default;
Console.WriteLine(s);
Console.WriteLine((Status)7);
Console.WriteLine(Enum.IsDefined(typeof(Status), 7));
```

**488. 🟡 Overload resolution**
```csharp
static void M(object o) => Console.WriteLine("object");
static void M(string s) => Console.WriteLine("string");
static void M(int? i) => Console.WriteLine("int?");
M(null);
```

**489. 🟡 Unobserved task exception**
```csharp
var t = Task.Run(() => throw new InvalidOperationException("boom"));
Thread.Sleep(500);
Console.WriteLine("Done");
```

**490. 🟢 Switch fall-through**
```csharp
int n = 1;
switch (n)
{
    case 1:
        Console.WriteLine("one");
    case 2:
        Console.WriteLine("two");
        break;
}
```

**491. 🟡 Static fields in generic types**
```csharp
class Counter<T> { public static int Count; }
Counter<int>.Count++;
Counter<int>.Count++;
Counter<string>.Count++;
Console.WriteLine($"{Counter<int>.Count} {Counter<string>.Count}");
```

**492. 🟡 Multicast delegate return value**
```csharp
Func<int> f = () => 1;
f += () => 2;
f += () => 3;
Console.WriteLine(f());
```

**493. 🟡 Exception inside finally**
```csharp
try
{
    try { throw new Exception("first"); }
    finally { throw new Exception("second"); }
}
catch (Exception ex) { Console.WriteLine(ex.Message); }
```

**494. 🟡 Struct vs class assignment**
```csharp
class RefPoint { public int X; }
struct ValPoint { public int X; }
var r1 = new RefPoint { X = 1 }; var r2 = r1; r2.X = 99;
var v1 = new ValPoint { X = 1 }; var v2 = v1; v2.X = 99;
Console.WriteLine($"{r1.X} {v1.X}");
```

**495. 🟡 Passing reference types by value vs by ref**
```csharp
static void Change(List<int> list) { list.Add(1); list = new List<int> { 100 }; }
static void ChangeRef(ref List<int> list) { list = new List<int> { 200 }; }
var data = new List<int>();
Change(data);
Console.WriteLine(string.Join(",", data));
ChangeRef(ref data);
Console.WriteLine(string.Join(",", data));
```

**496. 🟡 Static constructor timing**
```csharp
class Demo
{
    static Demo() => Console.WriteLine("static ctor");
    public Demo() => Console.WriteLine("instance ctor");
    public static void Hello() => Console.WriteLine("hello");
}
Demo.Hello();
new Demo();
new Demo();
```

**497. 🟡 Interface default method call**
```csharp
interface IGreeter { void Greet() => Console.WriteLine("Default hello"); }
class Greeter : IGreeter { }
IGreeter g = new Greeter();
g.Greet();
// new Greeter().Greet();   // what happens if uncommented?
```

**498. 🟡 Modifying a collection during foreach**
```csharp
var nums = new List<int> { 1, 2, 3, 4 };
foreach (var n in nums)
    if (n % 2 == 0) nums.Remove(n);
Console.WriteLine(nums.Count);
```

**499. 🔴 `First` on an empty sequence vs `FirstOrDefault`**
```csharp
var empty = new List<int>();
Console.WriteLine(empty.FirstOrDefault());
Console.WriteLine(empty.FirstOrDefault(-1));
Console.WriteLine(empty.First());
```

**500. 🔴 Lock on value type**
```csharp
int counter = 0;
lock (counter) { counter++; }
```

**501. 🟡 `is` pattern with null**
```csharp
string? s = null;
Console.WriteLine(s is string);
Console.WriteLine(s is null);
object o = 42;
Console.WriteLine(o is int n && n > 40);
```

**502. 🟡 String.Equals vs ==**
```csharp
string a = "Hello", b = "hello";
Console.WriteLine(a == b);
Console.WriteLine(a.Equals(b, StringComparison.OrdinalIgnoreCase));
Console.WriteLine(string.Compare(a, b, StringComparison.Ordinal) < 0);
```

---

## 18. Coding Problems — Strings

503. 🟢 Reverse a string without using built-in `Reverse()`.
504. 🟢 Check whether a string is a palindrome (ignore case and non-alphanumeric characters).
505. 🟢 Check whether two strings are anagrams.
506. 🟢 Count the occurrences of each character in a string.
507. 🟢 Find the first non-repeating character in a string.
508. 🟢 Count vowels and consonants in a string.
509. 🟢 Reverse the order of words in a sentence.
510. 🟢 Reverse each word in a sentence while keeping word order.
511. 🟢 Remove duplicate characters from a string while keeping the first occurrence order.
512. 🟢 Check if a string contains only digits without using `int.TryParse`.
513. 🟡 Implement your own `int.Parse` / `atoi` handling sign, whitespace and overflow.
514. 🟡 Compress a string: `"aaabbc"` → `"a3b2c1"`.
515. 🟡 Find the longest substring without repeating characters.
516. 🟡 Find the longest palindromic substring.
517. 🟡 Group a list of words into anagram groups.
518. 🟡 Check if parentheses/brackets in a string are balanced (`()[]{}`).
519. 🟡 Find all permutations of a string.
520. 🟡 Check whether one string is a rotation of another.
521. 🟡 Capitalize the first letter of every word.
522. 🟡 Find the most frequent word in a paragraph (case-insensitive, ignore punctuation).
523. 🟡 Convert a Roman numeral to an integer and vice versa.
524. 🟡 Check if a string is a valid email/PAN/IFSC format (with and without Regex).
525. 🔴 Implement string search (`IndexOf`) without built-ins (naive and KMP).
526. 🔴 Parse a CSV line of trade data using `ReadOnlySpan<char>` without allocating substrings.

---

## 19. Coding Problems — Arrays & Numbers

527. 🟢 Find the largest and smallest element in an array without LINQ.
528. 🟢 Find the second largest element in an array (single pass).
529. 🟢 Reverse an array in place.
530. 🟢 Find duplicate elements in an array.
531. 🟢 Remove duplicates from an array.
532. 🟢 Find the missing number in an array of 1..N.
533. 🟢 Move all zeros to the end while maintaining order.
534. 🟢 FizzBuzz (also using a switch expression).
535. 🟢 Check if a number is prime; print all primes up to N (Sieve of Eratosthenes).
536. 🟢 Fibonacci series — iterative, recursive, memoized and using `yield return`.
537. 🟢 Factorial — iterative and recursive; handle large values with `BigInteger`.
538. 🟢 Check Armstrong number, perfect number, palindrome number.
539. 🟢 Swap two numbers without a temporary variable (and with tuple swap).
540. 🟢 Sum of digits of a number; reverse a number.
541. 🟡 Two Sum: return indices of two numbers that add to a target.
542. 🟡 Rotate an array by K positions.
543. 🟡 Merge two sorted arrays into one sorted array.
544. 🟡 Find the intersection and union of two arrays.
545. 🟡 Maximum subarray sum (Kadane's algorithm).
546. 🟡 Find the majority element (appears more than n/2 times).
547. 🟡 Find a pair with the given sum in a sorted array (two pointers).
548. 🟡 Binary search — iterative and recursive.
549. 🟡 Implement bubble sort, selection sort, insertion sort.
550. 🟡 Implement quick sort and merge sort.
551. 🟡 Find the Kth largest element (using `PriorityQueue`).
552. 🟡 Rotate a matrix by 90 degrees.
553. 🟡 Print a matrix in spiral order.
554. 🟡 Find the longest consecutive sequence in an unsorted array.
555. 🟡 Product of array except self (without division).
556. 🔴 Find all triplets that sum to zero (3Sum).
557. 🔴 Merge overlapping intervals.
558. 🔴 Sliding window maximum.
559. 🔴 Best time to buy and sell stock (single and multiple transactions). 💰

---

## 20. Coding Problems — Collections, LINQ & Data Structures

560. 🟢 Given a list of employees, find the highest salary using LINQ.
561. 🟡 Find the second (and Nth) highest salary using LINQ.
562. 🟡 Group employees by department and find the count and average salary per department.
563. 🟡 Find the highest-paid employee in each department.
564. 🟡 Find employees whose salary is above their department's average.
565. 🟡 Join employees with departments and print employee name with department name (inner and left join).
566. 🟡 Find duplicate names in a list using LINQ.
567. 🟡 Find the top 3 most frequent words in a text using LINQ.
568. 🟡 Flatten a list of lists using LINQ.
569. 🟡 Split a list into batches of size N (with and without `Chunk`).
570. 🟡 Write your own `Where`, `Select` and `FirstOrDefault` extension methods.
571. 🟡 Write an extension method `IsNullOrEmpty()` for `IEnumerable<T>`.
572. 🟡 Return the top K frequent elements using `Dictionary` and `PriorityQueue`.
573. 🟡 Implement a generic `Stack<T>` using an array (with resizing).
574. 🟡 Implement a generic `Queue<T>` using two stacks.
575. 🟡 Implement a singly linked list with add, remove, reverse and find-middle operations.
576. 🟡 Detect a cycle in a linked list.
577. 🟡 Implement a binary search tree with insert, search and in-order traversal.
578. 🟡 Find the height of a binary tree; check whether it's balanced.
579. 🔴 Implement an LRU cache with O(1) get and put.
580. 🔴 Implement a min-heap from scratch.
581. 🔴 Implement your own `Dictionary<TKey,TValue>` (hash table with chaining and resizing).
582. 🔴 Implement a Trie for autocomplete.
583. 🔴 Implement BFS and DFS on a graph using adjacency lists.
584. 🔴 Implement a generic in-memory cache with expiry (TTL).

---

## 21. Coding Problems — OOP & Low-Level Design

585. 🟢 Design a `Shape` hierarchy (`Circle`, `Rectangle`, `Triangle`) with an `Area()` method using abstract classes/interfaces.
586. 🟢 Create an `Employee` base class with `Manager` and `Developer` derived classes and calculate salary polymorphically.
587. 🟡 Implement a thread-safe singleton in at least three different ways.
588. 🟡 Implement the Strategy pattern for different discount/fee calculations.
589. 🟡 Implement the Observer pattern using C# events (stock price ticker).
590. 🟡 Implement a Factory that creates different payment processors (UPI, card, net banking).
591. 🟡 Implement a Decorator that adds logging/caching to a service interface.
592. 🟡 Implement a Builder for a complex object (e.g., an HTTP request or report).
593. 🟡 Implement the Dispose pattern for a class that holds a file stream.
594. 🟡 Implement `IComparable<T>` and `IEquatable<T>` for a `Version` or `Employee` class.
595. 🟡 Implement a custom collection that supports `foreach` and LINQ (`IEnumerable<T>`).
596. 🟡 Create a custom exception hierarchy for a banking application.
597. 🟡 Implement a simple dependency injection container using reflection.
598. 🔴 Design a parking lot system (classes, interfaces, relationships).
599. 🔴 Design a library management system.
600. 🔴 Design a vending machine using the State pattern.
601. 🔴 Design an elevator system.
602. 🔴 Design an in-memory key-value store with transactions (begin/commit/rollback).
603. 🔴 Design a notification system (email/SMS/push) that is open for extension.
604. 🔴 Design a simple rule engine / validation pipeline using Chain of Responsibility.
605. 🔴 Design a plugin system that loads types at runtime.
606. 🔴 Design a URL shortener's core classes.

---

## 22. Coding Problems — Multithreading & Async

607. 🟡 Print odd and even numbers alternately using two threads.
608. 🟡 Print "Ping" and "Pong" alternately N times using two threads/tasks.
609. 🟡 Make a counter thread-safe in three ways (`lock`, `Interlocked`, `SemaphoreSlim`).
610. 🟡 Demonstrate a race condition and fix it.
611. 🟡 Write code that causes a deadlock, then fix it.
612. 🟡 Call three APIs in parallel and combine their results.
613. 🟡 Process a list of 1000 URLs asynchronously with at most 10 concurrent requests.
614. 🟡 Implement a timeout for an async operation using `CancellationToken`.
615. 🟡 Implement a retry mechanism with exponential backoff and jitter.
616. 🟡 Convert an event-based/callback API to a Task-based API using `TaskCompletionSource`.
617. 🔴 Implement the producer-consumer problem using `BlockingCollection`, and again using `Channel<T>`.
618. 🔴 Implement a thread-safe bounded blocking queue from scratch using `Monitor.Wait`/`Pulse`.
619. 🔴 Implement a rate limiter (token bucket or sliding window) that is thread-safe.
620. 🔴 Implement an async lock (`AsyncLock`) using `SemaphoreSlim`.
621. 🔴 Implement a simple thread pool.
622. 🔴 Implement a thread-safe lazy cache where the value factory runs only once per key.
623. 🔴 Implement a debounce/throttle utility for async calls.
624. 🔴 Implement a background worker that processes jobs from a queue and supports graceful shutdown.
625. 🔴 Implement `Task.WhenAll` behavior yourself (without using `Task.WhenAll`).
626. 🔴 Implement an async stream (`IAsyncEnumerable`) that pages through an API.

---

## 23. Coding Problems — Financial Domain 💰

627. 🟢💰 Calculate simple interest and compound interest using `decimal`.
628. 🟡💰 Calculate loan EMI given principal, annual rate and tenure in months.
629. 🟡💰 Generate a full loan amortization schedule (principal, interest, balance per month).
630. 🟡💰 Implement a `Money` value type with currency-safe addition, subtraction and rounding.
631. 🟡💰 Split an amount among N people so the total matches exactly (allocate remainder paisa/cents).
632. 🟡💰 Implement a bank `Account` class with deposit, withdraw and balance checks, throwing custom exceptions.
633. 🔴💰 Implement a thread-safe fund transfer between two accounts that avoids deadlocks.
634. 🔴💰 Implement idempotent payment processing using an idempotency key.
635. 🟡💰 Given a list of transactions, calculate the closing balance per account using LINQ.
636. 🟡💰 Given daily stock prices, find the maximum profit from one buy and one sell.
637. 🟡💰 Calculate a simple moving average (SMA) over a window of prices.
638. 🟡💰 Calculate the volume-weighted average price (VWAP) from a list of trades.
639. 🔴💰 Implement a simple order book that matches buy and sell orders (price-time priority).
640. 🔴💰 Detect potentially fraudulent transactions (e.g., more than N transactions in M minutes per card).
641. 🔴💰 Aggregate trades by symbol and compute net position and average price.
642. 🔴💰 Validate a credit card number using the Luhn algorithm.
643. 🔴💰 Convert currency amounts using exchange rates with correct rounding.
644. 🔴💰 Parse a large transaction CSV file in a streaming, low-allocation manner and compute totals.
645. 🔴💰 Implement a portfolio class that calculates total value, P&L and allocation percentage per holding.

---

## 24. Scenario-Based & Debugging Questions

646. 🟡 Your application's memory keeps growing over time. How would you investigate?
647. 🟡 An API becomes slow under load and you see thread pool starvation. What could be the cause in the C# code?
648. 🟡 A method using `async void` crashes the process occasionally. Why, and how do you fix it?
649. 🟡 You see a `NullReferenceException` in production with no clear source. How would you debug and prevent it?
650. 🟡 A `Dictionary` lookup fails for a key you know you inserted. What might be wrong?
651. 🟡 A UI application freezes when calling an async method. What is likely happening?
652. 🟡 A LINQ query hits the database many times inside a loop. How would you identify and fix it?
653. 🟡 A `foreach` throws "Collection was modified". How do you fix it?
654. 🔴 Two services deadlock occasionally while transferring money. How would you find and fix the issue?
655. 🔴 A counter shared across threads shows wrong totals. How would you fix it?
656. 🔴 GC pauses cause latency spikes in a trading application. What changes would you make?
657. 🔴 A library you ship breaks consumers after changing a `const`. Why?
658. 🔴 Exceptions from background tasks are being silently lost. How would you surface them?
659. 🔴 Your sum of `double` amounts doesn't match the accounting report. What's the cause and fix?
660. 🔴 How would you review a pull request in C#? What would you look for?
661. 🔴 How would you refactor a 3000-line "God class"?
662. 🔴 How would you make legacy synchronous code asynchronous safely?
663. 🔴 How would you improve the performance of a hot method that allocates heavily?

---

## 25. Rapid-Fire Round

664. 🟢 Default value of `int`, `bool`, `string`, `object`, `DateTime`, `decimal`?
665. 🟢 Can a class have multiple static constructors?
666. 🟢 Can a static method be virtual or overridden?
667. 🟢 Can we declare a private abstract method?
668. 🟢 Can a `sealed` class have virtual methods?
669. 🟢 Can an interface inherit from another interface? From a class?
670. 🟢 Can a struct have a finalizer?
671. 🟢 Can `string` be used in a `switch` statement?
672. 🟢 Is `string` a value type or reference type?
673. 🟢 What is the base class of all classes in C#?
674. 🟢 Can you inherit from `System.String`?
675. 🟢 Can you use `this` inside a static method?
676. 🟢 Can a constructor be private? Can it be static and have parameters?
677. 🟢 Can `foreach` loop variables be modified?
678. 🟢 Can you have a `try` block inside a `finally` block?
679. 🟢 Can a method return multiple values? Name four ways.
680. 🟢 Can an `out` parameter be left unassigned?
681. 🟢 Can you assign `null` to a `struct` variable?
682. 🟢 What is the maximum length of an array / string in .NET?
683. 🟢 Is `Dictionary` ordered?
684. 🟢 Which is faster: `for` or `foreach` over a `List<T>`? Over an array?
685. 🟢 Which namespace contains `Task`? `List<T>`? `StringBuilder`?
686. 🟡 Can a property be `virtual`, `abstract`, `static`?
687. 🟡 Can an indexer be static?
688. 🟡 Can an extension method override an instance method?
689. 🟡 Can you use `await` in a `catch` or `finally` block?
690. 🟡 Can you use `yield return` inside a `try` with a `catch`?
691. 🟡 Can a lambda be recursive?
692. 🟡 Can you `lock` on `null`?
693. 🟡 Can an event be declared in an interface?
694. 🟡 Can a record be `sealed` / `abstract`?
695. 🟡 Can a generic type parameter be `static`?
696. 🟡 Can you create an instance of an interface?
697. 🟡 What is the size of a `bool`? Of a `char`? Of a `decimal`?
698. 🟡 Is `int` thread-safe for reads and writes? Is `long` on a 32-bit system?
699. 🟡 Is `Random` thread-safe? What is `Random.Shared`?
700. 🔴 Is `HttpClient` safe to share across threads?
701. 🔴 Is `ToString()` on a record safe to log for objects holding sensitive data?
702. 🔴 What is the difference between `Environment.Exit` and `Environment.FailFast`?

---

> **Next part:** .NET / .NET Core runtime, ASP.NET Core, Web API, Dependency Injection, Middleware, EF Core, Authentication/Authorization, Microservices and Testing.
