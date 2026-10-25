# 🎯 AWS Interview Questions — Part 13 (Scenario-Focused, Questions Only)

> **Level:** 2–3 years of experience (backend / .NET developer working with AWS).
> **Built around our stack:** ASP.NET Core Web APIs & MVC, microservices, **Nginx** as reverse proxy / load balancer / API gateway on **RHEL**, **Kafka** (Amazon MSK), **Redis** (ElastiCache), **SQL Server / MySQL / PostgreSQL / Oracle** (Amazon RDS / Aurora), **YugabyteDB** (self-managed on EC2/EKS), JWT/OAuth authentication, Docker/Podman containers, CI/CD, observability, and financial-domain requirements.
> **Format:** A short concepts section to check basics, then **scenario-based questions** grouped by area — the style most interviewers use for 2–3 year candidates.
> **Based on question patterns from:** product companies, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced (good to know) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Core Concepts (Quick Check)**
1. AWS Basics, Regions & Availability Zones
2. IAM
3. Networking — VPC, Subnets, Security Groups, NAT, Endpoints
4. Compute — EC2, Auto Scaling, Lambda
5. Containers — ECR, ECS, Fargate, EKS
6. Load Balancing & API Gateway
7. Storage — S3, EBS, EFS
8. Databases — RDS, Aurora, DynamoDB
9. Caching & Messaging — ElastiCache, MSK, SQS, SNS, EventBridge
10. Security — KMS, Secrets Manager, Parameter Store, ACM, WAF, Cognito
11. Observability — CloudWatch, X-Ray, CloudTrail
12. DevOps — CodePipeline, CloudFormation/CDK/Terraform, Route 53, CloudFront

**Part B — Scenario-Based Questions (Our Stack)**
13. Scenarios — Deploying .NET APIs on AWS
14. Scenarios — Nginx on RHEL EC2 (Reverse Proxy, LB, Gateway)
15. Scenarios — Networking & Connectivity
16. Scenarios — IAM & Permissions
17. Scenarios — Load Balancers, API Gateway & Route 53
18. Scenarios — Auto Scaling & Performance
19. Scenarios — Containers on ECS/EKS
20. Scenarios — Microservices on AWS
21. Scenarios — Kafka on Amazon MSK
22. Scenarios — Redis on ElastiCache
23. Scenarios — RDS: SQL Server, MySQL, PostgreSQL, Oracle
24. Scenarios — YugabyteDB on AWS
25. Scenarios — S3, Files & Bulk Data
26. Scenarios — Authentication & Authorization (JWT, Cognito, OAuth)
27. Scenarios — Secrets, Configuration & Encryption
28. Scenarios — Serverless (Lambda, SQS, SNS, EventBridge)
29. Scenarios — Observability, Logging & Troubleshooting
30. Scenarios — CI/CD & Deployments
31. Scenarios — High Availability, Backup & Disaster Recovery
32. Scenarios — Security & Compliance (Financial Domain) 💰
33. Scenarios — Cost Optimization
34. Scenarios — Migration to AWS

**Part C — Practice**
35. Tricky Questions
36. Mini System Design on AWS
37. Hands-On Tasks
38. Rapid-Fire Round

---

# Part A — Core Concepts (Quick Check)

## 1. AWS Basics, Regions & Availability Zones

1. 🟢 What is AWS? What is cloud computing?
2. 🟢 What are IaaS, PaaS and SaaS? Give AWS examples of each.
3. 🟢 What is a Region? What is an Availability Zone? What is an edge location?
4. 🟢 Why should production workloads be deployed across multiple AZs?
5. 🟢 What is the AWS shared responsibility model?
6. 🟡 How do you choose a region (latency, cost, compliance, service availability)? Which regions are in India (Mumbai `ap-south-1`, Hyderabad `ap-south-2`)? 💰
7. 🟡 What is the AWS Well-Architected Framework? Name its pillars.
8. 🟢 What are the ways to interact with AWS (Console, CLI, SDK, IaC)?

---

## 2. IAM

9. 🟢 What is IAM? What are users, groups, roles and policies?
10. 🟢 Why shouldn't you use the root account for daily work?
11. 🟡 What is the difference between an IAM user and an IAM role?
12. 🟡 What is an IAM policy? What are identity-based vs resource-based policies?
13. 🟡 How is a policy evaluated (explicit deny, allow, implicit deny)?
14. 🟡 What is the principle of least privilege in IAM?
15. 🟡 What is an instance profile / EC2 IAM role? Why is it better than storing access keys on the server?
16. 🟡 What are ECS task roles and EKS IRSA / Pod Identity?
17. 🟡 What is `AssumeRole` and STS?
18. 🟡 What is MFA and why enable it?
19. 🔴 What are permission boundaries and Service Control Policies (SCPs)?

---

## 3. Networking — VPC, Subnets, Security Groups, NAT, Endpoints

20. 🟢 What is a VPC?
21. 🟢 What are public and private subnets? What makes a subnet "public"?
22. 🟢 What is an Internet Gateway? What is a NAT Gateway?
23. 🟢 What are route tables?
24. 🟢 What are security groups? What are network ACLs? What are the differences (stateful vs stateless, allow vs allow/deny)?
25. 🟡 What is a VPC endpoint (gateway vs interface / PrivateLink)?
26. 🟡 What is VPC peering vs Transit Gateway?
27. 🟡 What is a bastion host vs AWS Systems Manager Session Manager?
28. 🟡 What is an Elastic IP?
29. 🟡 What are VPC Flow Logs?
30. 🟡 What are Site-to-Site VPN and Direct Connect? 💰

