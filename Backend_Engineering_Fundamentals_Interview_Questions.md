# 🎯 Backend Engineering & Distributed Systems Fundamentals — Part 9 (Questions Only)

> **Source:** Built from your report *"Comprehensive Backend Development Architecture & Distributed Systems Engineering"* (generated from your NotebookLM YouTube transcripts), expanded with the related fundamentals interviewers ask around each topic.
> **Scope:** Language-agnostic and database-agnostic software engineering fundamentals — how the web works, HTTP, routing, serialization & validation, authentication & authorization, OAuth/OIDC, security vulnerabilities, layered architecture, middleware, REST & OpenAPI, databases & indexing, caching, search, object storage, background jobs, real-time communication, webhooks, fault tolerance, configuration & secrets, observability, graceful shutdown, performance, concurrency models, scaling, testing, Twelve-Factor App, DevOps & CI/CD, SLIs/SLOs/SLAs.
> **Applies to any stack:** .NET, Java, Go, Node.js, Python, Rust.

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

1. Backend Engineering Foundations
2. How a Request Reaches the Server (DNS, TCP, TLS, Proxies)
3. Browser Runtime vs Server Runtime
4. HTTP Fundamentals & Statelessness
5. HTTP Headers
6. HTTP/1.1 vs HTTP/2 vs HTTP/3
7. Content Negotiation & HTTP Caching
8. HTTP Status Codes
9. Routing, URIs & API Versioning
10. Serialization, Deserialization & Validation Pipelines
11. Authentication vs Authorization
12. Stateful Sessions vs Stateless JWTs
13. Cookies & Cookie Security
14. OAuth 2.0 & OpenID Connect
15. Backend Security — SQL Injection, Password Hashing, BOLA, BFLA
16. Layered Architecture (Controller, Service, Repository)
17. Middleware & Request Context
18. CORS
19. REST API Design & Idempotency
20. Contract-First Design & OpenAPI
21. Relational Databases, Data Types & ACID
22. Indexing & Query Analysis
23. Caching with Redis
24. Full-Text Search & Inverted Indexes
25. Object Storage, Pre-Signed URLs & Large Files
26. Background Jobs & Task Queues
27. Real-Time Communication (Polling, Long Polling, SSE, WebSockets)
28. Webhooks & the Transactional Outbox
29. Fault Tolerance & Error Handling
30. Configuration Management & Secrets
31. Observability — Logs, Metrics, Traces
32. Process Lifecycle & Graceful Shutdown
33. Performance Engineering
34. Concurrency vs Parallelism & Runtime Models
35. Scaling — Vertical, Horizontal & Load Balancing
36. Database Scaling — Connection Pooling, Read Replicas, Sharding
37. Testing Strategies & Testcontainers
38. Twelve-Factor App
39. DevOps, Containers & CI/CD
40. Deployment Strategies & Reliability (SLI, SLO, SLA)
41. Tricky Questions
42. Predict the Behavior
43. Scenario-Based Questions
44. System Design Questions
45. Hands-On Tasks (Any Language)
46. Rapid-Fire Round

---

## 1. Backend Engineering Foundations

1. 🟢 What is backend engineering? What responsibilities does a backend have?
2. 🟢 What is a server process? What does it mean for a server to "listen on a port"?
3. 🟢 What are ports 80 and 443 used for? What is the difference between a port and an IP address?
4. 🟢 What is the difference between frontend and backend?
5. 🟢 What are the fundamental problems every backend must solve regardless of language (state, network, durability, security, concurrency)?
6. 🟡 Why should you learn backend concepts from first principles instead of a specific framework?
7. 🟡 What is the difference between a library and a framework?
8. 🟡 What is a runtime? Compare the runtimes of compiled languages (Go, Rust), VM languages (Java, .NET) and interpreted languages (Python, Node.js).
9. 🟡 What does a typical production backend stack look like (proxy, app servers, database, cache, queue, object storage, search, observability)?
10. 🔴 How would you explain the full architecture of your current project from client to database?

---

## 2. How a Request Reaches the Server

11. 🟢 What happens when you type a URL into the browser and press Enter? (Explain step by step.)
12. 🟢 What is DNS? How does DNS resolution work (browser cache, OS cache, resolver, root, TLD, authoritative server)?
13. 🟡 What are DNS record types (A, AAAA, CNAME, MX, TXT, NS)?
14. 🟡 What is TTL in DNS? Why do DNS changes take time to propagate?
15. 🟢 What is TCP? What is the TCP three-way handshake?
16. 🟢 What is the difference between TCP and UDP?
17. 🟡 What is TLS? What happens during a TLS handshake?
18. 🟡 What is the OSI model? At which layers do HTTP, TLS, TCP and IP operate?
19. 🟢 What is a firewall?
20. 🟢 What is a load balancer?
21. 🟢 What is a reverse proxy (Nginx, Caddy)? Why is it placed in front of application servers?
22. 🟡 What is the difference between a forward proxy and a reverse proxy?
23. 🟡 What is an ingress?
24. 🟡 What is a CDN and how does it reduce latency?
25. 🔴 Where can latency be added in the request path, and how do you measure each part?

---

## 3. Browser Runtime vs Server Runtime

26. 🟢 What is the difference between a browser runtime and a server runtime?
27. 🟡 What is the browser sandbox? What can't browser JavaScript do?
28. 🟡 What is the Same-Origin Policy? What counts as the same origin (scheme, host, port)?
29. 🟡 Why can't a browser connect directly to a database?
30. 🟡 Why must secrets never be shipped to frontend code?
31. 🟡 What is the DOM? Is JavaScript in the browser single-threaded?
32. 🔴 Which validations must always be repeated on the server even if the frontend validates?

---

## 4. HTTP Fundamentals & Statelessness

33. 🟢 What is HTTP?
34. 🟢 What does it mean that HTTP is stateless?
35. 🟢 If HTTP is stateless, how do applications remember logged-in users?
36. 🟢 What are the parts of an HTTP request (method, URI, headers, body)?
37. 🟢 What are the parts of an HTTP response (status line, headers, body)?
38. 🟢 What are HTTP methods? Explain GET, POST, PUT, PATCH, DELETE, HEAD and OPTIONS.
39. 🟡 What is the difference between HTTP and HTTPS?
40. 🟡 What is keep-alive (persistent connections)? Why does it improve performance?
41. 🟡 Can a GET request have a body? Should it?
42. 🟡 What is the difference between a URI, URL and URN?

---

## 5. HTTP Headers

43. 🟢 What are HTTP headers?
44. 🟡 What are general headers, representation headers and security headers?
45. 🟢 What do `Content-Type`, `Content-Length` and `Content-Encoding` mean?
46. 🟡 What is the difference between `application/json`, `application/x-www-form-urlencoded` and `multipart/form-data`? When do you use each?
47. 🟡 What do `Accept`, `Accept-Language` and `Accept-Encoding` do?
48. 🟡 What is the `Authorization` header? What is a bearer token?
49. 🟡 What does `Strict-Transport-Security` (HSTS) do?
50. 🟡 What does `Content-Security-Policy` (CSP) do?
51. 🟡 What do `X-Frame-Options` and `X-Content-Type-Options` protect against?
52. 🟡 What is the `Location` header and when is it returned?
53. 🟡 What are custom headers (`X-Request-Id`, `X-API-Version`)? Should custom headers be prefixed with `X-`?
54. 🔴 Which headers should a reverse proxy add or forward to the application (`X-Forwarded-For`, `X-Forwarded-Proto`, `Host`)?

