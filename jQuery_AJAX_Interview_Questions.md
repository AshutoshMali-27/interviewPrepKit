# 🎯 jQuery & AJAX Interview Questions — Part 15 (Questions Only)

> **Scope:** jQuery fundamentals, selectors, traversing, DOM manipulation, CSS & attributes, events & delegation, effects & animations, utilities, plugins, **AJAX in depth** (`$.ajax`, shorthand methods, Deferred/Promises, error handling, JSON, forms, file uploads, CORS, caching, global AJAX events), **jQuery + AJAX with ASP.NET Core MVC / Web API** (antiforgery tokens, partial views, unobtrusive validation, model binding), jQuery DataTables & Select2, performance, security, migration to modern JS, output snippets, coding tasks and scenario questions.
> **Based on question patterns from:** service MNCs, financial-domain companies (many banking portals still use jQuery + ASP.NET MVC), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — jQuery**
1. jQuery Fundamentals
2. Selectors
3. Traversing the DOM
4. DOM Manipulation
5. Attributes, Properties, CSS & Dimensions
6. Events
7. Event Delegation & Custom Events
8. Effects & Animations
9. Utilities & Data
10. Forms with jQuery
11. Plugins & Extending jQuery
12. Performance & Best Practices
13. jQuery vs Vanilla JS & Migration

**Part B — AJAX**
14. AJAX Fundamentals
15. `$.ajax()` Options In Depth
16. Shorthand AJAX Methods
17. Deferred, Promises & Chaining
18. Error Handling, Timeouts & Retries
19. Sending Data — JSON, Form Data, Files
20. Global AJAX Events & `$.ajaxSetup`
21. Caching, CORS & Cross-Domain Requests
22. AJAX Security

**Part C — jQuery + AJAX with ASP.NET Core MVC / Web API**
23. Calling MVC Actions & Web API Endpoints
24. Antiforgery Tokens with AJAX
25. Partial Views & Dynamic Content
26. Validation — jQuery Validation & Unobtrusive Validation
27. Authentication with AJAX (Cookies & JWT)
28. DataTables, Select2 & Common Plugins

**Part D — Practice**
29. Tricky Questions
30. Predict the Output
31. Coding Tasks
32. Scenario-Based Questions
33. Rapid-Fire Round

---

# Part A — jQuery

## 1. jQuery Fundamentals

1. 🟢 What is jQuery? Why was it created?
2. 🟢 What are the advantages of jQuery?
3. 🟢 Is jQuery a library or a framework?
4. 🟢 What is the `$` symbol in jQuery? What is `jQuery()`?
5. 🟢 What does `$(document).ready()` do? What is the shorthand `$(function () { ... })`?
6. 🟢 What is the difference between `$(document).ready()` and `window.onload` / `$(window).on("load")`?
7. 🟢 How do you include jQuery in a page (CDN vs local)? What is the fallback if the CDN fails?
8. 🟡 What is the difference between the jQuery full build and slim build? What's missing in slim?
9. 🟡 What versions of jQuery exist (1.x, 2.x, 3.x, 4.x)? What changed in jQuery 3 and 4?
10. 🟡 What is a jQuery object? How is it different from a DOM element?
11. 🟡 How do you convert a jQuery object to a DOM element (`[0]`, `.get(0)`) and vice versa (`$(el)`)?
12. 🟡 What is `jQuery.noConflict()`? When do you need it?
13. 🟡 What is method chaining in jQuery? How does it work?
14. 🟡 Is jQuery still relevant today? Where is it still used?
15. 🟡 What is jQuery Migrate?

---

## 2. Selectors

16. 🟢 What are jQuery selectors? Name the basic types (id, class, element, universal).
17. 🟢 What is the difference between `$("#id")`, `$(".class")` and `$("div")`?
18. 🟢 How do you select multiple elements (`$("h1, h2, p")`)?
19. 🟡 What are attribute selectors (`[name='email']`, `[href^='https']`, `[src$='.png']`, `[class*='btn']`)?
20. 🟡 What are hierarchy selectors (descendant `A B`, child `A > B`, adjacent `A + B`, sibling `A ~ B`)?
21. 🟡 What are filter selectors (`:first`, `:last`, `:eq()`, `:even`, `:odd`, `:not()`, `:has()`, `:contains()`)?
22. 🟡 What are form selectors (`:input`, `:text`, `:checked`, `:selected`, `:disabled`, `:visible`, `:hidden`)?
23. 🟡 What is the difference between `:input` and `input`?
24. 🟡 Which jQuery pseudo-selectors were deprecated/removed (`:first`, `:eq()` etc. in favour of `.first()`, `.eq()`)? Why?
25. 🟡 How do you select an element with special characters in its ID (e.g., `user.name`, `Items[0].Name` from MVC)?
26. 🟡 Which selectors are fastest? Why is an ID selector faster than a class selector?
27. 🟡 What is the context parameter (`$("li", "#menu")`)? How is it different from `.find()`?
28. 🔴 Why are jQuery-specific selectors like `:visible` slower than CSS selectors?

