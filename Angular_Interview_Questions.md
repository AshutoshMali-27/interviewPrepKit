# 🎯 Angular Interview Questions — Part 16 (Questions Only)

> **Level:** 3–4 years of experience.
> **Scope:** Angular fundamentals & architecture, components, templates & data binding, **new control flow (`@if`, `@for`, `@switch`)**, **`@defer`**, directives & pipes, **standalone components** vs NgModules, dependency injection, services, **signals** (`signal`, `computed`, `effect`, `input()`, `output()`, `model()`, `linkedSignal`, `resource`), RxJS in Angular, change detection (Default, OnPush, **zoneless**), lifecycle hooks, routing (guards, resolvers, lazy loading), forms (template-driven, reactive, typed, signal forms), HttpClient & interceptors, state management (services, signals, NgRx), performance, security, SSR/hydration, testing, build & deployment, **Angular + ASP.NET Core Web API**, predict-the-behavior snippets, coding tasks and scenario-based questions.
> **Covers Angular 2 → 20 (latest versions emphasised).**
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banking portals), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. Angular Fundamentals & Architecture
2. Angular CLI & Project Structure
3. Components
4. Templates & Data Binding
5. Built-in Control Flow & `@defer`
6. Directives
7. Pipes
8. Component Communication
9. Content Projection, ViewChild & ContentChild
10. Lifecycle Hooks
11. Standalone Components vs NgModules
12. Dependency Injection
13. Services
14. Signals
15. RxJS in Angular
16. Change Detection & Zone.js / Zoneless
17. Routing & Navigation
18. Route Guards, Resolvers & Lazy Loading
19. Forms — Template-Driven
20. Forms — Reactive & Typed Forms
21. HttpClient & Interceptors
22. State Management
23. Performance Optimization
24. Security
25. SSR, Hydration & SEO
26. Testing
27. Build, Configuration & Deployment
28. Angular with ASP.NET Core Web API
29. Angular Version Upgrades & What's New
30. Tricky Questions
31. Predict the Behavior
32. Coding Tasks
33. Machine Coding Problems
34. Scenario-Based Questions
35. Rapid-Fire Round

---

## 1. Angular Fundamentals & Architecture

1. 🟢 What is Angular? How is it different from AngularJS?
2. 🟢 What are the main building blocks of an Angular application?
3. 🟢 What is a Single Page Application (SPA)? What are its pros and cons?
4. 🟢 Why does Angular use TypeScript?
5. 🟢 What is the difference between Angular, React and Vue?
6. 🟡 What is the Angular application bootstrap process (`main.ts`, `bootstrapApplication`, root component)?
7. 🟡 What is `app.config.ts` and `provideRouter`, `provideHttpClient` in standalone apps?
8. 🟡 What is AOT (Ahead-of-Time) vs JIT (Just-in-Time) compilation? Which is default and why?
9. 🟡 What is the Ivy rendering engine? What benefits did it bring?
10. 🟡 What are decorators in Angular (`@Component`, `@Injectable`, `@Input`, `@Output`, `@NgModule`, `@Directive`, `@Pipe`)?
11. 🟡 What is metadata in Angular?
12. 🟡 What is the Angular release cycle and LTS policy?

---

## 2. Angular CLI & Project Structure

13. 🟢 What is Angular CLI? Name common commands (`ng new`, `ng serve`, `ng generate`, `ng build`, `ng test`, `ng update`, `ng add`).
14. 🟢 Explain the structure of an Angular project (`src/app`, `assets`/`public`, `environments`, `angular.json`, `tsconfig.json`, `package.json`).
15. 🟡 What is `angular.json` used for?
16. 🟡 What are environments and how do you configure environment-specific values (API URL)?
17. 🟡 What is the new build system (esbuild + Vite-based `application` builder)?
18. 🟡 What are schematics?
19. 🟡 What is an Angular workspace with multiple projects / libraries?
20. 🟡 What is a monorepo with Nx?
21. 🟡 What is `proxy.conf.json` and why is it used during development to call a .NET API?

---

## 3. Components

22. 🟢 What is a component? What are its parts (class, template, styles, selector)?
23. 🟢 How do you create a component using the CLI?
24. 🟡 What are `templateUrl` vs `template` and `styleUrl(s)` vs `styles`?
25. 🟡 What is view encapsulation (Emulated, ShadowDom, None)?
26. 🟡 What is `:host`, `::ng-deep` (deprecated) and how do you style child components?
27. 🟡 What is the difference between a smart (container) component and a dumb (presentational) component?
28. 🟡 What is `host` metadata vs `@HostBinding` and `@HostListener`?
29. 🟡 What are dynamic components? How do you create them (`ViewContainerRef.createComponent`, `NgComponentOutlet`)?
30. 🔴 How do you design reusable components for a component library?

---

## 4. Templates & Data Binding

31. 🟢 What is data binding? What are its types?
32. 🟢 What is interpolation (`{{ }}`)?
33. 🟢 What is property binding (`[property]`)?
34. 🟢 What is event binding (`(event)`)?
35. 🟢 What is two-way binding (`[(ngModel)]`)? What is "banana in a box"?
36. 🟡 What is the difference between attribute binding (`[attr.x]`) and property binding?
37. 🟡 What are class and style bindings (`[class.active]`, `[style.width.px]`)?
38. 🟡 What are template reference variables (`#ref`)?
39. 🟡 What is the safe navigation operator (`?.`) and non-null assertion (`!`) in templates?
40. 🟡 What is `ng-template`, `ng-container` and `ngTemplateOutlet`?
41. 🟡 What are template expressions and what are their restrictions?
42. 🟡 Why should you avoid calling functions in templates?
43. 🟡 What is `$event`?
44. 🟡 What is `@let` in templates (Angular 18.1+)?

