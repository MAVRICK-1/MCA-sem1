# 1. Distributed Database

1. A **Distributed Database (DDB)** is a database where **data is stored at multiple locations** but appears as **one single database to users**.
2. These locations are connected through a **network**.
3. Each location may store **different parts of the database**.

### Example

A bank storing customer data in **different branches** but all connected together.

---

# 2. Centralized vs Non-Centralized Databases

## Centralized Database

1. Data is stored in **one single location**.
2. All users access the **same central server**.
3. Easy to manage but may cause **slow performance if many users access it**.

### Advantages

* Easy management
* Strong security

### Disadvantages

* Single point of failure
* Network congestion

---

## Non-Centralized Database (Distributed Database)

1. Data is stored in **multiple locations or computers**.
2. Each location can **process its own data**.
3. All locations are connected by a **network**.

### Advantages

* Faster access
* Better reliability
* Load is distributed

### Disadvantages

* Complex management
* Higher cost

---

# 3. Homogeneous Distributed Database

1. All databases use **same DBMS software**.
2. Same **data model and structure**.
3. Easier to manage.

### Example

All locations using **MySQL database**.

---

# 4. Heterogeneous Distributed Database

1. Different locations use **different DBMS systems**.
2. Data models may be **different**.
3. Integration becomes **more complex**.

### Example

One site uses **Oracle**, another uses **MySQL**.

---

# 5. Reference Architecture of DDBMS

Reference architecture describes **how a distributed database system is organized**.

### Components

1. **User Interface** – where users send queries.
2. **Global Query Processor** – processes queries across sites.
3. **Local Query Processor** – processes queries at local site.
4. **Distributed Database** – stores data across multiple locations.

Purpose

* Manage distributed data
* Process queries efficiently
* Maintain data consistency

---

# 6. Distributed Database Design

Distributed database design decides **how data is distributed across multiple sites**.

### Main Techniques

**Fragmentation**

* Breaking database into smaller pieces.

Example

Student table divided by departments.

---

**Replication**

* Copies of data stored at multiple locations.

Example

Same customer data stored in different branches.

---

**Allocation**

* Deciding **where data fragments should be stored**.

---

# 7. Query Processing in Distributed Database

1. Query processing means **executing SQL queries in distributed databases**.
2. The system divides the query into **subqueries for different sites**.
3. Results from all sites are **combined to produce final result**.

Example

User query → Distributed query → Local queries → Final result.

---

# 8. Distributed Concurrency Control

Concurrency control ensures **multiple users can access database simultaneously without conflicts**.

Goal

* Maintain **data consistency**
* Avoid **data conflicts**

---

# 9. Serializability

1. Serializability ensures **transactions produce the same result as if executed one by one**.
2. Even if transactions run simultaneously, the result remains **correct**.

Example

Transaction A and Transaction B should not create wrong data.

---

# 10. Locking Protocols

1. Locking is used to **prevent multiple users from modifying same data at same time**.
2. A transaction **locks a data item before using it**.

### Types of Locks

**Shared Lock**

* Multiple users can **read data**.

**Exclusive Lock**

* Only one user can **modify data**.

---

# 11. Timestamp Protocols

1. Each transaction is given a **timestamp (time value)**.
2. Transactions execute according to **timestamp order**.
3. Helps maintain **serializability**.

Example

Transaction with **earlier timestamp executes first**.

---

# 12. Distributed Deadlock Management

Deadlock occurs when **two or more transactions wait for each other forever**.

Example

Transaction A waiting for resource of B
Transaction B waiting for resource of A

### Solutions

* Deadlock detection
* Deadlock prevention
* Deadlock recovery

---

# 13. Distributed Commit Protocols

Commit protocols ensure **all sites either complete or cancel a transaction together**.

---

# 14. Two-Phase Commit Protocol (2PC)

Used to ensure **all distributed sites agree before committing transaction**.

### Phase 1 – Prepare Phase

Coordinator asks all sites **whether they are ready to commit**.

### Phase 2 – Commit Phase

If all sites agree → transaction **commits**.
If any site fails → transaction **rollbacks**.

---

# 15. Three-Phase Commit Protocol (3PC)

Improved version of **Two Phase Commit**.

### Phases

1. Prepare
2. Pre-Commit
3. Commit

Advantages

* Reduces chances of **system blocking**.

---

# 16. Basic Concept of Object-Oriented Databases

1. Object-Oriented Database (OODB) stores data in **objects instead of tables**.
2. Based on **object-oriented programming concepts**.
3. Objects contain **data and methods**.

Example

Student object

* Name
* Age
* Methods

---

# 17. Limitations of Relational Databases

Relational databases have some limitations.

1. Difficult to handle **complex data types**.
2. Poor support for **multimedia data (images, videos)**.
3. Hard to represent **complex relationships**.
4. Requires many **joins for complex queries**.
5. Not suitable for **object-oriented applications**.

---

# 18. Need for Object-Oriented Databases

Object-Oriented Databases were introduced to overcome relational limitations.

### Advantages

1. Supports **complex data structures**.
2. Integrates with **object-oriented programming languages**.
3. Supports **inheritance and encapsulation**.
4. Better for **multimedia and scientific applications**.

---

# Quick Exam Revision Mind Map

```
Distributed Database
│
├ Centralized vs Distributed
├ Homogeneous vs Heterogeneous
├ Reference Architecture
├ Database Design
│   ├ Fragmentation
│   ├ Replication
│   └ Allocation
│
├ Query Processing
├ Concurrency Control
│   ├ Serializability
│   ├ Locking
│   └ Timestamp
│
├ Deadlock Management
├ Commit Protocols
│   ├ 2PC
│   └ 3PC
│
└ Object Oriented Database
    ├ Limitations of RDBMS
    └ Need for OODB
```