---

## 6. HTTP/1.1 vs HTTP/2 vs HTTP/3

55. 🟡 What are the main differences between HTTP/1.1, HTTP/2 and HTTP/3?
56. 🟡 What is head-of-line blocking? At which layer does it occur in HTTP/1.1 and HTTP/2?
57. 🟡 Why did browsers open multiple TCP connections per domain with HTTP/1.1?
58. 🟡 What is multiplexing in HTTP/2?
59. 🟡 What is HPACK header compression?
60. 🟡 What is HTTP/2 server push? Why was it largely abandoned?
61. 🟡 What is QUIC? Why does HTTP/3 use UDP instead of TCP?
62. 🟡 What are 0-RTT and 1-RTT connection establishment?
63. 🟡 What is connection migration in HTTP/3 and why does it help mobile users?
64. 🔴 Does upgrading to HTTP/2 or HTTP/3 always improve performance? When might it not?

---

## 7. Content Negotiation & HTTP Caching

65. 🟢 What is content negotiation?
66. 🟡 What should a server return if it can't produce the format the client asked for (406)?
67. 🟢 What is HTTP caching? Why is it important?
68. 🟡 What do the `Cache-Control` directives `max-age`, `no-cache`, `no-store`, `private` and `public` mean?
69. 🟡 What is the difference between `no-cache` and `no-store`?
70. 🟡 What is an ETag? What is `Last-Modified`?
71. 🟡 What are conditional requests (`If-None-Match`, `If-Modified-Since`)?
72. 🟡 What does `304 Not Modified` mean and why does it save bandwidth?
73. 🟡 What is a strong vs weak ETag (`W/"..."`)?
74. 🟡 What is browser cache vs CDN cache vs proxy cache?
75. 🔴 How do you safely cache authenticated or user-specific API responses? 💰
76. 🔴 How do you invalidate HTTP caches when data changes?
77. 🔴 How can ETags and `If-Match` be used for optimistic concurrency (412 Precondition Failed)?

---

## 8. HTTP Status Codes

78. 🟢 What are the five classes of HTTP status codes?
79. 🟢 What is `100 Continue`? What is `101 Switching Protocols`?
80. 🟢 What is the difference between 200, 201 and 204?
81. 🟢 When should a POST return 201 and what header should accompany it?
82. 🟢 What is the difference between 301 and 302 redirects? What about 307 and 308?
83. 🟢 What is the difference between 400 and 422?
84. 🟢 What is the difference between 401 and 403?
85. 🟢 When do you return 404 vs 405?
86. 🟢 When do you return 409 Conflict?
87. 🟢 What is 429 Too Many Requests? What header should accompany it (`Retry-After`)?
88. 🟢 What is the difference between 500 and 501?
89. 🟡 What is the difference between 502, 503 and 504?
90. 🟡 When should you return 202 Accepted?
91. 🟡 Should you return 404 or 403 when a user requests a resource they are not allowed to see?
92. 🟡 Why is returning `200 OK` with `{ "success": false }` a bad practice?
93. 🟡 What should a standard error response body contain (error code, message, details, request ID)?

---

## 9. Routing, URIs & API Versioning

94. 🟢 What is routing?
95. 🟢 What is the difference between static routes and dynamic routes?
96. 🟢 What is the difference between path parameters and query parameters? When do you use each?
97. 🟡 How should nested resources be modeled (`/organizations/:orgId/projects/:projectId/tasks`)? How deep should nesting go?
98. 🟡 What is a catch-all / fallback route and why should it return a standard JSON 404?
99. 🟡 How does a router choose between overlapping routes?
100. 🟢 Why is API versioning needed?
101. 🟡 What are the versioning strategies (path, media type, custom header, query string)? Pros and cons of each?
102. 🟡 Why is path-based versioning popular?
103. 🟡 What are breaking vs non-breaking API changes?
104. 🟡 How do you deprecate an API version? What are the `Deprecation` and `Sunset` headers?
105. 🔴 How do you support two API versions at the same time without duplicating all the code?

---

## 10. Serialization, Deserialization & Validation Pipelines

106. 🟢 What is serialization? What is deserialization?
107. 🟢 Why is JSON the most common format for APIs?
108. 🟡 What other serialization formats exist (XML, Protocol Buffers, Avro, MessagePack)? When are they better than JSON?
109. 🟡 What is the performance cost of serialization and deserialization?
110. 🟡 How do strongly typed languages and dynamic languages differ in deserializing JSON?
111. 🟢 Why must incoming data be validated?
112. 🟡 What is syntactic validation? Give examples (email format, E.164 phone numbers, ISO 8601 dates).
113. 🟡 What is semantic validation? Give examples (date of birth not in the future, checkout after check-in, withdrawal within limits). 💰
114. 🟡 What is type validation? Why is `"5"` not the same as `5`?
115. 🟡 What is transformation and sanitization (trimming, lowercasing emails, default values, stripping HTML)?
116. 🟡 In what order should validation and transformation happen?
117. 🟡 Where should validation live — controller, service, database, or all of them?
118. 🟡 What is the difference between validation errors (400/422) and business rule errors (409)?
119. 🔴 Why can trusting client-side validation alone lead to security vulnerabilities?
120. 🔴 What is mass assignment / over-posting and how does strict deserialization prevent it?
121. 🔴 How do you handle precision for money and large numbers in JSON (e.g., sending amounts as strings or minor units)? 💰

---

## 11. Authentication vs Authorization

122. 🟢 What is authentication?
123. 🟢 What is authorization?
124. 🟢 What is the difference between authentication and authorization? Which comes first?
125. 🟡 What is Role-Based Access Control (RBAC)?
126. 🟡 What is Attribute-Based Access Control (ABAC)?
127. 🟡 What is the principle of least privilege?
128. 🟡 What is a "default deny" policy?
129. 🟡 What is multi-factor authentication?

---

## 12. Stateful Sessions vs Stateless JWTs

130. 🟢 How does session-based (stateful) authentication work?
131. 🟢 What is a session ID? How should it be generated?
132. 🟡 Where are sessions stored (memory, Redis, database)? Why is in-process memory a problem when scaling horizontally?
133. 🟡 What session metadata is commonly stored (user ID, created time, IP, user-agent)?
134. 🟢 How does token-based (stateless) authentication with JWT work?
135. 🟢 What are the three parts of a JWT?
136. 🟢 Is a JWT encrypted? Who can read its payload?
137. 🟡 What are standard JWT claims (`sub`, `iat`, `exp`, `iss`, `aud`, `nbf`, `jti`)?
138. 🟡 What is the difference between HS256 (symmetric) and RS256 (asymmetric) signing? When would you use each?
139. 🟡 How does a server verify a JWT?
140. 🟡 What are the pros and cons of sessions vs JWTs?
141. 🟡 Why is revoking a JWT before it expires difficult?
142. 🟡 How do short-lived access tokens + refresh tokens solve revocation?
143. 🟡 What is a token blacklist / denylist and what does it cost?
144. 🔴 What happens if a JWT signing secret is leaked?
145. 🔴 Why shouldn't sensitive data be stored in a JWT payload? 💰
146. 🔴 How do you log a user out from all devices with sessions vs JWTs?

