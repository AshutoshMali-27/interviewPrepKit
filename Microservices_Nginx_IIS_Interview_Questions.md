# 🎯 Microservices, Nginx & IIS Interview Questions — Part 6 (Questions Only)

> **Scope:** Microservices concepts and all major patterns (decomposition, communication, data management, transactions, resiliency, observability, deployment, security), .NET microservices, messaging, containers & orchestration — plus **Nginx in depth as API Gateway, Load Balancer and Reverse Proxy** (our hosting setup), and **IIS basics** in short.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Context:** ASP.NET Core services running on Kestrel behind Nginx (Linux/containers). IIS covered at a basic level.

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Microservices**
1. Microservices Fundamentals
2. Monolith vs Microservices vs Modular Monolith vs SOA
3. Domain-Driven Design & Service Decomposition
4. Decomposition & Migration Patterns
5. Communication — Synchronous (REST, gRPC)
6. Communication — Asynchronous (Messaging & Events)
7. Message Brokers (RabbitMQ, Kafka, Azure Service Bus)
8. Messaging Patterns & Reliability
9. API Gateway & Backend-for-Frontend Patterns
10. Service Discovery & Load Balancing (Concepts)
11. Data Management Patterns
12. Distributed Transactions — Saga, 2PC, Outbox, Inbox
13. CQRS & Event Sourcing
14. Resiliency & Fault-Tolerance Patterns
15. Caching in Microservices
16. Observability — Logging, Metrics, Tracing, Health Checks
17. Configuration & Secrets Management
18. Security in Microservices
19. Containers & Docker
20. Kubernetes & Orchestration
21. Service Mesh & Sidecar Patterns
22. Deployment Patterns & CI/CD
23. Testing Microservices
24. API Versioning & Contracts Between Services
25. .NET Microservices Ecosystem (MassTransit, YARP, Dapr, .NET Aspire, Ocelot)
26. Microservices Anti-Patterns

**Part B — Nginx (Reverse Proxy, Load Balancer, API Gateway)**
27. Nginx Fundamentals & Architecture
28. Nginx Configuration Structure
29. Nginx as a Reverse Proxy
30. Hosting ASP.NET Core Behind Nginx
31. Nginx as a Load Balancer
32. Nginx as an API Gateway
33. SSL/TLS Termination & HTTPS in Nginx
34. Nginx Caching, Compression & Performance
35. Nginx Security
36. Nginx with WebSockets, SignalR, gRPC & Streaming
37. Nginx Logging, Monitoring & Troubleshooting
38. Nginx in Docker & Kubernetes (Ingress)
39. Nginx Alternatives & Comparisons

**Part C — IIS Basics**
40. IIS Fundamentals
41. Hosting ASP.NET Core on IIS

**Part D — Practice**
42. Financial-Domain Microservices Questions 💰
43. Tricky Questions
44. Predict the Behavior (Nginx Config & Code Snippets)
45. Scenario-Based Questions — Microservices Design
46. Scenario-Based Questions — Nginx & Production Issues
47. System Design Scenarios
48. Hands-On Tasks
49. Rapid-Fire Round

---

# Part A — Microservices

## 1. Microservices Fundamentals

1. 🟢 What are microservices?
2. 🟢 What are the key characteristics of a microservice?
3. 🟢 What are the advantages of microservices architecture?
4. 🟢 What are the disadvantages and challenges of microservices?
5. 🟢 When should you NOT use microservices?
6. 🟢 What does "independently deployable" mean?
7. 🟢 What is "loose coupling and high cohesion" in microservices?
8. 🟡 What is the "single responsibility" principle at the service level?
9. 🟡 How small should a microservice be? Is "micro" about lines of code?
10. 🟡 What is Conway's Law and how does it affect microservices?
11. 🟡 What is the "two-pizza team" rule? What is team ownership ("you build it, you run it")?
12. 🟡 What are the 12-Factor App principles? Explain each briefly.
13. 🟡 What does "smart endpoints and dumb pipes" mean?
14. 🟡 What is decentralized governance and decentralized data management?
15. 🟡 What are the fallacies of distributed computing?
16. 🟡 What is the CAP theorem? How does it apply to microservices?
17. 🟡 What is the PACELC theorem?
18. 🟡 What is eventual consistency? Give an example.
19. 🟡 What is BASE vs ACID?
20. 🔴 What is the cost of a network call compared to an in-process call? Why does it matter?
21. 🔴 What organizational maturity is required before adopting microservices?

---

## 2. Monolith vs Microservices vs Modular Monolith vs SOA

22. 🟢 What is a monolithic application?
23. 🟢 What are the differences between monolith and microservices?
24. 🟡 What is a modular monolith? Why is it often recommended as a starting point?
25. 🟡 What is SOA (Service-Oriented Architecture)? How is it different from microservices?
26. 🟡 What is an ESB (Enterprise Service Bus)? Why do microservices avoid it?
27. 🟡 What is a distributed monolith? How do you recognise one?
28. 🟡 What is serverless? How does it compare to microservices?
29. 🔴 How would you decide between a modular monolith and microservices for a new product?
30. 🔴 Some companies moved back from microservices to monoliths. Why?

---

## 3. Domain-Driven Design & Service Decomposition

31. 🟢 What is Domain-Driven Design (DDD)?
32. 🟡 What is a bounded context?
33. 🟡 What is ubiquitous language?
34. 🟡 What is a context map? What are relationships like Shared Kernel, Customer-Supplier, Conformist, Anti-Corruption Layer, Open Host Service, Published Language?
35. 🟡 What is an aggregate? What is an aggregate root?
36. 🟡 What are entities and value objects?
37. 🟡 What are domain events vs integration events?
38. 🟡 What are subdomains: core, supporting and generic?
39. 🟡 How do you identify service boundaries?
40. 🟡 What is decomposition by business capability?
41. 🟡 What is decomposition by subdomain?
42. 🟡 What is Event Storming?
43. 🟡 What happens if service boundaries are drawn wrong? How do you detect it (chatty services, shared changes)?
44. 🔴 How do you split a shared "Customer" entity used by many services?
45. 🔴 How do you decompose a banking system into services (Accounts, Payments, Customers, Ledger, Notifications, KYC)? 💰

---

## 4. Decomposition & Migration Patterns

46. 🟡 What is the Strangler Fig pattern? How do you implement it?
47. 🟡 What is the Anti-Corruption Layer pattern?
48. 🟡 What is Branch by Abstraction?
49. 🟡 What is the Parallel Run pattern? 💰
50. 🟡 What is the Decorating Collaborator pattern?
51. 🟡 What is Change Data Capture (CDC) and how does it help migration?
52. 🔴 How do you migrate a monolith to microservices step by step?
53. 🔴 How do you split a shared database during migration?
54. 🔴 Which service would you extract first from a monolith and why?
55. 🔴 How does Nginx help with the Strangler Fig pattern (route some paths to new services, rest to monolith)?

---

## 5. Communication — Synchronous (REST, gRPC)

56. 🟢 What are the communication styles between microservices?
57. 🟢 What is synchronous communication? Give examples.
58. 🟡 What are the pros and cons of REST for inter-service communication?
59. 🟡 What is gRPC? Why is it popular for internal service-to-service communication?
60. 🟡 What are Protocol Buffers? How do you manage `.proto` contract versions?
61. 🟡 REST vs gRPC vs GraphQL for microservices — when to use which?
62. 🟡 What is temporal coupling? How does synchronous communication create it?
63. 🟡 What is a chain of synchronous calls? Why is it dangerous (latency, availability multiplication)?
64. 🟡 If each of 5 services in a chain has 99.9% availability, what is the overall availability?
65. 🟡 What is request/response vs request/async response?
66. 🟡 How do you call another service from ASP.NET Core (`IHttpClientFactory`, typed clients, Refit, gRPC client factory)?
67. 🟡 How do you set timeouts for inter-service calls? What is timeout budgeting / deadline propagation?
68. 🔴 What is the N+1 problem across services? How do you avoid it (batch APIs, data replication)?
69. 🔴 When is it acceptable for services to call each other synchronously?

---

## 6. Communication — Asynchronous (Messaging & Events)

70. 🟢 What is asynchronous communication?
71. 🟢 What are the benefits of asynchronous messaging?
72. 🟢 What is a message broker?
73. 🟢 What is the difference between a message, a command and an event?
74. 🟡 What is point-to-point (queue) vs publish-subscribe (topic)?
75. 🟡 What is event-driven architecture?
76. 🟡 What is event notification vs event-carried state transfer?
77. 🟡 What is choreography vs orchestration?
78. 🟡 What are fat events vs thin events?
79. 🟡 What is a message envelope? What metadata should every message carry (MessageId, CorrelationId, CausationId, Timestamp, Type, Version)?
80. 🟡 How do you version events and messages without breaking consumers?
81. 🟡 What is a schema registry?
82. 🔴 What are the downsides of event-driven architecture (debugging, eventual consistency, ordering)?
83. 🔴 How do you handle a consumer that is down for hours?
84. 🔴 What is back-pressure in messaging systems?

