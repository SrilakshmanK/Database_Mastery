# CHAPTER 15 — DATA INTEGRITY & VALIDATION

Data integrity means keeping data correct and consistent.

---

# 15.1 Entity Integrity

Each entity should be uniquely identifiable.

Example:

```text
PRIMARY KEY
```

---

# 15.2 Referential Integrity

Relationships should reference valid entities.

Example:

```text
orders.customer_id
        ↓
customers.id
```

---

# 15.3 Domain Integrity

Values should satisfy valid rules.

Examples:

```text
price >= 0
age >= 0
status IN (...)
```

---

# 15.4 Application Validation vs Database Validation

Application:

```text
if price < 0:
    reject
```

Database:

```text
CHECK (price >= 0)
```

We generally want important invariants protected at the database layer as well.

Why?

Because applications can contain bugs.

The database should be a final line of defense.

---

