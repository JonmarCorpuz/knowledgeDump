# SQL Commands

## Modify Table

### Columns

Rename a column in an existing table
```SQL
ALTER TABLE table_name
RENAME COLUMN current_column_name TO new_column_name
```

Add new column to an existing table
```SQL
ALTER TABLE table_name
ADD column_name DATA_TYPE;
```

Modify a column in an existing table
```SQL
ALTER TABLE table_name
MODIFY COLUMN column_name NEW_DATA_TYPE [CONSTRAINTS];
```

<br>

### Constraints

Add a constraint to a column in an existing table
```SQL
ALTER TABLE table_name
ADD CONSTRAINT constraint_name CONSTRAINT_TYPE (column_name);
```

Drop a constraint from a column in an existing table
```SQL
ALTER TABLE table_name
DROP CONSTRAINT constraint_name;
```
