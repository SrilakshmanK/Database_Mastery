# CHAPTER 13 — CONCURRENCY FUNDAMENTALS

Modern databases are rarely used by one person.

Imagine:

```text
1000 users
     ↓
Application
     ↓
Database
```

Many requests may access the same records simultaneously.

---

# 13.1 Race Condition

Suppose:

```text
Stock = 1
```

Two users buy the last item simultaneously.

Without proper concurrency handling:

```text
User A sees 1
User B sees 1

A buys
B buys

Stock becomes -1
```

The database/application must prevent invalid states.

---

# 13.2 Concurrency Problems

We will understand concepts such as:

* lost updates
* dirty reads
* non-repeatable reads
* phantom reads
* locking
* isolation levels

We will not yet dive deeply into PostgreSQL's internal implementation.

That belongs in DB V04.

---

# 13.3 Why This Matters for Backend Engineering

Every backend developer eventually encounters:

```text
Request A
Request B
Request C
   ↓
same database
```

Database concurrency is therefore an application engineering problem, not merely a DBA topic.

---

