# 🎯 JavaScript Interview Questions — Part 14 (Questions Only)

> **Level:** ~4 years of experience.
> **Scope:** Core JavaScript language (types, coercion, scope, hoisting, closures, `this`, prototypes, classes), functions, objects & arrays, ES6–ES2025 features, asynchronous JavaScript (callbacks, promises, async/await, event loop, microtasks), error handling, modules, memory & garbage collection, DOM & events, browser APIs & storage, networking (fetch, CORS, WebSockets), performance, security (XSS, CSRF, CSP), design patterns, functional programming, testing, a short Node.js section, a short TypeScript section, **predict-the-output snippets**, **coding / machine-coding problems** and **scenario-based questions**.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents
1. JavaScript Fundamentals
2. Data Types & Type Coercion
3. Variables, Scope & Hoisting
4. Functions
5. Closures
6. The `this` Keyword, `call`, `apply`, `bind`
7. Objects
8. Prototypes & Inheritance
9. Classes
10. Arrays & Array Methods
11. Strings, Numbers, Dates & Math
12. ES6+ Features (ES2015 → ES2025)
13. Iterators, Generators, Symbols, Map/Set, WeakMap/WeakSet, Proxy/Reflect
14. Asynchronous JavaScript — Callbacks & Promises
15. Async/Await
16. The Event Loop, Microtasks & Macrotasks
17. Error Handling
18. Modules
19. Memory Management & Garbage Collection
20. DOM Manipulation
21. Events, Bubbling, Capturing & Delegation
22. Browser APIs & Storage
23. Networking — Fetch, AJAX, CORS, WebSockets, SSE
24. Performance Optimization
25. Security
26. Functional Programming in JavaScript
27. Design Patterns in JavaScript
28. Testing JavaScript
29. Node.js Basics
30. TypeScript Basics
31. Tricky Questions
32. Predict the Output
33. Coding Problems — Implement From Scratch (Polyfills)
34. Coding Problems — Logic & Data Structures
35. Machine Coding Problems
36. Scenario-Based Questions
37. Rapid-Fire Round

---

## 1. JavaScript Fundamentals

1. 🟢 What is JavaScript? Is it compiled or interpreted?
2. 🟢 What is ECMAScript? How is it related to JavaScript?
3. 🟢 What is a JavaScript engine (V8, SpiderMonkey, JavaScriptCore)?
4. 🟡 How does a JS engine execute code (parsing, AST, interpreter, JIT compilation)?
5. 🟢 Is JavaScript single-threaded? How does it handle concurrency?
6. 🟢 What is the difference between JavaScript in the browser and Node.js?
7. 🟢 What is strict mode (`"use strict"`)? What does it change?
8. 🟢 What is the difference between `==` and `===`?
9. 🟡 What is `Object.is()`? How is it different from `===`?
10. 🟡 What is the execution context? What are the global and function execution contexts?
11. 🟡 What is the call stack?
12. 🟡 What are the creation and execution phases of an execution context?
13. 🟡 What is a lexical environment?
14. 🟢 What is the difference between an expression and a statement?
15. 🟢 What is the difference between `null` and `undefined`?
16. 🟢 What is `NaN`? How do you check for it (`Number.isNaN` vs `isNaN`)?

---

## 2. Data Types & Type Coercion

17. 🟢 What are the primitive data types in JavaScript?
18. 🟢 What is the difference between primitive and reference types?
19. 🟢 What does `typeof` return for each type? What is `typeof null`, `typeof []`, `typeof function(){}`, `typeof NaN`?
20. 🟡 How do you reliably check if a value is an array (`Array.isArray`)? An object? A plain object?
21. 🟡 What is `BigInt`? When do you need it? 💰
22. 🟡 What is type coercion? Implicit vs explicit coercion?
23. 🟡 How does the `+` operator behave with strings and numbers?
24. 🟡 What are truthy and falsy values? List all falsy values.
25. 🟡 How does `==` coercion work (abstract equality algorithm)?
26. 🟡 What does `ToPrimitive` do? What are `valueOf` and `toString` used for in coercion?
27. 🟡 What is `Symbol.toPrimitive`?
28. 🟡 What is the difference between `parseInt`, `parseFloat`, `Number()` and unary `+`?
29. 🟡 Why does `parseInt("08")` or `parseInt(0.0000005)` give surprising results?
30. 🟡 Why is `0.1 + 0.2 !== 0.3`? How do you handle money in JavaScript? 💰
31. 🟡 What is `Number.EPSILON`, `Number.MAX_SAFE_INTEGER` and `Number.isSafeInteger`?
32. 🔴 Why can large IDs or amounts from a JSON API lose precision in JavaScript? How do you prevent it? 💰

---

## 3. Variables, Scope & Hoisting

33. 🟢 What is the difference between `var`, `let` and `const`?
34. 🟢 Can you change the contents of a `const` object or array?
35. 🟢 What is scope? What are global, function and block scope?
36. 🟡 What is lexical scope?
37. 🟡 What is the scope chain?
38. 🟢 What is hoisting? Are `let` and `const` hoisted?
39. 🟡 What is the Temporal Dead Zone (TDZ)?
40. 🟡 How are function declarations vs function expressions hoisted?
41. 🟡 What is variable shadowing? What is illegal shadowing?
42. 🟡 What happens when you assign to an undeclared variable in non-strict vs strict mode?
43. 🟡 What is `globalThis`?
44. 🔴 Why does `var` in a `for` loop with `setTimeout` print the same value? How do `let` or closures fix it?

---

## 4. Functions

45. 🟢 What are the different ways to define a function?
46. 🟢 What is the difference between a function declaration and a function expression?
47. 🟢 What are arrow functions? How are they different from regular functions (`this`, `arguments`, `new`, `prototype`)?
48. 🟡 When should you NOT use an arrow function?
49. 🟢 What are first-class functions?
50. 🟢 What are higher-order functions? Give examples.
51. 🟢 What is a callback function?
52. 🟡 What is an IIFE? Why was it used?
53. 🟡 What are default parameters? What are rest parameters?
54. 🟡 What is the `arguments` object? How is it different from rest parameters?
55. 🟡 What is a pure function? What are side effects?
56. 🟡 What is currying? Write a curry function.
57. 🟡 What is partial application?
58. 🟡 What is function composition (`compose`, `pipe`)?
59. 🟡 What is memoization? Write a memoize function.
60. 🟡 What is recursion? What is tail call optimisation (and is it supported)?
61. 🟡 What is a constructor function? What does `new` do step by step?
62. 🟡 What is `new.target`?
63. 🟡 What is function length (`fn.length`)?
64. 🔴 What are debouncing and throttling? What is the difference? Give use cases.