---

## 3. Traversing the DOM

29. 🟢 What is DOM traversal?
30. 🟢 What do `.parent()`, `.parents()`, `.closest()` do? What is the difference between `parents()` and `closest()`?
31. 🟢 What do `.children()` and `.find()` do? What is the difference?
32. 🟡 What do `.siblings()`, `.next()`, `.prev()`, `.nextAll()`, `.prevAll()`, `.nextUntil()` do?
33. 🟡 What do `.first()`, `.last()`, `.eq()`, `.filter()`, `.not()`, `.has()`, `.is()` do?
34. 🟡 What does `.each()` do? How is it different from `$.each()`?
35. 🟡 How do you break out of `.each()`?
36. 🟡 What do `.end()` and `.addBack()` do?
37. 🟡 What is `.index()`?
38. 🟡 What does `.map()` do in jQuery? How is it different from `Array.map`?

---

## 4. DOM Manipulation

39. 🟢 What do `.html()`, `.text()` and `.val()` do (getter and setter)?
40. 🟢 What is the difference between `.html()` and `.text()`? Which is safer?
41. 🟢 What do `.append()`, `.prepend()`, `.after()`, `.before()` do?
42. 🟡 What is the difference between `.append()` and `.appendTo()`?
43. 🟡 What do `.remove()`, `.detach()` and `.empty()` do? What is the difference between `remove()` and `detach()`?
44. 🟡 What does `.clone()` do? What does `.clone(true)` do?
45. 🟡 What do `.wrap()`, `.unwrap()`, `.wrapAll()`, `.wrapInner()` do?
46. 🟡 What do `.replaceWith()` and `.replaceAll()` do?
47. 🟡 How do you create a new element with jQuery (`$("<div>", { class: "x", text: "y" })`)?
48. 🟡 How do you add many rows to a table efficiently?
49. 🔴 Why can repeated `.append()` in a loop be slow? How do you optimise it?

---

## 5. Attributes, Properties, CSS & Dimensions

50. 🟢 What do `.attr()` and `.removeAttr()` do?
51. 🟢 What is the difference between `.attr()` and `.prop()`? When do you use each (e.g., `checked`, `disabled`, `selected`)?
52. 🟢 What do `.addClass()`, `.removeClass()`, `.toggleClass()`, `.hasClass()` do?
53. 🟢 What does `.css()` do? How do you set multiple CSS properties?
54. 🟡 What do `.width()`, `.innerWidth()`, `.outerWidth()`, `.outerWidth(true)` return?
55. 🟡 What do `.offset()` and `.position()` return? What is the difference?
56. 🟡 What do `.scrollTop()` and `.scrollLeft()` do?
57. 🟡 How do you enable/disable a button with jQuery?
58. 🟡 How do you check/uncheck a checkbox and read its state?
59. 🟡 How do you get/set the selected value and text of a dropdown?

---

## 6. Events

60. 🟢 How do you bind events in jQuery (`.on()`, `.click()`, `.change()`, `.submit()`)?
61. 🟢 What is the difference between `.on()`, `.bind()`, `.live()` and `.delegate()`? Which are deprecated/removed?
62. 🟢 How do you remove an event handler (`.off()`)?
63. 🟡 What does `.one()` do?
64. 🟡 What is the jQuery event object? What are `e.target`, `e.currentTarget`, `e.which`, `e.type`?
65. 🟡 What do `e.preventDefault()`, `e.stopPropagation()` and `return false` do in a jQuery handler?
66. 🟡 What is the difference between `return false` in jQuery vs in vanilla JS?
67. 🟡 How do you pass data to an event handler (`.on("click", { id: 1 }, handler)`)?
68. 🟡 What are namespaced events (`click.myPlugin`)? Why are they useful?
69. 🟡 What do `.trigger()` and `.triggerHandler()` do? What is the difference?
70. 🟡 What is the difference between `mouseover`/`mouseout` and `mouseenter`/`mouseleave`? What is `.hover()`?
71. 🟡 What are `keydown`, `keypress` (deprecated) and `keyup` events?
72. 🟡 What is the difference between `change` and `input` events?
73. 🟡 Why does a click handler fire multiple times? How do you prevent duplicate binding?
74. 🔴 How does jQuery store event handlers internally (`$._data(el, "events")`)?

---

## 7. Event Delegation & Custom Events

75. 🟢 What is event delegation?
76. 🟡 How do you write a delegated handler (`$(document).on("click", ".btn-delete", handler)`)?
77. 🟡 Why don't click handlers work on elements added via AJAX? How does delegation fix it?
78. 🟡 Why is delegating everything to `document` not ideal? What should you delegate to instead?
79. 🟡 What is `this` inside a delegated event handler?
80. 🟡 How do you create and trigger custom events?
81. 🔴 How does event bubbling make delegation possible? Which events don't bubble?

---

## 8. Effects & Animations