---

## 5. Built-in Control Flow & `@defer`

45. 🟢 What is the new built-in control flow syntax (`@if`, `@else`, `@for`, `@switch`)?
46. 🟡 How is `@if` different from `*ngIf`?
47. 🟡 Why is `track` mandatory in `@for`? What should you track by?
48. 🟡 What is `@empty` in `@for`?
49. 🟡 What contextual variables are available in `@for` (`$index`, `$first`, `$last`, `$even`, `$odd`, `$count`)?
50. 🟡 How do you migrate from `*ngIf`/`*ngFor` to the new control flow (`ng generate @angular/core:control-flow`)?
51. 🟡 What is `@defer`? What problem does it solve?
52. 🟡 What are `@placeholder`, `@loading` and `@error` blocks?
53. 🟡 What are `@defer` triggers (`on idle`, `on viewport`, `on interaction`, `on hover`, `on timer`, `on immediate`, `when condition`)?
54. 🟡 What is prefetching with `@defer`?
55. 🔴 What are the requirements for a component to be deferrable (standalone, not referenced elsewhere)?

---

## 6. Directives

56. 🟢 What is a directive? What are its types (component, structural, attribute)?
57. 🟢 What are built-in structural directives (`*ngIf`, `*ngFor`, `*ngSwitch`)?
58. 🟢 What are built-in attribute directives (`ngClass`, `ngStyle`, `ngModel`)?
59. 🟡 How do you create a custom attribute directive (e.g., `appHighlight`, `appNumbersOnly`)?
60. 🟡 How do you create a custom structural directive (e.g., `*appHasRole`)?
61. 🟡 What does the `*` (asterisk) mean in structural directives (desugaring to `ng-template`)?
62. 🟡 Why can't you use two structural directives on the same element?
63. 🟡 What is `trackBy` in `*ngFor` and why is it important?
64. 🟡 What are host directives (directive composition API)?
65. 🟡 How do you pass inputs to a directive?
66. 🔴 Write a directive that allows only numbers with 2 decimal places in an amount field. 💰

---

## 7. Pipes

67. 🟢 What is a pipe? Name built-in pipes (`date`, `currency`, `decimal`, `percent`, `uppercase`, `lowercase`, `json`, `async`, `slice`, `keyvalue`, `titlecase`).
68. 🟢 How do you chain pipes and pass parameters?
69. 🟡 How do you format currency in INR (`currency:'INR':'symbol':'1.2-2':'en-IN'`)? 💰
70. 🟡 How do you create a custom pipe?
71. 🟡 What are pure vs impure pipes? What are the performance implications?
72. 🟡 What does the `async` pipe do? Why is it recommended?
73. 🟡 Why is using a pipe better than calling a method in the template?
74. 🟡 How do you register locale data for `en-IN` formatting?
75. 🔴 Write a custom pipe to mask account/card numbers (`XXXX-XXXX-1234`). 💰

---

## 8. Component Communication

76. 🟢 How do you pass data from parent to child (`@Input`, `input()`)?
77. 🟢 How do you pass data from child to parent (`@Output` + `EventEmitter`, `output()`)?
78. 🟡 What are required inputs and input transforms (`input.required()`, `transform: booleanAttribute`)?
79. 🟡 What is `model()` for two-way binding between components?
80. 🟡 How do sibling components communicate (shared service, signals, Subject)?
81. 🟡 What is `@Input` setter vs `ngOnChanges` for reacting to input changes?
82. 🟡 How do you access a child component's methods from the parent (`@ViewChild`, `viewChild()`)?
83. 🟡 What are the different ways to share data between unrelated components?
84. 🔴 When would you use a service with signals vs `BehaviorSubject` vs a store for sharing state?

---

## 9. Content Projection, ViewChild & ContentChild

85. 🟡 What is content projection (`<ng-content>`)?
86. 🟡 What is multi-slot content projection (`select` attribute)?
87. 🟡 What is the difference between `@ViewChild` and `@ContentChild`?
88. 🟡 What are `viewChild()`, `viewChildren()`, `contentChild()`, `contentChildren()` signal queries?
89. 🟡 What is the `static` option in `@ViewChild`?
90. 🟡 When is a `@ViewChild` available (which lifecycle hook)?
91. 🟡 What is `ElementRef`? Why should direct DOM access be avoided? What is `Renderer2`?
92. 🔴 What is `TemplateRef` and `ViewContainerRef`?

---

## 10. Lifecycle Hooks

93. 🟢 What are lifecycle hooks? List them in order.
94. 🟢 What is the difference between `constructor` and `ngOnInit`?
95. 🟡 When is `ngOnChanges` called? What is `SimpleChanges`?
96. 🟡 What is `ngDoCheck` and why should you be careful with it?
97. 🟡 What are `ngAfterContentInit`, `ngAfterContentChecked`, `ngAfterViewInit`, `ngAfterViewChecked`?
98. 🟡 What is `ngOnDestroy` used for? What should you clean up?
99. 🟡 What is `DestroyRef` and `takeUntilDestroyed`?
100. 🟡 What are `afterNextRender` and `afterRender` / `afterEveryRender`?
101. 🟡 What causes the `ExpressionChangedAfterItHasBeenCheckedError`? How do you fix it?
102. 🔴 In which hook should you make an API call, and why?

---

## 11. Standalone Components vs NgModules

