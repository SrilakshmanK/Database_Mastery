# CHAPTER 19 — DATABASE DESIGN WORKFLOW

This chapter turns everything into a repeatable engineering process.

---

# Step 1 — Understand the Problem

Don't start with:

```sql
CREATE TABLE
```

Start with:

> What problem are we solving?

---

# Step 2 — Identify Entities

Example:

Food delivery system:

```text
Customer
Restaurant
Food
Order
Payment
Delivery
```

---

# Step 3 — Identify Attributes

Customer:

```text
id
name
phone
email
```

---

# Step 4 — Identify Relationships

```text
Customer → Order
Restaurant → Food
Order → Order Items
Order → Payment
Order → Delivery
```

---

# Step 5 — Define Constraints

Examples:

```text
email UNIQUE
price >= 0
order.customer_id must exist
```

---

# Step 6 — Normalize

Remove unnecessary duplication and anomalies.

---

# Step 7 — Consider Access Patterns

Ask:

> How will the application query this data?

Examples:

```text
Find customer by email
Find orders by customer
Find pending orders
Find products by category
```

---

# Step 8 — Consider Performance

Only now think about indexes and other optimization mechanisms.

---

# Step 9 — Consider Security

Who can:

```text
read?
insert?
update?
delete?
```

---

# Step 10 — Consider Recovery

What happens if:

```text
server crashes?
data is deleted?
deployment fails?
```

---

# Step 11 — Implement

Only after the model is understood.

---

# Step 12 — Test

Test:

* valid data
* invalid data
* relationships
* constraints
* transactions
* failure scenarios

---

