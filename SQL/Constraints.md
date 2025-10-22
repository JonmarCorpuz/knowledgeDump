# Constraint Overview

Constraints in SQL are rules applied to columns or tables to enforce the accuracy, integrity, and validity of the data stored in a database

* Prevents invalid data from being inserted into the table
* Helps maintain consistency between related tables
* Ensures that relationships between records stay correct and accurate

<br>

# Constraint Types

## Value Constraints

| Constraint Type | Description |
| --- | --- |
| `NOT NULL` | Ensures that a column can't contain null values |
| `UNIQUE` | Ensures that all values in a column are distinct across all rows |
| `DEFAULT value` | Automatically assigns a specified value to a column when no value is provided during data insertion |

## Condition Constraints

| Constraint Type | Description |
| --- | --- |
| `CHECK (CONDITION)` | Ensures that the values in a column meet a specified condition or logical expression |

## Relationship Constraints

| Constraint Type | Description |
| --- | --- |
| `PRIMARY KEY` | |
| `FOREIGN KEY (column_name) REFERENCES table_name(column_name)` | |
