# 🎯 Redis Interview Questions — Part 12 (Questions Only)

> **Scope:** Focused for **2–3 years of experience** — Redis fundamentals, data types, expiry & eviction, caching patterns, persistence, replication & high availability basics, Redis in .NET (`StackExchange.Redis`, `IDistributedCache`, `HybridCache`), common use cases (sessions, rate limiting, locks, pub/sub, leaderboards), common problems, tricky questions and scenarios.
> **Based on question patterns from:** product companies, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced (good to know) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. Redis Fundamentals
2. Data Types & Common Commands
3. Keys, Expiry (TTL) & Eviction
4. Caching Patterns
5. Cache Problems — Stampede, Penetration, Avalanche, Hot Keys
6. Persistence — RDB & AOF
7. Replication, Sentinel & Cluster (Basics)
8. Transactions, Pipelining & Lua Scripts
9. Pub/Sub & Streams
10. Common Use Cases
11. Redis in .NET
12. Performance, Memory & Best Practices
13. Security & Operations
14. Tricky Questions
15. Scenario-Based Questions
16. Hands-On Tasks
17. Rapid-Fire Round

---

## 1. Redis Fundamentals

1. 🟢 What is Redis?
2. 🟢 Why is Redis so fast?
3. 🟢 Is Redis a database, a cache or a message broker? Can it be all three?
4. 🟢 What is the difference between Redis and a relational database?
5. 🟢 What is the difference between Redis and Memcached?
6. 🟡 Is Redis single-threaded? Why is that not usually a bottleneck? What is I/O threading in Redis 6+?
7. 🟡 Is Redis data lost when the server restarts?
8. 🟢 What is the default port of Redis?
9. 🟡 What are Redis databases (0–15)? Why are they discouraged in production and not supported in Redis Cluster?
10. 🟡 What changed with Redis licensing, and what is Valkey?
11. 🟡 What are managed Redis options (Azure Cache for Redis / Azure Managed Redis, AWS ElastiCache, Redis Cloud)?

---

## 2. Data Types & Common Commands

12. 🟢 What data types does Redis support?
13. 🟢 What is a String? Common commands: `SET`, `GET`, `INCR`, `DECR`, `INCRBY`, `APPEND`, `MSET`, `MGET`.
14. 🟢 What does `SET key value NX EX 60` do?
15. 🟢 What is a Hash? When would you use it instead of a JSON string? Commands: `HSET`, `HGET`, `HGETALL`, `HINCRBY`, `HDEL`.
16. 🟢 What is a List? Commands: `LPUSH`, `RPUSH`, `LPOP`, `RPOP`, `LRANGE`, `BLPOP`.
17. 🟢 What is a Set? Commands: `SADD`, `SREM`, `SMEMBERS`, `SISMEMBER`, `SINTER`, `SUNION`.
18. 🟢 What is a Sorted Set (ZSet)? Commands: `ZADD`, `ZRANGE`, `ZREVRANGE`, `ZRANK`, `ZSCORE`, `ZINCRBY`, `ZRANGEBYSCORE`.
19. 🟡 What are Bitmaps and HyperLogLog? Give a use case for each.
20. 🟡 What are Geospatial indexes (`GEOADD`, `GEOSEARCH`)?
21. 🟡 What are Redis Streams?
22. 🟡 What is RedisJSON / JSON support?
23. 🟡 Which data type would you use for: user session, page view counter, unique visitors, leaderboard, job queue, user's followers, product details?
24. 🟡 Are Redis operations like `INCR` atomic?

---

## 3. Keys, Expiry (TTL) & Eviction

