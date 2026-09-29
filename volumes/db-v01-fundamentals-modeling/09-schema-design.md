# CHAPTER 09 — DATABASE SCHEMA DESIGN

Schema design means turning a real-world domain into a structured data model.

---

# 9.1 Start With the Domain

Ask:

> What are we storing?

Example:

Online store.

Entities:

```text
Customer
Product
Order
Payment
Address
```

---

# 9.2 Identify Attributes

Customer:

```text
id
name
email
phone
```

Product:

```text
id
name
price
stock
```

---

# 9.3 Identify Relationships

```text
Customer → Orders
Order → Order Items
Order Item → Product
Order → Payment
```

---

# 9.4 Identify Rules

Examples:

```text
email must be unique
price cannot be negative
order must belong to a customer
order item must reference a product
```

These rules become constraints.

---

# 9.5 Design Before Implementation

The workflow should generally be:

```text
Problem
 ↓
Requirements
 ↓
Entities
 ↓
Attributes
 ↓
Relationships
 ↓
Constraints
 ↓
ER Model
 ↓
Schema
 ↓
Implementation
```

This workflow will become extremely important when we later design the database for the flagship project.

---

