# 🎯 Authentication & Authorization Interview Questions — Part 5 (Questions Only)

> **Scope:** Authentication & Authorization concepts, ASP.NET Core authentication, ASP.NET Core authorization (roles, claims, policies, resource-based), ASP.NET Core Identity, cookies & sessions, JWT, OAuth 2.0, OpenID Connect, API keys, certificates, SSO, MFA, security best practices, plus a large set of scenario-based questions, tricky questions and predict-the-behavior snippets.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks, payments, fintech), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.
> **Covers up to ASP.NET Core 10 and OAuth 2.1 / current OAuth best practices.**

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. Authentication & Authorization Fundamentals
2. Authentication Methods & Protocols Overview
3. ASP.NET Core Authentication Basics
4. Cookie Authentication & Sessions
5. ASP.NET Core Identity
6. JWT (JSON Web Token) Fundamentals
7. JWT Signing, Validation & Security
8. JWT in ASP.NET Core
9. Access Tokens, Refresh Tokens & Token Lifecycle
10. OAuth 2.0 Fundamentals
11. OAuth 2.0 Grant Types / Flows
12. OAuth 2.0 Security (PKCE, State, Redirect URIs)
13. OpenID Connect (OIDC)
14. Identity Providers & SSO (Entra ID, Okta, Auth0, Keycloak, Duende)
15. Authorization in ASP.NET Core — Roles & Claims
16. Policy-Based & Resource-Based Authorization
17. Securing Web APIs
18. API Keys, Basic Auth, Certificates & mTLS
19. Multi-Factor Authentication & Passwordless
20. Service-to-Service Authentication
21. Password Storage & Account Security
22. Security Attacks & Mitigations
23. Testing Authentication & Authorization
24. Financial-Domain Security Questions 💰
25. Tricky Questions
26. Predict the Behavior (Code Snippets)
27. Scenario-Based Questions — Authentication
28. Scenario-Based Questions — Authorization
29. Scenario-Based Questions — JWT & Tokens
30. Scenario-Based Questions — OAuth, OIDC & SSO
31. Scenario-Based Questions — Debugging & Production Issues
32. System Design Scenarios
33. Coding & Hands-On Tasks
34. Rapid-Fire Round

---

## 1. Authentication & Authorization Fundamentals

1. 🟢 What is authentication?
2. 🟢 What is authorization?
3. 🟢 What is the difference between authentication and authorization?
4. 🟢 Which happens first — authentication or authorization? Why?
5. 🟢 What is identity? What is a principal?
6. 🟢 What are credentials? Give examples.
7. 🟢 What are authentication factors (something you know, have, are)?
8. 🟢 What is the difference between identification, authentication and authorization?
9. 🟢 What is accounting/auditing in AAA (Authentication, Authorization, Accounting)?
10. 🟢 What is stateful vs stateless authentication?
11. 🟢 What is session-based authentication vs token-based authentication?
12. 🟡 What are the pros and cons of session-based vs token-based authentication?
13. 🟡 What is the principle of least privilege?
14. 🟡 What is defense in depth?
15. 🟡 What is Zero Trust security?
16. 🟡 What are RBAC, ABAC, PBAC and ReBAC? Compare them.
17. 🟡 What is Discretionary vs Mandatory Access Control?
18. 🟡 What is segregation of duties? 💰
19. 🟡 What is federated identity?
20. 🟡 What is delegated authorization?

---

## 2. Authentication Methods & Protocols Overview

21. 🟢 What authentication methods are commonly used in web applications?
22. 🟢 What is Basic Authentication? Why is it considered insecure without HTTPS?
23. 🟢 What is Digest Authentication?
24. 🟢 What is Windows Authentication? What are NTLM and Kerberos?
25. 🟡 How does Kerberos authentication work at a high level?
26. 🟢 What is form-based authentication?
27. 🟢 What is token-based authentication?
28. 🟢 What is an API key? Is it authentication or identification?
29. 🟡 What is certificate-based authentication?
30. 🟡 What is SAML? How is it different from OAuth and OpenID Connect?
31. 🟡 What is WS-Federation?
32. 🟡 What is LDAP? How is it different from Active Directory?
33. 🟡 What is the difference between OAuth 2.0, OpenID Connect and SAML?
34. 🟡 What is OAuth 1.0 vs OAuth 2.0?
35. 🟡 What is OAuth 2.1? What changed compared to OAuth 2.0?
36. 🟡 What is FIDO2 / WebAuthn / Passkeys?
37. 🟡 What is a bearer token?
38. 🟡 What is HMAC-based request signing (e.g., AWS Signature)?

---

## 3. ASP.NET Core Authentication Basics

39. 🟢 How does authentication work in ASP.NET Core?
40. 🟢 What is an authentication scheme?
41. 🟢 What is an authentication handler?
42. 🟢 What do `AddAuthentication()` and `UseAuthentication()` do?
43. 🟢 What is the correct order of `UseRouting`, `UseAuthentication`, `UseAuthorization` and endpoint mapping?
44. 🟡 What happens if `UseAuthorization()` is placed before `UseAuthentication()`?
45. 🟢 What are `ClaimsPrincipal`, `ClaimsIdentity` and `Claim`?
46. 🟢 What is `HttpContext.User`?
47. 🟡 What does `User.Identity.IsAuthenticated` depend on?
48. 🟡 What is the default scheme? What are `DefaultAuthenticateScheme`, `DefaultChallengeScheme`, `DefaultSignInScheme`, `DefaultForbidScheme`?
49. 🟡 What are the authentication actions: Authenticate, Challenge, Forbid, SignIn, SignOut?
50. 🟡 What is the difference between Challenge and Forbid?
51. 🟡 How do you use multiple authentication schemes in one application (cookies + JWT)?
52. 🟡 What is a policy scheme (`AddPolicyScheme`, `ForwardDefaultSelector`)?
53. 🟡 How do you specify the scheme for a specific endpoint (`[Authorize(AuthenticationSchemes = ...)]`)?
54. 🔴 How do you write a custom authentication handler (`AuthenticationHandler<TOptions>`)?
55. 🔴 What is `IClaimsTransformation`? When would you use it?
56. 🟡 What is `HttpContext.SignInAsync` and `SignOutAsync`?
57. 🟡 What are authentication events (`OnTokenValidated`, `OnAuthenticationFailed`, `OnChallenge`, `OnMessageReceived`)?
58. 🟡 How does authentication work in Minimal APIs?
59. 🟡 What is the new simplified authentication configuration in .NET 7+ (default scheme inference, `dotnet user-jwts`)?
60. 🔴 What is `IAuthenticationService` and how is it used internally?

---

## 4. Cookie Authentication & Sessions

