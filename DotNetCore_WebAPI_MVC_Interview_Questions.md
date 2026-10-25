# 🎯 .NET Core, Web API & MVC Interview Questions — Part 2 (Questions Only)

> **Scope:** .NET Core / modern .NET runtime & hosting, ASP.NET Core Web API, ASP.NET Core MVC, Dependency Injection, Middleware, REST API, SOAP API, and tricky API questions.
> **Not covered here:** EF Core, Microservices, Authentication/Authorization.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers up to .NET 10 / ASP.NET Core 10.**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. .NET Core Fundamentals & Runtime
2. Project Structure, Hosting & Startup
3. Configuration, Options & Environments
4. Logging, Diagnostics & Health Checks
5. Dependency Injection
6. Middleware & Request Pipeline
7. Routing
8. ASP.NET Core Web API — Controllers & Actions
9. Model Binding & Validation
10. Filters
11. Minimal APIs
12. Error Handling in APIs
13. Content Negotiation, Serialization & Formatters
14. Performance, Caching & Scalability
15. HttpClient & Calling External APIs
16. Background Services & Hosted Services
17. ASP.NET Core MVC
18. REST API Concepts & Design
19. API Versioning, Documentation & Contracts
20. SOAP API & WCF
21. REST vs SOAP vs gRPC vs GraphQL
22. Testing ASP.NET Core Applications
23. Deployment & Hosting
24. Tricky API Questions
25. Predict the Behavior (Code Snippets)
26. Coding & Hands-On Tasks
27. Scenario-Based & Debugging Questions
28. Rapid-Fire Round

---

## 1. .NET Core Fundamentals & Runtime

1. 🟢 What is .NET Core? How is it different from .NET Framework?
2. 🟢 What is the difference between .NET Framework, .NET Core, .NET 5+ and .NET Standard?
3. 🟢 Why did Microsoft drop "Core" from the name after .NET Core 3.1?
4. 🟢 What are the main advantages of .NET Core (cross-platform, performance, side-by-side, open source)?
5. 🟢 What is the CLR? What is CoreCLR?
6. 🟢 What is the BCL / CoreFX?
7. 🟢 What is the difference between the .NET SDK and the .NET Runtime?
8. 🟢 What is the ASP.NET Core shared framework (`Microsoft.AspNetCore.App`)?
9. 🟡 What is the difference between LTS and STS releases? Which versions are LTS?
10. 🟡 What is .NET Standard? Is it still relevant in modern .NET?
11. 🟡 What is a Target Framework Moniker (TFM)? What is multi-targeting?
12. 🟢 What is NuGet? What is the difference between a package reference and a project reference?
13. 🟡 What is Central Package Management (`Directory.Packages.props`)?
14. 🟡 What are `Directory.Build.props` and `Directory.Build.targets`?
15. 🟢 What is the `dotnet` CLI? Name the commands you use daily.
16. 🟡 What is `global.json` used for?
17. 🟡 What is the difference between framework-dependent and self-contained deployment?
18. 🟡 What is single-file publishing? What is trimming?
19. 🔴 What is ReadyToRun (R2R) compilation?
20. 🔴 What is Native AOT? What are its limitations for ASP.NET Core apps?
21. 🔴 What is tiered compilation and Dynamic PGO?
22. 🟡 What is the difference between `AppDomain` in .NET Framework and `AssemblyLoadContext` in .NET Core?
23. 🟡 Which .NET Framework technologies are not available in .NET Core (Web Forms, WCF server, Remoting, AppDomains)?
24. 🔴 How would you migrate a .NET Framework application to modern .NET? What tools help?
25. 🟡 What is the .NET Upgrade Assistant?
26. 🟡 What is `System.Runtime` metadata? What is a runtime identifier (RID)?
27. 🔴 What are .NET Aspire and its purpose (high-level only)?

---

## 2. Project Structure, Hosting & Startup

28. 🟢 Explain the structure of an ASP.NET Core project.
29. 🟢 What is the role of `Program.cs` in ASP.NET Core?
30. 🟢 What was `Startup.cs`? Why was it removed from templates in .NET 6?
31. 🟢 What is the difference between `ConfigureServices` and `Configure` methods?
32. 🟢 What is `WebApplication` and `WebApplicationBuilder`?
33. 🟡 What is the Generic Host (`IHost`)? How is it different from the old `WebHost`?
34. 🟡 What does `WebApplication.CreateBuilder(args)` configure by default?
35. 🟡 What is `WebApplication.CreateSlimBuilder` and `CreateEmptyBuilder`?
36. 🟢 What is Kestrel? Why is it the default web server?
37. 🟡 What is the difference between Kestrel, IIS, HTTP.sys and Nginx?
38. 🟡 What is the in-process vs out-of-process hosting model in IIS?
39. 🟡 What is the ASP.NET Core Module (ANCM)?
40. 🟡 Why do we use a reverse proxy in front of Kestrel?
41. 🟢 What is `launchSettings.json`? Is it used in production?
42. 🟢 What is the `wwwroot` folder?
43. 🟡 What is `IHostApplicationLifetime`? How do you run code on application start and stop?
44. 🟡 What is graceful shutdown? How do you configure the shutdown timeout?
45. 🟡 What is the order in which the host builds services and the request pipeline?
46. 🟡 What is `IWebHostEnvironment` / `IHostEnvironment`?
47. 🔴 How does ASP.NET Core process an HTTP request from the moment it reaches Kestrel to the response?
48. 🟡 What is `HttpContext`? What does it contain?
49. 🔴 Why is `HttpContext` not thread-safe? What is `IHttpContextAccessor` and when should you avoid it?
50. 🟡 What are `HttpRequest` and `HttpResponse` features (`IFeatureCollection`)?

---

## 3. Configuration, Options & Environments

51. 🟢 How does configuration work in ASP.NET Core?
52. 🟢 What is `appsettings.json`? What is `appsettings.{Environment}.json`?
53. 🟢 What configuration providers are available (JSON, environment variables, command line, user secrets, Key Vault, etc.)?
54. 🟡 What is the default order of configuration providers? Which one wins?
55. 🟢 How do you read a configuration value using `IConfiguration`?
56. 🟡 How do environment variables map to nested configuration keys (`__` separator)?
57. 🟢 What is the Options pattern? Why is it preferred over `IConfiguration` directly?
58. 🟡 What is the difference between `IOptions<T>`, `IOptionsSnapshot<T>` and `IOptionsMonitor<T>`?
59. 🟡 Which options interface can be injected into a singleton? Why?
60. 🟡 How do you validate options at startup (`ValidateDataAnnotations`, `ValidateOnStart`)?
61. 🟡 What are named options?
62. 🟡 How do you reload configuration without restarting the app (`reloadOnChange`)?
63. 🟢 What is the Secret Manager (user secrets)? Is it for production?
64. 🟡 How do you store secrets safely in production?
65. 🟢 What are the built-in environments (Development, Staging, Production)? How is the environment set?
66. 🟡 How do you write environment-specific code in `Program.cs`?
67. 🔴 How would you build a custom configuration provider (e.g., reading from a database)?
68. 🟡 What is `IConfigurationSection` and `GetSection().Bind()` vs `Get<T>()`?

---

## 4. Logging, Diagnostics & Health Checks

