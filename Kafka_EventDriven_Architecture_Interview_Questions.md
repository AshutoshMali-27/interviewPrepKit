# 🎯 Kafka & Event-Driven Architecture Interview Questions — Part 7 (Questions Only)

> **Scope:** Event-Driven Architecture (EDA) in microservices — concepts, event design, patterns (Outbox, Inbox, Saga, CQRS, Event Sourcing, Event-Carried State Transfer), consistency and reliability — and **Apache Kafka in depth**: architecture, topics & partitions, producers, consumers & consumer groups, offsets, delivery semantics, transactions & exactly-once, replication, KRaft, retention & compaction, Schema Registry, Kafka Connect & CDC, Kafka Streams/ksqlDB, security, performance, operations, and Kafka with .NET (`Confluent.Kafka`, MassTransit). Plus tricky questions, predict-the-behavior snippets, scenarios and system design.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks, trading, payments, fintech), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers Kafka 3.x/4.x (KRaft, no ZooKeeper in 4.0) and modern .NET.**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Event-Driven Architecture**
1. EDA Fundamentals
2. Events, Commands & Messages
3. Event Design & Modeling
4. Event Types & Communication Styles
5. Choreography vs Orchestration
6. Consistency in EDA
7. Reliability Patterns (Outbox, Inbox, Idempotency, DLQ)
8. Saga Pattern with Events
9. CQRS & Event Sourcing
10. Event Versioning & Schema Evolution
11. Ordering, Duplicates & Time
12. Observability & Debugging in EDA
13. Testing Event-Driven Systems
14. EDA Anti-Patterns

**Part B — Apache Kafka**
15. Kafka Fundamentals
16. Kafka Architecture (Brokers, Controller, ZooKeeper vs KRaft)
17. Topics & Partitions
18. Replication, Leaders, ISR & Durability
19. Producers
20. Producer Delivery Guarantees & Idempotence
21. Consumers & Consumer Groups
22. Offsets & Commit Strategies
23. Rebalancing
24. Delivery Semantics & Exactly-Once
25. Kafka Transactions
26. Retention, Log Compaction & Storage
27. Message Format, Keys, Headers & Serialization
28. Schema Registry (Avro, Protobuf, JSON Schema)
29. Error Handling, Retries & Dead Letter Topics
30. Kafka Connect & Change Data Capture (Debezium)
31. Kafka Streams & ksqlDB / Stream Processing
32. Kafka Security
33. Performance & Tuning
34. Monitoring & Operations
35. Kafka in Docker, Kubernetes & Cloud (Confluent Cloud, MSK, Event Hubs)
36. Kafka vs RabbitMQ vs Azure Service Bus vs Others

**Part C — Kafka with .NET**
37. Confluent.Kafka Client in .NET
38. Building Producers in ASP.NET Core
39. Building Consumers as BackgroundServices
40. MassTransit / Other Frameworks with Kafka

**Part D — Practice**
41. Financial-Domain EDA & Kafka Questions 💰
42. Tricky Questions
43. Predict the Behavior (Config & Code Snippets)
44. Scenario-Based Questions — Event-Driven Design
45. Scenario-Based Questions — Kafka Production Issues
46. System Design Scenarios
47. Hands-On Tasks
48. Rapid-Fire Round

---

# Part A — Event-Driven Architecture

## 1. EDA Fundamentals

1. 🟢 What is event-driven architecture (EDA)?
2. 🟢 What is an event?
3. 🟢 What are the main components of EDA (event producer, event broker/channel, event consumer)?
4. 🟢 What are the benefits of event-driven architecture?
5. 🟢 What are the challenges and drawbacks of EDA?
6. 🟢 How is EDA different from request/response (REST) architecture?
7. 🟡 How does EDA reduce temporal coupling between services?
8. 🟡 What is loose coupling in EDA? Is EDA always loosely coupled?
9. 🟡 What is the difference between event-driven and message-driven systems?
10. 🟡 What is reactive architecture and the Reactive Manifesto?
11. 🟡 When should you NOT use event-driven architecture?
12. 🟡 What is an event broker vs a message queue vs an event stream?
13. 🟡 What is an event backbone / event mesh?
14. 🟡 What is "event-first" thinking?
15. 🔴 How does EDA affect team autonomy and organisational design?
16. 🔴 How do you convince stakeholders to adopt EDA for an existing synchronous system?

---

## 2. Events, Commands & Messages

17. 🟢 What is the difference between an event, a command and a query?
18. 🟢 Why are events named in the past tense (`OrderPlaced`) and commands in the imperative (`PlaceOrder`)?
19. 🟡 Who owns an event — the producer or the consumer? Who owns a command?
20. 🟡 Can an event be rejected? Can a command be rejected?
21. 🟡 How many consumers does an event usually have vs a command?
22. 🟡 What is a domain event vs an integration event?
23. 🟡 Should domain events be published directly to Kafka? Why or why not?
24. 🟡 What is a message envelope? What metadata should every event contain (EventId, EventType, Version, Timestamp, Source, CorrelationId, CausationId, Key)?
25. 🟡 What is the CloudEvents specification?
26. 🟡 What is CorrelationId vs CausationId?
27. 🔴 When would you send a command over Kafka instead of an event?

---

## 3. Event Design & Modeling

28. 🟢 What makes a good event?
29. 🟡 What is a thin event (notification) vs a fat event (state transfer)? Pros and cons?
30. 🟡 What is a delta event vs a snapshot event?
31. 🟡 How much data should an event carry?
32. 🟡 What is Event Storming? How does it help discover events?
33. 🟡 How do you name events and topics consistently?
34. 🟡 Should one topic contain one event type or multiple event types? Trade-offs?
35. 🟡 How do you design events so that consumers don't need to call back the producer?
36. 🟡 Should events contain sensitive data (PII, card numbers)? How do you handle it? 💰
37. 🟡 How do you handle very large payloads in events (Claim Check pattern)?
38. 🔴 What is the difference between business events and technical/CRUD events (`CustomerUpdated` vs `CustomerAddressChanged`)?
39. 🔴 Why are CRUD-style events often considered an anti-pattern?
40. 🔴 How do you design events for a public event stream consumed by other organisations?

---

## 4. Event Types & Communication Styles

41. 🟡 What is Event Notification?
42. 🟡 What is Event-Carried State Transfer (ECST)?
43. 🟡 What is Event Sourcing?
44. 🟡 What is CQRS and how does it relate to events?
45. 🟡 What is publish-subscribe vs point-to-point messaging?
46. 🟡 What is fan-out?
47. 🟡 What is event streaming vs event messaging?
48. 🟡 What is the Request-Reply pattern over events? When is it used?
49. 🟡 What is a webhook? How is it related to EDA?
50. 🔴 What is the difference between a queue-based system (RabbitMQ) and a log-based system (Kafka) conceptually?

---

## 5. Choreography vs Orchestration

51. 🟢 What is choreography in EDA?
52. 🟢 What is orchestration?
53. 🟡 What are the pros and cons of choreography?
54. 🟡 What are the pros and cons of orchestration?
55. 🟡 When would you choose choreography vs orchestration?
56. 🟡 How do you visualise or track a business process in a choreographed system?
57. 🟡 What is a process manager?
58. 🔴 What tools support orchestration (MassTransit state machines, NServiceBus sagas, Temporal, Camunda/Zeebe, Durable Functions)?
59. 🔴 Can you mix choreography and orchestration? Give an example.