---

## 4. Compute — EC2, Auto Scaling, Lambda

31. 🟢 What is EC2? What are instance types (general purpose, compute, memory optimized)?
32. 🟢 What is an AMI?
33. 🟡 What are On-Demand, Reserved, Savings Plans and Spot instances?
34. 🟡 What is user data in EC2?
35. 🟡 What is an Auto Scaling Group? What are launch templates?
36. 🟡 What scaling policies exist (target tracking, step, scheduled)?
37. 🟡 What are EC2 health checks vs ELB health checks in an ASG?
38. 🟢 What is AWS Lambda? What are its limits (timeout, memory, package size)?
39. 🟡 What is a Lambda cold start? How does it affect .NET Lambdas (Native AOT, SnapStart)?
40. 🟡 When would you choose Lambda over EC2 or containers?

---

## 5. Containers — ECR, ECS, Fargate, EKS

41. 🟢 What is ECR?
42. 🟢 What is ECS? What are clusters, task definitions, tasks and services?
43. 🟡 What is Fargate? EC2 launch type vs Fargate?
44. 🟡 What is EKS? ECS vs EKS — when to use which?
45. 🟡 How do ECS services integrate with an ALB?
46. 🟡 How do you pass environment variables and secrets to ECS tasks?
47. 🟡 What is App Runner? When is it a simpler choice?

---

## 6. Load Balancing & API Gateway

48. 🟢 What is Elastic Load Balancing? What are ALB, NLB and GWLB?
49. 🟡 ALB vs NLB — when to use each?
50. 🟡 What are target groups and health checks?
51. 🟡 What are listener rules (path-based, host-based routing)?
52. 🟡 What is cross-zone load balancing?
53. 🟡 What is connection draining / deregistration delay?
54. 🟡 What is the ALB idle timeout (default 60s)?
55. 🟢 What is Amazon API Gateway? REST API vs HTTP API vs WebSocket API?
56. 🟡 API Gateway vs ALB vs Nginx as an API gateway — when do you choose each?

---

## 7. Storage — S3, EBS, EFS

57. 🟢 What is S3? What are buckets and objects?
58. 🟢 What are S3 storage classes (Standard, Intelligent-Tiering, Standard-IA, Glacier)?
59. 🟡 What are S3 lifecycle policies?
60. 🟡 What is S3 versioning? What is Object Lock? 💰
61. 🟡 What are pre-signed URLs?
62. 🟡 How do you block public access and secure buckets (bucket policies, Block Public Access, encryption)?
63. 🟢 What is EBS? What are gp3, io2 volume types?
64. 🟢 What is EFS? EBS vs EFS vs S3?
65. 🟡 What are EBS snapshots?

---

## 8. Databases — RDS, Aurora, DynamoDB

66. 🟢 What is Amazon RDS? Which engines does it support (SQL Server, MySQL, PostgreSQL, Oracle, MariaDB, Db2)?
67. 🟢 What is Multi-AZ in RDS? What is a read replica? What's the difference?
68. 🟡 What is Aurora? How is it different from RDS MySQL/PostgreSQL?
69. 🟡 What is Aurora Serverless v2?
70. 🟡 What are automated backups, manual snapshots and point-in-time recovery?
71. 🟡 What is RDS Proxy? Why use it (connection pooling, Lambda, failover)?
72. 🟡 What is a parameter group? What is an option group?
73. 🟡 What are RDS licensing options for SQL Server and Oracle (License Included vs BYOL)?
74. 🟡 What is Performance Insights?
75. 🟢 What is DynamoDB? When would you use it instead of RDS?
76. 🟡 RDS vs self-managed database on EC2 — trade-offs?

---

## 9. Caching & Messaging — ElastiCache, MSK, SQS, SNS, EventBridge

77. 🟢 What is ElastiCache? Redis/Valkey vs Memcached?
78. 🟡 What is cluster mode in ElastiCache Redis?
79. 🟢 What is Amazon MSK?
80. 🟡 MSK provisioned vs MSK Serverless?
81. 🟢 What is SQS? Standard vs FIFO queues?
82. 🟡 What is visibility timeout? What is a dead-letter queue in SQS?
83. 🟢 What is SNS? What is SNS + SQS fan-out?
84. 🟡 What is EventBridge? EventBridge vs SNS vs SQS vs Kafka?
85. 🟡 What is Amazon MQ (managed RabbitMQ/ActiveMQ)?

---

## 10. Security — KMS, Secrets Manager, Parameter Store, ACM, WAF, Cognito

86. 🟢 What is KMS? What are customer managed keys vs AWS managed keys?
87. 🟢 What is Secrets Manager? What is SSM Parameter Store? Differences?
88. 🟡 What is automatic secret rotation?
89. 🟢 What is ACM (AWS Certificate Manager)? Can ACM certificates be installed on EC2 Nginx directly?
90. 🟡 What is AWS WAF? What is AWS Shield?
91. 🟡 What is Amazon Cognito? User pools vs identity pools?
92. 🟡 What are GuardDuty, Security Hub, Inspector and Macie?

---

## 11. Observability — CloudWatch, X-Ray, CloudTrail

93. 🟢 What is CloudWatch? What are metrics, logs and alarms?
94. 🟡 What is the CloudWatch agent? Why is it needed for memory and disk metrics on EC2?
95. 🟡 What is CloudWatch Logs Insights?
96. 🟡 What is AWS X-Ray? How does it compare with OpenTelemetry (ADOT)?
97. 🟢 What is CloudTrail? CloudTrail vs CloudWatch?
98. 🟡 What is AWS Config?

