# 🎯 React Interview Questions (with Zustand & TanStack Query) — Part 17 (Questions Only)

> **Level:** 3–4 years of experience.
> **Our stack:** React + TypeScript, **Zustand** for client-side (UI/app) state, **TanStack Query (React Query v5)** for server-side state (fetching, caching, mutations), React Router, forms, ASP.NET Core Web API backend.
> **Scope:** React fundamentals, JSX, components & props, rendering & reconciliation, hooks in depth, custom hooks, Context, **client state vs server state**, **Zustand in depth**, **TanStack Query in depth**, Zustand + TanStack Query together, routing, forms & validation, performance, React 18/19 features (concurrent rendering, transitions, Suspense, Actions, `use`, Server Components overview, React Compiler), error handling, security, testing, build & deployment, **React + ASP.NET Core**, predict-the-behavior snippets, coding tasks and scenario-based questions.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies, mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — React Core**
1. React Fundamentals
2. JSX
3. Components & Props
4. State & Events
5. Rendering, Virtual DOM & Reconciliation
6. Lists & Keys
7. Conditional Rendering & Composition
8. Hooks — `useState` & `useReducer`
9. Hooks — `useEffect`, `useLayoutEffect` & Side Effects
10. Hooks — `useRef`, `useMemo`, `useCallback`, `useId` & Others
11. Custom Hooks
12. Context API
13. Refs, Portals & Forwarding Refs
14. Error Boundaries & Error Handling

**Part B — State Management**
15. Client State vs Server State
16. Zustand — Fundamentals
17. Zustand — Selectors, Re-renders & Performance
18. Zustand — Middleware (persist, devtools, immer, subscribeWithSelector)
19. Zustand — Patterns, Slices, TypeScript & Testing
20. TanStack Query — Fundamentals
21. TanStack Query — Query Keys & Caching (staleTime, gcTime)
22. TanStack Query — Fetching Patterns (dependent, parallel, paginated, infinite)
23. TanStack Query — Mutations, Invalidation & Optimistic Updates
24. TanStack Query — Error Handling, Retries, Suspense & Prefetching
25. TanStack Query — Advanced (select, placeholderData, refetch behaviour, DevTools, testing)
26. Zustand + TanStack Query Together
27. Other State Libraries (Redux Toolkit, RTK Query, Jotai, Recoil) — Comparison

**Part C — Application Concerns**
28. Routing (React Router)
29. Forms & Validation (React Hook Form, Zod)
30. Performance Optimization
31. React 18 & 19 Features
32. Server Components, SSR & Next.js (Overview)
33. Styling
34. Security
35. Testing
36. TypeScript with React
37. Build, Tooling & Deployment
38. React with ASP.NET Core Web API

**Part D — Practice**
39. Tricky Questions
40. Predict the Behavior
41. Coding Tasks
42. Machine Coding Problems
43. Scenario-Based Questions
44. Rapid-Fire Round

---

# Part A — React Core

## 1. React Fundamentals

1. 🟢 What is React? Is it a library or a framework?
2. 🟢 What are the main features of React?
3. 🟢 What is a component-based architecture?
4. 🟢 What is declarative vs imperative UI?
5. 🟢 What is unidirectional data flow?
6. 🟢 What is a Single Page Application? What are its pros and cons?
7. 🟡 What is the difference between React, Angular and Vue?
8. 🟡 How is a React app bootstrapped (`createRoot`, `root.render`)?
9. 🟡 What is `StrictMode`? Why do effects run twice in development?
10. 🟡 What tools do you use to create a React app today (Vite, Next.js, React Router framework mode)? Why is Create React App deprecated?

---

## 2. JSX

11. 🟢 What is JSX? Is it required?
12. 🟢 How does JSX get compiled (`React.createElement` / `jsx()` runtime)?
13. 🟢 Why must JSX return a single root element? What are Fragments (`<>...</>`)?
14. 🟢 Why do we use `className` and `htmlFor`?
15. 🟡 How do you embed expressions in JSX? Can you use `if` statements inside JSX?
16. 🟡 Does JSX prevent XSS? How?
17. 🟡 What is `dangerouslySetInnerHTML` and why is it dangerous?
18. 🟡 What happens if you render `0`, `false`, `null` or `undefined` in JSX?

---

## 3. Components & Props

19. 🟢 What is a component? Function components vs class components?
20. 🟢 What are props? Are props mutable?
21. 🟢 What is `props.children`?
22. 🟡 What are default props in function components?
23. 🟡 What is prop drilling? How do you avoid it?
24. 🟡 What is the difference between props and state?
25. 🟡 What are controlled vs uncontrolled components?
26. 🟡 What are presentational vs container components?
27. 🟡 What are higher-order components (HOCs)? Are they still used?
28. 🟡 What are render props?
29. 🟡 What is the compound component pattern?
30. 🔴 How do you design a reusable component library?

---

## 4. State & Events

31. 🟢 What is state in React?
32. 🟢 How do you handle events in React? What is a synthetic event?
33. 🟡 Is `setState` / `setCount` synchronous or asynchronous?
34. 🟡 What is state batching? What changed with automatic batching in React 18?
35. 🟡 Why should you use the functional updater form (`setCount(c => c + 1)`)?
36. 🟡 Why must state be treated as immutable? How do you update nested objects and arrays?
37. 🟡 What is lifting state up?
38. 🟡 What is derived state? Why should you avoid storing derived data in state?
39. 🟡 How do you pass parameters to event handlers?
40. 🔴 Where should state live — local, lifted, Context, Zustand or TanStack Query? How do you decide?

---

## 5. Rendering, Virtual DOM & Reconciliation

41. 🟢 What is the Virtual DOM?
42. 🟡 What is reconciliation? What is the diffing algorithm?
43. 🟡 What is React Fiber?
44. 🟡 What are the render phase and the commit phase?
45. 🟡 What causes a component to re-render?
46. 🟡 Does a child re-render when the parent re-renders even if props don't change?
47. 🟡 Is re-rendering the same as updating the DOM?
48. 🟡 How do you find out why a component re-rendered (React DevTools Profiler, "why did you render")?
49. 🔴 What is concurrent rendering?