---

## 5. Closures

65. 🟢 What is a closure?
66. 🟡 Give a practical use case of closures (data privacy, counters, memoization, once, module pattern).
67. 🟡 How do closures relate to lexical scope?
68. 🟡 What is the module pattern using closures?
69. 🟡 Write a function `once(fn)` that allows `fn` to run only once.
70. 🟡 Write a counter with private state using a closure.
71. 🟡 Can closures cause memory leaks? How?
72. 🔴 How do closures behave inside loops with `var` vs `let`?
73. 🔴 What are stale closures (e.g., in React hooks) and why do they happen?

---

## 6. The `this` Keyword, `call`, `apply`, `bind`

74. 🟢 What is `this` in JavaScript?
75. 🟡 What are the rules for determining `this` (default, implicit, explicit, `new`, arrow functions)?
76. 🟡 What is `this` in the global scope, in a function, in a method, in strict mode?
77. 🟡 What is `this` inside an arrow function?
78. 🟡 What is `this` in an event handler?
79. 🟡 What is `this` in a class method passed as a callback? How do you fix lost `this`?
80. 🟢 What are `call`, `apply` and `bind`? What are the differences?
81. 🟡 Can you re-bind a function that's already bound?
82. 🟡 What is method borrowing?
83. 🔴 What is the precedence order of `this` binding rules?

---

## 7. Objects

84. 🟢 What are the ways to create an object?
85. 🟢 What is the difference between dot notation and bracket notation?
86. 🟢 How do you check if a property exists (`in`, `hasOwnProperty`, `Object.hasOwn`)?
87. 🟢 How do you iterate over an object (`for...in`, `Object.keys`, `Object.values`, `Object.entries`)?
88. 🟡 What is the difference between `for...in` and `for...of`?
89. 🟡 What is shallow copy vs deep copy? How do you do each (`spread`, `Object.assign`, `structuredClone`, JSON methods)?
90. 🟡 What are the limitations of `JSON.parse(JSON.stringify(obj))` for deep copying?
91. 🟡 What do `Object.freeze`, `Object.seal` and `Object.preventExtensions` do? Is freeze deep?
92. 🟡 What are property descriptors (`writable`, `enumerable`, `configurable`)? What is `Object.defineProperty`?
93. 🟡 What are getters and setters?
94. 🟡 What are computed property names and shorthand properties/methods?
95. 🟡 What is `Object.fromEntries`?
96. 🟡 How do you compare two objects for equality (deep equal)?
97. 🟡 What is optional chaining (`?.`) and nullish coalescing (`??`)? How is `??` different from `||`?
98. 🟡 What are the logical assignment operators (`||=`, `&&=`, `??=`)?
99. 🔴 What is the order of keys in `Object.keys` (integer keys first)?

---

## 8. Prototypes & Inheritance

100. 🟢 What is a prototype?
101. 🟡 What is the prototype chain?
102. 🟡 What is the difference between `__proto__` and `prototype`?
103. 🟡 What is `Object.create()`? How do you create an object without a prototype (`Object.create(null)`)?
104. 🟡 How does prototypal inheritance differ from classical inheritance?
105. 🟡 How do you implement inheritance with constructor functions?
106. 🟡 What is `Object.getPrototypeOf` and `Object.setPrototypeOf`? Why is changing prototypes slow?
107. 🟡 What does `instanceof` check? How can it be fooled?
108. 🟡 What is `isPrototypeOf`?
109. 🔴 Why is extending built-in prototypes (e.g., `Array.prototype.myMethod`) considered bad practice?

---

## 9. Classes

110. 🟢 What are classes in JavaScript? Are they "real" classes?
111. 🟢 What are constructors, methods, `extends` and `super`?
112. 🟡 What are static methods and static properties?
113. 🟡 What are private fields and methods (`#field`)? How are they different from closure-based privacy?
114. 🟡 What are class fields (public instance fields)?
115. 🟡 What are static initialization blocks?
116. 🟡 What are getters and setters in classes?
117. 🟡 Are classes hoisted?
118. 🟡 What happens if you forget to call `super()` in a derived class constructor?
119. 🔴 What is the difference between a method defined in the class body and an arrow function class field (memory, `this`)?
120. 🔴 What are mixins? How do you implement them?

---

## 10. Arrays & Array Methods

121. 🟢 What are the common array methods (`push`, `pop`, `shift`, `unshift`, `slice`, `splice`, `concat`, `join`, `indexOf`, `includes`)?
122. 🟢 What is the difference between `slice` and `splice`?
123. 🟢 What do `map`, `filter`, `reduce`, `forEach`, `find`, `findIndex`, `some`, `every` do?
124. 🟡 What is the difference between `map` and `forEach`?
125. 🟡 Can you break out of a `forEach`? What are the alternatives?
126. 🟡 How does `reduce` work? Give 5 different use cases (sum, group by, flatten, count, pipe).
127. 🟡 What do `flat` and `flatMap` do?
128. 🟡 What do `findLast`, `findLastIndex` and `at()` do?
129. 🟡 What are the immutable array methods `toSorted`, `toReversed`, `toSpliced`, `with` (ES2023)?
130. 🟡 What is `Object.groupBy` / `Map.groupBy` (ES2024)?
131. 🟡 How does the default `sort()` work? Why does `[10, 9, 1].sort()` give `[1, 10, 9]`?
132. 🟡 Is `sort` stable in JavaScript?
133. 🟡 Which array methods mutate the original array?
134. 🟡 How do you remove duplicates from an array?
135. 🟡 What is `Array.from` and `Array.of`?
136. 🟡 What are array-like objects? How do you convert them to arrays?
137. 🟡 What are sparse arrays / holes?
138. 🟡 What is array destructuring? How do you swap two variables?
139. 🔴 What is the time complexity of `shift`/`unshift` vs `push`/`pop`?
140. 🔴 What are typed arrays (`Uint8Array`, `ArrayBuffer`)?

---

## 11. Strings, Numbers, Dates & Math

