# CHAPTER 12 — TRANSACTIONS & ACID

This is one of the most important foundations for backend engineering.

---

# 12.1 What Is a Transaction?

A transaction is a group of database operations treated as one logical unit of work.

Example:

Bank transfer:

```text
Account A - ₹1000
Account B + ₹1000
```

Both operations belong to one transaction.

---

# 12.2 Atomicity

Either:

```text
everything succeeds
```

or:

```text
nothing happens
```

---

# 12.3 Consistency

The transaction should move the database from one valid state to another valid state.

---

# 12.4 Isolation

Concurrent transactions should not incorrectly interfere with each other.

---

# 12.5 Durability

Once a committed transaction is accepted as durable, its changes should survive appropriate failures.

---

# 12.6 ACID

```text
A → Atomicity
C → Consistency
I → Isolation
D → Durability
```

Don't memorize the acronym only.

Understand the engineering problem each property addresses.

---