---

## 6. Lists & Keys

50. 🟢 How do you render a list in React?
51. 🟢 Why are keys needed?
52. 🟡 Why is using the array index as a key a bad idea in some cases?
53. 🟡 What happens if keys are not unique?
54. 🟡 How can changing a `key` be used to reset a component's state?

---

## 7. Conditional Rendering & Composition

55. 🟢 What are the ways to conditionally render in React (`&&`, ternary, early return)?
56. 🟡 Why can `{count && <List />}` render `0`?
57. 🟡 What is composition vs inheritance in React?
58. 🟡 What are slots/children patterns for layout components?

---

## 8. Hooks — `useState` & `useReducer`

59. 🟢 What are hooks? Why were they introduced?
60. 🟢 What are the rules of hooks? Why must hooks not be called conditionally?
61. 🟢 How does `useState` work?
62. 🟡 What is lazy initial state (`useState(() => expensive())`)?
63. 🟡 What is `useReducer`? When would you use it instead of `useState`?
64. 🟡 How do you combine `useReducer` with Context?
65. 🔴 How does React keep track of hook state between renders (hook order, linked list)?

---

## 9. Hooks — `useEffect`, `useLayoutEffect` & Side Effects

66. 🟢 What is `useEffect`? What are side effects?
67. 🟢 What does the dependency array do? What happens with `[]`, no array, or `[dep]`?
68. 🟡 What is the cleanup function in `useEffect`? When does it run?
69. 🟡 What is the difference between `useEffect` and `useLayoutEffect`?
70. 🟡 Why do effects run twice in development with StrictMode?
71. 🟡 How do you fetch data with `useEffect`? Why is TanStack Query preferred over manual fetching in effects?
72. 🟡 How do you avoid race conditions when fetching in `useEffect` (ignore flag, `AbortController`)?
73. 🟡 What is a stale closure in `useEffect`? How do you fix it?
74. 🟡 Why can putting objects or functions in the dependency array cause infinite loops?
75. 🟡 "You might not need an effect" — give examples of effects that should be removed.
76. 🔴 What is `useEffectEvent` (experimental) and what problem does it solve?

---

## 10. Hooks — `useRef`, `useMemo`, `useCallback`, `useId` & Others

77. 🟢 What is `useRef`? What are its two main uses?
78. 🟡 Does changing `ref.current` cause a re-render?
79. 🟡 What is `useMemo`? When should you use it?
80. 🟡 What is `useCallback`? When should you use it?
81. 🟡 What is the difference between `useMemo` and `useCallback`?
82. 🟡 What is `React.memo`? How does it work with `useCallback`?
83. 🟡 Why can overusing `useMemo`/`useCallback` hurt performance?
84. 🟡 What is `useId`?
85. 🟡 What is `useImperativeHandle`?
86. 🟡 What is `useSyncExternalStore`? How do Zustand and other stores use it?
87. 🟡 What is `useDeferredValue`?
88. 🟡 What is `useTransition`?
89. 🟡 What are `useActionState`, `useFormStatus` and `useOptimistic` (React 19)?
90. 🟡 What is the `use` API (React 19)?
91. 🔴 How does the React Compiler change the need for `useMemo`/`useCallback`/`memo`?

---

## 11. Custom Hooks

92. 🟢 What is a custom hook? Why must its name start with `use`?
93. 🟡 Do two components using the same custom hook share state?
94. 🟡 Write a `useDebounce` hook.
95. 🟡 Write a `useLocalStorage` hook.
96. 🟡 Write a `useOnClickOutside` hook.
97. 🟡 Write a `usePrevious` hook.
98. 🟡 How do you wrap TanStack Query hooks in custom hooks (`useAccounts`, `useTransferMutation`)? Why is this a good practice? 💰
99. 🔴 How do you test custom hooks (`renderHook`)?

---

## 12. Context API

100. 🟢 What is the Context API? What problem does it solve?
101. 🟡 How do you create and consume context (`createContext`, `Provider`, `useContext`)?
102. 🟡 Why does every consumer re-render when the context value changes?
103. 🟡 How do you avoid unnecessary re-renders with Context (splitting contexts, memoising value)?
104. 🟡 Context vs Zustand — when do you use each?
105. 🟡 Is Context a state management tool or a dependency injection tool?
106. 🔴 Why is Context not ideal for high-frequency updates?

---

## 13. Refs, Portals & Forwarding Refs

107. 🟡 How do you access a DOM element with refs?
108. 🟡 What is `forwardRef`? What changed in React 19 (ref as a prop)?
109. 🟡 What are callback refs?
110. 🟡 What are portals (`createPortal`)? Give use cases (modals, tooltips, toasts).
111. 🟡 How do events bubble through portals?

---

## 14. Error Boundaries & Error Handling

112. 🟢 What is an error boundary?
113. 🟡 Can error boundaries be written as function components? What is `react-error-boundary`?
114. 🟡 Which errors are NOT caught by error boundaries (event handlers, async code, SSR)?
115. 🟡 How do error boundaries work with TanStack Query (`throwOnError`, `QueryErrorResetBoundary`)?
116. 🟡 How do you report errors to a monitoring tool (Sentry)?
117. 🔴 How do you design error handling for API errors, validation errors and unexpected crashes in a React app?

---

# Part B — State Management

## 15. Client State vs Server State

118. 🟢 What is client state? Give examples (theme, sidebar open, selected tab, filters, wizard step, cart draft).
119. 🟢 What is server state? Give examples (accounts, transactions, user profile, product list).
120. 🟡 Why is server state different (asynchronous, owned remotely, can become stale, shared)?
121. 🟡 Why shouldn't you store API data in Zustand or Redux when you use TanStack Query?
122. 🟡 Why did your team choose Zustand + TanStack Query instead of Redux?
123. 🟡 Which problems does TanStack Query solve that `useEffect` + `useState` fetching doesn't (caching, dedup, refetching, retries, stale data, loading/error states)?
124. 🟡 What kind of state belongs in the URL (search params) instead of a store?
125. 🟡 What kind of state belongs in form libraries instead of global stores?
126. 🔴 How would you explain the "state ownership" decision tree to a new team member?

