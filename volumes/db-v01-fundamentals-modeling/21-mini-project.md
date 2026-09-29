# CHAPTER 21 — MINI-PROJECT

# Project: Real-World Database Design Lab

This is deliberately **not** a huge application.

The purpose is to practice database thinking.

We will design a realistic system from requirements without worrying about frontend/backend implementation yet.

---

## Project Domain

### Online Course Platform

This domain is intentionally different from your old LMS project.

We are **not building an LMS application**.

We are using a small domain only to practice database modeling.

---

# Requirements

The platform needs to store:

### Users

* id
* name
* email
* phone
* created date

### Courses

* id
* title
* description
* price
* created date

### Instructors

* id
* name
* email

### Course Categories

* id
* name

### Enrollments

* student
* course
* enrollment date
* status

### Lessons

* course
* title
* sequence/order

### Payments

* enrollment
* amount
* status
* payment date

---

# Project Tasks

## Phase 1 — Requirement Analysis

Write:

```text
Entities:
?

Attributes:
?

Relationships:
?

Business rules:
?
```

---

## Phase 2 — ER Model

Create an ER diagram showing:

```text
User
Course
Instructor
Category
Enrollment
Lesson
Payment
```

and their relationships.

---

## Phase 3 — Cardinality

Determine:

```text
User → Enrollment
Course → Enrollment
Course → Lesson
Course → Instructor
Course → Category
Enrollment → Payment
```

For each relationship, determine whether it is:

```text
1:1
1:N
N:N
```

---

## Phase 4 — Normalize

Take an intentionally bad design:

```text
enrollment_id
student_name
student_email
course_name
course_price
instructor_name
category_name
lesson1
lesson2
lesson3
payment_status
```

Identify:

* duplicate data
* repeating groups
* update anomalies
* insertion anomalies
* deletion anomalies

Then redesign it.

---

## Phase 5 — Define Constraints

For each table determine:

* Primary key
* Foreign keys
* Unique constraints
* NOT NULL fields
* CHECK constraints
* Default values

---

## Phase 6 — Design the Final Schema

Produce a schema document such as:

```text
users
courses
instructors
categories
enrollments
lessons
payments
```

For each table document:

```text
Column
Type
Nullable?
Default?
Constraint?
Purpose?
```

---

## Phase 7 — Design Important Queries

Without implementing SQL yet, write the requirements for queries such as:

```text
Find a user by email.

Find all courses for a category.

Find all courses taken by a student.

Find all students enrolled in a course.

Find lessons for a course in order.

Find unpaid enrollments.

Find total revenue by course.

Find courses taught by an instructor.
```

This teaches an important principle:

> **Schema design and query design influence each other.**

---

## Phase 8 — Failure Injection

Intentionally propose invalid situations:

```text
Enrollment references nonexistent user.

Payment references nonexistent enrollment.

Duplicate user email.

Negative course price.

Lesson with invalid course.

Enrollment without a required student.
```

For every case answer:

> Which database rule should prevent this?

---