---

## 12. DevOps — CodePipeline, CloudFormation/CDK/Terraform, Route 53, CloudFront

99. 🟢 What are CodeCommit, CodeBuild, CodeDeploy and CodePipeline?
100. 🟡 What is Infrastructure as Code? CloudFormation vs CDK vs Terraform?
101. 🟢 What is Route 53? What routing policies exist (simple, weighted, latency, failover, geolocation)?
102. 🟡 What is a Route 53 alias record?
103. 🟢 What is CloudFront? How does it work with S3 and ALB origins?
104. 🟡 What is Origin Access Control (OAC) for S3?
105. 🟡 What is Elastic Beanstalk? When would you use it for .NET?

---

# Part B — Scenario-Based Questions (Our Stack)

## 13. Scenarios — Deploying .NET APIs on AWS

106. 🟡 You have an ASP.NET Core Web API. Walk through deploying it on AWS: EC2 + Nginx on RHEL, ECS Fargate, Elastic Beanstalk, Lambda. Which do you choose and why?
107. 🟡 Your .NET API runs on one EC2 instance. Management wants it highly available. What changes do you make?
108. 🟡 Your API reads the connection string from `appsettings.Production.json` committed in Git. How do you move it to AWS securely?
109. 🟡 Your .NET app on EC2 needs to read from S3 and Secrets Manager. How do you give it access without storing access keys?
110. 🟡 After deploying behind an ALB, your ASP.NET Core app generates `http://` redirect URLs and logs the ALB's IP instead of the client IP. How do you fix it?
111. 🟡 Your MVC application uses in-memory sessions. Users get logged out when the ALB sends them to another instance. What are your options?
112. 🟡 Your app uses ASP.NET Core Data Protection (cookies, antiforgery). After scaling to 3 instances, users get "antiforgery token could not be decrypted" errors. Why, and how do you fix it on AWS?
113. 🟡 Your .NET API on AWS calls an external partner API and gets timeouts only in production. What do you check (NAT Gateway, security groups, NACLs, DNS, proxy)?
114. 🟡 Your .NET Lambda function has a 3–4 second cold start. How do you reduce it?
115. 🔴 You need to run a background job (e.g., nightly report) for your .NET app on AWS. Compare: hosted service on EC2, ECS scheduled task, Lambda + EventBridge Scheduler, AWS Batch.

---

## 14. Scenarios — Nginx on RHEL EC2 (Reverse Proxy, LB, Gateway)

116. 🟡 You run Nginx on RHEL EC2 as a reverse proxy to Kestrel. After launch, you get 502 Bad Gateway. What do you check (SELinux boolean, Kestrel binding, systemd service, security group)?
117. 🟡 Nginx on RHEL EC2 is your API gateway for 5 microservices. Should you keep Nginx, or move to ALB / API Gateway? What are the trade-offs?
118. 🟡 You want to keep Nginx but also put an ALB in front. What does each layer do? Is it redundant?
119. 🟡 Nginx is a single EC2 instance acting as load balancer. It becomes a single point of failure. How do you make it highly available on AWS?
120. 🟡 You want HTTPS. Do you use ACM on the ALB, or install certificates on Nginx? What about end-to-end encryption to the backend? 💰
121. 🟡 Nginx upstreams point to private IPs of EC2 instances. When the ASG replaces an instance, Nginx sends traffic to a dead IP. How do you fix it?
122. 🟡 Large file uploads fail with 413 through Nginx on EC2, and with timeouts through the ALB. What settings do you change at each layer?
123. 🟡 SignalR / WebSocket connections drop every 60 seconds behind ALB + Nginx. What timeouts do you check?
124. 🟡 How do you collect Nginx access and error logs from RHEL EC2 into CloudWatch?
125. 🟡 Nginx rate limiting works per instance, but you have 3 Nginx instances. Users get 3x the allowed limit. How do you fix it?
126. 🔴 You need to patch RHEL on Nginx and app servers monthly without downtime. How do you do it on AWS (ASG instance refresh, SSM Patch Manager, golden AMIs)?

---

## 15. Scenarios — Networking & Connectivity

127. 🟢 Design a VPC for a three-tier app: public subnet (ALB/Nginx), private app subnet (.NET services), private DB subnet (RDS, YugabyteDB, MSK, ElastiCache) across 2–3 AZs.
128. 🟡 Your EC2 instance in a private subnet can't download packages with `dnf`. What is missing?
129. 🟡 Your .NET API can't connect to RDS. Walk through troubleshooting (security groups, subnets, route tables, NACLs, DNS endpoint, credentials, SSL).
130. 🟡 Your app connects to RDS by IP instead of endpoint. After a Multi-AZ failover, it stops working. Why?
131. 🟡 Security groups: the app SG needs to reach the DB SG on port 5432. How do you configure it without opening to `0.0.0.0/0`?
132. 🟡 Your NAT Gateway bill is very high because services download large files from S3. How do you reduce it (S3 gateway endpoint)?
133. 🟡 Developers need to SSH into private EC2 instances. Bastion host or SSM Session Manager? Why? 💰
134. 🟡 Your services in two VPCs need to talk to each other. Peering or Transit Gateway?
135. 🟡 An on-premise Oracle database must be reachable from AWS services. What connectivity options exist? 💰
136. 🔴 Outbound calls from many ECS tasks start failing under heavy load through the NAT Gateway. What could cause it (port allocation, connection limits)?