---

## 16. Zustand — Fundamentals

127. 🟢 What is Zustand? Why is it popular?
128. 🟢 How do you create a store (`create`)?
129. 🟢 How do you read state and call actions from a component?
130. 🟡 Does Zustand need a Provider? Why not?
131. 🟡 What are `set` and `get` inside a store?
132. 🟡 Does `set` merge state? How do you replace state entirely?
133. 🟡 How do you update nested state immutably in Zustand?
134. 🟡 How do you access or update the store outside React components (`useStore.getState()`, `useStore.setState()`)?
135. 🟡 How do you subscribe to store changes outside React (`subscribe`)?
136. 🟡 How do you reset a store to its initial state (e.g., on logout)? 💰
137. 🟡 How do you write async actions in Zustand? Should you fetch server data in Zustand actions?
138. 🟡 How is Zustand different from Redux and Context?
139. 🟡 How does Zustand use `useSyncExternalStore` internally?
140. 🔴 What are the trade-offs of a global singleton store (testing, SSR, multiple instances)? When would you use a store created per-provider with `createStore` + Context?

---

## 17. Zustand — Selectors, Re-renders & Performance

141. 🟡 What is a selector in Zustand?
142. 🟡 Why does `const state = useStore()` (no selector) cause unnecessary re-renders?
143. 🟡 Why can returning a new object or array from a selector cause re-renders or infinite loops in Zustand v5?
144. 🟡 What is `useShallow` and when do you use it?
145. 🟡 How do you select multiple values efficiently?
146. 🟡 How do you create derived/computed values in Zustand (selectors vs storing derived state)?
147. 🟡 What is the "auto-generated selectors" pattern?
148. 🟡 How do you split a large store into smaller stores?
149. 🔴 What changed in Zustand v5 (React 18 minimum, `useShallow`, stricter selector behaviour, removed defaults)?

---

## 18. Zustand — Middleware (persist, devtools, immer, subscribeWithSelector)

150. 🟡 What is middleware in Zustand?
151. 🟡 What does the `persist` middleware do? Where does it store data by default?
152. 🟡 How do you persist only part of the state (`partialize`)?
153. 🟡 How do you use `sessionStorage` instead of `localStorage` with `persist`?
154. 🟡 What are `version` and `migrate` in `persist`? Why are they needed?
155. 🟡 What is hydration in `persist`? How do you know when the store has rehydrated (`onRehydrateStorage`, `hasHydrated`)?
156. 🟡 What does the `devtools` middleware do?
157. 🟡 What does the `immer` middleware do?
158. 🟡 What does `subscribeWithSelector` do?
159. 🟡 How do you combine multiple middlewares and in what order?
160. 🔴 What should NOT be persisted in localStorage (tokens, PII, account numbers)? 💰
161. 🔴 What problems can persisted state cause after a deployment changes the state shape?

---

## 19. Zustand — Patterns, Slices, TypeScript & Testing

162. 🟡 What is the slices pattern in Zustand?
163. 🟡 How do you type a Zustand store with TypeScript (`create<State>()(...)`)?
164. 🟡 Should actions live inside the store or outside it?
165. 🟡 How do you organise stores in a large app (feature-based stores)?
166. 🟡 How do you share state between two stores?
167. 🟡 How do you use Zustand for a multi-step form/wizard (e.g., account opening)? 💰
168. 🟡 How do you use Zustand for UI state like modals, toasts and sidebar?
169. 🟡 How do you use Zustand for user session info (non-sensitive) and permissions? 💰
170. 🟡 How do you test components that use Zustand stores (resetting state between tests, mocking)?
171. 🔴 How do you avoid storing a copy of server data in Zustand when you only need a selected ID?

---

## 20. TanStack Query — Fundamentals

172. 🟢 What is TanStack Query (React Query)? What problems does it solve?
173. 🟢 How do you set up TanStack Query (`QueryClient`, `QueryClientProvider`)?
174. 🟢 What is `useQuery`? What do `queryKey` and `queryFn` do?
175. 🟢 What does `useQuery` return (`data`, `error`, `isPending`, `isLoading`, `isFetching`, `isError`, `isSuccess`, `status`, `fetchStatus`, `refetch`)?
176. 🟡 What is the difference between `isPending`, `isLoading` and `isFetching` in v5?
177. 🟡 What is the difference between `status` and `fetchStatus`?
178. 🟡 What does TanStack Query do automatically by default (caching, deduplication, background refetching, retries, garbage collection)?
179. 🟡 What is request deduplication? What happens if 3 components use the same query at the same time?
180. 🟡 What are the main changes in TanStack Query v5 (single object signature, `isPending`, `gcTime`, `placeholderData`, removed callbacks on `useQuery`)?
181. 🟡 Why were `onSuccess`/`onError` callbacks removed from `useQuery` in v5? What should you use instead?
182. 🟡 What is `queryOptions()` helper and why is it useful?

---

## 21. TanStack Query — Query Keys & Caching (staleTime, gcTime)

183. 🟢 What is a query key? Why must it be unique and include all variables the query depends on?
184. 🟡 How do you structure query keys (`['accounts']`, `['accounts', id]`, `['transactions', { accountId, page }]`)?
185. 🟡 What is a query key factory? Why use one?
186. 🟡 What is `staleTime`? What is its default value?
187. 🟡 What is `gcTime` (formerly `cacheTime`)? What is its default value?
188. 🟡 What is the difference between `staleTime` and `gcTime`?
189. 🟡 What does "stale" mean? Does stale data get removed?
190. 🟡 When does a stale query refetch (mount, window focus, reconnect, interval)?
191. 🟡 How do you choose `staleTime` for different data (static config vs balance vs transactions)? 💰
192. 🟡 What happens when a query becomes inactive?
193. 🟡 How do you set global defaults in `QueryClient`?
194. 🔴 What are structural sharing and referential stability of `data`?

---

## 22. TanStack Query — Fetching Patterns

