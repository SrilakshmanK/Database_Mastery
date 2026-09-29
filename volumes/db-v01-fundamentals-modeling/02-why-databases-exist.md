# CHAPTER 02 — WHY DATABASES EXIST

Before databases became common, applications could simply store information in files.

For example:

```text
users.txt
products.txt
orders.txt
payments.txt
```

This works for small systems.

But problems appear as the system grows.

---

# 2.1 Problem: Searching

Imagine:

```text
1 million users
```

stored in a plain text file.

Finding one specific user efficiently becomes difficult.

---

# 2.2 Problem: Updating

Suppose the same customer information appears in:

```text
orders.txt
payments.txt
customers.txt
support.txt
```

The customer's phone number changes.

Now multiple files may need updating.

What happens if one update is missed?

You get inconsistent data.

---

# 2.3 Problem: Relationships

Real applications have relationships.

For example:

```text
Customer
   ↓
Orders
   ↓
Products
   ↓
Payments
```

Representing and maintaining these relationships using plain files becomes increasingly difficult.

---

# 2.4 Problem: Concurrent Access

Imagine:

```text
User A → withdraw ₹500
User B → withdraw ₹500
```

Both access the same account at almost the same time.

The system must prevent incorrect balances.

This requires controlled concurrency.

---

# 2.5 Problem: Failure

What happens if the server crashes halfway through an operation?

For example:

```text
Account A: -₹1000
Account B: +₹1000
```

If the system crashes after the first operation but before the second:

```text
A = -₹1000
B = unchanged
```

The data becomes inconsistent.

Databases provide transaction and recovery mechanisms to handle such situations.

---

# 2.6 Problem: Security

A real application needs:

* authentication
* authorization
* roles
* permissions
* controlled access
* auditing

A database system provides mechanisms to enforce these at the data layer.

---

# 2.7 Why Databases Exist

The core reason is:

> **Reliable management of structured data at scale and under concurrent access.**

Databases solve multiple engineering problems simultaneously:

```text
Storage
Retrieval
Organization
Integrity
Relationships
Concurrency
Transactions
Security
Recovery
Performance
```

---

