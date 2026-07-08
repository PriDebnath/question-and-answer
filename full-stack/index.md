## 100 full-stack interview questions with strong, interview-ready answers.

### Core Web + Frontend
1. What is the difference between HTML, CSS, and JavaScript?
HTML gives structure, CSS controls presentation, and JavaScript adds behavior and interactivity.

2. What is the DOM?
The DOM is the browser’s object representation of an HTML document. JavaScript can read and update it dynamically.

3. What is the difference between id and class in CSS?
An id is unique for one element, while a class can be reused on multiple elements.

4. What is responsive design?
Responsive design means a website adapts to different screen sizes and devices using flexible layouts, media queries, and scalable units.

5. What is the box model?
Every element is made of content, padding, border, and margin. Understanding this helps control spacing and sizing.

6. What is the difference between display: none and visibility: hidden?
display: none removes the element from layout. visibility: hidden hides it but keeps the space.

7. What is semantic HTML?
Semantic HTML uses meaningful tags like header, main, article, and footer to improve readability, accessibility, and SEO.

8. What is accessibility in frontend development?
Accessibility means making apps usable for everyone, including users with disabilities, through keyboard support, ARIA, labels, and proper contrast.

9. What is the difference between localStorage and sessionStorage?
localStorage persists until manually cleared. sessionStorage lasts only for the current tab session.

10. What are cookies?
Cookies are small pieces of data stored in the browser, often used for authentication, preferences, and tracking.

### JavaScript Fundamentals
11. What is the difference between var, let, and const?
var is function-scoped, while let and const are block-scoped. const cannot be reassigned.

12. What is hoisting in JavaScript?
Hoisting is JavaScript moving declarations to the top of their scope during compilation.

13. What is the difference between == and ===?
== compares values after type coercion. === compares both value and type, so it is safer.

14. What is a closure?
A closure is when a function remembers variables from its outer scope even after the outer function has finished.

15. What is the event loop?
The event loop handles asynchronous tasks by moving completed callbacks from the task queue to the call stack.

16. What is a Promise?
A Promise represents the future result of an asynchronous operation: pending, fulfilled, or rejected.

17. What is async/await?
async/await is syntax built on Promises that makes asynchronous code easier to read and write.

18. What is callback hell?
Callback hell happens when nested callbacks become difficult to read and maintain. Promises and async/await help solve it.

19. What is the difference between map, filter, and reduce?
map transforms items, filter selects items, and reduce combines items into one result.

20. What is destructuring?
Destructuring is a syntax that extracts values from arrays or objects into variables.

### React / Frontend Frameworks
21. What is React?
React is a JavaScript library for building user interfaces using reusable components.

22. What is a component in React?
A component is a reusable piece of UI that can manage its own logic and state.

23. What is the difference between props and state?
Props are read-only inputs passed from parent to child. State is internal data that can change over time.

24. What is the virtual DOM?
The virtual DOM is a lightweight copy of the real DOM. React uses it to update only what changed.

25. What are React hooks?
Hooks are functions that let functional components use features like state, lifecycle, and context.

26. What does useState do?
It lets a component store and update local state.

27. What does useEffect do?
It runs side effects such as fetching data, subscriptions, or DOM updates after rendering.

28. What is the dependency array in useEffect?
It controls when the effect runs. It reruns when one of the listed values changes.

29. What is prop drilling?
Prop drilling is passing props through multiple levels of components when only a deep child needs them.

30. How do you avoid unnecessary re-renders in React?
By using React.memo, useMemo, useCallback, proper state placement, and avoiding unnecessary parent updates.

### Backend Basics
31. What is backend development?
Backend development handles business logic, authentication, APIs, database operations, and server-side processing.

32. What is REST API?
REST is an architectural style for designing APIs around resources and HTTP methods like GET, POST, PUT, and DELETE.

33. What is the difference between PUT and PATCH?
PUT usually replaces the full resource, while PATCH updates only specific fields.

34. What is middleware?
Middleware is code that runs between request and response, often used for auth, logging, validation, and error handling.

35. What is the difference between synchronous and asynchronous code?
Synchronous code runs step by step. Asynchronous code allows other work to continue while waiting for tasks like I/O.

36. What is MVC?
MVC stands for Model, View, and Controller. It separates data, UI, and application logic.

37. What is server-side rendering?
SSR means the server generates HTML before sending it to the browser, which can improve initial load and SEO.

38. What is CORS?
CORS is a browser security mechanism that controls whether one origin can access resources from another origin.

39. What is authentication?
Authentication verifies who the user is, usually through login credentials, tokens, or sessions.

40. What is authorization?
Authorization decides what an authenticated user is allowed to do.

### Node.js / Express
41. What is Node.js?
Node.js is a JavaScript runtime built on Chrome’s V8 engine, commonly used for server-side development.

42. Why is Node.js good for APIs?
It handles many I/O operations efficiently and works well for fast, scalable API services.

43. What is Express.js?
Express is a minimal Node.js framework for building web servers and APIs.

44. What is an Express route?
A route maps an HTTP method and URL path to a handler function.

45. What is error handling in Express?
Error handling catches failures and sends proper responses instead of crashing the server.

46. What is the difference between req.params, req.query, and req.body?
params comes from the URL path, query comes from the URL string, and body contains request data sent by the client.

47. How do you validate request data?
By checking types, required fields, formats, and business rules using validation libraries or custom logic.

48. What is rate limiting?
Rate limiting restricts how many requests a user can make in a time period to protect the server.