141. 🟢 Are strings mutable in JavaScript?
142. 🟢 What are template literals? What are tagged templates?
143. 🟡 What do `slice`, `substring` and `substr` do? What's the difference?
144. 🟡 What do `padStart`, `padEnd`, `trimStart`, `trimEnd`, `replaceAll`, `at` do?
145. 🟡 How do you reverse a string? What breaks with emojis (Unicode surrogate pairs)?
146. 🟡 What is `localeCompare` and `Intl.Collator`?
147. 🟡 How do you format numbers and currency (`Intl.NumberFormat`, `toFixed`)? What are the rounding pitfalls of `toFixed`? 💰
148. 🟡 How do you format amounts in Indian numbering (lakhs, crores) using `Intl.NumberFormat('en-IN')`? 💰
149. 🟡 What are the problems with the `Date` object (months start at 0, time zones, parsing)?
150. 🟡 How do you handle time zones in JavaScript (`Intl.DateTimeFormat`, UTC methods, libraries like date-fns/Luxon/Day.js)?
151. 🟡 What is the Temporal API?
152. 🟡 How do you generate a random number in a range? Is `Math.random` secure? What is `crypto.getRandomValues` / `crypto.randomUUID`?

---

## 12. ES6+ Features (ES2015 → ES2025)

153. 🟢 What are the major ES6 (ES2015) features?
154. 🟢 What is destructuring (objects and arrays)? What are default values and renaming?
155. 🟢 What is the spread operator vs the rest operator?
156. 🟡 What are enhanced object literals?
157. 🟡 What features were added in ES2016–ES2020 (`includes`, `**`, `async/await`, `Object.entries`, rest/spread for objects, `Promise.finally`, optional catch binding, `flat`, `BigInt`, `?.`, `??`, `Promise.allSettled`, dynamic `import()`, `globalThis`)?
158. 🟡 What features were added in ES2021–ES2023 (`replaceAll`, `Promise.any`, logical assignment, numeric separators, `WeakRef`, `at()`, `Object.hasOwn`, top-level await, class fields, `findLast`, `toSorted`)?
159. 🟡 What features were added in ES2024–ES2025 (`Object.groupBy`, `Promise.withResolvers`, `Array.fromAsync`, `Set` methods like `union`/`intersection`, iterator helpers, `RegExp` `v` flag, `Promise.try`, JSON modules)?
160. 🟡 What are numeric separators (`1_000_000`)?
161. 🟡 What is `Promise.withResolvers()`?
162. 🔴 How does transpilation (Babel, TypeScript) and polyfilling help use modern features in older browsers?

---

## 13. Iterators, Generators, Symbols, Map/Set, WeakMap/WeakSet, Proxy/Reflect

163. 🟡 What is the iterator protocol and the iterable protocol?
164. 🟡 How do you make a custom object iterable (`Symbol.iterator`)?
165. 🟡 What is a generator function (`function*`, `yield`)?
166. 🟡 What are use cases of generators (lazy sequences, infinite sequences, async flows)?
167. 🟡 What are async iterators and `for await...of`?
168. 🟡 What is a `Symbol`? What are well-known symbols?
169. 🟢 What is a `Map`? How is it different from an object?
170. 🟢 What is a `Set`? How is it different from an array?
171. 🟡 What are `WeakMap` and `WeakSet`? Why can't you iterate them? Give use cases.
172. 🟡 What is `WeakRef` and `FinalizationRegistry`?
173. 🟡 What is a `Proxy`? Give use cases (validation, logging, reactivity).
174. 🟡 What is `Reflect`? Why is it used with `Proxy`?
175. 🔴 How do frameworks like Vue use `Proxy` for reactivity?

---

## 14. Asynchronous JavaScript — Callbacks & Promises

176. 🟢 What is synchronous vs asynchronous code?
177. 🟢 What is callback hell? How do you avoid it?
178. 🟢 What is a Promise? What are its states?
179. 🟢 What do `then`, `catch` and `finally` do?
180. 🟡 What is promise chaining? What does returning a value vs a promise inside `then` do?
181. 🟡 What happens if you throw inside a `then`?
182. 🟡 What is the difference between `Promise.all`, `Promise.allSettled`, `Promise.race` and `Promise.any`?
183. 🟡 What happens to `Promise.all` if one promise rejects? Are the others cancelled?
184. 🟡 What is `Promise.resolve` and `Promise.reject`?
185. 🟡 What is an unhandled promise rejection? How do you catch them globally (`unhandledrejection`)?
186. 🟡 How do you convert a callback-based function into a promise (promisify)?
187. 🟡 Are promises eager or lazy?
188. 🔴 How do you cancel a promise / fetch request (`AbortController`)?
189. 🔴 How do you run promises sequentially vs in parallel vs with limited concurrency?
190. 🔴 How do you implement a timeout for a promise?

---

## 15. Async/Await

191. 🟢 What is `async/await`? How does it relate to promises?
192. 🟢 What does an `async` function always return?
193. 🟡 How do you handle errors with `async/await`?
194. 🟡 What is the difference between `await` in a loop and `Promise.all`?
195. 🟡 Why doesn't `await` work inside `forEach` as expected?
196. 🟡 What is top-level `await`? Where can it be used?
197. 🟡 What happens if you forget `await` before a promise?
198. 🟡 How do you run two async operations in parallel and wait for both?
199. 🔴 What is the performance impact of unnecessary `await` (sequential waterfalls)?
200. 🔴 How do you implement retry with exponential backoff using `async/await`?

---

## 16. The Event Loop, Microtasks & Macrotasks

201. 🟢 What is the event loop?
202. 🟡 What are the call stack, Web APIs, callback (task) queue and microtask queue?
203. 🟡 What are macrotasks? Give examples (`setTimeout`, `setInterval`, I/O, UI events, `MessageChannel`).
204. 🟡 What are microtasks? Give examples (promise callbacks, `queueMicrotask`, `MutationObserver`).
205. 🟡 Which runs first — microtasks or macrotasks? When does the microtask queue get drained?
206. 🟡 Why doesn't `setTimeout(fn, 0)` run immediately?
207. 🟡 What is `requestAnimationFrame`? Where does it fit in the event loop?
208. 🟡 What is `requestIdleCallback`?
209. 🟡 Can microtasks starve the event loop? How?
210. 🟡 What blocks the main thread? How does it affect UI responsiveness?
211. 🟡 How is the Node.js event loop different from the browser event loop (phases, `process.nextTick`, `setImmediate`)?
212. 🔴 What is the order of `process.nextTick`, promise callbacks, `setTimeout` and `setImmediate` in Node.js?
213. 🔴 What are Web Workers? How do they help with CPU-heavy tasks? What can't they access?

