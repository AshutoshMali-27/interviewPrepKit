# 🎯 System Design Interview Questions — Part 10 (Questions Only)

> **Scope:** System design interviews end to end — the interview framework, requirements & estimation, core concepts (scalability, availability, consistency, CAP/PACELC, latency), building blocks (load balancers, caches, CDNs, databases, queues, storage, search, gateways), data modeling & partitioning, replication & consensus, distributed system patterns, reliability, security & observability at the design level, **High-Level Design (HLD) case studies with follow-up probes**, **financial-domain designs**, **Low-Level Design (LLD) / object-oriented design problems**, trade-off questions, tricky questions and scenario-based questions.
> **Based on question patterns from:** product MNCs (Amazon, Google, Microsoft, Uber, Flipkart, Atlassian), financial companies (banks, payments, trading, fintech — Razorpay, PhonePe, Paytm, JPMorgan, Goldman Sachs), service MNCs, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Language/stack agnostic.** Builds on Parts 6, 7, 8 and 9.

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Approach & Fundamentals**
1. The System Design Interview Framework
2. Requirements Gathering — Functional & Non-Functional
3. Back-of-the-Envelope Estimation
4. Scalability, Availability, Reliability & Latency
5. Consistency Models, CAP & PACELC
6. Networking & Communication for System Design

**Part B — Building Blocks**
7. DNS, CDN & Edge
8. Load Balancers & Reverse Proxies
9. API Gateway, Rate Limiting & Throttling
10. Caching (All Layers)
11. Databases — SQL vs NoSQL & Choosing Storage
12. Data Modeling for Scale
13. Replication
14. Partitioning, Sharding & Consistent Hashing
15. Message Queues, Pub/Sub & Event Streaming
16. Object Storage, Blob Storage & File Systems
17. Search Systems
18. Unique ID Generation
19. Time, Clocks & Ordering

**Part C — Distributed Systems Concepts & Patterns**
20. Consensus, Leader Election & Coordination
21. Distributed Transactions & Consistency Patterns
22. Reliability & Resiliency Patterns
23. Data Processing — Batch, Stream, Lambda & Kappa
24. Security in System Design
25. Observability & Operations in System Design
26. Multi-Region, Disaster Recovery & Cost

**Part D — High-Level Design (HLD) Case Studies**
27. Classic Beginner/Intermediate Designs
28. Social Media & Content Platforms
29. Messaging & Real-Time Systems
30. Media, Streaming & Storage Systems
31. Location-Based & Marketplace Systems
32. E-Commerce & Booking Systems
33. Infrastructure & Developer Platform Systems
34. Data, Analytics & ML Systems
35. Financial-Domain System Designs 💰

**Part E — Follow-Up Probes (Asked After Any HLD)**
36. Deep-Dive & Follow-Up Questions

**Part F — Low-Level Design (LLD) / Object-Oriented Design**
37. LLD Fundamentals
38. LLD Problems — Classic
39. LLD Problems — Financial & Business Domain 💰
40. LLD Problems — Infrastructure Components

**Part G — Practice**
41. Trade-Off Questions
42. Tricky Questions
43. Scenario-Based Questions
44. Rapid-Fire Round

---

# Part A — Approach & Fundamentals

## 1. The System Design Interview Framework

1. 🟢 What is system design? What is the difference between High-Level Design (HLD) and Low-Level Design (LLD)?
2. 🟢 What steps do you follow in a system design interview?
3. 🟡 How do you spend a 45-minute system design interview (requirements, estimation, API, data model, high-level design, deep dive, bottlenecks)?
4. 🟡 What clarifying questions should you ask before designing anything?
5. 🟡 How do you decide what is in scope and out of scope?
6. 🟡 Why should you start with a simple design and then scale it?
7. 🟡 How do you present trade-offs instead of a single "right" answer?
8. 🟡 What do interviewers evaluate at junior, mid and senior levels?
9. 🔴 How do you handle an interviewer who keeps changing requirements mid-way?
10. 🔴 How do you identify and discuss bottlenecks and single points of failure in your own design?
11. 🔴 What are the most common mistakes candidates make in system design interviews?

---

## 2. Requirements Gathering — Functional & Non-Functional

12. 🟢 What are functional requirements? Give examples.
13. 🟢 What are non-functional requirements? Give examples (scalability, availability, latency, consistency, durability, security, cost).
14. 🟡 How do non-functional requirements change the architecture?
15. 🟡 How do you decide between strong and eventual consistency for a feature?
16. 🟡 What is read-heavy vs write-heavy? Why does it matter?
17. 🟡 What questions do you ask about users, traffic, geography and growth?
18. 🟡 How do you define SLAs/SLOs for the system you are designing?
19. 🔴 How do compliance requirements (data residency, PCI-DSS, GDPR, RBI) shape a design? 💰

---

## 3. Back-of-the-Envelope Estimation

20. 🟢 Why do we do capacity estimation in system design?
21. 🟢 What are latency numbers every engineer should know (L1 cache, RAM, SSD, network within DC, cross-region)?
22. 🟡 How do you convert DAU into requests per second (QPS)?
23. 🟡 How do you estimate peak QPS from average QPS?
24. 🟡 How do you estimate storage needs per day, per year and for 5 years?
25. 🟡 How do you estimate bandwidth (ingress and egress)?
26. 🟡 How do you estimate the number of servers needed?
27. 🟡 How do you estimate cache memory size (80/20 rule)?
28. 🟡 What are powers of two and data size conversions (KB, MB, GB, TB, PB)?
29. 🟡 Estimate the QPS and storage for a URL shortener with 100 million new URLs per month.
30. 🟡 Estimate the storage needed for a chat app with 500 million users sending 40 messages per day.
31. 🟡 Estimate the storage and bandwidth for a video platform where 500 hours of video are uploaded per minute.
32. 🔴 Estimate the TPS a UPI-like payment system must handle during a festival peak. 💰
33. 🔴 How precise should your estimates be in an interview?