---

## 7. Message Brokers (RabbitMQ, Kafka, Azure Service Bus)

85. 🟢 What is RabbitMQ?
86. 🟡 What are exchanges, queues, bindings and routing keys in RabbitMQ?
87. 🟡 What are exchange types: direct, fanout, topic, headers?
88. 🟡 What are acknowledgements (ack, nack, reject) in RabbitMQ?
89. 🟡 What is prefetch count / QoS?
90. 🟡 What are durable queues, persistent messages and quorum queues?
91. 🟢 What is Apache Kafka?
92. 🟡 What are topics, partitions, offsets, brokers, producers and consumer groups in Kafka?
93. 🟡 How does Kafka guarantee ordering? Is ordering global or per partition?
94. 🟡 How do you choose a partition key?
95. 🟡 What is consumer lag?
96. 🟡 What is log compaction and retention in Kafka?
97. 🟡 What are Kafka delivery semantics and idempotent producers? What is "exactly-once" in Kafka?
98. 🟡 What happens during a consumer group rebalance?
99. 🟡 RabbitMQ vs Kafka — what are the differences and when do you choose each?
100. 🟡 What is Azure Service Bus? Queues vs topics vs subscriptions? Sessions?
101. 🟡 What are AWS SQS/SNS and Google Pub/Sub at a high level?
102. 🟡 What is Redis Streams / Redis Pub/Sub? When is Redis Pub/Sub not enough?
103. 🔴 How do you scale consumers in RabbitMQ vs Kafka?
104. 🔴 How do you replay events in Kafka?

---

## 8. Messaging Patterns & Reliability

105. 🟢 What are delivery guarantees: at-most-once, at-least-once, exactly-once?
106. 🟡 Why is "exactly-once delivery" practically impossible? What is "effectively-once processing"?
107. 🟡 What is an idempotent consumer? How do you implement one?
108. 🟡 What is message deduplication?
109. 🟡 What is a dead-letter queue (DLQ)? When do messages go there?
110. 🟡 What is a poison message? How do you handle it?
111. 🟡 What is retry with delay / delayed redelivery?
112. 🟡 What is the competing consumers pattern?
113. 🟡 How do you guarantee message ordering when you have multiple consumers?
114. 🟡 What is the Request-Reply pattern over messaging?
115. 🟡 What is the Claim Check pattern (large payloads)?
116. 🟡 What is the Message Router / Content-Based Router pattern?
117. 🟡 What is the Aggregator and Splitter pattern?
118. 🟡 What is the Scatter-Gather pattern?
119. 🟡 What is the Priority Queue pattern?
120. 🟡 What is the Queue-Based Load Leveling pattern?
121. 🔴 What is the dual-write problem? Why can't you save to DB and publish to the broker reliably without a pattern?
122. 🔴 How do you handle out-of-order events?
123. 🔴 How do you reprocess messages from a DLQ safely?

---

## 9. API Gateway & Backend-for-Frontend Patterns

124. 🟢 What is an API Gateway?
125. 🟢 Why do we need an API Gateway in microservices?
126. 🟢 What responsibilities can an API Gateway have (routing, authentication, rate limiting, SSL termination, caching, aggregation, transformation, logging)?
127. 🟡 What is the Gateway Routing pattern?
128. 🟡 What is the Gateway Aggregation pattern?
129. 🟡 What is the Gateway Offloading pattern?
130. 🟡 What is the Backend-for-Frontend (BFF) pattern? When would you have separate gateways for web and mobile?
131. 🟡 What are the drawbacks of an API Gateway (single point of failure, bottleneck, coupling)?
132. 🟡 How do you make an API Gateway highly available?
133. 🟡 What logic should NOT be placed in an API Gateway?
134. 🟡 What is the difference between an API Gateway, a reverse proxy and a load balancer?
135. 🟡 What is the difference between an API Gateway and a service mesh?
136. 🟡 What are popular API Gateways (Nginx, Kong, YARP, Ocelot, Azure API Management, AWS API Gateway, Envoy, Traefik)?
137. 🟡 Should authentication be done at the gateway, in each service, or both?
138. 🔴 What is north-south vs east-west traffic?

---

## 10. Service Discovery & Load Balancing (Concepts)

139. 🟢 What is service discovery? Why is it needed?
140. 🟡 What is client-side discovery vs server-side discovery?
141. 🟡 What is a service registry (Consul, Eureka, etcd)?
142. 🟡 What is self-registration vs third-party registration?
143. 🟡 How does Kubernetes do service discovery (DNS, Services)?
144. 🟢 What is load balancing?
145. 🟡 What is client-side load balancing vs server-side load balancing?
146. 🟡 What is Layer 4 vs Layer 7 load balancing?
147. 🟡 What are load balancing algorithms (round robin, weighted, least connections, IP hash, random, least response time)?
148. 🟡 What are sticky sessions? Why should stateless services avoid them?
149. 🟡 What are active vs passive health checks for load balancing?
150. 🔴 What is DNS-based load balancing and what are its limitations (TTL caching)?

---

## 11. Data Management Patterns

151. 🟢 What is the Database-per-Service pattern? Why is it recommended?
152. 🟢 What is the Shared Database anti-pattern? Why is it problematic?
153. 🟡 What are the options for database per service (private tables, schema per service, database per service)?
154. 🟡 What is polyglot persistence?
155. 🟡 How do you query data that spans multiple services?
156. 🟡 What is the API Composition pattern?
157. 🟡 What is data replication via events (local read models / materialized views)?
158. 🟡 What is the Materialized View pattern?
159. 🟡 How do you maintain referential integrity across services?
160. 🟡 How do you handle reporting and analytics across microservices (data lake, CDC, ETL)?
161. 🟡 What is the Shared Kernel vs data duplication trade-off?
162. 🔴 How do you handle joins across services efficiently?
163. 🔴 How do you deal with data ownership when two services need to write the same data?
164. 🔴 What is the Database Wrapping Service pattern?
165. 🔴 How do you handle GDPR / data deletion requests across many services?

---

## 12. Distributed Transactions — Saga, 2PC, Outbox, Inbox

166. 🟢 What is a distributed transaction?
167. 🟡 What is Two-Phase Commit (2PC)? Why is it avoided in microservices?
168. 🟡 What is the Saga pattern?
169. 🟡 What is a choreography-based saga? Give an example.
170. 🟡 What is an orchestration-based saga? Give an example.
171. 🟡 Choreography vs orchestration sagas — pros and cons?
172. 🟡 What are compensating transactions? Give an example.
173. 🟡 What are pivot transactions and retriable transactions in a saga?
174. 🟡 What are saga isolation anomalies (lost updates, dirty reads)? What countermeasures exist (semantic lock, commutative updates, pessimistic view, reread value)?
175. 🟡 What is the Transactional Outbox pattern? How does it solve dual writes?
176. 🟡 How is the outbox published — polling publisher vs transaction log tailing (Debezium)?
177. 🟡 What is the Inbox pattern (idempotent receiver)?
178. 🔴 What happens if a compensating transaction fails?
179. 🔴 How do you implement a saga state machine in .NET (MassTransit, NServiceBus, Durable Functions, Temporal)?
180. 🔴 What is the TCC (Try-Confirm-Cancel) pattern?
181. 🔴💰 Design a saga for an order: reserve stock → charge payment → create shipment, with compensations.
182. 🔴💰 Design a saga for an inter-bank fund transfer.

---

## 13. CQRS & Event Sourcing

183. 🟢 What is CQRS?
184. 🟡 What are the benefits and drawbacks of CQRS?
185. 🟡 Does CQRS require separate databases?
186. 🟡 How do you keep the read model in sync with the write model?
187. 🟡 What is MediatR and how is it used for CQRS in .NET? (Note its licensing change.)
188. 🟢 What is Event Sourcing?
189. 🟡 What is an event store? Give examples (EventStoreDB, Marten).
190. 🟡 What are snapshots in Event Sourcing?
191. 🟡 What are projections?
192. 🟡 How do you handle event schema changes in Event Sourcing (upcasting)?
193. 🟡 What are the benefits of Event Sourcing for auditability? 💰
194. 🔴 When should you NOT use Event Sourcing?
195. 🔴 How do you rebuild a read model from events?
196. 🔴 How do you handle "delete" in an event-sourced system?
197. 🔴💰 Why is Event Sourcing a natural fit for ledgers and account balances?

---

## 14. Resiliency & Fault-Tolerance Patterns

