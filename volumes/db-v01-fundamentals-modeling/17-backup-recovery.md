# CHAPTER 17 — BACKUP, RECOVERY & DURABILITY FUNDAMENTALS

A database is not safe merely because it is running.

---

# 17.1 Backup

A backup is a recoverable copy of data.

---

# 17.2 Recovery

Recovery means restoring the system/data after a failure.

---

# 17.3 Common Failure Scenarios

```text
Accidental DELETE
Database corruption
Disk failure
Server failure
Human error
Deployment mistake
Security incident
```

---

# 17.4 Backup ≠ Recovery

Having a backup file doesn't prove you can recover.

You need to test restoration.

Therefore:

> **A backup that has never been restored is an assumption, not a verified recovery mechanism.**

---

# 17.5 RPO & RTO

Later production engineering will use:

### RPO

Recovery Point Objective.

How much data loss can be tolerated?

### RTO

Recovery Time Objective.

How long can recovery take?

We only need the concepts here.

They become important later with:

* AWS
* production databases
* SRE
* disaster recovery

---