---

## 6. Consistency in EDA

60. 🟢 What is eventual consistency?
61. 🟡 How do you explain eventual consistency to business stakeholders?
62. 🟡 How do you handle the UI when data is eventually consistent (optimistic UI, polling, read-your-writes)?
63. 🟡 What is read-your-own-writes consistency? How do you achieve it in EDA?
64. 🟡 What is the dual-write problem?
65. 🟡 Why can't you write to the database and publish to Kafka atomically?
66. 🔴 What are the options to solve dual writes (Transactional Outbox, CDC, Listen-to-yourself, event sourcing)?
67. 🔴 What is the "listen to yourself" pattern?
68. 🔴 Where is strong consistency mandatory and eventual consistency unacceptable? 💰

---

## 7. Reliability Patterns

69. 🟡 What is the Transactional Outbox pattern? Explain step by step.
70. 🟡 How is the outbox table published — polling publisher vs log tailing (CDC with Debezium)? Pros and cons?
71. 🟡 How do you implement the Outbox pattern with EF Core in .NET?
72. 🟡 What happens if the outbox publisher crashes after publishing but before marking the row as sent?
73. 🟡 How do you clean up the outbox table?
74. 🟡 What is the Inbox pattern?
75. 🟡 What is an idempotent consumer? Name ways to achieve idempotency (processed-message table, unique constraints, upserts, natural idempotent operations, version checks).
76. 🟡 What is a Dead Letter Queue / Dead Letter Topic?
77. 🟡 What is a poison message?
78. 🟡 What are retry topics with backoff (retry-5s, retry-1m, DLT)?
79. 🟡 What is a parking lot queue?
80. 🔴 How do you design a reprocessing tool for DLQ messages?
81. 🔴 What is guaranteed delivery? What does it really guarantee?
82. 🔴 How do you guarantee that no events are lost end to end (producer → broker → consumer → DB)?

---

## 8. Saga Pattern with Events

83. 🟢 What is the Saga pattern?
84. 🟡 How does a choreography-based saga work with Kafka events?
85. 🟡 How does an orchestration-based saga work with Kafka commands and replies?
86. 🟡 What are compensating transactions?
87. 🟡 What are pivot, compensatable and retriable steps?
88. 🟡 How do you handle saga timeouts?
89. 🟡 How do you store saga state?
90. 🔴 What are saga anomalies (lack of isolation) and countermeasures (semantic lock, commutative updates, pessimistic view, reread value, version file)?
91. 🔴 What happens if a compensating action fails?
92. 🔴 How do you make each saga step idempotent?
93. 🔴💰 Design an event-driven saga for a fund transfer between two banks.
94. 🔴 Design an event-driven saga for order → inventory → payment → shipping.

---

## 9. CQRS & Event Sourcing

95. 🟢 What is CQRS?
96. 🟡 How does EDA enable CQRS (events update read models)?
97. 🟡 What are projections / materialized views?
98. 🟡 How do you rebuild a read model from Kafka events?
99. 🟢 What is Event Sourcing?
100. 🟡 What is the difference between Event Sourcing and event-driven architecture?
101. 🟡 Can Kafka be used as an event store? What are its limitations (no per-aggregate query, optimistic concurrency)?
102. 🟡 What are snapshots in Event Sourcing?
103. 🟡 What dedicated event stores exist (EventStoreDB/KurrentDB, Marten, Axon)?
104. 🔴 How do you handle schema changes of stored events (upcasting)?
105. 🔴 When is Event Sourcing a bad fit?
106. 🔴💰 Why is Event Sourcing a natural fit for ledgers and audit trails?

---

## 10. Event Versioning & Schema Evolution

107. 🟢 Why do events need versioning?
108. 🟡 What are backward, forward and full compatibility?
109. 🟡 Which schema changes are safe (adding optional fields) and which are breaking (removing, renaming, changing types)?
110. 🟡 What versioning strategies exist (version in event type, version field, new topic, schema registry compatibility)?
111. 🟡 What is the Tolerant Reader pattern?
112. 🟡 What is an upcaster?
113. 🟡 How do you migrate consumers when a breaking change is unavoidable?
114. 🔴 How do you deprecate an old event version that has many consumers?
115. 🔴 Should you share event contracts via a NuGet package? What are the risks?

---

## 11. Ordering, Duplicates & Time

116. 🟡 Why is message ordering hard in distributed systems?
117. 🟡 When does ordering matter? Give examples. 💰
118. 🟡 How do you guarantee ordering per entity (partition key)?
119. 🟡 What happens to ordering when you retry failed messages?
120. 🟡 How do you handle out-of-order events (sequence numbers, versions, ignoring older events)?
121. 🟡 Why are duplicates inevitable with at-least-once delivery?
122. 🟡 What is event time vs processing time vs ingestion time?
123. 🔴 Why can't you rely on wall-clock timestamps from different services to order events?
124. 🔴 What are logical clocks / Lamport timestamps / vector clocks (high level)?
125. 🔴 What are late-arriving events and watermarks in stream processing?

---

## 12. Observability & Debugging in EDA

126. 🟡 Why is debugging event-driven systems harder than synchronous systems?
127. 🟡 How do you propagate trace context through Kafka messages (W3C `traceparent` in headers)?
128. 🟡 How do you use OpenTelemetry with Kafka producers and consumers in .NET?
129. 🟡 What metrics should you monitor in an event-driven system (consumer lag, processing time, error rate, DLQ size, throughput)?
130. 🟡 How do you find "where did my event go"?
131. 🟡 What is an event catalog? What tools exist (AsyncAPI, EventCatalog)?
132. 🟡 What is AsyncAPI?
133. 🔴 How do you build an end-to-end business flow view across many services and topics?

---

## 13. Testing Event-Driven Systems

134. 🟡 How do you unit test an event handler / consumer?
135. 🟡 How do you integration test with a real Kafka broker (Testcontainers)?
136. 🟡 How do you test producers and consumers against schema compatibility?
137. 🟡 What is contract testing for events (Pact message contracts)?
138. 🟡 How do you test idempotency (sending the same event twice)?
139. 🟡 How do you test sagas and compensations?
140. 🔴 How do you test eventual consistency in end-to-end tests without flaky sleeps?
141. 🔴 How do you test behaviour under broker failure, rebalances and duplicates?

---

## 14. EDA Anti-Patterns

142. 🟡 What is the "event soup" / spaghetti events anti-pattern?
143. 🟡 What is using events as remote procedure calls?
144. 🟡 What is a "god event" that every service listens to?
145. 🟡 What is leaking internal domain models into events?
146. 🟡 What is "passive-aggressive events" (events that are actually commands)?
147. 🟡 What is ignoring idempotency?
148. 🟡 What is a shared database alongside events?
149. 🔴 What is "event-driven distributed monolith"?
150. 🔴 What is overusing Event Sourcing everywhere?

---

# Part B — Apache Kafka

## 15. Kafka Fundamentals