195. 🟡 How do you write dependent queries (`enabled` option)?
196. 🟡 How do you run parallel queries (`useQueries`)?
197. 🟡 How do you implement paginated queries? What is `placeholderData: keepPreviousData`?
198. 🟡 How do you implement infinite scrolling with `useInfiniteQuery` (`getNextPageParam`, `fetchNextPage`, `hasNextPage`, `initialPageParam`)?
199. 🟡 How do you pass filters/search to a query? How does changing the key trigger a refetch?
200. 🟡 How do you debounce a search query with TanStack Query?
201. 🟡 How do you cancel requests (`signal` from `queryFn` context, `AbortController`, `queryClient.cancelQueries`)?
202. 🟡 How do you implement polling (`refetchInterval`)? How do you stop polling when a condition is met? 💰
203. 🟡 How do you refetch on window focus, and how do you disable it?
204. 🔴 How do you implement cursor-based pagination with a .NET API?

---

## 23. TanStack Query — Mutations, Invalidation & Optimistic Updates

205. 🟢 What is `useMutation`? How is it different from `useQuery`?
206. 🟢 What do `mutate` and `mutateAsync` do? What is the difference?
207. 🟡 What do `onMutate`, `onSuccess`, `onError` and `onSettled` do in mutations?
208. 🟡 What is query invalidation (`queryClient.invalidateQueries`)? How does it work with partial keys?
209. 🟡 Invalidation vs `setQueryData` — when do you use each?
210. 🟡 What is an optimistic update? How do you implement one with rollback?
211. 🟡 What is the newer "optimistic UI via `variables`" approach in v5?
212. 🟡 Should you use optimistic updates for a fund transfer? Why or why not? 💰
213. 🟡 How do you prevent double submission with mutations (`isPending`, disabling the button)? 💰
214. 🟡 How do you show success/error toasts after mutations (in component callbacks vs global `MutationCache`)?
215. 🟡 How do you handle validation errors (400 ProblemDetails from ASP.NET Core) from a mutation?
216. 🟡 What is `useMutationState` and `mutationKey`?
217. 🔴 How do you handle mutations that should run sequentially (mutation `scope`)?
218. 🔴 How do you send an idempotency key with a payment mutation and retry safely? 💰

---

## 24. TanStack Query — Error Handling, Retries, Suspense & Prefetching

219. 🟡 How many times does TanStack Query retry failed queries by default? Mutations?
220. 🟡 How do you configure `retry` and `retryDelay`? When should you NOT retry (401, 403, 404, 400)?
221. 🟡 How do you handle errors globally (`QueryCache` / `MutationCache` `onError`)?
222. 🟡 How do you handle 401 errors and refresh tokens with TanStack Query and an Axios/fetch interceptor?
223. 🟡 What is `throwOnError` and how does it work with error boundaries?
224. 🟡 What is `useSuspenseQuery`? How do you use it with `<Suspense>`?
225. 🟡 What is prefetching (`queryClient.prefetchQuery`)? Give use cases (hover, route loaders).
226. 🟡 How do you use TanStack Query with React Router loaders?
227. 🔴 What is `ensureQueryData`?

---

## 25. TanStack Query — Advanced

228. 🟡 What does the `select` option do? Why is it useful for performance?
229. 🟡 What is `initialData` vs `placeholderData`? What is the difference in caching behaviour?
230. 🟡 How do you seed a detail query from a list query's cached data?
231. 🟡 What is `refetchOnMount`, `refetchOnWindowFocus` and `refetchOnReconnect`?
232. 🟡 What is `networkMode` (online, always, offlineFirst)?
233. 🟡 How do you persist the query cache (`persistQueryClient`)? Should you for sensitive data? 💰
234. 🟡 How do you clear the entire cache on logout (`queryClient.clear()`)? Why is that important? 💰
235. 🟡 How do you use TanStack Query DevTools?
236. 🟡 How do you test components that use TanStack Query (new `QueryClient` per test, `retry: false`, MSW)?
237. 🟡 How do you type queries and mutations with TypeScript?
238. 🟡 What is `queryClient.getQueryData` vs `fetchQuery` vs `refetchQueries`?
239. 🟡 How does TanStack Query work with WebSockets/SignalR for real-time updates (`setQueryData` or invalidate on message)? 💰
240. 🔴 What is a "query waterfall" and how do you avoid it?
241. 🔴 How does TanStack Query handle SSR and hydration (`HydrationBoundary`, `dehydrate`)?

---

## 26. Zustand + TanStack Query Together

242. 🟡 How do you decide whether something goes into Zustand or TanStack Query?
243. 🟡 How do you use filters stored in Zustand as part of a TanStack Query key?
244. 🟡 Should you copy TanStack Query data into Zustand? Why not?
245. 🟡 How do you store only the selected account ID in Zustand and read account details from TanStack Query? 💰
246. 🟡 How do you reset both Zustand stores and the query cache on logout? 💰
247. 🟡 How do you handle the auth token — where does it live (memory, Zustand, cookie) and how does the API client read it? 💰
248. 🟡 How do you implement a multi-step transfer wizard where form draft lives in Zustand and beneficiaries/accounts come from TanStack Query? 💰
249. 🟡 How do you trigger a query refetch from a Zustand action?
250. 🟡 How do you keep URL search params, Zustand filters and query keys consistent?
251. 🔴 Design the state architecture for a banking dashboard (accounts, transactions, filters, theme, notifications, session). 💰

---

## 27. Other State Libraries — Comparison

252. 🟡 What is Redux? What are actions, reducers and the store?
253. 🟡 What is Redux Toolkit? What is RTK Query? How does RTK Query compare with TanStack Query?
254. 🟡 Zustand vs Redux Toolkit — pros and cons?
255. 🟡 What are Jotai and Recoil (atom-based state)? How do they compare with Zustand?
256. 🟡 What is SWR? How does it compare with TanStack Query?
257. 🔴 How would you migrate a Redux app to Zustand + TanStack Query?

---

# Part C — Application Concerns

## 28. Routing (React Router)

