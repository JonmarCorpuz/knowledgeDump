# Query Information

tmp
```SQL
SHOW user;
```

tmp
```SQL
DESCRIBE table_name;
```

Retrieve the list of table names of the tables that are accessible to the current user from the `tab` view
```SQL
SELECT tname FROM tab;
```

<br>

# Connect to Database

tmp
```SQL
conn username/password@localhost:1521/XEPDB1;
```

tmp
```SQL
conn username/password@localhost:1521/XEPDB1 as sysdba;
```

<br>

# Modify Table

## Columns

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

Drop a column
```SQL
ALTER TABLE table_name
DROP COLUMN column_name;
```

<br>

## Constraints

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

<br>

# Database Users

Create a user
```SQL
CREATE USER username IDENTIFIED BY 'password'
[default tablespace users temporary tablespace temp];
```

Grant permissions
```SQL
GRANT dba, connect, resource TO username;
```

<br>

# Oracle Database Commands

## Query Informatio

Show database name, open mode, and database status blocks
```SQL
SELECT name, open_mode, dsb FROM v$database;
```

<br>

## Modify Databases

Open all pluggable databases under a multitenant container database in order to make them accessible for use
```SQL
ALTER pluggable DATABASE all OPEN;
```

Save the open/close state of all pluggable databases so that they return to the same state upon restart
```SQL
ALTER pluggable DATABASE all SAVE STATE;
```