---

## 4. Scalability, Availability, Reliability & Latency

34. 🟢 What is scalability?
35. 🟢 What is the difference between vertical and horizontal scaling?
36. 🟢 What is availability? How is it measured ("nines")?
37. 🟡 How much downtime per year do 99%, 99.9%, 99.99% and 99.999% allow?
38. 🟡 How do you calculate the availability of components in series vs in parallel?
39. 🟢 What is reliability? How is it different from availability?
40. 🟡 What is durability?
41. 🟡 What is fault tolerance vs high availability?
42. 🟢 What is a single point of failure? How do you remove one?
43. 🟢 What is the difference between latency and throughput?
44. 🟡 Why do we design for P99 latency rather than average latency?
45. 🟡 What is elasticity?
46. 🟡 What is statelessness and why does it enable scaling?
47. 🔴 What is the cost of each additional "nine" of availability?
48. 🔴 What is graceful degradation? Give an example from a real product.

---

## 5. Consistency Models, CAP & PACELC

49. 🟢 What is consistency in distributed systems?
50. 🟢 What is the CAP theorem? Explain each letter.
51. 🟡 Why must you choose between C and A only during a network partition?
52. 🟡 Give examples of CP systems and AP systems.
53. 🟡 What is the PACELC theorem? Why is it more useful than CAP?
54. 🟡 What is strong consistency? What is linearizability?
55. 🟡 What is eventual consistency?
56. 🟡 What are causal consistency, read-your-writes, monotonic reads and session consistency?
57. 🟡 What is sequential consistency vs linearizability?
58. 🟡 What are quorum reads and writes (N, R, W)? What does R + W > N guarantee?
59. 🟡 What is tunable consistency (e.g., Cassandra consistency levels)?
60. 🔴 Which consistency model would you choose for: bank balance, social media likes, product inventory, shopping cart, user profile? 💰
61. 🔴 What is ACID vs BASE?

---

## 6. Networking & Communication for System Design

62. 🟢 What is the difference between TCP and UDP? When do you use each?
63. 🟢 What is HTTP? What is HTTPS?
64. 🟡 REST vs gRPC vs GraphQL — when to use each in a design?
65. 🟡 What is long polling vs SSE vs WebSockets? When do you choose each?
66. 🟡 What is synchronous vs asynchronous communication between services?
67. 🟡 What is RPC?
68. 🟡 What is a webhook?
69. 🟡 What is service discovery?
70. 🔴 How do you reduce latency for users on the other side of the world?

---

# Part B — Building Blocks

## 7. DNS, CDN & Edge

71. 🟢 What is DNS and how does it work?
72. 🟡 How can DNS be used for load balancing (round-robin DNS, GeoDNS, latency-based routing)? What are its limitations?
73. 🟢 What is a CDN? What content should be served from a CDN?
74. 🟡 What is a push CDN vs a pull CDN?
75. 🟡 How does CDN cache invalidation work?
76. 🟡 What is edge computing?
77. 🟡 How do CDNs protect against DDoS?
78. 🔴 How do you serve dynamic or personalised content via a CDN?

---

## 8. Load Balancers & Reverse Proxies

79. 🟢 What is a load balancer? Why is it needed?
80. 🟢 What load balancing algorithms exist (round robin, weighted, least connections, least response time, IP hash, consistent hashing)?
81. 🟡 What is Layer 4 vs Layer 7 load balancing?
82. 🟡 What are health checks (active vs passive)?
83. 🟡 What are sticky sessions? Why are they discouraged?
84. 🟡 How do you make the load balancer itself highly available (active-passive, active-active, floating IP)?
85. 🟡 What is a reverse proxy? How is it different from a load balancer?
86. 🟡 What is SSL termination?
87. 🔴 How do global load balancers route traffic across regions?

---

## 9. API Gateway, Rate Limiting & Throttling

88. 🟢 What is an API Gateway? What responsibilities does it have?
89. 🟡 What is the Backend-for-Frontend (BFF) pattern?
90. 🟢 What is rate limiting? Why is it needed?
91. 🟡 What are rate-limiting algorithms (token bucket, leaky bucket, fixed window, sliding window log, sliding window counter)? Compare them.
92. 🟡 Where should rate limiting be applied (client, gateway, service)?
93. 🟡 How do you implement distributed rate limiting across many servers (Redis, Lua scripts)?
94. 🟡 What do you return when a client is rate limited (429, `Retry-After`, rate limit headers)?
95. 🟡 What is throttling vs rate limiting vs load shedding?
96. 🔴 How do you rate limit per user, per IP, per API key and per tenant at the same time?
97. 🔴 How do you handle rate limiting when Redis is unavailable (fail open vs fail closed)? 💰

---

## 10. Caching (All Layers)

