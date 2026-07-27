# 35 common interview questions and answers focused on **SQL + Drizzle ORM**,

---

## 1. What is Drizzle ORM?

**Answer:**

> Drizzle is a lightweight TypeScript ORM that lets me define my database schema in TypeScript. It provides end-to-end type safety while generating SQL behind the scenes. I like it because it's close to SQL and has very little abstraction.

---

## 2. Why did you choose Drizzle instead of Prisma?

**Answer:**

> Drizzle gives me more control over SQL and has less runtime overhead. It feels like writing SQL with TypeScript support. It's also faster to start and makes complex queries easier to understand.

---

## 3. What database have you used with Drizzle?

**Answer:**

> I've mainly used PostgreSQL with Drizzle.

---

## 4. How do you define a table in Drizzle?

**Answer:**

> I define it using `pgTable()`, then specify the columns, data types, constraints, indexes, and relationships in TypeScript.

---

## 5. How do you insert data?

**Answer:**

> I use `db.insert(table).values({...})`. It automatically validates the types at compile time.

---

## 6. How do you update data?

**Answer:**

> I use `db.update(table).set({...}).where(...)` to update only the required rows.

---

## 7. How do you delete data?

**Answer:**

> I use `db.delete(table).where(...)`. In production, I usually prefer soft deletes by keeping an `isDeleted` flag instead of removing records permanently.

---

## 8. How do you fetch data?

**Answer:**

> I use `db.select().from(table)` and add `where`, `orderBy`, `limit`, or `join` depending on the requirement.

---

## 9. What are migrations?

**Answer:**

> Migrations are version-controlled SQL changes that keep the database schema consistent across all environments.

---

## 10. How do you create migrations in Drizzle?

**Answer:**

> After updating the schema, I run `drizzle-kit generate`, which creates SQL migration files. Then I apply them using `drizzle-kit migrate`.

---

## 11. Why not edit the database manually?

**Answer:**

> Manual changes aren't tracked. Migrations make schema changes reproducible and ensure every environment stays in sync.

---

## 12. What is SQL?

**Answer:**

> SQL is the language used to create, read, update, and delete data in relational databases.

---

## 13. Difference between SQL and Drizzle?

**Answer:**

> SQL is the actual query language. Drizzle is an ORM that generates SQL while providing TypeScript type safety.

---

## 14. What is a Primary Key?

**Answer:**

> A primary key uniquely identifies each row in a table. It cannot be duplicated or null.

---

## 15. What is a Foreign Key?

**Answer:**

> A foreign key creates a relationship between two tables and maintains referential integrity.

---

## 16. What is an Index?

**Answer:**

> An index speeds up queries by allowing the database to find rows faster, but it increases storage usage and slightly slows writes.

---

## 17. When do you create indexes?

**Answer:**

> I create indexes on columns that are frequently used for filtering, sorting, joining, or pagination.

---

## 18. What is a JOIN?

**Answer:**

> A JOIN combines data from multiple tables based on a related column.

---

## 19. Types of JOIN?

**Answer:**

> The most common are INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN. I mostly use INNER and LEFT JOIN.

---

## 20. Difference between INNER JOIN and LEFT JOIN?

**Answer:**

> INNER JOIN returns only matching rows from both tables. LEFT JOIN returns all rows from the left table and matching rows from the right table.

---

## 21. What is normalization?

**Answer:**

> Normalization organizes data into separate tables to reduce duplication and improve consistency.

---

## 22. Why use transactions?

**Answer:**

> Transactions ensure that multiple database operations either all succeed or all fail, keeping data consistent.

---

## 23. How do you use transactions in Drizzle?

**Answer:**

> I use `db.transaction()` and perform all related queries inside it. If one query fails, everything is rolled back.

---

## 24. What is pagination?

**Answer:**

> Pagination limits the amount of data returned in one request, improving performance and user experience.

---

## 25. Offset vs Cursor Pagination?

**Answer:**

> Offset pagination is simple but becomes slower on large datasets. Cursor pagination is faster and more consistent because it starts after the last fetched record instead of skipping rows.

---

## 26. Why use UUID instead of auto-increment IDs?

**Answer:**

> UUIDs are globally unique, harder to guess, and useful in distributed systems, though they're larger than integers.

---

## 27. What is a UNIQUE constraint?

**Answer:**

> It ensures that no two rows can have the same value in a column, like an email address.

---

## 28. What is NOT NULL?

**Answer:**

> It prevents a column from storing null values, ensuring required data is always present.

---

## 29. Have you written raw SQL with Drizzle?

**Answer:**

> Yes. For complex queries that are easier in SQL, Drizzle allows executing raw SQL while still integrating with the ORM.

---

## 30. Why use an ORM if SQL already exists?

**Answer:**

> An ORM improves developer productivity by providing type safety, reducing boilerplate, and preventing many common mistakes, while still allowing raw SQL when needed.

---

## 31. What is N+1 problem?
It occurs when we first fetch a list and then run additional queries for each item, leading to performance issues.
```
// Bad code🟥 👉 1 query + N queries = 💀 slow
const users = await db.select().from(users);
for (const user of users) {
  const posts = await db.select().from(posts).where(eq(posts.userId, user.id));
}
```
```
// 🟩 Good code. 👉 1 query only ✅
await db.select()
  .from(users)
  .leftJoin(posts, eq(users.id, posts.userId));
````
---

## 32. Explain One-to-One vs One-to-Many vs Many-to-Many

Answer:

One-to-One: One user has one profile. 

One-to-Many: One department has many employees. 

Many-to-Many: One student can enroll in many courses, and one course has many students.

---

33. What is an Aggregate Function?

Answer:

Aggregate functions calculate values from multiple rows.

Examples:
```
COUNT()
SUM()
AVG()
MIN()
MAX()
```

---
34. What is ACID?

Answer:

Transactions follow the ACID properties:

Atomicity: All operations succeed or none do.
Consistency: Data remains valid.
Isolation: Concurrent transactions don't interfere.
Durability: Committed changes are permanent.

---

35. What is SQL ?
SQL (Structured Query Language) is the standard language used to define database schemas and to create, read, update, delete, and query data in relational databases.


  