69. 🟢 How does logging work in ASP.NET Core? What is `ILogger<T>`?
70. 🟢 What are log levels? Which one is the default?
71. 🟡 What are logging providers? Name the built-in ones.
72. 🟡 What is structured logging? Why is it better than string concatenation?
73. 🟡 Why should you write `logger.LogInformation("User {Id}", id)` instead of using string interpolation?
74. 🔴 What is `[LoggerMessage]` source-generated logging and why is it faster?
75. 🟡 What are log scopes (`BeginScope`)?
76. 🟡 How do you integrate Serilog or NLog?
77. 🟡 What is a correlation ID? How would you add it to every log in a request?
78. 🟡 What is HTTP logging middleware (`UseHttpLogging`) and W3C logging?
79. 🟡 What is OpenTelemetry? What are traces, metrics and logs?
80. 🔴 What is `System.Diagnostics.Activity` and distributed tracing in .NET?
81. 🔴 What are `dotnet-counters`, `dotnet-trace`, `dotnet-dump` and `dotnet-gcdump`?
82. 🟢 What are health checks? How do you add them?
83. 🟡 What is the difference between liveness and readiness health checks?
84. 🟡 How would you write a custom health check?
85. 🔴 What is `IMeterFactory` / the `System.Diagnostics.Metrics` API?

---

## 5. Dependency Injection

86. 🟢 What is Dependency Injection? What problem does it solve?
87. 🟢 What is Inversion of Control? How is it related to DI?
88. 🟢 What is the Dependency Inversion Principle? How is it different from DI?
89. 🟢 What are the types of dependency injection (constructor, property, method)? Which does ASP.NET Core support by default?
90. 🟢 What is the built-in DI container in .NET? What is `IServiceCollection` and `IServiceProvider`?
91. 🟢 What are the three service lifetimes? Explain `Transient`, `Scoped` and `Singleton`.
92. 🟢 Give a real-world example of when to use each lifetime.
93. 🟡 What is a scope in ASP.NET Core? When is a scope created and disposed?
94. 🔴 What is a captive dependency? What happens if a singleton depends on a scoped service?
95. 🟡 What is scope validation (`ValidateScopes`, `ValidateOnBuild`)? When is it enabled by default?
96. 🟡 How do you resolve a scoped service inside a singleton or a background service?
97. 🟡 What is `IServiceScopeFactory` and `CreateScope()` / `CreateAsyncScope()`?
98. 🟡 What is the difference between `AddSingleton(new X())` and `AddSingleton<X>()` in terms of disposal?
99. 🟡 Who disposes services resolved from the container? When?
100. 🔴 Why can transient `IDisposable` services cause memory leaks when resolved from the root provider?
101. 🟡 What is the difference between `Add`, `TryAdd`, `TryAddEnumerable` and `Replace`?
102. 🟡 What happens if you register multiple implementations for the same interface? Which one gets injected?
103. 🟡 How do you inject all implementations of an interface (`IEnumerable<T>`)?
104. 🟡 What are keyed services (.NET 8)? How do you use `[FromKeyedServices]`?
105. 🟡 How did you choose between multiple implementations before keyed services (factory, delegate, strategy)?
106. 🟡 How do you register a service using a factory delegate?
107. 🟡 How do you register open generic types (`AddScoped(typeof(IRepository<>), typeof(Repository<>))`)?
108. 🟡 What is constructor over-injection? What does it indicate?
109. 🟡 What is the Service Locator pattern? Why is it considered an anti-pattern?
110. 🟡 Is calling `app.Services.GetService<T>()` or `HttpContext.RequestServices` bad? When is it acceptable?
111. 🟡 What is the difference between `GetService<T>()` and `GetRequiredService<T>()`?
112. 🟡 How do you inject a service into a controller action instead of the constructor (`[FromServices]`)?
113. 🟡 How do you inject services into middleware? Constructor vs `Invoke` parameters?
114. 🟡 How do you inject services into a view in MVC (`@inject`)?
115. 🟡 How do you inject services into filters (`ServiceFilter`, `TypeFilter`)?
116. 🔴 What are the limitations of the built-in container compared to Autofac, Scrutor, etc.?
117. 🔴 How would you implement the Decorator pattern with the built-in DI container?
118. 🔴 How do you register services by convention / assembly scanning?
119. 🟡 How do you organise registrations with extension methods (`AddMyFeature()`)?
120. 🔴 What happens if there is a circular dependency between services?
121. 🔴 How does the container decide which constructor to use when there are multiple?
122. 🟡 Can you use DI in a console application? How?
123. 🟡 How is DI helpful for unit testing?
124. 🔴 Is the built-in container thread-safe? Are your singleton services automatically thread-safe?
125. 🔴 What is the difference between `IDisposable` and `IAsyncDisposable` services in the container?

---

## 6. Middleware & Request Pipeline

126. 🟢 What is middleware in ASP.NET Core?
127. 🟢 What is the request pipeline? Explain the request/response flow through middleware.
128. 🟢 What is a `RequestDelegate`?
129. 🟢 What is the difference between `app.Use()`, `app.Run()` and `app.Map()`?
130. 🟡 What is `app.MapWhen()` and `app.UseWhen()`? How do they differ?
131. 🟡 What is short-circuiting in middleware?
132. 🟢 Why does the order of middleware matter? Give an example where wrong order causes a bug.
133. 🟡 What is the recommended order of the built-in middleware?
134. 🟢 How do you create custom middleware? Explain convention-based middleware.
135. 🟡 What is factory-based middleware (`IMiddleware`)? How is it different from convention-based middleware?
136. 🔴 What lifetime does convention-based middleware have? Why can't you inject scoped services into its constructor?
137. 🟡 What happens if you modify response headers after the response has started?
138. 🟡 What is `HttpResponse.HasStarted` and `OnStarting()`?
139. 🟡 How do you read the request body in middleware more than once (`EnableBuffering`)?
140. 🟡 How do you capture or modify the response body in middleware?
141. 🟡 Middleware vs filters — what are the differences and when do you use each?
142. 🟡 Name built-in middleware: static files, routing, CORS, response compression, response caching, HTTPS redirection, HSTS, exception handler, rate limiter, request timeouts, output caching.
143. 🟢 What does `UseRouting()` and `UseEndpoints()` / `MapControllers()` do?
144. 🟡 What is endpoint routing? Why was it introduced?
145. 🟢 What is the static files middleware? How do you serve files outside `wwwroot`?
146. 🟡 What is `UseHttpsRedirection` and `UseHsts`?
147. 🟡 What is CORS? How do you configure CORS policies in ASP.NET Core?
148. 🟡 What is a CORS preflight request? When does a browser send one?
149. 🟡 Why can't you use `AllowAnyOrigin()` with `AllowCredentials()`?
150. 🟡 What is response compression middleware? When should you avoid it?
151. 🟡 What is the rate limiting middleware (.NET 7)? Explain fixed window, sliding window, token bucket and concurrency limiters.
152. 🟡 What is the request timeouts middleware (.NET 8)?
153. 🔴 How would you write middleware that logs request time, request body and response status?
154. 🔴 How would you write middleware that adds a correlation ID header to every request and response?
155. 🔴 How do you write middleware that handles exceptions globally?
156. 🔴 How does terminal middleware differ from non-terminal middleware?
157. 🔴 What happens if middleware calls `next()` and then writes to the response?
158. 🟡 What is `UseForwardedHeaders` and why is it needed behind a proxy or load balancer?