82. 🟢 What do `.show()`, `.hide()` and `.toggle()` do?
83. 🟢 What do `.fadeIn()`, `.fadeOut()`, `.fadeToggle()`, `.fadeTo()` do?
84. 🟢 What do `.slideUp()`, `.slideDown()`, `.slideToggle()` do?
85. 🟡 What does `.animate()` do? Which properties can be animated?
86. 🟡 What are animation callbacks? How do you run code after an animation completes?
87. 🟡 What is the animation queue? What do `.stop()`, `.finish()`, `.delay()` and `.queue()` do?
88. 🟡 Why do animations pile up when hovering quickly, and how do you fix it?
89. 🟡 What is `$.fx.off`?
90. 🔴 Why are CSS transitions/animations usually preferred over jQuery animations today?

---

## 9. Utilities & Data

91. 🟡 What do `$.each`, `$.map`, `$.grep`, `$.inArray`, `$.merge`, `$.unique`/`$.uniqueSort` do?
92. 🟡 What does `$.extend()` do? What is a deep extend (`$.extend(true, ...)`)?
93. 🟡 What do `$.trim`, `$.isArray`, `$.isFunction`, `$.type` do? Which are deprecated?
94. 🟡 What does `$.parseJSON` do? Why is it deprecated (use `JSON.parse`)?
95. 🟡 What does `$.proxy()` do? What is the modern alternative?
96. 🟡 What does `.data()` do? How is it different from `.attr("data-x")`?
97. 🟡 Does `.data()` update the HTML `data-*` attribute?
98. 🟡 How does `.data()` convert values (e.g., `"true"` → boolean, `"10"` → number)?
99. 🟡 What does `$.param()` do?
100. 🟡 What does `.serialize()` and `.serializeArray()` do?

---

## 10. Forms with jQuery

101. 🟢 How do you get and set values of text inputs, checkboxes, radio buttons and dropdowns?
102. 🟢 How do you handle form submit with jQuery and prevent page reload?
103. 🟡 How do you serialise a form to send via AJAX (`serialize`, `serializeArray`, `FormData`)?
104. 🟡 How do you convert a form into a JSON object?
105. 🟡 How do you reset a form?
106. 🟡 How do you dynamically add and remove form rows (e.g., multiple beneficiaries)? 💰
107. 🟡 How do you name dynamically added inputs so ASP.NET MVC model binding works for lists (`Items[0].Name`)?
108. 🟡 How do you populate a dropdown from an AJAX response?
109. 🟡 How do you implement cascading dropdowns (Country → State → City)?
110. 🟡 How do you restrict an input to numbers only or amounts with 2 decimals? 💰
111. 🟡 How do you prevent double submission of a form? 💰

---

## 11. Plugins & Extending jQuery

112. 🟡 What is a jQuery plugin?
113. 🟡 How do you write a jQuery plugin (`$.fn.myPlugin = function (options) { ... }`)?
114. 🟡 Why should a plugin `return this`?
115. 🟡 How do you provide default options in a plugin (`$.extend({}, defaults, options)`)?
116. 🟡 What is the difference between `$.fn.extend` and `$.extend`?
117. 🟡 How do you avoid conflicts with `$` in a plugin (IIFE with `jQuery` passed as `$`)?
118. 🟡 What are popular jQuery plugins (jQuery UI, jQuery Validation, DataTables, Select2, Bootstrap JS 4, Owl Carousel, Inputmask)?
119. 🟡 What is jQuery UI? Name some widgets (datepicker, dialog, autocomplete, sortable).
120. 🔴 How do you destroy a plugin instance and clean up events/data?

---

## 12. Performance & Best Practices

121. 🟡 Why should you cache jQuery selectors in variables?
122. 🟡 Why should you minimise DOM access inside loops?
123. 🟡 Why is building an HTML string and appending once faster than appending in a loop?
124. 🟡 Why is `$("#id").find(".x")` faster than `$("#id .x")` in some cases?
125. 🟡 Why should you use event delegation for large lists?
126. 🟡 Why should you use `.prop()` instead of `.attr()` for boolean properties?
127. 🟡 What is the `$` prefix naming convention for jQuery variables (`$btn`)?
128. 🟡 Where should you place script tags (end of body, `defer`)?
129. 🟡 How do you avoid memory leaks with jQuery (removing handlers, `.remove()` vs manual DOM removal)?
130. 🔴 How do you profile a slow jQuery page?

---

## 13. jQuery vs Vanilla JS & Migration

131. 🟡 What are the vanilla JS equivalents of `$()`, `.on()`, `.addClass()`, `.html()`, `.ajax()`, `.each()`?
132. 🟡 What can vanilla JS do today that once required jQuery (`querySelectorAll`, `classList`, `fetch`, `closest`)?
133. 🟡 When would you still use jQuery in a new project?
134. 🟡 Can jQuery be used with React/Angular/Vue? Why is it discouraged?
135. 🔴 How would you migrate a large jQuery + ASP.NET MVC application to modern JavaScript or a SPA framework?
136. 🔴 What problems do you face upgrading from jQuery 1.x/2.x to 3.x (deprecated methods, `.load()`, `.size()`, Deferred behaviour)?