103. 🟢 What is an NgModule? What are `declarations`, `imports`, `exports`, `providers` and `bootstrap`?
104. 🟢 What are standalone components? Why were they introduced?
105. 🟡 Are standalone components the default in Angular 19+?
106. 🟡 How do you import dependencies into a standalone component (`imports: [...]`)?
107. 🟡 How do you bootstrap a standalone application?
108. 🟡 What are feature modules, shared modules and core modules (NgModule-era patterns)?
109. 🟡 How do you migrate an NgModule-based app to standalone (`ng generate @angular/core:standalone`)?
110. 🟡 Can standalone components and NgModules be mixed?
111. 🔴 What is the `forRoot()` / `forChild()` pattern and what replaced it in standalone apps?

---

## 12. Dependency Injection

112. 🟢 What is dependency injection in Angular?
113. 🟢 What does `@Injectable({ providedIn: 'root' })` mean?
114. 🟡 What is the `inject()` function? How is it different from constructor injection?
115. 🟡 What is the injector hierarchy (root/environment injector, element injector)?
116. 🟡 What is the difference between providing a service in `root`, in a route, and in a component?
117. 🟡 What are provider types (`useClass`, `useValue`, `useFactory`, `useExisting`)?
118. 🟡 What is an `InjectionToken`? Give a use case (API base URL, configuration).
119. 🟡 What are resolution modifiers (`@Optional`, `@Self`, `@SkipSelf`, `@Host` / `inject(..., { optional: true })`)?
120. 🟡 What is a multi provider (`multi: true`)?
121. 🟡 What are environment providers and `makeEnvironmentProviders`?
122. 🔴 Why might a service be instantiated more than once in an app? How do you make it a true singleton?
123. 🔴 What is tree-shakable providers and why does `providedIn: 'root'` enable it?

---

## 13. Services

124. 🟢 What is a service? Why should you use services?
125. 🟡 How do you create a service for API calls?
126. 🟡 How do you share data between components using a service?
127. 🟡 How do you store and expose state in a service using signals or `BehaviorSubject`?
128. 🟡 Should components call `HttpClient` directly or go through a service? Why?
129. 🔴 How do you design a service layer for a large banking application (API services, facade services, state services)? 💰

---

## 14. Signals

130. 🟢 What are signals in Angular? Why were they introduced?
131. 🟢 How do you create and update a signal (`signal()`, `set()`, `update()`)?
132. 🟡 What is a `computed` signal? Is it lazy? Is it memoized?
133. 🟡 What is an `effect`? When should and shouldn't you use it?
134. 🟡 What is `untracked()`?
135. 🟡 What are signal inputs (`input()`), outputs (`output()`) and model inputs (`model()`)?
136. 🟡 What is `linkedSignal`?
137. 🟡 What are `resource()` and `httpResource()`? How do they handle loading and error states?
138. 🟡 How do you convert between signals and observables (`toSignal`, `toObservable`)?
139. 🟡 What is the difference between signals and RxJS observables? When do you use each?
140. 🟡 How do signals improve change detection?
141. 🟡 What are signal-based queries (`viewChild()`, `contentChildren()`)?
142. 🟡 How do you implement a simple store using signals?
143. 🔴 Why should you not write to signals inside `computed`? What happens if you set signals inside an `effect`?
144. 🔴 What are equality functions for signals?
145. 🔴 What are signal forms (experimental in Angular 21)?

---

## 15. RxJS in Angular

146. 🟢 What is RxJS? What is an Observable?
147. 🟢 What is the difference between an Observable and a Promise?
148. 🟢 What is a subscription? How do you unsubscribe?
149. 🟡 What is the difference between cold and hot observables?
150. 🟡 What are `Subject`, `BehaviorSubject`, `ReplaySubject` and `AsyncSubject`?
151. 🟡 What are the most commonly used operators (`map`, `filter`, `tap`, `switchMap`, `mergeMap`, `concatMap`, `exhaustMap`, `debounceTime`, `distinctUntilChanged`, `catchError`, `retry`, `takeUntil`, `take`, `finalize`, `shareReplay`)?
152. 🟡 What is the difference between `switchMap`, `mergeMap`, `concatMap` and `exhaustMap`? Give a use case for each.
153. 🟡 Which operator would you use for search-as-you-type? For a "Pay" button that must not be double-submitted? 💰
154. 🟡 What do `forkJoin`, `combineLatest`, `zip`, `merge` and `withLatestFrom` do?
155. 🟡 How do you make parallel API calls and wait for all?
156. 🟡 How do you handle errors in an observable stream without killing it?
157. 🟡 What is `shareReplay` and when is it useful (caching an HTTP call)?
158. 🟡 What are the ways to avoid memory leaks with subscriptions (`async` pipe, `takeUntilDestroyed`, `take(1)`)?
159. 🟡 Do you need to unsubscribe from `HttpClient` observables?
160. 🔴 How do you implement polling with RxJS (`interval` + `switchMap`)?
161. 🔴 How do you implement retry with exponential backoff (`retry({ count, delay })`)?
162. 🔴 What are higher-order observables?

---

## 16. Change Detection & Zone.js / Zoneless

163. 🟢 What is change detection in Angular?
164. 🟡 What is Zone.js? How does it trigger change detection?
165. 🟡 What is the Default change detection strategy?
166. 🟡 What is `OnPush`? When does an `OnPush` component get checked?
167. 🟡 Why does mutating an object input not update an `OnPush` child? How do you fix it (immutability)?
168. 🟡 What do `ChangeDetectorRef.markForCheck()`, `detectChanges()` and `detach()` do?
169. 🟡 What is `NgZone.runOutsideAngular()` and when would you use it?
170. 🟡 What is zoneless change detection (`provideZonelessChangeDetection`)? How do signals enable it?
171. 🟡 What are the benefits of going zoneless?
172. 🔴 How does Angular decide which components to check with signals + OnPush (local change detection)?
173. 🔴 Why can third-party libraries cause excessive change detection cycles?

