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
