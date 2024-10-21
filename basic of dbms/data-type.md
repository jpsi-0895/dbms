## Numeric Data Types

- `INT`: A standard integer type. Varies in size (e.g., `TINYINT`, `SMALLINT`, `MEDIUMINT`, `BIGINT`).
- `FLOAT`: A floating-point number, which can have decimal values. Precision may vary.
- `DOUBLE`: A double-precision floating-point number.
- `DECIMAL` (or NUMERIC): Exact numeric data type with a defined precision and scale (e.g., `DECIMAL(10, 2)` for numbers with up to 10 digits, 2 of which can be after the decimal).

## Character Data Types

- `CHAR`(n): A fixed-length string. If the input is shorter than n, it's padded with spaces.
- `VARCHAR`(n): A variable-length string that can hold up to n characters.
- `TEXT`: A large variable-length string, typically used for large blocks of text.

## Date and Time Data Types

`DATE`: Stores dates in the format YYYY-MM-DD.
`TIME`: Stores time in the format HH:MM:SS.
`DATETIME`: Combines date and time in the format YYYY-MM-DD HH:MM:SS.
`TIMESTAMP`: Similar to DATETIME, but often used to track changes in records. It usually includes timezone information.
`YEAR`: Stores year values, often in a 2 or 4-digit format.

## Binary Data Types

- `BINARY`(n): A fixed-length binary data type.
- `VARBINARY`(n): A variable-length binary data type.
- `BLOB`: Used for storing large binary objects like images or files.