198. 🟢 What is resiliency in microservices?
199. 🟢 What is the Retry pattern? What are its risks?
200. 🟡 What are exponential backoff and jitter? Why add jitter?
201. 🟡 What is a retry storm? How do you prevent it?
202. 🟡 What is the Circuit Breaker pattern? Explain the states (closed, open, half-open).
203. 🟡 What is the Timeout pattern? Why must every remote call have a timeout?
204. 🟡 What is the Bulkhead pattern?
205. 🟡 What is the Fallback pattern? Give examples.
206. 🟡 What is graceful degradation?
207. 🟡 What is rate limiting vs throttling vs load shedding?
208. 🟡 What is the Hedging pattern?
209. 🟡 What is a cascading failure? How do you prevent it?
210. 🟡 How do you implement resiliency in .NET (Polly v8, `Microsoft.Extensions.Http.Resilience`, `AddStandardResilienceHandler`)?
211. 🟡 Which errors should be retried and which should not?
212. 🔴 Why is retrying non-idempotent operations dangerous? 💰
213. 🔴 Where should retries happen — client, gateway, service mesh? What happens if all layers retry?
214. 🔴 What is chaos engineering? What tools exist (Chaos Monkey, Polly Chaos strategies, Azure Chaos Studio)?
215. 🔴 What are SLI, SLO, SLA and error budgets?

---

## 15. Caching in Microservices

216. 🟢 Where can caching be applied in a microservices architecture (client, CDN, gateway/Nginx, service, distributed cache, database)?
217. 🟡 What is the Cache-Aside pattern?
218. 🟡 What are read-through, write-through and write-behind caching?
219. 🟡 How do you invalidate caches across services (events, TTL)?
220. 🟡 What is a cache stampede / thundering herd? How do you prevent it?
221. 🟡 What is Redis and how is it used in microservices?
222. 🔴 How do you cache data owned by another service safely?
223. 🔴 What data should never be cached in financial systems? 💰

---

## 16. Observability — Logging, Metrics, Tracing, Health Checks

224. 🟢 What is observability? How is it different from monitoring?
225. 🟢 What are the three pillars of observability (logs, metrics, traces)?
226. 🟡 What is centralized logging? Name tools (ELK/Elastic, Seq, Loki, Splunk, Azure Monitor).
227. 🟡 What is structured logging and why is it essential in microservices?
228. 🟡 What is a correlation ID? How do you propagate it across HTTP calls and messages?
229. 🟡 What is distributed tracing? What are traces, spans and context propagation?
230. 🟡 What is W3C Trace Context (`traceparent` header)?
231. 🟡 What is OpenTelemetry? How do you add it to an ASP.NET Core service?
232. 🟡 What are Jaeger, Zipkin, Tempo and Application Insights?
233. 🟡 What metrics should every service expose (RED: Rate, Errors, Duration; USE: Utilization, Saturation, Errors)?
234. 🟡 What are Prometheus and Grafana?
235. 🟡 What is the Health Check API pattern? Liveness vs readiness vs startup probes?
236. 🟡 What should a readiness check verify? Should it check downstream dependencies?
237. 🟡 How do you pass the correlation ID from Nginx to backend services (`$request_id`)?
238. 🔴 What is log aggregation cost control (sampling, log levels)?
239. 🔴 What is tail-based vs head-based sampling in tracing?
240. 🔴 How do you alert effectively without alert fatigue?

---

## 17. Configuration & Secrets Management

241. 🟢 What is externalized configuration?
242. 🟡 How do you manage configuration across many services and environments?
243. 🟡 What are configuration servers / stores (Azure App Configuration, Consul KV, Spring Cloud Config, Kubernetes ConfigMaps)?
244. 🟡 How do you manage secrets (Azure Key Vault, HashiCorp Vault, Kubernetes Secrets, AWS Secrets Manager)?
245. 🟡 Why should secrets not be stored in `appsettings.json`, Docker images or Git?
246. 🟡 What are feature flags? How are they used in microservices?
247. 🔴 How do you rotate secrets without downtime?
248. 🔴 How do you change configuration at runtime without redeploying?

---

## 18. Security in Microservices

249. 🟢 How do you secure microservices?
250. 🟡 Where do you validate tokens — at the gateway, in each service, or both? Why?
251. 🟡 How do you propagate user identity from the gateway to downstream services?
252. 🟡 How do services authenticate each other (client credentials, mTLS, managed identity)?
253. 🟡 What is mTLS between services? How does a service mesh provide it?
254. 🟡 What is zero trust networking in microservices?
255. 🟡 What is the "token relay" pattern?
256. 🟡 Should internal services trust headers like `X-User-Id` set by the gateway? What are the risks?
257. 🟡 How do you secure message brokers (authentication, TLS, per-queue permissions)?
258. 🟡 How do you secure container images (scanning, minimal base images, non-root)?
259. 🔴 How do you implement authorization across services (central policy service vs local policies)?
260. 🔴 How do you audit cross-service actions in a regulated environment? 💰

---

## 19. Containers & Docker

261. 🟢 What is a container? How is it different from a virtual machine?
262. 🟢 What is Docker?
263. 🟢 What is a Docker image vs a container?
264. 🟢 What is a Dockerfile? Explain common instructions (`FROM`, `WORKDIR`, `COPY`, `RUN`, `EXPOSE`, `ENTRYPOINT`, `CMD`).
265. 🟡 What is a multi-stage Dockerfile? Write one for an ASP.NET Core app.
266. 🟡 What is the difference between `CMD` and `ENTRYPOINT`?
267. 🟡 What is Docker layer caching? How do you order Dockerfile instructions to use it?
268. 🟡 What are Docker volumes and bind mounts?
269. 🟡 What are Docker networks (bridge, host, overlay)?
270. 🟡 What is Docker Compose? How do you run Nginx + multiple ASP.NET Core services + Redis + RabbitMQ with Compose?
271. 🟡 What is `.dockerignore`?
272. 🟡 What are .NET container images (`sdk`, `aspnet`, `runtime`, `runtime-deps`, chiseled/distroless)?
273. 🟡 What port does an ASP.NET Core container listen on by default in .NET 8+ (8080)? Why changed from 80?
274. 🟡 Why do .NET 8+ images run as a non-root `app` user?
275. 🟡 How do you publish a container without a Dockerfile (`dotnet publish /t:PublishContainer`)?
276. 🔴 How do you reduce Docker image size?
277. 🔴 How do you handle graceful shutdown (SIGTERM) in a containerized ASP.NET Core app?

---

## 20. Kubernetes & Orchestration

278. 🟢 What is container orchestration? Why is it needed?
279. 🟢 What is Kubernetes?
280. 🟡 What are Pods, Deployments, ReplicaSets, Services, Namespaces?
281. 🟡 What are ClusterIP, NodePort and LoadBalancer services?
282. 🟡 What is an Ingress? What is an Ingress Controller? How does Nginx Ingress Controller work?
283. 🟡 What is the Gateway API in Kubernetes?
284. 🟡 What are ConfigMaps and Secrets?
285. 🟡 What are liveness, readiness and startup probes?
286. 🟡 What is Horizontal Pod Autoscaler (HPA)? What is KEDA?
287. 🟡 What are resource requests and limits?
288. 🟡 What is a rolling update in Kubernetes? How do you roll back?
289. 🟡 What are StatefulSets and DaemonSets?
290. 🟡 What is Helm?
291. 🟡 What are AKS, EKS and GKE?
292. 🔴 What happens to in-flight requests when a pod is terminated? How do you avoid dropped requests?
293. 🔴 Docker Compose vs Docker Swarm vs Kubernetes — when to use each?

---

## 21. Service Mesh & Sidecar Patterns

294. 🟡 What is the Sidecar pattern?
295. 🟡 What is the Ambassador pattern?
296. 🟡 What is the Adapter pattern (in container design)?
297. 🟡 What is a service mesh? What problems does it solve?
298. 🟡 What are Istio, Linkerd and Consul Connect?
299. 🟡 What is Envoy proxy?
300. 🟡 What is the data plane vs control plane?
301. 🔴 What is ambient mesh (sidecar-less)?
302. 🔴 When is a service mesh overkill?
303. 🟡 What is Dapr? What building blocks does it provide?

---

## 22. Deployment Patterns & CI/CD

304. 🟢 What is CI/CD?
305. 🟡 What is a rolling deployment?
306. 🟡 What is blue-green deployment? How do you implement it with Nginx?
307. 🟡 What is canary deployment? How do you implement weighted traffic splitting with Nginx?
308. 🟡 What is A/B testing vs canary release?
309. 🟡 What is a feature toggle / dark launch?
310. 🟡 What is shadow traffic / traffic mirroring (Nginx `mirror` directive)?
311. 🟡 What is immutable infrastructure?
312. 🟡 What is Infrastructure as Code (Terraform, Bicep, ARM, Pulumi)?
313. 🟡 What is GitOps (Argo CD, Flux)?
314. 🟡 What is a mono-repo vs poly-repo for microservices?
315. 🟡 How do you version and release independent services?
316. 🔴 How do you handle database schema changes during zero-downtime deployments (expand/contract)?
317. 🔴 How do you roll back a release that included a database migration?
318. 🔴 How do you deploy a change that spans three services in the right order?

---

## 23. Testing Microservices