25. 🟢 What is TTL in Redis? How do you set it (`EXPIRE`, `SETEX`, `SET ... EX`)?
26. 🟢 How do you check the TTL of a key (`TTL`, `PTTL`)? What do `-1` and `-2` mean?
27. 🟢 How do you remove an expiry (`PERSIST`)?
28. 🟡 How does Redis delete expired keys (lazy expiration and active expiration)?
29. 🟡 What happens to the TTL when you `SET` an existing key again?
30. 🟡 What are good key naming conventions (`app:user:102:profile`)?
31. 🟡 Why should you never use `KEYS *` in production? What should you use instead (`SCAN`)?
32. 🟢 What is `maxmemory`?
33. 🟡 What eviction policies does Redis support (`noeviction`, `allkeys-lru`, `volatile-lru`, `allkeys-lfu`, `volatile-lfu`, `allkeys-random`, `volatile-random`, `volatile-ttl`)?
34. 🟡 What is the difference between LRU and LFU?
35. 🟡 Which eviction policy would you choose for a pure cache? For a cache that also stores sessions?
36. 🟡 What happens when memory is full and the policy is `noeviction`?
37. 🟡 What is `DEL` vs `UNLINK`?

---

## 4. Caching Patterns

38. 🟢 What is caching? What should you cache?
39. 🟢 What is cache-aside (lazy loading)? Explain the read flow.
40. 🟡 What is read-through caching?
41. 🟡 What is write-through caching? Pros and cons?
42. 🟡 What is write-behind (write-back) caching? What is the risk?
43. 🟡 What is write-around?
44. 🟡 How do you choose a TTL for cached data?
45. 🟡 What is cache invalidation? What strategies exist (TTL, delete on update, events)?
46. 🟡 When updating data, should you update the cache or delete the cache key? Why?
47. 🟡 What is the problem with "update DB then update cache" when two requests run concurrently?
48. 🟡 What is a cache hit ratio and how do you measure it (`INFO stats`)?
49. 🟡 What is a two-level cache (in-memory + Redis)? When is it useful?
50. 🔴 What data should not be cached or should be cached very carefully (balances, permissions)? 💰

---

## 5. Cache Problems — Stampede, Penetration, Avalanche, Hot Keys

