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

## 2. UNIQUE

**Purpose**: Ensures that all values in a column (or a combination of columns) are unique across the table.
**Example**:

```sql
CREATE TABLE Users (
    UserID INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE
);
```

## 3. PRIMARY KEY

**Purpose**: Combines the properties of NOT NULL and UNIQUE. It uniquely identifies each record in a table.
**Example**:

```sql
CREATE TABLE Products (
    ProductID INT PRIMARY KEY,
    ProductName VARCHAR(100)
);
```

## 4. FOREIGN KEY

Purpose: Ensures referential integrity by linking a column in one table to a primary key in another table.
Example:

```sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
```
