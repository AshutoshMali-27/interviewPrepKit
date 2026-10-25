# 🎯 Python, AI, ML, LLM & RAG Interview Questions — Part 19 (Questions Only)

> **Level:** Basics → intermediate, for a **software engineer (.NET full-stack) adding AI skills**. Not a data-scientist/ML-researcher interview.
> **Scope:**
> **Part A — Python basics** (syntax, data types, collections, functions, OOP, errors, modules, files, comprehensions, generators, async, typing, virtual environments, popular libraries, FastAPI basics).
> **Part B — AI & ML fundamentals** (AI vs ML vs DL, supervised/unsupervised/reinforcement learning, common algorithms, training & evaluation, overfitting, metrics, features, NumPy/Pandas/scikit-learn).
> **Part C — Deep learning & NLP basics** (neural networks, backpropagation, CNNs/RNNs overview, transformers, attention, tokenization, embeddings).
> **Part D — LLMs & Generative AI** (how LLMs work, tokens, context window, temperature, prompting, function/tool calling, structured output, fine-tuning vs RAG, hallucinations, model selection, cost & latency).
> **Part E — RAG** (embeddings, chunking, vector databases, pgvector, retrieval, re-ranking, hybrid search, evaluation, advanced RAG).
> **Part F — AI agents & MCP** (agents, tools, planning, memory, multi-agent, Model Context Protocol).
> **Part G — Building AI apps** (AI in .NET with Semantic Kernel & Microsoft.Extensions.AI, Python frameworks like LangChain/LlamaIndex, AWS Bedrock/Azure OpenAI, LLMOps, evaluation, observability, security, responsible AI, financial-domain use cases).
> **Part H — Practice** (tricky questions, scenarios, system design, hands-on tasks, rapid fire).
> **Based on question patterns from:** product companies, service MNCs, financial-domain companies, startups building GenAI features, plus questions candidates commonly report on LinkedIn and Glassdoor.

**Legend:** 🟢 Basic · 🟡 Intermediate · 🔴 Advanced (good to know) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Python**
1. Python Fundamentals
2. Data Types & Variables
3. Strings
4. Collections — List, Tuple, Set, Dictionary
5. Control Flow & Comprehensions
6. Functions, Lambdas & Decorators
7. Object-Oriented Python
8. Exceptions & Context Managers
9. Modules, Packages & Virtual Environments
10. Iterators, Generators & Itertools
11. File Handling, JSON & CSV
12. Concurrency — Threads, Multiprocessing, asyncio, GIL
13. Type Hints & Pydantic
14. Popular Libraries & FastAPI Basics
15. Python vs C# for .NET Developers
16. Python Predict-the-Output & Coding Tasks

**Part B — AI & ML Fundamentals**
17. AI, ML, DL & GenAI — Concepts
18. Types of Machine Learning
19. Data, Features & Preprocessing
20. Common ML Algorithms
21. Training, Validation & Testing
22. Overfitting, Underfitting & Regularization
23. Evaluation Metrics
24. NumPy, Pandas & scikit-learn Basics
25. MLOps Basics

**Part C — Deep Learning & NLP Basics**
26. Neural Networks
27. CNNs, RNNs & Sequence Models (Overview)
28. Transformers & Attention
29. NLP Basics — Tokenization & Embeddings

**Part D — LLMs & Generative AI**
30. LLM Fundamentals
31. Tokens, Context Window & Generation Parameters
32. Prompt Engineering
33. Function / Tool Calling & Structured Output
34. Fine-Tuning, Adapters & Alignment
35. Hallucinations & Grounding
36. Model Selection, Cost & Latency
37. Multimodal & Other Generative Models

**Part E — Retrieval-Augmented Generation (RAG)**
38. RAG Fundamentals
39. Embeddings & Similarity Search
40. Chunking & Document Processing
41. Vector Databases (pgvector, OpenSearch, Pinecone, Qdrant, etc.)
42. Retrieval, Hybrid Search & Re-ranking
43. Advanced RAG Patterns
44. RAG Evaluation

**Part F — AI Agents & MCP**
45. AI Agents Fundamentals
46. Tools, Planning & Memory
47. Multi-Agent Systems & Workflows
48. Model Context Protocol (MCP)

**Part G — Building AI Applications**
49. AI in .NET — Semantic Kernel, Microsoft.Extensions.AI, Azure OpenAI
50. Python AI Frameworks — LangChain, LlamaIndex, LangGraph
51. Cloud AI Services — AWS Bedrock, Azure OpenAI, SageMaker
52. LLMOps — Evaluation, Observability, Versioning
53. AI Security — Prompt Injection, Data Leakage, Guardrails
54. Responsible AI, Privacy & Compliance
55. Financial-Domain AI Use Cases 💰

**Part H — Practice**
56. Tricky Questions
57. Scenario-Based Questions
58. AI System Design Questions
59. Hands-On Tasks
60. Rapid-Fire Round

---

# Part A — Python

## 1. Python Fundamentals

1. 🟢 What is Python? What are its key features?
2. 🟢 Is Python compiled or interpreted? What is bytecode (`.pyc`)?
3. 🟢 What is CPython? What are PyPy and other implementations?
4. 🟢 What is PEP 8? What is PEP 20 (The Zen of Python)?
5. 🟢 How is indentation used in Python?
6. 🟢 What is dynamic typing? What is strong typing? Is Python strongly typed?
7. 🟢 What is `None`?
8. 🟢 What is the difference between `is` and `==`?
9. 🟢 What is `if __name__ == "__main__":` used for?
10. 🟡 How is memory managed in Python (reference counting, garbage collector)?
11. 🟡 What is the difference between Python 2 and Python 3? Which version should you use today?

---

## 2. Data Types & Variables

12. 🟢 What are Python's built-in data types?
13. 🟢 What is the difference between mutable and immutable types? Give examples.
14. 🟢 What is the difference between `int`, `float`, `complex` and `Decimal`? Why use `Decimal` for money? 💰
15. 🟢 What are truthy and falsy values in Python?
16. 🟡 How does variable assignment work (names bound to objects)?
17. 🟡 What is the difference between shallow copy and deep copy (`copy.copy`, `copy.deepcopy`)?
18. 🟡 What is integer caching / interning in Python?
19. 🟡 What are `global` and `nonlocal`?