---

# Part B — AJAX

## 14. AJAX Fundamentals

137. 🟢 What is AJAX? What does it stand for?
138. 🟢 What are the advantages and disadvantages of AJAX?
139. 🟢 Is AJAX a programming language or a technique?
140. 🟢 What is `XMLHttpRequest`? What are its `readyState` values (0–4)?
141. 🟢 What is the difference between synchronous and asynchronous AJAX? Why is synchronous AJAX deprecated?
142. 🟢 What data formats can AJAX use (JSON, XML, HTML, text)?
143. 🟢 What is the difference between AJAX with jQuery, XHR and `fetch`?
144. 🟡 What HTTP methods can you use with AJAX?
145. 🟡 What HTTP status codes should the client handle (200, 201, 204, 400, 401, 403, 404, 409, 422, 500)?
146. 🟡 How does AJAX affect SEO and browser history? How do you handle the back button in AJAX apps?

---

## 15. `$.ajax()` Options In Depth

147. 🟢 What is the syntax of `$.ajax()`?
148. 🟢 What do `url`, `type`/`method`, `data` and `dataType` do?
149. 🟡 What is the difference between `contentType` and `dataType`?
150. 🟡 What is the default `contentType` in `$.ajax`? What happens when you send JSON without changing it?
151. 🟡 What does `processData: false` do? When must you use it?
152. 🟡 What does `contentType: false` do? When must you use it?
153. 🟡 What do `success`, `error` and `complete` callbacks receive?
154. 🟡 What are `done`, `fail` and `always`? How are they different from `success`, `error`, `complete`?
155. 🟡 What does `async: false` do? Why should you avoid it?
156. 🟡 What do `beforeSend` and `headers` options do?
157. 🟡 What does `timeout` do?
158. 🟡 What does `cache: false` do? How does it work (`_=timestamp`)?
159. 🟡 What does `traditional: true` do when sending arrays?
160. 🟡 What do `xhrFields: { withCredentials: true }` and `crossDomain` do?
161. 🟡 What is `statusCode` option in `$.ajax`?
162. 🟡 What is `jqXHR`? What properties does it have (`status`, `statusText`, `responseText`, `responseJSON`)?
163. 🟡 What is `context` option?
164. 🔴 What does the `xhr` option do? How do you use it to track upload progress?

---

## 16. Shorthand AJAX Methods

165. 🟢 What are `$.get()`, `$.post()`, `$.getJSON()` and `$.getScript()`?
166. 🟢 What does `.load()` do? How do you load a fragment of a page (`.load("page.html #content")`)?
167. 🟡 What is the difference between `$.get` and `$.ajax`?
168. 🟡 What are the limitations of shorthand methods (no custom headers, contentType, error handling)?
169. 🟡 Does `$.post` send JSON by default?
170. 🟡 What is JSONP? Why is it insecure and obsolete?

---

## 17. Deferred, Promises & Chaining

171. 🟡 What is `$.Deferred()`?
172. 🟡 What do `.resolve()`, `.reject()`, `.notify()` and `.promise()` do?
173. 🟡 What is the difference between a jQuery Deferred and a native Promise?
174. 🟡 What changed in jQuery 3 to make Deferreds Promises/A+ compliant?
175. 🟡 How do you chain AJAX calls (`.then()`)?
176. 🟡 What does `$.when()` do? How do you run multiple AJAX calls in parallel and wait for all?
177. 🟡 How do you use `async/await` with `$.ajax`?
178. 🟡 How do you convert a jQuery promise to a native Promise?
179. 🔴 How do you run AJAX calls sequentially (one after another)?
180. 🔴 How do you limit the number of concurrent AJAX calls?

---

## 18. Error Handling, Timeouts & Retries

181. 🟢 How do you handle AJAX errors in jQuery?
182. 🟡 What do the parameters of the error callback mean (`jqXHR`, `textStatus`, `errorThrown`)?
183. 🟡 What are possible `textStatus` values (`"timeout"`, `"error"`, `"abort"`, `"parsererror"`)?
184. 🟡 Why do you get a `parsererror` even though the server returned 200?
185. 🟡 How do you read validation errors returned by ASP.NET Core (ProblemDetails / ModelState) in jQuery?
186. 🟡 How do you show a user-friendly message for 401, 403, 404 and 500 errors?
187. 🟡 How do you implement a timeout and show a "Server is taking too long" message?
188. 🟡 How do you abort an in-progress AJAX request (`jqXHR.abort()`)?
189. 🟡 How do you cancel previous requests in search-as-you-type?
190. 🔴 How do you implement automatic retry with backoff for failed AJAX calls?
191. 🔴 How do you handle session timeout when an AJAX call gets redirected to the login page (HTML instead of JSON)? 💰

---

## 19. Sending Data — JSON, Form Data, Files