---

## 17. Routing & Navigation

174. 🟢 What is the Angular Router? How do you configure routes?
175. 🟢 What are `routerLink`, `routerLinkActive` and `router-outlet`?
176. 🟢 How do you navigate programmatically (`router.navigate`, `navigateByUrl`)?
177. 🟡 How do you read route parameters and query parameters (`ActivatedRoute`, `paramMap`, `queryParamMap`, `withComponentInputBinding`)?
178. 🟡 What is the difference between `snapshot` and observable params?
179. 🟡 What are child routes and nested router outlets?
180. 🟡 What are wildcard routes and redirects (`**`, `redirectTo`, `pathMatch: 'full'`)?
181. 🟡 What are named outlets (auxiliary routes)?
182. 🟡 What is `PathLocationStrategy` vs `HashLocationStrategy`? Why do you need a server fallback (Nginx `try_files`) for path routing?
183. 🟡 What are router events? How do you show a loading bar on navigation?
184. 🟡 How do you pass data/state between routes (route `data`, `state` in `navigate`, query params, service)?
185. 🟡 What is `title` in route config and `TitleStrategy`?
186. 🔴 What is a custom `RouteReuseStrategy`?

---

## 18. Route Guards, Resolvers & Lazy Loading

187. 🟢 What are route guards? Name the types (`canActivate`, `canActivateChild`, `canDeactivate`, `canMatch`, `resolve`).
188. 🟡 What are functional guards vs class-based guards?
189. 🟡 How do you write an auth guard that redirects to login? 💰
190. 🟡 How do you write a role-based guard? 💰
191. 🟡 How do you write a `canDeactivate` guard to warn about unsaved changes?
192. 🟡 What is the difference between `canActivate` and `canMatch`?
193. 🟡 What is a resolver? What are its pros and cons?
194. 🟡 What is lazy loading? How do you lazy load components (`loadComponent`) and routes (`loadChildren`)?
195. 🟡 What are preloading strategies (`PreloadAllModules`, custom)?
196. 🟡 Are route guards enough for security? Why must the API also authorize? 💰
197. 🔴 How do you protect routes based on permissions loaded from an API after login?

---

## 19. Forms — Template-Driven

198. 🟢 What are template-driven forms?
199. 🟢 How do you use `ngModel`, `ngForm` and `name` attributes?
200. 🟡 How do you add validation (`required`, `minlength`, `pattern`, `email`) in template-driven forms?
201. 🟡 What are form control states (`touched`, `untouched`, `dirty`, `pristine`, `valid`, `invalid`)?
202. 🟡 What CSS classes does Angular add (`ng-valid`, `ng-invalid`, `ng-touched`, `ng-dirty`)?
203. 🟡 When would you choose template-driven forms over reactive forms?

---

## 20. Forms — Reactive & Typed Forms

204. 🟢 What are reactive forms? What are `FormControl`, `FormGroup`, `FormArray` and `FormBuilder`?
205. 🟢 What is the difference between template-driven and reactive forms?
206. 🟡 How do you add built-in validators?
207. 🟡 How do you create a custom validator (e.g., PAN, IFSC, Aadhaar, mobile, amount limit)? 💰
208. 🟡 How do you create a cross-field validator (password confirmation, from-date/to-date, transfer amount ≤ balance)? 💰
209. 🟡 How do you create an async validator (checking if a username/account exists via API)?
210. 🟡 What are typed reactive forms (Angular 14+)? What is `NonNullableFormBuilder`?
211. 🟡 How do you dynamically add/remove controls using `FormArray` (multiple nominees/beneficiaries)? 💰
212. 🟡 What is the difference between `setValue` and `patchValue`?
213. 🟡 What do `valueChanges` and `statusChanges` do?
214. 🟡 What is `updateOn: 'blur'` / `'submit'`?
215. 🟡 How do you disable/enable controls and why are disabled values excluded from `form.value` (`getRawValue()`)?
216. 🟡 How do you show validation messages properly (only after touch/submit)?
217. 🟡 What is `ControlValueAccessor`? How do you create a custom form control (e.g., amount input, OTP input)?
218. 🟡 How do you map server-side validation errors from an ASP.NET Core API to form controls?
219. 🔴 How do you build dynamic forms from JSON configuration?
220. 🔴 How do you handle a large form with many sections and save drafts? 💰

---

## 21. HttpClient & Interceptors

221. 🟢 What is `HttpClient`? How do you make GET, POST, PUT and DELETE requests?
222. 🟢 How do you set up `HttpClient` (`provideHttpClient()`)? What is `withFetch()`?
223. 🟡 How do you add headers, query parameters and request bodies?
224. 🟡 How do you handle HTTP errors (`catchError`, `HttpErrorResponse`)?
225. 🟡 How do you type API responses with interfaces/models?
226. 🟡 What are HTTP interceptors? What are functional interceptors (`withInterceptors`)?
227. 🟡 How do you add a JWT token to all requests using an interceptor?
228. 🟡 How do you implement a global error handling interceptor (401 → login, 403, 500 → toast)?
229. 🟡 How do you implement a loading spinner interceptor?
230. 🟡 How do you implement token refresh in an interceptor without making multiple refresh calls?
231. 🟡 How do you upload files with progress (`reportProgress`, `observe: 'events'`)?
232. 🟡 How do you download files (blob) such as PDF statements or Excel reports? 💰
233. 🟡 How do you cancel an HTTP request?
234. 🟡 How do you cache HTTP responses?
235. 🟡 What is `HttpContext` and `HttpContextToken` (e.g., to skip the loader or auth for some requests)?
236. 🟡 How do you retry failed requests?
237. 🔴 What is the order of execution of multiple interceptors for request and response?
238. 🔴 What is `HttpTestingController`?

