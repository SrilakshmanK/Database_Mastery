# CHAPTER 04 — RELATIONAL DATABASE FUNDAMENTALS

The relational model is the foundation of our PostgreSQL journey.

---

# 4.1 Relation

In practical SQL terminology, we usually work with a table.

Example:

```text
students
```

| id | name  | age |
| -: | ----- | --: |
|  1 | Arun  |  21 |
|  2 | Priya |  22 |
|  3 | Kumar |  20 |

Conceptually, the relational model provides a mathematical foundation underneath tables.

We don't need to become mathematicians.

We need to understand the engineering consequences.

---

# 4.2 Row

A row represents one record/tuple.

```text
1 | Arun | 21
```

---

# 4.3 Column

A column represents an attribute.

```text
id
name
age
```

---

# 4.4 Schema

A schema describes the structure of the data.

For example:

```text
students

id      INTEGER
name    VARCHAR
age     INTEGER
```

A schema answers:

> What data exists and how is it structured?

---

# 4.5 Why Structure Matters

Without structure:

```text
Sri,22,Coimbatore
Arun,twenty,Chennai
Priya,23
```

The system cannot reliably enforce meaning.

With a schema:

```text
age INTEGER NOT NULL
```

the database can reject invalid values.

This is one of the most important database principles:

> **The database should protect data quality, not blindly trust the application.**

---