61. 🟢 How does cookie-based authentication work?
62. 🟢 How do you configure cookie authentication in ASP.NET Core?
63. 🟡 What is stored in an authentication cookie? How is it protected?
64. 🟡 What is the Data Protection API and how does it relate to cookies?
65. 🟡 What happens to authentication cookies when you run multiple instances without shared data protection keys?
66. 🟡 What are `HttpOnly`, `Secure` and `SameSite` cookie attributes? Why are they important?
67. 🟡 Explain `SameSite=Strict`, `Lax` and `None`.
68. 🟡 What is sliding expiration vs absolute expiration for cookies?
69. 🟡 What are `LoginPath`, `LogoutPath`, `AccessDeniedPath`?
70. 🟡 Why should APIs return 401/403 instead of redirecting to a login page? How do you configure that?
71. 🟡 What is a persistent cookie vs session cookie (`IsPersistent`)?
72. 🟡 How do you invalidate a cookie when a user's password or roles change (`OnValidatePrincipal`, security stamp)?
73. 🟡 What is session state in ASP.NET Core? How is it different from authentication?
74. 🟡 What is session fixation and how do you prevent it?
75. 🔴 What is a server-side ticket store (`ITicketStore`)? Why would you use it?
76. 🔴 What is the cookie size limit and what is chunked cookies?
77. 🔴 What is the Backend-for-Frontend (BFF) pattern and why is it recommended for SPAs?

---

## 5. ASP.NET Core Identity

78. 🟢 What is ASP.NET Core Identity?
79. 🟢 What features does ASP.NET Core Identity provide?
80. 🟢 What are `UserManager<TUser>`, `SignInManager<TUser>` and `RoleManager<TRole>`?
81. 🟡 What are the default Identity tables?
82. 🟡 How do you customize the `IdentityUser` class?
83. 🟡 How does Identity hash passwords? Which algorithm does it use?
84. 🟡 How do you configure password, lockout and user options?
85. 🟡 What is the security stamp and what is it used for?
86. 🟡 What is account lockout? How do you configure it?
87. 🟡 How do you implement email confirmation and password reset tokens?
88. 🟡 How do you implement two-factor authentication with Identity?
89. 🟡 How do you add external logins (Google, Microsoft, Facebook)?
90. 🟡 What are Identity API endpoints (`MapIdentityApi`) in .NET 8? What are their limitations?
91. 🟡 Is ASP.NET Core Identity an identity provider / OAuth server? What is it not?
92. 🔴 How do you use Identity with a custom data store (non-EF)?
93. 🔴 How does passkey support work in ASP.NET Core Identity (.NET 10)?
94. 🟡 What is the difference between ASP.NET Core Identity and Duende IdentityServer / OpenIddict?

---

## 6. JWT (JSON Web Token) Fundamentals

95. 🟢 What is a JWT?
96. 🟢 What is the structure of a JWT (header, payload, signature)?
97. 🟢 What is Base64URL encoding? Is a JWT encrypted?
98. 🟢 What information is stored in the JWT header (`alg`, `typ`, `kid`)?
99. 🟢 What are claims in a JWT?
100. 🟢 What are registered claims (`iss`, `sub`, `aud`, `exp`, `nbf`, `iat`, `jti`)?
101. 🟡 What are public claims and private claims?
102. 🟡 What is the difference between JWS and JWE?
103. 🟡 When would you use an encrypted JWT (JWE)?
104. 🟢 Why shouldn't you store sensitive data (passwords, PAN, account numbers) in a JWT payload? 💰
105. 🟢 What are the advantages of JWT?
106. 🟢 What are the disadvantages of JWT?
107. 🟡 Is JWT a protocol? How is it related to OAuth 2.0?
108. 🟡 What is the difference between a JWT and an opaque token?
109. 🟡 What is a self-contained token vs a reference token?
110. 🟡 How big can a JWT get? What problems do large JWTs cause?
111. 🟡 What is `jti` and how can it be used to prevent replay?
112. 🟡 What is the difference between `exp` and `nbf`?
113. 🟡 What time format do `exp`, `iat` and `nbf` use?
114. 🟡 What are JWT profiles for access tokens (RFC 9068, `typ: at+jwt`)?

---

## 7. JWT Signing, Validation & Security

115. 🟢 How is a JWT signed?
116. 🟢 What is the difference between symmetric (HS256) and asymmetric (RS256, ES256) signing?
117. 🟡 When would you choose HS256 vs RS256?
118. 🟡 What is the minimum key length for HS256?
119. 🟡 What is JWKS (JSON Web Key Set)? What is the `jwks_uri` endpoint?
120. 🟡 What is the `kid` header used for? How does key rotation work?
121. 🟢 How does a server validate a JWT? List all validation steps.
122. 🟡 What is issuer validation? Audience validation? Lifetime validation? Signature validation?
123. 🟡 What is `ClockSkew` and what is its default value in ASP.NET Core?
124. 🔴 What is the `alg: none` attack? How do libraries prevent it?
125. 🔴 What is the algorithm confusion attack (RS256 → HS256)?
126. 🔴 What is the `kid` injection / `jku` / `x5u` header attack?
127. 🔴 What is token sidejacking / token theft? How do you mitigate it?
128. 🔴 What is sender-constrained tokens? Explain DPoP and mTLS-bound tokens.
129. 🔴 What is token replay? How do you prevent it?
130. 🟡 Why can't you "log out" a JWT? What are the options for revocation?
131. 🔴 How do you implement token revocation / a denylist for JWTs? What is the cost?
132. 🟡 What is token introspection (RFC 7662)?
133. 🟡 Where should a JWT be stored in a browser? Compare localStorage, sessionStorage, memory and cookies.
134. 🔴 What are the XSS risks of storing tokens in localStorage?
135. 🔴 What are the CSRF risks of storing tokens in cookies? How do you mitigate them?
136. 🔴 How do you securely store and rotate signing keys (Key Vault, HSM)? 💰

---

## 8. JWT in ASP.NET Core

137. 🟢 How do you configure JWT bearer authentication in ASP.NET Core (`AddJwtBearer`)?
138. 🟢 What are the important `TokenValidationParameters`?
139. 🟡 What do `Authority` and `Audience` do in `JwtBearerOptions`?
140. 🟡 How does `AddJwtBearer` fetch signing keys automatically from the OIDC discovery document?
141. 🟢 How do you generate a JWT in C# (`JwtSecurityTokenHandler` vs `JsonWebTokenHandler`)?
142. 🟡 What is the difference between `System.IdentityModel.Tokens.Jwt` and `Microsoft.IdentityModel.JsonWebTokens`?
143. 🟡 Why did .NET 8 switch the default JWT handler to `JsonWebTokenHandler`? What breaking changes did it cause?
144. 🟡 What is claim type mapping (`MapInboundClaims`, `DefaultInboundClaimTypeMap`)? Why does `sub` become `nameidentifier`?
145. 🟡 How do you configure `NameClaimType` and `RoleClaimType`?
146. 🟡 How do you read claims from the current user in a controller?
147. 🟡 How do you read a JWT from a query string (e.g., SignalR WebSockets) using `OnMessageReceived`?
148. 🟡 How do you customise the 401 response body for an invalid or expired token?
149. 🟡 How do you return `WWW-Authenticate` header details for expired tokens?
150. 🟡 What is `dotnet user-jwts` and how do you use it for local development?
151. 🔴 How do you support multiple issuers / tenants in JWT validation?
152. 🔴 How do you validate tokens from both Azure AD and a custom issuer in the same API?
153. 🔴 How do you implement custom validation logic (e.g., checking a denylist) in `OnTokenValidated`?