98. 🟢 Where can caching be applied (client, CDN, gateway, application, distributed cache, database)?
99. 🟢 What are cache-aside, read-through, write-through, write-behind and write-around?
100. 🟡 What are cache eviction policies (LRU, LFU, FIFO, TTL)?
101. 🟡 How do you decide what to cache and for how long?
102. 🟡 What is cache invalidation? What strategies exist?
103. 🟡 What is a cache stampede / thundering herd? How do you prevent it (locking, request coalescing, early expiration)?
104. 🟡 What is cache penetration? How do Bloom filters help?
105. 🟡 What is cache avalanche (many keys expiring at once)? How do you prevent it?
106. 🟡 What are hot keys? How do you handle them (replication, local cache, key splitting)?
107. 🟡 Redis vs Memcached — when to use each?
108. 🟡 How do you scale a distributed cache (sharding, replication, Redis Cluster)?
109. 🔴 How do you keep cache and database consistent?
110. 🔴 What happens to your system if the cache cluster goes down?
111. 🔴 What is a near cache / local in-memory cache in front of a distributed cache?

---

## 11. Databases — SQL vs NoSQL & Choosing Storage

112. 🟢 What is the difference between SQL and NoSQL databases?
113. 🟢 What types of NoSQL databases exist (key-value, document, wide-column, graph, time-series, vector)? Give examples.
114. 🟡 When would you choose a relational database?
115. 🟡 When would you choose a document database (MongoDB)?
116. 🟡 When would you choose a wide-column store (Cassandra, HBase, ScyllaDB)?
117. 🟡 When would you choose a key-value store (Redis, DynamoDB)?
118. 🟡 When would you choose a graph database (Neo4j)?
119. 🟡 When would you choose a time-series database (InfluxDB, TimescaleDB)?
120. 🟡 When would you choose a vector database?
121. 🟡 What is NewSQL / distributed SQL (Spanner, CockroachDB, YugabyteDB)?
122. 🟡 What is polyglot persistence?
123. 🟡 What is an LSM tree vs a B-tree? Which databases use each and why?
124. 🔴 How do you choose a database for a new system? What questions do you ask?
125. 🔴 What are the trade-offs of using one database for everything vs multiple specialised databases?

---

## 12. Data Modeling for Scale

126. 🟡 How do you design a schema based on access patterns?
127. 🟡 When should you denormalise data?
128. 🟡 How do you model one-to-many and many-to-many relationships in NoSQL?
129. 🟡 How do you design partition keys and sort keys (DynamoDB/Cassandra)?
130. 🟡 What is a wide row and what problems do very wide partitions cause?
131. 🟡 How do you model time-series data?
132. 🟡 How do you model a social graph (followers/following)?
133. 🟡 What are secondary indexes in distributed databases and what do they cost?
134. 🔴 How do you design for "hot" partitions (celebrity users, viral posts)?
135. 🔴 How do you model data for multi-tenant SaaS?

---

## 13. Replication

136. 🟢 What is replication? Why is it needed?
137. 🟡 What is leader-follower (master-slave) replication?
138. 🟡 What is multi-leader replication? What are write conflicts?
139. 🟡 What is leaderless replication (Dynamo-style)?
140. 🟡 What is synchronous vs asynchronous replication? Trade-offs?
141. 🟡 What is replication lag? What problems does it cause?
142. 🟡 How do you achieve read-your-writes consistency with replicas?
143. 🟡 What is failover? What is split-brain?
144. 🔴 How are write conflicts resolved (last-write-wins, vector clocks, CRDTs)?
145. 🔴 What are anti-entropy, read repair, hinted handoff and Merkle trees?

---

## 14. Partitioning, Sharding & Consistent Hashing

146. 🟢 What is partitioning? What is sharding?
147. 🟡 What is horizontal vs vertical partitioning?
148. 🟡 What are range-based, hash-based, directory-based and geo-based sharding?
149. 🟡 How do you choose a shard key?
150. 🟡 What is a hot shard? How do you fix it?
151. 🟡 What problems does sharding introduce (cross-shard joins, transactions, rebalancing, unique constraints)?
152. 🟢 What is consistent hashing? Why is it needed?
153. 🟡 What are virtual nodes in consistent hashing?
154. 🟡 What happens when a node is added or removed in consistent hashing?
155. 🔴 How do you reshard a live database without downtime?
156. 🔴 What is rendezvous (highest random weight) hashing?

---

## 15. Message Queues, Pub/Sub & Event Streaming

157. 🟢 What is a message queue? Why use one?
158. 🟢 What is the difference between a queue and pub/sub?
159. 🟡 What is the difference between message queues (RabbitMQ, SQS) and event streams (Kafka, Kinesis)?
160. 🟡 What are delivery guarantees (at-most-once, at-least-once, exactly-once)?
161. 🟡 How do you guarantee ordering?
162. 🟡 What is a dead letter queue?
163. 🟡 How do queues help with load leveling and decoupling?
164. 🟡 What is back-pressure?
165. 🟡 What is fan-out on write vs fan-out on read?
166. 🔴 How do you make consumers idempotent?
167. 🔴 How do you design a delayed/scheduled message system?

---

## 16. Object Storage, Blob Storage & File Systems

168. 🟢 What is object storage? How is it different from block and file storage?
169. 🟡 When do you use S3/Blob storage vs a database for files?
170. 🟡 What are pre-signed URLs and why are they used?
171. 🟡 What are multipart uploads and resumable uploads?
172. 🟡 What is a distributed file system (HDFS, GFS)?
173. 🟡 How do you store and serve images at different resolutions (thumbnails)?
174. 🔴 How do you deduplicate files in a storage system (content hashing)?
175. 🔴 What are storage tiers (hot, warm, cold, archive) and lifecycle policies?