---

## 22. State Management

239. 🟡 What is state management? Why is it needed in large Angular apps?
240. 🟡 What are the options (services + signals, services + BehaviorSubject, NgRx Store, NgRx SignalStore, NGXS, Akita/Elf)?
241. 🟡 What is NgRx? Explain actions, reducers, selectors, effects and the store.
242. 🟡 What is the Redux pattern and unidirectional data flow?
243. 🟡 What is NgRx SignalStore? How is it different from the classic NgRx Store?
244. 🟡 What are NgRx Effects used for?
245. 🟡 What are memoized selectors?
246. 🟡 What is Redux DevTools?
247. 🟡 When is NgRx overkill?
248. 🔴 How do you persist state across page refreshes (localStorage, sessionStorage) securely? 💰

---

## 23. Performance Optimization

249. 🟡 How do you improve the performance of an Angular application?
250. 🟡 How does `OnPush` improve performance?
251. 🟡 How do `track` / `trackBy` improve list rendering performance?
252. 🟡 How do lazy loading and `@defer` reduce initial bundle size?
253. 🟡 What is virtual scrolling (`cdk-virtual-scroll-viewport`)? When do you need it? 💰
254. 🟡 How do you avoid memory leaks in Angular?
255. 🟡 How do you analyse bundle size (`ng build --stats-json`, source-map-explorer)?
256. 🟡 What are budgets in `angular.json`?
257. 🟡 What is `NgOptimizedImage`?
258. 🟡 Why are functions in templates bad for performance? What are the alternatives (pipes, computed signals)?
259. 🟡 How do you debounce expensive operations like search?
260. 🟡 How do you profile Angular apps (Angular DevTools profiler, Chrome Performance)?
261. 🔴 How do you render a grid with 1 lakh transactions efficiently? 💰
262. 🔴 How do Web Workers help in Angular (`ng generate web-worker`)?

---

## 24. Security

263. 🟡 How does Angular protect against XSS (automatic sanitisation)?
264. 🟡 What is `DomSanitizer`? What does `bypassSecurityTrustHtml` do and why is it dangerous?
265. 🟡 Is `[innerHTML]` safe in Angular?
266. 🟡 How does Angular help with CSRF/XSRF protection (`HttpClientXsrfModule`, `withXsrfConfiguration`)?
267. 🟡 Where should you store JWT tokens in an Angular app? What are the risks? 💰
268. 🟡 Why are route guards not a security boundary?
269. 🟡 How do you hide sensitive data in the UI (masking) and prevent it from being logged? 💰
270. 🟡 What is Content Security Policy and how does it affect Angular (inline styles, nonces)?
271. 🟡 How do you implement auto-logout on inactivity? 💰
272. 🔴 How do you integrate OAuth 2.0 / OpenID Connect (Authorization Code + PKCE) in Angular (angular-auth-oidc-client, MSAL Angular)?
273. 🔴 What is the Backend-for-Frontend (BFF) pattern for Angular + ASP.NET Core and why is it more secure than storing tokens in the browser? 💰

---

## 25. SSR, Hydration & SEO

274. 🟡 What is server-side rendering (SSR) in Angular? What was Angular Universal?
275. 🟡 What is hydration? What is incremental hydration?
276. 🟡 What are SSR vs SSG (prerendering) vs CSR? When do you use each?
277. 🟡 What problems occur when using `window`, `document` or `localStorage` with SSR? How do you handle them (`isPlatformBrowser`, `afterNextRender`)?
278. 🟡 What is `TransferState` / HTTP transfer cache?
279. 🟡 How do you set meta tags and titles for SEO (`Meta`, `Title` services)?
280. 🔴 Does a banking internet portal need SSR? Why or why not? 💰

---

## 26. Testing

281. 🟢 What testing tools does Angular use (Jasmine, Karma, Jest, Vitest, Web Test Runner)?
282. 🟡 What is `TestBed`? How do you configure a component test?
283. 🟡 How do you test a component with inputs and outputs?
284. 🟡 How do you test a service that uses `HttpClient` (`provideHttpClientTesting`, `HttpTestingController`)?
285. 🟡 How do you mock services and dependencies?
286. 🟡 How do you test async code (`fakeAsync`, `tick`, `waitForAsync`, `flush`)?
287. 🟡 How do you test reactive forms and validators?
288. 🟡 How do you test pipes and directives?
289. 🟡 How do you test components that use signals?
290. 🟡 What is component harness testing (CDK harnesses)?
291. 🟡 What are E2E testing tools for Angular (Cypress, Playwright)? What happened to Protractor?
292. 🔴 How do you test route guards and interceptors?

---

## 27. Build, Configuration & Deployment

293. 🟡 What does `ng build` produce? What is the production configuration?
294. 🟡 What is the `base href` and when must you change it?
295. 🟡 How do you deploy an Angular app on Nginx (static files, `try_files $uri $uri/ /index.html`)?
296. 🟡 How do you deploy an Angular app on IIS (URL Rewrite for deep links)?
297. 🟡 How do you host an Angular SPA together with an ASP.NET Core API (same origin vs separate origins)?
298. 🟡 How do you configure the API URL per environment without rebuilding the app (runtime config via `config.json` / `APP_INITIALIZER` / `provideAppInitializer`)?
299. 🟡 What is cache busting (output hashing) and why is it important after deployments?
300. 🟡 Why do users sometimes see the old version after deployment? How do you fix it (cache headers for `index.html`)?
301. 🟡 How do you deploy Angular to S3 + CloudFront or Azure Static Web Apps?
302. 🟡 How do you containerise an Angular app with Nginx in Docker?
303. 🔴 What is a micro-frontend architecture? What is Module Federation / Native Federation?