---

## 3. Strings

20. 🟢 Are strings mutable in Python?
21. 🟢 What are f-strings? How are they different from `format()` and `%` formatting?
22. 🟢 What do `split`, `join`, `strip`, `replace`, `find`, `upper`, `lower`, `startswith` do?
23. 🟢 What is string slicing (`s[1:4]`, `s[::-1]`)?
24. 🟡 What are raw strings (`r"..."`)?
25. 🟡 How do you handle Unicode and encoding (`encode`, `decode`, UTF-8)?

---

## 4. Collections — List, Tuple, Set, Dictionary

26. 🟢 What is the difference between a list and a tuple?
27. 🟢 What is a set? What is a dictionary?
28. 🟢 What can be used as a dictionary key? Why can't a list be a key?
29. 🟢 What do `append`, `extend`, `insert`, `pop`, `remove`, `sort`, `sorted` do?
30. 🟡 What is the difference between `sort()` and `sorted()`?
31. 🟡 Are dictionaries ordered in Python 3.7+?
32. 🟡 What do `get`, `setdefault`, `update`, `items`, `keys`, `values` do on dictionaries?
33. 🟡 What are `defaultdict`, `Counter`, `OrderedDict`, `deque` and `namedtuple`?
34. 🟡 What is a `dataclass`?
35. 🟡 What is the time complexity of lookups in a list vs a set vs a dictionary?
36. 🟡 How do you merge two dictionaries (`|`, `**`, `update`)?

---

## 5. Control Flow & Comprehensions

37. 🟢 How do `if`, `elif`, `else`, `for`, `while`, `break`, `continue` and `pass` work?
38. 🟢 What does `range()` do?
39. 🟢 What do `enumerate()` and `zip()` do?
40. 🟡 What is a list comprehension? Dict comprehension? Set comprehension?
41. 🟡 What is a generator expression? How is it different from a list comprehension?
42. 🟡 What is the `for...else` and `while...else` construct?
43. 🟡 What is structural pattern matching (`match`/`case`, Python 3.10+)?
44. 🟡 What is the walrus operator (`:=`)?

---

## 6. Functions, Lambdas & Decorators

45. 🟢 How do you define a function? What are default arguments?
46. 🟢 What are `*args` and `**kwargs`?
47. 🟢 What is a lambda function?
48. 🟡 What are keyword-only and positional-only arguments?
49. 🟡 Why is using a mutable default argument (`def f(x=[])`) a bug?
50. 🟡 What are first-class functions and higher-order functions (`map`, `filter`, `reduce`)?
51. 🟡 What is a closure in Python?
52. 🟡 What is a decorator? Write a timing decorator.
53. 🟡 What does `functools.wraps` do?
54. 🟡 What is `functools.lru_cache`?
55. 🟡 How are arguments passed in Python (pass-by-object-reference)?

---

## 7. Object-Oriented Python

56. 🟢 How do you define a class? What is `__init__` and `self`?
57. 🟢 What are instance variables vs class variables?
58. 🟡 What are `@staticmethod` and `@classmethod`?
59. 🟡 How does inheritance work? What is `super()`?
60. 🟡 Does Python support multiple inheritance? What is the MRO (method resolution order)?
61. 🟡 How is encapsulation done in Python (`_protected`, `__private` name mangling)?
62. 🟡 What are dunder/magic methods (`__str__`, `__repr__`, `__len__`, `__eq__`, `__hash__`, `__iter__`, `__call__`)?
63. 🟡 What is the difference between `__str__` and `__repr__`?
64. 🟡 What is `@property`?
65. 🟡 What are abstract base classes (`abc.ABC`, `@abstractmethod`)?
66. 🟡 What is duck typing? What are Protocols?
67. 🔴 What are `__slots__` and metaclasses (high level)?

---

## 8. Exceptions & Context Managers

68. 🟢 How does `try`, `except`, `else`, `finally` work?
69. 🟢 How do you raise and create custom exceptions?
70. 🟡 What is the difference between `except Exception` and a bare `except:`?
71. 🟡 What is a context manager? What does the `with` statement do?
72. 🟡 How do you write a custom context manager (`__enter__`/`__exit__`, `contextlib.contextmanager`)?
73. 🟡 What is exception chaining (`raise ... from ...`)?

---

## 9. Modules, Packages & Virtual Environments

74. 🟢 What is a module? What is a package? What is `__init__.py`?
75. 🟢 How do `import`, `from ... import` and `as` work?
76. 🟢 What is `pip`? What is `requirements.txt`?
77. 🟢 What is a virtual environment (`venv`)? Why is it needed?
78. 🟡 What are `pyproject.toml`, Poetry, `uv` and conda?
79. 🟡 What is `sys.path` and how does Python find modules?
80. 🟡 What causes circular imports and how do you fix them?

---

## 10. Iterators, Generators & Itertools

81. 🟡 What is an iterator? What is an iterable?
82. 🟡 What is a generator? What does `yield` do?
83. 🟡 Why are generators memory-efficient? Give a use case (reading a large file, streaming LLM tokens).
84. 🟡 What is `yield from`?
85. 🟡 What are useful `itertools` functions (`chain`, `islice`, `groupby`, `product`, `permutations`, `batched`)?

---

## 11. File Handling, JSON & CSV

86. 🟢 How do you read and write files in Python?
87. 🟢 What are file modes (`r`, `w`, `a`, `rb`, `wb`)?
88. 🟢 How do you read and write JSON (`json.load`, `json.dumps`)?
89. 🟡 How do you read and write CSV and Excel files (`csv`, `pandas`, `openpyxl`)?
90. 🟡 How do you work with paths (`pathlib`)?
91. 🟡 How do you read a very large file without loading it entirely into memory?

---

## 12. Concurrency — Threads, Multiprocessing, asyncio, GIL