151. 🟢 What is Apache Kafka?
152. 🟢 What are the main use cases of Kafka (messaging, event streaming, log aggregation, CDC, metrics, stream processing)?
153. 🟢 What are the core concepts of Kafka (producer, consumer, broker, topic, partition, offset, consumer group)?
154. 🟢 Why is Kafka called a distributed commit log?
155. 🟢 What makes Kafka fast (sequential disk I/O, page cache, zero-copy, batching, compression)?
156. 🟢 Is Kafka a queue or a pub/sub system? Can it be both?
157. 🟡 What is the difference between Kafka and traditional message queues?
158. 🟡 Does Kafka delete a message after it is consumed?
159. 🟡 What is the difference between Apache Kafka and Confluent Platform?
160. 🟡 What is Kafka's pull-based consumption model? Why pull instead of push?
161. 🟡 What is a Kafka record? What does it contain (key, value, headers, timestamp, offset, partition)?
162. 🟡 What are the Kafka APIs (Producer, Consumer, Streams, Connect, Admin)?

---

## 16. Kafka Architecture

163. 🟢 What is a Kafka broker?
164. 🟢 What is a Kafka cluster?
165. 🟡 What is the controller in Kafka? What does it do?
166. 🟡 What was ZooKeeper's role in Kafka?
167. 🟡 What is KRaft mode? Why did Kafka remove ZooKeeper?
168. 🟡 What changed in Kafka 4.0 (ZooKeeper removed, KRaft only, new consumer rebalance protocol by default)?
169. 🟡 What are controller nodes vs broker nodes in KRaft? What is combined mode?
170. 🟡 What is the metadata log (`__cluster_metadata`)?
171. 🟡 How do clients discover the cluster (bootstrap servers, metadata requests)?
172. 🟡 What are `listeners` and `advertised.listeners`? Why do they matter in Docker/Kubernetes?
173. 🔴 What is rack awareness?
174. 🔴 What is tiered storage in Kafka?
175. 🔴 What are Kafka 4.x "Queues for Kafka" (share groups, KIP-932) at a high level?

---

## 17. Topics & Partitions

176. 🟢 What is a topic?
177. 🟢 What is a partition? Why are topics split into partitions?
178. 🟢 What is an offset?
179. 🟡 How does Kafka decide which partition a message goes to (key hash, round robin / sticky partitioner, custom partitioner)?
180. 🟡 What happens if a message has no key?
181. 🟡 What is the sticky partitioner?
182. 🟡 How is ordering guaranteed in Kafka? Is it per topic or per partition?
183. 🟡 How do you choose the number of partitions for a topic?
184. 🟡 What is the relationship between partitions and consumer parallelism?
185. 🟡 Can you increase the number of partitions? What happens to key-to-partition mapping?
186. 🟡 Can you decrease the number of partitions?
187. 🟡 What are the costs of having too many partitions?
188. 🟡 What is a hot partition? What causes it (skewed keys)? How do you fix it?
189. 🟡 What are segments and indexes inside a partition?
190. 🟡 What are internal topics (`__consumer_offsets`, `__transaction_state`)?
191. 🟡 What is `auto.create.topics.enable`? Why disable it in production?
192. 🔴 How do you choose a partition key for a banking system (account ID, customer ID)? 💰

---

## 18. Replication, Leaders, ISR & Durability

193. 🟢 What is replication in Kafka?
194. 🟢 What is the replication factor?
195. 🟡 What is a leader replica and follower replica?
196. 🟡 What is the ISR (In-Sync Replicas) list?
197. 🟡 When is a replica removed from the ISR (`replica.lag.time.max.ms`)?
198. 🟡 What is `min.insync.replicas`? How does it work with `acks=all`?
199. 🟡 What happens when the number of ISRs drops below `min.insync.replicas`?
200. 🟡 What is leader election? What happens when a broker fails?
201. 🟡 What is unclean leader election? Why is it dangerous? 💰
202. 🟡 What is the high watermark? What is the log end offset (LEO)?
203. 🟡 Can consumers read messages that are not yet replicated to all ISRs?
204. 🟡 What is preferred leader election?
205. 🔴 What is the recommended durability configuration (RF=3, `min.insync.replicas=2`, `acks=all`)?
206. 🔴 How many broker failures can a topic with RF=3 and `min.insync.replicas=2` tolerate for writes? For reads?
207. 🔴 How does Kafka replicate across data centres (MirrorMaker 2, Cluster Linking)?

---

## 19. Producers

208. 🟢 What is a Kafka producer?
209. 🟢 What happens when a producer sends a message (serialization → partitioner → batch → send → ack)?
210. 🟡 What are `acks=0`, `acks=1` and `acks=all`? Trade-offs?
211. 🟡 What is producer batching (`batch.size`, `linger.ms`)?
212. 🟡 What is producer compression (`compression.type`: gzip, snappy, lz4, zstd)?
213. 🟡 What is `buffer.memory` and `max.block.ms`?
214. 🟡 What is `max.in.flight.requests.per.connection` and how does it affect ordering?
215. 🟡 What are `retries`, `retry.backoff.ms` and `delivery.timeout.ms`?
216. 🟡 What is `request.timeout.ms`?
217. 🟡 What is a synchronous send vs an asynchronous send with a callback?
218. 🟡 What happens if the producer sends faster than the broker can accept?
219. 🟡 Is a Kafka producer thread-safe? Should you share one instance?
220. 🟡 What is `message.max.bytes` / `max.request.size`? What happens if a message is too large?
221. 🔴 What happens to buffered messages if the producer process crashes before they're sent?
222. 🔴 What is `Flush()` and why is it important on shutdown?

---

## 20. Producer Delivery Guarantees & Idempotence

223. 🟡 What is an idempotent producer (`enable.idempotence=true`)?
224. 🟡 How does the idempotent producer prevent duplicates (producer ID, sequence numbers)?
225. 🟡 Is idempotence enabled by default in recent Kafka clients?
226. 🟡 What configs does idempotence require (`acks=all`, `max.in.flight <= 5`, retries > 0)?
227. 🟡 Does the idempotent producer prevent duplicates across producer restarts? Across application-level retries?
228. 🔴 What is the difference between producer idempotence and consumer idempotence?
229. 🔴 Can retries cause message reordering? How does idempotence prevent it?

---

## 21. Consumers & Consumer Groups

230. 🟢 What is a Kafka consumer?
231. 🟢 What is a consumer group?
232. 🟢 How are partitions assigned to consumers in a group?
233. 🟡 What happens if there are more consumers than partitions?
234. 🟡 What happens if there are fewer consumers than partitions?
235. 🟡 How do multiple consumer groups read the same topic independently?
236. 🟡 What is the poll loop? What does `poll()` / `Consume()` do?
237. 🟡 What are `max.poll.records` and `max.poll.interval.ms`?
238. 🟡 What are `session.timeout.ms` and `heartbeat.interval.ms`?
239. 🟡 What happens if processing a batch takes longer than `max.poll.interval.ms`?
240. 🟡 What is `auto.offset.reset` (`earliest`, `latest`, `none`)? When does it apply?
241. 🟡 What are `fetch.min.bytes`, `fetch.max.wait.ms` and `max.partition.fetch.bytes`?
242. 🟡 Is a Kafka consumer thread-safe?
243. 🟡 How do you process messages in parallel within a single partition? What do you lose?
244. 🟡 What is consumer lag? How do you measure it?
245. 🟡 What is `isolation.level` (`read_uncommitted`, `read_committed`)?
246. 🟡 What is a static group membership (`group.instance.id`)?
247. 🔴 How do you pause and resume consumption of specific partitions (back-pressure)?
248. 🔴 How do you seek to a specific offset or timestamp?
249. 🔴 What is follower fetching (reading from the closest replica)?

---

## 22. Offsets & Commit Strategies