---

## 28. Angular with ASP.NET Core Web API

304. 🟢 How does an Angular front end communicate with an ASP.NET Core Web API?
305. 🟡 Why do you get CORS errors when Angular (`localhost:4200`) calls a .NET API (`localhost:5001`)? How do you fix it (CORS policy or dev proxy)?
306. 🟡 Why does the .NET API return camelCase JSON, and how should Angular models be defined?
307. 🟡 How do you handle `ProblemDetails` / validation errors from ASP.NET Core in Angular?
308. 🟡 How do you send dates between Angular and .NET without time zone issues? 💰
309. 🟡 How do you send `decimal` amounts safely between .NET and Angular (number vs string, precision)? 💰
310. 🟡 How do you implement JWT authentication between Angular and ASP.NET Core?
311. 🟡 How do you implement cookie authentication with Angular and ASP.NET Core (same site, `withCredentials`, antiforgery)?
312. 🟡 How do you implement file upload from Angular to an ASP.NET Core API (`IFormFile`)?
313. 🟡 How do you implement server-side paging, sorting and filtering with Angular Material table + .NET API?
314. 🟡 How do you implement real-time updates with SignalR in Angular (`@microsoft/signalr`)? 💰
315. 🟡 How do you generate Angular API clients from the .NET OpenAPI/Swagger spec (NSwag, OpenAPI Generator)?
316. 🟡 How do you use the ASP.NET Core Angular SPA template / `UseSpa` / SPA proxy?
317. 🔴 How do you handle API versioning changes in the Angular client?

---

## 29. Angular Version Upgrades & What's New

318. 🟡 How do you upgrade an Angular app from one major version to another (`ng update`, update.angular.dev)?
319. 🟡 What were the major changes in Angular 14–15 (standalone components, typed forms, `inject()`, functional guards)?
320. 🟡 What were the major changes in Angular 16 (signals developer preview, `takeUntilDestroyed`, required inputs, SSR hydration)?
321. 🟡 What were the major changes in Angular 17 (new control flow, `@defer`, new logo/docs, esbuild builder default, standalone default for new projects)?
322. 🟡 What were the major changes in Angular 18 (zoneless experimental, `@let`, stable control flow & defer, Material 3)?
323. 🟡 What were the major changes in Angular 19 (standalone default, `linkedSignal`, `resource`, incremental hydration, signal APIs stable)?
324. 🟡 What were the major changes in Angular 20 (zoneless stable/developer preview progression, `httpResource`, stabilised signals APIs, new style guide)?
325. 🔴 What problems did you face while upgrading an Angular application and how did you solve them?
326. 🔴 How would you migrate an AngularJS (1.x) application to modern Angular?

---

## 30. Tricky Questions

327. 🟡 Why doesn't the view update when you push an item into an array in an `OnPush` component?
328. 🟡 Why do you get `ExpressionChangedAfterItHasBeenCheckedError` only in development?
329. 🟡 Why does an HTTP call fire twice?
330. 🟡 Why does a service hold different data in two components?
331. 🟡 Why is `@ViewChild` undefined in `ngOnInit`?
332. 🟡 Why does `ngOnChanges` not fire when you mutate an object input?
333. 🟡 Why does a subscription in a component keep running after you navigate away?
334. 🟡 Why does `form.value` not include a disabled control's value?
335. 🟡 Why does refreshing a deep link (e.g., `/accounts/123`) give 404 in production but not locally?
336. 🟡 Why do users still see the old version after a deployment?
337. 🟡 Why does an interceptor not run for some requests?
338. 🟡 Why can putting a function call in a template slow down the app?
339. 🟡 Is `constructor` or `ngOnInit` the right place to call APIs?
340. 🟡 Do you always need to unsubscribe from observables?
341. 🟡 Can you use `async/await` instead of observables with `HttpClient`?
342. 🟡 Are route guards enough to secure an admin page?
343. 🟡 Why does `localStorage` throw an error with SSR?
344. 🟡 Why does an `effect` run more often than expected?
345. 🟡 Why does `@for` throw an error without `track`?
346. 🔴 Why does `switchMap` cancel your previous save request, and why could that be dangerous for payments? 💰
347. 🔴 Why can `combineLatest` not emit anything?
348. 🔴 Why can `shareReplay` without `refCount` cause memory leaks?

---

## 31. Predict the Behavior

> What happens in each snippet? Explain why and how to fix it if needed.

**349. 🟡 OnPush with mutation**
```ts
@Component({ selector: 'app-list', changeDetection: ChangeDetectionStrategy.OnPush,
  template: `@for (i of items; track i) { <li>{{ i }}</li> }` })
export class ListComponent { @Input() items: string[] = []; }

// parent
addItem() { this.items.push('New'); }
```

**350. 🟡 ViewChild timing**
```ts
@ViewChild('box') box!: ElementRef;
ngOnInit() { console.log(this.box); }
ngAfterViewInit() { console.log(this.box); }
```

**351. 🟡 Constructor vs ngOnInit**
```ts
export class UserComponent implements OnInit {
  @Input() userId!: number;
  constructor() { console.log('ctor', this.userId); }
  ngOnInit() { console.log('init', this.userId); }
}
// <app-user [userId]="5" />
```

