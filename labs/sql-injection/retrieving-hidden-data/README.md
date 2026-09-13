# SQL Injection

## Overview

SQL Injection (SQLi) is a web security vulnerability that occurs when an application incorporates untrusted user input into SQL queries without safely separating data from SQL syntax.

An attacker may be able to manipulate the structure or logic of a SQL query and cause the application to perform unintended database operations.

SQL Injection can potentially result in:

- Unauthorized access to sensitive data
- Authentication bypass
- Modification or deletion of database records
- Access to data belonging to other users
- Database enumeration
- In some cases, compromise of underlying systems

---

## How SQL Injection Happens

A typical vulnerable application may construct a SQL query by concatenating user input directly into the query.

Example:

```sql
SELECT * FROM products
WHERE category = 'Gifts'
AND released = 1;