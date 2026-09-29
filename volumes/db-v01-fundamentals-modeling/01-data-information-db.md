# CHAPTER 01 — DATA, INFORMATION & DATABASES

## 1.1 What Is Data?

Data is a representation of some fact, observation, measurement, event, or value.

Examples:

```text
22
Sri
14000
2026-09-27
true
Coimbatore
```

Individually, these values may not tell us much.

For example:

```text
22
```

is just a value.

When we add context:

```text
Age = 22
```

it becomes meaningful information.

---

## 1.2 Data vs Information

### Data

Raw values.

### Information

Data placed into a meaningful context.

Example:

```text
Data:

22
7.1
2026
```

Information:

```text
Age: 22
CGPA: 7.1
Graduation Year: 2026
```

The database usually stores the **data**, while the application gives that data meaning through structure and context.

---

# 1.3 What Is a Database?

A database is an organized collection of data designed so that the data can be stored, accessed, modified, and managed efficiently.

A database is **not simply an SSD or hard disk**.

The physical storage device is hardware.

The database is a logical organization of data implemented using software.

Think:

```text
Hardware
    ↓
Storage
    ↓
Database software
    ↓
Database
    ↓
Tables / documents / indexes / metadata
    ↓
Application
```

---

# 1.4 What Is a DBMS?

DBMS = **Database Management System**

It is the software responsible for managing databases.

Examples:

* PostgreSQL
* MySQL
* MariaDB
* MongoDB
* Microsoft SQL Server
* Oracle Database
* Redis

A DBMS provides mechanisms for:

* storing data
* retrieving data
* modifying data
* enforcing constraints
* handling concurrent users
* managing transactions
* recovering from failures
* controlling access
* optimizing queries

---

# 1.5 Database vs DBMS

Think about a library.

### Database

The actual collection of books and their organized information.

### DBMS

The system that manages:

* where books are stored
* who can access them
* how they are found
* how new books are added
* how books are removed
* how multiple people use the library simultaneously

---

# 1.6 First-Principles Question

Ask:

> Why not just store everything in files?

This question leads directly to the next chapter.

---