**352. 🟡 Signals and computed**
```ts
const price = signal(100);
const qty = signal(2);
const total = computed(() => price() * qty());
console.log(total());
price.set(150);
console.log(total());
qty.update(q => q + 1);
console.log(total());
```

**353. 🟡 Mutating a signal's object**
```ts
const user = signal({ name: 'Asha', age: 30 });
const label = computed(() => `${user().name} (${user().age})`);
user().age = 31;
console.log(label());
user.set({ ...user(), age: 32 });
console.log(label());
```

**354. 🟡 Cold observable**
```ts
const users$ = this.http.get<User[]>('/api/users');
users$.subscribe();
users$.subscribe();
```
How many HTTP requests are made? How do you make it one?

**355. 🟡 async pipe twice**
```html
<div>{{ (user$ | async)?.name }}</div>
<div>{{ (user$ | async)?.email }}</div>
```

**356. 🟡 switchMap vs exhaustMap**
```ts
this.payClicks$.pipe(switchMap(() => this.api.pay(this.amount))).subscribe();
// user clicks "Pay" 3 times quickly
```
What happens? What happens with `exhaustMap`? With `concatMap`? 💰

**357. 🟡 BehaviorSubject vs Subject**
```ts
const s = new Subject<number>();
const b = new BehaviorSubject<number>(0);
s.next(1); b.next(1);
s.subscribe(v => console.log('subject', v));
b.subscribe(v => console.log('behavior', v));
s.next(2); b.next(2);
```

**358. 🟡 forkJoin with an error**
```ts
forkJoin({ accounts: this.api.accounts(), cards: this.api.cards() })  // cards() returns 500
  .subscribe({ next: r => console.log(r), error: e => console.log('error') });
```

**359. 🟡 combineLatest**
```ts
const a$ = new Subject<number>();
const b$ = new Subject<number>();
combineLatest([a$, b$]).subscribe(v => console.log(v));
a$.next(1); a$.next(2); b$.next(10); a$.next(3);
```

**360. 🟡 Disabled control**
```ts
const form = new FormGroup({
  amount: new FormControl(500),
  account: new FormControl({ value: 'SB123', disabled: true }),
});
console.log(form.value);
console.log(form.getRawValue());
```

**361. 🟡 setValue vs patchValue**
```ts
const form = new FormGroup({ name: new FormControl(''), email: new FormControl('') });
form.patchValue({ name: 'Ravi' });
form.setValue({ name: 'Ravi' });
```

**362. 🟡 Pure pipe with mutation**
```ts
@Pipe({ name: 'total' }) export class TotalPipe implements PipeTransform {
  transform(items: { amt: number }[]) { return items.reduce((s, i) => s + i.amt, 0); }
}
// template: {{ txns | total }}
// component: this.txns.push({ amt: 100 });
```

**363. 🟡 Service provided in component**
```ts
@Component({ selector: 'app-a', providers: [CartService], template: '' }) class A { constructor(public cart: CartService) {} }
@Component({ selector: 'app-b', providers: [CartService], template: '' }) class B { constructor(public cart: CartService) {} }
```
Do A and B share the same cart?

**364. 🟡 Interceptor order**
```ts
provideHttpClient(withInterceptors([authInterceptor, loggingInterceptor, errorInterceptor]))
```
In which order do they process the request and the response?

**365. 🟡 Route matching**
```ts
const routes: Routes = [
  { path: '', redirectTo: 'home' },
  { path: '**', component: NotFoundComponent },
  { path: 'accounts', component: AccountsComponent },
];
```
What happens when navigating to `/accounts`? What's wrong with the redirect?

**366. 🔴 Effect writing to a signal**
```ts
const count = signal(0);
const doubled = signal(0);
effect(() => { doubled.set(count() * 2); });
```
Does this work? Is it a good practice? What should you use instead?

**367. 🔴 Unsubscribed interval**
```ts
ngOnInit() { interval(1000).subscribe(() => this.refreshBalance()); }
// user navigates away from the component
```
💰

**368. 🔴 ExpressionChangedAfterItHasBeenChecked**
```ts
@Component({ template: `{{ message }}` })
export class Child implements AfterViewInit {
  message = 'Loading';
  ngAfterViewInit() { this.message = 'Loaded'; }
}
```

---

## 32. Coding Tasks

369. 🟢 Create a component that displays a list of accounts using `@for` with `track`.
370. 🟢 Pass data from a parent to a child and emit an event from the child back to the parent (using `input()`/`output()`).
371. 🟡 Create a counter using signals with `computed` values.
372. 🟡 Create a custom pipe to format numbers in Indian currency format. 💰
373. 🟡 Create a custom pipe to mask account numbers. 💰
374. 🟡 Create a custom directive that allows only numeric input with 2 decimal places. 💰
375. 🟡 Create a structural directive `*appHasRole="'Admin'"`.
376. 🟡 Create a service that fetches data from a .NET API and caches the result.
377. 🟡 Create an HTTP interceptor that adds a JWT token and handles 401 by redirecting to login.
378. 🟡 Create a loading spinner interceptor with a counter for concurrent requests.
379. 🟡 Create an auth guard and a role guard using functional guards.
380. 🟡 Create a `canDeactivate` guard that warns about unsaved form changes.
381. 🟡 Create a reactive form for fund transfer with validators (amount > 0, amount ≤ balance, required beneficiary). 💰
382. 🟡 Create custom validators for PAN, IFSC and Indian mobile numbers. 💰
383. 🟡 Create an async validator to check whether a username exists.
384. 🟡 Create a dynamic `FormArray` for adding multiple nominees.
385. 🟡 Implement search-as-you-type with `debounceTime`, `distinctUntilChanged` and `switchMap`.
386. 🟡 Implement file upload with a progress bar.
387. 🟡 Implement a PDF/Excel download from a .NET API. 💰
388. 🟡 Lazy load a feature route with `loadComponent` and `loadChildren`.
389. 🟡 Use `@defer (on viewport)` to lazy load a heavy chart component.
390. 🟡 Build a simple state store with signals (add, remove, total).
391. 🔴 Implement token refresh in an interceptor with a single refresh call for concurrent 401s.
392. 🔴 Implement a custom form control (`ControlValueAccessor`) for an amount input that formats on blur. 💰
393. 🔴 Implement an inactivity timer that warns at 4 minutes and logs out at 5 minutes. 💰
394. 🔴 Implement real-time balance updates using SignalR. 💰