250. 🟢 What is an offset commit?
251. 🟢 Where are committed offsets stored (`__consumer_offsets`)?
252. 🟡 What is auto-commit (`enable.auto.commit`, `auto.commit.interval.ms`)? What are its risks?
253. 🟡 What is manual commit? Synchronous vs asynchronous commit?
254. 🟡 What is committing before processing vs after processing? Which semantics does each give?
255. 🟡 What is the committed offset vs the current position?
256. 🟡 Which offset should you commit — the last processed offset or the next offset to read?
257. 🟡 How do you commit offsets per partition?
258. 🟡 What is `StoreOffset` + auto-commit in `Confluent.Kafka` (`enable.auto.offset.store=false`)?
259. 🟡 What happens to committed offsets when retention deletes old messages (`offsets.retention.minutes`)?
260. 🔴 How do you store offsets in your own database together with processing results (exactly-once with external DB)?
261. 🔴 How do you reset consumer group offsets (`kafka-consumer-groups --reset-offsets`)? When would you?

---

## 23. Rebalancing

262. 🟡 What is a consumer group rebalance?
263. 🟡 What triggers a rebalance (consumer joins/leaves/crashes, partitions added, poll timeout)?
264. 🟡 What is the group coordinator?
265. 🟡 What are partition assignment strategies (Range, RoundRobin, Sticky, CooperativeSticky)?
266. 🟡 What is eager rebalancing vs incremental cooperative rebalancing?
267. 🟡 What is the "stop-the-world" rebalance problem?
268. 🟡 What is the new consumer rebalance protocol (KIP-848) in Kafka 4.0?
269. 🟡 What are partition assigned / revoked / lost callbacks? What should you do in them?
270. 🔴 Why can a rebalance cause duplicate processing?
271. 🔴 How do you reduce rebalances in Kubernetes deployments (static membership, graceful shutdown)?
272. 🔴 What is a rebalance storm and how do you diagnose it?

---

## 24. Delivery Semantics & Exactly-Once

273. 🟢 What are at-most-once, at-least-once and exactly-once semantics?
274. 🟡 How do you achieve at-most-once in Kafka?
275. 🟡 How do you achieve at-least-once in Kafka?
276. 🟡 What does exactly-once semantics (EOS) mean in Kafka?
277. 🟡 Is exactly-once possible end to end when the consumer writes to an external database?
278. 🟡 What is "effectively-once" processing?
279. 🔴 What is the read-process-write (consume-transform-produce) pattern with EOS?
280. 🔴 What is `processing.guarantee=exactly_once_v2` in Kafka Streams?
281. 🔴💰 How do you guarantee that a payment event results in exactly one debit?

---

## 25. Kafka Transactions

282. 🟡 What are Kafka transactions?
283. 🟡 What is `transactional.id`? Why must it be stable across restarts?
284. 🟡 What are `InitTransactions`, `BeginTransaction`, `CommitTransaction`, `AbortTransaction`?
285. 🟡 How do you send consumer offsets inside a producer transaction (`SendOffsetsToTransaction`)?
286. 🟡 What is a transaction coordinator? What is `__transaction_state`?
287. 🟡 What are control records / transaction markers?
288. 🟡 What is producer fencing / zombie fencing?
289. 🟡 How do `read_committed` consumers behave with open transactions (Last Stable Offset)?
290. 🔴 Do Kafka transactions include your database writes? Why not?
291. 🔴 What is the performance cost of Kafka transactions?
292. 🔴 What is a hanging transaction and how is it detected?

---

## 26. Retention, Log Compaction & Storage

293. 🟢 What is retention in Kafka?
294. 🟡 What are time-based (`retention.ms`) and size-based (`retention.bytes`) retention?
295. 🟡 What is `cleanup.policy` (`delete`, `compact`, `compact,delete`)?
296. 🟡 What is log compaction? How does it work?
297. 🟡 What is a tombstone message? How do you delete a key in a compacted topic?
298. 🟡 What is `delete.retention.ms`?
299. 🟡 When would you use a compacted topic (latest state per key, KTables, config, CDC)?
300. 🟡 Does compaction guarantee only one message per key at any time?
301. 🟡 What are segments (`segment.bytes`, `segment.ms`) and why does retention apply per segment?
302. 🔴 Can you use Kafka as a permanent store of events? What are the considerations?
303. 🔴 How do you handle GDPR "right to be forgotten" in Kafka (compaction + tombstones, crypto-shredding)? 💰

---

## 27. Message Format, Keys, Headers & Serialization

304. 🟢 What is the role of the message key?
305. 🟢 What are message headers? What do you store in them?
306. 🟡 What serialization formats are used with Kafka (JSON, Avro, Protobuf, JSON Schema, MessagePack)?
307. 🟡 JSON vs Avro vs Protobuf — pros and cons?
308. 🟡 What are serializers and deserializers (SerDes)?
309. 🟡 What is message timestamp (`CreateTime` vs `LogAppendTime`)?
310. 🟡 What is the maximum message size and how do you change it (broker, topic, producer, consumer settings)?
311. 🟡 What happens if a consumer can't deserialize a message?
312. 🔴 Why should you avoid putting large binary payloads in Kafka?

---

## 28. Schema Registry

313. 🟡 What is Schema Registry? Why is it needed?
314. 🟡 How does Schema Registry work with producers and consumers (schema ID in the message)?
315. 🟡 What is a subject? What are subject naming strategies (TopicNameStrategy, RecordNameStrategy, TopicRecordNameStrategy)?
316. 🟡 What are compatibility modes (BACKWARD, FORWARD, FULL, NONE, *_TRANSITIVE)?
317. 🟡 Which compatibility mode should you use and why?
318. 🟡 How do you evolve an Avro schema safely (defaults for new fields)?
319. 🟡 How do you evolve a Protobuf schema safely (field numbers, reserved)?
320. 🟡 What happens when a producer tries to register an incompatible schema?
321. 🟡 What alternatives to Confluent Schema Registry exist (Apicurio, AWS Glue Schema Registry, Azure Schema Registry)?
322. 🔴 How do you put multiple event types in one topic with Schema Registry?
323. 🔴 What is data contract / schema validation on the broker side?

---

## 29. Error Handling, Retries & Dead Letter Topics

324. 🟡 What types of errors can occur when consuming (deserialization, transient, business, poison)?
325. 🟡 Should a consumer stop, skip, retry or dead-letter a failing message? How do you decide?
326. 🟡 Why does Kafka not have built-in DLQ like RabbitMQ? How do you implement one?
327. 🟡 What is the retry topic pattern (non-blocking retries)?
328. 🟡 What is blocking retry vs non-blocking retry? Effect on ordering?
329. 🟡 How do you add error context (exception, original topic, partition, offset) to DLT messages?
330. 🟡 How do you replay messages from a DLT?
331. 🟡 What happens if a consumer keeps failing on the same message forever (stuck partition)?
332. 🔴 How do you preserve ordering per key when one message for that key goes to a retry topic?
333. 🔴 How do you handle errors when producing (retriable vs non-retriable errors, `delivery.timeout.ms`)?

---

## 30. Kafka Connect & Change Data Capture