---

## 7. Routing

159. 🟢 What is routing in ASP.NET Core?
160. 🟢 What is the difference between conventional routing and attribute routing?
161. 🟢 Which routing type is recommended for Web APIs? Why?
162. 🟢 How do you define route parameters and optional parameters?
163. 🟡 What are route constraints (`{id:int}`, `{name:alpha}`, `{date:datetime}`)? Should they be used for validation?
164. 🟡 How do you create a custom route constraint?
165. 🟡 What are route tokens (`[controller]`, `[action]`)?
166. 🟡 What is a catch-all route parameter (`{*path}`)?
167. 🟡 What is route precedence/ordering? How does ASP.NET Core resolve ambiguous routes?
168. 🟡 What causes `AmbiguousMatchException` in routing?
169. 🟡 What are route names and link generation (`Url.Action`, `CreatedAtAction`, `LinkGenerator`)?
170. 🟡 What is a route prefix at controller level (`[Route("api/[controller]")]`)?
171. 🟡 What are areas in MVC routing?
172. 🟡 What are route groups in Minimal APIs (`MapGroup`)?
173. 🟡 What is the difference between `[HttpGet("{id}")]` and `[Route("{id}")]` + `[HttpGet]`?
174. 🔴 How do you implement lowercase URLs and slugs?
175. 🔴 What is `IEndpointRouteBuilder` and how do you inspect registered endpoints?

---

## 8. ASP.NET Core Web API — Controllers & Actions

176. 🟢 What is ASP.NET Core Web API?
177. 🟢 What is the difference between `Controller` and `ControllerBase`?
178. 🟢 What does the `[ApiController]` attribute do? List all its behaviors.
179. 🟢 What are action methods? What can an action return?
180. 🟢 What is the difference between returning `IActionResult`, `ActionResult<T>` and a plain type `T`?
181. 🟡 Why is `ActionResult<T>` preferred over `IActionResult` in Web APIs?
182. 🟢 Name common action results: `Ok`, `Created`, `CreatedAtAction`, `NoContent`, `BadRequest`, `NotFound`, `Conflict`, `StatusCode`, `Problem`, `ValidationProblem`.
183. 🟡 What does `CreatedAtAction` return? Why is it important for REST?
184. 🟢 What are `[HttpGet]`, `[HttpPost]`, `[HttpPut]`, `[HttpPatch]`, `[HttpDelete]` attributes?
185. 🟡 Can one action handle multiple HTTP verbs?
186. 🟢 Should Web API actions be async? Why?
187. 🟡 What happens if you return `Task<IActionResult>` but block with `.Result` inside?
188. 🟡 How do you accept a `CancellationToken` in an action? When is it cancelled?
189. 🟡 What is `[NonAction]`?
190. 🟡 What is `[Produces]`, `[Consumes]` and `[ProducesResponseType]`?
191. 🟡 How do you return a file from an API (`File`, `PhysicalFile`, `FileStreamResult`)?
192. 🟡 How do you upload single and multiple files (`IFormFile`, `IFormFileCollection`)?
193. 🔴 How do you upload very large files without buffering them in memory (streaming)?
194. 🟡 What are request size limits and how do you change them (`RequestSizeLimit`, Kestrel limits)?
195. 🟡 How do you return a stream of data (`IAsyncEnumerable<T>`) from an API?
196. 🟡 How do you set response headers from an action?
197. 🟡 What is `ControllerContext` and `HttpContext` inside a controller?
198. 🔴 How are controllers created? What is their lifetime? Can a controller be a singleton?
199. 🟡 What is a thin controller? Why should business logic not be in controllers?
200. 🟡 What are DTOs? Why should you not expose domain entities directly from APIs?
201. 🟡 What is AutoMapper? What are its pros and cons? What alternatives exist (manual mapping, Mapster)?

---

## 9. Model Binding & Validation

202. 🟢 What is model binding?
203. 🟢 What binding sources exist: `[FromRoute]`, `[FromQuery]`, `[FromBody]`, `[FromForm]`, `[FromHeader]`, `[FromServices]`?
204. 🟡 What is the default binding source for complex types and simple types with `[ApiController]`?
205. 🟡 Can you have more than one `[FromBody]` parameter? Why not?
206. 🟡 Why does a `[FromBody]` parameter come as `null` sometimes? List the common causes.
207. 🟡 How do you bind arrays and lists from query strings?
208. 🟡 What is `[AsParameters]` in Minimal APIs?
209. 🔴 How do you write a custom model binder? When is it needed?
210. 🔴 What is a model binder provider?
211. 🟢 What is model validation? How do Data Annotations work?
212. 🟢 Name common validation attributes: `[Required]`, `[StringLength]`, `[Range]`, `[RegularExpression]`, `[EmailAddress]`, `[Compare]`.
213. 🟡 What is `ModelState`? What is `ModelState.IsValid`?
214. 🟡 Do you need to check `ModelState.IsValid` when using `[ApiController]`?
215. 🟡 How do you customize the automatic 400 validation response (`InvalidModelStateResponseFactory`)?
216. 🟡 How do you create a custom validation attribute?
217. 🟡 What is `IValidatableObject`?
218. 🟡 What is FluentValidation? Data Annotations vs FluentValidation?
219. 🟡 What is the difference between `[Required]` on a non-nullable `int` and on `int?`?
220. 🔴 What is over-posting (mass assignment)? How do you prevent it?
221. 🔴 How does validation work for nested objects and collections?
222. 🟡 How does Minimal API validation work in .NET 10 (`AddValidation`)?

---

## 10. Filters

223. 🟢 What are filters in ASP.NET Core MVC / Web API?
224. 🟢 What are the types of filters? Explain the order in which they run.
225. 🟡 What is the difference between action filters, result filters, resource filters and exception filters?
226. 🟡 What is the difference between synchronous and asynchronous filters (`IActionFilter` vs `IAsyncActionFilter`)?
227. 🟡 What are the filter scopes (global, controller, action)? What is the execution order across scopes?
228. 🟡 How do you control the order of filters (`Order` property)?
229. 🟡 What is the difference between `ServiceFilter`, `TypeFilter` and attribute-based filters?
230. 🟡 How do you inject dependencies into a filter?
231. 🟡 How do you short-circuit a request in a filter?
232. 🟡 What is `ActionExecutingContext` and `ActionExecutedContext`?
233. 🟡 Exception filters vs exception handling middleware — which is better and why?
234. 🟡 What exceptions do exception filters NOT catch?
235. 🟡 What is an endpoint filter in Minimal APIs (`IEndpointFilter`)?
236. 🔴 Write an action filter that logs execution time of every action.
237. 🔴 Write a filter that validates an idempotency key header. 💰
238. 🔴 What are `IAlwaysRunResultFilter` and `IFilterFactory`?

---

## 11. Minimal APIs

