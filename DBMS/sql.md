Below is a **point-wise explanation in simple language** for **exam preparation**. The points are short so you can **remember easily and write directly in the exam**.

---

# 1. Structured Query Language (SQL)

1. SQL stands for **Structured Query Language**.
2. It is used to **communicate with relational databases**.
3. SQL helps to **create, insert, update, delete, and retrieve data**.
4. It works with **tables (relations)** in a database.
5. SQL is supported by most DBMS like **MySQL, Oracle, PostgreSQL, SQL Server**.

Example

```sql
SELECT * FROM Student;
```

---

# 2. SQL Commands

SQL commands are divided into **five main categories**.

1. **DDL – Data Definition Language**
2. **DML – Data Manipulation Language**
3. **DQL – Data Query Language**
4. **DCL – Data Control Language**
5. **TCL – Transaction Control Language**

---

# 3. Data Definition Language (DDL)

DDL is used to **define and modify database structure**.

### Common DDL Commands

**CREATE**
Creates database objects like tables.

```sql
CREATE TABLE Student(
ID INT,
Name VARCHAR(50)
);
```

**ALTER**
Modifies existing table structure.

```sql
ALTER TABLE Student ADD Age INT;
```

**DROP**
Deletes table or database.

```sql
DROP TABLE Student;
```

**TRUNCATE**
Deletes all records from table.

```sql
TRUNCATE TABLE Student;
```

---

# 4. Data Manipulation Language (DML)

DML is used to **insert, update, and delete records in a table**.

### Common Commands

**INSERT**

```sql
INSERT INTO Student VALUES (1,'Rishi',22);
```

Adds new record.

---

**UPDATE**

```sql
UPDATE Student
SET Age = 23
WHERE ID = 1;
```

Modifies existing record.

---

**DELETE**

```sql
DELETE FROM Student
WHERE ID = 1;
```

Removes records.

---

# 5. Data Control Language (DCL)

DCL is used to **control user access and permissions**.

### Commands

**GRANT**

```sql
GRANT SELECT ON Student TO user1;
```

Gives permission to user.

---

**REVOKE**

```sql
REVOKE SELECT ON Student FROM user1;
```

Removes permission.

---

# 6. Transaction Control Language (TCL)

TCL is used to **manage database transactions**.

### Commands

**COMMIT**

```sql
COMMIT;
```

Saves changes permanently.

---

**ROLLBACK**

```sql
ROLLBACK;
```

Undo changes.

---

**SAVEPOINT**

```sql
SAVEPOINT A;
```

Creates a checkpoint in transaction.

---

# 7. Queries Using ORDER BY

Used to **sort records** in ascending or descending order.

Example

```sql
SELECT * FROM Student
ORDER BY Name;
```

Ascending order.

```sql
SELECT * FROM Student
ORDER BY Marks DESC;
```

Descending order.

---

# 8. Queries Using WHERE

WHERE clause is used to **filter records based on conditions**.

Example

```sql
SELECT * FROM Student
WHERE Age > 20;
```

Only students with age greater than 20.

---

# 9. Queries Using GROUP BY

GROUP BY is used to **group rows with same values**.

Example

```sql
SELECT Department, COUNT(*)
FROM Student
GROUP BY Department;
```

Counts number of students in each department.

---

# 10. Nested Queries

A nested query is a **query inside another query**.

Example

```sql
SELECT Name
FROM Student
WHERE Marks >
(SELECT AVG(Marks) FROM Student);
```

Find students with marks greater than average.

---

# 11. Joins

Joins are used to **combine data from multiple tables**.

### Types of Joins

**1. Inner Join**

Returns matching records from both tables.

```sql
SELECT Student.Name, Course.CourseName
FROM Student
INNER JOIN Course
ON Student.CourseID = Course.ID;
```

---

**2. Left Join**

Returns all records from **left table**.

---

**3. Right Join**

Returns all records from **right table**.

---

**4. Full Join**

Returns records from **both tables**.

---

# 12. Views

1. View is a **virtual table created from a query**.
2. It does not store data permanently.
3. It shows **data from one or more tables**.

Example

```sql
CREATE VIEW StudentView AS
SELECT Name, Age FROM Student;
```

Use

```sql
SELECT * FROM StudentView;
```

---

# 13. Sequences

1. Sequence is used to **generate unique numbers automatically**.
2. Often used for **primary keys**.

Example

```sql
CREATE SEQUENCE student_seq
START WITH 1
INCREMENT BY 1;
```

---

# 14. Indexes

1. Index is used to **speed up data searching**.
2. Works similar to **index in a book**.
3. Created on frequently searched columns.

Example

```sql
CREATE INDEX idx_name
ON Student(Name);
```

---

# 15. Synonyms

1. Synonym is an **alternate name for database objects**.
2. It simplifies query writing.

Example

```sql
CREATE SYNONYM Stud FOR Student;
```

---