---

## 9. Access Tokens, Refresh Tokens & Token Lifecycle

154. 🟢 What is an access token?
155. 🟢 What is a refresh token?
156. 🟢 Why do we need refresh tokens?
157. 🟢 What is the difference between an access token and a refresh token?
158. 🟡 What is a good lifetime for access tokens and refresh tokens? Why?
159. 🟡 Where should refresh tokens be stored on the client and on the server?
160. 🟡 What is refresh token rotation?
161. 🔴 What is refresh token reuse detection? How does it detect theft?
162. 🟡 Should a refresh token be a JWT or an opaque token? Why?
163. 🟡 How do you revoke a refresh token?
164. 🟡 How do you implement logout from all devices?
165. 🟡 What is the difference between sliding and absolute refresh token expiration?
166. 🔴 How do you handle concurrent refresh requests from the same client (race condition)?
167. 🟡 What is an ID token? How is it different from an access token?
168. 🟡 Should an API accept an ID token instead of an access token? Why not?
169. 🟡 What is token exchange (RFC 8693)?
170. 🔴 What is the "on-behalf-of" flow?

---

## 10. OAuth 2.0 Fundamentals

171. 🟢 What is OAuth 2.0?
172. 🟢 What problem does OAuth 2.0 solve?
173. 🟢 Is OAuth 2.0 an authentication protocol or an authorization framework?
174. 🟢 What are the four roles in OAuth 2.0 (resource owner, client, authorization server, resource server)?
175. 🟢 What is a client ID and a client secret?
176. 🟢 What are scopes?
177. 🟡 What is the difference between scopes and roles/permissions?
178. 🟢 What is the authorization endpoint? What is the token endpoint?
179. 🟡 What is a redirect URI (callback URL)? Why must it be pre-registered?
180. 🟡 What is a confidential client vs a public client?
181. 🟡 What is consent in OAuth?
182. 🟡 What is the `state` parameter?
183. 🟡 What is the authorization server metadata / discovery document (`/.well-known/openid-configuration`)?
184. 🟡 What is dynamic client registration?
185. 🟡 What is the difference between OAuth 2.0 and API keys?
186. 🟡 Why is "OAuth for authentication" (pseudo-authentication) considered dangerous?
187. 🟡 What are Pushed Authorization Requests (PAR)?
188. 🟡 What is Rich Authorization Requests (RAR)? 💰
189. 🔴 What is FAPI (Financial-grade API) and why is it used in open banking? 💰

---

## 11. OAuth 2.0 Grant Types / Flows

190. 🟢 What are OAuth 2.0 grant types?
191. 🟢 Explain the Authorization Code flow step by step.
192. 🟡 Explain Authorization Code flow with PKCE step by step.
193. 🟡 What is the Client Credentials flow? When is it used?
194. 🟡 What is the Implicit flow? Why is it deprecated?
195. 🟡 What is the Resource Owner Password Credentials (ROPC) flow? Why is it deprecated?
196. 🟡 What is the Device Authorization (device code) flow? When is it used?
197. 🟡 What is the Refresh Token grant?
198. 🟡 What is the JWT Bearer grant / client assertion (`private_key_jwt`)?
199. 🟡 What is CIBA (Client-Initiated Backchannel Authentication)? 💰
200. 🟡 Which flow would you use for: a SPA, a mobile app, a server-side web app, a background service, a smart TV, a CLI tool?
201. 🔴 Why is the authorization code exchanged on the back channel and not returned as a token directly?
202. 🔴 What is the hybrid flow in OIDC?
203. 🔴 What flows were removed in OAuth 2.1?

---

## 12. OAuth 2.0 Security

204. 🟡 What is PKCE? What problem does it solve?
205. 🟡 What are `code_verifier` and `code_challenge`? What is `S256` vs `plain`?
206. 🟡 Why is PKCE now recommended even for confidential clients?
207. 🟡 What attacks does the `state` parameter prevent?
208. 🟡 What is the `nonce` parameter in OIDC? How is it different from `state`?
209. 🔴 What is an authorization code interception attack?
210. 🔴 What is an open redirect vulnerability in OAuth? Why must redirect URIs be matched exactly?
211. 🔴 What is a mix-up attack? How does the `iss` response parameter help?
212. 🔴 What is token leakage via the Referer header or browser history?
213. 🔴 How do you protect client secrets? Why can't SPAs or mobile apps keep secrets?
214. 🔴 What are the OAuth 2.0 Security Best Current Practice (RFC 9700) recommendations?
215. 🔴 What is consent phishing / illicit consent grant?

---

## 13. OpenID Connect (OIDC)

216. 🟢 What is OpenID Connect?
217. 🟢 How is OpenID Connect related to OAuth 2.0?
218. 🟢 What is an ID token? What claims does it contain?
219. 🟡 What is the `openid` scope? What are the `profile`, `email`, `offline_access` scopes?
220. 🟡 What is the UserInfo endpoint?
221. 🟡 How do you validate an ID token?
222. 🟡 What are `at_hash` and `c_hash`?
223. 🟡 What are `acr` and `amr` claims? How are they used for step-up authentication? 💰
224. 🟡 What is the `prompt` parameter (`login`, `consent`, `none`, `select_account`)?
225. 🟡 What is `max_age` and `auth_time`?
226. 🟡 How do you configure OIDC in ASP.NET Core (`AddOpenIdConnect`)?
227. 🟡 What is `SaveTokens` and `GetTokenAsync("access_token")`?
228. 🟡 What is front-channel logout vs back-channel logout vs RP-initiated logout?
229. 🟡 What is silent authentication / silent refresh? Why does it break with third-party cookie blocking?
230. 🔴 How do you implement single logout (SLO) across multiple applications?

---

## 14. Identity Providers & SSO