239. 🟢 What are Minimal APIs? When were they introduced?
240. 🟢 What is the difference between Minimal APIs and controller-based APIs?
241. 🟡 When would you choose Minimal APIs over controllers, and vice versa?
242. 🟡 How do you organise Minimal API endpoints in a large project?
243. 🟡 What is `TypedResults` vs `Results`? Why use `TypedResults`?
244. 🟡 What is `Results<Ok<T>, NotFound>` (union return types)?
245. 🟡 How does parameter binding work in Minimal APIs?
246. 🟡 How do you add OpenAPI metadata to Minimal APIs (`WithName`, `WithTags`, `Produces`)?
247. 🟡 What are route groups and how do you apply filters to a group?
248. 🔴 Why are Minimal APIs considered faster? What is Request Delegate Generator (RDG)?
249. 🔴 Are Minimal APIs compatible with Native AOT? What about controllers?

---

## 12. Error Handling in APIs

250. 🟢 How do you handle exceptions globally in ASP.NET Core?
251. 🟢 What is `UseExceptionHandler()`? What is `UseDeveloperExceptionPage()`?
252. 🟡 What is `IExceptionHandler` (.NET 8)? How do you register multiple handlers?
253. 🟡 What is Problem Details (RFC 7807 / RFC 9457)? What fields does it contain?
254. 🟡 How do you enable Problem Details for all errors (`AddProblemDetails`)?
255. 🟡 What is `UseStatusCodePages()`?
256. 🟡 How do you return consistent error responses across all APIs?
257. 🟡 Should you return exception stack traces in API responses? Why not?
258. 🟡 How do you map custom domain exceptions to HTTP status codes?
259. 🟡 Exceptions vs Result pattern for business errors — which would you choose?
260. 🔴 How do you handle exceptions thrown after the response has already started?
261. 🔴 How do you handle errors in background tasks started from an API request?
262. 🟡 What is a trace ID in Problem Details and why is it useful?

---

## 13. Content Negotiation, Serialization & Formatters

263. 🟢 What is content negotiation?
264. 🟢 What role do the `Accept` and `Content-Type` headers play?
265. 🟡 What happens if the client requests a format the server doesn't support? How do you return 406?
266. 🟡 How do you add XML support to a Web API?
267. 🟡 What are input formatters and output formatters?
268. 🔴 How do you write a custom output formatter (e.g., CSV)?
269. 🟢 What JSON serializer does ASP.NET Core use by default?
270. 🟡 How do you configure `System.Text.Json` options globally (camelCase, enums as strings, null handling)?
271. 🟡 How do you switch to Newtonsoft.Json? When would you need to?
272. 🟡 How do you handle reference loops/cycles in JSON serialization?
273. 🟡 How do you serialize enums as strings?
274. 🟡 How do you handle date and time formats in JSON?
275. 🟡💰 How should `decimal` values and monetary amounts be serialized to avoid precision loss on clients?
276. 🔴 What is source-generated JSON serialization (`JsonSerializerContext`) and why use it?
277. 🔴 How do you write a custom `JsonConverter`?
278. 🟡 What is polymorphic serialization (`[JsonDerivedType]`)?

---

## 14. Performance, Caching & Scalability

279. 🟢 What types of caching are available in ASP.NET Core?
280. 🟢 What is in-memory caching (`IMemoryCache`)? What are its limitations?
281. 🟡 What is distributed caching (`IDistributedCache`)? When do you need it?
282. 🟡 What is Redis and how do you use it as a distributed cache?
283. 🟡 What is `HybridCache` (.NET 9)? What problem does it solve (cache stampede)?
284. 🟡 What is absolute expiration vs sliding expiration?
285. 🟡 What is response caching vs output caching? How are they different?
286. 🟡 What does `[ResponseCache]` do? Does it cache on the server?
287. 🟡 What is cache invalidation? What strategies exist?
288. 🔴 What is a cache stampede and how do you prevent it?
289. 🟡 What are ETags and conditional requests (`If-None-Match`, `If-Match`)?
290. 🟡 How do you improve the performance of an ASP.NET Core API? List at least 10 techniques.
291. 🟡 Why is `async` important for API scalability?
292. 🔴 What is thread pool starvation in ASP.NET Core? How do you detect it?
293. 🟡 What is response compression? Gzip vs Brotli?
294. 🟡 What is pagination? Offset-based vs cursor/keyset-based pagination?
295. 🔴 What is object pooling (`ObjectPool<T>`) in ASP.NET Core?
296. 🔴 How do you benchmark and load test an API (BenchmarkDotNet, k6, JMeter, NBomber)?
297. 🟡 What is HTTP/2 and HTTP/3 support in Kestrel? What benefits do they provide?
298. 🔴 How do you scale an ASP.NET Core API horizontally? What must be stateless?
299. 🔴 What is sticky session and why should APIs avoid it?

---

## 15. HttpClient & Calling External APIs

300. 🟢 How do you call an external API from ASP.NET Core?
301. 🟡 What is the problem with creating `new HttpClient()` for every request (socket exhaustion)?
302. 🟡 What is the problem with a single static `HttpClient` (DNS changes)?
303. 🟡 What is `IHttpClientFactory`? What problems does it solve?
304. 🟡 What are named clients and typed clients?
305. 🟡 What is `SocketsHttpHandler` and `PooledConnectionLifetime`?
306. 🟡 What are `DelegatingHandler`s? Give a use case.
307. 🟡 How do you set a timeout for `HttpClient` calls?
308. 🟡 What is Polly? What resilience strategies does it provide (retry, circuit breaker, timeout, fallback, bulkhead)?
309. 🟡 What is `Microsoft.Extensions.Http.Resilience` and `AddStandardResilienceHandler`?
310. 🔴 What is a circuit breaker? Explain its states.
311. 🔴 Why can retries be dangerous for non-idempotent operations (POST payments)? 💰
312. 🟡 How do you deserialize responses efficiently (`GetFromJsonAsync`, `ReadFromJsonAsync`)?
313. 🟡 What is `EnsureSuccessStatusCode()`? Should you always use it?
314. 🔴 How do you stream a large response with `HttpCompletionOption.ResponseHeadersRead`?
315. 🔴 What is Refit? What are its pros and cons?

---

## 16. Background Services & Hosted Services

316. 🟢 What is `IHostedService`?
317. 🟢 What is `BackgroundService`? How is it different from `IHostedService`?
318. 🟡 How do you run a recurring task in ASP.NET Core (`PeriodicTimer`)?
319. 🟡 How do you use scoped services inside a `BackgroundService`?
320. 🟡 What happens if `ExecuteAsync` throws an exception? (`BackgroundServiceExceptionBehavior`)
321. 🟡 How do you handle graceful shutdown in a background service?
322. 🟡 What is a Worker Service project template?
323. 🔴 How would you implement a background job queue using `Channel<T>`?
324. 🟡 Hosted services vs Hangfire vs Quartz.NET — when would you use each?
325. 🔴 Why is `Task.Run` fire-and-forget inside a controller dangerous? What is the alternative?
326. 🔴 What is `IHostedLifecycleService` (.NET 8)?

---

## 17. ASP.NET Core MVC