92. 🟡 What is the GIL (Global Interpreter Lock)? How does it affect multithreading?
93. 🟡 What is the "free-threaded" (no-GIL) Python build in 3.13+?
94. 🟡 When should you use `threading` vs `multiprocessing` vs `asyncio`?
95. 🟡 What is `asyncio`? What are `async def` and `await`?
96. 🟡 How is Python's `async/await` similar to and different from C#'s?
97. 🟡 What is `concurrent.futures` (`ThreadPoolExecutor`, `ProcessPoolExecutor`)?
98. 🟡 How do you call multiple LLM APIs concurrently in Python (`asyncio.gather`)?

---

## 13. Type Hints & Pydantic

99. 🟢 What are type hints? Are they enforced at runtime?
100. 🟡 What are `Optional`, `Union`, `List`, `Dict`, `Any` and the new `X | Y` syntax?
101. 🟡 What is `mypy`?
102. 🟡 What is Pydantic? Why is it widely used in AI apps (validating LLM structured output, API models)?
103. 🟡 What is `TypedDict` and `Literal`?

---

## 14. Popular Libraries & FastAPI Basics

104. 🟢 What are the popular Python libraries for data and AI (NumPy, Pandas, Matplotlib, scikit-learn, PyTorch, TensorFlow, Hugging Face Transformers)?
105. 🟢 What is `requests` / `httpx`?
106. 🟢 What is Jupyter Notebook? When is it used?
107. 🟡 What is FastAPI? Why is it popular for serving AI models and APIs?
108. 🟡 How do you create a simple REST endpoint with FastAPI?
109. 🟡 What is the difference between Flask, Django and FastAPI?
110. 🟡 What is Uvicorn?
111. 🟡 How do you write tests in Python (`pytest`)?
112. 🟡 What are Ruff, Black and isort?

---

## 15. Python vs C# for .NET Developers

113. 🟡 What are the main differences between Python and C# (typing, performance, syntax, ecosystem)?
114. 🟡 What is the Python equivalent of LINQ (comprehensions, `map`/`filter`, itertools, Pandas)?
115. 🟡 What is the Python equivalent of C# properties, interfaces, generics and `using` statements?
116. 🟡 Why is Python dominant in AI/ML while C# is common in enterprise backends?
117. 🟡 How can a .NET application call Python code or models (REST/gRPC microservice, ONNX, Python.NET)?
118. 🔴 When would you build an AI feature in .NET directly vs in a separate Python service?

---

## 16. Python Predict-the-Output & Coding Tasks

119. 🟡 What is printed?
```python
a = [1, 2, 3]
b = a
b.append(4)
print(a, a is b)
```
120. 🟡 What is printed?
```python
def add(item, bucket=[]):
    bucket.append(item)
    return bucket
print(add(1)); print(add(2))
```
121. 🟡 What is printed?
```python
x = 10
def f():
    print(x)
    x = 5
f()
```
122. 🟡 What is printed?
```python
print([i * i for i in range(5) if i % 2 == 0])
print({k: v for k, v in zip("abc", [1, 2, 3])})
print(0.1 + 0.2 == 0.3)
from decimal import Decimal
print(Decimal("0.1") + Decimal("0.2") == Decimal("0.3"))
```
123. 🟡 What is printed?
```python
funcs = [lambda: i for i in range(3)]
print([f() for f in funcs])
```
124. 🟢 Reverse a string, check a palindrome, count character frequency.
125. 🟢 Remove duplicates from a list while preserving order.
126. 🟡 Find the second largest number in a list.
127. 🟡 Group a list of transactions (dicts) by category and sum amounts. 💰
128. 🟡 Read a CSV of transactions and find the top 5 customers by total amount using Pandas. 💰
129. 🟡 Write a decorator that retries a function 3 times on exception.
130. 🟡 Write a generator that yields chunks of a list of size N.
131. 🟡 Call a REST API with `httpx`, handle errors and parse JSON.
132. 🟡 Build a FastAPI endpoint that accepts JSON, validates it with Pydantic and returns a response.

---

# Part B — AI & ML Fundamentals

## 17. AI, ML, DL & GenAI — Concepts

133. 🟢 What is Artificial Intelligence?
134. 🟢 What is Machine Learning? How is it different from traditional programming?
135. 🟢 What is Deep Learning?
136. 🟢 What is Generative AI? How is it different from traditional (predictive) AI?
137. 🟢 What is the relationship between AI, ML, DL and GenAI?
138. 🟢 What is a model? What is training? What is inference?
139. 🟢 What are parameters and hyperparameters?
140. 🟡 What is narrow AI vs general AI (AGI)?
141. 🟡 What are real-world applications of AI in banking and fintech (fraud detection, credit scoring, chatbots, KYC, document processing)? 💰

---

## 18. Types of Machine Learning

142. 🟢 What is supervised learning? Give examples.
143. 🟢 What is unsupervised learning? Give examples.
144. 🟢 What is reinforcement learning? Give examples.
145. 🟡 What is semi-supervised and self-supervised learning?
146. 🟢 What is classification vs regression?
147. 🟢 What is clustering?
148. 🟡 What is anomaly detection? How is it used in fraud detection? 💰
149. 🟡 What is a recommendation system?
150. 🟡 What is transfer learning?

---

## 19. Data, Features & Preprocessing

151. 🟢 What is a dataset? What are features and labels?
152. 🟢 What is feature engineering?
153. 🟡 How do you handle missing values?
154. 🟡 What is normalization vs standardization?
155. 🟡 What is one-hot encoding vs label encoding?
156. 🟡 What is an imbalanced dataset? How do you handle it (oversampling, SMOTE, class weights)? 💰
157. 🟡 What is data leakage?
158. 🟡 What is dimensionality reduction (PCA)?
159. 🟡 Why is data quality more important than the algorithm?

---

## 20. Common ML Algorithms

160. 🟢 What is linear regression?
161. 🟢 What is logistic regression? Is it used for regression or classification?
162. 🟡 What is a decision tree?
163. 🟡 What is a random forest? What is bagging?
164. 🟡 What is gradient boosting (XGBoost, LightGBM)? Why is it popular for tabular data? 💰
165. 🟡 What is K-Nearest Neighbors (KNN)?
166. 🟡 What is K-Means clustering?
167. 🟡 What is a Support Vector Machine (SVM)?
168. 🟡 What is Naive Bayes?
169. 🟡 How do you choose an algorithm for a problem?