---

## 17. Search Systems

176. 🟢 Why can't a normal database index handle full-text search well?
177. 🟡 What is an inverted index?
178. 🟡 How do Elasticsearch/OpenSearch scale (shards and replicas)?
179. 🟡 How do you keep the search index in sync with the primary database?
180. 🟡 What is autocomplete / typeahead? Which data structure helps (trie)?
181. 🟡 How is relevance ranking done (TF-IDF, BM25)?
182. 🔴 How do you design search for 1 billion documents with sub-second latency?

---

## 18. Unique ID Generation

183. 🟢 Why is generating unique IDs hard in distributed systems?
184. 🟡 What are the options (auto-increment, UUID v4, UUID v7, ULID, Snowflake IDs, database ticket servers, range allocation)?
185. 🟡 How does Twitter Snowflake ID work (timestamp, machine ID, sequence)?
186. 🟡 What are the pros and cons of UUIDs as primary keys?
187. 🟡 Why are time-sortable IDs useful?
188. 🔴 How do you handle clock going backwards in Snowflake-style generators?
189. 🔴 How do you generate short, human-readable unique codes (e.g., order numbers, URL short codes)? 💰

---

## 19. Time, Clocks & Ordering

190. 🟡 Why can't you rely on wall-clock time across machines?
191. 🟡 What is clock skew and clock drift? What is NTP?
192. 🟡 What are logical clocks (Lamport timestamps)?
193. 🟡 What are vector clocks?
194. 🟡 What are hybrid logical clocks?
195. 🔴 How does Google Spanner use TrueTime?
196. 🔴 How do you order events across services?

---

# Part C — Distributed Systems Concepts & Patterns

## 20. Consensus, Leader Election & Coordination

197. 🟡 What is consensus? Why is it needed?
198. 🟡 How does Raft work (leader election, log replication, terms)?
199. 🟡 What is Paxos (high level)?
200. 🟡 What is leader election? How is it implemented (ZooKeeper, etcd, Consul, database lease)?
201. 🟡 What is a quorum?
202. 🟡 What is a distributed lock? How do you implement one (Redis Redlock, ZooKeeper, etcd, database)?
203. 🔴 What are fencing tokens and why are distributed locks dangerous without them?
204. 🔴 What is the Byzantine Generals problem?
205. 🔴 What is a gossip protocol?

---

## 21. Distributed Transactions & Consistency Patterns

206. 🟡 What is a distributed transaction?
207. 🟡 What is two-phase commit (2PC)? What are its problems?
208. 🟡 What is three-phase commit?
209. 🟡 What is the Saga pattern? Choreography vs orchestration?
210. 🟡 What are compensating transactions?
211. 🟡 What is the Transactional Outbox pattern?
212. 🟡 What is idempotency and how do idempotency keys work?
213. 🟡 What is CQRS?
214. 🟡 What is Event Sourcing?
215. 🔴 How do you guarantee exactly-once processing end to end? 💰
216. 🔴 What is the TCC (Try-Confirm-Cancel) pattern?

---

## 22. Reliability & Resiliency Patterns

217. 🟢 What is a timeout and why does every call need one?
218. 🟡 What is retry with exponential backoff and jitter?
219. 🟡 What is a circuit breaker?
220. 🟡 What is the bulkhead pattern?
221. 🟡 What is a fallback?
222. 🟡 What is load shedding?
223. 🟡 What is a health check? Liveness vs readiness?
224. 🟡 What is a heartbeat?
225. 🟡 What is a cascading failure? How do you prevent it?
226. 🔴 What is chaos engineering?
227. 🔴 How do you design for partial failures?
228. 🔴 What is the "metastable failure" problem (systems that stay down after load returns to normal)?

---

## 23. Data Processing — Batch, Stream, Lambda & Kappa

229. 🟡 What is batch processing? What is stream processing?
230. 🟡 What is MapReduce?
231. 🟡 What are Spark, Flink and Kafka Streams used for?
232. 🟡 What is the Lambda architecture?
233. 🟡 What is the Kappa architecture?
234. 🟡 What is ETL vs ELT?
235. 🟡 What is a data warehouse vs a data lake vs a lakehouse?
236. 🟡 What is Change Data Capture (CDC)?
237. 🔴 How do you compute real-time aggregates (counts, top-K) over a stream?
238. 🔴 What is windowing (tumbling, sliding, session) in stream processing?

---

## 24. Security in System Design

239. 🟢 How do you secure a system at the design level?
240. 🟡 Where do authentication and authorization happen in a distributed system?
241. 🟡 How do services authenticate each other (mTLS, OAuth client credentials)?
242. 🟡 What is encryption in transit vs encryption at rest?
243. 🟡 How do you manage secrets in a distributed system?
244. 🟡 How do you protect against DDoS attacks?
245. 🟡 What is a WAF?
246. 🟡 What is the principle of least privilege and zero trust?
247. 🔴 How do you design for PII and PCI data (tokenisation, vaults, masking)? 💰
248. 🔴 How do you design an audit logging system that can't be tampered with? 💰

---

## 25. Observability & Operations in System Design

249. 🟢 What are logs, metrics and traces?
250. 🟡 How do you add observability to a design?
251. 🟡 What metrics would you monitor for a high-traffic API?
252. 🟡 What is distributed tracing and why is it important in microservices?
253. 🟡 What are SLIs, SLOs and error budgets?
254. 🟡 How do you design alerting?
255. 🔴 How do you design a deployment strategy (blue/green, canary, feature flags) into the system?