---

## 16. Scenarios — IAM & Permissions

137. 🟡 Your application fails with `AccessDenied` when uploading to S3. How do you debug it (IAM role policy, bucket policy, KMS key policy, explicit deny)?
138. 🟡 A developer accidentally committed AWS access keys to GitHub. What do you do immediately?
139. 🟡 You need different permissions for dev, staging and production. How do you structure accounts and roles?
140. 🟡 An ECS task needs to read only one secret from Secrets Manager. Write the least-privilege approach (task role, resource ARN).
141. 🟡 Your CI/CD pipeline needs to deploy to AWS. How do you authenticate without long-lived keys (OIDC federation from GitHub/GitLab/Azure DevOps)?
142. 🟡 An EKS pod needs to access MSK and S3. How do you give it permissions (IRSA / Pod Identity)?
143. 🔴 Your security team wants to ensure nobody can create public S3 buckets or disable CloudTrail in any account. How?

---

## 17. Scenarios — Load Balancers, API Gateway & Route 53

144. 🟡 Your ALB health check keeps marking healthy instances as unhealthy. What do you check (path, port, status code, timeout, security group, startup time)?
145. 🟡 You need `/api/orders/*` to go to the orders service and `/api/payments/*` to the payments service. How do you configure it with an ALB? With Nginx?
146. 🟡 Your gRPC service needs to be exposed. ALB or NLB? What configuration is needed?
147. 🟡 A long-running report API takes 90 seconds and fails with 504 via the ALB. How do you fix it properly?
148. 🟡 Partners require a fixed IP address to whitelist your API. ALB IPs change. What do you do (NLB with Elastic IPs, Global Accelerator)? 💰
149. 🟡 You want to route 10% of traffic to a new version of your API. How do you do it (ALB weighted target groups, Route 53 weighted, Nginx `split_clients`)?
150. 🟡 You need to expose an API to external partners with API keys, usage plans and throttling. API Gateway or Nginx?
151. 🟡 After changing a Route 53 record, some users still hit the old server. Why?
152. 🔴 How do you set up active-passive failover between two regions using Route 53 health checks?

---

## 18. Scenarios — Auto Scaling & Performance

153. 🟡 Traffic spikes every day at 10 AM and the API slows down until new instances launch. How do you fix it (scheduled scaling, warm pools, faster AMIs)?
154. 🟡 Your ASG scales on CPU, but your .NET API is slow while CPU is only 30%. What metric should you scale on instead (request count per target, latency, queue depth)?
155. 🟡 New instances join the ALB before the app is ready and users get errors. How do you fix it (health check grace period, readiness endpoint)?
156. 🟡 Scale-in kills instances while they are still processing requests. How do you drain gracefully (deregistration delay, SIGTERM handling, lifecycle hooks)?
157. 🟡 Kafka consumers on ECS can't keep up during peak. How do you autoscale them based on consumer lag?
158. 🟡 Your API's P99 latency is high only during scale-out. Why?
159. 🔴 Your EC2 instances run out of memory occasionally but CloudWatch shows no memory metric. Why, and how do you fix it?

---

## 19. Scenarios — Containers on ECS/EKS

160. 🟡 You need to containerise your .NET API and deploy it. Walk through: Dockerfile → ECR → ECS Fargate service → ALB.
161. 🟡 Your ECS task keeps restarting with exit code 139 / 137. What do these mean and how do you investigate?
162. 🟡 Your ECS service deployment is stuck and never reaches steady state. What do you check?
163. 🟡 Your .NET container listens on port 8080 (.NET 8+), but the task definition maps port 80. What happens?
164. 🟡 How do you inject secrets from Secrets Manager into an ECS task as environment variables?
165. 🟡 Your container images are large and deployments are slow. How do you reduce image size?
166. 🟡 Your team uses Podman locally on RHEL. Can you push images built with Podman to ECR?
167. 🟡 ECS vs EKS: your team runs 15 microservices. Which would you choose for a team with limited Kubernetes experience?
168. 🟡 On EKS, how do you expose services (AWS Load Balancer Controller, Ingress, NGINX Ingress Controller)?
169. 🔴 Pods on EKS can't resolve the RDS endpoint or reach MSK. How do you troubleshoot (CoreDNS, security groups for pods, subnets)?

---

## 20. Scenarios — Microservices on AWS

170. 🟡 Design an AWS deployment for 8 .NET microservices with Nginx/ALB, ECS, RDS, ElastiCache and MSK.
171. 🟡 Service A calls Service B synchronously and B is often slow. How do you make A resilient on AWS (timeouts, retries, circuit breaker, SQS)?
172. 🟡 How do microservices discover each other on ECS (Service Connect, Cloud Map) and on EKS (Kubernetes DNS)?
173. 🟡 Each microservice has its own database. Which AWS database services would you use and why?
174. 🟡 You need a correlation ID across Nginx → ALB → services → Kafka. How do you implement and view it in CloudWatch/X-Ray?
175. 🟡 How do you implement the Transactional Outbox pattern on AWS (RDS outbox table + publisher, or DynamoDB Streams, or Debezium on MSK Connect)?
176. 🟡 Order → Payment → Inventory saga across services. Would you use Kafka events, Step Functions or SQS? Why?
177. 🔴 A breaking change in one service's API broke three others in production. How do you prevent this in AWS deployments (versioning, contract tests, canary)?

---

## 21. Scenarios — Kafka on Amazon MSK

