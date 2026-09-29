# CHAPTER 06 — KEYS & CONSTRAINTS

This is one of the most important chapters.

---

# 6.1 What Is a Key?

A key helps identify or relate records.

---

# 6.2 Primary Key

A primary key uniquely identifies a row.

Example:

```text
users

id
---
1
2
3
```

We can say:

```text
id = 2
```

identifies one particular user.

Properties:

* unique
* identifies a row
* should not be NULL

---

# 6.3 Candidate Key

A candidate key is an attribute or combination of attributes that could uniquely identify a record.

For example:

```text
user_id
email
```

could potentially be unique.

One may be chosen as the primary key.

---

# 6.4 Natural vs Surrogate Keys

### Natural key

A real-world meaningful value.

Example:

```text
email
```

### Surrogate key

An artificial identifier.

Example:

```text
id = 1042
```

Both have uses.

We will learn how to choose appropriately.

---

# 6.5 Foreign Key

A foreign key creates a relationship between tables.

Example:

```text
customers

id
---
1
2
3
```

```text
orders

id    customer_id
---   -----------
101       1
102       1
103       3
```

`customer_id` refers to:

```text
customers.id
```

This creates a relationship.

---

# 6.6 Constraints

Constraints enforce rules.

Common constraints:

```text
PRIMARY KEY
FOREIGN KEY
UNIQUE
NOT NULL
CHECK
DEFAULT
```

Example:

```text
age >= 0
```

A `CHECK` constraint can enforce this rule.

---

# 6.7 Why Constraints Matter

Without constraints:

```text
user_id = 999999
```

could reference a user who doesn't exist.

With a foreign key:

```text
customer_id → customers.id
```

the database can reject invalid relationships.

---