---

## 21. Training, Validation & Testing

170. 🟢 Why do we split data into training, validation and test sets?
171. 🟡 What is cross-validation (k-fold)?
172. 🟡 What is a loss function?
173. 🟡 What is gradient descent? What is the learning rate?
174. 🟡 What are epochs, batches and iterations?
175. 🟡 What is hyperparameter tuning (grid search, random search)?

---

## 22. Overfitting, Underfitting & Regularization

176. 🟢 What is overfitting? What is underfitting?
177. 🟡 What is the bias-variance trade-off?
178. 🟡 How do you prevent overfitting (more data, regularization, dropout, early stopping, simpler model)?
179. 🟡 What are L1 and L2 regularization?

---

## 23. Evaluation Metrics

180. 🟢 What is accuracy? Why can it be misleading?
181. 🟡 What are precision, recall and F1-score?
182. 🟡 What is a confusion matrix (TP, FP, TN, FN)?
183. 🟡 In fraud detection, is precision or recall more important? Why? 💰
184. 🟡 What is ROC curve and AUC?
185. 🟡 What are MAE, MSE, RMSE and R² for regression?
186. 🟡 What metrics are used for LLMs and RAG (faithfulness, relevance, BLEU/ROUGE, LLM-as-judge)?

---

## 24. NumPy, Pandas & scikit-learn Basics

187. 🟢 What is NumPy? What is a NumPy array? Why is it faster than a Python list?
188. 🟢 What is Pandas? What are `Series` and `DataFrame`?
189. 🟡 How do you read a CSV, filter rows, group by and aggregate in Pandas?
190. 🟡 How do you handle missing values in Pandas (`isna`, `fillna`, `dropna`)?
191. 🟡 What is `merge`/`join` in Pandas?
192. 🟡 What is scikit-learn? What are `fit`, `predict` and `transform`?
193. 🟡 What is a scikit-learn Pipeline?
194. 🟡 How do you save and load a trained model (`joblib`, `pickle`, ONNX)?
195. 🟡 What is ML.NET? When would a .NET team use it?

---

## 25. MLOps Basics

196. 🟡 What is MLOps?
197. 🟡 What is model deployment? How do you serve a model (REST API, batch, streaming)?
198. 🟡 What is model drift and data drift?
199. 🟡 What is model monitoring and retraining?
200. 🟡 What are MLflow, SageMaker and Azure ML used for?
201. 🔴 What is a feature store?

---

# Part C — Deep Learning & NLP Basics

## 26. Neural Networks

202. 🟢 What is a neural network? What are neurons, weights and biases?
203. 🟢 What are input, hidden and output layers?
204. 🟡 What is an activation function (ReLU, sigmoid, tanh, softmax)? Why is it needed?
205. 🟡 What is forward propagation and backpropagation?
206. 🟡 What is dropout?
207. 🟡 What are PyTorch and TensorFlow? What is a tensor?
208. 🟡 Why are GPUs used for deep learning?

---

## 27. CNNs, RNNs & Sequence Models (Overview)

209. 🟡 What is a Convolutional Neural Network (CNN)? What is it used for?
210. 🟡 What is a Recurrent Neural Network (RNN)? What is it used for?
211. 🟡 What are LSTM and GRU? What problem do they solve (vanishing gradients)?
212. 🟡 Why did transformers replace RNNs for most NLP tasks?

---

## 28. Transformers & Attention

213. 🟢 What is a transformer?
214. 🟡 What is the attention mechanism? What is self-attention?
215. 🟡 What are queries, keys and values in attention (high level)?
216. 🟡 What is multi-head attention?
217. 🟡 What are encoder-only (BERT), decoder-only (GPT, Claude, Llama) and encoder-decoder (T5) models?
218. 🟡 What is positional encoding?
219. 🟡 Why are transformers parallelizable during training?
220. 🔴 What is the "Attention Is All You Need" paper and why is it important?

---

## 29. NLP Basics — Tokenization & Embeddings

221. 🟢 What is Natural Language Processing (NLP)?
222. 🟢 What is tokenization? What are subword tokenizers (BPE, WordPiece)?
223. 🟡 What are stop words, stemming and lemmatization (classic NLP)?
224. 🟡 What is an embedding? Why are embeddings useful?
225. 🟡 What is the difference between word embeddings (Word2Vec) and contextual embeddings (BERT, modern embedding models)?
226. 🟡 What is semantic similarity?
227. 🟡 What are named entity recognition (NER), sentiment analysis and text classification?

---

# Part D — LLMs & Generative AI

## 30. LLM Fundamentals

228. 🟢 What is a Large Language Model (LLM)?
229. 🟢 How does an LLM generate text (next-token prediction)?
230. 🟢 What is pre-training? What data are LLMs trained on?
231. 🟡 What is instruction tuning and RLHF (Reinforcement Learning from Human Feedback)?
232. 🟡 What is a foundation model?
233. 🟡 What are popular LLMs (GPT, Claude, Gemini, Llama, Mistral, DeepSeek, Qwen)? Open-weight vs closed models?
234. 🟡 What are reasoning/"thinking" models? How are they different from standard chat models?
235. 🟡 What is the knowledge cutoff? Why does it matter?
236. 🟡 What are system, user and assistant messages?
237. 🟡 Are LLMs deterministic? Why can the same prompt give different answers?
238. 🟡 What are small language models (SLMs)? When would you use one (e.g., on-premise, edge, low cost)?
239. 🔴 What is a Mixture of Experts (MoE) model?

---

## 31. Tokens, Context Window & Generation Parameters

