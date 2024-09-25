# Execute the Subquery in the FROM Clause

When you execute a subquery in the `FROM` clause, it essentially acts as a temporary table or derived table for the outer query to use.

## How Subqueries in the FROM Clause Work

1. `Subquery Execution`: The subquery in the `FROM` clause is executed first. It produces a result set that can be treated like a table.

2. `Outer Query`: The outer query then references this result set, allowing you to perform further operations such as `filtering`, `aggregation`, or `joining` with other tables.

### Example

Let’s say we have two tables: `employees` and `departments`. We want to find the average salary of employees in each department but only for `departments` located in a specific location.

```sql
SELECT department_name, avg_salary
FROM (
    SELECT d.department_name, AVG(e.salary) AS avg_salary
    FROM departments d
    JOIN employees e ON d.department_id = e.department_id
    WHERE d.location_id = 1000
    GROUP BY d.department_name
) AS department_avg;
```

### Step-by-Step Execution

1. Execute the Subquery:

   - The subquery (SELECT d.department_name, AVG(e.salary) AS avg_salary ... GROUP BY d.department_name) runs first. It joins the departments and employees tables, filters based on location_id, and calculates the average salary for each department located at that specific location.

2. Result of the Subquery:

   - Assume the subquery returns the following result set:

```sql
department_name | avg_salary
----------------|-----------
Sales          | 60000
Marketing      | 55000
```

3. Outer Query Execution:

   - The outer query then selects department_name and avg_salary from the result of the subquery, which is treated like a table named department_avg.

4. Final Output:

   - The outer query returns the final result based on the data provided by the subquery.