334. 🟡 What is Kafka Connect?
335. 🟡 What are source connectors and sink connectors?
336. 🟡 What are workers, connectors and tasks? Standalone vs distributed mode?
337. 🟡 What are Single Message Transforms (SMTs)?
338. 🟡 What are converters in Kafka Connect?
339. 🟡 How does Kafka Connect handle errors (`errors.tolerance`, DLQ)?
340. 🟡 What is Change Data Capture (CDC)?
341. 🟡 What is Debezium? How does it capture changes (transaction log / binlog / WAL)?
342. 🟡 How does Debezium help implement the Outbox pattern (Outbox Event Router SMT)?
343. 🟡 What is log-based CDC vs query-based CDC?
344. 🔴 How do you do CDC from SQL Server to Kafka?
345. 🔴 What are the risks of exposing raw database CDC events to other services?

---

## 31. Kafka Streams & ksqlDB / Stream Processing

346. 🟡 What is stream processing?
347. 🟡 What is Kafka Streams? Is it available for .NET? (Streamiz.Kafka.Net)
348. 🟡 What is a KStream vs a KTable vs a GlobalKTable?
349. 🟡 What are stateless vs stateful operations?
350. 🟡 What are state stores and changelog topics?
351. 🟡 What are windowing types (tumbling, hopping, sliding, session)?
352. 🟡 What are stream-stream joins vs stream-table joins?
353. 🟡 What is ksqlDB?
354. 🟡 What is Apache Flink and how does it compare with Kafka Streams?
355. 🔴 How do you compute a real-time running balance or aggregate per account? 💰
356. 🔴 How do you detect fraud patterns (e.g., 5 transactions in 1 minute) using stream processing? 💰
357. 🔴 How are late events handled in windowed aggregations (grace period)?

---

## 32. Kafka Security

358. 🟡 How do you secure a Kafka cluster?
359. 🟡 What is encryption in transit (TLS/SSL) in Kafka?
360. 🟡 What authentication mechanisms does Kafka support (SASL/PLAIN, SASL/SCRAM, SASL/GSSAPI-Kerberos, SASL/OAUTHBEARER, mTLS)?
361. 🟡 What are ACLs in Kafka? How do you restrict a service to specific topics and consumer groups?
362. 🟡 What is encryption at rest for Kafka data?
363. 🟡 How do you protect sensitive fields inside messages (field-level encryption, tokenisation)? 💰
364. 🟡 How do you manage Kafka credentials in .NET applications (Key Vault, managed identity with Event Hubs)?
365. 🔴 How do you audit who produced or consumed data from a topic? 💰
366. 🔴 How do you implement multi-tenancy in Kafka (topic prefixes, ACLs, quotas)?

---

## 33. Performance & Tuning

367. 🟡 How do you increase producer throughput (batching, `linger.ms`, compression, async sends)?
368. 🟡 How do you reduce producer latency?
369. 🟡 How do you increase consumer throughput (more partitions, more consumers, batch processing, fetch sizes)?
370. 🟡 What is the throughput vs latency trade-off in Kafka?
371. 🟡 How does compression affect CPU, network and disk?
372. 🟡 How do you handle consumer lag that keeps growing?
373. 🟡 What are quotas in Kafka?
374. 🟡 How do partition count and replication factor affect performance?
375. 🔴 What is zero-copy transfer?
376. 🔴 How does the OS page cache help Kafka?
377. 🔴 How do you size a Kafka cluster (throughput, retention, replication, partitions)?
378. 🔴 How do you benchmark Kafka (`kafka-producer-perf-test`, `kafka-consumer-perf-test`)?

---

## 34. Monitoring & Operations

379. 🟡 What key Kafka metrics should you monitor (under-replicated partitions, offline partitions, active controller count, request latency, consumer lag, disk usage, ISR shrink/expand)?
380. 🟡 What tools monitor Kafka (Burrow, Kafka UI, AKHQ, Conduktor, Confluent Control Center, Prometheus JMX exporter, Grafana)?
381. 🟡 What CLI tools do you use daily (`kafka-topics`, `kafka-console-producer`, `kafka-console-consumer`, `kafka-consumer-groups`, `kafka-configs`)?
382. 🟡 How do you create a topic with specific partitions, RF and configs?
383. 🟡 How do you check consumer group lag from the CLI?
384. 🟡 How do you reassign partitions or add a broker?
385. 🟡 How do you perform a rolling upgrade or restart of brokers without downtime?
386. 🔴 What happens when a broker disk fills up?
387. 🔴 How do you do disaster recovery for Kafka?
388. 🔴 What is a Kafka "under-replicated partition" alert and how do you respond?

---

## 35. Kafka in Docker, Kubernetes & Cloud

389. 🟡 How do you run Kafka locally with Docker Compose (KRaft mode)?
390. 🟡 Why can't clients connect to Kafka in Docker (`advertised.listeners` misconfiguration)?
391. 🟡 How do you run Kafka on Kubernetes (Strimzi, Confluent for Kubernetes)?
392. 🟡 What managed Kafka services exist (Confluent Cloud, Amazon MSK, Aiven, Azure Event Hubs Kafka endpoint)?
393. 🟡 What are the limitations of Azure Event Hubs' Kafka compatibility?
394. 🟡 What is Redpanda? How does it compare to Kafka?
395. 🔴 Self-managed Kafka vs managed Kafka — how do you decide?

---

## 36. Kafka vs RabbitMQ vs Azure Service Bus vs Others

396. 🟢 What is the difference between Kafka and RabbitMQ?
397. 🟡 When would you choose RabbitMQ over Kafka?
398. 🟡 When would you choose Kafka over RabbitMQ?
399. 🟡 Kafka vs Azure Service Bus?
400. 🟡 Kafka vs Azure Event Hubs?
401. 🟡 Kafka vs AWS SQS/SNS/Kinesis?
402. 🟡 Kafka vs Apache Pulsar?
403. 🟡 Kafka vs Redis Streams?
404. 🟡 Can Kafka replace a database? Can it replace a queue?
405. 🔴 Can you use Kafka and RabbitMQ together in one architecture? Give a design.

---

# Part C — Kafka with .NET

## 37. Confluent.Kafka Client in .NET

406. 🟢 Which library do you use to work with Kafka in .NET?
407. 🟢 What is `librdkafka` and how does `Confluent.Kafka` use it?
408. 🟡 What are `ProducerBuilder<TKey,TValue>` and `ConsumerBuilder<TKey,TValue>`?
409. 🟡 What is `ProducerConfig` / `ConsumerConfig`? Name important settings.
410. 🟡 What is the difference between `ProduceAsync` and `Produce` (with delivery handler)?
411. 🟡 What is `DeliveryResult` and what does `PersistenceStatus` tell you?
412. 🟡 What exceptions can `ProduceAsync` throw (`ProduceException`)?
413. 🟡 Is `IProducer` thread-safe? Should it be a singleton?
414. 🟡 Is `IConsumer` thread-safe? Can multiple threads call `Consume` on the same instance?
415. 🟡 What does `Consume(CancellationToken)` do? Is it blocking?
416. 🟡 What does `consumer.Close()` do and why must it be called on shutdown?
417. 🟡 What are `SetPartitionsAssignedHandler`, `SetPartitionsRevokedHandler`, `SetPartitionsLostHandler`?
418. 🟡 How do you use Avro/Protobuf/JSON serializers with Schema Registry in .NET (`Confluent.SchemaRegistry.Serdes`)?
419. 🟡 How do you create topics programmatically with `IAdminClient`?
420. 🟡 What is `SetErrorHandler`, `SetLogHandler` and `SetStatisticsHandler`?
421. 🔴 How do you implement transactions in .NET (`InitTransactions`, `BeginTransaction`, `SendOffsetsToTransaction`, `CommitTransaction`)?
422. 🔴 Why is `Consume()` a blocking call and how do you run it without starving the thread pool?