49. What is logging?
Logging records important events, errors, and requests for debugging, monitoring, and auditing.

50. What is environment configuration?
It means storing values like database URLs, secrets, and API keys outside the code, usually in environment variables.

### Databases
51. What is a database?
A database is a system for storing and retrieving data efficiently.

52. What is the difference between SQL and NoSQL?
SQL databases are relational and use structured tables. NoSQL databases are more flexible and support document, key-value, graph, or wide-column models.

53. What is a primary key?
A primary key uniquely identifies each row in a table.

54. What is a foreign key?
A foreign key links one table to another and maintains relationship integrity.

55. What is normalization?
Normalization organizes data to reduce duplication and improve consistency.

56. What is denormalization?
Denormalization intentionally duplicates some data to improve read performance.

57. What is an index?
An index speeds up data retrieval, but it can slow down inserts and updates because it must also be maintained.

58. What is a JOIN?
A JOIN combines rows from two or more tables based on a related column.

59. What is a transaction?
A transaction is a group of database operations that succeed or fail together.

60. What are ACID properties?
ACID means Atomicity, Consistency, Isolation, and Durability. These ensure reliable transactions.

### ORM / Data Access
61. What is an ORM?
An ORM maps database tables to application objects, making database operations easier in code.

62. Why use an ORM?
It improves developer productivity, reduces raw SQL repetition, and helps with portability and maintainability.

63. What is the downside of an ORM?
It can sometimes generate inefficient queries if used poorly, and complex queries may still need raw SQL.

64. What is lazy loading?
Lazy loading fetches data only when it is needed.

65. What is eager loading?
Eager loading fetches related data immediately in one query or during the initial request.

66. What is an N+1 query problem?
It happens when one query loads a list and then many extra queries are made for related data, causing poor performance.

67. How do you avoid N+1 queries?
By using joins, eager loading, batching, or optimized query patterns.

68. What is pagination?
Pagination splits large result sets into smaller pages to improve performance and user experience.

69. What is soft delete?
Soft delete marks data as deleted without actually removing it from the database.

70. What is database migration?
A migration is a versioned change to the database schema, such as adding or modifying tables and columns.

### APIs, Auth, Security
71. What is JWT?
JWT is a token format used to securely transmit information, often for authentication.

72. What is the difference between session-based auth and JWT auth?
Session auth stores server-side session state. JWT auth is usually stateless and stores token data on the client.

73. What is password hashing?
Hashing converts a password into a fixed string using a one-way algorithm so the original password cannot be recovered easily.

74. Why should passwords never be stored in plain text?
Because plain text passwords are dangerous if the database is leaked.

75. What is salting?
Salting adds random data to a password before hashing to make attacks harder.

76. What is CSRF?
Cross-Site Request Forgery is an attack where a user is tricked into sending an unwanted request to a trusted site.

77. What is XSS?
Cross-Site Scripting is an attack where malicious scripts are injected into web pages.

78. How do you prevent XSS?
By escaping output, validating input, avoiding unsafe HTML insertion, and using security headers.

79. How do you prevent SQL injection?
By using parameterized queries, prepared statements, and ORM safeguards instead of string concatenation.

80. What is HTTPS?
HTTPS encrypts communication between client and server using TLS, protecting data in transit.

### Testing
81. Why is testing important?
Testing helps catch bugs early, improves confidence, and makes code safer to change.

82. What is unit testing?
Unit testing checks a small piece of code, usually one function or module, in isolation.

83. What is integration testing?
Integration testing checks whether different parts of the system work correctly together.

84. What is end-to-end testing?
E2E testing checks user flows from start to finish, usually through the UI.

85. What is a mock?
A mock is a fake version of a dependency used to control behavior during testing.

86. What is test coverage?
Coverage measures how much of the code is exercised by tests, though high coverage does not automatically mean good tests.

87. Why use snapshot testing carefully?
Because snapshots can catch unexpected UI changes, but they can also become noisy and difficult to maintain.

88. What makes a good test?
A good test is clear, reliable, independent, and focused on behavior rather than implementation details.

89. How do you test API endpoints?
By sending requests to the endpoint and verifying status codes, response structure, data, and error cases.

90. What is TDD?
Test-Driven Development means writing the test first, then implementing code to make the test pass.

### System Design / DevOps / Collaboration
91. What is scalability?
Scalability is the ability of a system to handle more load without breaking performance.

92. What is load balancing?
Load balancing spreads traffic across multiple servers so no single server is overloaded.

93. What is caching?
Caching stores frequently used data in a faster location to reduce repeated work and improve speed.

94. What is a CDN?
A Content Delivery Network serves static content from locations closer to users to reduce latency.

95. What is CI/CD?
CI/CD automates testing, building, and deployment so changes can be delivered faster and more safely.

96. What is Docker?
Docker packages an application with its dependencies into a container so it runs consistently across environments.

97. Why is version control important?
Version control tracks changes, supports teamwork, allows rollback, and keeps development organized.

98. How do you handle production bugs?
By reproducing the issue, checking logs, isolating the cause, applying a safe fix, and verifying with tests or monitoring.

99. What makes a good full-stack developer?
A good full-stack developer understands frontend, backend, databases, APIs, debugging, and how all parts of a product connect.

100. How do you approach building a full-stack feature?
I start by understanding the requirement, define data flow and API contract, build the backend, connect the frontend, test the flow, and then refine for performance and usability.