---

## 17. Error Handling

214. 🟢 How does `try...catch...finally` work?
215. 🟢 What are the built-in error types (`Error`, `TypeError`, `ReferenceError`, `SyntaxError`, `RangeError`)?
216. 🟡 How do you create a custom error class?
217. 🟡 What is `error.cause` (ES2022)?
218. 🟡 Can `try...catch` catch errors inside `setTimeout` callbacks?
219. 🟡 How do you catch errors in async code (promises, async/await)?
220. 🟡 What do `window.onerror` and `window.addEventListener('error')` catch?
221. 🟡 What is `AggregateError`?
222. 🔴 How do you design centralised error handling and logging for a front-end app (e.g., Sentry)?

---

## 18. Modules

223. 🟢 What are modules? Why do we need them?
224. 🟡 What is the difference between CommonJS (`require`, `module.exports`) and ES Modules (`import`, `export`)?
225. 🟡 What is the difference between named exports and default exports?
226. 🟡 What is dynamic `import()`? What is code splitting?
227. 🟡 Are ES modules loaded synchronously or asynchronously? Are imports live bindings?
228. 🟡 What is tree shaking? Why does it work better with ES modules?
229. 🟡 What is a circular dependency? How do CommonJS and ESM handle it?
230. 🟡 What are `type="module"` scripts in the browser? What are `defer` and `async` script attributes?
231. 🟡 What are bundlers (Webpack, Vite, Rollup, esbuild)? Why are they needed?
232. 🔴 What are import maps?

---

## 19. Memory Management & Garbage Collection

233. 🟡 How does garbage collection work in JavaScript (mark-and-sweep, generational GC)?
234. 🟡 What is a memory leak in JavaScript?
235. 🟡 What are common causes of memory leaks (global variables, forgotten timers, detached DOM nodes, closures, event listeners, unbounded caches)?
236. 🟡 How do you detect memory leaks using Chrome DevTools (heap snapshots, allocation timeline)?
237. 🟡 How do `WeakMap`/`WeakRef` help avoid leaks?
238. 🔴 What is the stack vs heap in JavaScript?

---

## 20. DOM Manipulation

239. 🟢 What is the DOM?
240. 🟢 How do you select elements (`getElementById`, `querySelector`, `querySelectorAll`)?
241. 🟡 What is the difference between `NodeList` and `HTMLCollection`? Which is live?
242. 🟡 What is the difference between `innerHTML`, `innerText` and `textContent`? Which is safer?
243. 🟡 How do you create, insert and remove elements?
244. 🟡 What is `DocumentFragment` and why is it faster?
245. 🟡 What are reflow (layout) and repaint? What causes them?
246. 🟡 What is layout thrashing? How do you avoid it?
247. 🟡 What are `data-*` attributes and `dataset`?
248. 🟡 What is the Shadow DOM? What are Web Components?
249. 🟡 What is the Virtual DOM? Is it faster than the real DOM?
250. 🟡 What are `MutationObserver`, `IntersectionObserver` and `ResizeObserver`? Give use cases.

---

## 21. Events, Bubbling, Capturing & Delegation

251. 🟢 What is an event? How do you add and remove event listeners?
252. 🟢 What is event bubbling? What is event capturing?
253. 🟡 What are the three phases of event propagation?
254. 🟡 What is the difference between `stopPropagation`, `stopImmediatePropagation` and `preventDefault`?
255. 🟡 What is event delegation? Why is it useful?
256. 🟡 What is the difference between `event.target` and `event.currentTarget`?
257. 🟡 What are passive event listeners? Why do they improve scroll performance?
258. 🟡 What does the `once` option in `addEventListener` do?
259. 🟡 What are custom events (`CustomEvent`, `dispatchEvent`)?
260. 🟡 Why does `removeEventListener` sometimes not work (different function reference)?
261. 🟡 What is the difference between `DOMContentLoaded` and `load`?
262. 🔴 Which events don't bubble (`focus`, `blur`, `mouseenter`)? How do you delegate them (`focusin`, `focusout`)?

---

## 22. Browser APIs & Storage

263. 🟢 What is the difference between `localStorage`, `sessionStorage` and cookies?
264. 🟡 What are the size limits of each storage type?
265. 🟡 Is it safe to store tokens in `localStorage`? Why or why not? 💰
266. 🟡 What is IndexedDB? When would you use it?
267. 🟡 What is the Cache API?
268. 🟡 What is a Service Worker? What can it do (offline, caching, push notifications)?
269. 🟡 What is a Progressive Web App (PWA)?
270. 🟡 What is the History API (`pushState`, `replaceState`, `popstate`)? How do SPAs use it for routing?
271. 🟡 What is the `storage` event?
272. 🟡 What is `BroadcastChannel` and `postMessage`?
273. 🟡 What is the Clipboard API, Geolocation API, Notification API?
274. 🟡 What is `navigator.sendBeacon`?
275. 🟡 What is `Blob`, `File`, `FileReader` and `URL.createObjectURL`?
276. 🔴 What is the Page Visibility API and how would you use it?

---

## 23. Networking — Fetch, AJAX, CORS, WebSockets, SSE

277. 🟢 What is AJAX? What is `XMLHttpRequest`?
278. 🟢 What is the Fetch API? How is it different from XHR and Axios?
279. 🟡 Does `fetch` reject on HTTP 404 or 500? How do you handle HTTP errors?
280. 🟡 How do you send JSON, form data and files with `fetch`?
281. 🟡 How do you send cookies with `fetch` (`credentials: 'include'`)?
282. 🟡 How do you cancel a `fetch` request (`AbortController`)? How do you implement a timeout (`AbortSignal.timeout`)?
283. 🟡 What is CORS? Why do you get CORS errors in the browser but not in Postman?
284. 🟡 What is a preflight request?
285. 🟡 How do you upload a file with progress?
286. 🟡 What are Axios interceptors? How do you implement token refresh with them?
287. 🟡 What are WebSockets? How do you use them in JavaScript?
288. 🟡 What are Server-Sent Events (`EventSource`)?
289. 🟡 WebSockets vs SSE vs long polling — when to use which?
290. 🔴 How do you handle race conditions when multiple requests return out of order (e.g., search-as-you-type)?
291. 🔴 How do you implement automatic retry and token refresh without duplicate refresh calls?