192. 🟢 How do you send JSON with `$.ajax` (`JSON.stringify` + `contentType: "application/json"`)?
193. 🟢 How do you send form data (`$("form").serialize()`)?
194. 🟡 What is the difference between sending `data: { a: 1 }` and `data: JSON.stringify({ a: 1 })`?
195. 🟡 How do you send an array or a list of objects to the server?
196. 🟡 How do you upload a file with jQuery AJAX (`FormData`, `processData: false`, `contentType: false`)?
197. 🟡 How do you upload multiple files?
198. 🟡 How do you upload a file along with other form fields?
199. 🟡 How do you show upload progress?
200. 🟡 How do you download a file (PDF/Excel) via AJAX (`xhrFields: { responseType: "blob" }`, creating an object URL)? 💰
201. 🟡 How do you send query string parameters with GET?
202. 🔴 How do you upload a large Excel file and show server-side processing status? 💰

---

## 20. Global AJAX Events & `$.ajaxSetup`

203. 🟡 What are global AJAX events (`ajaxStart`, `ajaxStop`, `ajaxSend`, `ajaxSuccess`, `ajaxError`, `ajaxComplete`)?
204. 🟡 How do you show a global loading spinner for all AJAX requests?
205. 🟡 What does `$.ajaxSetup()` do? Why is it discouraged for most options?
206. 🟡 How do you add a header (e.g., antiforgery token or JWT) to all AJAX requests?
207. 🟡 How do you handle 401 errors globally and redirect to login?
208. 🟡 What does `global: false` do in an AJAX call?
209. 🔴 What is `$.ajaxPrefilter()`?

---

## 21. Caching, CORS & Cross-Domain Requests

210. 🟡 Why do GET requests sometimes return stale data in older browsers (IE)? How do you fix it?
211. 🟡 What is the same-origin policy?
212. 🟡 What is CORS? Why do you get a CORS error with jQuery AJAX?
213. 🟡 Is CORS fixed on the client or the server?
214. 🟡 When does a jQuery AJAX request trigger a preflight `OPTIONS` request?
215. 🟡 How do you send cookies with a cross-origin AJAX request?
216. 🟡 How do you configure CORS in ASP.NET Core for a jQuery front end?
217. 🔴 Why do you get CORS errors only for POST/PUT with JSON but not for simple GET requests?

---

## 22. AJAX Security

218. 🟡 How can AJAX responses lead to XSS? Why is `.html(response)` dangerous with untrusted data?
219. 🟡 How do you safely display user data returned from AJAX (`.text()`, encoding)?
220. 🟡 What is CSRF? Why do AJAX POST requests need antiforgery protection when using cookies?
221. 🟡 Should sensitive data (passwords, card numbers) ever be sent via GET query strings? 💰
222. 🟡 Why must validation always be repeated on the server even if jQuery validates on the client?
223. 🟡 What is the risk of loading scripts via `$.getScript` or `.load()` from untrusted sources?
224. 🔴 What are known security issues in old jQuery versions and why should you upgrade? 💰

---

# Part C — jQuery + AJAX with ASP.NET Core MVC / Web API

## 23. Calling MVC Actions & Web API Endpoints

225. 🟢 How do you call an ASP.NET Core MVC controller action using jQuery AJAX?
226. 🟢 How do you return JSON from an MVC action (`return Json(data)`, `Ok(data)`)?
227. 🟡 How do you call a Web API endpoint with GET, POST, PUT and DELETE using jQuery?
228. 🟡 Why does the `[FromBody]` model come as `null` when called from jQuery? (contentType, JSON.stringify, property names)
229. 🟡 When should you use `[FromBody]` vs `[FromForm]` with jQuery AJAX?
230. 🟡 How do you generate the correct URL for an action in JavaScript (`@Url.Action(...)`, `data-url` attributes)?
231. 🟡 How do you send a list of objects to an MVC action and bind it to `List<T>`?
232. 🟡 Why do JSON property names come back as camelCase in ASP.NET Core? How does it affect jQuery code?
233. 🟡 How do you handle `400 Bad Request` with validation errors from `[ApiController]` in jQuery?
234. 🟡 How do you return and handle a file download from an MVC action via AJAX?
235. 🔴 Why does an AJAX call to an MVC action return the login page HTML with status 200 when the session expires? How do you fix it?

---

## 24. Antiforgery Tokens with AJAX

236. 🟡 What is the antiforgery token in ASP.NET Core MVC? Why is it needed?
237. 🟡 How do you include the antiforgery token in a jQuery AJAX POST (`__RequestVerificationToken` in form data or header)?
238. 🟡 How do you configure the header name for antiforgery in ASP.NET Core (`options.HeaderName = "RequestVerificationToken"`)?
239. 🟡 How do you add the antiforgery token to all AJAX requests globally?
240. 🟡 Why do you get a 400 error on AJAX POST after adding `[ValidateAntiForgeryToken]`?
241. 🟡 Do you need antiforgery tokens when calling a Web API with JWT bearer tokens?
242. 🔴 Why do antiforgery tokens fail when the app runs on multiple servers behind Nginx/load balancer (data protection keys)?