---

## 26. Multi-Region, Disaster Recovery & Cost

256. 🟡 What is multi-AZ vs multi-region deployment?
257. 🟡 What is active-passive vs active-active multi-region?
258. 🟡 What are RPO and RTO?
259. 🟡 What are DR strategies (backup & restore, pilot light, warm standby, multi-site active-active)?
260. 🟡 How do you replicate data across regions? What consistency problems arise?
261. 🟡 How do you route users to the nearest region?
262. 🔴 How do you handle data residency requirements (data must stay in India)? 💰
263. 🔴 How do you estimate and reduce cloud cost in a design?
264. 🔴 What is the trade-off between cost, latency and availability in multi-region designs?

---

# Part D — High-Level Design (HLD) Case Studies

> For each design, be ready to cover: requirements (functional and non-functional), capacity estimation, API design, data model, high-level architecture, deep dives into 2–3 components, scaling, bottlenecks, failure handling and trade-offs.

## 27. Classic Beginner/Intermediate Designs

265. 🟢 Design a URL shortener (TinyURL / Bitly).
266. 🟢 Design a Pastebin.
267. 🟡 Design a rate limiter.
268. 🟡 Design a key-value store.
269. 🟡 Design a distributed cache (like Redis/Memcached).
270. 🟡 Design a unique ID generator (like Snowflake).
271. 🟡 Design a web crawler.
272. 🟡 Design a typeahead / search autocomplete system.
273. 🟡 Design a notification system (email, SMS, push).
274. 🟡 Design a counter service (likes, views) at very high scale.
275. 🟡 Design a leaderboard for a gaming platform.
276. 🟡 Design a parking lot reservation system (HLD).

---

## 28. Social Media & Content Platforms

277. 🟡 Design Twitter / X (post tweets, timeline, follow).
278. 🟡 Design Instagram (photo upload, feed, likes, comments).
279. 🟡 Design the Facebook news feed.
280. 🟡 Design LinkedIn (connections, feed, "people you may know").
281. 🟡 Design Reddit / a discussion forum (voting, ranking, comments tree).
282. 🟡 Design a comment system for a large news website.
283. 🟡 Design trending hashtags / trending topics.
284. 🟡 Design a "like" counter for posts with millions of likes per minute.
285. 🔴 Design Facebook's "people you may know" recommendation.
286. 🔴 Design a content moderation pipeline.

---

## 29. Messaging & Real-Time Systems

287. 🟡 Design WhatsApp / a chat application (1:1 and group chat, delivered/read receipts, online status).
288. 🟡 Design Slack / Microsoft Teams (channels, threads, search, presence).
289. 🟡 Design an online presence / "last seen" service.
290. 🟡 Design a live comments system for a live video stream.
291. 🟡 Design a real-time collaborative editor (Google Docs) — OT vs CRDT.
292. 🟡 Design a live sports score system.
293. 🟡 Design a push notification service for 100 million devices.
294. 🔴 Design Zoom / a video conferencing system.
295. 🔴 Design a multiplayer online game backend.

---

## 30. Media, Streaming & Storage Systems

296. 🟡 Design YouTube (upload, transcoding, streaming, recommendations).
297. 🟡 Design Netflix (catalogue, streaming, CDN, recommendations).
298. 🟡 Design Spotify (music streaming, playlists, offline downloads).
299. 🟡 Design Google Drive / Dropbox (file sync, versioning, sharing, deduplication).
300. 🟡 Design an image hosting service (like Imgur) with thumbnails.
301. 🟡 Design a video transcoding pipeline.
302. 🔴 Design a live streaming platform (Twitch / YouTube Live / Hotstar for 25 million concurrent viewers).
303. 🔴 Design S3 / an object storage system.

---

## 31. Location-Based & Marketplace Systems

304. 🟡 Design Uber / Ola (ride matching, driver location updates, ETA, pricing).
305. 🟡 Design a proximity service / Yelp ("find restaurants near me").
306. 🟡 Design Google Maps (routing, ETA, traffic).
307. 🟡 Design a food delivery system (Swiggy / Zomato / DoorDash).
308. 🟡 Design a "nearby friends" feature.
309. 🟡 Design Airbnb (listings, search, availability, booking).
310. 🔴 Design surge pricing for a ride-hailing platform.
311. 🔴 How do geohashes, quadtrees and S2/H3 cells work for location indexing?

---

## 32. E-Commerce & Booking Systems

312. 🟡 Design Amazon / Flipkart (catalogue, search, cart, checkout, orders).
313. 🟡 Design a shopping cart service.
314. 🟡 Design an inventory management system that prevents overselling.
315. 🟡 Design a flash sale system (Big Billion Days — 1 lakh items, 1 crore users in 1 minute).
316. 🟡 Design a coupon / discount / promo code system.
317. 🟡 Design BookMyShow / a movie ticket booking system (seat locking, concurrency).
318. 🟡 Design an airline / IRCTC train ticket booking system (Tatkal surge).
319. 🟡 Design a hotel reservation system.
320. 🟡 Design an order management and fulfillment system.
321. 🟡 Design a product recommendation system ("customers also bought").
322. 🔴 Design a price comparison / price tracking service.
323. 🔴 Design an e-commerce search ranking system.

---

## 33. Infrastructure & Developer Platform Systems