---

## 24. Performance Optimization

292. 🟡 How do you improve JavaScript performance in a web app?
293. 🟡 What are Core Web Vitals (LCP, INP, CLS)?
294. 🟡 What are lazy loading and code splitting?
295. 🟡 What are `defer` and `async` for scripts? Which one preserves order?
296. 🟡 What is debouncing and throttling used for in performance?
297. 🟡 What is virtualization (windowing) for long lists?
298. 🟡 How do you avoid blocking the main thread for heavy computations?
299. 🟡 What is minification, compression (gzip/brotli) and caching for JS bundles?
300. 🟡 How do you analyse bundle size (webpack-bundle-analyzer, source-map-explorer)?
301. 🟡 What is preloading, prefetching and preconnecting (`<link rel="preload">`)?
302. 🟡 How do you use the Performance tab and Lighthouse in Chrome DevTools?
303. 🔴 What is the cost of large `JSON.parse` / `JSON.stringify` operations?
304. 🔴 How do you optimise rendering a table with 1 lakh rows of transactions? 💰

---

## 25. Security

305. 🟢 What is XSS (Cross-Site Scripting)? What are stored, reflected and DOM-based XSS?
306. 🟡 How do you prevent XSS in JavaScript (escaping, `textContent`, sanitising with DOMPurify, CSP)?
307. 🟡 Why is `innerHTML` with user input dangerous? Why is `eval` dangerous?
308. 🟡 What is CSRF? How do you protect against it?
309. 🟡 What is Content Security Policy (CSP)?
310. 🟡 What is clickjacking?
311. 🟡 What is prototype pollution? How can it happen and how do you prevent it?
312. 🟡 Where should JWTs be stored in the browser? 💰
313. 🟡 What are `HttpOnly`, `Secure` and `SameSite` cookies?
314. 🟡 What is Subresource Integrity (SRI)?
315. 🟡 Why should you never put secrets or API keys in front-end code?
316. 🔴 What are supply chain attacks via npm packages and how do you reduce the risk (`npm audit`, lockfiles, pinning)?
317. 🔴 What are the risks of `postMessage` and how do you validate the origin?

---

## 26. Functional Programming in JavaScript

318. 🟡 What is functional programming?
319. 🟡 What is immutability and why is it important?
320. 🟡 What are pure functions and referential transparency?
321. 🟡 What are higher-order functions, currying and composition?
322. 🟡 What is point-free style?
323. 🟡 How do `map`, `filter` and `reduce` support functional programming?
324. 🔴 What are functors and monads in simple terms (e.g., arrays and promises)?

---

## 27. Design Patterns in JavaScript

325. 🟡 What is the module pattern?
326. 🟡 What is the revealing module pattern?
327. 🟡 What is the singleton pattern in JavaScript?
328. 🟡 What is the factory pattern?
329. 🟡 What is the observer / pub-sub pattern? Implement an event emitter.
330. 🟡 What is the decorator pattern?
331. 🟡 What is the strategy pattern?
332. 🟡 What is the proxy pattern?
333. 🟡 What is the mediator pattern?
334. 🔴 What is dependency injection in JavaScript?

---

## 28. Testing JavaScript

335. 🟡 What are unit, integration and end-to-end tests in front-end development?
336. 🟡 What are Jest, Vitest, Mocha, Jasmine?
337. 🟡 What are Testing Library, Cypress and Playwright?
338. 🟡 How do you mock functions, modules and timers (`jest.fn`, `jest.mock`, fake timers)?
339. 🟡 How do you test asynchronous code?
340. 🟡 How do you mock `fetch` or API calls (MSW)?
341. 🟡 What is code coverage?
342. 🔴 What is snapshot testing and what are its drawbacks?

---

## 29. Node.js Basics

343. 🟢 What is Node.js? Why is it good for I/O-heavy applications?
344. 🟡 What is libuv?
345. 🟡 What is the Node.js event loop and its phases?
346. 🟡 What is the difference between `process.nextTick` and `setImmediate`?
347. 🟡 What are streams in Node.js? What are readable, writable, duplex and transform streams?
348. 🟡 What is a Buffer?
349. 🟡 What is `EventEmitter`?
350. 🟡 What are worker threads and the cluster module?
351. 🟡 What is `package.json`, `package-lock.json`, `npm`, `npx`, `pnpm`, `yarn`?
352. 🟡 What are dependencies vs devDependencies vs peerDependencies?
353. 🟡 What is semantic versioning (`^`, `~`)?
354. 🟡 What is Express? What is middleware in Express?
355. 🔴 Why does a CPU-heavy task block a Node.js server? How do you fix it?

---

## 30. TypeScript Basics

356. 🟢 What is TypeScript? Why use it over JavaScript?
357. 🟡 What is the difference between `interface` and `type`?
358. 🟡 What are `any`, `unknown`, `never` and `void`?
359. 🟡 What are union and intersection types?
360. 🟡 What are generics?
361. 🟡 What are utility types (`Partial`, `Required`, `Pick`, `Omit`, `Record`, `Readonly`, `ReturnType`)?
362. 🟡 What are type guards and type narrowing?
363. 🟡 What are enums? What are the alternatives (`as const` objects, union types)?
364. 🟡 What is `strict` mode in `tsconfig.json`?
365. 🔴 Does TypeScript provide runtime type safety? How do you validate API responses at runtime (Zod)?

---

## 31. Tricky Questions

366. 🟡 Why is `typeof null === "object"`?
367. 🟡 Why is `NaN !== NaN`?
368. 🟡 Why is `[] == ![]` true?
369. 🟡 Why is `[] + []` an empty string and `[] + {}` `"[object Object]"`?
370. 🟡 Why is `0.1 + 0.2 !== 0.3`?
371. 🟡 Why does `"5" - 3` give `2` but `"5" + 3` gives `"53"`?
372. 🟡 Why does `[1, 2, 3] + [4, 5]` give `"1,2,34,5"`?
373. 🟡 Why does `const` not make an object immutable?
374. 🟡 Why does an arrow function not have its own `this`?
375. 🟡 Why does `setTimeout(fn, 0)` run after `Promise.resolve().then(fn)`?
376. 🟡 Why does `await` inside `forEach` not wait?
377. 🟡 Why does `["1", "2", "3"].map(parseInt)` return `[1, NaN, NaN]`?
378. 🟡 Why does `Math.max()` return `-Infinity` and `Math.min()` return `Infinity`?
379. 🟡 Why does `fetch` not throw for a 500 response?
380. 🟡 Why can `JSON.stringify` lose data (`undefined`, functions, `Date`, `Map`, `BigInt`)?
381. 🟡 Why can two objects with the same properties not be equal with `===`?
382. 🟡 Why is `function` hoisted but `class` is not usable before declaration?
383. 🟡 Why does modifying an object passed to a function change the original?
384. 🟡 Is JavaScript pass-by-value or pass-by-reference?
385. 🔴 Why can `for...in` over an array give unexpected results?
386. 🔴 Why does `new Date("2025-01-01")` sometimes show December 31 in India/US? 💰
387. 🔴 Why can `toFixed(2)` give `1.00` for `1.005`? 💰