---

## 25. Partial Views & Dynamic Content

243. 🟡 How do you load a partial view with jQuery AJAX (`.load()` or `$.get` + `.html()`)?
244. 🟡 How do you return a partial view from an MVC action (`return PartialView("_List", model)`)?
245. 🟡 How do you refresh only part of a page (e.g., a table) after saving data?
246. 🟡 Why do click handlers stop working on content loaded via a partial view? How do you fix it?
247. 🟡 Why doesn't client-side validation work on a form loaded via AJAX? How do you re-parse it (`$.validator.unobtrusive.parse`)?
248. 🟡 How do you open a modal (Bootstrap) and load its content via AJAX?
249. 🟡 Partial views via AJAX vs returning JSON and rendering on the client — pros and cons?
250. 🔴 What is a View Component and can it be loaded via AJAX?

---

## 26. Validation — jQuery Validation & Unobtrusive Validation

251. 🟢 What is the jQuery Validation plugin?
252. 🟢 What is jQuery Unobtrusive Validation in ASP.NET MVC?
253. 🟡 How do Data Annotations in C# become client-side validation rules (`data-val-*` attributes)?
254. 🟡 How do you check if a form is valid before an AJAX submit (`$("form").valid()`)?
255. 🟡 How do you add custom validation rules (`$.validator.addMethod`)?
256. 🟡 How do you create a custom client-side validator for a custom C# validation attribute (adapters)?
257. 🟡 What is remote validation (`[Remote]`) and how does it use AJAX (e.g., checking if a username/account exists)?
258. 🟡 How do you show server-side validation errors returned from an AJAX call next to the right fields?
259. 🟡 How do you validate amounts, PAN, IFSC, mobile and email on the client? 💰
260. 🔴 Why does `$("form").valid()` always return true for dynamically added fields?

---

## 27. Authentication with AJAX (Cookies & JWT)

261. 🟡 How does cookie authentication work with jQuery AJAX in the same domain?
262. 🟡 How do you send a JWT with jQuery AJAX (`Authorization: Bearer` header)?
263. 🟡 Where should you store the JWT in a jQuery application? What are the risks? 💰
264. 🟡 How do you handle token expiry and refresh tokens with jQuery AJAX?
265. 🟡 How do you redirect to the login page when an AJAX call returns 401?
266. 🔴 How do you make sure only one refresh-token call happens when many AJAX calls fail with 401 at the same time?

---

## 28. DataTables, Select2 & Common Plugins

267. 🟡 What is jQuery DataTables? What features does it provide?
268. 🟡 What is client-side vs server-side processing in DataTables?
269. 🟡 How do you implement server-side processing with ASP.NET Core (paging, sorting, searching parameters `start`, `length`, `search[value]`, `order[0][column]`)?
270. 🟡 How do you reload DataTables data after an insert/update (`ajax.reload()`)?
271. 🟡 How do you add action buttons (edit/delete) to DataTables rows and handle clicks?
272. 🟡 How do you export DataTables data to Excel/PDF?
273. 🟡 Why does DataTables become slow with 50,000 rows on the client? What do you do? 💰
274. 🟡 What is Select2? How do you load Select2 options via AJAX with search?
275. 🟡 How do you use jQuery UI Autocomplete with an AJAX source?
276. 🟡 How do you use a datepicker and send the date in the correct format to the server?
277. 🟡 How do you use an input mask plugin for amounts, dates and mobile numbers? 💰

---

# Part D — Practice

## 29. Tricky Questions

278. 🟡 Why doesn't `$("#myId")` find an element with `id="my.id"`?
279. 🟡 Why does `$(".item").click(...)` not work for items added later?
280. 🟡 Why does `.attr("checked")` not reflect whether the checkbox is currently checked?
281. 🟡 Why does `$("#el").length` return 0 even though the element exists in the page source?
282. 🟡 Why does code inside `$(document).ready` run before images are loaded?
283. 🟡 Why does `return false` in a jQuery handler stop both default action and bubbling?
284. 🟡 Why does an AJAX `success` callback run even when the server returns an error message in JSON?
285. 🟡 Why does an AJAX call return `undefined` when you try to return its result from a function?
286. 🟡 Why does an AJAX POST to ASP.NET Core return 415 Unsupported Media Type?
287. 🟡 Why does an AJAX POST to ASP.NET Core return 400 Bad Request even though the data looks correct?
288. 🟡 Why does `[FromBody]` receive `null` from jQuery?
289. 🟡 Why do numbers in the JSON response lose precision for large account numbers? 💰
290. 🟡 Why does a dropdown change event not fire when the value is changed via `.val()`?
291. 🟡 Why does `.data("value")` return a number when the attribute is `data-value="00123"`? 💰
292. 🟡 Why does a form submit twice when you click the submit button?
293. 🟡 Why does `$.ajax` with `async: false` freeze the browser?
294. 🟡 Why do two versions of jQuery on the same page cause errors?
295. 🔴 Why does `$(this)` refer to the wrong element inside an AJAX callback?
296. 🔴 Why do event handlers keep accumulating every time a partial view is reloaded?

