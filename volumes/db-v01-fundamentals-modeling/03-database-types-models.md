# CHAPTER 03 — DATABASE TYPES & DATA MODELS

Not every problem requires the same type of database.

---

# 3.1 Relational Databases

Data is organized primarily into related tables.

Examples:

* PostgreSQL
* MySQL
* SQL Server
* Oracle

Typical structure:

```text
customers
orders
products
payments
```

Relationships connect them.

---

# 3.2 Document Databases

Data is represented as documents.

Example:

```json
{
  "name": "Sri",
  "age": 22,
  "skills": [
    "JavaScript",
    "Python",
    "React"
  ]
}
```

MongoDB is an example.

---

# 3.3 Key-Value Databases

Data is primarily represented as:

```text
key → value
```

Example:

```text
user:123 → session-data
```

Redis is commonly used this way, although Redis supports additional data structures.

---

# 3.4 Column-Oriented Databases

Designed around analytical workloads where large numbers of rows may be processed.

Examples include systems such as:

* ClickHouse
* BigQuery
* Snowflake

We don't need deep specialization here yet.

---

# 3.5 Graph Databases

Designed around relationships between entities.

Example:

```text
Person
 ↓
FRIEND_OF
 ↓
Person
```

Useful in certain relationship-heavy domains.

Again, this volume only needs conceptual understanding.

---

# 3.6 Vector Databases / Vector Stores

Important for our later AI roadmap.

They store vector representations such as embeddings.

Example:

```text
Document
    ↓
Embedding
    ↓
[0.13, -0.82, 0.44, ...]
```

These allow semantic similarity searches.

This becomes important in:

**AI V10 — Embeddings, Vector Search & RAG**

and later:

**DB V06 — AI-Native Databases & Database DevOps**

---

# 3.7 Data Model

A data model describes how data is represented and related.

Examples:

```text
Relational
Document
Key-Value
Graph
```

Important distinction:

> **Database type** and **data model** are related concepts but shouldn't be treated as identical terminology.

---