258. 🟢 What is React Router? How do you define routes?
259. 🟢 What are `Link`, `NavLink`, `useNavigate`, `useParams`, `useSearchParams`, `useLocation`?
260. 🟡 What are nested routes and `<Outlet />`?
261. 🟡 How do you implement protected/private routes? 💰
262. 🟡 How do you implement role-based routes? 💰
263. 🟡 What are loaders and actions in React Router (data APIs)?
264. 🟡 How do you lazy load routes (`React.lazy`, `Suspense`, route `lazy`)?
265. 🟡 How do you handle 404 routes?
266. 🟡 How do you store filters and pagination in URL search params?
267. 🟡 Why do deep links return 404 on Nginx/IIS after deployment? How do you fix it?
268. 🟡 What changed in React Router v7 (merged with Remix, framework mode vs library mode)?
269. 🔴 What is TanStack Router and how does it compare with React Router?

---

## 29. Forms & Validation (React Hook Form, Zod)

270. 🟢 How do you handle forms in React (controlled inputs)?
271. 🟡 What is React Hook Form? Why is it more performant than controlled inputs for large forms?
272. 🟡 What are `register`, `handleSubmit`, `formState`, `watch`, `setValue`, `reset`, `Controller`?
273. 🟡 What is Zod? How do you use it with React Hook Form (`zodResolver`)?
274. 🟡 How do you write validation for PAN, IFSC, mobile, email and amount limits? 💰
275. 🟡 How do you implement cross-field validation (amount ≤ balance, from date < to date)? 💰
276. 🟡 How do you implement dynamic fields (`useFieldArray`) for multiple nominees/beneficiaries? 💰
277. 🟡 How do you submit a form with a TanStack Query mutation?
278. 🟡 How do you map server-side validation errors (ASP.NET Core ProblemDetails) to form fields (`setError`)?
279. 🟡 How do you reset a form after successful submission?
280. 🟡 How do you share Zod schemas between form validation and API response validation?
281. 🟡 What are React 19 form Actions and `useActionState`? When would you use them instead of React Hook Form?
282. 🔴 How do you build a multi-step form with validation per step and draft saving?

---

## 30. Performance Optimization

283. 🟡 How do you optimise a slow React app?
284. 🟡 How do `React.memo`, `useMemo` and `useCallback` help? When are they useless?
285. 🟡 How do Zustand selectors reduce re-renders?
286. 🟡 How does TanStack Query `select` reduce re-renders?
287. 🟡 What is code splitting and lazy loading?
288. 🟡 What is list virtualization (TanStack Virtual, react-window)? When is it needed? 💰
289. 🟡 How do you debounce/throttle expensive operations?
290. 🟡 How do you avoid unnecessary re-renders caused by Context?
291. 🟡 How do you analyse bundle size?
292. 🟡 How do you use the React DevTools Profiler?
293. 🟡 What are Core Web Vitals and how do they apply to React apps?
294. 🟡 How do `useTransition` and `useDeferredValue` keep the UI responsive?
295. 🔴 How do you render a table with 1 lakh transactions smoothly? 💰
296. 🔴 What is the React Compiler and how does it automatically memoize components?

---

## 31. React 18 & 19 Features

297. 🟡 What are the key features of React 18 (concurrent rendering, automatic batching, transitions, Suspense improvements, `createRoot`)?
298. 🟡 What are the key features of React 19 (Actions, `useActionState`, `useFormStatus`, `useOptimistic`, `use`, ref as a prop, document metadata, stylesheet/script support, improved hydration errors)?
299. 🟡 What is Suspense? What can it suspend on?
300. 🟡 What are transitions and how do they differ from urgent updates?
301. 🟡 How does `useOptimistic` compare with TanStack Query optimistic updates?
302. 🔴 What is the React Compiler (v1.0)? What are its rules and limitations?

---

## 32. Server Components, SSR & Next.js (Overview)

303. 🟡 What is client-side rendering vs server-side rendering vs static site generation?
304. 🟡 What are React Server Components? How are they different from SSR?
305. 🟡 What are `'use client'` and `'use server'` directives?
306. 🟡 What is Next.js? What is the App Router?
307. 🟡 How do Zustand and TanStack Query work with SSR/Next.js (store per request, hydration)?
308. 🔴 Does an internal banking portal need SSR or Server Components? Why or why not? 💰

---

## 33. Styling

309. 🟢 What are the ways to style React components (CSS, CSS Modules, Tailwind, styled-components, Emotion, MUI)?
310. 🟡 What are CSS Modules and how do they scope styles?
311. 🟡 What are the pros and cons of Tailwind CSS?
312. 🟡 What are component libraries (MUI, Ant Design, Chakra, shadcn/ui)? How do you choose?
313. 🔴 Why are CSS-in-JS runtime libraries less recommended with Server Components?

---

## 34. Security

314. 🟡 How does React protect against XSS? Where can XSS still happen (`dangerouslySetInnerHTML`, `href="javascript:"`)?
315. 🟡 How do you sanitise HTML before rendering (DOMPurify)?
316. 🟡 Where should you store JWT tokens in a React app? What are the risks of localStorage and Zustand persist? 💰
317. 🟡 What is the BFF (Backend-for-Frontend) pattern with HttpOnly cookies and why is it more secure? 💰
318. 🟡 How do you implement auto-logout after inactivity? 💰
319. 🟡 How do you log out from all tabs (`BroadcastChannel`, `storage` event)? 💰
320. 🟡 Why are protected routes not a security boundary?
321. 🟡 How do you avoid leaking sensitive data in TanStack Query DevTools, Redux/Zustand DevTools or error logs in production? 💰
322. 🟡 What is CSRF and when does a React app need protection?
323. 🔴 How do you integrate OAuth 2.0 / OIDC (Authorization Code + PKCE) in a React SPA (MSAL React, oidc-client-ts)?

---

## 35. Testing