---

## 38. Building Producers in ASP.NET Core

423. 🟡 How do you register a Kafka producer in ASP.NET Core DI?
424. 🟡 Why should the producer be a singleton and not created per request?
425. 🟡 How do you publish an event from a Web API controller after saving to the database? What is the risk?
426. 🟡 How do you implement the Outbox pattern in ASP.NET Core with EF Core and a background publisher?
427. 🟡 How do you add correlation ID and trace context to Kafka message headers?
428. 🟡 How do you flush the producer on application shutdown?
429. 🔴 How do you handle `ProduceAsync` failures in an API request (return 500, retry, outbox)?
430. 🔴 How do you produce messages with a high throughput from an API without increasing request latency?

---

## 39. Building Consumers as BackgroundServices

431. 🟡 How do you build a Kafka consumer using `BackgroundService`?
432. 🟡 Why should you wrap the blocking consume loop in `Task.Run` or a dedicated thread (`LongRunning`)?
433. 🟡 How do you use scoped services (DbContext) inside a Kafka consumer?
434. 🟡 How do you commit offsets after successful processing?
435. 🟡 How do you handle exceptions inside the consume loop without killing the BackgroundService?
436. 🟡 How do you implement graceful shutdown for a consumer (cancellation token, `Close()`)?
437. 🟡 How do you scale consumers (multiple pods, multiple consumer instances per pod)?
438. 🟡 How do you implement an idempotent consumer with EF Core (processed messages table)?
439. 🟡 How do you implement retry and DLT in a .NET consumer?
440. 🟡 How do you expose consumer health checks (lag, last poll time)?
441. 🔴 How do you process messages in parallel while still preserving per-key ordering in .NET (`Channel<T>` per key/partition)?
442. 🔴 How do you batch-consume messages and commit offsets for the batch?
443. 🔴 What happens to in-flight messages when Kubernetes sends SIGTERM to a consumer pod?

---

## 40. MassTransit / Other Frameworks with Kafka

444. 🟡 How does MassTransit support Kafka (Riders)?
445. 🟡 What are the differences between using raw `Confluent.Kafka` and MassTransit?
446. 🟡 How do you use MassTransit's transactional outbox with Kafka?
447. 🟡 How do you implement a saga state machine with MassTransit and Kafka?
448. 🟡 What other .NET options exist (KafkaFlow, Silverback, Brighter, Dapr pub/sub, CAP, Wolverine)?
449. 🟡 What is KafkaFlow and what does it add (middlewares, typed handlers, worker distribution)?
450. 🔴 What is Dapr pub/sub with Kafka and when would you use it?

---

# Part D — Practice

## 41. Financial-Domain EDA & Kafka Questions 💰

451. 🟡💰 Why is Kafka widely used in banks, payments and trading platforms?
452. 🟡💰 How do you choose the partition key for transactions so that all events for an account are ordered?
453. 🔴💰 How do you guarantee a payment event is never lost?
454. 🔴💰 How do you guarantee a payment is never processed twice?
455. 🔴💰 How do you design a real-time transaction notification system (SMS/push) using Kafka?
456. 🔴💰 How do you design a real-time fraud detection pipeline using Kafka and stream processing?
457. 🔴💰 How do you build a ledger service fed by Kafka events with correct balances?
458. 🔴💰 How do you handle reconciliation between Kafka events and the core banking database?
459. 🔴💰 How do you design an audit trail using Kafka (immutable, retention, compaction)?
460. 🔴💰 How do you handle regulatory data retention (e.g., keep transactions for 7–10 years) when Kafka retention is limited?
461. 🔴💰 How do you handle PII and card data in Kafka messages (PCI-DSS, tokenisation, encryption)?
462. 🔴💰 How do you process market data feeds with low latency using Kafka?
463. 🔴💰 How do you design end-of-day settlement using events?
464. 🔴💰 What Kafka configuration would you use for a payments topic (RF, min ISR, acks, idempotence, retention)?
465. 🔴💰 How do you handle an event that says "payment successful" from a provider but your system timed out earlier?

---

## 42. Tricky Questions

466. 🟡 Does Kafka guarantee message ordering?
467. 🟡 Does Kafka delete messages after they are consumed?
468. 🟡 Can two consumers in the same group read the same partition at the same time?
469. 🟡 Can one consumer read from multiple partitions?
470. 🟡 If you have 10 partitions and 15 consumers in a group, what do 5 consumers do?
471. 🟡 If you add partitions to a topic, will existing keys still go to the same partition?
472. 🟡 Is `acks=all` enough to guarantee no data loss?
473. 🟡 Does `enable.idempotence=true` give exactly-once processing end to end?
474. 🟡 Does auto-commit guarantee at-least-once delivery?
475. 🟡 Can a message be lost with `acks=1`? How?
476. 🟡 Can a consumer receive a message that is later "lost" due to leader failure?
477. 🟡 Why does a new consumer group with `auto.offset.reset=latest` see no old messages?
478. 🟡 Why does a consumer re-read old messages after a restart?
479. 🟡 Why does a consumer skip messages after a restart?
480. 🟡 Why does consumer lag keep increasing even though consumers are running?
481. 🟡 Why do consumers rebalance constantly?
482. 🟡 Why does one partition have much more data than others?
483. 🟡 Why do messages with the same key appear out of order?
484. 🟡 Why is a compacted topic still showing multiple values for the same key?
485. 🟡 Why can't my .NET app connect to Kafka in Docker even though the port is open?
486. 🟡 Why does `ProduceAsync` take a long time for each message in a loop?
487. 🟡 Why does my BackgroundService consumer block application startup?
488. 🟡 Why does my consumer stop consuming after an unhandled exception?
489. 🟡 Is Kafka a database?
490. 🟡 Is Kafka a good fit for request/response communication?
491. 🔴 Why can increasing `max.in.flight.requests.per.connection` break ordering without idempotence?
492. 🔴 Why can unclean leader election cause data loss?
493. 🔴 Why can a long-running message handler cause duplicates (poll interval exceeded → rebalance)?
494. 🔴 Why do Kafka transactions not make your database write atomic with the produce?
495. 🔴 Why can a `read_committed` consumer appear stuck?
496. 🔴 Why does deleting a topic not immediately free disk space?
497. 🔴 Why does a retry topic break per-key ordering?
498. 🔴 Why can events be reordered when the outbox publisher runs on multiple instances?
499. 🔴 Why is "exactly-once delivery" a misleading term?
500. 🔴 What happens if two producers use the same `transactional.id`?
501. 🔴 If an event is published but the consumer's database is down for a day, what happens?
502. 🔴 If retention is 7 days and a consumer is down for 10 days, what happens?
503. 🔴 Can you change the partition key of an existing topic without breaking ordering?
504. 🔴 Why can using `DateTime.Now` as an event timestamp cause problems across services?

---

## 43. Predict the Behavior (Config & Code Snippets)

> What happens with each configuration or code snippet? If it's wrong, explain why and how to fix it.

**505. 🟡 Durability config**
```properties
replication.factor=3
min.insync.replicas=2
acks=1
```
Two brokers go down. Can the producer still write? Can data be lost? What if `acks=all`?