178. 🟡 Should you run Kafka yourself on EC2 or use MSK? What are the trade-offs?
179. 🟡 Your .NET consumer (`Confluent.Kafka`) can't connect to MSK. What do you check (bootstrap brokers, security groups, TLS/IAM auth, client config)?
180. 🟡 How do you authenticate a .NET app to MSK (IAM auth, SASL/SCRAM with Secrets Manager, mTLS)?
181. 🟡 Consumer lag is growing on an MSK topic during business hours. How do you investigate and scale (partitions, consumers, CloudWatch metrics)?
182. 🟡 MSK broker disk is getting full. What do you do (retention, storage auto-scaling, tiered storage)?
183. 🟡 You need CDC from RDS PostgreSQL to Kafka. How do you set it up on AWS (Debezium on MSK Connect)?
184. 🟡 Kafka vs SQS vs EventBridge for your order events — which do you choose and why?
185. 🟡 You need to replay the last 3 days of payment events after a bug fix. How do you do it on MSK? 💰
186. 🔴 A broker in one AZ fails. What happens to producers using `acks=all` and `min.insync.replicas=2` with RF=3?

---

## 22. Scenarios — Redis on ElastiCache

187. 🟡 Your API caches product data in ElastiCache Redis. After a price update, users still see the old price. How do you fix it?
188. 🟡 Your .NET app logs `RedisTimeoutException` against ElastiCache under load. What do you check (thread pool, multiplexer reuse, big keys, instance size, network)?
189. 🟡 You enabled encryption in transit on ElastiCache and the app can't connect. What changed in the connection string?
190. 🟡 ElastiCache memory is full and evictions are high. What do you do?
191. 🟡 You use ElastiCache for ASP.NET Core sessions, Data Protection keys and the SignalR backplane. Is one cluster OK? What are the risks?
192. 🟡 ElastiCache failover happened and your app had errors for 30 seconds. How do you make the app tolerate it?
193. 🟡 Cluster mode enabled vs disabled — which do you choose and how does it affect your code (multi-key operations)?
194. 🔴 Can ElastiCache be reached from your laptop for debugging? How do developers access it safely?

---

## 23. Scenarios — RDS: SQL Server, MySQL, PostgreSQL, Oracle

195. 🟡 You need to move an on-premise SQL Server database to AWS. RDS for SQL Server or SQL Server on EC2? What features might you lose on RDS (SQL Agent limits, CLR, sysadmin)?
196. 🟡 Your Oracle database uses packages and `SYS_REFCURSOR` procedures. Will it work on RDS for Oracle? What about migrating it to Aurora PostgreSQL? 💰
197. 🟡 Your PostgreSQL functions use refcursors and JSONB. Will they work on RDS PostgreSQL and Aurora PostgreSQL? What do you test?
198. 🟡 Your .NET app opens too many connections to RDS PostgreSQL and hits `max_connections`. What do you do (pool settings, RDS Proxy, PgBouncer)?
199. 🟡 A bulk insert of 50,000 rows using SQL Server TVPs is slower on RDS than on-prem. What could be different (instance class, storage IOPS, network latency)?
200. 🟡 You need to load lakhs of rows from Excel/CSV into RDS MySQL. `LOAD DATA LOCAL INFILE` fails. What do you check (parameter group `local_infile`, client setting)?
201. 🟡 You need to run `COPY` from a CSV in S3 into RDS PostgreSQL. How (`aws_s3` extension)?
202. 🟡 Read-heavy reporting queries slow down the primary RDS instance. What do you do?
203. 🟡 Users see stale data right after saving because reads go to a read replica. How do you fix it?
204. 🟡 Multi-AZ failover took 60–120 seconds and the app failed during that time. How do you reduce impact (RDS Proxy, retry logic, DNS TTL)?
205. 🟡 Someone ran a wrong `UPDATE` without a `WHERE` clause on production RDS 20 minutes ago. How do you recover? 💰
206. 🟡 You need to give a developer read-only access to production data for debugging. How do you do it safely? 💰
207. 🟡 RDS storage is almost full. What happens and what do you do (storage autoscaling)?
208. 🟡 A slow query appeared after a release. How do you find it on RDS (Performance Insights, slow query log, `pg_stat_statements`, Query Store)?
209. 🔴 You need to upgrade RDS PostgreSQL major version with minimal downtime. How (blue/green deployments for RDS)?
210. 🔴 Oracle/SQL Server licensing on AWS is expensive. What options do you consider?

---

## 24. Scenarios — YugabyteDB on AWS

211. 🟡 YugabyteDB is not an AWS-managed service. What options do you have to run it on AWS (self-managed on EC2, on EKS with Helm, YugabyteDB Aeon on AWS)?
212. 🟡 How would you lay out a 3-node YugabyteDB cluster across 3 AZs? What replication factor would you use?
213. 🟡 Which EC2 instance types and EBS volumes would you consider for YugabyteDB (CPU, memory, gp3/io2, IOPS)?
214. 🟡 Which security group ports must be opened between YugabyteDB nodes and from the app (5433 YSQL, 7100/7000 master, 9100/9000 tserver)?
215. 🟡 Your .NET app should use the YugabyteDB smart driver or Npgsql. How do you configure load balancing across nodes in different AZs?
216. 🟡 One AZ goes down. What happens to your YugabyteDB cluster and your app?
217. 🟡 How do you back up YugabyteDB on AWS to S3 and restore it?
218. 🔴 YugabyteDB vs Aurora PostgreSQL vs RDS PostgreSQL for a high-scale payments system — trade-offs? 💰