324. 🟡 Design a distributed message queue (like Kafka).
325. 🟡 Design a distributed job scheduler (like cron at scale).
326. 🟡 Design a logging and monitoring system (like Datadog / ELK).
327. 🟡 Design a metrics collection and alerting system (like Prometheus).
328. 🟡 Design a distributed tracing system.
329. 🟡 Design a CI/CD system (like GitHub Actions / Jenkins).
330. 🟡 Design a feature flag service.
331. 🟡 Design a configuration management service.
332. 🟡 Design an API gateway.
333. 🟡 Design a load balancer.
334. 🟡 Design a CDN.
335. 🔴 Design a distributed file system (like HDFS / GFS).
336. 🔴 Design a container orchestration system (simplified Kubernetes).
337. 🔴 Design GitHub (repositories, pull requests, code search).
338. 🔴 Design a secrets management system (like Vault).
339. 🔴 Design an authentication and SSO service (like Okta / Auth0).

---

## 34. Data, Analytics & ML Systems

340. 🟡 Design an ad click aggregation system (real-time click counting and billing).
341. 🟡 Design a top-K / heavy hitters system (top 10 most viewed videos in the last hour).
342. 🟡 Design a real-time analytics dashboard.
343. 🟡 Design an event tracking / clickstream system (like Google Analytics).
344. 🟡 Design a data pipeline from OLTP databases to a data warehouse.
345. 🔴 Design a recommendation engine.
346. 🔴 Design a search engine (like Google — crawling, indexing, ranking).
347. 🔴 Design a ChatGPT-like LLM serving system (inference, streaming tokens, rate limits, GPU scheduling).
348. 🔴 Design a RAG (retrieval-augmented generation) system over company documents.

---

## 35. Financial-Domain System Designs 💰

349. 🟡💰 Design a digital wallet (Paytm / PhonePe wallet) — add money, pay, balance, history.
350. 🟡💰 Design a payment gateway (Razorpay / Stripe) — merchants, checkout, payment methods, webhooks, refunds.
351. 🔴💰 Design a UPI-like real-time payment system (VPA resolution, PSP, NPCI switch, bank integration, collect/pay flows).
352. 🔴💰 Design a core banking ledger with double-entry bookkeeping.
353. 🔴💰 Design a fund transfer system between accounts in the same bank and across banks (NEFT/RTGS/IMPS-style).
354. 🔴💰 Design a payment reconciliation system (matching bank statements with internal records).
355. 🔴💰 Design a credit card transaction authorization system (low latency, fraud checks, limits).
356. 🔴💰 Design a real-time fraud detection system.
357. 🔴💰 Design a stock exchange / order matching engine.
358. 🔴💰 Design a stock trading platform (Zerodha / Robinhood) — orders, market data, portfolio, P&L.
359. 🔴💰 Design a market data distribution system (price ticks to millions of clients).
360. 🔴💰 Design a loan origination and approval system (KYC, credit score, underwriting, disbursal).
361. 🔴💰 Design an EMI / recurring payment (auto-debit / mandate) system.
362. 🔴💰 Design a currency exchange / forex conversion service.
363. 🔴💰 Design a KYC verification system.
364. 🔴💰 Design an expense sharing app (Splitwise).
365. 🔴💰 Design a billing and subscription system (invoices, proration, retries, dunning).
366. 🔴💰 Design a bank statement generation system for crores of accounts at month end.
367. 🔴💰 Design a transaction notification system (SMS/push for every debit/credit within seconds).
368. 🔴💰 Design an audit trail system for regulators.
369. 🔴💰 Design an idempotent payment API that never charges twice.
370. 🔴💰 Design a cashback / rewards points system.
371. 🔴💰 Design an insurance claims processing system.

---

# Part E — Follow-Up Probes (Asked After Any HLD)

## 36. Deep-Dive & Follow-Up Questions

> Interviewers ask these after you present your initial design. Practise answering them for every case study above.

372. 🟡 What happens if this component goes down?
373. 🟡 Where is the single point of failure in your design?
374. 🟡 How would the design change if traffic increased 10x? 100x?
375. 🟡 Which part of your system will become the bottleneck first?
376. 🟡 Why did you choose this database? What would happen with a different one?
377. 🟡 How do you partition this data? What is your shard key and why?
378. 🟡 How do you handle hot keys / celebrity users?
379. 🟡 What do you cache, where, and how do you invalidate it?
380. 🟡 What consistency guarantee does this feature need and how do you provide it?
381. 🟡 How do you handle duplicate requests?
382. 🟡 How do you handle a message being processed twice?
383. 🟡 How do you guarantee ordering where it matters?
384. 🟡 How do you handle a slow or failing downstream dependency?
385. 🟡 How would you monitor this system? What alerts would you set?
386. 🟡 How would you deploy changes without downtime?
387. 🟡 How do you secure the APIs and the data?
388. 🟡 How do you handle data growth over 5 years (archival, tiering)?
389. 🟡 How would you support users in multiple countries/regions?
390. 🟡 What would you do differently if you had to build an MVP in 2 weeks?
391. 🔴 What would you do differently if cost was the most important constraint?
392. 🔴 How would you migrate from the current design to a new one with zero downtime?
393. 🔴 How would you handle a full region outage?
394. 🔴 What are the trade-offs you made and what did you give up?
395. 🔴 How would you test this system before launch (load tests, chaos tests)?
396. 🔴 How do you handle schema changes in a running system?
397. 🔴 What would you change in your design if strong consistency was required everywhere? 💰

---

# Part F — Low-Level Design (LLD) / Object-Oriented Design