240. 🟢 What is a token? Roughly how many tokens is 1,000 words?
241. 🟢 What is a context window? What happens when the input exceeds it?
242. 🟡 Why do LLMs charge by input and output tokens?
243. 🟡 What is temperature? What happens at temperature 0 vs 1?
244. 🟡 What are top-p (nucleus sampling) and top-k?
245. 🟡 What is `max_tokens`? What are stop sequences?
246. 🟡 What is streaming (server-sent tokens) and why does it improve user experience?
247. 🟡 What is prompt caching and how does it reduce cost and latency?
248. 🟡 What is "lost in the middle" in long contexts?
249. 🔴 Long context vs RAG — when is putting everything in the context window enough?

---

## 32. Prompt Engineering

250. 🟢 What is prompt engineering?
251. 🟢 What is zero-shot, one-shot and few-shot prompting?
252. 🟡 What is a system prompt? What should it contain?
253. 🟡 What is chain-of-thought prompting?
254. 🟡 What are best practices for writing prompts (clear instructions, context, examples, format, constraints)?
255. 🟡 How do you use delimiters or XML tags to structure prompts?
256. 🟡 What is role prompting?
257. 🟡 How do you make an LLM say "I don't know" instead of guessing?
258. 🟡 What are prompt templates and prompt versioning?
259. 🟡 What is prompt chaining?
260. 🟡 What is "context engineering" and how is it different from prompt engineering?
261. 🔴 How do you test and evaluate prompt changes before deploying them?

---

## 33. Function / Tool Calling & Structured Output