319. 🟢 What is the testing pyramid for microservices?
320. 🟡 What are unit, integration, component, contract and end-to-end tests?
321. 🟡 What is consumer-driven contract testing (Pact)?
322. 🟡 How do you test a service in isolation (mocks, stubs, WireMock, Testcontainers)?
323. 🟡 How do you test message consumers and producers?
324. 🟡 Why are end-to-end tests expensive and flaky in microservices?
325. 🟡 What is testing in production (canary, synthetic monitoring)?
326. 🔴 How do you load test a microservices system?
327. 🔴 How do you test resiliency (fault injection, chaos testing)?
328. 🔴 How do you test sagas and compensations?

---

## 24. API Versioning & Contracts Between Services

329. 🟡 How do you version APIs between services?
330. 🟡 What is backward compatibility and forward compatibility?
331. 🟡 What is the tolerant reader pattern?
332. 🟡 What are breaking vs non-breaking changes in REST, gRPC and events?
333. 🟡 How do you share contracts — shared NuGet package vs OpenAPI/proto generation? Pros and cons?
334. 🔴 Why can a shared "common models" library create coupling?
335. 🔴 How do you deprecate and remove an old API version used by other teams?

---

## 25. .NET Microservices Ecosystem

336. 🟡 How do you build a microservice in ASP.NET Core? What does a typical service template include?
337. 🟡 What is eShop / eShopOnContainers reference application?
338. 🟡 What is MassTransit? What does it provide (abstraction over brokers, sagas, outbox, retries)? Note its licensing change in v9.
339. 🟡 What are NServiceBus, Wolverine, Rebus, Brighter, CAP?
340. 🟡 What is YARP (Yet Another Reverse Proxy)? How does it compare to Nginx as a gateway?
341. 🟡 What is Ocelot? What are its limitations?
342. 🟡 What is .NET Aspire? What does it provide (orchestration for local dev, service defaults, telemetry dashboard)?
343. 🟡 What is Dapr and how does it integrate with .NET?
344. 🟡 What is Steeltoe?
345. 🟡 What is gRPC in ASP.NET Core? What is gRPC JSON transcoding?
346. 🟡 How do you implement health checks, OpenTelemetry and resilience as "service defaults" shared by all services?
347. 🔴 What is Orleans (virtual actors) and when would you use it?

---

## 26. Microservices Anti-Patterns

348. 🟡 What is a distributed monolith?
349. 🟡 What is the shared database anti-pattern?
350. 🟡 What are nano-services (too fine-grained services)?
351. 🟡 What are chatty services?
352. 🟡 What is a "God service" / "entity service" anti-pattern?
353. 🟡 What is synchronous call chains / "death star" architecture?
354. 🟡 What is the "shared library hell" anti-pattern?
355. 🟡 What is "microservices envy" / adopting microservices for the wrong reasons?
356. 🟡 What is lack of automation / manual deployments in microservices?
357. 🔴 What is "big bang" migration and why does it fail?
358. 🔴 What is putting business logic in the API Gateway / ESB?

---

# Part B — Nginx (Reverse Proxy, Load Balancer, API Gateway)

## 27. Nginx Fundamentals & Architecture

359. 🟢 What is Nginx?
360. 🟢 What can Nginx be used for (web server, reverse proxy, load balancer, API gateway, cache, TLS terminator)?
361. 🟢 Why is Nginx popular for hosting ASP.NET Core applications on Linux?
362. 🟡 What is Nginx's architecture (master process and worker processes)?
363. 🟡 What is the event-driven, non-blocking model of Nginx? How does it differ from Apache's process/thread-per-request model?
364. 🟡 What are `worker_processes` and `worker_connections`? How do you calculate max clients?
365. 🟡 What is Nginx Open Source vs Nginx Plus? What features are only in Plus (active health checks, session persistence, API dashboard, dynamic upstream reconfiguration)?
366. 🟢 What are common Nginx commands (`nginx -t`, `nginx -s reload`, `nginx -s stop`, `systemctl reload nginx`)?
367. 🟡 What is the difference between `reload` and `restart`? Does `reload` drop connections?
368. 🟡 Where are Nginx configuration files located (`/etc/nginx/nginx.conf`, `conf.d/`, `sites-available/`, `sites-enabled/`)?
369. 🟡 What is OpenResty? What are Nginx modules (static vs dynamic)?

---

## 28. Nginx Configuration Structure

370. 🟢 What are contexts in Nginx (`main`, `events`, `http`, `server`, `location`, `upstream`, `stream`)?
371. 🟢 What is a `server` block? How does Nginx choose which server block handles a request (`listen`, `server_name`, `default_server`)?
372. 🟢 What is a `location` block?
373. 🟡 What are the types of location matching: exact (`=`), prefix, preferential prefix (`^~`), regex (`~`, `~*`)?
374. 🔴 What is the order/priority in which Nginx evaluates location blocks?
375. 🟡 What is the difference between `root` and `alias`?
376. 🟡 What does `try_files` do? How is it used for SPAs (Angular/React)?
377. 🟡 What is `rewrite` vs `return`? When should you prefer `return`?
378. 🟡 What are rewrite flags (`last`, `break`, `redirect`, `permanent`)?
379. 🟡 Why is `if` considered "evil" inside `location` blocks?
380. 🟡 What are Nginx variables (`$host`, `$remote_addr`, `$request_uri`, `$uri`, `$args`, `$scheme`, `$request_id`, `$upstream_addr`)?
381. 🟡 What is the `map` directive? Give a use case.
382. 🟡 What is `include` and how do you organise configs per service?
383. 🟡 How is directive inheritance handled between contexts? Why does `proxy_set_header` in a `location` override all inherited ones?
384. 🟡 What is the `error_page` directive?
385. 🟡 What is `client_max_body_size`? What error appears when it is exceeded (413)?

---

## 29. Nginx as a Reverse Proxy

386. 🟢 What is a reverse proxy?
387. 🟢 What is the difference between a forward proxy and a reverse proxy?
388. 🟢 What are the benefits of a reverse proxy (security, SSL termination, load balancing, caching, compression, single entry point)?
389. 🟢 What does `proxy_pass` do?
390. 🔴 What is the difference between `proxy_pass http://backend;` and `proxy_pass http://backend/;` (trailing slash and URI rewriting)?
391. 🟡 What headers should you forward to the backend (`Host`, `X-Real-IP`, `X-Forwarded-For`, `X-Forwarded-Proto`, `X-Forwarded-Host`)?
392. 🟡 What is `$proxy_add_x_forwarded_for`?
393. 🟡 What do `proxy_connect_timeout`, `proxy_send_timeout` and `proxy_read_timeout` control? What are their defaults?
394. 🟡 What is proxy buffering (`proxy_buffering`, `proxy_buffers`, `proxy_buffer_size`)? When should you disable it?
395. 🟡 What is `proxy_http_version 1.1` and why is it needed for keep-alive and WebSockets?
396. 🟡 What is `proxy_redirect`?
397. 🟡 What is `proxy_next_upstream`? What are the risks of retrying non-idempotent requests (POST)? 💰
398. 🟡 How do you hide or add response headers (`proxy_hide_header`, `add_header`)?
399. 🟡 What is `proxy_intercept_errors`?
400. 🟡 What is `proxy_cookie_path` / `proxy_cookie_domain`?
401. 🔴 What happens when the upstream closes the connection early? What does a 502 mean in Nginx?
402. 🔴 What is the difference between 502 Bad Gateway, 503 Service Unavailable and 504 Gateway Timeout from Nginx?

---

## 30. Hosting ASP.NET Core Behind Nginx

403. 🟢 How do you host an ASP.NET Core application on Linux with Nginx and Kestrel?
404. 🟢 Why is Nginx placed in front of Kestrel?
405. 🟡 How do you run the ASP.NET Core app as a service with systemd? What does a `.service` file contain?
406. 🟡 What is `UseForwardedHeaders` / `ForwardedHeadersOptions` and why is it required behind Nginx?
407. 🟡 What are `KnownProxies` and `KnownNetworks` (`KnownIPNetworks` in .NET 10)? What happens if they are not configured?
408. 🟡 Why does `Request.Scheme` show `http` instead of `https` behind Nginx? How do you fix it?
409. 🟡 Why does `HttpContext.Connection.RemoteIpAddress` show the Nginx IP instead of the client IP?
410. 🟡 Why do OIDC redirect URIs become `http://` behind Nginx?
411. 🟡 Should you use `UseHttpsRedirection` in the app when Nginx terminates TLS?
412. 🟡 Should HSTS be set in Nginx or ASP.NET Core?
413. 🟡 How should Kestrel listen (localhost port, Unix socket)? What are the benefits of Unix domain sockets?
414. 🟡 What is `ASPNETCORE_URLS` / `ASPNETCORE_HTTP_PORTS` and how does it relate to Nginx `proxy_pass`?
415. 🟡 How do you configure Kestrel limits (`MaxRequestBodySize`) to match Nginx `client_max_body_size`?
416. 🟡 How do you serve static files — from Nginx or from ASP.NET Core? Pros and cons?
417. 🟡 How do you host an Angular/React SPA and an ASP.NET Core API on the same domain using Nginx?
418. 🟡 How do you handle `PathBase` when the app is hosted under a sub-path (e.g., `/api/orders/`)?
419. 🔴 How do you achieve zero-downtime deployments of an ASP.NET Core app behind Nginx on a VM?
420. 🔴 How do you share Data Protection keys between multiple instances behind Nginx?
421. 🔴 How do you handle graceful shutdown so Nginx stops sending traffic before Kestrel stops?