---

## 30. Predict the Output

> What happens or what is printed? Explain why.

**297. 🟢 ready vs load**
```js
$(function () { console.log("ready"); });
$(window).on("load", function () { console.log("load"); });
console.log("script");
```

**298. 🟡 attr vs prop**
```html
<input type="checkbox" id="chk" checked>
<script>
  $("#chk").prop("checked", false);
  console.log($("#chk").attr("checked"));
  console.log($("#chk").prop("checked"));
</script>
```

**299. 🟡 html vs text**
```js
$("#out").text("<b>Bold</b>");
console.log($("#out").html());
$("#out").html("<b>Bold</b>");
console.log($("#out").text());
```

**300. 🟡 parents vs closest**
```html
<div class="box"><div class="box"><span id="s"></span></div></div>
<script>
  console.log($("#s").closest(".box").length);
  console.log($("#s").parents(".box").length);
</script>
```

**301. 🟡 Direct binding vs delegation**
```js
$(".row").on("click", () => console.log("direct"));
$("#table").on("click", ".row", () => console.log("delegated"));
$("#table").append('<div class="row">New</div>');
// user clicks the newly added row
```

**302. 🟡 Multiple bindings**
```js
function bind() { $("#save").on("click", () => console.log("saved")); }
bind(); bind(); bind();
// user clicks #save once
```

**303. 🟡 return false**
```html
<div id="outer"><a href="https://example.com" id="link">Go</a></div>
<script>
  $("#outer").on("click", () => console.log("outer"));
  $("#link").on("click", () => { console.log("link"); return false; });
</script>
<!-- user clicks the link -->
```

**304. 🟡 .data() type conversion**
```html
<div id="d" data-id="00123" data-active="true" data-amount="10.50"></div>
<script>
  console.log($("#d").data("id"), typeof $("#d").data("id"));
  console.log($("#d").data("active"), typeof $("#d").data("active"));
  console.log($("#d").attr("data-id"));
</script>
```

**305. 🟡 .data() vs attribute**
```js
$("#d").data("id", 999);
console.log($("#d").data("id"));
console.log($("#d").attr("data-id"));
```

**306. 🟡 each and return false**
```js
$.each([1, 2, 3, 4], function (i, v) {
  if (v === 3) return false;
  console.log(v);
});
```

**307. 🟡 AJAX is asynchronous**
```js
function getUser() {
  let user;
  $.get("/api/user/1", data => { user = data; });
  return user;
}
console.log(getUser());
```

**308. 🟡 Order of callbacks**
```js
$.ajax({ url: "/api/ok" })        // returns 200 with JSON
  .done(() => console.log("done"))
  .fail(() => console.log("fail"))
  .always(() => console.log("always"));
console.log("after");
```

**309. 🟡 contentType and model binding**
```js
$.ajax({
  url: "/api/orders",
  type: "POST",
  data: { productId: 5, qty: 2 }   // no contentType, no JSON.stringify
});
// Controller: public IActionResult Create([FromBody] OrderDto dto)
```
What does the controller receive? What status code is returned?

**310. 🟡 dataType mismatch**
```js
$.ajax({ url: "/Home/Partial", dataType: "json" })  // server returns HTML partial view
  .done(d => console.log("done"))
  .fail((x, status) => console.log("fail:", status));
```

**311. 🟡 $.when**
```js
$.when($.get("/api/a"), $.get("/api/b"))
  .done((a, b) => console.log("both", a[0], b[0]))
  .fail(() => console.log("one failed"));
// /api/a returns 200, /api/b returns 500
```

**312. 🟡 this in callback**
```js
$(".btn").on("click", function () {
  $.get("/api/x", function () {
    $(this).addClass("done");
  });
});
```
Does the clicked button get the class? Why? How do you fix it?

**313. 🔴 File upload without processData**
```js
const fd = new FormData($("#uploadForm")[0]);
$.ajax({ url: "/upload", type: "POST", data: fd });
```

**314. 🔴 Partial view validation**
```js
$("#modalBody").load("/Customers/CreatePartial", function () {
  $("#createForm").on("submit", function (e) {
    e.preventDefault();
    console.log($(this).valid());
  });
});
// the form has required fields but they are empty
```

---

## 31. Coding Tasks

