# CHAPTER 08 — ENTITY-RELATIONSHIP MODELING

Before creating tables, model the real-world problem.

---

# 8.1 Entity

An entity is something about which we store information.

Example:

```text
Customer
Product
Order
Payment
```

---

# 8.2 Attribute

An attribute describes an entity.

Customer:

```text
id
name
email
phone
```

---

# 8.3 Relationship

A relationship describes how entities interact.

```text
Customer
   |
places
   |
Order
```

---

# 8.4 Example

E-commerce system:

```text
Customer
   |
   | places
   ↓
Order
   |
   | contains
   ↓
Product
```

But an order can contain multiple products.

Therefore we may need:

```text
orders
order_items
products
```

---

# 8.5 Why ER Modeling Matters

Without modeling first, developers often jump directly into:

```sql
CREATE TABLE ...
```

and discover later that the structure is wrong.

Database engineering begins before SQL.

---