---

## 32. Predict the Output

> What is printed? Explain why.

**388. 🟢 Hoisting**
```js
console.log(a);
var a = 10;
console.log(b);
let b = 20;
```

**389. 🟢 Function hoisting**
```js
greet();
sayHi();
function greet() { console.log("hello"); }
var sayHi = function () { console.log("hi"); };
```

**390. 🟡 Closures in loops**
```js
for (var i = 0; i < 3; i++) setTimeout(() => console.log(i), 0);
for (let j = 0; j < 3; j++) setTimeout(() => console.log(j), 0);
```

**391. 🟡 Event loop order**
```js
console.log("1");
setTimeout(() => console.log("2"), 0);
Promise.resolve().then(() => console.log("3"));
queueMicrotask(() => console.log("4"));
console.log("5");
```

**392. 🔴 Nested microtasks and macrotasks**
```js
setTimeout(() => console.log("A"), 0);
Promise.resolve().then(() => {
  console.log("B");
  setTimeout(() => console.log("C"), 0);
  Promise.resolve().then(() => console.log("D"));
});
console.log("E");
```

**393. 🔴 async/await order**
```js
async function f() {
  console.log("1");
  await null;
  console.log("2");
}
console.log("3");
f();
console.log("4");
```

**394. 🟡 `this` in methods**
```js
const user = {
  name: "Asha",
  regular() { return this.name; },
  arrow: () => this?.name,
};
console.log(user.regular());
console.log(user.arrow());
const fn = user.regular;
console.log(fn());
```

**395. 🟡 `this` with setTimeout**
```js
const obj = {
  name: "Ravi",
  greet() { setTimeout(function () { console.log(this.name); }, 0); },
  greetArrow() { setTimeout(() => console.log(this.name), 0); },
};
obj.greet();
obj.greetArrow();
```

**396. 🟡 bind**
```js
function show() { return this.x; }
const a = { x: 1 };
const b = { x: 2 };
const bound = show.bind(a);
console.log(bound.call(b));
console.log(bound.bind(b)());
```

**397. 🟡 Coercion**
```js
console.log(1 + "2");
console.log("3" - 1);
console.log(true + 1);
console.log([] + {});
console.log({} + []);
console.log(null + 1);
console.log(undefined + 1);
console.log("5" * "2");
```

**398. 🟡 Equality**
```js
console.log(null == undefined);
console.log(null === undefined);
console.log(NaN == NaN);
console.log(Object.is(NaN, NaN));
console.log(0 == "");
console.log("0" == false);
console.log([] == false);
console.log(Object.is(0, -0));
```

**399. 🟡 typeof**
```js
console.log(typeof null);
console.log(typeof undefined);
console.log(typeof []);
console.log(typeof (() => {}));
console.log(typeof NaN);
console.log(typeof 10n);
console.log(typeof Symbol());
```

**400. 🟡 Object references**
```js
const a = { x: 1 };
const b = a;
b.x = 2;
const c = { ...a };
c.x = 3;
console.log(a.x, b.x, c.x);
```

**401. 🟡 Shallow copy**
```js
const orig = { n: 1, inner: { v: 1 } };
const copy = { ...orig };
copy.inner.v = 99;
console.log(orig.inner.v);
```

**402. 🟡 Function arguments**
```js
function change(obj, num) {
  obj.value = 100;
  obj = { value: 200 };
  num = 50;
}
const o = { value: 1 };
let n = 1;
change(o, n);
console.log(o.value, n);
```

**403. 🟡 Array methods**
```js
console.log(["1", "2", "3"].map(parseInt));
console.log([10, 1, 3].sort());
console.log([1, 2, 3].map(x => { x * 2 }));
console.log([1, 2, 3, 4].filter((x, i) => i % 2));
```

**404. 🟡 reduce without initial value**
```js
console.log([1, 2, 3].reduce((a, b) => a + b));
console.log([].reduce((a, b) => a + b));
```

**405. 🟡 Closure counter**
```js
function counter() {
  let count = 0;
  return { inc: () => ++count, get: () => count };
}
const c1 = counter();
const c2 = counter();
c1.inc(); c1.inc(); c2.inc();
console.log(c1.get(), c2.get());
```

**406. 🟡 TDZ**
```js
let x = 1;
{
  console.log(x);
  let x = 2;
}
```

**407. 🟡 Default parameters**
```js
function f(a, b = a * 2, c = a + b) { return [a, b, c]; }
console.log(f(1));
console.log(f(1, undefined, 5));
console.log(f(1, null));
```

**408. 🟡 Promise chaining**
```js
Promise.resolve(1)
  .then(x => x + 1)
  .then(x => { throw new Error("boom " + x); })
  .then(x => console.log("never", x))
  .catch(e => { console.log(e.message); return 10; })
  .then(x => console.log("after catch", x))
  .finally(() => console.log("finally"));
```

**409. 🟡 Promise.all vs allSettled**
```js
const p1 = Promise.resolve(1);
const p2 = Promise.reject("fail");
const p3 = new Promise(r => setTimeout(() => r(3), 100));
Promise.all([p1, p2, p3]).then(console.log).catch(e => console.log("all:", e));
Promise.allSettled([p1, p2, p3]).then(r => console.log(r.map(x => x.status)));
Promise.any([p2, p3]).then(v => console.log("any:", v));
Promise.race([p3, p1]).then(v => console.log("race:", v));
```

**410. 🟡 await in forEach**
```js
const delay = (ms, v) => new Promise(r => setTimeout(() => r(v), ms));
async function run() {
  [3, 1, 2].forEach(async n => {
    await delay(n * 100);
    console.log(n);
  });
  console.log("done");
}
run();
```

