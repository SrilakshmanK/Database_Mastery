# CHAPTER 18 — APPLICATION ↔ DATABASE ARCHITECTURE

Now connect databases to your existing backend knowledge.

Typical architecture:

```text
Client
  ↓
Frontend
  ↓
API
  ↓
Backend Service
  ↓
Database Driver / ORM
  ↓
Database
```

Example:

```text
React
  ↓
FastAPI
  ↓
SQLAlchemy / driver
  ↓
PostgreSQL
```

or:

```text
React
  ↓
Node.js / Express
  ↓
MongoDB driver / Mongoose
  ↓
MongoDB
```

---

# 18.1 Why Not Let Frontend Access Database Directly?

Because the backend provides:

* authentication
* authorization
* validation
* business logic
* transaction boundaries
* security
* rate limiting
* controlled access

The normal architecture is:

```text
Frontend
    ↓
Backend
    ↓
Database
```

---

# 18.2 Connection

The application communicates with the database through a driver/client.

Examples:

```text
Python → PostgreSQL
Node.js → PostgreSQL
Node.js → MongoDB
Python → Redis
```

We will implement these in later volumes.

---

# 18.3 Connection Pooling

Opening a completely new database connection for every request can be expensive.

A connection pool maintains reusable connections.

Conceptually:

```text
Application
     ↓
Connection Pool
 ┌───┼───┐
 ↓   ↓   ↓
DB connections
     ↓
Database
```

This becomes important when we study backend performance and production systems.

---

