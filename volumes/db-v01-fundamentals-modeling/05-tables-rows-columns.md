# CHAPTER 05 — TABLES, ROWS, COLUMNS & DATA TYPES

Before designing relationships, understand what a table actually represents.

---

# 5.1 Choosing Columns

Suppose we have:

```text
users
```

Possible columns:

```text
id
name
email
phone
created_at
```

Each column should represent a meaningful attribute.

Avoid random dumping:

```text
extra1
extra2
misc
data
something
```

---

# 5.2 Data Types

Different values require different types.

Examples:

```text
INTEGER
BIGINT
DECIMAL
BOOLEAN
TEXT
VARCHAR
DATE
TIMESTAMP
UUID
```

The exact types vary between database systems.

We will learn PostgreSQL-specific details in DB V02.

---

# 5.3 Why Data Types Matter

Consider:

```text
age = "22"
```

versus:

```text
age = 22
```

A number should generally be represented as a numeric type.

Correct data types allow the database to:

* validate values
* compare correctly
* sort correctly
* perform calculations
* store efficiently

---

# 5.4 NULL

`NULL` means:

> The value is absent/unknown/not provided.

It does **not** mean:

```text
0
```

and it does not necessarily mean:

```text
""
```

Example:

```text
phone = NULL
```

means there is no phone value currently stored.

NULL becomes extremely important when we study:

* constraints
* queries
* joins
* logic
* application behavior

---