231. 🟢 What is an Identity Provider (IdP)?
232. 🟢 What is Single Sign-On (SSO)? How does it work?
233. 🟡 Name popular identity providers (Microsoft Entra ID, Azure AD B2C / Entra External ID, Okta, Auth0, Keycloak, AWS Cognito, Google Identity).
234. 🟡 What are Duende IdentityServer and OpenIddict? When would you host your own authorization server?
235. 🟡 Build vs buy: should you build your own authentication server?
236. 🟡 How do you integrate Microsoft Entra ID with an ASP.NET Core application (`Microsoft.Identity.Web`)?
237. 🟡 What is an app registration in Entra ID? What are app roles vs delegated permissions vs application permissions?
238. 🟡 What is the difference between single-tenant and multi-tenant applications in Entra ID?
239. 🟡 What is MSAL? How is it used in client apps?
240. 🟡 What is the difference between SAML SSO and OIDC SSO?
241. 🟡 What is SCIM? What is user provisioning?
242. 🟡 What is Just-In-Time (JIT) provisioning?
243. 🔴 How do you handle group claims overage in Entra ID tokens?
244. 🔴 How do you implement multi-tenant SaaS authentication where each customer brings their own IdP?

---

## 15. Authorization in ASP.NET Core — Roles & Claims

245. 🟢 How does authorization work in ASP.NET Core?
246. 🟢 What does the `[Authorize]` attribute do?
247. 🟢 What does `[AllowAnonymous]` do? What takes precedence?
248. 🟢 What is role-based authorization? How do you use `[Authorize(Roles = "Admin")]`?
249. 🟡 What does `[Authorize(Roles = "Admin,Manager")]` mean vs two separate `[Authorize(Roles = ...)]` attributes?
250. 🟢 What is claims-based authorization?
251. 🟡 What is the difference between roles and claims?
252. 🟡 How are roles represented inside claims?
253. 🟡 How do you apply authorization globally (fallback policy, `RequireAuthorization()`)?
254. 🟡 What is the difference between `DefaultPolicy` and `FallbackPolicy`?
255. 🟡 How do you authorize Minimal API endpoints (`RequireAuthorization`, `AllowAnonymous`)?
256. 🟡 How do you check roles or claims in code (`User.IsInRole`, `User.HasClaim`)?
257. 🟡 How do you authorize in Razor views (`IAuthorizationService` in views)?
258. 🔴 Why can putting too many roles/permissions in a token become a problem?
259. 🔴 What is permission-based authorization and how would you implement it in ASP.NET Core?

---

## 16. Policy-Based & Resource-Based Authorization

260. 🟢 What is policy-based authorization?
261. 🟡 How do you define a policy (`AddAuthorization(options => options.AddPolicy(...))`)?
262. 🟡 What are `IAuthorizationRequirement` and `AuthorizationHandler<TRequirement>`?
263. 🟡 How do you write a custom requirement and handler (e.g., minimum age, employee of department)?
264. 🟡 What happens when multiple handlers handle the same requirement? (OR logic)
265. 🟡 What happens when a policy has multiple requirements? (AND logic)
266. 🟡 What are `context.Succeed()` and `context.Fail()`? What happens if a handler does neither?
267. 🟡 What is `InvokeHandlersAfterFailure`?
268. 🟡 What is resource-based authorization? Why can't it be done with attributes alone?
269. 🟡 How do you use `IAuthorizationService.AuthorizeAsync(User, resource, policy)`?
270. 🟡 What is operation-based authorization (`OperationAuthorizationRequirement`)?
271. 🔴 What is `IAuthorizationPolicyProvider`? How do you create dynamic policies (e.g., `[HasPermission("orders.read")]`)?
272. 🔴 What is `IAuthorizationMiddlewareResultHandler`? How do you customise 401/403 responses?
273. 🔴 What is `IAuthorizationRequirementData` (.NET 8)?
274. 🔴 How do you implement ABAC (attribute-based access control) in ASP.NET Core?
275. 🔴 How do you implement row-level security / data-level authorization (user sees only their own records)?
276. 🔴 How do external policy engines (OPA, Cedar, OpenFGA) fit with ASP.NET Core authorization?

---

## 17. Securing Web APIs

277. 🟢 How do you secure an ASP.NET Core Web API?
278. 🟢 What is the difference between 401 Unauthorized and 403 Forbidden?
279. 🟡 How do you protect an API with scopes (`RequireScope`, `scp` claim)?
280. 🟡 How do you protect an API with app roles for daemon apps (`roles` claim)?
281. 🟡 How do you secure Swagger/OpenAPI UI with OAuth?
282. 🟡 How do you secure SignalR hubs?
283. 🟡 How do you secure gRPC services?
284. 🟡 How do you secure file downloads (signed URLs / SAS tokens)?
285. 🟡 What is CORS and why is it not a security mechanism for APIs?
286. 🟡 How do you rate-limit per user or per client ID?
287. 🟡 How do you implement IP allowlisting?
288. 🟡 How do you log authentication and authorization events for auditing?
289. 🔴 How do you secure an API that is called by both a SPA and a mobile app?
290. 🔴 What is an API gateway's role in authentication and authorization?
291. 🔴 How do you propagate the user identity from a gateway to downstream APIs?

---

## 18. API Keys, Basic Auth, Certificates & mTLS

292. 🟢 What is API key authentication? How do you implement it in ASP.NET Core?
293. 🟡 Where should API keys be sent (header vs query string)? Why?
294. 🟡 How should API keys be stored on the server (hashed)?
295. 🟡 How do you rotate API keys without downtime?
296. 🟡 What are the limitations of API keys compared to OAuth tokens?
297. 🟡 How do you implement Basic Authentication in ASP.NET Core? When is it acceptable?
298. 🟡 What is certificate authentication in ASP.NET Core (`AddCertificate`)?
299. 🟡 What is mutual TLS (mTLS)? How does it work? 💰
300. 🟡 How do you validate a client certificate (chain, thumbprint, issuer, revocation)?
301. 🔴 How do you handle client certificates behind a load balancer or reverse proxy (certificate forwarding)?
302. 🔴 How do you implement HMAC request signing for webhooks or partner APIs? 💰

---

## 19. Multi-Factor Authentication & Passwordless

303. 🟢 What is MFA / 2FA?
304. 🟢 What are common second factors (SMS OTP, email OTP, TOTP app, push, hardware key, biometrics)?
305. 🟡 Why is SMS OTP considered weak? What is SIM swapping?
306. 🟡 What is TOTP? How does it work (shared secret, time step)?
307. 🟡 What is HOTP?
308. 🟡 What is step-up authentication? Give a banking example. 💰
309. 🟡 What is adaptive / risk-based authentication? 💰
310. 🟡 What is MFA fatigue (push bombing) and how do you prevent it (number matching)?
311. 🟡 What are passkeys? How do they work (public-key cryptography, WebAuthn)?
312. 🟡 Why are passkeys phishing-resistant?
313. 🟡 What is magic link authentication? What are its risks?
314. 🔴 What is Strong Customer Authentication (SCA) under PSD2? 💰
315. 🔴 How do you implement recovery codes and account recovery securely?