324. 🟢 What tools do you use for testing React (Vitest/Jest, React Testing Library, Playwright/Cypress)?
325. 🟡 What is the philosophy of React Testing Library (test behaviour, not implementation)?
326. 🟡 What are `getBy`, `queryBy` and `findBy` queries?
327. 🟡 How do you simulate user events (`userEvent`)?
328. 🟡 How do you mock API calls (MSW)?
329. 🟡 How do you test components using TanStack Query (wrapper with `QueryClientProvider`, `retry: false`)?
330. 🟡 How do you test components using Zustand (reset store between tests)?
331. 🟡 How do you test custom hooks (`renderHook`)?
332. 🟡 How do you test forms with React Hook Form and Zod?
333. 🟡 How do you test routing and protected routes?
334. 🔴 What should you cover in E2E tests for a fund transfer flow? 💰

---

## 36. TypeScript with React

335. 🟡 How do you type props, state and events in React?
336. 🟡 How do you type `children` (`React.ReactNode`)?
337. 🟡 How do you type `useRef` for DOM elements?
338. 🟡 How do you type custom hooks and generic components?
339. 🟡 How do you type API responses and use them with TanStack Query?
340. 🟡 How do you type a Zustand store with actions?
341. 🟡 How do you generate TypeScript types from the .NET OpenAPI spec (openapi-typescript, Orval, NSwag)?
342. 🔴 Why do TypeScript types not guarantee API response shape at runtime? How does Zod help?

---

## 37. Build, Tooling & Deployment

343. 🟡 What is Vite? Why is it faster than Webpack-based CRA?
344. 🟡 How do you manage environment variables in Vite (`import.meta.env`, `VITE_` prefix)? Are they secret?
345. 🟡 How do you configure a dev proxy in Vite to call a .NET API and avoid CORS?
346. 🟡 How do you configure runtime API URLs without rebuilding for each environment?
347. 🟡 How do you deploy a React SPA on Nginx (static files, `try_files`, caching headers)?
348. 🟡 How do you deploy on IIS (URL Rewrite) or S3 + CloudFront?
349. 🟡 Why do users see an old version after deployment? How do you fix it (cache headers for `index.html`, hashed assets)?
350. 🟡 How do you containerise a React app with Nginx in Docker?
351. 🟡 What are ESLint, Prettier and `eslint-plugin-react-hooks`?
352. 🔴 What is a micro-frontend architecture with React (Module Federation)?

---

## 38. React with ASP.NET Core Web API

353. 🟢 How does a React app call an ASP.NET Core Web API?
354. 🟡 Why do you get CORS errors calling the .NET API from `localhost:5173`? How do you fix it (CORS policy or Vite proxy)?
355. 🟡 How do you create an API client (fetch wrapper or Axios instance) used by TanStack Query `queryFn`s?
356. 🟡 How do you handle ASP.NET Core `ProblemDetails` errors in the API client and in mutations?
357. 🟡 How do you send dates and decimal amounts safely between React and .NET? 💰
358. 🟡 How do you implement JWT authentication between React and ASP.NET Core?
359. 🟡 How do you implement cookie-based authentication with antiforgery tokens between React and ASP.NET Core?
360. 🟡 How do you implement server-side pagination, sorting and filtering with a .NET API and TanStack Query?
361. 🟡 How do you upload files to an ASP.NET Core API with progress?
362. 🟡 How do you download PDF/Excel reports from a .NET API? 💰
363. 🟡 How do you integrate SignalR with React and update TanStack Query cache on events? 💰
364. 🟡 How do you generate a typed API client from Swagger/OpenAPI and use it with TanStack Query?
365. 🔴 How do you handle API versioning changes in the React client?

---

# Part D — Practice

## 39. Tricky Questions

