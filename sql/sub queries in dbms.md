# Sub query in DBMS

Subqueries in a Database Management System (DBMS) are queries nested within another query.

They can be used in various SQL statements, such as `SELECT`, `INSERT`, `UPDATE`, and `DELETE`.

### Usage in SQL Statements

- `In SELECT`: Retrieve specific data based on another query.

- `In WHERE`: Filter records based on conditions from another query.

- `In FROM`: `Use the result of a subquery as a table`.

`Example:`

```sql
INSERT INTO high_earners (employee_name, salary)
SELECT employee_name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
