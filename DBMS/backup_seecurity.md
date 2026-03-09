Here are **easy exam notes with small definitions**.

---

# 15. Backup and Recovery Techniques

## Backup

**Backup** means creating a **copy of the database and storing it in another location** so that data can be restored if a failure occurs.

### Types of Backup

**1. Full Backup**
A **complete copy of the entire database** is stored.

Example:
All tables and data are copied.

---

**2. Incremental Backup**
Only the **data that changed after the last backup** is saved.

Example:
If a backup was taken yesterday, today only the **new or changed data** is backed up.

---

**3. Differential Backup**
It stores **all changes made since the last full backup**.

Example:
If the last full backup was on Sunday, every day the backup contains **all changes since Sunday**.

---

## Recovery

**Recovery** is the process of **restoring the database to a correct state after failure** using backups and transaction logs.

Example:
If the system crashes, the database uses **backup files and logs to restore lost data**.

---

# 16. Security and Integrity

## Security

**Database security** means **protecting the database from unauthorized users, access, or attacks**.

Goal:

* Protect data
* Prevent misuse
* Keep information safe

---

### Security Methods

**1. Authentication**
Authentication means **verifying the identity of a user before allowing access to the database**.

Example:

* Username and password
* OTP
* Biometric login

---

**2. Encryption**
Encryption means **converting data into a coded form so that unauthorized users cannot understand it**.

Example:
Sensitive data like passwords are stored in **encrypted format**.

---

**3. Access Control**
Access control means **giving specific permissions to users to access or modify data**.

Example:

* Admin → full access
* User → only read data

---

## Integrity

**Data integrity** means **maintaining the accuracy and consistency of data in the database**.

Example:

* No duplicate primary keys
* Valid data values

---

✅ **Short exam definition:**

* **Backup:** Copy of database stored for safety.
* **Recovery:** Restoring database after failure.
* **Security:** Protecting database from unauthorized access.
* **Integrity:** Ensuring data remains accurate and consistent.
