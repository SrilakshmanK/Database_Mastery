# CHAPTER 10 — NORMALIZATION

Normalization is one of the most commonly misunderstood database concepts.

Don't memorize normal forms first.

Understand the problem.

---

# 10.1 The Problem

Imagine:

```text
student_id
student_name
course1
course2
course3
```

This creates structural problems.

What happens when a student takes:

```text
course4
```

Do we add another column?

That doesn't scale.

---

# 10.2 Repeating Data

Bad design:

```text
order_id
customer_name
customer_phone
product1
product2
product3
```

The table mixes multiple concepts.

Better:

```text
customers
orders
products
order_items
```

---

# 10.3 First Normal Form

The simplified practical idea:

> Store atomic values and avoid repeating groups.

Instead of:

```text
skills = "Python, Java, JavaScript"
```

inside a relational column for a multi-valued relationship, model the relationship appropriately.

---

# 10.4 Second Normal Form

The practical idea:

> Non-key attributes should depend on the whole key.

This becomes especially important with composite keys.

---

# 10.5 Third Normal Form

The practical idea:

> Non-key attributes should depend on the key, not on another non-key attribute.

Example:

```text
employee_id
employee_name
department_id
department_name
```

`department_name` depends on `department_id`, not directly on `employee_id`.

So department information may belong in:

```text
departments
```

---

# 10.6 Why Normalize?

Normalization reduces:

* duplicate data
* update anomalies
* insertion anomalies
* deletion anomalies
* inconsistency

---

