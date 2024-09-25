# Execute the Subquery in the FROM Clause

When you execute a subquery in the `FROM` clause, it essentially acts as a temporary table or derived table for the outer query to use.

## How Subqueries in the FROM Clause Work

1. `Subquery Execution`: The subquery in the `FROM` clause is executed first. It produces a result set that can be treated like a table.

2. `Outer Query`: The outer query then references this result set, allowing you to perform further operations such as `filtering`, `aggregation`, or `joining` with other tables.

### Example
Let’s say we have two tables: employees and departments. We want to find the average salary of employees in each department but only for departments located in a specific location.