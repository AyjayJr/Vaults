# Creating a Database

The query to create a database:
```
CREATE DATABASE myDB;
```
Note: Keywords in MySQL are case-insensitive. Common to be UPPERCASE. All queries must end in semicolon.
# Selecting a Database
```
USE myDB;
```
# Drop a Database
```
DROP DATABASE myDB;
```
Note: Basically deletion
# Make Read-only
```
ALTER DATABASE myDB READ ONLY = 1;
```
Note: Set to 0 to be able to alter database