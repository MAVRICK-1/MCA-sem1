Here is the **simple explanation in easy exam language**:

---

## 13. Failure Controlling Methods

Failure controlling methods are **techniques used to handle database failures and recover data** so the system can work normally again.

### 1. Transaction Logs

A **transaction log** is a file that records all changes made in the database.

Example:
If the system crashes, the database can check the log and **redo or undo transactions** to recover data.

---

### 2. Checkpointing

Checkpointing means **saving the current state of the database at regular intervals**.

Example:
If the system fails, the database can start recovery from the **last checkpoint instead of the beginning**, which saves time.

---

### 3. Backup Systems

Backup means **making a copy of the database and storing it in another location**.

Example:
If the database is damaged, the backup copy can be used to **restore the data**.

---

### 4. Recovery Algorithms

Recovery algorithms are **special methods used by DBMS to restore the database after a failure**.

They use **logs and backups** to bring the database back to a **correct and consistent state**.

---

## 14. Database Errors

Database errors are **problems that occur in a database system and may affect data correctness**.

### 1. Logical Errors

Errors caused by **wrong program logic or incorrect operations**.

Example:
A program subtracts money instead of adding it.

---

### 2. System Errors

Errors caused by **software or operating system failure**.

Example:
Database server crash.

---

### 3. Hardware Errors

Errors caused by **hardware problems**.

Example:
Hard disk crash or power failure.

---

### 4. User Errors

Errors caused by **mistakes made by users**.

Example:
User deletes important data by mistake.

---

✅ **One line for exam:**
Failure controlling methods help **recover the database after failures**, while database errors are **problems that cause data loss or incorrect data**.