**411. 🔴 Promise constructor is synchronous**
```js
console.log("start");
new Promise(resolve => {
  console.log("inside");
  resolve();
  console.log("after resolve");
}).then(() => console.log("then"));
console.log("end");
```

**412. 🟡 Prototype chain**
```js
function Animal(name) { this.name = name; }
Animal.prototype.speak = function () { return this.name + " speaks"; };
const dog = new Animal("Tommy");
console.log(dog.speak());
console.log(dog.hasOwnProperty("speak"));
console.log("speak" in dog);
console.log(Object.getPrototypeOf(dog) === Animal.prototype);
```

**413. 🟡 Class fields and methods**
```js
class Btn {
  label = "OK";
  arrow = () => this.label;
  method() { return this.label; }
}
const b = new Btn();
const { arrow, method } = b;
console.log(arrow());
console.log(method());
```

**414. 🟡 Getter**
```js
const account = {
  _balance: 100,
  get balance() { return this._balance + " INR"; },
};
account.balance = 500;
console.log(account.balance);
```

**415. 🟡 Object.freeze**
```js
"use strict";
const cfg = Object.freeze({ env: "prod", db: { host: "a" } });
cfg.db.host = "b";
console.log(cfg.db.host);
cfg.env = "dev";
```

**416. 🟡 Optional chaining and nullish**
```js
const u = { profile: { age: 0, name: "" } };
console.log(u.profile?.age || 18);
console.log(u.profile?.age ?? 18);
console.log(u.address?.city ?? "NA");
console.log(u.profile.name || "Anonymous");
console.log(u.profile.name ?? "Anonymous");
```

**417. 🟡 Floating point**
```js
console.log(0.1 + 0.2);
console.log((0.1 + 0.2).toFixed(2));
console.log(1.005.toFixed(2));
console.log(9007199254740993);
console.log(9007199254740993n);
```

**418. 🟡 String methods**
```js
const s = "hello";
s[0] = "H";
console.log(s);
console.log(s.at(-1));
console.log("a-b-c".split("-", 2));
console.log("abc".padStart(5, "*"));
```

**419. 🟡 Spread and Set**
```js
console.log([...new Set([1, 2, 2, 3, 1])]);
console.log(Math.max(...[]));
console.log([..."hey"]);
```

**420. 🟡 Destructuring**
```js
const { a = 1, b: { c } = { c: 5 } } = { a: undefined };
console.log(a, c);
const [x, , y = 10, ...rest] = [1, 2, undefined, 4, 5];
console.log(x, y, rest);
```

**421. 🟡 Variable shadowing with var**
```js
var name = "global";
function test() {
  console.log(name);
  var name = "local";
  console.log(name);
}
test();
```

**422. 🔴 Generator**
```js
function* gen() {
  const x = yield 1;
  console.log("received", x);
  yield x * 2;
}
const g = gen();
console.log(g.next().value);
console.log(g.next(5).value);
console.log(g.next().done);
```

**423. 🔴 Map vs object keys**
```js
const obj = {};
const k1 = { id: 1 }, k2 = { id: 2 };
obj[k1] = "first";
obj[k2] = "second";
console.log(obj[k1]);
const m = new Map([[k1, "first"], [k2, "second"]]);
console.log(m.get(k1));
```

**424. 🔴 Object key order**
```js
const o = { b: 1, 2: "two", a: 3, 1: "one" };
console.log(Object.keys(o));
```

**425. 🟡 Event delegation target**
```html
<ul id="list"><li><span>Item</span></li></ul>
<script>
document.getElementById("list").addEventListener("click", e => {
  console.log(e.target.tagName, e.currentTarget.tagName);
});
// user clicks on the word "Item"
</script>
```

**426. 🔴 fetch error handling**
```js
fetch("/api/not-found")      // server returns 404
  .then(res => { console.log("ok?", res.ok); return res.json(); })
  .then(data => console.log("data", data))
  .catch(err => console.log("caught", err.message));
```

---

## 33. Coding Problems — Implement From Scratch (Polyfills)

427. 🟡 Implement `Array.prototype.map`.
428. 🟡 Implement `Array.prototype.filter`.
429. 🟡 Implement `Array.prototype.reduce` (with and without initial value).
430. 🟡 Implement `Array.prototype.forEach`, `find`, `some`, `every`.
431. 🟡 Implement `Array.prototype.flat` (with depth).
432. 🟡 Implement `Function.prototype.call`, `apply` and `bind`.
433. 🟡 Implement `Promise.all`.
434. 🟡 Implement `Promise.allSettled`, `Promise.race` and `Promise.any`.
435. 🔴 Implement a basic `Promise` class (with `then`, `catch`, chaining).
436. 🟡 Implement `debounce` (with leading/trailing options).
437. 🟡 Implement `throttle`.
438. 🟡 Implement `memoize`.
439. 🟡 Implement `curry` for any number of arguments (`sum(1)(2)(3)` and `sum(1, 2)(3)`).
440. 🟡 Implement infinite currying `sum(1)(2)(3)...()`.
441. 🟡 Implement `compose` and `pipe`.
442. 🟡 Implement `once`.
443. 🟡 Implement a deep clone function (handling arrays, objects, Dates, circular references).
444. 🟡 Implement deep equality check.
445. 🟡 Implement `Object.assign` and `structuredClone`-like copy.
446. 🟡 Implement `JSON.stringify` (simplified).
447. 🟡 Implement an `EventEmitter` (`on`, `off`, `emit`, `once`).
448. 🟡 Implement `setInterval` using `setTimeout`.
449. 🟡 Implement `sleep(ms)` / `delay`.
450. 🟡 Implement `promisify`.
451. 🔴 Implement a function that runs async tasks with a concurrency limit.
452. 🔴 Implement retry with exponential backoff for an async function.
453. 🔴 Implement a promise with timeout.
454. 🔴 Implement `getElementsByClassName` / a simple `querySelector`.
455. 🔴 Implement `instanceof`.
456. 🔴 Implement `new` operator as a function.
457. 🔴 Implement `Object.create`.
458. 🔴 Implement an LRU cache in JavaScript.

---

## 34. Coding Problems — Logic & Data Structures