51. 🟡 What is a cache stampede (thundering herd)? How do you prevent it (locking, request coalescing, early refresh)?
52. 🟡 What is cache penetration (requests for keys that don't exist)? How do you prevent it (cache null values, Bloom filter, validation)?
53. 🟡 What is cache avalanche (many keys expiring at the same time or Redis going down)? How do you prevent it (TTL jitter, HA, fallbacks)?
54. 🟡 What is a hot key? How do you handle it (local cache, key replication)?
55. 🟡 What is a big key? Why are big keys a problem? How do you find them (`redis-cli --bigkeys`, `MEMORY USAGE`)?
56. 🔴 What happens to your application if Redis becomes unavailable? How do you design for it?

---

## 6. Persistence — RDB & AOF

57. 🟢 Does Redis persist data to disk?
58. 🟡 What is RDB (snapshotting)? Pros and cons?
59. 🟡 What is AOF (Append Only File)? Pros and cons?
60. 🟡 What are the AOF fsync options (`always`, `everysec`, `no`)?
61. 🟡 What is AOF rewrite?
62. 🟡 Can you use RDB and AOF together?
63. 🟡 What do `SAVE` and `BGSAVE` do? Why shouldn't you use `SAVE` in production?
64. 🟡 If Redis is used only as a cache, do you need persistence?
65. 🔴 How much data can you lose with RDB only vs AOF `everysec`? 💰

---

## 7. Replication, Sentinel & Cluster (Basics)

66. 🟢 What is Redis replication (primary/replica)?
67. 🟡 Is Redis replication synchronous or asynchronous? What does that mean for data loss?
68. 🟡 Can you write to a replica?
69. 🟡 What is Redis Sentinel? What does it do (monitoring, automatic failover)?
70. 🟡 What is Redis Cluster? How does it shard data?
71. 🟡 What are hash slots? How many are there (16384)?
72. 🟡 What is a hash tag (`{user:102}:cart`) and why is it needed in Redis Cluster?
73. 🟡 Why do multi-key commands fail in Redis Cluster with a `CROSSSLOT` error?
74. 🟡 Sentinel vs Cluster — when do you use each?
75. 🔴 What happens during a failover? Can writes be lost?

---

## 8. Transactions, Pipelining & Lua Scripts

76. 🟡 What are Redis transactions (`MULTI`, `EXEC`, `DISCARD`)?
77. 🟡 Do Redis transactions roll back if one command fails?
78. 🟡 What is `WATCH` and optimistic locking in Redis?
79. 🟡 What is pipelining? How does it improve performance?
80. 🟡 What is the difference between pipelining and transactions?
81. 🟡 What are Lua scripts in Redis (`EVAL`)? Why are they atomic?
82. 🔴 Why can a long-running Lua script block all other clients?
83. 🔴 What are Redis Functions (Redis 7)?

---

## 9. Pub/Sub & Streams

84. 🟢 What is Redis Pub/Sub? Commands: `PUBLISH`, `SUBSCRIBE`, `PSUBSCRIBE`.
85. 🟡 What happens to a Pub/Sub message if no subscriber is connected?
86. 🟡 Is Redis Pub/Sub reliable? What are its limitations?
87. 🟡 What is a Redis Stream? Commands: `XADD`, `XREAD`, `XRANGE`.
88. 🟡 What are consumer groups in Redis Streams (`XGROUP`, `XREADGROUP`, `XACK`, `XPENDING`)?
89. 🟡 Pub/Sub vs Streams vs Lists for queues — when do you use each?
90. 🟡 Redis Streams vs Kafka vs RabbitMQ — when is Redis enough?
91. 🟡 How is Redis Pub/Sub used as a SignalR backplane?

---

## 10. Common Use Cases

92. 🟢 How do you use Redis for caching database query results?
93. 🟢 How do you store user sessions in Redis? Why is it better than in-memory sessions when you have multiple servers?
94. 🟡 How do you implement a rate limiter with Redis (fixed window with `INCR` + `EXPIRE`, sliding window with sorted sets, token bucket with Lua)?
95. 🟡 How do you implement a distributed lock with Redis (`SET key value NX PX`)?
96. 🟡 Why must the lock value be unique, and why must unlocking check the value (Lua script)?
97. 🔴 What is Redlock? What are its known criticisms?
98. 🟡 How do you implement a leaderboard with sorted sets?
99. 🟡 How do you implement counters (page views, likes) with Redis?
100. 🟡 How do you implement unique visitor counting (Set vs HyperLogLog)?
101. 🟡 How do you implement a simple job queue with Lists (`LPUSH` + `BRPOP`)? What is the reliable queue pattern (`LMOVE`/`BLMOVE`)?
102. 🟡 How do you store OTPs with Redis (TTL, attempts limit)? 💰
103. 🟡 How do you implement idempotency keys with Redis (`SET NX EX`)? 💰
104. 🟡 How do you store a shopping cart in Redis (Hash)?
105. 🟡 How do you implement "recently viewed items" (List with `LTRIM`)?
106. 🟡 How do you implement a JWT/token denylist with Redis?
107. 🟡 How do you implement feature flags or configuration caching with Redis?

---

## 11. Redis in .NET

108. 🟢 Which library do you use to connect to Redis from .NET (`StackExchange.Redis`)?
109. 🟢 What is `ConnectionMultiplexer`? Why should it be created once and reused (singleton)?
110. 🟡 What happens if you create a new `ConnectionMultiplexer` per request?
111. 🟡 What is `IDatabase` and how do you get it (`GetDatabase()`)? Is it cheap to call?
112. 🟡 What is the difference between sync and async methods (`StringGet` vs `StringGetAsync`)? Which should you use in ASP.NET Core?
113. 🟡 How do you store and read objects (serialize to JSON with `System.Text.Json`)?
114. 🟡 What is `IDistributedCache`? How do you configure it with Redis (`AddStackExchangeRedisCache`)?
115. 🟡 What are `DistributedCacheEntryOptions` (`AbsoluteExpirationRelativeToNow`, `SlidingExpiration`)?
116. 🟡 What is the difference between `IMemoryCache`, `IDistributedCache` and `HybridCache` (.NET 9)?
117. 🟡 How does `HybridCache` protect against cache stampede?
118. 🟡 How do you use Redis for ASP.NET Core session state (`AddSession` + distributed cache)?
119. 🟡 How do you use Redis for output caching in ASP.NET Core?
120. 🟡 How do you use Redis for Data Protection key storage when running multiple instances?
121. 🟡 How do you use Redis as a SignalR backplane (`AddStackExchangeRedis`)?
122. 🟡 What connection string options matter (`abortConnect=false`, `ssl=true`, `password`, `connectTimeout`, `syncTimeout`)?
123. 🟡 What is a `RedisTimeoutException`? What are common causes (thread pool starvation, big values, network, slow commands)?
124. 🟡 How do you use transactions and batches in StackExchange.Redis (`CreateTransaction`, `CreateBatch`)?
125. 🟡 How do you run a Lua script from .NET (`ScriptEvaluateAsync`)?
126. 🟡 How do you implement a distributed lock in .NET (`LockTakeAsync`, `LockReleaseAsync`, or libraries like RedLock.net)?
127. 🟡 How do you subscribe to Pub/Sub in .NET (`GetSubscriber()`)?
128. 🟡 How do you add a health check for Redis in ASP.NET Core?
129. 🔴 How do you write a generic cache-aside helper (`GetOrSetAsync<T>`) in .NET?
130. 🔴 How do you test code that uses Redis (Testcontainers, interfaces/mocks)?

---

## 12. Performance, Memory & Best Practices

131. 🟡 What are slow commands to avoid in production (`KEYS`, `FLUSHALL`, `SMEMBERS`/`HGETALL` on huge keys, `LRANGE 0 -1` on big lists)?
132. 🟡 What is `SLOWLOG`?
133. 🟡 What does `INFO` show (memory, stats, clients, replication, keyspace)?
134. 🟡 What does `MONITOR` do? Why shouldn't you run it in production for long?
135. 🟡 How do you check memory usage of a key (`MEMORY USAGE`)?
136. 🟡 Why should values be kept small? What is a reasonable size limit?
137. 🟡 Should you store large JSON objects as one string or as a Hash?
138. 🟡 How do you reduce memory usage (shorter keys, compression, TTLs, right data types)?
139. 🟡 What is memory fragmentation in Redis?
140. 🟡 How many connections should an application open to Redis?
141. 🔴 How do you measure Redis latency (`redis-cli --latency`)?

---

## 13. Security & Operations

142. 🟡 How do you secure Redis (password/ACLs, TLS, bind to private network, no public exposure)?
143. 🟡 What are Redis ACLs (Redis 6+)?
144. 🟡 Why is exposing Redis to the internet dangerous?
145. 🟡 How do you rename or disable dangerous commands (`FLUSHALL`, `CONFIG`)?
146. 🟡 What are basic `redis-cli` commands you use (`PING`, `INFO`, `TTL`, `TYPE`, `SCAN`, `DBSIZE`)?
147. 🟡 How do you back up Redis?
148. 🟡 What should you monitor (memory, evictions, hit ratio, connected clients, latency, replication lag)?
149. 🔴 Should sensitive data (PII, card numbers) be stored in Redis? How would you protect it? 💰

---

## 14. Tricky Questions

150. 🟡 If Redis is single-threaded, how can it handle 100,000+ operations per second?
151. 🟡 Is data in Redis always safe after `SET` returns OK?
152. 🟡 Does a Redis transaction roll back if a command fails at runtime?
153. 🟡 Why can `KEYS *` bring production down?
154. 🟡 Why can deleting one big key block Redis?
155. 🟡 What happens if you set a TTL and then overwrite the key with `SET` without TTL?
156. 🟡 Why do keys sometimes disappear before their TTL? (eviction)
157. 🟡 Why can a cache make your application return wrong data?
158. 🟡 Can you rely on Redis Pub/Sub to never lose messages?
159. 🟡 Why does a distributed lock without a TTL cause problems? Why does a lock with a short TTL also cause problems?
160. 🟡 Why do you get `CROSSSLOT` errors in Redis Cluster?
161. 🟡 Why do you get `RedisTimeoutException` even though Redis server is fine?
162. 🟡 Why is creating a new `ConnectionMultiplexer` per request bad?
163. 🟡 Is `IDistributedCache` with Redis faster than `IMemoryCache`? Why or why not?
164. 🔴 Can you use Redis as your primary database? When is that acceptable?
165. 🔴 Should account balances be cached in Redis? What can go wrong? 💰

---

## 15. Scenario-Based Questions

166. 🟡 Your API is slow because of repeated database calls for the same data. How do you add Redis caching?
167. 🟡 Users see outdated product prices after an update. How do you fix cache invalidation?
168. 🟡 A cached key expires and 1,000 requests hit the database at the same time. How do you fix it?
169. 🟡 Attackers request random non-existent IDs and all requests go to the database. What do you do?
170. 🟡 Redis memory is full and keys are being evicted unexpectedly. How do you investigate?
171. 🟡 Users get logged out when you deploy because sessions were in memory. How does Redis help?
172. 🟡 Your ASP.NET Core app logs many `RedisTimeoutException` errors under load. How do you troubleshoot?
173. 🟡 You need to limit each user to 100 API calls per minute across 5 servers. Design it with Redis.
174. 🟡 A scheduled job runs on 3 servers but should run only once. How do you use Redis to ensure that?
175. 🟡 You need a real-time leaderboard for 1 million players. How do you design it?
176. 🟡 Redis went down and your whole application stopped working. How do you make the app tolerate Redis failure?
177. 🟡 You need to prevent duplicate payment submissions within 30 seconds. How do you use Redis? 💰
178. 🟡 You need to store OTPs that expire in 5 minutes and allow max 3 attempts. Design it. 💰
179. 🟡 One key (e.g., homepage data) receives a huge amount of traffic. How do you handle it?
180. 🔴 You must choose between Redis Pub/Sub, Redis Streams and Kafka for order events. What do you choose and why?

---

## 16. Hands-On Tasks

181. 🟢 Run Redis locally with Docker and connect with `redis-cli`.
182. 🟢 Practise `SET`/`GET`/`EXPIRE`/`TTL`/`INCR` and the Hash, List, Set and Sorted Set commands.
183. 🟡 Implement cache-aside for a "get product by ID" API in ASP.NET Core using `IDistributedCache`.
184. 🟡 Replace it with `HybridCache` and compare behaviour.
185. 🟡 Implement delete-on-update cache invalidation.
186. 🟡 Implement a fixed-window rate limiter middleware using `INCR` + `EXPIRE`.
187. 🟡 Implement a distributed lock with `SET NX PX` and a safe Lua unlock.
188. 🟡 Build a leaderboard API using sorted sets (top 10, rank of a user).
189. 🟡 Store ASP.NET Core sessions in Redis.
190. 🟡 Configure Redis as a SignalR backplane for two app instances.
191. 🟡 Add a Redis health check to your API.
192. 🔴 Write an integration test using Testcontainers for Redis.

---

## 17. Rapid-Fire Round

193. 🟢 Default Redis port?
194. 🟢 Command to check if Redis is alive?
195. 🟢 Command to set a key with a 60-second expiry?
196. 🟢 What does `TTL` return for a key without expiry? For a missing key?
197. 🟢 Which data type is best for a leaderboard?
198. 🟢 Which data type is best for unique items?
199. 🟢 Which command should you use instead of `KEYS`?
200. 🟡 Which eviction policy is best for a pure cache?
201. 🟡 Which persistence option gives better durability — RDB or AOF?
202. 🟡 How many hash slots are in Redis Cluster?
203. 🟡 Which .NET class should be a singleton for Redis connections?
204. 🟡 Which .NET 9 cache API combines in-memory and distributed caching?
205. 🟡 Which command makes a set-if-not-exists for locks?
206. 🟡 Which Redis feature provides reliable message consumption with acknowledgements?
207. 🟡 What is the difference between `DEL` and `UNLINK` in one line?
208. 🟡 What is the difference between cache-aside and write-through in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis.