327. 🟢 What is MVC? Explain Model, View and Controller.
328. 🟢 What is the difference between ASP.NET MVC (Framework) and ASP.NET Core MVC?
329. 🟢 What is the request life cycle in ASP.NET Core MVC?
330. 🟢 What is Razor? What is the Razor view engine?
331. 🟢 What is the difference between `View()`, `PartialView()`, `RedirectToAction()`, `Redirect()` and `Json()`?
332. 🟢 What is `ViewData`, `ViewBag` and `TempData`? What are the differences?
333. 🟡 How long does `TempData` persist? What are `Keep()` and `Peek()`?
334. 🟡 What providers can store `TempData` (cookie, session)?
335. 🟢 What is a strongly typed view? What is `@model`?
336. 🟢 What is a ViewModel? How is it different from a domain model?
337. 🟢 What is a layout page (`_Layout.cshtml`)? What is `@RenderBody()` and `@RenderSection()`?
338. 🟢 What are `_ViewStart.cshtml` and `_ViewImports.cshtml`?
339. 🟢 What are partial views?
340. 🟡 What are View Components? How are they different from partial views?
341. 🟡 What are Tag Helpers? How are they different from HTML Helpers?
342. 🟡 How do you create a custom Tag Helper?
343. 🟡 Name built-in Tag Helpers (`asp-for`, `asp-action`, `asp-controller`, `asp-route-*`, `asp-validation-for`, `environment`, `cache`).
344. 🟡 What are Razor Pages? How are they different from MVC?
345. 🟡 When would you choose Razor Pages over MVC?
346. 🟡 What are areas in MVC? When do you use them?
347. 🟡 What is the Post-Redirect-Get (PRG) pattern? Why is it used?
348. 🟡 What is client-side vs server-side validation in MVC?
349. 🟡 How does unobtrusive validation work?
350. 🟡 What is anti-forgery (CSRF) protection in MVC forms? What does `[ValidateAntiForgeryToken]` do?
351. 🟡 Why don't Web APIs typically need anti-forgery tokens? When do they?
352. 🟡 What is session state in ASP.NET Core? How do you enable it?
353. 🟡 What are cookies and how do you read/write them?
354. 🟡 What is view location expansion and how are views located?
355. 🟡 What is Razor runtime compilation?
356. 🟡 What is bundling and minification in ASP.NET Core?
357. 🟡 How do you handle 404 and error pages in MVC?
358. 🟡 What is `ChildActionOnly` and what replaced it in ASP.NET Core?
359. 🟡 What is output encoding in Razor and how does it prevent XSS?
360. 🟡 What is `Html.Raw()` and why is it dangerous?
361. 🔴 How would you structure a large MVC application?
362. 🔴 What is Blazor and how does it relate to Razor (high-level)?

---

## 18. REST API Concepts & Design

363. 🟢 What is REST? What does it stand for?
364. 🟢 What are the six constraints of REST (client-server, stateless, cacheable, uniform interface, layered system, code on demand)?
365. 🟢 What is a resource in REST?
366. 🟢 What is the difference between REST and RESTful?
367. 🟢 What are HTTP methods? Explain GET, POST, PUT, PATCH, DELETE, HEAD and OPTIONS.
368. 🟢 What is the difference between PUT and POST?
369. 🟢 What is the difference between PUT and PATCH?
370. 🟡 What is JSON Patch (RFC 6902) vs JSON Merge Patch (RFC 7396)?
371. 🟢 What are safe methods? What are idempotent methods? Classify each HTTP method.
372. 🟡 Is DELETE idempotent? What should the second DELETE of the same resource return?
373. 🟡 Is PATCH idempotent?
374. 🟢 What are HTTP status code classes (1xx, 2xx, 3xx, 4xx, 5xx)?
375. 🟢 Explain the most common status codes: 200, 201, 202, 204, 301, 302, 304, 400, 401, 403, 404, 405, 409, 412, 415, 422, 429, 500, 502, 503, 504.
376. 🟡 What is the difference between 401 and 403?
377. 🟡 What is the difference between 400 and 422?
378. 🟡 When should you return 202 Accepted?
379. 🟡 When should you return 204 vs 200 with a body?
380. 🟡 When should you return 409 Conflict?
381. 🟡 What is the difference between 502, 503 and 504?
382. 🟢 What are best practices for naming REST endpoints (nouns, plural, lowercase, hyphens)?
383. 🟡 How do you design nested resources (`/customers/{id}/orders`)? How deep should nesting go?
384. 🟡 How do you design actions that don't fit CRUD (e.g., `/orders/{id}/cancel`)?
385. 🟡 How do you implement filtering, sorting, searching and field selection in a REST API?
386. 🟡 How do you implement pagination? Where do you return pagination metadata (body vs headers)?
387. 🟡 What is HATEOAS? Have you used it?
388. 🟡 What is the Richardson Maturity Model?
389. 🟡 What does "stateless" mean in REST? Where is state kept?
390. 🟡 What are HTTP headers commonly used in APIs (`Accept`, `Content-Type`, `Cache-Control`, `ETag`, `Location`, `Retry-After`)?
391. 🟡 What is the `Location` header and when is it returned?
392. 🟡 What is idempotency key and how do you design idempotent POST APIs? 💰
393. 🟡 What is optimistic concurrency in REST APIs (ETag + `If-Match`, 412 Precondition Failed)?
394. 🟡 How do you design bulk/batch operations in REST?
395. 🟡 How do you design long-running operations in REST (202 + status endpoint / polling)?
396. 🟡 What are webhooks? How are they different from polling?
397. 🟡 What is rate limiting from an API design perspective? Which headers do you return?
398. 🟡 What is the difference between query parameters and path parameters?
399. 🟡 Should you send a request body with GET? Why not?
400. 🟡 What is the maximum URL length? When would you use POST for search?
401. 🟡 What is a URI vs URL vs URN?
402. 🟡 What is API-first design / contract-first design?
403. 🟡 What makes a good API error response?
404. 🔴 How would you design a REST API for a banking fund transfer? 💰
405. 🔴 How would you design a REST API for an e-commerce order lifecycle?
406. 🔴 How do you handle backward compatibility when changing an API?
407. 🔴 What are breaking vs non-breaking API changes? Give examples.
408. 🟡 What is CORS from an API consumer's perspective?
409. 🟡 What is the difference between HTTP/1.1, HTTP/2 and HTTP/3 for APIs?
410. 🟡 What is TLS/HTTPS and why must APIs use it?

---

## 19. API Versioning, Documentation & Contracts

411. 🟢 What is API versioning? Why is it needed?
412. 🟡 What are the strategies for API versioning (URL path, query string, header, media type)? Pros and cons?
413. 🟡 How do you implement versioning in ASP.NET Core (`Asp.Versioning`)?
414. 🟡 How do you deprecate an API version? How do you communicate it (`api-deprecated-versions`, `Sunset` header)?
415. 🟢 What is OpenAPI? What is Swagger? Are they the same?
416. 🟡 What is Swashbuckle vs NSwag vs `Microsoft.AspNetCore.OpenApi`?
417. 🟡 Why did the default Web API template stop including Swashbuckle in .NET 9?
418. 🟡 How do you add XML comments and examples to Swagger documentation?
419. 🟡 What is Scalar / ReDoc / Swagger UI?
420. 🟡 How do you generate a client SDK from an OpenAPI document?
421. 🟡 What is contract testing (e.g., Pact)?
422. 🟡 Should Swagger UI be enabled in production?
423. 🔴 How do you document multiple API versions in OpenAPI?

---

