# SELECT query follows a specific sequence

In SQL, the order of execution for a SELECT query follows a specific sequence, regardless of the order in which you write the clauses.

## Order of Execution for a SELECT Statement

1. FROM:

The database identifies the tables or views from which to retrieve data. This includes executing any joins.

2. WHERE:

The WHERE clause filters the rows returned by the FROM clause based on specified conditions.

3. GROUP BY:

If aggregation is involved, the rows are grouped based on the specified columns.

4. HAVING:

The HAVING clause filters the groups created by GROUP BY. This is typically used to apply conditions to aggregated data.

5. SELECT:

The SELECT clause specifies the columns to be returned in the result set. This is where any expressions or calculations are applied.

6. ORDER BY:

Finally, the ORDER BY clause sorts the result set based on specified columns.

7. LIMIT / OFFSET:

If applicable, the `LIMIT` clause restricts the number of rows returned. `OFFSET` specifies where to start returning rows.

**Example**:

```sql
SELECT department_name, AVG(salary) AS avg_salary
FROM employees e
JOIN departments d ON e.department_id = d.department_id
WHERE e.salary > 50000
GROUP BY department_name
HAVING AVG(salary) > 60000
ORDER BY avg_salary DESC
LIMIT 10;
```
