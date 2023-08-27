Tables in a Relational database consist of rows and columns
# Creating a table
```
CREATE TABLE employees (
	employee_id INT NOT NULL AUTO_INCREMENT,
	first_name VARCHAR(50),
	last_name VARCHAR(50),
	hourly_pay DECIMAL(5, 2),
	hire_date DATE
	PRIMARY KEY (employee_id)
);
```

To create table we make a table name followed by parentheses.

Inside the parentheses we list each column.

after each column name we list the datatype.

**Note**: NOT NULL keyword can be used to ensure a column is always required 

[Datatypes for MySQL](https://www.w3schools.com/mysql/mysql_datatypes.asp)
## Primary keys

Primary keys are unique identifiers that are used to identify individual rows within a table.

**Note:** AUTO_INCREMENT can be used to automatically generate an id for each new addition to a table. This is useful for creating unique primary keys.
## Foreign keys

Foreign keys are use to reference rows in another table.
```
FOREIGN KEY (band_id) REFERENCES bands(id)
```
Must specify which column will act as the foreign key and which column it is referring to in the other table.
# Selecting a table
```
SELECT * FROM employees;
```

Asterisk grabs all columns from a selected table.
## Limiting entries
```
SELECT * FROM employees LIMIT 2;
```

Use LIMIT keyword to limit the amount of entries returned.

This will only return the first 2 entries of the table.
## Ordering entries
```
SELECT * FROM employees ORDER BY first_name DESCENDING;
```
You can choose a column to order your query by.

**Note:** use key word ascending/descending to change the default order. It is ascending by default

## Unique rows
```
SELECT DISTINCT first_name FROM employees;
```

The distinct keyword will return only unique rows in you table.
# Renaming a table
```
RENAME TABLE employees TO workers;
```
# Altering a table
```
ALTER TABLE employees
ADD phone_number VARCHAR(15);
```
## Renaming a column
```
ALTER TABLE employees
RENAME COLUMN phone_number TO email;
```
## Changing column datatype
```
ALTER TABLE employees
MODIFY COLUMN email VARCHAR(100)
```
## Moving column
```
ALTER TABLE employees
MODIFY email VARCHAR(100)
AFTER last_name;
```

# Inserting entry into table
```
INSERT INTO bands (name)
VALUES ('Iron Maiden');
```
 to insert multiple entries put columns between values.

# Updating entries
```
UPDATE albums
SET release_year = 1982
WHERE id = 1;
```

WHERE keyword can be added to almost all queries in order to specify which row or column you want to modify.

Used commonly to filter results of a select query.