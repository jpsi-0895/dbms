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

## 4. Set Difference (−)

Returns records in one relation that are not in another.

**Syntax:**

```
Relation1 − Relation2
```

**Example:**

```
Employees − Managers
```

This retrieves employees who are not managers.

## 5. Cartesian Product (×)

Combines all rows from two relations, creating a new relation.

**Syntax:**

```
Relation1 × Relation2
```

**Example:**

```
Employees × Departments
```

This produces a relation with every combination of employees and departments.

## 6. Rename (ρ)

Renames a relation or its attributes.

**Syntax:**

```
ρ(new_relation_name, Relation)
```

**Example:**

```
ρ(Staff, Employees)
```

This renames the Employees `relation` to `Staff`.

## 7. Join (⨝)

Combines related tuples from two relations based on a condition.

**Syntax:**

```
Relation1 ⨝ condition Relation2
```

**Example:**

```
Employees (table) ⨝ `Employees.department_id = Departments.id`(condition) Departments (table)
```

This retrieves all employee records along with their department information.

## Combining Operations

Relational algebra allows the combination of these operations to form complex queries. For example:

```
π(name)(σ(age > 30)(Employees)) ∪ π(name)(Managers)
```

This retrieves the names of employees older than 30 and all managers.

## Importance in DBMS

Relational algebra serves as a theoretical foundation for SQL and is used in query optimization. Understanding relational algebra can help database designers and developers create efficient queries and understand how data is processed in a relational database.
