# Constraints in sql

In SQL, constraints are rules applied to table columns that enforce data integrity and ensure the accuracy and reliability of the data.

## 1. NOT NULL

**Purpose**: Ensures that a column cannot have a NULL value.
**Example**:

```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL
);
```
