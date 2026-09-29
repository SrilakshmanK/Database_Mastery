# CHAPTER 16 — DATABASE SECURITY FUNDAMENTALS

Security starts at the database layer.

---

# 16.1 Authentication

Who are you?

---

# 16.2 Authorization

What are you allowed to do?

---

# 16.3 Least Privilege

A service should receive only the permissions it actually needs.

For example:

```text
Read-only service
```

should not automatically have:

```text
DROP DATABASE
```

permissions.

---

# 16.4 Secrets

Never hardcode:

```text
DB_PASSWORD=123456
```

inside source code.

Use appropriate secret/configuration mechanisms.

---

# 16.5 SQL Injection

Never construct queries unsafely using user input.

Conceptually dangerous:

```text
"SELECT * FROM users WHERE name = '" + userInput + "'"
```

Use parameterized queries/prepared statements.

We'll practice this later.

---

# 16.6 Database Security Layers

Think:

```text
Network
 ↓
Database authentication
 ↓
Authorization
 ↓
Application permissions
 ↓
Query safety
 ↓
Data protection
 ↓
Auditing/monitoring
```

Security will become much deeper in:

**DB V04 and DB V06**

and in:

**DevOps V17 — DevSecOps & Production Security**

---