---

## 13. Cookies & Cookie Security

147. 🟢 What is a cookie? How is it set (`Set-Cookie`) and sent back?
148. 🟢 What does the `HttpOnly` flag do? Which attack does it mitigate?
149. 🟢 What does the `Secure` flag do?
150. 🟡 What does `SameSite` do? Explain `Strict`, `Lax` and `None`.
151. 🟡 Why must `SameSite=None` be used together with `Secure`?
152. 🟡 What are `Domain`, `Path`, `Expires` and `Max-Age` cookie attributes?
153. 🟡 What is XSS? How can it steal tokens?
154. 🟡 What is CSRF? How do cookies make CSRF possible? How do you prevent it?
155. 🔴 Where should tokens be stored in a browser — cookie, localStorage, sessionStorage or memory? Defend your answer.

---

## 14. OAuth 2.0 & OpenID Connect

156. 🟢 What is OAuth 2.0? What problem does it solve?
157. 🟢 Is OAuth 2.0 authentication or authorization?
158. 🟢 What is OpenID Connect? How does it extend OAuth 2.0?
159. 🟢 What is an ID token? How is it different from an access token?
160. 🟡 What are the four OAuth roles (resource owner, client, authorization server, resource server)?
161. 🟡 Explain the Authorization Code flow with PKCE step by step.
162. 🟡 What are `code_verifier` and `code_challenge`? What attack does PKCE prevent?
163. 🟡 What is the Client Credentials flow? When is it used?
164. 🟡 What is the Device Authorization Grant? Give an example.
165. 🟡 What are scopes?
166. 🟡 Why are the Implicit flow and Password grant discouraged?
167. 🟡 What is the `state` parameter used for?
168. 🔴 Which flow would you use for a single-page app, a mobile app, a server-rendered web app, a background job, and a smart TV?
169. 🔴 What is "Login with Google"? Walk through what happens behind the scenes.

---

## 15. Backend Security — SQL Injection, Password Hashing, BOLA, BFLA

170. 🟢 What is SQL injection? Give an example.
171. 🟢 What is the definitive defense against SQL injection?
172. 🟡 How do parameterized queries / prepared statements separate code from data?
173. 🟡 Can ORMs still be vulnerable to SQL injection? When?
174. 🟡 Can you parameterize table or column names? How do you handle dynamic sorting safely?
175. 🟢 Why must passwords never be stored in plain text or with reversible encryption?
176. 🟢 What is the difference between hashing, encryption and encoding?
177. 🟡 Why are fast hashes like MD5 or SHA-256 not suitable for passwords?
178. 🟡 What are Argon2id and bcrypt? Why are they recommended?
179. 🟡 What is a salt? Why must every password have a unique salt?
180. 🟡 What is a rainbow table attack?
181. 🟡 What is a work factor / cost factor? Why target ~250–500 ms per hash?
182. 🟡 What is a pepper?
183. 🟡 What is BOLA / IDOR? Give an example with `/api/v1/invoices/1052`. 💰
184. 🟡 How do you prevent BOLA at the repository layer (`WHERE id = ? AND user_id = ?`)?
185. 🟡 What is BFLA (Broken Function Level Authorization)?
186. 🟡 Why is hiding admin buttons in the UI not security?
187. 🟡 Why must error messages never expose stack traces, SQL, schema details or file paths?
188. 🟡 Do UUIDs instead of sequential IDs prevent BOLA? Why or why not?
189. 🟡 What is the OWASP Top 10? What is the OWASP API Security Top 10?
190. 🟡 What is rate limiting's role in security (brute force, credential stuffing)?
191. 🔴 What are XSS, SSRF, path traversal and command injection? How do you prevent each?
192. 🔴 What is account enumeration and how do you prevent it on login and password reset?
193. 🔴 How do you design security in layers (defense in depth) for a public API? 💰

---

## 16. Layered Architecture (Controller, Service, Repository)

194. 🟢 What is layered (three-tier) application architecture?
195. 🟢 What is the responsibility of the controller/handler layer?
196. 🟢 What is the responsibility of the service layer?
197. 🟢 What is the responsibility of the repository/data access layer?
198. 🟡 Why should controllers contain no business logic or database queries?
199. 🟡 Why should the service layer not know about HTTP status codes or request objects?
200. 🟡 Can a service call multiple repositories? Can a repository call a service?
201. 🟡 Where should transactions be started and committed — controller, service or repository?
202. 🟡 What are DTOs vs domain models vs database entities?
203. 🟡 How does layering make unit testing easier?
204. 🟡 What is separation of concerns? What is tight vs loose coupling?
205. 🟡 What is clean architecture / hexagonal architecture (ports and adapters)? How is it related to layering?
206. 🔴 What are the disadvantages of strict layering (too much boilerplate, anemic domain models)?
207. 🔴 Where would you put logic that sends an email after an order is placed?

---

## 17. Middleware & Request Context

208. 🟢 What is middleware?
209. 🟢 What does calling `next()` do? What happens if middleware doesn't call it (short-circuit)?
210. 🟢 What are cross-cutting concerns? Give examples (logging, auth, CORS, rate limiting, error handling).
211. 🟡 What is the correct order of middleware (CORS → logging/tracing → rate limiting → authentication → handler, with a global error handler wrapping everything)? Why?
212. 🟡 Why should CORS run first?
213. 🟡 Why should rate limiting run before expensive authentication or business logic?
214. 🟡 What does a global error handling middleware do?
215. 🟡 What is request context? What data does it carry (user ID, roles, request ID, client IP, deadlines/cancellation)?
216. 🟡 Why is request context better than global variables?
217. 🟡 What is a request ID / correlation ID and why should every log line include it?
218. 🔴 How are timeouts and cancellation propagated through request context to database and HTTP calls?
219. 🔴 What happens if middleware modifies the response after the response has already started?

---

## 18. CORS

220. 🟢 What is CORS? Why does it exist?
221. 🟢 Is CORS enforced by the browser or the server?
222. 🟡 What is a preflight `OPTIONS` request? When does the browser send one?
223. 🟡 What are simple requests vs preflighted requests?
224. 🟡 What do `Access-Control-Allow-Origin`, `Access-Control-Allow-Methods`, `Access-Control-Allow-Headers` and `Access-Control-Max-Age` do?
225. 🟡 What is `Access-Control-Allow-Credentials` and why can't it be used with `*`?
226. 🟡 Why does a request work in Postman/curl but fail in the browser with a CORS error?
227. 🔴 Does CORS protect your API from attackers? Why not?

---

## 19. REST API Design & Idempotency