366. 🟡 Why does `setCount(count + 1)` called three times only increase the count by 1?
367. 🟡 Why does `console.log(count)` right after `setCount` show the old value?
368. 🟡 Why does my `useEffect` run twice in development?
369. 🟡 Why does my `useEffect` run in an infinite loop?
370. 🟡 Why does `{items.length && <List />}` render `0`?
371. 🟡 Why does a child re-render even though its props didn't change?
372. 🟡 Why doesn't `React.memo` prevent re-renders when I pass an inline function or object?
373. 🟡 Why does mutating state directly not trigger a re-render?
374. 🟡 Why does using index as key break input values when items are reordered?
375. 🟡 Why is `useRef` value not shown in the UI after changing it?
376. 🟡 Why does my component using `useStore()` (no selector) re-render on every store change?
377. 🟡 Why does a Zustand selector returning `{ a, b }` cause an infinite render loop in v5?
378. 🟡 Why doesn't changing a value inside a persisted Zustand store reflect after a page refresh?
379. 🟡 Why does my TanStack Query refetch every time I switch browser tabs?
380. 🟡 Why does my query show old data for a moment after changing filters?
381. 🟡 Why does my query not refetch when a filter changes? (key doesn't include the filter)
382. 🟡 Why does the list not update after a successful mutation? (no invalidation)
383. 🟡 Why does my query run with `undefined` ID? How do you fix it (`enabled`)?
384. 🟡 Why do two components show different data for the same entity? (different query keys)
385. 🟡 Why did data from the previous user appear after logging in as another user? 💰
386. 🟡 Is `isLoading` true during background refetches?
387. 🟡 Does `staleTime: 0` mean data is not cached?
388. 🔴 Why can optimistic updates show a wrong balance briefly, and why is it risky for financial data? 💰
389. 🔴 Why does `mutate` inside a `useEffect` cause duplicate mutations in StrictMode?
390. 🔴 Why does a stale closure appear inside a `setInterval` in a component?

---

## 40. Predict the Behavior

> What happens in each snippet? Explain why and how to fix it if needed.

**391. 🟡 Batched state updates**
```jsx
function Counter() {
  const [count, setCount] = useState(0);
  const handle = () => { setCount(count + 1); setCount(count + 1); setCount(count + 1); };
  return <button onClick={handle}>{count}</button>;
}
// clicked once
```

**392. 🟡 Functional updater**
```jsx
const handle = () => { setCount(c => c + 1); setCount(c => c + 1); setCount(c => c + 1); };
// clicked once
```

**393. 🟡 Logging after setState**
```jsx
const handle = () => { setCount(5); console.log(count); };
```

**394. 🟡 useEffect dependencies**
```jsx
function Profile({ user }) {
  const [data, setData] = useState(null);
  useEffect(() => { fetch(`/api/users/${user.id}`).then(r => r.json()).then(setData); }, [user]);
}
// parent: <Profile user={{ id: 1 }} />  (re-renders every second)
```

**395. 🟡 Missing dependency**
```jsx
function Timer() {
  const [count, setCount] = useState(0);
  useEffect(() => {
    const id = setInterval(() => setCount(count + 1), 1000);
    return () => clearInterval(id);
  }, []);
  return <p>{count}</p>;
}
```

**396. 🟡 Rendering 0**
```jsx
const items = [];
return <div>{items.length && <ul>...</ul>}</div>;
```

**397. 🟡 React.memo with inline function**
```jsx
const Row = React.memo(({ onSelect }) => { console.log('render row'); return <button onClick={onSelect}>x</button>; });
function Table() {
  const [n, setN] = useState(0);
  return <><Row onSelect={() => console.log('sel')} /><button onClick={() => setN(n + 1)}>+</button></>;
}
// "+" clicked 3 times
```

**398. 🟡 Key reset**
```jsx
<TransferForm key={selectedAccountId} accountId={selectedAccountId} />
// user switches selected account
```

**399. 🟡 Zustand without selector**
```js
const useUiStore = create(set => ({ theme: 'light', sidebarOpen: false,
  toggleSidebar: () => set(s => ({ sidebarOpen: !s.sidebarOpen })) }));

function ThemeLabel() { const { theme } = useUiStore(); return <span>{theme}</span>; }
// toggleSidebar() is called repeatedly
```

**400. 🔴 Zustand v5 selector returning object**
```js
const { a, b } = useStore(s => ({ a: s.a, b: s.b }));
```
What happens? How do you fix it?

**401. 🟡 Zustand set merges**
```js
const useStore = create(set => ({ count: 0, name: 'x', reset: () => set({ count: 0 }) }));
// after reset(), what is name?
// what about set({ count: 0 }, true)?
```

**402. 🟡 Zustand nested update**
```js
const useStore = create(set => ({
  filter: { status: 'all', page: 1 },
  setStatus: status => set(state => { state.filter.status = status; return state; }),
}));
```
Will components re-render? How do you fix it?

**403. 🟡 Query key without variable**
```js
function Transactions({ accountId }) {
  const { data } = useQuery({ queryKey: ['transactions'], queryFn: () => api.getTxns(accountId) });
}
// accountId changes from 1 to 2
```
💰

**404. 🟡 enabled for dependent query**
```js
const { data: user } = useQuery({ queryKey: ['me'], queryFn: api.me });
const { data: accounts } = useQuery({ queryKey: ['accounts', user.id], queryFn: () => api.accounts(user.id) });
```

**405. 🟡 Deduplication**
```js
// Three components on the same page each call:
useQuery({ queryKey: ['accounts'], queryFn: api.getAccounts });
```
How many network requests are made?

**406. 🟡 staleTime**
```js
useQuery({ queryKey: ['branches'], queryFn: api.branches, staleTime: 5 * 60_000 });
// component unmounts and remounts after 1 minute; after 6 minutes
```

**407. 🟡 gcTime**
```js
useQuery({ queryKey: ['report', id], queryFn: ..., gcTime: 60_000 });
// user leaves the page for 2 minutes and comes back
```

**408. 🟡 Mutation without invalidation**
```js
const add = useMutation({ mutationFn: api.addBeneficiary });
// after add.mutate(newBeneficiary) succeeds, the beneficiary list doesn't show the new item
```
💰

**409. 🟡 Invalidation with partial key**
```js
queryClient.invalidateQueries({ queryKey: ['transactions'] });
// cached keys: ['transactions', {accountId: 1}], ['transactions', {accountId: 2}], ['accounts']
```
Which queries are invalidated?

**410. 🟡 placeholderData**
```js
useQuery({ queryKey: ['txns', page], queryFn: () => api.txns(page), placeholderData: keepPreviousData });
// user goes from page 1 to page 2
```

**411. 🟡 Retries on 404**
```js
useQuery({ queryKey: ['account', id], queryFn: () => api.account(id) });  // API returns 404
```
How long until the error shows (default settings)? How do you avoid retrying 404s?

**412. 🔴 Optimistic update rollback**
```js
useMutation({
  mutationFn: api.toggleFavourite,
  onMutate: async id => {
    await queryClient.cancelQueries({ queryKey: ['accounts'] });
    const prev = queryClient.getQueryData(['accounts']);
    queryClient.setQueryData(['accounts'], old => old.map(a => a.id === id ? { ...a, fav: !a.fav } : a));
    return { prev };
  },
  onError: (_e, _id, ctx) => queryClient.setQueryData(['accounts'], ctx.prev),
  onSettled: () => queryClient.invalidateQueries({ queryKey: ['accounts'] }),
});
// the API call fails
```

**413. 🔴 Logout without clearing cache**
```js
function logout() { useAuthStore.getState().clear(); navigate('/login'); }
// another user logs in on the same browser
```
💰

**414. 🔴 Copying server data into Zustand**
```js
const { data } = useQuery({ queryKey: ['accounts'], queryFn: api.accounts });
useEffect(() => { if (data) useAccountStore.getState().setAccounts(data); }, [data]);
```
What problems does this cause?

---

## 41. Coding Tasks

415. 🟢 Build a counter with increment, decrement and reset.
416. 🟢 Build a controlled input with live character count.
417. 🟡 Write `useDebounce`, `useLocalStorage`, `useOnClickOutside` and `usePrevious` hooks.
418. 🟡 Create a Zustand store for UI state (theme, sidebar, active modal) with `persist` for theme only.
419. 🟡 Create a Zustand store for transaction filters (date range, type, amount range) and use it in a TanStack Query key. 💰
420. 🟡 Create a query key factory for accounts and transactions.
421. 🟡 Create custom hooks `useAccounts`, `useAccount(id)`, `useTransactions(filters)` with TanStack Query. 💰
422. 🟡 Implement a beneficiary list with add/delete mutations and proper invalidation. 💰
423. 🟡 Implement server-side paginated transactions with `keepPreviousData`. 💰
424. 🟡 Implement infinite scroll transaction history with `useInfiniteQuery`. 💰
425. 🟡 Implement search-as-you-type with debounce and TanStack Query.
426. 🟡 Implement an optimistic "mark as favourite" with rollback.
427. 🟡 Implement a fund transfer form with React Hook Form + Zod (amount ≤ balance, required beneficiary, remarks) and submit via `useMutation`. 💰
428. 🟡 Map ASP.NET Core ProblemDetails validation errors to React Hook Form fields.
429. 🟡 Implement protected routes and role-based routes with React Router.
430. 🟡 Implement an Axios/fetch API client that adds a JWT and handles 401 with a single refresh call.
431. 🟡 Implement logout that clears Zustand stores, the query cache and redirects. 💰
432. 🟡 Implement polling of a payment status until it becomes SUCCESS or FAILED. 💰
433. 🔴 Implement an inactivity auto-logout with a warning modal. 💰
434. 🔴 Implement real-time balance updates via SignalR that update the TanStack Query cache. 💰
435. 🔴 Implement a virtualized table for 1 lakh rows with TanStack Virtual. 💰

---

## 42. Machine Coding Problems

436. 🟡 Build a todo app with filters using Zustand.
437. 🟡 Build a product list with search, filters (Zustand), server data (TanStack Query) and pagination.
438. 🟡 Build a multi-step account opening wizard (Zustand for draft, Zod validation per step, final mutation). 💰
439. 🟡 Build a banking dashboard: accounts summary, recent transactions, filters and quick transfer. 💰
440. 🟡 Build a modal and toast system using Zustand.
441. 🟡 Build an autocomplete component with keyboard navigation.
442. 🟡 Build a file upload component with drag-and-drop and progress.
443. 🔴 Build a fund transfer flow: select account → beneficiary → amount → OTP → confirmation, preventing double submission and handling idempotency. 💰
444. 🔴 Build a data table with server-side sorting, filtering, pagination and column selection persisted in Zustand.

---

## 43. Scenario-Based Questions

445. 🟡 Your app makes the same API call 5 times on one page. How do you fix it?
446. 🟡 After adding a beneficiary, the list doesn't update until refresh. How do you fix it? 💰
447. 🟡 After logout and login as a different user, the previous user's account data appears briefly. How do you fix it? 💰
448. 🟡 Your dashboard refetches all data every time the user switches tabs and the API is overloaded. What do you change?
449. 🟡 The balance shown is stale after a transfer. How do you keep it fresh (invalidate, refetch, real-time push)? 💰
450. 🟡 A search box causes a request on every keystroke and results flicker. How do you fix it?
451. 🟡 A component re-renders 50 times when typing in an unrelated input. How do you find and fix it?
452. 🟡 Your Zustand store has grown to 2,000 lines with API data, UI state and form drafts. How do you refactor it?
453. 🟡 A user double-clicks "Pay" and two payments are created. How do you prevent it on the client and server? 💰
454. 🟡 Your team stores the JWT in a persisted Zustand store. The security team objects. What do you propose? 💰
455. 🟡 A form with 80 fields becomes slow while typing. How do you optimise it?
456. 🟡 Dates from the .NET API display one day earlier for some users. How do you fix it? 💰
457. 🟡 A page shows a blank screen when one widget throws an error. How do you isolate failures?
458. 🟡 After a deployment, users with old persisted Zustand state get crashes. How do you prevent it?
459. 🟡 You need to show transaction status updates in real time. Polling vs SignalR vs SSE — what do you choose? 💰
460. 🟡 The list of 50,000 transactions freezes the browser. How do you fix it? 💰
461. 🟡 Two tabs are open; logging out in one should log out the other and clear caches. How do you implement it? 💰
462. 🟡 A mutation fails with a 400 validation error from ASP.NET Core and the user sees "Something went wrong". How do you show field-level errors?
463. 🔴 Your app must work for users with unstable mobile networks. How do you configure TanStack Query (retries, network mode, refetch on reconnect)?
464. 🔴 Your team wants to migrate from Redux + useEffect fetching to Zustand + TanStack Query. What is your plan?
465. 🔴 The CTO wants to move the banking portal to Next.js with Server Components. What would you evaluate and how would Zustand and TanStack Query fit? 💰

---

## 44. Rapid-Fire Round

466. 🟢 Which hook manages local state?
467. 🟢 Which hook runs side effects?
468. 🟢 Which hook gives access to a DOM element?
469. 🟢 Which hook memoizes a value?
470. 🟢 Which hook memoizes a function?
471. 🟢 What prop must list items have?
472. 🟢 What is the `<></>` syntax called?
473. 🟡 Which Zustand function creates a store?
474. 🟡 Does Zustand need a Provider?
475. 🟡 Which Zustand hook helper prevents re-renders when selecting multiple values?
476. 🟡 Which Zustand middleware saves state to localStorage?
477. 🟡 How do you read Zustand state outside a component?
478. 🟡 Which TanStack Query hook fetches data?
479. 🟡 Which TanStack Query hook changes data?
480. 🟡 Which TanStack Query hook handles infinite scrolling?
481. 🟡 What is the default `staleTime`?
482. 🟡 What is the default `gcTime`?
483. 🟡 How many times are failed queries retried by default?
484. 🟡 Which method marks queries stale and refetches active ones?
485. 🟡 Which method updates cached data directly?
486. 🟡 Which method clears the entire cache?
487. 🟡 Which option prevents a query from running until a value exists?
488. 🟡 Which option keeps showing previous page data during pagination?
489. 🔴 What is the difference between `isPending` and `isFetching` in one line?
490. 🔴 What is the difference between `staleTime` and `gcTime` in one line?
491. 🔴 What is the difference between client state and server state in one line?
492. 🔴 What is the difference between `useEffect` and `useLayoutEffect` in one line?
493. 🔴 What is the difference between `mutate` and `mutateAsync` in one line?
494. 🔴 What is the difference between `initialData` and `placeholderData` in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS · Part 14 — JavaScript · Part 15 — jQuery & AJAX · Part 16 — Angular · Part 17 — React (Zustand & TanStack Query).