---

## 31. Nginx as a Load Balancer

422. 🟢 How do you configure load balancing in Nginx (`upstream` block)?
423. 🟢 What is the default load balancing method in Nginx?
424. 🟡 What load balancing methods does Nginx support (round robin, `least_conn`, `ip_hash`, `hash`, `random two least_conn`, `least_time` in Plus)?
425. 🟡 What is weighted load balancing (`weight=`)?
426. 🟡 What do `max_fails` and `fail_timeout` do? What is passive health checking?
427. 🟡 What are `backup` and `down` server parameters?
428. 🟡 What is `max_conns`?
429. 🟡 What is upstream `keepalive` and why does it improve performance? Which other directives are required with it?
430. 🟡 What is session persistence / sticky sessions in Nginx (`ip_hash`, `hash $cookie_...`, `sticky` in Plus)?
431. 🟡 Why can `ip_hash` cause uneven load (clients behind NAT/corporate proxies)?
432. 🟡 How do you do active health checks with Nginx Open Source (workarounds) vs Nginx Plus (`health_check`)?
433. 🟡 What is `resolve` / DNS re-resolution in upstreams? Why does Nginx cache DNS at startup by default?
434. 🟡 What is Layer 4 (TCP/UDP) load balancing with the `stream` module?
435. 🟡 How do you load balance a database or RabbitMQ with the `stream` module?
436. 🔴 How do you drain a server from the upstream pool during deployment?
437. 🔴 How do you implement blue-green switching with Nginx upstreams?
438. 🔴 How do you implement canary traffic splitting with `split_clients`?
439. 🔴 How do you make Nginx itself highly available (keepalived + VRRP, multiple instances behind a cloud LB)?
440. 🔴 What happens to load balancing when one backend is slow but not failing?

---

## 32. Nginx as an API Gateway

441. 🟢 How can Nginx act as an API Gateway?
442. 🟡 How do you route requests to different microservices by path (`/api/orders` → orders service, `/api/payments` → payments service)?
443. 🟡 How do you route by host/subdomain, header or HTTP method?
444. 🟡 How do you strip a path prefix before forwarding to a service?
445. 🟡 How do you implement rate limiting in Nginx (`limit_req_zone`, `limit_req`, `burst`, `nodelay`)?
446. 🟡 How do you limit concurrent connections (`limit_conn_zone`, `limit_conn`)?
447. 🟡 How do you rate limit per API key or per client ID instead of per IP?
448. 🟡 What status code does Nginx return when rate limited by default (503)? How do you change it to 429 (`limit_req_status`)?
449. 🟡 How do you validate API keys in Nginx (`map` + `if`)?
450. 🟡 How do you implement authentication at the gateway using `auth_request` (subrequest to an auth service)?
451. 🟡 Can Nginx Open Source validate JWTs natively? What are the options (Nginx Plus `auth_jwt`, njs, OpenResty/Lua, `auth_request`)?
452. 🟡 How do you pass user claims from the gateway to services as headers? How do you prevent clients from spoofing them?
453. 🟡 How do you configure CORS at the Nginx level? Should CORS be handled in Nginx or ASP.NET Core?
454. 🟡 How do you add a correlation ID (`$request_id`) and forward it to all services?
455. 🟡 How do you implement request size limits and timeouts per route?
456. 🟡 How do you return custom JSON error responses for 404/429/502/504 from Nginx?
457. 🟡 How do you implement API versioning routing in Nginx (`/v1/`, `/v2/`)?
458. 🟡 How do you implement IP allowlisting/denylisting for admin APIs (`allow`, `deny`)?
459. 🟡 How do you protect internal-only endpoints (e.g., `/health`, `/metrics`, `/swagger`) from public access?
460. 🔴 Can Nginx do response aggregation (Gateway Aggregation pattern)? What are the alternatives (BFF service, njs)?
461. 🔴 What is njs (Nginx JavaScript)? What can you do with it?
462. 🔴 Nginx vs YARP vs Ocelot vs Kong vs Azure API Management — when would you choose each as an API gateway?
463. 🔴 What are the limitations of using Nginx Open Source as a full API gateway?

---

## 33. SSL/TLS Termination & HTTPS in Nginx

464. 🟢 What is SSL/TLS termination?
465. 🟢 How do you configure HTTPS in Nginx (`ssl_certificate`, `ssl_certificate_key`, `listen 443 ssl`)?
466. 🟡 How do you redirect HTTP to HTTPS in Nginx?
467. 🟡 What TLS protocols and ciphers should be enabled (`ssl_protocols TLSv1.2 TLSv1.3`)?
468. 🟡 What is HSTS and how do you set it in Nginx?
469. 🟡 What is OCSP stapling?
470. 🟡 What is SSL session caching (`ssl_session_cache`, `ssl_session_timeout`)?
471. 🟡 How do you obtain and renew certificates with Let's Encrypt / Certbot?
472. 🟡 What is SNI and how does Nginx serve multiple domains with different certificates?
473. 🟡 What is SSL termination vs SSL passthrough vs SSL re-encryption (end-to-end TLS)?
474. 🟡 When must traffic between Nginx and backend services also be encrypted? 💰
475. 🔴 How do you configure mTLS (client certificate verification) in Nginx (`ssl_verify_client`, `ssl_client_certificate`)? 💰
476. 🔴 How do you forward client certificate details to the backend?
477. 🟡 How do you enable HTTP/2 and HTTP/3 (QUIC) in Nginx?

---

## 34. Nginx Caching, Compression & Performance

478. 🟡 How do you enable proxy caching in Nginx (`proxy_cache_path`, `proxy_cache`, `proxy_cache_valid`, `proxy_cache_key`)?
479. 🟡 How do you bypass the cache for certain requests (`proxy_cache_bypass`, `proxy_no_cache`)?
480. 🟡 What is `proxy_cache_use_stale` and how does it improve resilience?
481. 🟡 What is `proxy_cache_lock` and how does it prevent cache stampede?
482. 🟡 How do you purge cache entries?
483. 🟡 What is micro-caching?
484. 🔴 Why must you be careful caching authenticated API responses at the Nginx level? 💰
485. 🟡 How do you enable gzip compression (`gzip`, `gzip_types`, `gzip_min_length`)? What about Brotli?
486. 🟡 How do you cache static files with `expires` and `Cache-Control` headers?
487. 🟡 What are `sendfile`, `tcp_nopush`, `tcp_nodelay` and `keepalive_timeout`?
488. 🟡 What is `open_file_cache`?
489. 🔴 How do you tune Nginx for high concurrency (`worker_rlimit_nofile`, OS `ulimit`, `somaxconn`)?
490. 🔴 How do you benchmark Nginx and backends (wrk, ab, k6)?

---

## 35. Nginx Security

491. 🟡 How do you hide the Nginx version (`server_tokens off`)?
492. 🟡 Which security headers should Nginx add (`X-Content-Type-Options`, `X-Frame-Options`, `Content-Security-Policy`, `Referrer-Policy`, `Strict-Transport-Security`)?
493. 🟡 Why does `add_header` not apply to error responses unless you use `always`?
494. 🟡 How do you protect against slowloris attacks (`client_body_timeout`, `client_header_timeout`)?
495. 🟡 How do you limit request body size and header size?
496. 🟡 How do you block specific user agents, IPs or countries (GeoIP)?
497. 🟡 How do you prevent clients from spoofing `X-Forwarded-For` / internal headers?
498. 🟡 How do you add basic authentication in Nginx (`auth_basic`)? Where is it acceptable?
499. 🟡 What is ModSecurity / a WAF with Nginx?
500. 🔴 What is an open proxy misconfiguration and how do you avoid it?
501. 🔴 What is the alias path traversal vulnerability (`location /files { alias /data/; }`)?
502. 🔴 What is HTTP request smuggling and how do proxies like Nginx relate to it?
503. 🔴 How do you protect Nginx against DDoS (rate limits, connection limits, CDN, cloud protection)?

---

## 36. Nginx with WebSockets, SignalR, gRPC & Streaming

504. 🟡 How do you configure Nginx to proxy WebSockets (`Upgrade` and `Connection` headers, `map $http_upgrade`)?
505. 🟡 How do you configure Nginx for ASP.NET Core SignalR? Why do you need sticky sessions when scaling SignalR without Azure SignalR/backplane?
506. 🟡 Why do WebSocket connections drop after 60 seconds behind Nginx? How do you fix it?
507. 🟡 How do you proxy gRPC with Nginx (`grpc_pass`, HTTP/2)?
508. 🟡 How do you configure Server-Sent Events (SSE) or streaming responses (disable buffering, `X-Accel-Buffering: no`)?
509. 🟡 How do you handle large file uploads and downloads through Nginx (`client_max_body_size`, `proxy_request_buffering off`, `X-Accel-Redirect`)?
510. 🔴 What is `X-Accel-Redirect` and how can ASP.NET Core use it to let Nginx serve protected files?