228. 🟢 What is REST? Who defined it?
229. 🟢 What are the six REST constraints?
230. 🟢 What is a resource?
231. 🟢 Which HTTP method should be used for create, read, full update, partial update and delete?
232. 🟢 What is the difference between PUT and PATCH?
233. 🟢 What is the difference between PUT and POST?
234. 🟢 What does "safe" mean for an HTTP method? Which methods are safe?
235. 🟢 What does "idempotent" mean? Which methods are idempotent?
236. 🟡 Why is POST not idempotent?
237. 🟡 Is PATCH idempotent? When is it and when isn't it?
238. 🟡 Is DELETE idempotent if the second call returns 404?
239. 🟡 What are REST URI naming conventions (plural nouns, kebab-case, no verbs)?
240. 🟡 How do you model non-CRUD actions (`POST /invoices/102/archive`, `POST /users/45/reset-password`)?
241. 🟡 How do you design filtering, sorting and pagination?
242. 🟡 Offset pagination vs cursor-based pagination — pros and cons?
243. 🟡 What is HATEOAS?
244. 🔴 How do you make a POST endpoint idempotent using an idempotency key? 💰
245. 🔴 How do you design bulk operations in REST?
246. 🔴 How do you design an API for a long-running operation (202 + status endpoint)?
247. 🔴 REST vs GraphQL vs gRPC — when do you choose each?

---

## 20. Contract-First Design & OpenAPI

248. 🟢 What is the OpenAPI Specification? What is Swagger?
249. 🟡 What is code-first vs contract-first API design? Pros and cons?
250. 🟡 Why does contract-first allow frontend and backend teams to work in parallel?
251. 🟡 What does an OpenAPI document describe (servers, paths, parameters, request bodies, responses, schemas, security schemes)?
252. 🟡 What are `components/schemas` and `$ref` used for?
253. 🟡 How can mock servers (e.g., Prism) be generated from a contract?
254. 🟡 How can client SDKs and server interfaces be generated from OpenAPI?
255. 🟡 What is contract/fuzz testing against an OpenAPI spec (e.g., Schemathesis)?
256. 🟡 What tools render API documentation (Swagger UI, Scalar, ReDoc)?
257. 🔴 How do you detect breaking changes between two versions of an OpenAPI contract in CI?

---

## 21. Relational Databases, Data Types & ACID

258. 🟢 Why are databases stored on disk instead of only in memory?
259. 🟢 What is ACID? Explain each property.
260. 🟢 What is a schema? What are foreign keys and why do they matter?
261. 🟡 Why is `TIMESTAMP WITH TIME ZONE` / storing UTC important in distributed systems?
262. 🟡 What are the pros and cons of UUID primary keys vs auto-increment integers?
263. 🟡 Why can random UUIDs hurt index performance? What are time-ordered UUIDs (UUIDv7)?
264. 🟡 In PostgreSQL, is `VARCHAR(255)` faster than `TEXT`? How should you enforce length?
265. 🟡 What is the difference between JSON and JSONB storage? When should you store JSON in a relational database?
266. 🟡 When is storing an array in a column better than a junction table? When is it worse?
267. 🟡 What are database triggers? Give an example (auto-updating `updated_at`).
268. 🟡 What is a transaction? What is a transaction isolation level?
269. 🔴 Relational vs NoSQL — how do you choose for a new system?

---

## 22. Indexing & Query Analysis

270. 🟢 What is a sequential (full table) scan? Why does it become slow?
271. 🟢 What is an index? What data structure do most indexes use?
272. 🟡 Why does a B-tree turn an O(N) search into O(log N)?
273. 🟡 What does an index store (key values + pointers to rows / tuple IDs)?
274. 🟡 Which columns should you index (primary keys, foreign keys used in joins, frequently filtered columns)?
275. 🟡 What is a composite index? What is the left-prefix rule?
276. 🟡 For an index on `(user_id, status)`, which queries can use it?
277. 🟡 What is a covering index (`INCLUDE`)? What is an index-only scan?
278. 🟡 What is the cost of indexes on writes?
279. 🟡 What does `EXPLAIN ANALYZE` show?
280. 🟡 What is the difference between Seq Scan, Index Scan and Bitmap Heap Scan?
281. 🔴 When will the database ignore an index even though one exists?
282. 🔴 How do you decide whether adding an index is worth it?

---

## 23. Caching with Redis

