# Query Information

Return the current user account that's connected to the database server
```SQL
SHOW user;
```

Display the structure (schema) of a table
```SQL
DESCRIBE table_name;
```

Retrieve the list of table names of the tables that are accessible to the current user from the `tab` view
```SQL
SELECT tname FROM tab;
```

<br>

# Connect to Database

Connect as a normal user to the database
```SQL
conn username/password@localhost:1521/database_name;
```

Connect as a database administrator with full system privileges to the database
```SQL
conn username/password@localhost:1521/database_name as sysdba;
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

## Connect to Database

Connect as a normal user to 
```SQL
conn username/password@localhost:1521/XEPDB1;
```

Connect as a database administrator with full system privileges
```SQL
conn username/password@localhost:1521/XEPDB1 as sysdba;
```

Add primary key to column
```SQL
CREATE TABLE table_name (
  column_name data_type [constraint],
  PRIMARY KEY (column_name)
);
```

Add a foreign key to table
```SQL
CREATE TABLE table_name (
  column_name data_type [constraint],
  FOREIGN KEY (column_name) REFERENCE foreign_table_name(foreign_column_name)
);
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