**506. 🟡 min.insync.replicas**
```properties
replication.factor=3
min.insync.replicas=3
acks=all
```
One broker goes down for maintenance. What happens to producers?

**507. 🟡 Consumers vs partitions**
```text
Topic "payments": 6 partitions
Consumer group "ledger": 8 consumer instances
```
How are partitions distributed? What do the extra consumers do?

**508. 🟡 No key**
```csharp
await producer.ProduceAsync("account-events", new Message<Null, string> { Value = json });
```
Two events for the same account (`Debited`, then `Credited`) are produced. Is their order guaranteed for consumers? 💰

**509. 🟡 Keyed messages**
```csharp
await producer.ProduceAsync("account-events", new Message<string, string> { Key = accountId, Value = json });
```
What ordering guarantee do you get now? What if partitions are increased from 6 to 12 later?

**510. 🟡 Auto commit**
```csharp
var config = new ConsumerConfig { GroupId = "ledger", EnableAutoCommit = true, AutoCommitIntervalMs = 5000 };
while (true)
{
    var cr = consumer.Consume(ct);
    await ProcessAsync(cr.Message);   // crashes after 3 seconds on some message
}
```
After a restart, which messages are reprocessed or lost?

**511. 🟡 Commit before processing**
```csharp
var cr = consumer.Consume(ct);
consumer.Commit(cr);
await ProcessAsync(cr.Message);   // throws
```
Which delivery semantic is this? What happens to the message?

**512. 🟡 Commit after processing**
```csharp
var cr = consumer.Consume(ct);
await ProcessAsync(cr.Message);
consumer.Commit(cr);              // process crashes right before this line
```
What happens after a restart? What must `ProcessAsync` be?

**513. 🟡 auto.offset.reset**
```csharp
var config = new ConsumerConfig { GroupId = "new-report-service", AutoOffsetReset = AutoOffsetReset.Latest };
```
The topic already has 1 million messages. What does the new consumer group read? What changes with `Earliest`?

**514. 🔴 Long processing**
```csharp
var config = new ConsumerConfig { GroupId = "exports", MaxPollIntervalMs = 300000 };
var cr = consumer.Consume(ct);
await GenerateLargeReportAsync(cr.Message);   // takes 8 minutes
consumer.Commit(cr);
```
What happens?

**515. 🔴 Producer created per request**
```csharp
[HttpPost]
public async Task<IActionResult> Publish(OrderDto dto)
{
    using var producer = new ProducerBuilder<string, string>(_config).Build();
    await producer.ProduceAsync("orders", new Message<string, string> { Key = dto.Id, Value = JsonSerializer.Serialize(dto) });
    return Accepted();
}
```
What are the problems under load?

**516. 🔴 ProduceAsync in a loop**
```csharp
foreach (var e in events)          // 100,000 events
    await producer.ProduceAsync("events", new Message<string, string> { Key = e.Id, Value = e.Json });
```
Why is this slow? How do you make it faster?

**517. 🔴 No flush on shutdown**
```csharp
foreach (var e in events)
    producer.Produce("events", new Message<string, string> { Key = e.Id, Value = e.Json });
// application exits immediately
```
What happens to the messages?

**518. 🔴 Dual write**
```csharp
await _db.Payments.AddAsync(payment);
await _db.SaveChangesAsync();
await _producer.ProduceAsync("payments", new Message<string, string> { Key = payment.AccountId, Value = Serialize(payment) });
```
What happens if Kafka is unavailable after `SaveChangesAsync`? What if the app crashes between the two lines? 💰

**519. 🔴 Non-idempotent consumer**
```csharp
var cr = consumer.Consume(ct);
var evt = Deserialize<MoneyDeposited>(cr.Message.Value);
var acc = await db.Accounts.FindAsync(evt.AccountId);
acc.Balance += evt.Amount;
await db.SaveChangesAsync();
consumer.Commit(cr);
```
A rebalance happens after `SaveChangesAsync` but before `Commit`. What happens? How do you fix it? 💰

**520. 🔴 Exception kills the loop**
```csharp
protected override async Task ExecuteAsync(CancellationToken ct)
{
    while (!ct.IsCancellationRequested)
    {
        var cr = _consumer.Consume(ct);
        var order = JsonSerializer.Deserialize<Order>(cr.Message.Value)!;   // one message has invalid JSON
        await HandleAsync(order);
        _consumer.Commit(cr);
    }
}
```
What happens when the invalid message arrives? What happens after the service restarts?

**521. 🔴 Blocking startup**
```csharp
protected override async Task ExecuteAsync(CancellationToken ct)
{
    while (!ct.IsCancellationRequested)
    {
        var cr = _consumer.Consume(ct);   // synchronous blocking call, no await before it
        await HandleAsync(cr);
    }
}
```
What happens to application startup? How do you fix it?

**522. 🔴 Compaction and tombstones**
```text
Compacted topic "customer-profile", key = customerId
Messages: (C1, v1), (C2, v1), (C1, v2), (C1, null), (C2, v2)
```
After compaction and `delete.retention.ms` passes, what remains?

**523. 🔴 Transactions and read_committed**
```text
Producer: BeginTransaction → produce 3 messages → (crashes before Commit)
Consumer A: isolation.level=read_uncommitted
Consumer B: isolation.level=read_committed
```
What does each consumer see?

**524. 🔴 Retry topic ordering**
```text
Key "ACC-1": Event1 (fails → sent to retry topic), Event2 (succeeds immediately)
```
In which order are Event1 and Event2 applied? Why is this a problem for balances? 💰

**525. 🟡 Retention**
```properties
retention.ms=604800000   # 7 days
```
A consumer group was offline for 10 days. What happens when it comes back with `auto.offset.reset=earliest`? With `none`?

**526. 🟡 Advertised listeners**
```yaml
KAFKA_ADVERTISED_LISTENERS: PLAINTEXT://localhost:9092
# .NET service runs in another container and uses bootstrap server kafka:9092
```
What happens when the .NET service connects?

---

## 44. Scenario-Based Questions — Event-Driven Design

527. 🟡 You need to notify Inventory, Shipping, Email and Analytics services when an order is placed. Design it with events.
528. 🟡 The Order service needs customer details without calling the Customer service. How do you design it with events?
529. 🟡 A consumer receives duplicate `PaymentCompleted` events and sends two emails. How do you fix it?
530. 🟡 Product prices change frequently and 5 services need the latest price. Fat events or thin events? Compacted topic?
531. 🟡 Your team wants to rename a field in a widely used event. How do you roll it out?
532. 🟡 A new service needs all historical orders from the last 2 years. How do you backfill it?
533. 🟡 A consumer is down for 3 hours. What happens and how does it catch up?
534. 🟡 A business user asks "why wasn't the customer notified?" How do you trace the event flow?
535. 🟡 How do you migrate from synchronous REST calls between services to events gradually?
536. 🟡 Two services publish events that are needed together to build one report. How do you join them?
537. 🔴 Design an event-driven order fulfillment saga with compensations and timeouts.
538. 🔴 You need strong consistency for one step (e.g., reserving the last seat/ticket) in an otherwise event-driven flow. How do you design it?
539. 🔴 A consumer must call a slow external API for each event. How do you avoid lag and keep ordering per key?
540. 🔴 Events must be processed in order per customer but you need high parallelism. How do you design partitions and consumers?
541. 🔴 The outbox table grows to 50 million rows and publishing lags. How do you fix it?
542. 🔴 You must delete a customer's personal data from all services and Kafka topics (GDPR). How do you design it?
543. 🔴 Multiple teams publish to shared topics with inconsistent schemas. How do you introduce governance?
544. 🔴 An upstream service published 100,000 wrong events due to a bug. How do you correct downstream data?
545. 🔴 How do you design a "replay from the beginning" capability for rebuilding a read model without affecting live consumers?
546. 🔴 How do you implement a scheduled/delayed event (e.g., "send reminder in 24 hours") with Kafka?

