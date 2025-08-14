# 📚 SQL Notes – Complete Guide

A well-structured SQL notes repository covering **everything from basics to advanced concepts**.  
This guide is designed to help you **understand, practice, and master SQL** for data analysis, database management, and development.

---

## 🗂 Topics Covered

### 1. **📖 Introduction to SQL**
- What is SQL?
- History & Importance
- Popular SQL Databases (MySQL, PostgreSQL, SQL Server, etc.)
- SQL Syntax Basics

### 2. **🔹 Basic Data Operations**
- `SELECT` statement
- `DISTINCT` keyword
- `ORDER BY` and `LIMIT`

### 3. **🛠 CRUD Operations**
- `CREATE` – Create tables
- `INSERT` – Insert data
- `READ` – Query data
- `UPDATE` – Modify existing records
- `DELETE` – Remove records

### 4. **✏ Data Changing Operations**
- `ALTER TABLE`
- `DROP TABLE`
- `RENAME`
- `TRUNCATE`

### 5. **🔤 String Operations**
- `CONCAT`, `SUBSTRING`, `LENGTH`
- `UPPER`, `LOWER`, `TRIM`
- Pattern Matching using `LIKE` & `REGEXP`

### 6. **📊 Aggregate Functions**
- `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- `GROUP BY` & `HAVING`

### 7. **🔗 Joins**
- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN`
- `FULL OUTER JOIN`
- `SELF JOIN`
- Cross Joins & Use Cases

### 8. **🔄 CASE Statements**
- Conditional Logic in SQL
- Using `CASE` in `SELECT`, `WHERE`, `ORDER BY`

### 9. **📥 Subqueries**
- Single-row Subqueries
- Multi-row Subqueries
- Correlated Subqueries
- Subqueries in `FROM` clause

### 10. **📅 Date Manipulation**
- `DATE()`, `NOW()`, `CURRENT_TIMESTAMP`
- Date arithmetic (`DATE_ADD`, `DATE_SUB`)
- Extracting parts of date (`YEAR`, `MONTH`, `DAY`)

### 11. **📈 Window Functions**
- `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`
- `LEAD()` & `LAG()`
- Running Totals & Moving Averages
- `PARTITION BY` and `ORDER BY`

### 12. **👁 Views**
- Creating & Using Views
- Updating data through Views
- Advantages & Limitations

### 13. **⚡ Indexes & Partitioning**
- Types of Indexes (Clustered, Non-Clustered, Unique)
- When & Why to Use Indexes
- Data Partitioning – Range, List, Hash

### 14. **⚙ Stored Procedures & Triggers**
- Writing & Executing Stored Procedures
- Input & Output Parameters
- Triggers – BEFORE, AFTER events
- Automating tasks with triggers

### 15. **🛡 Transaction Control Language (TCL)**
TCL commands manage transactions in a database, ensuring **data integrity**.

| Command | Description |
|---------|-------------|
| `COMMIT` | Saves all changes made by the current transaction. |
| `ROLLBACK` | Undoes all changes made by the current transaction. |
| `SAVEPOINT` | Sets a point within a transaction to which you can later roll back. |
| `SET TRANSACTION` | Configures the properties of a transaction. |

### 16.  **🔐 Data Control Language (DCL)**

DCL commands control access rights & permissions in a database.

**Command  	    Description** 
**GRANT**	        Gives a user access privileges to the database.
**REVOKE**	      Removes previously granted privileges from a user.

Example:

GRANT SELECT, INSERT ON employees TO 'user1'@'localhost';
REVOKE INSERT ON employees FROM 'user1'@'localhost';

**Example:**
```sql
START TRANSACTION;
UPDATE accounts SET balance = balance - 100 WHERE account_id = 1;
UPDATE accounts SET balance = balance + 100 WHERE account_id = 2;
COMMIT;
```
---

## 📌 How to Use These Notes
1. Go through topics **in order** if you’re a beginner.
2. Practice each query using an SQL database (MySQL, PostgreSQL, etc.).
3. Try combining concepts (e.g., JOIN + Aggregate Functions).
4. Review & revise with real-world datasets.

---

## 💡 Tips for Mastery
- **Practice daily** – SQL is best learned by doing.
- Use **real datasets** instead of dummy data.
- Experiment with different SQL engines.
- Keep optimizing queries for performance.

---

## 📬 Contribution
If you have improvements or more examples, feel free to **open a pull request** or share your ideas.

---

**Author:** Tushar Gupta  
🚀 _Happy Querying!_