262. 🟢 What is function calling / tool use in LLMs?
263. 🟡 How does tool calling work step by step (tool definitions → model requests a tool → app executes → result sent back → final answer)?
264. 🟡 Does the LLM execute the function itself?
265. 🟡 How do you define a tool schema (name, description, JSON schema parameters)?
266. 🟡 What is structured output / JSON mode? How do you guarantee valid JSON?
267. 🟡 How do you validate LLM output (Pydantic, JSON schema, C# records)?
268. 🟡 Give examples of tools for a banking assistant (get balance, list transactions, block card). 💰
269. 🔴 How do you prevent an LLM from calling a dangerous tool (e.g., transferring money) without user confirmation? 💰

---

## 34. Fine-Tuning, Adapters & Alignment

270. 🟢 What is fine-tuning?
271. 🟡 What is the difference between prompt engineering, RAG and fine-tuning? When do you use each?
272. 🟡 What is supervised fine-tuning (SFT)?
273. 🟡 What are LoRA and QLoRA (parameter-efficient fine-tuning)?
274. 🟡 What is model distillation?
275. 🟡 What is quantization (8-bit, 4-bit) and why is it used?
276. 🟡 Why is fine-tuning NOT the best way to teach a model new facts?
277. 🔴 What are DPO and RLHF in alignment (high level)?

---

## 35. Hallucinations & Grounding

278. 🟢 What is hallucination in LLMs?
279. 🟡 Why do LLMs hallucinate?
280. 🟡 How do you reduce hallucinations (RAG, grounding, citations, lower temperature, asking for "I don't know", verification)?
281. 🟡 What is grounding?
282. 🟡 How do you show sources/citations in an AI answer?
283. 🔴 Why are hallucinations especially dangerous in banking, legal and healthcare? 💰

---

## 36. Model Selection, Cost & Latency

284. 🟡 How do you choose an LLM for a use case (quality, cost, latency, context size, privacy, deployment options)?
285. 🟡 How do you estimate the monthly cost of an LLM feature?
286. 🟡 How do you reduce LLM cost (smaller models, caching, shorter prompts, routing, batching)?
287. 🟡 How do you reduce latency (streaming, smaller models, parallel calls, caching)?
288. 🟡 What is model routing (using a small model for simple queries and a large model for complex ones)?
289. 🟡 When would you self-host an open-weight model vs use an API (Bedrock, Azure OpenAI, Anthropic, OpenAI)? 💰
290. 🟡 What are Ollama, vLLM and LM Studio used for?
291. 🔴 How do you handle rate limits and outages from an LLM provider (retries, fallbacks, multiple providers)?

---

## 37. Multimodal & Other Generative Models

292. 🟡 What is a multimodal model (text + image + audio)?
293. 🟡 What are diffusion models (image generation) at a high level?
294. 🟡 What are speech-to-text (Whisper) and text-to-speech models?
295. 🟡 How can vision models be used for document processing (cheques, KYC documents, invoices)? 💰
296. 🟡 What is OCR and how is it combined with LLMs?

---

# Part E — Retrieval-Augmented Generation (RAG)

## 38. RAG Fundamentals

297. 🟢 What is RAG (Retrieval-Augmented Generation)?
298. 🟢 Why is RAG needed? What problems does it solve (outdated knowledge, private data, hallucinations)?
299. 🟢 What are the main steps of a RAG pipeline (ingest → chunk → embed → store → retrieve → augment prompt → generate)?
300. 🟡 What is the difference between the indexing pipeline and the query pipeline?
301. 🟡 RAG vs fine-tuning — when do you use each?
302. 🟡 What are the limitations of naive RAG?
303. 🟡 How do you add citations to RAG answers?
304. 🟡 How do you keep a RAG index up to date when documents change?
305. 💰 Give examples of RAG use cases in banking (policy Q&A, product information, internal SOPs, compliance documents).

---

## 39. Embeddings & Similarity Search

306. 🟢 What is a vector embedding?
307. 🟡 How are embeddings created (embedding models like text-embedding-3, Titan, Cohere, BGE, E5)?
308. 🟡 What is the dimension of an embedding? Does a higher dimension always mean better quality?
309. 🟡 What are cosine similarity, dot product and Euclidean distance?
310. 🟡 Why must the same embedding model be used for indexing and querying?
311. 🟡 What happens if you change the embedding model later?
312. 🟡 What is approximate nearest neighbour (ANN) search? Why not exact search?
313. 🟡 What are HNSW and IVF indexes?
314. 🔴 What are multilingual embeddings (useful for Hindi/regional languages)?

---

## 40. Chunking & Document Processing

315. 🟢 What is chunking? Why is it needed?
316. 🟡 What chunking strategies exist (fixed size, overlap, sentence/paragraph, recursive, semantic, document-structure-based)?
317. 🟡 How do you choose chunk size and overlap?
318. 🟡 What problems occur if chunks are too small or too large?
319. 🟡 How do you extract text from PDFs, Word, Excel, HTML and scanned documents?
320. 🟡 How do you handle tables and images in documents for RAG?
321. 🟡 What metadata should you store with each chunk (source, page, date, department, access level)?
322. 🔴 What is parent-child / small-to-big chunking?

---

## 41. Vector Databases

323. 🟢 What is a vector database?
324. 🟡 What are popular vector databases (pgvector, Pinecone, Qdrant, Weaviate, Milvus, Chroma, OpenSearch/Elasticsearch, Redis, Azure AI Search, Amazon OpenSearch Serverless)?
325. 🟡 What is pgvector? How do you store and query embeddings in PostgreSQL?
326. 🟡 What index types does pgvector support (IVFFlat, HNSW)?
327. 🟡 Can you use YugabyteDB, SQL Server or Oracle for vectors (vector types in newer versions)?
328. 🟡 Why might a team choose pgvector instead of a dedicated vector database?
329. 🟡 How do you filter vector search by metadata (e.g., department, date, user permissions)?
330. 🔴 How do you scale vector search to millions of chunks?

---

## 42. Retrieval, Hybrid Search & Re-ranking

331. 🟡 What is top-k retrieval?
332. 🟡 What is keyword search (BM25) vs semantic search?
333. 🟡 What is hybrid search? Why does it often perform better?
334. 🟡 What is re-ranking? What are cross-encoder re-rankers?
335. 🟡 What is query rewriting / query expansion?
336. 🟡 What is HyDE (Hypothetical Document Embeddings)?
337. 🟡 What is Maximal Marginal Relevance (MMR)?
338. 🔴 Why does semantic search sometimes fail for exact terms like account numbers, product codes or IFSC codes? 💰

---

## 43. Advanced RAG Patterns

339. 🟡 What is multi-query RAG?
340. 🟡 What is conversational RAG (using chat history to rewrite queries)?
341. 🟡 What is agentic RAG?
342. 🟡 What is GraphRAG / knowledge graph RAG?
343. 🟡 What is corrective RAG and self-RAG?
344. 🟡 What is contextual retrieval (adding context to chunks before embedding)?
345. 🟡 How do you combine RAG with SQL queries over structured data (text-to-SQL)? 💰
346. 🔴 How do you enforce document-level access control in RAG so users only see documents they are allowed to? 💰

---

## 44. RAG Evaluation

347. 🟡 How do you evaluate a RAG system?
348. 🟡 What are retrieval metrics (recall@k, precision@k, MRR, nDCG)?
349. 🟡 What are generation metrics (faithfulness/groundedness, answer relevance, context relevance)?
350. 🟡 What is LLM-as-a-judge? What are its limitations?
351. 🟡 What is a golden dataset / evaluation set?
352. 🟡 What tools exist for RAG evaluation (RAGAS, DeepEval, TruLens, Promptfoo, LangSmith)?
353. 🔴 How do you debug a RAG system that gives wrong answers (retrieval problem vs generation problem)?

---

# Part F — AI Agents & MCP

## 45. AI Agents Fundamentals

354. 🟢 What is an AI agent?
355. 🟢 How is an agent different from a chatbot or a simple LLM call?
356. 🟡 What is the agent loop (observe → think → act → observe)?
357. 🟡 What is the ReAct pattern?
358. 🟡 What are workflows vs agents? When should you prefer a deterministic workflow?
359. 🟡 What are the risks of autonomous agents (wrong actions, loops, cost, security)?
360. 🟡 What is human-in-the-loop? Why is it important for financial actions? 💰
361. 🔴 How do you limit an agent (max steps, budgets, allowed tools, approvals)?

---

## 46. Tools, Planning & Memory

362. 🟡 What are tools in an agent system?
363. 🟡 How should tool descriptions be written so the model uses them correctly?
364. 🟡 What is planning in agents?
365. 🟡 What is short-term memory (conversation history) vs long-term memory?
366. 🟡 How do you manage long conversations (summarisation, trimming, memory stores)?
367. 🟡 What is a code interpreter / sandboxed execution tool?
368. 🔴 How do you make agent tools idempotent and safe to retry? 💰

---

## 47. Multi-Agent Systems & Workflows

369. 🟡 What is a multi-agent system?
370. 🟡 What are orchestrator-worker, router and supervisor patterns?
371. 🟡 What are agent frameworks (LangGraph, CrewAI, AutoGen, Semantic Kernel Agents / Microsoft Agent Framework, OpenAI Agents SDK, Claude Agent SDK, AWS Bedrock Agents)?
372. 🟡 When is a multi-agent system overkill?
373. 🔴 What is the A2A (Agent-to-Agent) protocol?

---

## 48. Model Context Protocol (MCP)

374. 🟢 What is the Model Context Protocol (MCP)?
375. 🟡 What problem does MCP solve?
376. 🟡 What are MCP hosts, clients and servers?
377. 🟡 What do MCP servers expose (tools, resources, prompts)?
378. 🟡 What transports does MCP support (stdio, streamable HTTP)?
379. 🟡 How is MCP different from regular function calling?
380. 🟡 How would you build an MCP server in C# (.NET MCP SDK) or Python?
381. 🔴 What are the security risks of MCP servers (tool poisoning, over-permissioned tools, data exfiltration) and how do you mitigate them? 💰

---

# Part G — Building AI Applications

## 49. AI in .NET — Semantic Kernel, Microsoft.Extensions.AI, Azure OpenAI

382. 🟡 How can a .NET developer integrate LLMs into an ASP.NET Core application?
383. 🟡 What is Microsoft.Extensions.AI (`IChatClient`, `IEmbeddingGenerator`)?
384. 🟡 What is Semantic Kernel? What are plugins/functions in Semantic Kernel?
385. 🟡 What is the Microsoft Agent Framework (successor combining Semantic Kernel and AutoGen)?
386. 🟡 How do you call Azure OpenAI, OpenAI, Anthropic or AWS Bedrock from C#?
387. 🟡 How do you stream LLM responses from an ASP.NET Core API to Angular/React (SSE, `IAsyncEnumerable`)?
388. 🟡 How do you implement RAG in .NET (Microsoft.Extensions.VectorData, pgvector with Npgsql, Azure AI Search)?
389. 🟡 How do you implement tool calling in .NET?
390. 🟡 How do you run models locally from .NET (Ollama, ONNX Runtime, Foundry Local)?
391. 🟡 What is ML.NET vs Semantic Kernel vs Microsoft.Extensions.AI — when to use each?
392. 🔴 How do you add retries, timeouts, rate limiting and caching to LLM calls in .NET (Polly, `IDistributedCache`)?

---

## 50. Python AI Frameworks — LangChain, LlamaIndex, LangGraph

393. 🟡 What is LangChain? What are chains, prompts, retrievers and tools?
394. 🟡 What is LlamaIndex? How is it different from LangChain?
395. 🟡 What is LangGraph? Why is it used for agents?
396. 🟡 What is Hugging Face? What are the Transformers library and model hub?
397. 🟡 What are the criticisms of heavy frameworks, and when should you use plain SDK calls instead?

---

## 51. Cloud AI Services — AWS Bedrock, Azure OpenAI, SageMaker

398. 🟡 What is Amazon Bedrock? Which models does it provide?
399. 🟡 What are Bedrock Knowledge Bases, Agents and Guardrails?
400. 🟡 What is Azure OpenAI / Azure AI Foundry?
401. 🟡 What is Amazon SageMaker? When would you use it instead of Bedrock?
402. 🟡 What are Amazon Textract and Comprehend used for (documents, entities)? 💰
403. 🟡 How do you keep data private when using cloud LLMs (no training on your data, private endpoints, region selection)? 💰
404. 🔴 Which AWS region and data residency considerations apply when using LLMs for Indian banking data? 💰

---

## 52. LLMOps — Evaluation, Observability, Versioning

405. 🟡 What is LLMOps?
406. 🟡 How do you evaluate an LLM feature before release (test sets, human review, automated evals)?
407. 🟡 What should you log for LLM calls (prompt version, model, tokens, latency, cost, outcome) — and what must you NOT log? 💰
408. 🟡 What are LLM observability tools (LangSmith, Langfuse, Arize Phoenix, OpenTelemetry GenAI conventions)?
409. 🟡 How do you version prompts and models?
410. 🟡 How do you do A/B testing of prompts or models?
411. 🟡 How do you monitor quality in production (user feedback, sampling, evals)?
412. 🔴 How do you handle a model provider updating or deprecating a model you depend on?

---

## 53. AI Security — Prompt Injection, Data Leakage, Guardrails

413. 🟢 What is prompt injection? What is indirect prompt injection?
414. 🟡 What is jailbreaking?
415. 🟡 How do you defend against prompt injection (input validation, separating instructions from data, least-privilege tools, output filtering, human approval)?
416. 🟡 What is data leakage through LLMs (PII in prompts, training data, logs)? 💰
417. 🟡 How do you mask PII before sending data to an LLM (account numbers, PAN, Aadhaar, card numbers)? 💰
418. 🟡 What are guardrails? Give examples (Bedrock Guardrails, NeMo Guardrails, Azure Content Safety).
419. 🟡 What is the OWASP Top 10 for LLM Applications?
420. 🔴 How do you secure a RAG system so that a user can't retrieve documents they don't have access to? 💰
421. 🔴 How can a malicious document in your RAG index manipulate the assistant?

---

## 54. Responsible AI, Privacy & Compliance

422. 🟡 What is responsible AI? What are its principles (fairness, transparency, accountability, privacy, safety)?
423. 🟡 What is bias in AI models? How can it affect loan approvals or credit scoring? 💰
424. 🟡 What is explainability (XAI)? Why do regulators require it in finance? 💰
425. 🟡 What regulations apply to AI and data (DPDP Act in India, GDPR, EU AI Act, RBI guidelines)? 💰
426. 🟡 Should an AI system make final decisions on loans or fraud blocking? Why or why not? 💰
427. 🟡 How do you get user consent and disclose that users are talking to AI?

---

## 55. Financial-Domain AI Use Cases 💰

428. 🟡💰 How is ML used for fraud detection in card and UPI transactions?
429. 🟡💰 How is ML used for credit scoring and loan approval?
430. 🟡💰 How would you build a customer-support chatbot for a bank using RAG?
431. 🟡💰 How would you build an assistant that answers questions about a customer's own transactions safely (tool calling + authorization)?
432. 🟡💰 How would you use LLMs to extract data from KYC documents, bank statements or invoices?
433. 🟡💰 How would you use AI to classify transactions into categories (food, travel, bills)?
434. 🟡💰 How would you use AI to help compliance teams search regulations and internal policies?
435. 🟡💰 How would you use AI for anomaly detection in logs and monitoring?
436. 🔴💰 What are the risks of using LLMs in customer-facing banking applications?

---

# Part H — Practice

## 56. Tricky Questions

437. 🟡 Is a bigger model always better?
438. 🟡 Does setting temperature to 0 guarantee the same output every time?
439. 🟡 Does RAG eliminate hallucinations completely?
440. 🟡 Can you "teach" an LLM your company's latest policies by fine-tuning it?
441. 🟡 Does an LLM "know" today's date or the latest news?
442. 🟡 Does the LLM run your function when you use tool calling?
443. 🟡 Why can an LLM do complex reasoning but fail at counting letters in a word?
444. 🟡 Why can't you just put all your company documents into one prompt?
445. 🟡 Why does semantic search miss exact matches like "IFSC HDFC0001234"? 💰
446. 🟡 Why do two embedding models produce incompatible vectors?
447. 🟡 Is 99% accuracy good for a fraud detection model? 💰
448. 🟡 Is AI-generated code safe to merge without review?
449. 🟡 Can an LLM safely be given direct write access to a production database? 💰
450. 🟡 Why is Python slower than C# but still dominant in AI?
451. 🔴 What happens to your RAG answers if documents in the index are outdated or contradictory?
452. 🔴 Why is "agent" sometimes the wrong solution when a simple workflow would do?

---

## 57. Scenario-Based Questions

453. 🟡 Your manager asks you to add a "chat with our product documentation" feature to an ASP.NET Core + Angular/React app. How do you build it?
454. 🟡 Your RAG chatbot gives confident but wrong answers. How do you find out whether the problem is retrieval or generation?
455. 🟡 Your RAG system retrieves irrelevant chunks. What do you change (chunking, embeddings, hybrid search, re-ranking, metadata filters)?
456. 🟡 Your LLM feature costs ₹5 lakh per month and the CFO wants it halved. What do you do?
457. 🟡 Your chatbot is slow (8 seconds per answer). How do you improve the user experience and latency?
458. 🟡 The LLM sometimes returns invalid JSON and your C# deserialization fails. How do you fix it?
459. 🟡 A user tricks your chatbot into revealing its system prompt. How do you prevent it?
460. 🟡 A user asks the banking assistant "What is my balance?" How do you design it so it only shows *their* balance? 💰
461. 🟡 The compliance team forbids sending customer PII to external LLM APIs. What options do you have? 💰
462. 🟡 Your company wants to use AI to auto-approve small loans. What concerns would you raise? 💰
463. 🟡 You need to process 10,000 scanned KYC documents per day. Design the pipeline. 💰
464. 🟡 The LLM provider is down for 30 minutes. How does your application behave?
465. 🟡 Users complain that the chatbot forgets earlier parts of the conversation. How do you handle memory?
466. 🟡 You must choose between Bedrock, Azure OpenAI and a self-hosted Llama model. How do you decide? 💰
467. 🟡 An agent with a "send email" tool sent 200 emails in a loop. How do you prevent this?
468. 🔴 A document uploaded to your RAG index contains hidden instructions ("ignore previous instructions and..."). How do you protect the system?
469. 🔴 Your team wants to build an AI agent that can initiate fund transfers on behalf of customers. What controls do you require? 💰

---

## 58. AI System Design Questions

470. 🟡 Design a RAG-based Q&A system over 50,000 internal PDF documents with access control. 💰
471. 🟡 Design a customer-support chatbot for a bank with escalation to a human agent. 💰
472. 🟡 Design a document extraction system for invoices/KYC using OCR + LLMs. 💰
473. 🟡 Design a semantic search feature for an e-commerce catalogue using pgvector.
474. 🟡 Design an AI assistant inside your .NET + React/Angular app that can call internal APIs via tools.
475. 🔴 Design a real-time fraud detection system combining rules and ML models. 💰
476. 🔴 Design an LLM gateway service for your company (multiple providers, rate limiting, caching, logging, PII masking, cost tracking). 💰
477. 🔴 Design an MCP server that exposes your company's internal APIs to AI assistants safely.

---

## 59. Hands-On Tasks

478. 🟢 Set up a Python virtual environment and install packages with `pip` or `uv`.
479. 🟢 Write a Python script that reads a CSV and summarises it with Pandas.
480. 🟡 Train a simple classification model with scikit-learn and report precision, recall and F1.
481. 🟡 Build a FastAPI endpoint that serves predictions from a trained model.
482. 🟡 Call an LLM API (OpenAI/Anthropic/Bedrock) from Python and from C#.
483. 🟡 Stream LLM responses from an ASP.NET Core endpoint to a React/Angular UI.
484. 🟡 Implement tool calling with two tools (e.g., `get_weather`, `get_account_balance` with mock data).
485. 🟡 Generate embeddings for 100 documents and store them in PostgreSQL with pgvector.
486. 🟡 Build a simple RAG pipeline: load PDFs → chunk → embed → store → retrieve → answer with citations.
487. 🟡 Add hybrid search (BM25 + vector) and compare results.
488. 🟡 Get structured JSON output from an LLM and validate it with Pydantic or a C# record.
489. 🟡 Create an evaluation set of 20 questions and measure your RAG system's answers.
490. 🟡 Build a simple agent with a loop, max steps and two tools.
491. 🟡 Build a simple MCP server (Python or C#) that exposes one tool and connect it to an MCP client.
492. 🔴 Add PII masking (account numbers, PAN, mobile) before sending text to an LLM. 💰
493. 🔴 Add logging of tokens, latency and cost for every LLM call with OpenTelemetry.

---

## 60. Rapid-Fire Round

494. 🟢 What does LLM stand for?
495. 🟢 What does RAG stand for?
496. 🟢 What does MCP stand for?
497. 🟢 What architecture do modern LLMs use?
498. 🟢 What is the basic unit of text for an LLM?
499. 🟢 Which parameter controls randomness?
500. 🟢 What converts text into vectors?
501. 🟢 Which PostgreSQL extension stores vectors?
502. 🟢 Which similarity measure is most common for embeddings?
503. 🟢 What is it called when an LLM makes up facts?
504. 🟡 Which Python library is used for DataFrames?
505. 🟡 Which Python library is used for classic ML?
506. 🟡 Which Python web framework is popular for AI APIs?
507. 🟡 Which Python library validates data models?
508. 🟡 What limits true parallel threads in standard CPython?
509. 🟡 Which .NET abstraction provides `IChatClient`?
510. 🟡 Which Microsoft SDK provides plugins and agents for .NET?
511. 🟡 Which AWS service provides managed foundation models?
512. 🟡 Which metric matters more for fraud detection when missing fraud is costly — precision or recall?
513. 🟡 What is the most common ANN index type in vector databases?
514. 🔴 What is the difference between RAG and fine-tuning in one line?
515. 🔴 What is the difference between an agent and a workflow in one line?
516. 🔴 What is the difference between function calling and MCP in one line?
517. 🔴 What is the difference between precision and recall in one line?
518. 🔴 What is the difference between `json` and structured output with a schema in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux · Part 12 — Redis · Part 13 — AWS · Part 14 — JavaScript · Part 15 — jQuery & AJAX · Part 16 — Angular · Part 17 — React (Zustand & TanStack Query) · Part 18 — HR & Manager Round · Part 19 — Python, AI, ML, LLM & RAG.
