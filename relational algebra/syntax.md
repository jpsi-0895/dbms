# Relational Algebra

Relational algebra is a fundamental theory used in database management systems (`DBMS`) for querying and manipulating relational data.

It provides a set of operations that can be performed on relations (`tables`).

## 1. Selection (σ)

Filters rows based on a specified condition.

**Syntax:**

```
σ(condition)(Relation)
```

**Example:**

```
σ(age > 30)(Employees)
```

This retrieves all employees older than 30.

## 2. Projection (π)

Selects specific columns from a relation.

**Syntax:**

```
π(column1, column2, ...)(Relation)
```

**Example:**

```
π(name, age)(Employees)
```

This retrieves only the names and ages of employees.

## 3. Union (∪)

Combines the results of two relations, removing duplicates.

**Syntax:**

```
Relation1 ∪ Relation2
```

**Example:**

```
Managers ∪ Employees
```

This retrieves all distinct records from both tables.