---

## 37. Nginx Logging, Monitoring & Troubleshooting

511. 🟢 Where are Nginx access and error logs? What do they contain?
512. 🟡 How do you define a custom log format (`log_format`) including `$request_time`, `$upstream_response_time`, `$upstream_addr`, `$request_id`?
513. 🟡 What is the difference between `$request_time` and `$upstream_response_time`? How do you use them to find whether Nginx or the backend is slow?
514. 🟡 How do you log in JSON format for ELK/Loki?
515. 🟡 What are error log levels (`debug`, `info`, `notice`, `warn`, `error`, `crit`)?
516. 🟡 How do you monitor Nginx (`stub_status`, Prometheus Nginx exporter, Nginx Plus API)?
517. 🟡 How do you troubleshoot a 502 Bad Gateway?
518. 🟡 How do you troubleshoot a 504 Gateway Timeout?
519. 🟡 How do you troubleshoot a 413 Request Entity Too Large?
520. 🟡 How do you troubleshoot a 404 that happens only through Nginx but not when calling Kestrel directly?
521. 🟡 How do you troubleshoot "upstream sent too big header while reading response header from upstream"?
522. 🟡 How do you troubleshoot "connect() failed (111: Connection refused) while connecting to upstream"?
523. 🟡 How do you troubleshoot "no live upstreams while connecting to upstream"?
524. 🟡 What does a 499 status code in Nginx logs mean?
525. 🔴 How do you trace a single request from Nginx through multiple microservices?
526. 🔴 What is log rotation (`logrotate`) and why does Nginx need `USR1` signal / reopen?

---

## 38. Nginx in Docker & Kubernetes

527. 🟡 How do you run Nginx in Docker as a reverse proxy for multiple ASP.NET Core containers?
528. 🟡 How does Nginx resolve container names in Docker Compose (Docker DNS `127.0.0.11`, `resolver`)?
529. 🟡 Why does Nginx fail to start if an upstream container is not yet running? How do you fix it?
530. 🟡 Why does Nginx keep sending traffic to an old container IP after a container restarts?
531. 🟡 How do you use environment variables in Nginx configs in Docker (`envsubst` templates)?
532. 🟡 What is the Nginx Ingress Controller in Kubernetes? Community `ingress-nginx` vs F5 NGINX Ingress Controller?
533. 🟡 How do you configure rate limiting, TLS, rewrites and timeouts using Ingress annotations?
534. 🟡 What is the status of the community `ingress-nginx` project and the move to Gateway API?
535. 🔴 Do you still need Nginx in front of services inside Kubernetes? When is it redundant?

---

## 39. Nginx Alternatives & Comparisons

536. 🟡 Nginx vs Apache HTTP Server?
537. 🟡 Nginx vs HAProxy?
538. 🟡 Nginx vs Envoy?
539. 🟡 Nginx vs Traefik?
540. 🟡 Nginx vs YARP for .NET teams?
541. 🟡 Nginx vs IIS + ARR (Application Request Routing)?
542. 🟡 Nginx vs cloud load balancers (Azure Application Gateway, AWS ALB)?
543. 🔴 Why would you put a cloud load balancer in front of Nginx? Why not?

---

# Part C — IIS Basics

## 40. IIS Fundamentals

544. 🟢 What is IIS (Internet Information Services)?
545. 🟢 What is the difference between IIS, IIS Express and Kestrel?
546. 🟢 What is a website, an application and a virtual directory in IIS?
547. 🟢 What is an application pool? Why is it used?
548. 🟢 What is the worker process (`w3wp.exe`)?
549. 🟡 What is the application pool identity (`ApplicationPoolIdentity`, NetworkService, custom account)?
550. 🟡 What is application pool recycling? What triggers it?
551. 🟡 What is idle timeout in an application pool and why does it cause slow first requests?
552. 🟡 What are bindings (protocol, IP, port, host header) in IIS?
553. 🟡 How do you configure HTTPS and certificates in IIS?
554. 🟡 What is `web.config` used for in IIS?
555. 🟡 What is the integrated vs classic pipeline mode?
556. 🟡 What is a web garden? Why is it not recommended for ASP.NET Core?
557. 🟡 What is IIS URL Rewrite module?
558. 🟡 What is ARR (Application Request Routing)? How can IIS act as a reverse proxy/load balancer?
559. 🟡 What is HTTP.sys and how does it relate to IIS?
560. 🟡 Where are IIS logs stored? What is Failed Request Tracing?

---

## 41. Hosting ASP.NET Core on IIS

561. 🟢 How do you host an ASP.NET Core application on IIS?
562. 🟢 What is the .NET Hosting Bundle? Why must it be installed?
563. 🟢 What is the ASP.NET Core Module (ANCM)?
564. 🟡 What is in-process hosting vs out-of-process hosting? Which is the default and faster?
565. 🟡 In out-of-process hosting, what web server runs the app (Kestrel) and how does IIS forward requests?
566. 🟡 What should the application pool's .NET CLR version be set to for ASP.NET Core ("No Managed Code")? Why?
567. 🟡 What does the generated `web.config` for ASP.NET Core contain (`aspNetCore` element, `processPath`, `hostingModel`, `stdoutLogEnabled`)?
568. 🟡 How do you troubleshoot "HTTP Error 500.30 / 500.31 / 500.19 / 502.5" in IIS?
569. 🟡 How do you enable stdout logs for startup errors?
570. 🟡 What is `app_offline.htm` and how is it used during deployment?
571. 🟡 How do you set environment variables for an app hosted in IIS?
572. 🟡 How do you host multiple ASP.NET Core apps on the same IIS server?
573. 🟡 How do you use Windows Authentication with ASP.NET Core on IIS?
574. 🔴 IIS vs Nginx for hosting ASP.NET Core — when would you choose each?
575. 🔴 What changes when you move an app from IIS (Windows) to Nginx (Linux) — forwarded headers, file paths, case sensitivity, Windows auth, logging?

---

# Part D — Practice

## 42. Financial-Domain Microservices Questions 💰

576. 🟡💰 How would you decompose a core banking or payments platform into microservices?
577. 🔴💰 How do you guarantee that a payment is processed exactly once across services?
578. 🔴💰 How do you design a ledger service that is the single source of truth for balances?
579. 🔴💰 How do you implement a fund transfer saga with compensations?
580. 🔴💰 How do you handle a timeout from a payment provider (unknown outcome)? What is reconciliation?
581. 🔴💰 How do you guarantee ordering of transactions for the same account (partition key = account ID)?
582. 🔴💰 How do you prevent double debits when messages are redelivered?
583. 🔴💰 How do you design an audit trail across microservices for regulators?
584. 🔴💰 How do you keep latency low for a trading platform built with microservices?
585. 🔴💰 How do you design fraud detection as an event-driven service?
586. 🔴💰 How do you handle end-of-day batch processing in a microservices architecture?
587. 🔴💰 How do you meet data residency and compliance requirements (RBI data localisation, PCI-DSS)?
588. 🔴💰 How do you configure Nginx for a banking API (TLS 1.2+, mTLS for partners, strict timeouts, no retries on POST, rate limits)?
589. 🔴💰 Why must `proxy_next_upstream` be carefully configured for payment endpoints?
590. 🔴💰 How do you design a notification service (SMS, email, push) for transaction alerts that is reliable but doesn't block payments?

---

## 43. Tricky Questions

