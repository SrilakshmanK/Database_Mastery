# CHAPTER 14 — INDEX FUNDAMENTALS

An index helps the database find data more efficiently.

---

# 14.1 Without an Index

Suppose:

```text
1,000,000 users
```

and we search:

```text
email = "user@example.com"
```

Without a suitable index, the database may need to inspect many rows.

---

# 14.2 With an Index

The database maintains additional structures that help locate matching rows faster.

Conceptually:

```text
Query
 ↓
Index
 ↓
Relevant rows
```

---

# 14.3 Indexes Are Not Free

An index consumes:

* storage
* memory/cache resources
* write/update overhead
* maintenance work

Therefore:

> **More indexes does not automatically mean better performance.**

---

# 14.4 Core Principle

Indexes should be designed around:

> **Actual query patterns.**

Not:

> "Put an index on every column."

We'll study actual PostgreSQL index types and query planning in later volumes.

---