## 20. SOAP API & WCF

424. 🟢 What is SOAP? What does it stand for?
425. 🟢 What is the structure of a SOAP message (Envelope, Header, Body, Fault)?
426. 🟢 What is WSDL? What does it describe?
427. 🟡 What are the main parts of a WSDL document (types, message, portType, binding, service)?
428. 🟢 What is XSD and how is it used in SOAP?
429. 🟡 What transport protocols can SOAP use (HTTP, SMTP, TCP, JMS)?
430. 🟡 What is a SOAP Fault? What are its elements?
431. 🟡 What is the difference between SOAP 1.1 and SOAP 1.2?
432. 🟡 What is the SOAPAction header?
433. 🟡 What are the SOAP styles: Document/Literal, RPC/Literal, RPC/Encoded? Which is most common?
434. 🟡 What is WS-* (WS-Security, WS-ReliableMessaging, WS-AtomicTransaction, WS-Addressing)?
435. 🟡 Why is SOAP still used in banking, insurance, telecom and government systems? 💰
436. 🟢 What is WCF? What are its ABCs (Address, Binding, Contract)?
437. 🟡 What are `[ServiceContract]`, `[OperationContract]`, `[DataContract]` and `[DataMember]`?
438. 🟡 What are WCF bindings (BasicHttpBinding, WSHttpBinding, NetTcpBinding)?
439. 🟡 Is WCF server supported in .NET Core / modern .NET? What are the alternatives?
440. 🟡 What is CoreWCF?
441. 🟡 How do you consume a SOAP service from .NET Core (Connected Services, `dotnet-svcutil`)?
442. 🟡 What is `System.ServiceModel` client package in .NET?
443. 🟡 How do you create a SOAP service in ASP.NET Core (CoreWCF or SoapCore)?
444. 🔴 How would you expose a legacy SOAP service through a modern REST API (facade/adapter)?
445. 🔴 How do you debug SOAP calls (logging raw XML, Fiddler, SoapUI)?
446. 🟡 What is SoapUI / Postman used for in SOAP testing?
447. 🔴 What is MTOM and how are attachments sent in SOAP?
448. 🔴 What are the performance overheads of SOAP compared to REST?

---

## 21. REST vs SOAP vs gRPC vs GraphQL

449. 🟢 What are the differences between REST and SOAP? (protocol vs style, format, contract, transport, security, performance)
450. 🟢 When would you choose SOAP over REST?
451. 🟡 Is REST always JSON? Is SOAP always XML?
452. 🟡 Is REST stateless? Can SOAP be stateful?
453. 🟡 What is gRPC? How is it different from REST?
454. 🟡 What are Protocol Buffers?
455. 🟡 What are the four types of gRPC calls (unary, server streaming, client streaming, bidirectional)?
456. 🟡 Why can't browsers call gRPC directly? What is gRPC-Web?
457. 🟡 What is JSON transcoding for gRPC in ASP.NET Core?
458. 🟡 What is GraphQL? How does it solve over-fetching and under-fetching?
459. 🟡 What are the downsides of GraphQL compared to REST (caching, complexity, N+1)?
460. 🟡 What is SignalR? When would you use WebSockets/SignalR instead of REST?
461. 🟡 What is Server-Sent Events (SSE)? How is it supported in .NET 10?
462. 🔴 How would you choose between REST, gRPC, GraphQL and SignalR for a new system?

---

## 22. Testing ASP.NET Core Applications

463. 🟢 How do you unit test a controller?
464. 🟡 How do you mock dependencies (Moq, NSubstitute, FakeItEasy)?
465. 🟡 What is integration testing in ASP.NET Core? What is `WebApplicationFactory<TEntryPoint>`?
466. 🟡 How do you replace services in integration tests (`ConfigureTestServices`)?
467. 🟡 What is `TestServer`?
468. 🟡 How do you test middleware in isolation?
469. 🟡 How do you test filters?
470. 🟡 How do you mock `HttpClient` calls in tests?
471. 🟡 How do you test code that depends on time (`TimeProvider`, `FakeTimeProvider`)?
472. 🟡 How do you test `IOptions<T>`-based services?
473. 🟡 How do you test logging (`FakeLogger`)?
474. 🔴 What are Testcontainers and why use them?
475. 🟡 What is the difference between xUnit, NUnit and MSTest? What is `IClassFixture`?
476. 🟡 How do you make `Program` accessible to integration tests with top-level statements?
477. 🔴 How do you test an API for performance and load?
478. 🟡 What is the Arrange-Act-Assert pattern?

---

## 23. Deployment & Hosting

479. 🟢 How do you publish an ASP.NET Core application (`dotnet publish`)?
480. 🟡 How do you host ASP.NET Core on IIS? What must be installed (Hosting Bundle)?
481. 🟡 How do you host ASP.NET Core on Linux with Nginx and systemd?
482. 🟡 How do you run ASP.NET Core in Docker? Explain a multi-stage Dockerfile.
483. 🟡 What is the `ASPNETCORE_ENVIRONMENT` variable?
484. 🟡 What is `ASPNETCORE_URLS` / `ASPNETCORE_HTTP_PORTS`? Which port does the container listen on by default in .NET 8+?
485. 🟡 Why do .NET 8+ container images run as a non-root user by default?
486. 🟡 What is the difference between `aspnet`, `runtime`, `runtime-deps` and chiseled images?
487. 🟡 How do you deploy to Azure App Service?
488. 🟡 What is a zero-downtime deployment? Blue-green vs canary?
489. 🔴 How do you configure Kestrel endpoints and certificates for HTTPS in production?
490. 🔴 How do you handle data protection keys when running multiple instances?

---

## 24. Tricky API Questions