591. 🟡 If microservices are independent, why does deploying one service break another?
592. 🟡 Is calling another service's database directly ever acceptable?
593. 🟡 Can two microservices share the same database server but different schemas? Is that a shared database?
594. 🟡 If all your services must be deployed together, are they microservices?
595. 🟡 Is a message broker a single point of failure?
596. 🟡 Can events be lost even with at-least-once delivery?
597. 🟡 Why can retries make an outage worse?
598. 🟡 Why can a circuit breaker per instance behave differently from a global one?
599. 🟡 Why does adding more instances not always improve throughput?
600. 🟡 Why can a health check that checks the database cause a cascading restart of all pods?
601. 🟡 Is eventual consistency acceptable for account balances? Where is it and where isn't it? 💰
602. 🟡 Why can a shared NuGet package of DTOs become a distributed monolith?
603. 🟡 Why is a 2PC transaction across microservices discouraged even though it guarantees consistency?
604. 🟡 What happens if the outbox publisher publishes a message twice?
605. 🟡 What happens if events arrive out of order (e.g., `OrderShipped` before `OrderCreated`)?
606. 🟡 What happens if a saga step succeeds but the reply message is lost?
607. 🟡 Why can't you rely on timestamps to order events from different services?
608. 🟡 Is Nginx an API Gateway or a reverse proxy? Can it be both?
609. 🟡 Is a load balancer always a reverse proxy? Is a reverse proxy always a load balancer?
610. 🟡 Why does Nginx return 502 right after deploying a new version of the app?
611. 🟡 Why does Nginx return 504 for a report endpoint that takes 90 seconds?
612. 🟡 Why do POST requests get executed twice when one backend times out?
613. 🟡 Why does `ip_hash` send most traffic to one server?
614. 🟡 Why does Nginx keep routing to a backend that was removed or whose IP changed?
615. 🟡 Why does my app generate `http://` links even though users access it over HTTPS?
616. 🟡 Why does my app log Nginx's IP as the client IP?
617. 🟡 Why do my WebSocket/SignalR connections fail behind Nginx?
618. 🟡 Why do uploads larger than 1 MB fail behind Nginx?
619. 🟡 Why do my custom security headers disappear on some responses?
620. 🟡 Why does `location /api` also match `/apidocs`?
621. 🟡 Why does `proxy_pass http://orders/;` change the forwarded path but `proxy_pass http://orders;` doesn't?
622. 🟡 Why does a regex location override my prefix location?
623. 🟡 Why do my `proxy_set_header` directives at the `server` level stop working when I add one inside a `location`?
624. 🟡 Why does `nginx -s reload` not pick up my config change? (syntax error, wrong file, not included)
625. 🔴 Why is the client IP wrong even after configuring `X-Forwarded-For` (multiple proxies, `KnownProxies`, `ForwardLimit`)?
626. 🔴 Why can caching at Nginx leak one user's data to another user?
627. 🔴 Why does Nginx rate limiting allow bursts above the configured rate?
628. 🔴 Why does rate limiting behave inconsistently with multiple Nginx instances?
629. 🔴 Why does the first request after IIS idle time take several seconds?
630. 🔴 Why does an app work in IIS Express but fail in full IIS (permissions, app pool identity, Hosting Bundle)?

---

## 44. Predict the Behavior (Nginx Config & Code Snippets)

> What happens with each configuration or code snippet? If it's wrong, explain why and how to fix it.

**631. 🟡 Trailing slash in proxy_pass**
```nginx
location /api/orders/ {
    proxy_pass http://orders_service/;
}
```
A client calls `/api/orders/123`. What path does the orders service receive? What if `proxy_pass` has no trailing slash?

**632. 🟡 Location priority**
```nginx
location /images/ { return 200 "prefix"; }
location ~* \.(png|jpg)$ { return 200 "regex"; }
location ^~ /images/static/ { return 200 "preferential"; }
location = /images/logo.png { return 200 "exact"; }
```
What is returned for `/images/logo.png`, `/images/photo.png`, `/images/static/a.png`, `/images/readme.txt`?

**633. 🟡 Default load balancing**
```nginx
upstream api {
    server 10.0.0.1:5000;
    server 10.0.0.2:5000 weight=3;
}
```
How are 8 requests distributed?

**634. 🟡 Passive health check**
```nginx
upstream api {
    server 10.0.0.1:5000 max_fails=3 fail_timeout=30s;
    server 10.0.0.2:5000;
}
```
Server 1 fails 3 times in 30 seconds. What happens to traffic? When does it come back?

**635. 🔴 Retrying POST**
```nginx
location /api/payments/ {
    proxy_pass http://payments;
    proxy_next_upstream error timeout http_502 non_idempotent;
}
```
A payment request times out on server 1. What happens? Why is this dangerous? 💰

**636. 🟡 Missing forwarded headers**
```nginx
location / { proxy_pass http://localhost:5000; }
```
```csharp
app.MapGet("/info", (HttpContext c) => $"{c.Request.Scheme}://{c.Request.Host} from {c.Connection.RemoteIpAddress}");
```
A user calls `https://bank.example.com/info`. What is returned? How do you fix it in both Nginx and ASP.NET Core?

**637. 🟡 Forwarded headers without KnownProxies**
```csharp
app.UseForwardedHeaders(new ForwardedHeadersOptions
{
    ForwardedHeaders = ForwardedHeaders.XForwardedFor | ForwardedHeaders.XForwardedProto
});
// Nginx runs on a different host/container (10.0.0.5)
```
Are the headers applied? Why or why not?

**638. 🟡 WebSocket proxying**
```nginx
location /hubs/ {
    proxy_pass http://signalr_backend;
}
```
What happens to SignalR WebSocket connections? What must be added?

**639. 🟡 Proxy read timeout**
```nginx
location /api/reports/ { proxy_pass http://reports; }
```
The report endpoint takes 75 seconds. What does the client receive?

**640. 🟡 Body size**
```nginx
server { listen 80; location / { proxy_pass http://app; } }
```
A client uploads a 5 MB file. What happens?

**641. 🟡 Rate limiting**
```nginx
limit_req_zone $binary_remote_addr zone=api:10m rate=10r/s;
location /api/ {
    limit_req zone=api burst=20 nodelay;
    proxy_pass http://api;
}
```
A client sends 40 requests in one second. How many succeed? What status do the rest get? How do you change it to 429?

**642. 🟡 add_header inheritance**
```nginx
server {
    add_header X-Frame-Options DENY;
    location /api/ {
        add_header X-Request-Id $request_id;
        proxy_pass http://api;
    }
}
```
Does a response from `/api/` contain `X-Frame-Options`?

**643. 🟡 ip_hash behind a corporate proxy**
```nginx
upstream app { ip_hash; server a:5000; server b:5000; server c:5000; }
```
Most users come from one corporate network with a single public IP. What happens?

**644. 🔴 DNS caching**
```nginx
upstream orders { server orders-service:8080; }
```
In Docker, the `orders-service` container restarts and gets a new IP. What happens to traffic?

**645. 🔴 Caching authenticated responses**
```nginx
proxy_cache_path /var/cache/nginx keys_zone=api_cache:10m;
location /api/accounts/ {
    proxy_cache api_cache;
    proxy_cache_valid 200 5m;
    proxy_pass http://accounts;
}
```
What is the risk? 💰

**646. 🔴 alias path traversal**
```nginx
location /files {
    alias /var/www/files/;
}
```
What happens with a request to `/files../app/appsettings.json`?

**647. 🟡 SPA routing**
```nginx
location / { root /var/www/spa; }
```
A user refreshes the page at `/dashboard/settings`. What happens? How do you fix it?

**648. 🟡 Canary split**
```nginx
split_clients "${remote_addr}" $backend {
    10%  orders_v2;
    *    orders_v1;
}
location /api/orders/ { proxy_pass http://$backend; }
```
What does this do? What are its limitations?

**649. 🔴 Outbox missing**
```csharp
await _db.Orders.AddAsync(order);
await _db.SaveChangesAsync();
await _bus.Publish(new OrderCreated(order.Id));   // broker is down at this moment
```
What happens? How do you fix it?

**650. 🔴 Non-idempotent consumer**
```csharp
public async Task Consume(ConsumeContext<PaymentReceived> ctx)
{
    var acc = await _db.Accounts.FindAsync(ctx.Message.AccountId);
    acc.Balance += ctx.Message.Amount;
    await _db.SaveChangesAsync();
}
```
The broker redelivers the message after a consumer crash. What happens? How do you fix it? 💰

**651. 🔴 Retry everywhere**
```text
Client retries 3x → Nginx proxy_next_upstream tries 2 servers → Service A Polly retries 3x → Service B
```
Service B is down. How many calls can Service B receive from one user click?

**652. 🟡 IIS app pool setting**
```text
Application pool: .NET CLR Version v4.0, Managed pipeline: Integrated, ASP.NET Core 8 app, Hosting Bundle not installed
```
What happens when the site starts? What needs to change?

---

## 45. Scenario-Based Questions — Microservices Design

653. 🟡 Your monolith e-commerce app is slow to release. Management wants microservices. How do you start?
654. 🟡 The Orders service needs customer name and address for every order listing. How do you get that data without calling the Customer service each time?
655. 🟡 An order requires stock reservation, payment and shipping across 3 services. How do you keep data consistent?
656. 🟡 The Payment service is down. What should the Order service do?
657. 🟡 A downstream service is slow and causing your service's thread pool to exhaust. What patterns do you apply?
658. 🟡 A consumer receives the same event twice and creates duplicate records. How do you fix it?
659. 🟡 Events must be processed in order per customer. How do you design it with Kafka or RabbitMQ?
660. 🟡 One team changes an event schema and breaks three consumers. How do you prevent this?
661. 🟡 You need to search across Orders, Customers and Products. How do you design it (search service with Elasticsearch fed by events)?
662. 🟡 You need a dashboard that shows data from 8 services. How do you build it?
663. 🟡 How do you trace a failed request that went through 6 services?
664. 🟡 A new service needs historical data from other services. How do you backfill it?
665. 🔴 Two services keep calling each other synchronously in a loop. How do you redesign?
666. 🔴 A message is stuck in the DLQ for an important payment. What is your process to investigate and replay it? 💰
667. 🔴 You have 50 services and every team implements logging, health checks and resilience differently. How do you standardise?
668. 🔴 A shared "Common" library is updated and all 30 services must be redeployed. How do you break this coupling?
669. 🔴 How do you split a large shared database used by 10 services?
670. 🔴 How do you handle a long-running business process (loan approval over several days) across services? 💰
671. 🔴 A service's database needs a breaking schema change while other services consume its events. How do you roll it out?
672. 🔴 You need to delete a customer's data from all services (GDPR / right to be forgotten). How do you design it?
673. 🔴 A third-party payment provider callback (webhook) may arrive before your own service has saved the payment. How do you handle it? 💰
674. 🔴 Your Kafka consumer lag keeps growing during peak hours. How do you investigate and fix it?