# 16. Table Handling

Table handling means **creating and managing tables in database**.

### Common operations

**Create Table**

```sql
CREATE TABLE Student(
ID INT,
Name VARCHAR(50),
Age INT
);
```

---

**Insert Data**

```sql
INSERT INTO Student VALUES (1,'Rishi',22);
```

---

**View Table**

```sql
SELECT * FROM Student;
```

---

**Delete Table**

```sql
DROP TABLE Student;
```

---

# Quick SQL Exam Revision

```
SQL
│
├ DDL → CREATE, ALTER, DROP
├ DML → INSERT, UPDATE, DELETE
├ DCL → GRANT, REVOKE
├ TCL → COMMIT, ROLLBACK
│
├ WHERE → Filter rows
├ ORDER BY → Sort rows
├ GROUP BY → Group data
├ Nested Query → Query inside query
│
├ Joins → Combine tables
├ Views → Virtual table
├ Sequences → Auto numbers
├ Index → Fast searching
└ Synonyms → Alternate names
```

---

✅ **Exam Tip:**
Very common **5-mark questions** from this topic:

* Difference between **DDL and DML**
* Types of **SQL commands**
* **Joins in SQL**
* **Views and Indexes**
* **Nested Queries**

---

If you want, I can also make a **SQL cheat sheet (all commands in 1 page)** that is **perfect for last-day revision before MCA exams**.



Here is the **same topic explained in very simple language with short points** so you can **remember the meaning easily for exams**.

---

# Types of SQL Commands

SQL commands are divided into **five main categories** depending on what they do in the database.

---

# 1. DDL – Data Definition Language

**Meaning:**
DDL is used to **create or change the structure of the database or tables**.

### Simple Idea

DDL = **Designing the database structure**

### Commands

**CREATE**

* Used to **create a new table or database**.

Example

```sql
CREATE TABLE Student;
```

Meaning: Create a table named Student.

---

**ALTER**

* Used to **change the structure of an existing table**.

Example

```sql
ALTER TABLE Student ADD Age;
```

Meaning: Add a new column Age in Student table.

---

**DROP**

* Used to **delete a table or database completely**.

Example

```sql
DROP TABLE Student;
```

Meaning: Delete the Student table.

---

**TRUNCATE**

* Used to **remove all records from a table but keep the table structure**.

Example

```sql
TRUNCATE TABLE Student;
```

Meaning: Delete all data in Student table.

---

# 2. DML – Data Manipulation Language

**Meaning:**
DML is used to **add, change, or remove data in tables**.

### Simple Idea

DML = **Working with the data inside tables**

### Commands

**INSERT**

* Used to **add new data into a table**.

Example

```sql
INSERT INTO Student VALUES (1,'Rishi');
```

Meaning: Add a new student record.

---

**UPDATE**

* Used to **modify existing data**.

Example

```sql
UPDATE Student SET Age = 22;
```

Meaning: Change the age value.

---

**DELETE**

* Used to **remove records from a table**.

Example

```sql
DELETE FROM Student WHERE ID = 1;
```

Meaning: Delete student with ID = 1.

---

# 3. DQL – Data Query Language

**Meaning:**
DQL is used to **retrieve (get) data from the database**.

### Simple Idea

DQL = **Searching or viewing data**

### Command

**SELECT**

* Used to **display data from a table**.

Example

```sql
SELECT * FROM Student;
```

Meaning: Show all student records.

---

# 4. DCL – Data Control Language

**Meaning:**
DCL is used to **control user permissions and security**.

### Simple Idea

DCL = **Giving or removing access to users**

### Commands

**GRANT**

* Gives permission to a user.

Example

```sql
GRANT SELECT ON Student TO user1;
```

Meaning: Allow user1 to view Student table.

---

**REVOKE**

* Removes permission from a user.

Example

```sql
REVOKE SELECT ON Student FROM user1;
```

Meaning: Remove access from user1.

---

# 5. TCL – Transaction Control Language

**Meaning:**
TCL is used to **manage database transactions (changes made to database)**.

### Simple Idea

TCL = **Saving or undoing changes**

### Commands

**COMMIT**

* Saves changes permanently.

Example

```sql
COMMIT;
```

Meaning: Save all changes.

---

**ROLLBACK**

* Cancels changes and returns to previous state.

Example

```sql
ROLLBACK;
```

Meaning: Undo changes.

---

**SAVEPOINT**

* Creates a checkpoint in a transaction.

Example

```sql
SAVEPOINT A;
```

Meaning: Create a point to return later.

---

# Easy Memory Trick for Exam

Remember this order:

```
DDL → Structure
DML → Data change
DQL → Data view
DCL → Control access
TCL → Transaction control
```

or simply:

```
Define
Modify
Query
Control
Transaction
```

---

If you want, I can also give you a **very small 5-line definition version (perfect for 2-mark questions)** which many teachers expect in **MCA DBMS exams**.