## 37. LLD Fundamentals

398. 🟢 What is Low-Level Design? How is it different from High-Level Design?
399. 🟢 What steps do you follow in an LLD interview (requirements, entities, relationships, class diagram, APIs, design patterns, code)?
400. 🟢 What are SOLID principles and how do they apply in LLD?
401. 🟡 What are UML class diagrams? What do association, aggregation, composition, inheritance and dependency look like?
402. 🟡 What are sequence diagrams and when would you draw one?
403. 🟡 How do you identify entities and their responsibilities from requirements?
404. 🟡 When do you use interfaces vs abstract classes in a design?
405. 🟡 How do you make an LLD extensible (Open/Closed Principle, Strategy, Factory)?
406. 🟡 How do you handle concurrency in an LLD (locks, thread-safe collections, optimistic locking)?
407. 🟡 Which design patterns are most commonly used in LLD interviews (Strategy, Factory, Singleton, Observer, State, Builder, Decorator, Command, Chain of Responsibility)?
408. 🔴 How do you balance over-engineering vs simplicity in an LLD round?
409. 🔴 How do you write testable code in an LLD round?

---

## 38. LLD Problems — Classic

410. 🟢 Design a parking lot system.
411. 🟢 Design a library management system.
412. 🟢 Design a tic-tac-toe game.
413. 🟡 Design a snake and ladder game.
414. 🟡 Design a chess game.
415. 🟡 Design an elevator system.
416. 🟡 Design a vending machine (State pattern).
417. 🟡 Design a movie ticket booking system (BookMyShow) with seat locking.
418. 🟡 Design a hotel management system.
419. 🟡 Design a car rental system.
420. 🟡 Design a food delivery app (classes, order lifecycle).
421. 🟡 Design a ride-sharing app (Uber) — riders, drivers, trips, matching strategy.
422. 🟡 Design Splitwise (expense sharing, balances, simplify debts).
423. 🟡 Design a shopping cart with discounts and coupons.
424. 🟡 Design a notification service with multiple channels (email, SMS, push).
425. 🟡 Design a logging framework (log levels, appenders, formatters).
426. 🟡 Design a file system (files, directories, permissions).
427. 🟡 Design a calendar / meeting room scheduler.
428. 🟡 Design Stack Overflow (questions, answers, votes, reputation).
429. 🟡 Design a social media feed (posts, follows, likes) — classes only.
430. 🔴 Design a cache with pluggable eviction policies (LRU, LFU, FIFO).
431. 🔴 Design a rate limiter class with multiple algorithms.
432. 🔴 Design an in-memory key-value store with transactions (begin, commit, rollback).
433. 🔴 Design a pub/sub messaging system (in-memory).
434. 🔴 Design a task scheduler with priorities and retries.

---

## 39. LLD Problems — Financial & Business Domain 💰

435. 🟡💰 Design an ATM machine (card, PIN, withdraw, deposit, balance, states).
436. 🟡💰 Design a bank account system (savings, current, transactions, interest, limits).
437. 🟡💰 Design a digital wallet (add money, transfer, transaction history, limits).
438. 🟡💰 Design a payment processing module supporting UPI, card and net banking (Strategy + Factory).
439. 🔴💰 Design a loan EMI calculator and repayment schedule module.
440. 🔴💰 Design a stock exchange order book (buy/sell orders, matching by price-time priority).
441. 🔴💰 Design a credit card billing system (statement cycle, minimum due, interest, late fees).
442. 🔴💰 Design a fraud rule engine (configurable rules, Chain of Responsibility).
443. 🔴💰 Design a maker-checker approval workflow.
444. 🔴💰 Design an invoice and billing system with taxes (GST) and discounts.
445. 🔴💰 Design a currency converter with pluggable rate providers.
446. 🔴💰 Design a rewards / loyalty points system.

---

## 40. LLD Problems — Infrastructure Components

447. 🟡 Design an LRU cache (O(1) get/put).
448. 🟡 Design a thread pool.
449. 🟡 Design a connection pool.
450. 🟡 Design a circuit breaker.
451. 🟡 Design a retry mechanism with exponential backoff.
452. 🟡 Design a URL shortener (classes and encoding logic).
453. 🟡 Design a job queue with workers.
454. 🔴 Design a consistent hashing ring.
455. 🔴 Design a distributed ID generator (Snowflake) class.
456. 🔴 Design a bloom filter.
457. 🔴 Design an event bus with subscribers and filters.
458. 🔴 Design a plugin/middleware pipeline (like ASP.NET Core middleware).

---

# Part G — Practice

## 41. Trade-Off Questions

459. 🟡 SQL vs NoSQL — how do you decide?
460. 🟡 Strong consistency vs eventual consistency — when do you choose each?
461. 🟡 Monolith vs microservices for a new startup?
462. 🟡 REST vs gRPC for internal services?
463. 🟡 Polling vs WebSockets vs SSE?
464. 🟡 Push (fan-out on write) vs pull (fan-out on read) for a news feed?
465. 🟡 Cache-aside vs write-through?
466. 🟡 Synchronous vs asynchronous processing?
467. 🟡 Queue (RabbitMQ) vs log (Kafka)?
468. 🟡 Normalisation vs denormalisation?
469. 🟡 Vertical vs horizontal scaling?
470. 🟡 Range sharding vs hash sharding?
471. 🟡 UUID vs auto-increment vs Snowflake IDs?
472. 🟡 Optimistic vs pessimistic locking? 💰
473. 🟡 Batch vs stream processing?
474. 🟡 Build vs buy (e.g., own auth server vs Auth0)?
475. 🟡 Server-side rendering vs client-side rendering (from a backend perspective)?
476. 🔴 Active-active vs active-passive multi-region?
477. 🔴 Latency vs consistency (PACELC) for a global product?
478. 🔴 Cost vs performance — give an example where you chose the cheaper option.
479. 🔴 Exactly-once vs at-least-once + idempotency? 💰