---

## 46. Scenario-Based Questions — Nginx & Production Issues

675. 🟡 After a deployment, users get 502 Bad Gateway for 30 seconds. How do you achieve zero-downtime deploys behind Nginx?
676. 🟡 Users get 504 Gateway Timeout on a file export endpoint. How do you fix it properly (timeouts vs async export)?
677. 🟡 Login works on one server but users get logged out when the load balancer sends them to another server. Why?
678. 🟡 OIDC login fails with "Correlation failed" only behind Nginx. What do you check?
679. 🟡 Your API generates Swagger links and redirects with `http://` and the wrong host. How do you fix it?
680. 🟡 Client IPs in your audit logs all show `127.0.0.1`. How do you fix it? 💰
681. 🟡 One backend server is slower than others and users report intermittent slowness. How do you identify and handle it in Nginx?
682. 🟡 You need to route 5% of traffic to a new version of the Payments service. How do you configure Nginx?
683. 🟡 You need to block a specific client that is abusing your API. How do you do it in Nginx?
684. 🟡 You need to expose `/swagger` only to the internal network. How do you configure Nginx?
685. 🟡 SignalR connections keep reconnecting every minute behind Nginx. How do you fix it?
686. 🟡 You need to host an Angular frontend and 5 microservice APIs under one domain with Nginx. Write the routing plan.
687. 🟡 Nginx error log shows "upstream sent too big header". How do you fix it?
688. 🟡 A burst of traffic during a sale overloads your services. How do you protect them using Nginx?
689. 🔴 Nginx itself becomes a single point of failure. How do you make it highly available?
690. 🔴 You see many 499 status codes in Nginx logs. What does it mean and how do you investigate?
691. 🔴 A partner bank requires mutual TLS for API calls. How do you configure Nginx and pass the certificate identity to your service? 💰
692. 🔴 Your security team wants TLS between Nginx and backend services too. How do you configure it?
693. 🔴 You are moving from IIS on Windows to Nginx on Linux. What changes and risks do you list?
694. 🔴 Rate limiting must be per user (from JWT) rather than per IP. How would you implement it with Nginx?
695. 🔴 You must add authentication at the gateway but Nginx Open Source has no native JWT validation. What are your options?
696. 🔴 Nginx caches a response containing one customer's data and serves it to another. How do you find and fix the issue? 💰

---

## 47. System Design Scenarios

697. 🔴 Design a microservices-based e-commerce platform with Nginx as gateway and load balancer.
698. 🔴 Design a digital banking platform (accounts, payments, cards, notifications, KYC) with microservices. 💰
699. 🔴 Design a UPI-like payment processing system with high throughput and exactly-once processing. 💰
700. 🔴 Design a stock trading order management system with low latency. 💰
701. 🔴 Design a notification service that sends millions of SMS/emails per day reliably.
702. 🔴 Design a food delivery platform (orders, restaurants, riders, payments, tracking).
703. 🔴 Design a ride-hailing platform's microservices and communication patterns.
704. 🔴 Design a URL shortener as microservices behind Nginx.
705. 🔴 Design a centralized logging, metrics and tracing platform for 100 microservices.
706. 🔴 Design the migration of a 15-year-old .NET Framework monolith hosted on IIS to .NET microservices on Linux behind Nginx.
707. 🔴 Design a multi-region active-active deployment with Nginx and microservices.
708. 🔴 Design a loan origination system with long-running workflows and human approvals. 💰

---

## 48. Hands-On Tasks

709. 🟢 Write a multi-stage Dockerfile for an ASP.NET Core Web API.
710. 🟢 Write a Docker Compose file with Nginx, two ASP.NET Core services, Redis and RabbitMQ.
711. 🟡 Write an Nginx config that routes `/api/orders/` and `/api/payments/` to two different upstreams.
712. 🟡 Configure Nginx load balancing across three instances with `least_conn`, `max_fails` and upstream `keepalive`.
713. 🟡 Configure HTTPS with HTTP→HTTPS redirect, TLS 1.2/1.3 only, and HSTS.
714. 🟡 Configure rate limiting returning 429 for `/api/` and stricter limits for `/api/auth/login`.
715. 🟡 Configure WebSocket proxying for a SignalR hub.
716. 🟡 Configure `ForwardedHeaders` in ASP.NET Core correctly for Nginx.
717. 🟡 Configure Nginx to serve an Angular SPA with `try_files` and proxy `/api/` to the backend.
718. 🟡 Add `$request_id` as a correlation ID header and include it in a JSON access log format.
719. 🟡 Configure custom JSON error pages for 502, 503, 504 and 429.
720. 🟡 Create a systemd service file to run an ASP.NET Core app behind Nginx.
721. 🟡 Implement a resilient `HttpClient` with retry, timeout and circuit breaker using `AddStandardResilienceHandler`.
722. 🟡 Implement health checks with separate liveness and readiness endpoints.
723. 🟡 Add OpenTelemetry tracing to two services and view a trace across both.
724. 🔴 Implement the Transactional Outbox pattern with EF Core and a background publisher.
725. 🔴 Implement an idempotent message consumer using an Inbox table.
726. 🔴 Implement an orchestration saga for order → payment → shipping using MassTransit or a custom state machine.
727. 🔴 Implement a choreography saga using events and compensations.
728. 🔴 Implement gateway authentication using Nginx `auth_request` with an ASP.NET Core auth service.
729. 🔴 Implement blue-green deployment switching using Nginx upstreams and a reload.
730. 🔴 Implement canary routing with `split_clients` or a header-based `map`.
731. 🔴 Configure Nginx mTLS for a partner endpoint and forward the client certificate subject to the backend. 💰
732. 🔴 Implement the Strangler Fig pattern with Nginx routing some paths to a new service and the rest to the legacy app.

---

## 49. Rapid-Fire Round

733. 🟢 What does the "12" in 12-Factor App refer to?
734. 🟢 What pattern gives each service its own database?
735. 🟢 What pattern manages distributed transactions with compensations?
736. 🟢 What pattern stops calling a failing service for a while?
737. 🟢 What pattern isolates resources so one failure doesn't sink everything?
738. 🟢 What pattern solves the dual-write problem?
739. 🟢 What pattern separates reads and writes?
740. 🟢 What pattern stores state as a sequence of events?
741. 🟢 What pattern gradually replaces a legacy system?
742. 🟢 What pattern creates a separate gateway per client type?
743. 🟢 What is the default Nginx load balancing algorithm?
744. 🟢 Which Nginx directive forwards requests to a backend?
745. 🟢 Which command tests Nginx configuration syntax?
746. 🟢 Which command reloads Nginx without downtime?
747. 🟢 What is the default `client_max_body_size` in Nginx?
748. 🟢 What is the default `proxy_read_timeout` in Nginx?
749. 🟡 What status code does Nginx return when the upstream is unreachable?
750. 🟡 What status code does Nginx return when the upstream times out?
751. 🟡 What status code does Nginx log when the client closes the connection early?
752. 🟡 What status code does Nginx return by default when a request is rate limited?
753. 🟡 Which Nginx directive enables sticky sessions by client IP in open source?
754. 🟡 Which Nginx directive splits traffic by percentage?
755. 🟡 Which Nginx module does TCP/UDP load balancing?
756. 🟡 Which Nginx directive delegates authentication to a subrequest?
757. 🟡 Which ASP.NET Core middleware must be configured behind Nginx?
758. 🟡 Which header tells the backend the original protocol (HTTP/HTTPS)?
759. 🟡 Which header carries the original client IP chain?
760. 🟡 What is the IIS worker process name?
761. 🟡 What must the IIS app pool CLR version be for ASP.NET Core?
762. 🟡 What is installed on a server to host ASP.NET Core in IIS?
763. 🟡 Which IIS hosting model runs the app inside `w3wp.exe`?
764. 🔴 What is the difference between `$request_time` and `$upstream_response_time` in one line?
765. 🔴 What is the difference between a service mesh and an API gateway in one line?
766. 🔴 What is the difference between choreography and orchestration in one line?
767. 🔴 What is the difference between at-least-once delivery and idempotent processing in one line?

---

> **Series complete:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS.