---

## 20. Service-to-Service Authentication

316. 🟡 How do two backend services authenticate each other?
317. 🟡 How do you use the client credentials flow for service-to-service calls?
318. 🟡 What are managed identities / workload identities?
319. 🟡 What is workload identity federation (e.g., GitHub Actions → Azure without secrets)?
320. 🟡 How do you cache and reuse access tokens for outgoing calls?
321. 🟡 How do you attach tokens automatically to outgoing `HttpClient` calls (`DelegatingHandler`)?
322. 🔴 How do you propagate the end-user identity through a chain of services (token exchange, on-behalf-of)?
323. 🔴 What is SPIFFE/SPIRE? What is service mesh mTLS?
324. 🔴 How do you avoid storing client secrets in configuration files?

---

## 21. Password Storage & Account Security

325. 🟢 How should passwords be stored? Why not encrypt them?
326. 🟢 What is hashing vs encryption vs encoding?
327. 🟢 What is a salt? Why is it needed?
328. 🟡 What is a pepper?
329. 🟡 Why are MD5 and SHA-256 alone not suitable for password hashing?
330. 🟡 What are PBKDF2, bcrypt, scrypt and Argon2?
331. 🟡 What is key stretching / work factor?
332. 🟡 What are rainbow table attacks?
333. 🟡 What are credential stuffing and brute force attacks? How do you prevent them?
334. 🟡 What is account enumeration? How do you prevent it on login, registration and password reset pages?
335. 🟡 What are modern password policy recommendations (NIST SP 800-63B)?
336. 🟡 How do you check passwords against breached password lists?
337. 🟡 How do you implement a secure "forgot password" flow?
338. 🟡 How should password reset tokens be generated, stored and expired?
339. 🔴 How do you migrate users from an old hashing algorithm to a new one without forcing password resets?
340. 🔴 What is a timing attack? Why use constant-time comparison (`CryptographicOperations.FixedTimeEquals`)?

---

## 22. Security Attacks & Mitigations

341. 🟢 What is XSS? How does it relate to token theft?
342. 🟢 What is CSRF? How does ASP.NET Core protect against it?
343. 🟡 Why do cookie-authenticated APIs need CSRF protection but bearer-token APIs usually don't?
344. 🟡 What is clickjacking? How do you prevent it (`X-Frame-Options`, CSP `frame-ancestors`)?
345. 🟡 What is a man-in-the-middle attack? How do HTTPS and HSTS help?
346. 🟡 What is session hijacking?
347. 🟡 What is privilege escalation (horizontal vs vertical)?
348. 🟡 What is IDOR (Insecure Direct Object Reference)? Give an example. 💰
349. 🟡 What is Broken Object Level Authorization (BOLA) in the OWASP API Top 10?
350. 🟡 What is Broken Function Level Authorization?
351. 🟡 What is mass assignment and how can it lead to privilege escalation (e.g., setting `IsAdmin=true`)?
352. 🟡 What are the OWASP Top 10 and OWASP API Security Top 10 items related to authentication and authorization?
353. 🟡 What is a phishing attack? How do phishing-resistant factors help?
354. 🟡 What is a replay attack? How do nonces and timestamps prevent it?
355. 🟡 What is Content Security Policy (CSP)?
356. 🔴 What is a confused deputy problem?
357. 🔴 What is JWT audience confusion — using a token issued for API A against API B?
358. 🔴 What is a subdomain takeover risk for OAuth redirect URIs?

---

## 23. Testing Authentication & Authorization

359. 🟡 How do you unit test an authorization handler?
360. 🟡 How do you integration test protected endpoints with `WebApplicationFactory`?
361. 🟡 How do you create a fake authentication handler for tests?
362. 🟡 How do you generate test JWTs?
363. 🟡 How do you test that unauthorized users get 401 and forbidden users get 403?
364. 🟡 How do you test resource-based authorization (user A can't access user B's data)?
365. 🔴 How do you do security testing / penetration testing of authentication flows?
366. 🔴 How do you automate checks that every endpoint has an authorization policy?

---

## 24. Financial-Domain Security Questions 💰

367. 🟡💰 Why do banks use short-lived tokens and step-up authentication for transactions?
368. 🟡💰 What is transaction signing / dynamic linking (amount + payee bound to authentication)?
369. 🔴💰 How do you implement step-up authentication before a high-value fund transfer?
370. 🔴💰 How do you implement maker-checker (four-eyes) authorization?
371. 🔴💰 How do you implement transaction limits per role or per user (e.g., clerks up to ₹1 lakh, managers up to ₹10 lakh)?
372. 🔴💰 How do you ensure a user can only access their own accounts (IDOR prevention)?
373. 🔴💰 How do you handle joint accounts and delegated access (power of attorney) in authorization?
374. 🔴💰 How do you secure open banking APIs (FAPI, mTLS, PAR, signed request objects)?
375. 🔴💰 What is consent management in open banking? How do you model consent in tokens?
376. 🔴💰 How do you meet audit requirements for authentication and authorization events (who did what, when)?
377. 🔴💰 How do you protect against session hijacking in internet banking (device binding, IP checks, idle timeout)?
378. 🔴💰 What is the typical idle session timeout for banking apps and why?
379. 🔴💰 How do you implement privileged access management for admins and support staff?
380. 🔴💰 How do you secure webhook callbacks from a payment gateway?
381. 🔴💰 What is PCI-DSS and what does it require for authentication and access control?
382. 🔴💰 How do you implement "break-glass" emergency access?

---

## 25. Tricky Questions