---

## 42. Tricky Questions

480. 🟡 Can a system be both highly available and strongly consistent?
481. 🟡 Is adding a cache always a good idea?
482. 🟡 Is horizontal scaling always better than vertical scaling?
483. 🟡 Do microservices automatically make a system scalable?
484. 🟡 Why can't you just add more servers to fix a slow database?
485. 🟡 Is Kafka a database?
486. 🟡 Why is "exactly-once delivery" considered impossible in distributed systems?
487. 🟡 If you have 3 replicas, can you still lose data?
488. 🟡 Why can a load balancer itself become a bottleneck?
489. 🟡 Why do celebrities break naive news feed designs?
490. 🟡 Why can't you use `SELECT COUNT(*)` for a like counter at Instagram scale?
491. 🟡 Why can't you store all chat messages in one database table forever?
492. 🟡 Why is generating a short URL with `hash(url)` problematic?
493. 🟡 Why does consistent hashing need virtual nodes?
494. 🟡 Why do distributed locks need fencing tokens?
495. 🟡 Why is two-phase commit avoided in microservices?
496. 🟡 Why is a "last write wins" strategy dangerous?
497. 🟡 Why can retries cause an outage instead of fixing one?
498. 🟡 Why can't you trust timestamps from different servers to order events?
499. 🟡 Is 99.99% availability for every service in a chain enough for 99.99% overall?
500. 🔴 How do you prevent overselling the last item when 10,000 users click "buy" at the same moment?
501. 🔴 How do you prevent two people from booking the same seat?
502. 🔴 How do you prevent a payment from being charged twice when the client retries after a timeout? 💰
503. 🔴 How do you design a system that must never lose a single transaction? 💰
504. 🔴 What happens if the clock on one server jumps 10 minutes forward?

---

## 43. Scenario-Based Questions

505. 🟡 Your API's database is at 90% CPU and traffic will double next month. What do you do?
506. 🟡 Your read replicas show stale data and users complain. How do you fix it?
507. 🟡 A viral post causes one cache key to receive 1 million requests per second. What do you do?
508. 🟡 Your notification system sends duplicate SMS messages. How do you fix it?
509. 🟡 Your search results don't show newly added products for 10 minutes. Why, and how do you improve it?
510. 🟡 Your video uploads fail for large files on mobile networks. How do you redesign uploads?
511. 🟡 Your system must support 10x traffic during a sale for 2 hours. How do you prepare?
512. 🟡 One microservice's slowness is causing timeouts across the whole system. What do you do?
513. 🟡 Your Kafka consumers can't keep up during peak hours. How do you scale?
514. 🟡 A region of your cloud provider goes down. What happens to your system and users?
515. 🟡 Product wants "real-time" analytics, but your pipeline is daily batch. How do you evolve it?
516. 🟡 You need to move from a single database to a sharded setup without downtime. How?
517. 🔴 Your payment provider's API times out and you don't know whether the payment succeeded. What do you do? 💰
518. 🔴 Your daily reconciliation shows ₹2 lakh mismatch between your ledger and the bank's statement. How do you design the system to find and fix it? 💰
519. 🔴 Regulators require that all customer data stays in India while your system runs in multiple regions. How do you redesign? 💰
520. 🔴 Your monthly cloud bill doubled. How do you find and reduce the cost without hurting reliability?
521. 🔴 Your team must design a system for 100 users today that could grow to 100 million. How do you avoid both over- and under-engineering?
522. 🔴 You inherit a system with no monitoring and frequent outages. What is your 30-60-90 day plan?

---

## 44. Rapid-Fire Round

523. 🟢 What does CAP stand for?
524. 🟢 What does ACID stand for?
525. 🟢 What does BASE stand for?
526. 🟢 What does CDN stand for?
527. 🟢 What is the 80/20 rule in caching?
528. 🟢 How many seconds are in a day (approx.)?
529. 🟢 How much downtime per year does 99.9% allow?
530. 🟢 Which data structure is used for autocomplete?
531. 🟢 Which data structure checks "possibly in set" with no false negatives?
532. 🟢 Which algorithm distributes keys with minimal movement when nodes change?
533. 🟢 Which rate-limiting algorithm allows bursts up to a bucket size?
534. 🟡 Which consensus algorithm do etcd and many modern databases use?
535. 🟡 What does R + W > N guarantee?
536. 🟡 What are the parts of a Snowflake ID?
537. 🟡 Which indexing structures are used for location search?
538. 🟡 What is fan-out on write in one line?
539. 🟡 What is a hot partition in one line?
540. 🟡 What is split-brain in one line?
541. 🟡 What is a quorum in one line?
542. 🟡 What is RPO vs RTO in one line?
543. 🔴 What is the difference between linearizability and serializability in one line?
544. 🔴 What is the difference between OT and CRDT in one line?
545. 🔴 What is the difference between Lambda and Kappa architecture in one line?
546. 🔴 What is the difference between an LSM tree and a B-tree in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design (HLD & LLD).
