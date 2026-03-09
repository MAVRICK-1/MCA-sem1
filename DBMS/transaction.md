Here are **exam-friendly notes in easy words** for **Transaction & Concurrency Management and Database Recovery & Security**. I also included **simple mind maps** to help you revise quickly. 📚

---

# Transaction and Concurrency Management

## 1. Transaction

A **transaction** is a **sequence of database operations** performed as a single unit of work.

Example:

* Transfer money from Account A to Account B

1. Deduct money from A
2. Add money to B

Both steps must complete successfully.

### ACID Properties

* **Atomicity** – All operations happen or none happen
* **Consistency** – Database remains correct
* **Isolation** – Transactions do not affect each other
* **Durability** – Once completed, changes are permanent

---

## 2. Concurrent Transactions

When **multiple transactions run at the same time** in a database.

Example:

* Two users withdrawing money from the same bank account simultaneously.

### Advantages

* Better **performance**
* Faster **system response**

But it may cause **data inconsistency**.

---

## 3. Locking Protocol

A **locking protocol** controls access to data so that multiple users do not modify data at the same time.

Before accessing data, a transaction must **lock the data item**.

Purpose:

* Prevent conflicts
* Maintain data consistency

---

## 4. Locks

Locks are used to **control concurrent access**.

### Types of Locks

**Shared Lock (Read Lock)**

* Multiple transactions can read the data
* No one can modify it

**Exclusive Lock (Write Lock)**

* Only one transaction can read and write the data
* Others must wait

---

## 5. Serializable Schedules

A **schedule** is the order in which transactions are executed.

A **serializable schedule** means the result of concurrent transactions is **same as if they were executed one after another**.

This keeps the database **consistent**.


Serialization in DBMS ensures the execustion of concurrent transaction is concurrent and the result is same as if the operatrions are executed serially one after another.
it ensures data integrety and data consistency in multi user environment .

types 
- 1) conflict : occure when 2 transation try to read/write data at same time
  2) view : when 2 transcation try to read and write the data but it produces the same result as it executed serially
---

## 6. Two Phase Locking (2PL)

Two Phase Locking is a **protocol used to maintain serializability**.

It has **two phases**:

### 1. Growing Phase

* Transaction **acquires locks**
* Cannot release locks

### 2. Shrinking Phase

* Transaction **releases locks**
* Cannot acquire new locks

This ensures **safe concurrent execution**.

---

## 7. Deadlock

Deadlock occurs when **two or more transactions wait for each other’s resources** and none can continue.

Example:

* T1 locks A and waits for B
* T2 locks B and waits for A

Both transactions **wait forever**.

---

## 8. Deadlock Prevention

Ways to prevent deadlock:

* **Resource ordering**
* **Timeout method**
* **Wait–Die scheme**
* **Wound–Wait scheme**

The system ensures transactions **do not wait indefinitely**.

---

## 9. Optimistic Concurrency Control

This method **assumes conflicts are rare**.

Steps:

1. Transaction executes without locks
2. At commit time, system checks conflicts
3. If conflict exists → transaction restarts

Advantages:

* Better performance
* No locking overhead

---

## 10. Pessimistic Concurrency Control

This method **assumes conflicts may happen**.

Transactions **lock data before accessing it**.

Example:

* Two Phase Locking (2PL)

Advantages:

* Prevents conflicts before they occur

---

# Database Recovery and Security

---

## 11. Database Recovery (Meaning)

Database recovery means **restoring the database to a correct state after a failure**.

Example:

* System crash
* Power failure

Recovery ensures **no data is lost**.

---

## 12. Kinds of Failures

### Transaction Failure

Occurs when a transaction cannot complete.

Example:

* Invalid input
* System error

### System Failure

System crashes due to:

* Power failure
* Operating system crash

### Media Failure

Failure of storage devices like:

* Hard disk damage
* Disk crash

---

## 13. Failure Controlling Methods

Methods used to manage failures:

* **Transaction logs**
* **Checkpointing**
* **Backup systems**
* **Recovery algorithms**

These help restore database quickly.

---

## 14. Database Errors

Errors that may occur in databases:

* Logical errors
* System errors
* Hardware errors
* User errors

These errors may cause **data loss or inconsistency**.

---

## 15. Backup and Recovery Techniques

### Backup

Copy of database stored in another location.

Types:

* Full backup
* Incremental backup
* Differential backup

### Recovery

Process of **restoring data using backups and logs** after failure.

---

## 16. Security and Integrity

### Security

Protecting the database from **unauthorized access**.

Methods:

* Authentication
* Encryption
* Access control

### Integrity

Ensures **data remains accurate and consistent**.

Example:

* No duplicate primary keys
* Correct data values

---

## 17. Database Security Authorization

Authorization means **giving permission to users to access database resources**.

Examples of privileges:

* SELECT (read data)
* INSERT (add data)
* UPDATE (modify data)
* DELETE (remove data)

Only authorized users can perform these actions.

---

# Mind Map – Transaction & Concurrency

```
Transaction & Concurrency
        |
        |-- Transaction
        |      |-- ACID Properties
        |
        |-- Concurrent Transactions
        |
        |-- Locking Protocol
        |      |-- Shared Lock
        |      |-- Exclusive Lock
        |
        |-- Serializable Schedule
        |
        |-- Two Phase Locking
        |      |-- Growing Phase
        |      |-- Shrinking Phase
        |
        |-- Deadlock
        |      |-- Prevention
        |
        |-- Concurrency Control
               |-- Optimistic
               |-- Pessimistic
```

---

# Mind Map – Recovery & Security

```
Database Recovery & Security
        |
        |-- Database Recovery
        |
        |-- Failures
        |      |-- Transaction Failure
        |      |-- System Failure
        |      |-- Media Failure
        |
        |-- Failure Control Methods
        |
        |-- Database Errors
        |
        |-- Backup
        |      |-- Full
        |      |-- Incremental
        |
        |-- Recovery
        |
        |-- Security
        |      |-- Authentication
        |      |-- Encryption
        |
        |-- Authorization
               |-- SELECT
               |-- INSERT
               |-- UPDATE
               |-- DELETE
```

---

✅ **Exam Tip:**
Write **definition (2 lines) + small example + bullet points**. This gives **full marks in theory papers**.

---

If you want, I can also give a **super short 1-page DBMS revision sheet (covers 80% exam questions)** so you can revise everything in **10 minutes before the exam**.