383. 🟡 Is a JWT encrypted? Can anyone read its contents?
384. 🟡 If a JWT is signed, can the user modify the payload? What happens if they do?
385. 🟡 If someone steals a valid JWT, can they use it? For how long?
386. 🟡 Can you revoke a JWT before it expires? How?
387. 🟡 Why does my API return 401 even though I am sending a valid token?
388. 🟡 Why does my API return 403 instead of 401?
389. 🟡 Why does my API return 302 redirect to a login page instead of 401?
390. 🟡 Why is `User.Identity.IsAuthenticated` false even though the token is valid?
391. 🟡 Why are my role checks failing even though the token has a `role` claim?
392. 🟡 Why is `User.Identity.Name` null?
393. 🟡 Why does `User.FindFirst("sub")` return null but `ClaimTypes.NameIdentifier` works?
394. 🟡 Why does my token become invalid exactly 5 minutes late (or early)?
395. 🟡 Why does `[AllowAnonymous]` on a controller override `[Authorize]` on an action?
396. 🟡 Why does `[Authorize]` on a base controller apply to derived controllers?
397. 🟡 Why does a fallback policy block my static files / health check endpoint?
398. 🟡 Why do users get logged out when the app restarts or scales out?
399. 🟡 Why does authentication work locally but fail behind a reverse proxy (HTTPS, redirect URI mismatch)?
400. 🟡 Why do I get "IDX10501: Signature validation failed. Unable to match key"?
401. 🟡 Why do I get "IDX10214: Audience validation failed"?
402. 🟡 Why do I get "IDX10223: Lifetime validation failed. The token is expired"?
403. 🟡 Why do I get "IDX10720: Unable to create KeyedHashAlgorithm... key size must be greater than 256 bits"?
404. 🟡 Why do I get "Correlation failed" in OIDC login?
405. 🟡 Why do I get "redirect_uri_mismatch" from the identity provider?
406. 🟡 Why does silent token renewal fail in Safari/Chrome?
407. 🟡 Is OAuth 2.0 used for authentication? Then why do we need OpenID Connect?
408. 🟡 Can you use an ID token to call an API?
409. 🟡 Should the frontend decode the JWT to make authorization decisions?
410. 🟡 Should you put user roles in the JWT or load them from the database on each request?
411. 🟡 If HTTPS is used, do you still need to sign tokens?
412. 🟡 Is storing JWTs in cookies better than localStorage? Is it completely safe?
413. 🟡 Does `HttpOnly` cookie protect against CSRF?
414. 🟡 Does `SameSite=Lax` fully protect against CSRF?
415. 🟡 Does CORS prevent attackers from calling your API?
416. 🟡 Is Base64 encoding a form of encryption?
417. 🟡 Is hashing reversible? Is encryption reversible?
418. 🔴 Why is the Implicit flow insecure even though it uses HTTPS?
419. 🔴 Why is ROPC (password grant) discouraged even for first-party apps?
420. 🔴 Why can a long-lived refresh token be more dangerous than a long-lived access token?
421. 🔴 If access tokens are short-lived, why do we still need revocation?
422. 🔴 What happens if two APIs share the same audience value?
423. 🔴 What happens if you don't validate the `aud` claim?
424. 🔴 What happens if you don't validate the `iss` claim in a multi-tenant app?
425. 🔴 Why should you not use the same signing key for all environments?
426. 🔴 Why is "role explosion" a problem in RBAC? How do you avoid it?
427. 🔴 Can an attacker change `alg` to `none` and bypass validation in ASP.NET Core?
428. 🔴 Is `[Authorize]` enough to prevent IDOR?
429. 🔴 What is wrong with checking authorization only in the UI?
430. 🔴 Why can caching responses break authorization (shared cache serving private data)?

---

## 26. Predict the Behavior (Code Snippets)

> What happens when each snippet runs? If it fails, say why.

**431. 🟡 Middleware order**
```csharp
app.UseAuthorization();
app.UseAuthentication();
app.MapControllers();
```
A request with a valid token calls an `[Authorize]` endpoint. What is the response?

**432. 🟡 Missing UseAuthentication**
```csharp
builder.Services.AddAuthentication().AddJwtBearer();
app.UseAuthorization();
app.MapControllers();
```

**433. 🟡 AllowAnonymous precedence**
```csharp
[Authorize]
public class AccountsController : ControllerBase
{
    [AllowAnonymous]
    [Authorize(Roles = "Admin")]
    [HttpGet("balance")]
    public IActionResult Balance() => Ok();
}
```
Can an unauthenticated user call `/balance`? 💰

**434. 🟡 Multiple role attributes**
```csharp
[Authorize(Roles = "Admin,Manager")]
public IActionResult A() => Ok();

[Authorize(Roles = "Admin")]
[Authorize(Roles = "Manager")]
public IActionResult B() => Ok();
```
A user has only the `Manager` role. Can they call `A`? `B`?

**435. 🟡 Policy with multiple requirements**
```csharp
options.AddPolicy("Transfer", p =>
{
    p.RequireAuthenticatedUser();
    p.RequireClaim("kyc_verified", "true");
    p.RequireRole("Customer");
});
```
A user with role `Customer` but no `kyc_verified` claim calls the endpoint. What is returned? 💰

**436. 🟡 Multiple handlers for one requirement**
```csharp
public class IsOwnerHandler : AuthorizationHandler<CanEditRequirement, Document> { /* Succeed if owner */ }
public class IsAdminHandler : AuthorizationHandler<CanEditRequirement, Document> { /* Succeed if admin */ }
```
A non-owner admin tries to edit. A non-admin owner tries to edit. Who succeeds?

**437. 🔴 Handler calling Fail**
```csharp
// Handler A calls context.Succeed(requirement)
// Handler B calls context.Fail()
```
Is authorization successful?

**438. 🟡 Expired token with ClockSkew**
```csharp
new TokenValidationParameters { ValidateLifetime = true /* ClockSkew not set */ };
// token exp = 10:00:00, request time = 10:03:00
```
Is the token accepted? What if `ClockSkew = TimeSpan.Zero`?

**439. 🔴 Audience not validated**
```csharp
new TokenValidationParameters
{
    ValidateIssuer = true, ValidIssuer = "https://login.bank.com",
    ValidateAudience = false,
    ValidateIssuerSigningKey = true, IssuerSigningKey = key
};
```
A token issued by the same IdP for a different API is sent. What happens? Why is it a risk? 💰

**440. 🟡 Role claim mapping**
```csharp
// JWT payload: { "sub": "42", "roles": ["Admin"] }
[Authorize(Roles = "Admin")]
public IActionResult Delete() => Ok();
```
Does the user get access? What configuration is needed?

**441. 🟡 Name claim**
```csharp
// JWT payload: { "sub": "42", "preferred_username": "asha" }
Console.WriteLine(User.Identity?.Name);
```
What is printed? How do you fix it?

**442. 🟡 Short HS256 key**
```csharp
var key = new SymmetricSecurityKey(Encoding.UTF8.GetBytes("secret123"));
var creds = new SigningCredentials(key, SecurityAlgorithms.HmacSha256);
```

**443. 🟡 Cookie auth on an API**
```csharp
builder.Services.AddAuthentication(CookieAuthenticationDefaults.AuthenticationScheme).AddCookie();
// API client calls [Authorize] endpoint without a cookie
```
What response does the API client receive? How do you return 401 instead?

**444. 🔴 IDOR**
```csharp
[Authorize]
[HttpGet("accounts/{id}")]
public async Task<IActionResult> Get(int id) => Ok(await _db.Accounts.FindAsync(id));
```
What is the vulnerability? How do you fix it? 💰

**445. 🔴 Fallback policy**
```csharp
builder.Services.AddAuthorization(o =>
    o.FallbackPolicy = new AuthorizationPolicyBuilder().RequireAuthenticatedUser().Build());
app.MapHealthChecks("/health");
app.UseStaticFiles();   // placed after UseAuthorization
```
Can anonymous users access `/health` and static files?