---

## 25. Scenarios — S3, Files & Bulk Data

219. 🟡 Users upload KYC documents (PDF/images). Design the upload flow using S3 pre-signed URLs from your .NET API. 💰
220. 🟡 Uploaded files must be scanned for viruses before use. How do you design it (S3 event → Lambda/ECS scanner → move to clean bucket)?
221. 🟡 Your API proxies large file downloads from S3 and consumes a lot of memory. How do you fix it?
222. 🟡 Business users upload Excel files with 5 lakh rows. Design the processing on AWS (S3 → SQS/EventBridge → ECS/Lambda worker → RDS bulk load).
223. 🟡 A file processing Lambda times out at 15 minutes for very large files. What are alternatives?
224. 🟡 You must retain bank statements for 7–10 years cheaply and immutably. How do you configure S3? 💰
225. 🟡 Someone deleted important files from S3. How could you have prevented or recovered from it (versioning, MFA delete, Object Lock, replication)?
226. 🟡 S3 bucket is accidentally public. How do you detect and prevent this?
227. 🟡 You need to serve static files (Angular/React SPA) globally with low latency. How (S3 + CloudFront + OAC)?
228. 🔴 You need to share files securely with an external partner bank daily. Options (pre-signed URLs, Transfer Family SFTP, cross-account bucket access)? 💰

---

## 26. Scenarios — Authentication & Authorization (JWT, Cognito, OAuth)

229. 🟡 Your .NET APIs use JWT issued by your own auth service. Where should the signing key be stored on AWS (Secrets Manager / KMS)?
230. 🟡 Would you use Cognito, an external IdP (Entra ID/Okta/Keycloak) or your own auth service? What are the trade-offs?
231. 🟡 How do you validate Cognito JWTs in ASP.NET Core (`AddJwtBearer` with Cognito authority)?
232. 🟡 Should JWT validation happen at Nginx/API Gateway, in each microservice, or both?
233. 🟡 How does API Gateway validate JWTs (JWT authorizer, Lambda authorizer, Cognito authorizer)?
234. 🟡 Services need to call each other securely on AWS. Options (client credentials, IAM SigV4, mTLS, private networking)?
235. 🟡 You need SSO for internal employees into an admin portal hosted on AWS. How (Cognito federation with Entra ID, ALB OIDC authentication)?
236. 🟡 Your login endpoint is being brute-forced. What AWS services help (WAF rate-based rules, Shield, Cognito advanced security)?
237. 🔴 You need to rotate the JWT signing key without logging everyone out. How (JWKS with `kid`, multiple active keys)?

---

## 27. Scenarios — Secrets, Configuration & Encryption