459. 🟢 Reverse a string. Reverse words in a sentence.
460. 🟢 Check if a string is a palindrome.
461. 🟢 Check if two strings are anagrams.
462. 🟢 Find the first non-repeating character in a string.
463. 🟢 Count the frequency of each character / word.
464. 🟢 Remove duplicates from an array (3 ways).
465. 🟢 Find the largest and second largest number in an array.
466. 🟢 FizzBuzz.
467. 🟡 Flatten a nested array without `flat()`.
468. 🟡 Flatten a nested object into dot-notation keys (`{a: {b: 1}}` → `{"a.b": 1}`).
469. 🟡 Unflatten a dot-notation object.
470. 🟡 Group an array of objects by a property (without `Object.groupBy`).
471. 🟡 Find the intersection and union of two arrays.
472. 🟡 Chunk an array into groups of size N.
473. 🟡 Rotate an array by K positions.
474. 🟡 Two Sum.
475. 🟡 Find the missing number in an array of 1..N.
476. 🟡 Move all zeros to the end.
477. 🟡 Check balanced parentheses.
478. 🟡 Find the longest substring without repeating characters.
479. 🟡 Implement binary search.
480. 🟡 Sort an array of objects by multiple keys.
481. 🟡 Convert a string to title case / camelCase / snake_case.
482. 🟡 Deep get with a path string (`get(obj, "a.b[0].c")`).
483. 🟡 Compare two version strings (`"1.2.10"` vs `"1.10.2"`).
484. 🟡 Format a number as Indian currency without `Intl` (`1234567.5` → `₹12,34,567.50`). 💰
485. 🟡 Calculate the total balance and running balance from a list of transactions. 💰
486. 🔴 Implement a function that returns all permutations of an array.
487. 🔴 Implement a trie for autocomplete.
488. 🔴 Find the maximum profit from a list of stock prices (buy once, sell once). 💰

---

## 35. Machine Coding Problems

489. 🟡 Build a todo list with add, edit, delete, filter (all/active/completed) using vanilla JS.
490. 🟡 Build a search-as-you-type input with debouncing and cancellation of stale requests.
491. 🟡 Build an infinite scroll list using `IntersectionObserver`.
492. 🟡 Build a modal/dialog with focus trapping and close on Escape.
493. 🟡 Build a tabs component and an accordion component.
494. 🟡 Build a star rating component.
495. 🟡 Build a countdown timer / stopwatch.
496. 🟡 Build a paginated, sortable, filterable data table. 💰
497. 🟡 Build a form with validation (email, mobile, PAN, amount limits). 💰
498. 🟡 Build an image carousel with auto-play.
499. 🟡 Build a file upload with drag and drop and progress bar.
500. 🟡 Build a nested comments component (recursive rendering).
501. 🔴 Build a live stock price ticker using WebSockets with throttled UI updates. 💰
502. 🔴 Build a simple state management store (like a mini Redux) with subscribe/dispatch.
503. 🔴 Build a virtualized list that renders 1 lakh rows smoothly.
504. 🔴 Build an OTP input component (auto-focus next box, paste support). 💰

---

## 36. Scenario-Based Questions

505. 🟡 A page becomes unresponsive when a user uploads a large Excel file to be parsed in the browser. How do you fix it?
506. 🟡 A search box sends a request on every keystroke and results appear out of order. How do you fix it?
507. 🟡 Your SPA's memory usage keeps growing as users navigate between pages. How do you find and fix the leak?
508. 🟡 A button click handler fires twice. What could cause it?
509. 🟡 After login, the access token expires and multiple API calls fail at the same time. How do you refresh the token once and retry all of them?
510. 🟡 Users report incorrect totals in a transaction summary due to decimal rounding. How do you fix it? 💰
511. 🟡 Dates shown in the UI are one day off for some users. Why, and how do you fix it?
512. 🟡 Your bundle size is 5 MB and the first load is slow. How do you reduce it?
513. 🟡 A third-party script slows down your page. How do you limit its impact?
514. 🟡 You must show real-time balance updates without polling every second. What do you use? 💰
515. 🟡 A form must work offline and sync when the network returns. How do you design it?
516. 🟡 A security review found that user comments can execute scripts. How do you fix it?
517. 🟡 An API sometimes returns IDs larger than `Number.MAX_SAFE_INTEGER`. What problems occur and how do you fix them? 💰
518. 🟡 You need to call 50 APIs but only 5 at a time. How do you implement it?
519. 🟡 A long list of 10,000 items scrolls slowly. How do you optimise it?
520. 🔴 Users open your banking app in multiple tabs; logging out in one tab should log out all tabs. How do you implement it? 💰
521. 🔴 Your app must auto-logout users after 5 minutes of inactivity. How do you implement it reliably? 💰
522. 🔴 You need to prevent double submission of a payment form. How do you do it on the client (and why is the server still required)? 💰
523. 🔴 You see `Uncaught (in promise)` errors in production logs with no stack trace. How do you improve error tracking?
524. 🔴 Your app works in Chrome but breaks in Safari. How do you investigate?

---

## 37. Rapid-Fire Round

525. 🟢 What does `typeof null` return?
526. 🟢 What does `typeof NaN` return?
527. 🟢 How many falsy values are there? Name them.
528. 🟢 Which keyword is block-scoped and reassignable?
529. 🟢 What is the result of `"2" + 2`? `"2" - 2`?
530. 🟢 Which method converts JSON text to an object?
531. 🟢 Which array method does not return a new array: `map` or `forEach`?
532. 🟢 Which runs first: a microtask or a macrotask?
533. 🟡 What does `Promise.allSettled` return?
534. 🟡 What does `Array.prototype.at(-1)` return?
535. 🟡 What does `Object.freeze` do in one line?
536. 🟡 What is the difference between `??` and `||` in one line?
537. 🟡 What is the difference between `call` and `apply` in one line?
538. 🟡 What is the difference between `slice` and `splice` in one line?
539. 🟡 What is the difference between `Map` and `WeakMap` in one line?
540. 🟡 What is the difference between `defer` and `async` in one line?
541. 🟡 What is the difference between `localStorage` and `sessionStorage` in one line?
542. 🟡 What is the difference between debounce and throttle in one line?
543. 🟡 What API cancels a fetch request?
544. 🟡 Which observer is used for lazy loading images?
545. 🔴 What is the difference between `process.nextTick` and `setImmediate` in one line?
546. 🔴 What is the difference between `interface` and `type` in TypeScript in one line?
547. 🔴 What is the difference between CommonJS and ES Modules in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS · Part 14 — JavaScript.
