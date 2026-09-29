# CHAPTER 07 — RELATIONSHIPS & CARDINALITY

Applications are built from related entities.

---

# 7.1 One-to-One

Example:

```text
User
  ↓
Profile
```

One user has one profile.

---

# 7.2 One-to-Many

Very common.

```text
Customer
   ↓
Orders
```

One customer can have many orders.

But:

```text
Order → one Customer
```

---

# 7.3 Many-to-Many

Example:

```text
Students ↔ Courses
```

A student can enroll in many courses.

A course can have many students.

We usually introduce an intermediate table:

```text
students
courses
enrollments
```

---

# 7.4 Cardinality

Cardinality describes how many records can participate in a relationship.

Examples:

```text
1 : 1
1 : N
N : N
```

This becomes critical when designing schemas.

---