**446. 🔴 Data protection keys**
```csharp
// Cookie auth, 3 instances behind a load balancer, no shared data protection key ring
```
What happens to logged-in users?

**447. 🔴 Mass assignment**
```csharp
public class UpdateUserDto { public string Name { get; set; } public string Role { get; set; } }
[Authorize]
[HttpPut("me")]
public async Task<IActionResult> Update(UpdateUserDto dto)
{
    var user = await _db.Users.FindAsync(User.GetId());
    user.Name = dto.Name; user.Role = dto.Role;
    await _db.SaveChangesAsync();
    return NoContent();
}
```
What can an attacker do?

**448. 🔴 Token in query string**
```csharp
// GET /api/statements/download?access_token=eyJ...
```
What are the risks? When is this pattern used legitimately and how is it made safer? 💰

**449. 🔴 Comparing secrets**
```csharp
if (Request.Headers["X-Api-Key"] == _storedApiKey) { /* allow */ }
```
What are the security problems?

**450. 🔴 Caching a private response**
```csharp
[Authorize]
[ResponseCache(Duration = 60, Location = ResponseCacheLocation.Any)]
[HttpGet("profile")]
public IActionResult Profile() => Ok(GetProfile(User));
```

---

## 27. Scenario-Based Questions — Authentication

451. 🟡 Design the login flow for an ASP.NET Core MVC web application. What components do you use?
452. 🟡 Design authentication for a React/Angular SPA calling an ASP.NET Core API. Which flow and token storage would you use?
453. 🟡 Design authentication for a mobile banking app. Which OAuth flow would you use and why? 💰
454. 🟡 Your company wants "Login with Google and Microsoft" along with local accounts. How do you implement it?
455. 🟡 Users complain they have to log in again every 20 minutes. How do you improve this without weakening security?
456. 🟡 How would you implement "Remember me" securely?
457. 🟡 How do you implement "logout from all devices"?
458. 🟡 How do you force re-login for all users after a security incident?
459. 🟡 How do you lock an account after 5 failed login attempts without allowing attackers to lock out users (DoS)?
460. 🟡 How would you add MFA to an existing application without disrupting existing users?
461. 🟡 A user's phone is lost and they can't access their authenticator app. How do you design the recovery flow?
462. 🟡 How would you implement passwordless login with passkeys?
463. 🔴 An enterprise customer wants SSO with their own Okta/Entra tenant. How do you support it?
464. 🔴 You are migrating 2 million users from a legacy system with MD5 password hashes. How do you migrate securely?
465. 🔴 Your app must support both internal employees (Entra ID) and external customers (B2C). How do you design authentication?
466. 🔴 How would you implement impersonation ("login as user") for support staff securely and auditably? 💰
467. 🔴 A banking app should require re-authentication if the user is idle for 5 minutes. How do you implement this across web and mobile? 💰
468. 🔴 How do you detect and block suspicious logins (new device, new country, impossible travel)? 💰
469. 🔴 How do you design authentication for an IoT device or smart TV app?
470. 🔴 How do you design authentication for a CLI tool used by developers?

---

## 28. Scenario-Based Questions — Authorization

471. 🟡 Design authorization for an HR system with roles Employee, Manager and HR Admin.
472. 🟡 A manager should see only their own team's leave requests. How do you implement it?
473. 🟡 A user should edit only documents they own, but admins can edit all. How do you implement it?
474. 🟡 How do you implement feature-level permissions that admins can change at runtime without redeploying?
475. 🟡 How do you implement permission checks for hundreds of fine-grained permissions without creating hundreds of policies?
476. 🟡 How do you hide UI elements based on permissions while still enforcing security on the server?
477. 🟡 How do you implement multi-tenant authorization so tenant A cannot access tenant B's data?
478. 🟡 A user belongs to multiple organizations with different roles in each. How do you model and enforce this?
479. 🔴 Design maker-checker approval for payments above a threshold. 💰
480. 🔴 Clerks can approve transfers up to ₹50,000, managers up to ₹5,00,000, and above that requires two approvals. How do you implement it? 💰
481. 🔴 A customer can grant read-only access to their accountant. How do you model delegated access? 💰
482. 🔴 How do you implement time-based access (access only during business hours or for a temporary period)?
483. 🔴 How do you implement row-level and column-level security (e.g., hide salary or PAN from some roles)? 💰
484. 🔴 Security audit found that some endpoints have no authorization. How do you fix it and prevent it in future?
485. 🔴 How would you migrate from role-based to permission-based authorization in a large application?
486. 🔴 How do you implement "break-glass" emergency admin access with full auditing? 💰
487. 🔴 How do you authorize access to files stored in blob storage without proxying every download through the API?
488. 🔴 How do you design authorization for a microservice system where each service owns its data?

---

## 29. Scenario-Based Questions — JWT & Tokens

489. 🟡 Implement JWT-based login: what endpoints, claims and validation would you design?
490. 🟡 Your access tokens are valid for 24 hours. What risks does this create and how would you change the design?
491. 🟡 A user's role is changed from Admin to User, but they still have admin access until their token expires. How do you fix it?
492. 🟡 A user is deleted or disabled, but their JWT still works. How do you handle it?
493. 🟡 Your JWT has grown to 8 KB because of roles and permissions and requests start failing. What do you do?
494. 🟡 How do you implement refresh token rotation with reuse detection?
495. 🟡 Two browser tabs try to refresh the token at the same time and one gets logged out. How do you fix it?
496. 🟡 How do you rotate the JWT signing key without logging out all users?
497. 🔴 Your signing key has been leaked. What do you do immediately and afterwards?
498. 🔴 A refresh token was stolen from a mobile device. How do you detect and limit the damage?
499. 🔴 You need to call a downstream API on behalf of the user. How do you pass the identity securely?
500. 🔴 Your API must accept tokens from two different identity providers during a migration. How do you configure it?
501. 🔴 How do you implement token binding to a device to prevent token theft in a banking app? 💰
502. 🔴 How do you design a system where tokens can be revoked instantly but you don't want a DB call on every request?
503. 🔴 Your SPA stores JWTs in localStorage and a pen test found an XSS vulnerability. What do you change?

---

## 30. Scenario-Based Questions — OAuth, OIDC & SSO

