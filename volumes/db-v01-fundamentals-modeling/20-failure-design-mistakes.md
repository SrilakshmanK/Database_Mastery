# CHAPTER 20 — DATABASE FAILURE & DESIGN MISTAKES

This chapter is about learning from bad designs.

---

# Mistake 1 — One Giant Table

```text
customer_name
customer_phone
product1
product2
product3
payment_method
delivery_person
delivery_phone
...
```

This becomes difficult to maintain.

---

# Mistake 2 — Everything as TEXT

```text
age TEXT
price TEXT
created_at TEXT
```

This destroys useful type guarantees.

---

# Mistake 3 — No Primary Key

Without a reliable identifier, rows become difficult to reference safely.

---

# Mistake 4 — No Foreign Keys

Relationships become unreliable.

---

# Mistake 5 — Too Many Indexes

Writes and maintenance become more expensive.

---

# Mistake 6 — No Constraints

The database accepts invalid states.

---

# Mistake 7 — Trusting Only Application Validation

A second application or script could bypass those checks.

---

# Mistake 8 — Storing Repeated Data Everywhere

Creates update anomalies and inconsistencies.

---

# Mistake 9 — Over-Normalizing

A theoretically elegant design can become inconvenient or inefficient if it ignores real access patterns.

---

# Mistake 10 — Designing Without Queries

A schema should support how the application actually uses the data.

---

# Mistake 11 — No Backup Strategy

Production data should never depend on:

> "The server is working, so we're safe."

---

# Mistake 12 — No Recovery Testing

A backup isn't enough.

You need:

```text
Backup
 ↓
Restore
 ↓
Verify
```

---