283. 🟢 What is caching? Why does it improve performance?
284. 🟢 What is Redis? Why is it fast?
285. 🟢 What is the difference in access speed between RAM and disk?
286. 🟡 Is Redis single-threaded? Why is that not a bottleneck for most workloads?
287. 🟢 What is a cache hit and a cache miss?
288. 🟡 What is cache-aside (lazy caching)? Walk through a read.
289. 🟡 What is write-through caching? Pros and cons?
290. 🟡 What is write-behind (write-back) caching? What is the risk?
291. 🟡 What is TTL? How do you choose a TTL?
292. 🟡 What are Redis eviction policies (`noeviction`, `allkeys-lru`, `volatile-lru`, `allkeys-lfu`, `volatile-ttl`)?
293. 🟡 What is the difference between LRU and LFU?
294. 🟡 What are common Redis use cases (query caching, sessions, rate limiting, counters, leaderboards, pub/sub, distributed locks)?
295. 🟡 What is cache invalidation? Why is it called one of the hardest problems in computer science?
296. 🔴 What is a cache stampede / thundering herd? How do you prevent it?
297. 🔴 What is cache penetration (requests for keys that don't exist) and how do you prevent it?
298. 🔴 What happens to your system if Redis goes down? How do you design for it?
299. 🔴 What data should never be cached, or cached only with care? 💰
300. 🔴 How do you keep the cache and the database consistent when updating data?

---

## 24. Full-Text Search & Inverted Indexes

301. 🟢 Why is `WHERE title ILIKE '%keyword%'` slow on large tables?
302. 🟡 What are the limitations of SQL pattern matching for search (no relevance, no typo tolerance)?
303. 🟡 What is Elasticsearch? What is Apache Lucene?
304. 🟡 What is an inverted index? How does it work?
305. 🟡 What is tokenization, lowercasing and stemming?
306. 🟡 What is relevance scoring? What is BM25 (term frequency, inverse document frequency)?
307. 🟡 What is fuzzy matching? What is Levenshtein distance?
308. 🟡 What is the ELK stack?
309. 🔴 How do you keep a search index in sync with the primary database (dual writes, CDC, events)?
310. 🔴 When would you use database full-text search instead of Elasticsearch?

---

## 25. Object Storage, Pre-Signed URLs & Large Files

311. 🟢 Why shouldn't user uploads be stored on the application server's local disk?
312. 🟢 What is object storage (AWS S3, Azure Blob, GCS)?
313. 🟡 How is object storage different from a file system and a database?
314. 🟡 What are the data plane and the metadata plane in S3-like systems?
315. 🟡 What is a hot partition in object storage keys? How do random prefixes help?
316. 🟡 Why shouldn't large uploads be proxied through the application server?
317. 🟡 What is a pre-signed URL? Walk through the upload flow.
318. 🟡 How is a pre-signed URL secured (HMAC signature, expiry, permissions)?
319. 🟡 What is a multipart upload? When should you use it?
320. 🟡 What are HTTP range requests? How do they enable video seeking and resumable downloads?
321. 🔴 How do you validate an uploaded file (size, type, virus scan) when it goes directly to object storage?
322. 🔴 How do you serve private files securely to authorized users only? 💰

---

## 26. Background Jobs & Task Queues

323. 🟢 Why shouldn't slow operations (PDF generation, video encoding, emails) run inside the HTTP request?
324. 🟢 What is a background job / task queue?
325. 🟢 What is a message broker? Name examples (Redis, RabbitMQ, AWS SQS, Kafka).
326. 🟢 What is a worker?
327. 🟡 Why should the API return `202 Accepted` with a job ID?
328. 🟡 How does the client find out when the job is done (polling a status endpoint, webhooks, WebSockets, SSE)?
329. 🟡 What is a visibility timeout?
330. 🟡 What happens if a worker crashes before acknowledging a job?
331. 🟡 What is acknowledgement (ACK)?
332. 🟡 What are retries with exponential backoff and jitter? Why add jitter?
333. 🟡 What is a dead letter queue?
334. 🟡 What does at-least-once delivery mean? Why does it require idempotent jobs?
335. 🟡 How do you make a job idempotent (tracking processed job IDs)?
336. 🟡 What are scheduled/cron jobs? How do you prevent a cron job from running twice on multiple servers?
337. 🔴 How do you prioritise jobs (priority queues)?
338. 🔴 How do you scale workers and prevent them from overwhelming the database?
339. 🔴 How do you monitor queues (queue depth, processing time, failure rate)?

---

## 27. Real-Time Communication

340. 🟢 Why can't plain HTTP push data from server to client?
341. 🟢 What is short polling? What are its drawbacks?
342. 🟢 What is long polling? How is it different from short polling?
343. 🟡 What are Server-Sent Events (SSE)? How do they work?
344. 🟡 What headers are used for SSE (`Accept: text/event-stream`)?
345. 🟡 How does SSE reconnect automatically (`Last-Event-ID`)?
346. 🟡 What are WebSockets? How is the connection upgraded (`Upgrade: websocket`, `101 Switching Protocols`)?
347. 🟡 What does full-duplex mean?
348. 🟡 SSE vs WebSockets vs long polling — when do you choose each?
349. 🟡 Give use cases for each (notifications, live dashboards, chat, multiplayer games, stock tickers).
350. 🔴 How do you scale WebSockets across multiple server instances (Redis Pub/Sub, Kafka)?
351. 🔴 Why do WebSockets complicate load balancing (sticky sessions, long-lived connections)?
352. 🔴 How do you authenticate WebSocket connections?
353. 🔴 How do you handle reconnection and missed messages?

---

## 28. Webhooks & the Transactional Outbox

354. 🟢 What is a webhook? How is it different from polling an API?
355. 🟢 Give a real example of a webhook (payment provider notifying payment success). 💰
356. 🟡 Why must webhook requests be verified?
357. 🟡 How does HMAC signature verification work for webhooks?
358. 🟡 Why must the signature be computed over the raw request body before JSON parsing?
359. 🟡 What is a replay attack? How do timestamps in the signature prevent it?
360. 🟡 Why must webhook processing be idempotent? How do you use the event/delivery ID?
361. 🟡 Why should a webhook receiver respond quickly and process the work asynchronously?
362. 🟡 What happens if your webhook endpoint is down when the provider sends an event?
363. 🟡 Why is calling an external API inside a database transaction dangerous?
364. 🟡 What is the Transactional Outbox pattern? Walk through it.
365. 🟡 What does the outbox worker do? How does it handle retries?
366. 🔴 How do you design an outbound webhook system for your own customers (registration, signing, retries, backoff, disabling failing endpoints, delivery logs)?
367. 🔴 How do you handle events arriving out of order? 💰

---

## 29. Fault Tolerance & Error Handling

368. 🟢 What is fault tolerance?
369. 🟢 What are recoverable errors vs non-recoverable errors? Give examples of each.
370. 🟡 How do you handle recoverable errors (validation feedback, retries, fallbacks)?
371. 🟡 What should happen when a non-recoverable error occurs in one request?
372. 🟡 Why must one failing request never crash the whole process?
373. 🟡 What is a cascading failure? How do you prevent it?
374. 🟡 What is a timeout? Why must every network call have one?
375. 🟡 What is a retry? When is retrying harmful?
376. 🟡 What is a circuit breaker?
377. 🟡 What is a bulkhead?
378. 🟡 What is a fallback / graceful degradation?
379. 🔴 Which errors should be retried and which should not?
380. 🔴 What is a retry storm and how do you prevent it?

---

## 30. Configuration Management & Secrets

381. 🟢 Why must configuration be separated from code?
382. 🟢 What is the difference between non-sensitive configuration and secrets?
383. 🟢 Why must secrets never be committed to Git?
384. 🟡 What are environment variables? Why are they used for configuration?
385. 🟡 What are secret managers (AWS Secrets Manager, Parameter Store, HashiCorp Vault, Azure Key Vault)?
386. 🟡 What is the principle of least privilege for secrets?
387. 🟡 What is startup validation of configuration?
388. 🟡 What is the fail-fast principle? Why is crashing at startup better than failing later?
389. 🟡 How do you manage different configs for local, staging and production?
390. 🔴 How do you rotate secrets without downtime?
391. 🔴 What do you do if a secret is accidentally committed to a public repository?

---

## 31. Observability — Logs, Metrics, Traces

392. 🟢 What is the difference between monitoring and observability?
393. 🟢 What are the three pillars of observability?
394. 🟢 What is structured logging? Why is JSON logging better than plain text?
395. 🟡 What fields should every log entry contain (timestamp, level, message, request ID, user ID, duration)?
396. 🟡 What are log levels (DEBUG, INFO, WARN, ERROR, FATAL)? Which should be enabled in production?
397. 🟡 What should never be logged (passwords, tokens, card numbers, PII)? 💰
398. 🟡 What are log collectors and log platforms (Fluentd, Logstash, Loki, Elasticsearch, Datadog)?
399. 🟢 What are metrics? How are they different from logs?
400. 🟡 What are the four golden signals (latency, traffic, errors, saturation)?
401. 🟡 What are counters, gauges and histograms?
402. 🟡 How does Prometheus collect metrics (scraping `/metrics`)?
403. 🟢 What is distributed tracing?
404. 🟡 What are traces, spans, trace IDs and span IDs?
405. 🟡 What is OpenTelemetry?
406. 🟡 What is the `traceparent` header (W3C Trace Context)?
407. 🟡 How do traces help find latency bottlenecks across services?
408. 🟡 What are Jaeger and Zipkin?
409. 🔴 How do you connect logs, metrics and traces for one request?
410. 🔴 How do you design alerts that are useful and avoid alert fatigue?

---

## 32. Process Lifecycle & Graceful Shutdown

411. 🟢 What is graceful shutdown?
412. 🟢 What are SIGTERM and SIGKILL? What is the difference?
413. 🟡 When does an orchestrator (Kubernetes, Docker) send SIGTERM?
414. 🟡 What are the steps of a graceful shutdown (stop accepting connections, drain in-flight requests, finish jobs, flush logs, close DB/Redis pools, exit 0)?
415. 🟡 What is a grace period? What happens if it's exceeded?
416. 🟡 What happens to in-flight requests if the process is killed abruptly?
417. 🟡 What happens to a background job if the worker is killed mid-job?
418. 🔴 How do load balancers and health checks work together during shutdown (readiness failing first)?
419. 🔴 What is the difference between liveness and readiness health checks?

---

## 33. Performance Engineering

420. 🟢 What is the difference between throughput and latency?
421. 🟢 What are RPS and QPS?
422. 🟡 Why should latency be measured with percentiles (P50, P95, P99) instead of averages?
423. 🟡 What does it mean if P50 is 20 ms but P99 is 5 seconds?
424. 🟡 What is premature optimization? Why should you measure before optimizing?
425. 🟡 What is profiling?
426. 🟢 What is the N+1 query problem? Give an example.
427. 🟡 How do you fix N+1 queries (joins, `WHERE id IN (...)`, eager loading, batching)?
428. 🟡 What is serialized (sequential) I/O blocking? How do concurrent calls reduce latency?
429. 🟡 Why are huge response payloads slow? How does pagination help?
430. 🟡 What is load testing? Stress testing? Soak testing?
431. 🟡 What is a bottleneck? How do you find one?
432. 🔴 What is tail latency and why does it matter in distributed systems with many service calls?
433. 🔴 What is Little's Law and how can it help with capacity planning?
434. 🔴 How do you approach a "the API is slow" complaint end to end?

---

## 34. Concurrency vs Parallelism & Runtime Models

435. 🟢 What is concurrency?
436. 🟢 What is parallelism?
437. 🟢 What is the difference between concurrency and parallelism? Can you have one without the other?
438. 🟢 What are I/O-bound and CPU-bound workloads? Give examples of each.
439. 🟡 What is a process vs a thread?
440. 🟡 What is context switching and why is it expensive?
441. 🟡 What is blocking vs non-blocking I/O?
442. 🟡 What is synchronous vs asynchronous programming?
443. 🟡 What is the thread-per-request model? What are its limits (memory per thread, context switching)?
444. 🟡 How does a single-threaded event loop (Node.js) handle thousands of connections?
445. 🟡 What are epoll and kqueue?
446. 🟡 Why does a CPU-heavy task block the entire Node.js event loop? How do you handle CPU work there?
447. 🟡 What are green threads / M:N scheduling (Go goroutines, Java virtual threads)?
448. 🟡 Why are goroutines/virtual threads cheaper than OS threads?
449. 🟡 How does async/await in .NET compare with these models (thread pool + I/O completion)?
450. 🟡 What is a race condition? What is a deadlock?
451. 🟡 What are locks, mutexes and semaphores?
452. 🔴 Which runtime model would you choose for a highly concurrent I/O-bound API vs a CPU-heavy image processing service?
453. 🔴 What is back-pressure?

---

## 35. Scaling — Vertical, Horizontal & Load Balancing

454. 🟢 What is scalability?
455. 🟢 What is vertical scaling (scale up)? Pros and cons?
456. 🟢 What is horizontal scaling (scale out)? Pros and cons?
457. 🟡 Why does horizontal scaling require stateless application servers?
458. 🟡 Where should state go when servers are stateless (sessions → Redis, files → object storage, data → database)?
459. 🟢 What is a single point of failure (SPOF)?
460. 🟡 What are load balancing algorithms (round robin, least connections, IP hash, weighted)?
461. 🟡 When is least connections better than round robin?
462. 🟡 What are the downsides of IP hash (sticky sessions)?
463. 🟡 What are health checks? What happens when an instance fails them?
464. 🟡 What is Layer 4 vs Layer 7 load balancing?
465. 🟡 What is auto-scaling? What metrics trigger it?
466. 🔴 What is high availability? What is the difference between HA and disaster recovery?
467. 🔴 What happens to scaling if the database becomes the bottleneck?

---

## 36. Database Scaling — Connection Pooling, Read Replicas, Sharding

468. 🟢 Why is opening a database connection expensive?
469. 🟢 What is connection pooling?
470. 🟡 What is PgBouncer (or another external pooler)? Why use it in addition to the driver's pool?
471. 🟡 What happens when the connection pool is exhausted?
472. 🟡 How do you size a connection pool?
473. 🟢 What is a read replica?
474. 🟡 How does primary-replica replication work (WAL streaming)?
475. 🟡 What is replication lag? What problems does it cause (reading stale data right after a write)?
476. 🟡 How do you handle read-your-own-writes consistency with replicas?
477. 🟢 What is sharding (horizontal partitioning)?
478. 🟡 What is a shard key? How do you choose one?
479. 🟡 What is `hash(user_id) % num_shards`? What is the problem when you add a new shard?
480. 🔴 What is consistent hashing and why does it help resharding?
481. 🔴 What are the problems with cross-shard queries and transactions?
482. 🔴 What is the difference between partitioning and sharding?
483. 🔴 What is the CAP theorem? How does it apply when you replicate or shard data?

---

## 37. Testing Strategies & Testcontainers

484. 🟢 What is the testing pyramid?
485. 🟢 What are unit tests? What should they not do?
486. 🟢 What are integration tests?
487. 🟢 What are end-to-end tests?
488. 🟡 What are test doubles? What is the difference between mocks, stubs and fakes?
489. 🟡 What is dependency injection and how does it make code testable?
490. 🟡 Why should components depend on interfaces instead of concrete implementations?
491. 🟡 Why can in-memory database fakes (SQLite, H2, in-memory providers) give false confidence?
492. 🟡 What is Testcontainers? How does it work?
493. 🟡 What is the "Functional Core, Imperative Shell" pattern?
494. 🟡 What is TDD? Explain Red → Green → Refactor.
495. 🟡 What is code coverage? Is 100% coverage a good goal?
496. 🟡 What are flaky tests and how do you fix them?
497. 🔴 What is contract testing? How is it different from integration testing?
498. 🔴 How do you test code that depends on time, randomness or external APIs?
499. 🔴 What would you test for a payment API before going to production? 💰

---

## 38. Twelve-Factor App

500. 🟢 What is the Twelve-Factor App methodology?
501. 🟡 Explain factor 1 — Codebase.
502. 🟡 Explain factor 2 — Dependencies.
503. 🟡 Explain factor 3 — Config.
504. 🟡 Explain factor 4 — Backing services.
505. 🟡 Explain factor 5 — Build, release, run.
506. 🟡 Explain factor 6 — Processes (stateless, share-nothing).
507. 🟡 Explain factor 7 — Port binding.
508. 🟡 Explain factor 8 — Concurrency.
509. 🟡 Explain factor 9 — Disposability.
510. 🟡 Explain factor 10 — Dev/prod parity.
511. 🟡 Explain factor 11 — Logs as event streams.
512. 🟡 Explain factor 12 — Admin processes.
513. 🔴 Which Twelve-Factor principles does your current project violate, and how would you fix them?

---

## 39. DevOps, Containers & CI/CD

514. 🟢 What is DevOps?
515. 🟢 What is a container? How is it different from a virtual machine?
516. 🟢 What is Docker? What is a Docker image vs a container?
517. 🟡 What problem does containerization solve ("works on my machine")?
518. 🟡 What is a multi-stage Dockerfile and why does it produce smaller, safer images?
519. 🟡 Why should containers run as a non-root user?
520. 🟡 Why use minimal base images (alpine, distroless, chiseled)?
521. 🟡 What does a reverse proxy do in front of containers (TLS termination, compression, static caching, routing)?
522. 🟢 What is CI? What is CD (continuous delivery vs continuous deployment)?
523. 🟡 What steps does a typical CI/CD pipeline have (lint, security scan, tests, build image, deploy)?
524. 🟡 What is Infrastructure as Code?
525. 🟡 What is container orchestration (Kubernetes)? Why is it needed?
526. 🔴 How do you run database migrations safely in a CI/CD pipeline?
527. 🔴 How do you scan for vulnerable dependencies and leaked secrets in CI?

---

## 40. Deployment Strategies & Reliability (SLI, SLO, SLA)

528. 🟢 What is zero-downtime deployment?
529. 🟡 What is a rolling deployment?
530. 🟡 What is a blue/green deployment? Walk through the switch.
531. 🟡 What is a canary deployment?
532. 🟡 What are feature flags?
533. 🟡 How do you roll back a bad release in each strategy?
534. 🔴 How do database schema changes affect zero-downtime deployments (expand/contract migrations)?
535. 🟢 What is an SLI?
536. 🟢 What is an SLO?
537. 🟢 What is an SLA?
538. 🟡 What is the relationship between SLI, SLO and SLA? Give an example.
539. 🟡 What is an error budget?
540. 🟡 What does 99.9% availability mean in downtime per month? What about 99.99%? 💰
541. 🔴 How do you choose realistic SLOs for a new API?

---

## 41. Tricky Questions

542. 🟡 HTTP is stateless — so how can a shopping cart "remember" items?
543. 🟡 If a JWT is signed, can a user change their role inside it?
544. 🟡 If you use HTTPS, do you still need to hash passwords?
545. 🟡 Does using UUIDs instead of integer IDs make your API secure?
546. 🟡 Does an ORM make you completely safe from SQL injection?
547. 🟡 Does CORS stop attackers from calling your API with curl?
548. 🟡 Is DELETE idempotent if the first call returns 204 and the second returns 404?
549. 🟡 Can a GET request change data? What can go wrong if it does?
550. 🟡 Why can adding an index make writes slower?
551. 🟡 Why can adding more application servers make the system slower?
552. 🟡 Why is the average latency misleading?
553. 🟡 Why is "async" not the same as "parallel"?
554. 🟡 Why can a single CPU-heavy request slow down every other request in Node.js?
555. 🟡 Why can a cache make data incorrect?
556. 🟡 Why can retries turn a small outage into a big one?
557. 🟡 Why does storing files on the app server break horizontal scaling?
558. 🟡 Why do you need idempotency if the message broker "guarantees delivery"?
559. 🟡 Why must a webhook signature be verified on the raw body and not on the parsed JSON?
560. 🟡 Why shouldn't you call a third-party API inside a database transaction?
561. 🟡 Why can a read replica return data that "doesn't exist yet" from the user's point of view?
562. 🟡 Why is `SameSite=Lax` not complete CSRF protection?
563. 🟡 Why is crashing at startup on a missing config value a good thing?
564. 🟡 Why should logs go to stdout instead of files inside containers?
565. 🟡 Why is a 302 redirect after a POST commonly used (Post/Redirect/Get)?
566. 🔴 Can a system be 100% available? Why not?
567. 🔴 Is the database always the bottleneck? How do you prove where the bottleneck is?
568. 🔴 If two requests update the same record at the same time, what can go wrong and how do you prevent it? 💰
569. 🔴 Why does `hash(id) % N` sharding cause massive data movement when N changes?
570. 🔴 Why are distributed transactions avoided in microservices?

---

## 42. Predict the Behavior

> What happens in each situation? Explain why and how to fix it if it's wrong.

571. 🟡 A client sends `PUT /api/v1/users/5` with only `{ "name": "Asha" }`. What should happen to the other fields of the user?
572. 🟡 A client retries `POST /api/v1/payments` three times after timeouts. No idempotency key is used. What happens? 💰
573. 🟡 A browser frontend on `https://app.example.com` calls `https://api.example.com` with an `Authorization` header. The API doesn't handle `OPTIONS`. What does the user see?
574. 🟡 An auth cookie is set without `HttpOnly`, and the site has an XSS vulnerability. What can the attacker do?
575. 🟡 An API stores sessions in application memory and runs 3 instances behind a round-robin load balancer. What happens to logged-in users?
576. 🟡 A JWT with `exp` 24 hours in the future is stolen. The user changes their password. Can the attacker still use the token?
577. 🟡 A cache-aside implementation updates the database but never deletes the cache key. What do users see?
578. 🟡 1,000 requests miss the cache for the same popular key at the same moment. What happens to the database?
579. 🟡 An endpoint loads 100 posts and then loads each post's author in a loop. How many queries run? How do you fix it?
580. 🟡 A composite index exists on `(user_id, status)`. Which of these queries use it: `WHERE user_id = 1`, `WHERE status = 'paid'`, `WHERE user_id = 1 AND status = 'paid'`?
581. 🟡 A user writes a comment and is immediately redirected to a page that reads from a read replica with 200 ms lag. What do they see?
582. 🟡 A webhook receiver parses JSON, re-serializes it and then verifies the HMAC signature. What happens?
583. 🟡 A webhook provider sends the same `payment.succeeded` event twice. The receiver isn't idempotent. What happens? 💰
584. 🟡 A background worker crashes after sending an email but before acknowledging the job. What happens next?
585. 🟡 Kubernetes sends SIGTERM to a pod that doesn't handle it, with a 30-second grace period. What happens to in-flight requests?
586. 🟡 A Node.js API computes a bcrypt hash with a very high cost synchronously on the main thread. What happens to other requests?
587. 🟡 An API returns `500` with a full stack trace and SQL query in the response body. What is the risk?
588. 🟡 `GET /api/v1/invoices/1052` returns any invoice for any logged-in user. What vulnerability is this?
589. 🟡 An admin delete endpoint only checks that the user is logged in, not their role. What vulnerability is this?
590. 🟡 An app reads `DATABASE_URL` only when the first request needs the database. The variable is missing in production. When is the problem discovered?
591. 🟡 Logs are written as plain text like `"user logged in"` across 50 services. What problems do you face during an incident?
592. 🟡 A system's average latency is 20 ms but P99 is 5 s. 10 services are called per user request. What is the chance a user request hits at least one slow call?
593. 🟡 A blue/green switch happens but the new version requires a database column that the old version doesn't know about. What can go wrong?
594. 🔴 Sharding uses `hash(user_id) % 4`, and you add a 5th shard. What happens to existing data?

---

## 43. Scenario-Based Questions

595. 🟡 Users upload 500 MB videos through your API and servers run out of memory. How do you redesign uploads?
596. 🟡 A "generate report" endpoint takes 2 minutes and users get 504 errors. How do you redesign it?
597. 🟡 Your product needs live notifications when an order status changes. Which real-time technology do you choose and why?
598. 🟡 A chat feature using WebSockets works with one server but messages are lost when you add a second server. Why, and how do you fix it?
599. 🟡 Your search feature using `ILIKE '%term%'` takes 8 seconds on 10 million rows. What do you do?
600. 🟡 Your login endpoint is being brute-forced. What protections do you add?
601. 🟡 A security audit finds users can access other users' invoices by changing the ID in the URL. How do you fix it everywhere? 💰
602. 🟡 A developer accidentally committed the production database password to Git. What do you do?
603. 🟡 Your API's P99 latency spiked after a release, but the average looks fine. How do you investigate?
604. 🟡 The database CPU is at 100% after traffic doubled. What are your short-term and long-term options?
605. 🟡 You need to integrate with a payment provider that sends webhooks. Design the receiver. 💰
606. 🟡 You must send an email after an order is saved, without losing emails and without slowing the API. Design it.
607. 🟡 Your mobile app needs to work with both an old and a new version of the API for six months. How do you manage it?
608. 🟡 The frontend team is blocked waiting for backend APIs. How do you unblock them?
609. 🟡 Your integration tests pass with an in-memory database but production fails on a JSONB query. What do you change?
610. 🟡 During deployments, users get errors for about 10 seconds. How do you achieve zero downtime?
611. 🟡 Your Redis cache went down and the database collapsed under load. How do you make the system resilient?
612. 🟡 Duplicate jobs are being processed because two workers picked up the same task. How do you fix it?
613. 🔴 Your monolith needs to handle 10x traffic in three months. What do you scale first and why?
614. 🔴 Your team stores timestamps without time zones and users in different countries see wrong times. How do you fix existing data and future writes?
615. 🔴 A third-party API you depend on is slow and sometimes down, and it's making your API fail. What patterns do you apply?
616. 🔴 Your system logs contain customer card numbers and passwords. What is your remediation plan? 💰
617. 🔴 You inherited a codebase where controllers contain SQL queries and business logic. How do you refactor it safely?
618. 🔴 Read replicas are causing "I saved it but it disappeared" complaints. How do you fix the user experience?
619. 🔴 Management asks for 99.99% availability. What questions do you ask and what does it require?

---

## 44. System Design Questions

620. 🔴 Design a URL shortener.
621. 🔴 Design a file upload and sharing service (like Google Drive) using object storage and pre-signed URLs.
622. 🔴 Design a notification system (email, SMS, push) with background queues and retries.
623. 🔴 Design a real-time chat application with WebSockets and horizontal scaling.
624. 🔴 Design a live sports score or stock ticker using SSE. 💰
625. 🔴 Design a rate limiter (token bucket with Redis).
626. 🔴 Design a payment webhook processing system with idempotency and the outbox pattern. 💰
627. 🔴 Design a product search system using an inverted index synced from the primary database.
628. 🔴 Design an authentication service supporting sessions, JWT and "Login with Google".
629. 🔴 Design a report generation system that produces large PDFs asynchronously.
630. 🔴 Design a task management API (contract-first with OpenAPI, layered architecture, pagination, caching).
631. 🔴 Design the observability setup (logs, metrics, traces) for a system with 20 services.
632. 🔴 Design a system that handles 100,000 requests per second for a read-heavy product catalogue.
633. 🔴 Design a multi-tenant SaaS backend with strict data isolation between tenants. 💰

---

## 45. Hands-On Tasks (Any Language)

634. 🟢 Build a REST API for tasks with correct HTTP methods, status codes and a JSON 404 fallback route.
635. 🟢 Add request validation (syntactic, semantic, type) and return structured 400/422 errors.
636. 🟡 Implement the controller → service → repository layers with dependency injection.
637. 🟡 Write middleware for request ID, structured logging, rate limiting and global error handling in the correct order.
638. 🟡 Configure CORS correctly for a frontend on a different domain.
639. 🟡 Implement session-based authentication with Redis and secure cookies.
640. 🟡 Implement JWT authentication with short-lived access tokens and refresh tokens.
641. 🟡 Implement password hashing with Argon2id or bcrypt.
642. 🟡 Add ownership checks to prevent BOLA on every read/update/delete.
643. 🟡 Write an OpenAPI 3.1 spec first, generate a mock server and implement the API against it.
644. 🟡 Add cache-aside caching with Redis and TTLs to a read endpoint, and invalidate on update.
645. 🟡 Add ETag support with `304 Not Modified` responses.
646. 🟡 Implement cursor-based pagination.
647. 🟡 Find and fix an N+1 query problem.
648. 🟡 Analyze a slow query with `EXPLAIN ANALYZE` and add the right composite index.
649. 🟡 Implement pre-signed URL uploads to object storage.
650. 🟡 Move a slow operation to a background job with retries and idempotency.
651. 🟡 Build an SSE endpoint that streams order status updates.
652. 🟡 Build a WebSocket chat that works across two instances using Redis Pub/Sub.
653. 🟡 Build a webhook receiver with HMAC verification, timestamp checks and idempotency.
654. 🟡 Implement the transactional outbox pattern with a background publisher.
655. 🟡 Implement startup config validation that fails fast on missing variables.
656. 🟡 Add structured JSON logging, Prometheus metrics and OpenTelemetry tracing.
657. 🟡 Implement graceful shutdown on SIGTERM.
658. 🟡 Write unit tests with mocks/stubs/fakes and integration tests with Testcontainers.
659. 🟡 Write a multi-stage Dockerfile that runs as a non-root user.
660. 🟡 Build a CI pipeline that lints, scans, tests, builds and pushes a Docker image.
661. 🔴 Implement a token bucket rate limiter in Redis.
662. 🔴 Load test your API and report P50/P95/P99 latency and max throughput.

---

## 46. Rapid-Fire Round

663. 🟢 Default port for HTTP? HTTPS?
664. 🟢 Is HTTP stateful or stateless?
665. 🟢 Which status code means "created"?
666. 🟢 Which status code means "not authenticated"?
667. 🟢 Which status code means "authenticated but not allowed"?
668. 🟢 Which status code means "too many requests"?
669. 🟢 Which status code means "upstream timed out"?
670. 🟢 Which status code means "not modified"?
671. 🟢 Which status code is used to upgrade to WebSockets?
672. 🟢 Which HTTP method is used for a CORS preflight?
673. 🟢 Which HTTP methods are idempotent?
674. 🟢 What are the three parts of a JWT?
675. 🟢 Which cookie flag blocks JavaScript access?
676. 🟢 Which cookie flag requires HTTPS?
677. 🟢 What is the defense against SQL injection?
678. 🟢 Which algorithm is the OWASP-recommended password hash?
679. 🟢 What does BOLA stand for?
680. 🟢 What data structure do most database indexes use?
681. 🟢 What data structure does Elasticsearch use?
682. 🟢 Which HTTP status should an async job endpoint return?
683. 🟡 Which HTTP version runs on UDP?
684. 🟡 Which header carries the trace context in W3C Trace Context?
685. 🟡 Which signal does Kubernetes send before killing a pod?
686. 🟡 What are the four golden signals?
687. 🟡 What does P99 mean?
688. 🟡 What does PKCE stand for?
689. 🟡 Which OAuth flow is used for machine-to-machine?
690. 🟡 Which caching strategy can lose data if the cache crashes?
691. 🟡 Which Redis eviction policy removes least recently used keys from all keys?
692. 🟡 What pattern solves "update DB + send event/webhook" reliably?
693. 🟡 What is the left-prefix rule in one line?
694. 🟡 What is the difference between concurrency and parallelism in one line?
695. 🟡 What is the difference between SLO and SLA in one line?
696. 🔴 What is the difference between SSE and WebSockets in one line?
697. 🔴 What is the difference between a mock, a stub and a fake in one line?
698. 🔴 What is the difference between vertical and horizontal scaling in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering & Distributed Systems Fundamentals.