504. 🟡 Explain step by step what happens when a user clicks "Login with Microsoft" in your web app.
505. 🟡 A partner company wants to access your customers' data through an API with customer consent. Which OAuth flow do you use?
506. 🟡 A nightly batch job needs to call your API. Which flow do you use?
507. 🟡 You have a public SPA that cannot keep a secret. Which flow do you use and why?
508. 🟡 Your company uses 10 internal applications. How do you implement SSO across all of them?
509. 🟡 A user logs out of one application. Should they be logged out of all SSO applications? How?
510. 🔴 You need to build your own OAuth/OIDC authorization server. What would you use and what must you get right?
511. 🔴 How do you implement consent screens and allow users to revoke third-party app access?
512. 🔴 Design an open banking API that third-party providers can call with customer consent. 💰
513. 🔴 How do you protect against a malicious app registering a redirect URI to steal codes?
514. 🔴 Third-party cookie blocking broke silent token renewal in your SPA. How do you fix it?
515. 🔴 How do you implement a BFF (Backend-for-Frontend) for a SPA? What are its benefits?
516. 🔴 How do you handle a customer's IdP being down? Should users still be able to log in?

---

## 31. Scenario-Based Questions — Debugging & Production Issues

517. 🟡 Your API returns 401 for all requests after deployment to production. How do you debug it?
518. 🟡 Users are logged out randomly in production but not in development. What could cause it?
519. 🟡 OIDC login fails with "Correlation failed" behind a load balancer. What do you check?
520. 🟡 Login works over HTTP locally but fails over HTTPS in production behind Nginx. Why?
521. 🟡 Tokens issued in one environment are accepted in another environment. What is wrong?
522. 🟡 Some users get 403 on an endpoint they should be able to access. How do you investigate?
523. 🟡 Role-based authorization stopped working after upgrading to .NET 8. What changed?
524. 🟡 Your application stops validating tokens after the identity provider rotates keys. Why?
525. 🟡 A pen test reports that the login page reveals whether an email exists. How do you fix it?
526. 🟡 A pen test reports missing `HttpOnly`/`Secure` flags on cookies. How do you fix it?
527. 🔴 You see a spike in failed login attempts from many IPs. What is happening and how do you respond?
528. 🔴 An auditor asks for a report of who accessed a specific customer's data in the last 90 days. How do you make that possible? 💰
529. 🔴 A support engineer accidentally got admin rights to production. How do you prevent and detect this?
530. 🔴 You discover an API endpoint returns other customers' account details by changing the ID. What are your immediate and long-term actions? 💰

---

## 32. System Design Scenarios

531. 🔴 Design the authentication and authorization architecture for an internet banking platform (web + mobile + APIs). 💰
532. 🔴 Design an identity system for a multi-tenant SaaS product with SSO, MFA and per-tenant roles.
533. 🔴 Design authentication for a payment gateway that serves merchants (API keys, webhooks, mTLS). 💰
534. 🔴 Design authorization for a trading platform where traders, risk managers and compliance officers have different access. 💰
535. 🔴 Design a centralized permission service used by 20 microservices.
536. 🔴 Design an API gateway that handles authentication, rate limiting and token validation for downstream services.
537. 🔴 Design a secure partner API platform with onboarding, credentials, scopes and usage limits.
538. 🔴 Design an audit logging system for all authentication and authorization events. 💰

---

## 33. Coding & Hands-On Tasks

539. 🟢 Configure cookie authentication in an ASP.NET Core MVC app with login and logout.
540. 🟢 Protect a controller with `[Authorize]` and allow one action with `[AllowAnonymous]`.
541. 🟡 Implement a JWT login endpoint that issues an access token with user claims and roles.
542. 🟡 Configure `AddJwtBearer` with full validation of issuer, audience, lifetime and signing key.
543. 🟡 Implement a refresh token endpoint with rotation and revocation.
544. 🟡 Implement role-based authorization with Admin and User roles.
545. 🟡 Implement a custom policy with a requirement and handler (e.g., `MinimumAge`, `SameDepartment`).
546. 🟡 Implement resource-based authorization so users can only edit their own resources.
547. 🟡 Implement a dynamic permission-based `[HasPermission("x")]` attribute using a custom `IAuthorizationPolicyProvider`.
548. 🟡 Implement API key authentication using a custom authentication handler.
549. 🟡 Return custom JSON for 401 and 403 responses.
550. 🟡 Integrate Google or Microsoft external login.
551. 🟡 Integrate an ASP.NET Core API with Microsoft Entra ID using `Microsoft.Identity.Web`.
552. 🟡 Configure Swagger UI to authenticate with OAuth2/JWT.
553. 🟡 Implement claims transformation to add permissions from the database.
554. 🟡 Implement TOTP-based two-factor authentication.
555. 🔴 Implement a fake authentication handler and write integration tests for 401, 403 and 200 cases.
556. 🔴 Implement a client credentials token cache and a `DelegatingHandler` that attaches tokens to outgoing calls.
557. 🔴 Implement step-up authentication for a high-value transfer endpoint using `acr`/`amr` claims. 💰
558. 🔴 Implement maker-checker approval with authorization rules. 💰
559. 🔴 Implement HMAC signature validation for incoming webhooks. 💰
560. 🔴 Implement a JWT denylist check in `OnTokenValidated` using a distributed cache.
561. 🔴 Implement multi-tenant JWT validation with per-tenant issuers.
562. 🔴 Implement certificate (mTLS) authentication for a partner API. 💰

---

## 34. Rapid-Fire Round

563. 🟢 What status code means "not authenticated"?
564. 🟢 What status code means "authenticated but not allowed"?
565. 🟢 What are the three parts of a JWT?
566. 🟢 Is a JWT payload encrypted by default?
567. 🟢 Which claim holds the token expiry?
568. 🟢 Which claim identifies the user?
569. 🟢 Which claim identifies the intended recipient of the token?
570. 🟢 Which middleware must come first: authentication or authorization?
571. 🟢 Which attribute allows anonymous access?
572. 🟢 What header carries a bearer token?
573. 🟢 Is OAuth 2.0 an authentication protocol?
574. 🟢 Which protocol adds authentication on top of OAuth 2.0?
575. 🟡 What is the default `ClockSkew` in ASP.NET Core JWT validation?
576. 🟡 Which OAuth flow is recommended for SPAs?
577. 🟡 Which OAuth flow is used for machine-to-machine communication?
578. 🟡 Which OAuth flows are deprecated?
579. 🟡 What does PKCE stand for?
580. 🟡 What is the OIDC discovery endpoint path?
581. 🟡 What does `HttpOnly` prevent?
582. 🟡 What does `SameSite` help prevent?
583. 🟡 Which password hashing algorithm does ASP.NET Core Identity use?
584. 🟡 What does the security stamp do in one line?
585. 🟡 Multiple requirements in one policy — AND or OR?
586. 🟡 Multiple handlers for one requirement — AND or OR?
587. 🔴 What does DPoP stand for?
588. 🔴 What does FAPI stand for?
589. 🔴 What is the difference between `scp` and `roles` claims in Entra ID tokens in one line?
590. 🔴 What is RFC 9700 about?

---

> **Next part (optional):** Microservices.
