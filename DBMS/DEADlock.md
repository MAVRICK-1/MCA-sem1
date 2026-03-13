Here is the **simple explanation in easy exam words**.

---

# 7. Deadlock

**Deadlock** happens when **two or more transactions are waiting for each other’s resources**, so none of them can continue.

In this situation, the transactions are **stuck forever**.

### Example

Transaction **T1**

* Locks data **A**
* Wants to access **B**

Transaction **T2**

* Locks data **B**
* Wants to access **A**

Now:

* T1 is waiting for **B**
* T2 is waiting for **A**

Both keep waiting → **Deadlock occurs**.

### One line for exam

**Deadlock is a situation where transactions wait for each other’s resources and cannot proceed.**

---

# 8. Deadlock Prevention

Deadlock prevention means **methods used to stop deadlocks from happening in a database system**.

### 1. Resource Ordering

All resources are **accessed in a fixed order**.

Example:
If the rule is **A → B**, transactions must lock **A first then B**.
This avoids circular waiting.

---

### 2. Timeout Method

If a transaction **waits too long for a resource**, the system cancels it.

Example:
If T1 waits for 10 seconds, the system **aborts the transaction**.

---

### 3. Wait–Die Scheme

This method uses **timestamps (age of transactions)**.

* **Older transaction waits**
* **Younger transaction is aborted (dies)**

This prevents circular waiting.

---

### 4. Wound–Wait Scheme

Also uses **transaction timestamps**.

* **Older transaction stops (wounds) younger transaction**
* Younger transaction is **rolled back**

---

### One line for exam

**Deadlock prevention methods stop transactions from waiting for each other indefinitely.**