491. 🟡 Why does my `[FromBody]` model come as `null` even though the JSON looks correct?
492. 🟡 Why does my API return 415 Unsupported Media Type?
493. 🟡 Why does my API return 405 Method Not Allowed?
494. 🟡 Why does my API return 404 even though the controller exists?
495. 🟡 Why does my API automatically return 400 without hitting the action?
496. 🟡 Why do CORS errors happen only in the browser and not in Postman?
497. 🟡 Why does a preflight OPTIONS request fail while the actual request would work?
498. 🟡 Why are my JSON property names camelCase when my C# properties are PascalCase?
499. 🟡 Why does my enum appear as a number in the JSON response?
500. 🟡 Why does returning `null` from an action that returns `ActionResult<T>` give 204?
501. 🟡 What happens if two actions have the same route and HTTP verb?
502. 🟡 What happens if you register the same middleware twice?
503. 🟡 What happens if you call `UseRouting()` after `MapControllers()` or forget it?
504. 🟡 Why are changes in `appsettings.json` not reflected in my singleton service?
505. 🟡 Why does my scoped service behave like a singleton?
506. 🟡 Why does a service throw "Cannot consume scoped service from singleton"?
507. 🟡 Why do I get "Unable to resolve service for type X while attempting to activate Y"?
508. 🟡 Why are my response headers not being set ("Headers are read-only, response has already started")?
509. 🟡 Why can I read the request body only once?
510. 🟡 Why does my API hang or time out under load when it works fine locally?
511. 🟡 Why should you never use `async void` in a controller?
512. 🟡 Should a GET endpoint ever change server state? What can go wrong?
513. 🟡 Can a POST be idempotent? Can a GET be non-idempotent?
514. 🟡 Should you return 200 with `{ "success": false }` for errors? Why not?
515. 🟡 Should you return 404 or 200 with an empty list when a search returns no results?
516. 🟡 Should you return 404 or 403 when a user requests a resource they shouldn't know exists?
517. 🟡 Is it OK to put sensitive data in query strings? Why not?
518. 🟡 What is the difference between returning `Ok(null)` and `NoContent()`?
519. 🟡 What happens to an in-flight request when the client disconnects?
520. 🟡 What happens if the client sends a request without a `Content-Type` header?
521. 🟡 How does ASP.NET Core handle trailing slashes in routes?
522. 🟡 Are route parameters case-sensitive?
523. 🟡 What happens if a query string contains the same key twice?
524. 🟡 Why should `DateTime` be avoided in API contracts in favor of `DateTimeOffset`? 💰
525. 🟡💰 Why can sending money amounts as JSON numbers cause problems in JavaScript clients?
526. 🔴 How do you prevent duplicate payments when a client retries a POST after a timeout? 💰
527. 🔴 How do you design an API that must never process the same transaction twice? 💰
528. 🔴 How do you handle the "lost update" problem when two clients update the same resource?
529. 🔴 If your API calls three downstream services and one fails, what do you return?
530. 🔴 How do you return partial success in a bulk API?
531. 🔴 How would you design an API for an operation that takes 10 minutes?
532. 🔴 How do you protect your API from being overloaded by one client?
533. 🔴 How do you handle large response payloads (100k records)?
534. 🔴 What happens if a client sends a 2 GB request body?
535. 🔴 How do you design an API so that adding a new field doesn't break old clients?
536. 🔴 How do you remove a field from a response without breaking clients?
537. 🔴 Your API is fast in isolation but slow in production. What could be the reasons?
538. 🔴 How would you detect and prevent N+1 calls to downstream APIs?
539. 🔴 Can you return different response types from the same endpoint? How would you document it?
540. 🔴 Why is `HttpContext` null in a background thread started from a controller?
541. 🔴 Why does `IHttpContextAccessor.HttpContext` return a different/stale value in async code?
542. 🔴 What is the difference between request timeout, Kestrel timeout, `HttpClient` timeout and load balancer timeout?

---

## 25. Predict the Behavior (Code Snippets)

> What happens when each snippet runs? If it fails, say why.

**543. 🟡 Middleware order**
```csharp
var app = builder.Build();
app.Use(async (ctx, next) => { Console.Write("A1 "); await next(); Console.Write("A2 "); });
app.Use(async (ctx, next) => { Console.Write("B1 "); await next(); Console.Write("B2 "); });
app.Run(async ctx => { Console.Write("C "); await ctx.Response.WriteAsync("done"); });
app.Run();
```

**544. 🟡 `Run` before `Use`**
```csharp
app.Run(async ctx => await ctx.Response.WriteAsync("first"));
app.Use(async (ctx, next) => { await ctx.Response.WriteAsync("second"); await next(); });
```

**545. 🟡 Writing headers after the response starts**
```csharp
app.Use(async (ctx, next) =>
{
    await next();
    ctx.Response.Headers["X-Time"] = DateTime.UtcNow.ToString();
});
app.MapGet("/", () => "hello");
```

**546. 🔴 Captive dependency**
```csharp
builder.Services.AddScoped<IUnitOfWork, UnitOfWork>();
builder.Services.AddSingleton<IReportService, ReportService>(); // ReportService(IUnitOfWork uow)
var app = builder.Build();
```
What happens in Development? What happens in Production?

**547. 🟡 Lifetimes**
```csharp
builder.Services.AddTransient<IIdService, IdService>();   // IdService has Guid Id = Guid.NewGuid()
app.MapGet("/", (IIdService a, IIdService b) => a.Id == b.Id);
```
What is returned? What if it were `AddScoped`? `AddSingleton`?

**548. 🟡 Multiple registrations**
```csharp
builder.Services.AddScoped<INotifier, EmailNotifier>();
builder.Services.AddScoped<INotifier, SmsNotifier>();
// Constructor: public AlertService(INotifier notifier, IEnumerable<INotifier> all)
```
Which implementation is `notifier`? How many items are in `all`?

**549. 🟡 `TryAdd`**
```csharp
builder.Services.AddSingleton<ICache, RedisCache>();
builder.Services.TryAddSingleton<ICache, MemoryCache>();
```
Which implementation is resolved for `ICache`?

**550. 🟡 Two `[FromBody]` parameters**
```csharp
[HttpPost]
public IActionResult Create([FromBody] Order order, [FromBody] Customer customer) => Ok();
```

**551. 🟡 Missing `[ApiController]`**
```csharp
[Route("api/orders")]
public class OrdersController : ControllerBase
{
    [HttpPost]
    public IActionResult Create(OrderDto dto) => Ok(dto);
}
```
A JSON body is sent. What will `dto` contain? What changes if `[ApiController]` is added?

**552. 🟡 Ambiguous routes**
```csharp
[HttpGet("{id}")]   public IActionResult GetById(int id) => Ok();
[HttpGet("{name}")] public IActionResult GetByName(string name) => Ok();
```
What happens on `GET /api/items/5`? How do you fix it?

**553. 🟡 Route constraint**
```csharp
[HttpGet("{id:int}")] public IActionResult Get(int id) => Ok(id);
```
What is returned for `GET /api/items/abc`?

**554. 🟡 Returning null**
```csharp
[HttpGet("{id}")]
public ActionResult<Product> Get(int id) => _repo.Find(id); // returns null
```

**555. 🟡 IOptions vs IOptionsMonitor**
```csharp
builder.Services.Configure<FeatureFlags>(builder.Configuration.GetSection("Features"));
builder.Services.AddSingleton<FlagReader>(); // FlagReader(IOptions<FeatureFlags> opts)
```
`appsettings.json` is edited while the app runs. Does `FlagReader` see the new value? What about `IOptionsSnapshot` and `IOptionsMonitor`?

**556. 🟡 Exception filter vs middleware**
```csharp
app.Use(async (ctx, next) => { throw new Exception("from middleware"); });
// A global exception filter is registered for MVC
```
Will the exception filter handle this exception?

**557. 🟡 CORS order**
```csharp
app.MapControllers();
app.UseCors("AllowFrontend");
```

**558. 🔴 Reading the body twice**
```csharp
app.Use(async (ctx, next) =>
{
    using var reader = new StreamReader(ctx.Request.Body);
    var body = await reader.ReadToEndAsync();
    await next();
});
// controller action uses [FromBody]
```
What does the controller receive?

**559. 🔴 HttpClient misuse**
```csharp
public async Task<string> GetRate()
{
    using var client = new HttpClient();
    return await client.GetStringAsync("https://rates.example.com/usd");
}
```
What happens when this runs 10,000 times per minute?

**560. 🟡 Filter order**
```csharp
// Global filter: LogFilter (Order = 0)
[ServiceFilter(typeof(AuditFilter))]   // controller level
public class PaymentsController : ControllerBase
{
    [TypeFilter(typeof(TimingFilter))]  // action level
    public IActionResult Pay() => Ok();
}
```
In which order do `OnActionExecuting` and `OnActionExecuted` run?