---

## 45. Scenario-Based Questions — Kafka Production Issues

547. 🟡 Consumer lag for one consumer group keeps increasing during peak hours. How do you investigate and fix it?
548. 🟡 Consumers keep rebalancing every few minutes. What could be causing it?
549. 🟡 One partition has 10x more lag than others. Why, and how do you fix it?
550. 🟡 After a deployment, a consumer group starts reprocessing messages from 3 days ago. What happened?
551. 🟡 After a deployment, consumers skipped a large number of messages. What happened?
552. 🟡 A poison message is blocking a partition and the consumer keeps crashing. What do you do immediately and long term?
553. 🟡 Producers get `NotEnoughReplicas` errors. What does it mean and how do you respond?
554. 🟡 Producers get `MessageSizeTooLarge` errors. What do you check?
555. 🟡 Producers time out with `Local: Message timed out`. What could be wrong?
556. 🟡 .NET consumers can't connect to the cluster after moving to Kubernetes. What do you check?
557. 🟡 Broker disk usage is at 90%. What actions do you take?
558. 🔴 A broker failed and some partitions are offline. What happened and how do you recover?
559. 🔴 You see under-replicated partitions after a network issue. What is the impact and fix?
560. 🔴 Duplicate payments were created after a consumer rebalance. How do you find root cause and prevent recurrence? 💰
561. 🔴 Events for the same account were processed out of order, causing a wrong balance. How do you investigate? 💰
562. 🔴 The DLT for payments has 5,000 messages after a downstream outage. How do you safely reprocess them? 💰
563. 🔴 You need to move a consumer group to start from a specific timestamp after a bug fix. How do you do it?
564. 🔴 You need to migrate from a self-hosted Kafka cluster to Confluent Cloud / MSK with zero data loss. How do you plan it?
565. 🔴 You need to increase partitions of a keyed topic that requires strict per-key ordering. How do you do it safely?
566. 🔴 Your Kafka cluster still runs ZooKeeper and must move to Kafka 4.0. What is the migration path?

---

## 46. System Design Scenarios

567. 🔴 Design an event-driven e-commerce platform (orders, inventory, payments, shipping, notifications) using Kafka.
568. 🔴 Design a real-time payment processing platform (UPI-like) with Kafka, exactly-once processing and reconciliation. 💰
569. 🔴 Design a real-time fraud detection system on card transactions. 💰
570. 🔴 Design a transaction alert / notification system for millions of bank customers. 💰
571. 🔴 Design a stock market data pipeline that ingests and distributes price ticks. 💰
572. 🔴 Design an audit logging platform for 100 microservices using Kafka.
573. 🔴 Design a CDC pipeline from a legacy SQL Server core banking database to new microservices. 💰
574. 🔴 Design a ride-hailing location tracking system using Kafka.
575. 🔴 Design a real-time analytics dashboard (orders per minute, revenue) using Kafka and stream processing.
576. 🔴 Design a multi-region Kafka deployment with disaster recovery.
577. 🔴 Design a loan application workflow using events, sagas and human approvals. 💰
578. 🔴 Design an event-sourced account ledger with snapshots and projections. 💰

---

## 47. Hands-On Tasks

579. 🟢 Run Kafka in KRaft mode with Docker Compose along with Kafka UI.
580. 🟢 Create a topic with 6 partitions and RF 3 using the CLI.
581. 🟢 Produce and consume messages with `kafka-console-producer` and `kafka-console-consumer`.
582. 🟡 Write a .NET producer using `Confluent.Kafka` with keys, headers and idempotence enabled.
583. 🟡 Write a .NET consumer as a `BackgroundService` with manual commits and graceful shutdown.
584. 🟡 Add correlation ID and W3C trace context to message headers and log them in the consumer.
585. 🟡 Implement an idempotent consumer using an EF Core "ProcessedMessages" table.
586. 🟡 Implement retry topics (retry-1, retry-2) and a dead letter topic in .NET.
587. 🟡 Use Avro or Protobuf with Schema Registry in a .NET producer and consumer.
588. 🟡 Check consumer group lag and reset offsets to a timestamp using the CLI.
589. 🟡 Write integration tests for a producer and consumer using Testcontainers for Kafka.
590. 🔴 Implement the Transactional Outbox pattern with EF Core and a background publisher to Kafka.
591. 🔴 Implement the Outbox pattern using Debezium and the Outbox Event Router.
592. 🔴 Implement a consume-transform-produce flow with Kafka transactions in .NET.
593. 🔴 Implement a choreography saga for order → payment → inventory with compensation events.
594. 🔴 Implement an orchestration saga using MassTransit state machine with Kafka riders.
595. 🔴 Implement parallel processing within a consumer while preserving per-key ordering.
596. 🔴 Implement a real-time per-account running balance projection from transaction events. 💰
597. 🔴 Implement a fraud rule ("more than 5 transactions in 60 seconds per card") using a windowed stream processor. 💰
598. 🔴 Implement OpenTelemetry tracing across an ASP.NET Core API → Kafka → consumer service.

---

## 48. Rapid-Fire Round

599. 🟢 What is the unit of parallelism in Kafka?
600. 🟢 What is the unit of ordering in Kafka?
601. 🟢 Where are consumer offsets stored?
602. 🟢 What replaced ZooKeeper in Kafka?
603. 🟢 In which Kafka version was ZooKeeper removed?
604. 🟢 What determines the partition of a keyed message?
605. 🟢 What is the default `auto.offset.reset`?
606. 🟢 What does RF stand for?
607. 🟢 What does ISR stand for?
608. 🟢 What is a tombstone?
609. 🟡 Which producer setting waits for all in-sync replicas?
610. 🟡 Which setting prevents duplicate writes from producer retries?
611. 🟡 Which consumer setting makes consumers skip aborted transactional messages?
612. 🟡 Which setting controls how long a consumer can go between polls?
613. 🟡 Which cleanup policy keeps the latest value per key?
614. 🟡 What is the default retention period in Kafka?
615. 🟡 What is the default maximum message size (approximately)?
616. 🟡 Which assignment strategy enables incremental cooperative rebalancing?
617. 🟡 What tool replicates data between Kafka clusters?
618. 🟡 What is the most popular CDC tool for Kafka?
619. 🟡 Which .NET library wraps `librdkafka`?
620. 🟡 Which pattern solves the dual-write problem?
621. 🟡 Which pattern makes consumers safe against duplicates?
622. 🟡 Which pattern manages distributed transactions with compensation?
623. 🔴 What is the difference between the high watermark and the log end offset in one line?
624. 🔴 What is producer fencing in one line?
625. 🔴 What is KIP-848 in one line?
626. 🔴 What is KIP-932 (share groups) in one line?
627. 🔴 What is the difference between Event Sourcing and event-driven architecture in one line?
628. 🔴 What is the difference between choreography and orchestration in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture.
