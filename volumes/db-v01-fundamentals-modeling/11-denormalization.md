# CHAPTER 11 — DENORMALIZATION

Normalization is not an absolute law.

Sometimes we intentionally duplicate data for performance or convenience.

This is denormalization.

---

# 11.1 Example

Instead of joining:

```text
orders
customers
```

every time, a system might intentionally store:

```text
order_customer_name
```

inside an order snapshot.

Why?

Because the order may need to preserve the customer's name **as it was when the order happened**.

---

# 11.2 Another Example

Analytics systems may duplicate or precompute data to reduce expensive joins.

---

# 11.3 Important Rule

Do not think:

> Normalization = good
> Denormalization = bad

Think:

> **Normalization protects consistency.**

> **Denormalization can improve access patterns/performance when deliberately designed.**

This distinction becomes important in production systems.

---

