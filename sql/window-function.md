# Window functions in SQL

Window functions in SQL are powerful tools that allow you to perform calculations across a set of table rows related to the current row.

They are particularly useful for tasks like calculating running `totals`, `ranking`, and `aggregating` data without collapsing the result set.

```sql
SELECT column1,
       column2,
       WINDOW_FUNCTION() OVER (PARTITION BY column3 ORDER BY column4)
FROM table_name;
```

## Components

1. **WINDOW_FUNCTION**: This can be any aggregate function (like `SUM()`, `AVG()`, `COUNT()`, etc.), ranking function (like `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`), or analytical function.

2. **PARTITION BY**: This clause divides the result set into partitions to which the window function is applied. It’s similar to grouping but does not reduce the number of rows returned.

3. **ORDER BY**: This clause specifies the order of rows within each partition.

### Examples

1. Calculating a Running Total:
2. Ranking Rows:

```sql
SELECT employee_id,
       salary,
       RANK() OVER (ORDER BY salary DESC) AS salary_rank
FROM employees;
```

3. Finding a Moving Average:

```sql
SELECT order_date,
       amount,
       AVG(amount) OVER (ORDER BY order_date ROWS BETWEEN 2 PRECEDING AND CURRENT ROW) AS moving_average
FROM orders;
```

- The OVER() clause in SQL is essential for using window functions. It defines the window or set of rows that the function operates on.

```sql
WINDOW_FUNCTION() OVER (
    [PARTITION BY column1, column2, ...]
    [ORDER BY column3, column4, ...]
    [ROWS | RANGE BETWEEN ...]
)
```
