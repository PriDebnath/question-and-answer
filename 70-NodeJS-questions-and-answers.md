# 70 NodeJS Questions and Answers

1. What is Node.js?
Answer:
Node.js is a JavaScript runtime built on Chrome's V8 engine. It lets us run JavaScript on the server to build scalable backend applications.
---
2. Why use Node.js?
Answer:
Because it's fast, non-blocking, event-driven, and great for APIs, real-time apps, and microservices.
---
3. What is the V8 engine?
Answer:
V8 is Google's JavaScript engine that compiles JavaScript into machine code for fast execution.
---
4. What is the Event Loop?
Answer:
The Event Loop continuously checks the call stack and callback queues. When the call stack is empty, it paces pending asynchronous callbacks to call stack for execution, allowing Node.js to handle many concurrent operations without blocking the main JavaScript thread.
---
5. What is non-blocking I/O?
Answer:
Instead of waiting for an operation like reading a file to finish, Node.js continues executing other code and handles the result later.
---
6. What is asynchronous programming?
Answer:
It allows tasks to run without blocking the main thread using callbacks, Promises, or async/await.
---
7. Difference between synchronous and asynchronous code?
Answer:
Synchronous waits for one task to finish before starting another. Asynchronous allows other work while waiting.
---
8. What are callbacks?
Answer:
Callbacks are functions passed to another function that execute after an operation completes.
---
9. What is callback hell?
Answer:
It's deeply nested callbacks that make code difficult to read and maintain.
---
10. How do you avoid callback hell?
Answer:
By using Promises, async/await, or breaking logic into smaller functions.
---
11. What are Promises?
Answer:
Promises represent the future result of an asynchronous operation.
---
12. What is async/await?
Answer:
It's syntax built on Promises that makes asynchronous code easier to read.
---
13. Difference between Promise and async/await?
Answer:
Async/await is cleaner and easier to write, but internally it uses Promises.
---
14. What is npm?
Answer:
npm is Node.js's package manager used to install and manage dependencies.
---
15. What is package.json?
Answer:
It stores project metadata, scripts, dependencies, and version information.
---
16. What is package-lock.json?
Answer:
It locks dependency versions so every installation uses the same package versions.
---
17. What is npx?
Answer:
npx runs packages without installing them globally.
---
18. Difference between dependencies and devDependencies?
Answer:
Dependencies are required in production. DevDependencies are only needed during development.
---
19. What are modules?
Answer:
Modules are reusable pieces of code that can be imported into other files.
---
20. Difference between CommonJS and ES Modules?
Answer:
CommonJS uses require(). ES Modules use import and export.
---
21. What is Express.js?
Answer:
Express is a minimal framework for building web servers and REST APIs with Node.js.
---
22. What is middleware?
Answer:
Middleware is a function that runs between receiving a request and sending a response.
---
23. Why do we use middleware?
Answer:
For authentication, logging, validation, error handling, and request processing.
---
24. What is REST API?
Answer:
A REST API lets clients communicate with a server using HTTP methods like GET, POST, PUT, and DELETE.
---
25. Difference between PUT and PATCH?
Answer:
PUT replaces the entire resource. PATCH updates only specified fields.
---
26. Difference between authentication and authorization?
Answer:
Authentication verifies who the user is. Authorization checks what they are allowed to access.
---
27. What is JWT?
Answer:
JWT is a token used for securely identifying authenticated users between client and server.
---
28. Where do you store JWT?
Answer:
For web applications, HTTP-only cookies are generally preferred because they help protect against XSS. For APIs used by mobile or non-browser clients, tokens are often stored securely by the client and sent in the Authorization header.
---
29. What is CORS?
Answer:
CORS allows or restricts requests between different origins.
---
30. Why use environment variables?
Answer:
To keep secrets like API keys and database credentials outside the source code.
---
31. What is dotenv?
Answer:
It loads environment variables from a .env file into the application.
---
32. What is event-driven architecture?
Answer:
It's a design where actions trigger events, and listeners respond to those events.
---
33. What is the EventEmitter?
Answer:
It's a Node.js class used to create and listen for custom events.
---
34. What are Streams?
Answer:
Streams process data in chunks instead of loading everything into memory.
---
35. Types of streams?
Answer:
Readable, Writable, Duplex, and Transform streams.
---
36. Why are streams useful?
Answer:
They reduce memory usage and improve performance when handling large files.
---
37. What is clustering?
Answer:
Clustering allows a Node.js application to use multiple CPU cores by running multiple processes.(Generally solved by multiple docker container now a days)
---
38. What is child_process?
Answer:
It lets Node.js create and communicate with separate processes.
---
39. What is buffering?
Answer:
A Buffer stores binary data directly in memory.
----
40. How do you handle errors in async code?
Answer:
Using try/catch with async/await or .catch() with Promises.
---
41. What is rate limiting?
Answer:
It restricts how many requests a client can make within a specific time.
---
42. What is hashing?
Answer:
Hashing converts data into a fixed-length value, commonly used for storing passwords securely.
---
43. Why use bcrypt?
Answer:
bcrypt securely hashes passwords and adds salt to protect against attacks.
---
44. What is WebSocket?
Answer:
WebSocket provides full-duplex, real-time communication between client and server.
---
45. When would you use Socket.IO?
Answer:
For chat apps, live notifications, multiplayer games, and real-time dashboards.
---
46. How do you improve Node.js performance?
Answer:
Use caching, asynchronous operations, streams, database indexing, connection pooling, and clustering when appropriate.
---
47. What is Redis used for?
Answer:
Redis is used for caching, session storage, queues, and rate limiting.
---
48. What logging library have you used?
Answer:
I've used console logging for development and libraries like  Pino for structured logging.
---
49. Describe a Node.js project you've built.
Answer:
I built a chat application using Express, Socket.IO, JWT authentication, and PostgreSQL, where users can send real-time messages and see online status.
---
50. Why should we hire you as a Node.js developer?
Answer:
I have hands-on experience building REST APIs and real-time applications with Node.js, Express, JWT authentication, databases, and Socket.IO. I'm comfortable learning new technologies and writing clean, maintainable code.
---
51. What is libuv?
Answer:
libuv is the C library used by Node.js that provides the Event Loop, asynchronous I/O, networking, file system operations, and the thread pool.
---
52. Is Node.js single-threaded?
Answer:
JavaScript execution in Node.js is single-threaded, but Node.js itself uses libuv, a thread pool, and can create additional processes or worker threads for parallel work.
----
53. Which operations use the thread pool?
Answer:
Operations such as file system (fs), cryptography (crypto), DNS lookups, and compression (zlib) use the libuv thread pool
---
54. What is express.Router()?
Answer:
express.Router() creates modular route handlers, making it easier to organize routes into separate files.
---
55. What is error-handling middleware?
Answer:
It's Express middleware that catches errors and sends appropriate responses. It has four parameters: (err, req, res, next)
---
56. What's the difference between app.use() and app.get()?
Answer:
app.use() registers middleware for one or more routes, while app.get() handles only GET requests for a specific route.
---
57. Which HTTP status codes do you commonly use?
Answer:
200 – OK
201 – Created
204 – No Content
400 – Bad Request
401 – Unauthorized
403 – Forbidden
404 – Not Found
409 – Conflict
500 – Internal Server Error
---
58. What is CSRF?
Answer:
Cross-Site Request Forgery (CSRF) tricks an authenticated user into performing unwanted actions on a website.
---
59. What is XSS?
Answer:
Cross-Site Scripting (XSS) is an attack where malicious JavaScript is injected into a webpage and executed in users' browsers.
---
60. What is SQL Injection?
Answer:
SQL Injection is an attack where malicious SQL is inserted into queries to read or modify database data.
---
61. How do you secure an Express application?
Answer:
Use HTTPS, validate inputs, hash passwords with bcrypt, use Helmet, enable CORS properly, rate limit requests, authenticate users, and store secrets in environment variables.
---
62. How do you deploy a Node.js application?
Answer:
Typically by building the application, setting environment variables, running it with a process manager like PM2 or inside Docker, and placing Nginx as a reverse proxy.
---
63. Why use Nginx in front of Node.js?
Answer:
Nginx acts as a reverse proxy, handles SSL termination, serves static files efficiently, load balances requests, and improves security.
---
64. What is MVC?
Answer:
MVC (Model-View-Controller) separates data (Model), business logic (Controller), and user interface (View) to improve code organization.
---
65. What is a service layer?
Answer:
A service layer contains business logic between controllers and the database, making code more reusable and easier to test.
---
66. How do you structure a large Express project?
Answer:
Organize code into folders such as routes, controllers, services, models, middleware, utilities, and configuration for better maintainability.
---
67. What causes Event Loop blocking?
Answer:
CPU-intensive tasks, large synchronous loops, synchronous file operations, or complex calculations can block the Event Loop and delay other requests.
--&
68. Explain the request lifecycle in Express.
Answer:
A request reaches the Express server, passes through middleware, reaches the matching route handler, performs business logic and database operations, then sends a response back to the client.

---
69. What is caching?
Answer:
Caching stores frequently accessed data in fast storage, such as Redis or memory, reducing database queries and improving response times.
---
70. When would you use queues like BullMQ?
Answer:
Use queues for long-running background tasks such as sending emails, generating reports, processing images, or handling scheduled jobs without blocking incoming requests.
---