315. 🟢 Toggle the visibility of a div when a button is clicked.
316. 🟢 Highlight table rows on hover and on click.
317. 🟢 Count and display the number of checked checkboxes.
318. 🟢 Implement "Select All" / "Deselect All" checkboxes for a table. 💰
319. 🟡 Add and remove rows dynamically in a form (e.g., multiple nominees/beneficiaries) with correct MVC model binding names. 💰
320. 🟡 Implement cascading dropdowns (Country → State → City) using AJAX.
321. 🟡 Implement a search box with debounced AJAX calls and cancellation of previous requests.
322. 🟡 Submit a form with AJAX including the antiforgery token and show validation errors from the server.
323. 🟡 Load a partial view into a Bootstrap modal for "Edit Customer", submit via AJAX, then refresh the list.
324. 🟡 Implement a delete confirmation and delete via AJAX, then remove the row from the table.
325. 🟡 Upload a file with progress bar using jQuery AJAX and `FormData`.
326. 🟡 Download an Excel/PDF report via AJAX as a blob. 💰
327. 🟡 Implement infinite scroll that loads more records via AJAX when reaching the bottom.
328. 🟡 Implement a global AJAX loader and global 401/500 error handling.
329. 🟡 Implement server-side paging, sorting and searching with DataTables and an ASP.NET Core API. 💰
330. 🟡 Implement remote validation to check whether an account number or username already exists. 💰
331. 🟡 Write a simple jQuery plugin that formats an input as Indian currency on blur. 💰
332. 🟡 Restrict an amount input to numbers with max 2 decimal places and a maximum limit. 💰
333. 🔴 Implement session-timeout handling: warn the user at 4 minutes and auto-logout at 5 minutes of inactivity, extending the session via AJAX. 💰
334. 🔴 Implement automatic JWT refresh on 401 with only one refresh call for concurrent requests.
335. 🔴 Rewrite a jQuery feature (e.g., a form submit with AJAX) in vanilla JS using `fetch`.

---

## 32. Scenario-Based Questions

336. 🟡 A page has 5,000 rows and each row has a delete button with its own click handler. The page is slow. How do you fix it?
337. 🟡 After loading content via AJAX, buttons inside it don't respond to clicks. Why, and how do you fix it?
338. 🟡 After reloading a partial view several times, a click triggers the save AJAX call multiple times. How do you fix it?
339. 🟡 Your AJAX POST to an ASP.NET Core controller fails with 400 after adding antiforgery validation. How do you fix it?
340. 🟡 Your `[FromBody]` DTO is always null when called from jQuery. Walk through the possible causes.
341. 🟡 Users get a login page rendered inside a div after their session expires. How do you handle it properly? 💰
342. 🟡 The client-side validation works on normal pages but not inside modals loaded via AJAX. How do you fix it?
343. 🟡 Users double-click "Pay Now" and two payments are submitted. How do you prevent it on the client and the server? 💰
344. 🟡 A DataTable with 1 lakh transactions loads slowly and freezes the browser. How do you redesign it? 💰
345. 🟡 A cascading dropdown sometimes shows wrong cities because responses arrive out of order. How do you fix it?
346. 🟡 After deploying behind Nginx with multiple servers, AJAX POSTs fail randomly with antiforgery errors. Why?
347. 🟡 The application loads jQuery 1.x and a plugin needs 3.x. How do you handle it?
348. 🟡 A security scan reports XSS in a page where AJAX responses are inserted with `.html()`. How do you fix it?
349. 🟡 A file upload works for small files but fails for files above 30 MB. What do you check (Kestrel/IIS/Nginx limits, `RequestSizeLimit`)?
350. 🟡 The same AJAX GET returns cached old data in some browsers. How do you fix it?
351. 🔴 Your company wants to modernise a large jQuery + MVC banking portal. What is your step-by-step plan? 💰
352. 🔴 An AJAX-heavy page makes 30 requests on load. How do you reduce them?

---

## 33. Rapid-Fire Round

353. 🟢 What symbol is an alias for `jQuery`?
354. 🟢 Which method runs code when the DOM is ready?
355. 🟢 Which method gets/sets the value of an input?
356. 🟢 Which method is used for all event binding in modern jQuery?
357. 🟢 Which method removes event handlers?
358. 🟢 Which method finds the nearest matching ancestor including itself?
359. 🟢 Which method is used for boolean properties like `checked`?
360. 🟢 Which method serialises a form to a query string?
361. 🟢 Which AJAX method is the most configurable?
362. 🟢 Which shorthand method loads HTML into an element?
363. 🟡 Which options are required to upload `FormData` with `$.ajax`?
364. 🟡 Which option tells jQuery what type of data to expect from the server?
365. 🟡 Which option tells the server what type of data you are sending?
366. 🟡 Which method runs multiple AJAX calls in parallel and waits for all?
367. 🟡 Which method aborts an AJAX request?
368. 🟡 Which global event can show a loader when any AJAX request starts?
369. 🟡 Which method re-parses unobtrusive validation for dynamically loaded forms?
370. 🟡 Which header name does ASP.NET Core commonly use for the antiforgery token in AJAX calls?
371. 🔴 What is the difference between `.remove()` and `.detach()` in one line?
372. 🔴 What is the difference between `contentType` and `dataType` in one line?
373. 🔴 What is the difference between `success` and `.done()` in one line?
374. 🔴 What is the difference between `.trigger()` and `.triggerHandler()` in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS · Part 14 — JavaScript · Part 15 — jQuery & AJAX.
