# Tranction in dbms

A transaction is a `sequence of operations` performed as a single logical unit of work. Transactions are crucial for maintaining data `integrity` and `consistency` in a database system.

## ACID Properties

Transactions are governed by the ACID properties:

### 1. Atomicity:

Ensures that all operations in a transaction are completed successfully or none at all. If one part fails, the entire transaction is rolled back.

### 2. Consistency:

Guarantees that a transaction will bring the database from one valid state to another, maintaining data integrity. All constraints (e.g., primary keys, foreign keys) must be upheld.

### 3. Isolation:

Ensures that transactions are executed independently. The changes made in a transaction are not visible to other transactions until the transaction is committed.

### 4. Durability:

Once a transaction is committed, its effects are permanent, even in the event of a system crash. The changes are recorded in non-volatile memory.