238. 🟡 Your .NET app needs database passwords, Kafka credentials and API keys. Where do you store each (Secrets Manager vs Parameter Store) and how do you load them into `IConfiguration`?
239. 🟡 RDS password rotation is enabled in Secrets Manager. Your app starts failing after rotation. Why, and how do you handle it?
240. 🟡 You need different config values per environment without rebuilding the image. How?
241. 🟡 You must encrypt RDS, S3, EBS, ElastiCache and MSK data at rest. How (KMS keys)? 💰
242. 🟡 You must encrypt sensitive columns (PAN, account number) at the application level. How do you use KMS (envelope encryption)? 💰
243. 🟡 How do you install and renew TLS certificates on Nginx running on EC2 (ACM can't export public certs to EC2 — what are the options)?
244. 🔴 Your app calls KMS for every request and hits throttling. How do you fix it (data key caching)?

---

## 28. Scenarios — Serverless (Lambda, SQS, SNS, EventBridge)

245. 🟡 You need to send email/SMS notifications after an order is placed without slowing down the API. Design it with SQS/SNS/Lambda.
246. 🟡 An SQS consumer processes the same message twice. Why, and how do you make it idempotent?
247. 🟡 Messages keep failing and reappear in the queue forever. How do you handle poison messages (DLQ, `maxReceiveCount`)?
248. 🟡 You need strict ordering of messages per account. Standard SQS or FIFO? What are FIFO limits (message group ID)? 💰
249. 🟡 Your Lambda connects to RDS and exhausts connections during a spike. How do you fix it (RDS Proxy, reserved concurrency)?
250. 🟡 You need a cron job that runs every night at 1 AM. How do you do it on AWS (EventBridge Scheduler + Lambda/ECS task)?
251. 🟡 A Lambda inside a VPC can't reach the internet or AWS APIs. Why, and how do you fix it?
252. 🟡 You need a multi-step workflow with retries and human approval (loan approval). Would you use Step Functions? Why? 💰

---

## 29. Scenarios — Observability, Logging & Troubleshooting

253. 🟡 How do you send structured JSON logs from your .NET app (Serilog) on EC2/ECS to CloudWatch Logs?
254. 🟡 How do you search all logs for one correlation ID across services (CloudWatch Logs Insights query)?
255. 🟡 Your API returns 5xx errors intermittently. Walk through investigation: ALB metrics → target health → app logs → DB metrics → traces.
256. 🟡 How do you add distributed tracing with OpenTelemetry/ADOT or X-Ray to .NET services on ECS?
257. 🟡 What CloudWatch alarms would you set for an API (5xx rate, latency P99, unhealthy hosts, CPU, memory, DB connections, consumer lag)?
258. 🟡 CloudWatch Logs cost is very high. How do you reduce it (log levels, retention, sampling, archiving to S3)?
259. 🟡 Someone changed a security group and production broke. How do you find who did it (CloudTrail, AWS Config)?
260. 🟡 Your app's memory grows steadily on ECS until the task is killed. How do you diagnose a .NET memory leak in a container?
261. 🔴 How do you build a dashboard showing the health of all microservices, Kafka, Redis and databases?

---

## 30. Scenarios — CI/CD & Deployments

262. 🟡 Design a CI/CD pipeline for a .NET microservice: build, test, scan, push to ECR, deploy to ECS (CodePipeline, GitHub Actions or Azure DevOps).
263. 🟡 How do you deploy a new version to EC2 instances behind Nginx/ALB with zero downtime (rolling, blue/green with CodeDeploy, ASG instance refresh)?
264. 🟡 How do you implement blue/green deployment for ECS services?
265. 🟡 A deployment introduced a bug. How do you roll back quickly on ECS / EC2?
266. 🟡 Your release includes a database migration. How do you deploy safely without breaking the old version (expand/contract)?
267. 🟡 How do you manage infrastructure for dev/staging/prod consistently (Terraform/CloudFormation/CDK with environments)?
268. 🟡 Your pipeline needs to run integration tests against PostgreSQL, Redis and Kafka. How do you do it in CI (Testcontainers, Docker in CodeBuild)?
269. 🔴 How do you scan container images and dependencies for vulnerabilities before deployment (ECR scanning, Inspector)?

---

## 31. Scenarios — High Availability, Backup & Disaster Recovery

270. 🟡 What happens to your system if one Availability Zone goes down? Walk through each component (Nginx/ALB, ECS/EC2, RDS, ElastiCache, MSK, YugabyteDB).
271. 🟡 How do you back up RDS, EBS, S3, ElastiCache and MSK data? What is AWS Backup?
272. 🟡 Your business requires RPO of 5 minutes and RTO of 1 hour. Which DR strategy do you choose (backup & restore, pilot light, warm standby, active-active)? 💰
273. 🟡 How do you test that your backups can actually be restored?
274. 🟡 The whole Mumbai region has an outage. What is your plan (cross-region replicas, Route 53 failover, Hyderabad region)? 💰
275. 🔴 How do you keep Kafka (MSK) data available in a DR region (MSK Replicator, MirrorMaker 2)?

---

## 32. Scenarios — Security & Compliance (Financial Domain) 💰

276. 🟡💰 Your banking API must not be directly reachable from the internet except through a WAF and load balancer. Design it.
277. 🟡💰 All traffic between services and databases must be encrypted. How do you enforce TLS for RDS, ElastiCache, MSK and internal APIs?
278. 🟡💰 Customer data must stay in India. How do you enforce it on AWS (region restrictions via SCPs, replication settings)?
279. 🟡💰 Auditors want logs of every API call made to AWS and every admin login for 7 years. How?
280. 🟡💰 You need to meet PCI-DSS for card data. Which AWS services and patterns help (segmentation, KMS, tokenisation, CloudTrail, Config, Security Hub)?
281. 🟡💰 How do you protect your public APIs from SQL injection, XSS and bots (WAF managed rules)?
282. 🟡💰 A partner bank requires mTLS and IP whitelisting for API calls. How do you implement it (API Gateway mTLS, NLB + Nginx mTLS, Elastic IPs)?
283. 🔴💰 GuardDuty reports an EC2 instance communicating with a known malicious IP. What are your immediate actions?

---

## 33. Scenarios — Cost Optimization

284. 🟡 Your monthly AWS bill doubled. How do you find out why (Cost Explorer, cost allocation tags, Budgets)?
285. 🟡 Dev and test environments run 24x7. How do you reduce cost (scheduled stop/start, smaller instances, Spot)?
286. 🟡 EC2 instances are underutilised at 10% CPU. What do you do (right-sizing, Compute Optimizer, Graviton)?
287. 🟡 Can your .NET app run on Graviton (ARM64) instances? What do you need to check?
288. 🟡 NAT Gateway and data transfer costs are high. How do you reduce them (VPC endpoints, same-AZ traffic)?
289. 🟡 RDS costs are high. What options exist (Reserved Instances, right-sizing, Aurora Serverless v2 for spiky loads, storage type)?
290. 🟡 S3 costs keep growing. How do you reduce them (lifecycle rules, Intelligent-Tiering)?
291. 🔴 When should you use Savings Plans vs Reserved Instances vs Spot?

---

## 34. Scenarios — Migration to AWS

292. 🟡 Your company runs .NET apps on IIS (Windows) and Nginx (RHEL) on-premise. How do you plan migration to AWS (rehost, replatform, refactor)?
293. 🟡 What are the "7 Rs" of migration?
294. 🟡 How do you migrate an on-premise SQL Server / Oracle / MySQL / PostgreSQL database to RDS with minimal downtime (DMS, native backup/restore, CDC)?
295. 🟡 How do you migrate a self-managed Kafka cluster to MSK (MirrorMaker 2, MSK Replicator)?
296. 🟡 How do you migrate Redis to ElastiCache?
297. 🟡 How do you migrate large files (terabytes) from on-premise to S3 (DataSync, Snowball, S3 multipart)?
298. 🟡 What changes are needed in a .NET app moving from IIS on Windows to containers on Linux (paths, case sensitivity, Windows auth, config, logging)?
299. 🔴 How do you run on-premise and AWS in parallel during migration (hybrid connectivity, Route 53 weighted routing, data sync)?

---

# Part C — Practice

## 35. Tricky Questions

300. 🟡 Is a security group stateful or stateless? What does that mean for return traffic?
301. 🟡 Can a security group deny traffic?
302. 🟡 If you deny traffic in a NACL but allow it in a security group, what happens?
303. 🟡 Is an RDS read replica a backup? Is Multi-AZ a backup?
304. 🟡 Does Multi-AZ RDS improve read performance?
305. 🟡 Is data in an EC2 instance store kept after stopping the instance?
306. 🟡 What happens to the public IP of an EC2 instance when you stop and start it?
307. 🟡 Can you attach one EBS volume to multiple instances?
308. 🟡 Is S3 a file system? Can you "append" to an S3 object?
309. 🟡 Why does an EC2 instance in a "public subnet" still have no internet access?
310. 🟡 Why can't an EC2 instance in a private subnet reach S3 even with an IAM role?
311. 🟡 Why do IAM changes sometimes take a few seconds to apply?
312. 🟡 Why does CloudWatch not show memory usage of EC2 by default?
313. 🟡 Can an ALB have a static IP?
314. 🟡 Why can't a Lambda function hold a long-lived WebSocket connection?
315. 🟡 Is SQS FIFO always better than SQS Standard?
316. 🟡 Can you use ACM certificates directly on Nginx running on EC2?
317. 🟡 Is MSK fully serverless? What do you still manage?
318. 🟡 Is ElastiCache accessible from outside the VPC?
319. 🟡 Does RDS give you OS-level access to the database server?
320. 🔴 Why can cross-AZ traffic increase your bill?
321. 🔴 Why can storing access keys in environment variables of an EC2 instance be a bad practice even if the server is private?

---

## 36. Mini System Design on AWS

322. 🟡 Design a highly available .NET Web API on AWS with Nginx, ALB, ECS/EC2, RDS PostgreSQL and ElastiCache.
323. 🟡 Design an event-driven order processing system on AWS with .NET services and MSK.
324. 🟡 Design a file upload and processing system (Excel upload → validation → bulk insert into RDS).
325. 🟡 Design a notification service using SQS, SNS and Lambda.
326. 🔴 Design a payment processing backend on AWS with idempotency, Kafka, RDS and audit logs. 💰
327. 🔴 Design a multi-region active-passive setup for a banking API. 💰
328. 🔴 Design the deployment of YugabyteDB alongside .NET microservices on EKS across 3 AZs.

---

## 37. Hands-On Tasks

329. 🟢 Create a VPC with public and private subnets in 2 AZs, an Internet Gateway and a NAT Gateway.
330. 🟢 Launch a RHEL EC2 instance with an IAM role and connect using SSM Session Manager.
331. 🟡 Install Nginx and the ASP.NET Core runtime on RHEL EC2 and deploy a sample API behind Nginx.
332. 🟡 Put the EC2 instances in an Auto Scaling Group behind an ALB with health checks.
333. 🟡 Containerise the .NET API, push it to ECR and run it on ECS Fargate behind an ALB.
334. 🟡 Create an RDS PostgreSQL instance in a private subnet and connect from the API using Secrets Manager.
335. 🟡 Create an ElastiCache Redis cluster and use it for caching via `IDistributedCache`.
336. 🟡 Create an MSK cluster, then produce and consume messages from .NET with IAM authentication.
337. 🟡 Upload files to S3 via pre-signed URLs from the API.
338. 🟡 Send app logs to CloudWatch and write a Logs Insights query to find errors by correlation ID.
339. 🟡 Create CloudWatch alarms for 5xx errors and high latency on the ALB.
340. 🟡 Write a GitHub Actions / CodePipeline workflow that builds, tests, pushes to ECR and deploys to ECS.
341. 🔴 Write Terraform or CDK for the VPC + ALB + ECS + RDS setup.

---

## 38. Rapid-Fire Round

342. 🟢 What is the AWS service for virtual servers?
343. 🟢 What is the AWS service for object storage?
344. 🟢 What is the AWS service for managed relational databases?
345. 🟢 What is the AWS service for managed Kafka?
346. 🟢 What is the AWS service for managed Redis?
347. 🟢 What is the AWS service for container images?
348. 🟢 What is the AWS service for DNS?
349. 🟢 What is the AWS service for CDN?
350. 🟢 What is the AWS service for storing secrets?
351. 🟢 What is the AWS service for encryption keys?
352. 🟢 What is the AWS service for audit logs of API calls?
353. 🟢 What is the AWS service for metrics, logs and alarms?
354. 🟡 Which load balancer works at Layer 7?
355. 🟡 Which load balancer supports static IPs?
356. 🟡 Which subnet type has a route to an Internet Gateway?
357. 🟡 Which gateway lets private subnets reach the internet?
358. 🟡 Which endpoint type is free for S3 and DynamoDB?
359. 🟡 Which RDS feature gives automatic failover?
360. 🟡 Which RDS feature scales reads?
361. 🟡 Which service pools database connections for RDS?
362. 🟡 Which SQS queue type guarantees ordering?
363. 🟡 What is the maximum Lambda timeout?
364. 🟡 What is the default ALB idle timeout?
365. 🟡 Which service lets you access EC2 without SSH keys or a bastion?
366. 🟡 Which service lets you migrate databases with CDC?
367. 🔴 What is the difference between Secrets Manager and Parameter Store in one line?
368. 🔴 What is the difference between ECS and EKS in one line?
369. 🔴 What is the difference between security groups and NACLs in one line?
370. 🔴 What is the difference between Multi-AZ and read replicas in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS (Scenario-Focused).