---

## 33. Machine Coding Problems

395. 🟡 Build a todo app with add/edit/delete/filter using signals.
396. 🟡 Build a paginated, sortable, filterable data table (Angular Material or custom) connected to a .NET API. 💰
397. 🟡 Build a multi-step form wizard (e.g., account opening / KYC) with validation per step and draft save. 💰
398. 🟡 Build a dashboard with cards and charts that load lazily with `@defer`.
399. 🟡 Build a login page with JWT authentication, guards and an interceptor.
400. 🟡 Build a typeahead/autocomplete component.
401. 🟡 Build a modal dialog service (open, close, return result).
402. 🟡 Build an infinite scroll / virtual scroll transaction list. 💰
403. 🔴 Build a fund transfer flow: select account → enter beneficiary and amount → OTP verification → confirmation, preventing double submission. 💰
404. 🔴 Build a role-based menu where items are shown based on permissions from the API.

---

## 34. Scenario-Based Questions

405. 🟡 Your Angular app's initial load is very slow (5 MB bundle). How do you reduce it?
406. 🟡 A page with a large table is laggy when typing in a search box. How do you fix it?
407. 🟡 The app's memory usage keeps increasing as users navigate. How do you find and fix leaks?
408. 🟡 After login, multiple API calls fail with 401 when the token expires. How do you handle refresh?
409. 🟡 A user double-clicks the "Transfer" button and two transfers are sent. How do you prevent it on the Angular side (and why must the API also prevent it)? 💰
410. 🟡 Dates shown in the UI are one day behind for some users. How do you fix it? 💰
411. 🟡 Amounts like 0.1 + 0.2 show rounding errors in totals. How do you handle money in Angular? 💰
412. 🟡 Deep links return 404 after deploying to Nginx. How do you fix it?
413. 🟡 Users see an old version after deployment. How do you fix caching?
414. 🟡 The same API endpoint is called multiple times on one page. How do you fix it?
415. 🟡 You must display validation errors returned from an ASP.NET Core API next to form fields. How?
416. 🟡 Your app must work with different API URLs in dev, UAT and production without rebuilding. How?
417. 🟡 A security scan reports XSS through `[innerHTML]` with `bypassSecurityTrustHtml`. How do you fix it?
418. 🟡 You need to show real-time transaction notifications. Which approach do you choose (SignalR, SSE, polling)? 💰
419. 🟡 Users opening the app in multiple tabs should be logged out from all tabs when they log out in one. How? 💰
420. 🟡 A form with 100 fields is slow to validate and render. How do you optimise it?
421. 🔴 Your team wants to migrate from NgModules + Zone.js to standalone + signals + zoneless. What is your migration plan?
422. 🔴 Your company wants to split a large banking portal into micro-frontends owned by different teams. How do you approach it? 💰
423. 🔴 Your app must store tokens securely; the security team doesn't allow tokens in localStorage. What architecture do you propose (BFF with cookies)? 💰
424. 🔴 An `effect` causes an infinite loop and the browser freezes. How do you debug and fix it?

---

## 35. Rapid-Fire Round

425. 🟢 Which decorator defines a component?
426. 🟢 Which CLI command creates a new component?
427. 🟢 Which directive is used for two-way binding in template forms?
428. 🟢 Which lifecycle hook runs once after the first `ngOnChanges`?
429. 🟢 Which lifecycle hook is used for cleanup?
430. 🟢 Which pipe subscribes to observables automatically?
431. 🟢 Which tag displays routed components?
432. 🟢 Which service is used for HTTP calls?
433. 🟡 Which control flow block requires `track`?
434. 🟡 Which block lazily loads part of a template?
435. 🟡 Which function creates a derived signal?
436. 🟡 Which function converts an observable to a signal?
437. 🟡 Which RxJS operator cancels the previous inner observable?
438. 🟡 Which RxJS operator ignores new emissions while one is in progress?
439. 🟡 Which Subject type requires an initial value?
440. 🟡 Which change detection strategy checks a component only on input reference changes, events or signals?
441. 🟡 Which guard type warns before leaving a page?
442. 🟡 Which route property lazy loads a standalone component?
443. 🟡 Which form method returns values including disabled controls?
444. 🟡 Which interface creates a custom form control?
445. 🟡 Which Nginx directive supports Angular deep links?
446. 🔴 What is the difference between `setValue` and `patchValue` in one line?
447. 🔴 What is the difference between `@ViewChild` and `@ContentChild` in one line?
448. 🔴 What is the difference between `switchMap` and `mergeMap` in one line?
449. 🔴 What is the difference between pure and impure pipes in one line?
450. 🔴 What is the difference between `canActivate` and `canMatch` in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS · Part 14 — JavaScript · Part 15 — jQuery & AJAX · Part 16 — Angular.