**561. 🔴 Background task with scoped service**
```csharp
[HttpPost]
public IActionResult Start()
{
    _ = Task.Run(async () => await _scopedService.ProcessAsync());
    return Accepted();
}
```

**562. 🟡 Model validation**
```csharp
public class TransferDto
{
    [Required] public int Amount { get; set; }
    [Required] public string? ToAccount { get; set; }
}
```
The client sends `{ "toAccount": "123" }` with no amount. Does validation fail? Why or why not? 💰

---

## 26. Coding & Hands-On Tasks

563. 🟢 Create a CRUD Web API for `Product` using an in-memory list with proper status codes.
564. 🟢 Create an MVC application with a form to add and list employees with validation.
565. 🟡 Write custom middleware that logs request method, path, status code and elapsed time.
566. 🟡 Write middleware that adds and propagates an `X-Correlation-ID` header.
567. 🟡 Implement global exception handling that returns Problem Details using `IExceptionHandler`.
568. 🟡 Write an action filter that measures action execution time.
569. 🟡 Write a custom validation attribute (e.g., `[FutureDate]`, `[ValidIfsc]`).
570. 🟡 Implement pagination, filtering and sorting on a `GET /products` endpoint.
571. 🟡 Implement API versioning with two versions of the same endpoint.
572. 🟡 Configure Swagger/OpenAPI with XML comments and response types.
573. 🟡 Configure the Options pattern with validation for a settings section.
574. 🟡 Register multiple implementations of an interface and select one at runtime (factory or keyed services).
575. 🟡 Implement the Decorator pattern over a service using DI.
576. 🟡 Create a typed `HttpClient` with retry and circuit breaker policies.
577. 🟡 Implement file upload and download endpoints.
578. 🟡 Implement ETag-based caching and `If-None-Match` support.
579. 🟡 Implement output caching for a GET endpoint and invalidate it on update.
580. 🟡 Implement rate limiting for a specific endpoint.
581. 🟡 Write a `BackgroundService` that processes jobs from a `Channel<T>` queue.
582. 🟡 Implement a health check for an external dependency.
583. 🔴 Implement an idempotency-key mechanism for a payment POST endpoint. 💰
584. 🔴 Implement optimistic concurrency on PUT using ETag and `If-Match` (return 412 on mismatch).
585. 🔴 Implement a long-running operation API with 202 Accepted and a status endpoint.
586. 🔴 Implement a custom output formatter that returns CSV.
587. 🔴 Implement a custom model binder (e.g., comma-separated IDs into `int[]`).
588. 🔴 Implement JSON Patch support for partial updates.
589. 🔴 Implement a request/response logging middleware that masks sensitive fields (card number, PAN). 💰
590. 🔴 Build a REST facade over a legacy SOAP service.
591. 🔴 Create a SOAP service with CoreWCF and consume it from a .NET client.
592. 🔴 Write integration tests for an API using `WebApplicationFactory`.
593. 🔴 Implement a webhook receiver with signature validation and retries.
594. 🔴 Stream a large dataset from an API using `IAsyncEnumerable<T>`.

---

## 27. Scenario-Based & Debugging Questions

595. 🟡 Your API works locally but returns 500 in production with no details. How do you investigate?
596. 🟡 After deployment, the API returns 502/503 from IIS. What do you check?
597. 🟡 Your API's response time increases sharply under load. How do you find the bottleneck?
598. 🟡 Memory usage of your API keeps growing. What could cause it in ASP.NET Core?
599. 🟡 Clients report duplicate orders being created. How do you investigate and fix it? 💰
600. 🟡 A third-party API you call is slow and causes your API to time out. What do you do?
601. 🟡 Your configuration values are not loading in a Docker container. What do you check?
602. 🟡 Swagger shows no endpoints. What could be wrong?
603. 🟡 A frontend app gets CORS errors after you deployed to a new domain. How do you fix it?
604. 🟡 Logs from different requests are mixed and hard to trace. How do you fix it?
605. 🟡 Your API is getting "socket exhaustion" errors when calling other services. Why?
606. 🔴 You need to make a breaking change to an API used by 50 clients. How do you roll it out?
607. 🔴 You must migrate a large .NET Framework Web API (with WCF services) to .NET 10. How do you plan it?
608. 🔴 A downstream bank SOAP service frequently times out. How do you make your system resilient? 💰
609. 🔴 Your API must handle 10,000 requests per second. How would you design and tune it?
610. 🔴 A request occasionally gets processed twice due to load balancer retries. How do you prevent it? 💰
611. 🔴 How would you review an ASP.NET Core API pull request? What would you look for?
612. 🔴 How do you design an API that is consumed by mobile apps with poor connectivity?
613. 🔴 How would you introduce caching to a read-heavy API without serving stale financial data? 💰
614. 🔴 Your background service stops processing silently. How do you detect and recover?

---

## 28. Rapid-Fire Round

615. 🟢 What is the default port of Kestrel for HTTP and HTTPS in development?
616. 🟢 Which file contains the app's entry point in .NET 6+?
617. 🟢 What is the default JSON naming policy in ASP.NET Core?
618. 🟢 Which attribute makes a controller an API controller?
619. 🟢 Which base class should Web API controllers inherit from?
620. 🟢 What status code does `CreatedAtAction` return?
621. 🟢 What status code does `NoContent()` return?
622. 🟢 Which HTTP methods are idempotent?
623. 🟢 Which HTTP methods are safe?
624. 🟢 What does `app.Run()` do at the end of `Program.cs`?
625. 🟢 What is the default service lifetime of a controller?
626. 🟢 Is `HttpClient` disposable? Should you dispose it?
627. 🟢 What is the extension of a Razor view file?
628. 🟢 What is the difference between `ViewBag` and `ViewData` in one line?
629. 🟡 Can middleware be async void?
630. 🟡 Can you have multiple `app.Run()` terminal delegates?
631. 🟡 Can you inject `IOptionsSnapshot<T>` into a singleton?
632. 🟡 Can you register a service after `builder.Build()`?
633. 🟡 Can a Minimal API and controllers exist in the same project?
634. 🟡 Can you use `[FromBody]` with a GET request?
635. 🟡 Can a REST API return XML?
636. 🟡 Can SOAP work over something other than HTTP?
637. 🟡 Does `[ResponseCache]` cache responses on the server?
638. 🟡 Does `UseHttpsRedirection` work for APIs called by non-browser clients?
639. 🟡 What is the default request body size limit in Kestrel?
640. 🟡 What is the default lifetime of `HttpMessageHandler` in `IHttpClientFactory`?
641. 🟡 What does `[ApiController]` require for routing?
642. 🟡 Which interface do you implement for a factory-based middleware?
643. 🟡 What does `ValidateOnBuild` check?
644. 🔴 What is the difference between `IStartupFilter` and normal middleware registration?
645. 🔴 What is `IApplicationModelConvention` used for?
646. 🔴 What is the difference between `MapControllers()` and `MapDefaultControllerRoute()`?
647. 🔴 What is `IActionDescriptorCollectionProvider` used for?
648. 🔴 What is `ProblemDetailsFactory`?

---

> **Next part (optional):** EF Core, Microservices, Authentication/Authorization.
