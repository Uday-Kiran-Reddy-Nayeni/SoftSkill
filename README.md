# Structured Query Language (SQL)

>**SQL** is a standard Database language that is used to create, maintain and retrieve the relational database.

<div style='text-align:center'><img src="https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/sql-server-and-relational-database-part-one/Images/image001.png" style="background-color:white"></div>

## RDBMS

- RDBMS stands for Relational Database Management System. It is the basis for SQL.

- The data in RDBMS is stored in database objects called tables. A table is a collection of related data entries and consists of columns and rows.

### SQL standard and proprietary extensions

- An official SQL standard was adopted by the American National Standards Institute (ANSI) in 1986.

- International Organization for Standardization, known as ISO, in 1987.

- More than a half-dozen joint updates to the standard has been released by the two standards development bodies since then.

## RDBMS built on SQL

- Microsoft SQL Server

- Oracle Database 

- IBM DB2 

- SAP HANA 

- MySQL

- PostgreSQL

# Basic SQL Commands

### SELECT

- Extracts data from a database.

```
SELECT column1, column2, ...
FROM table_name;
```

### SELECT DISTINCT

- The SELECT DISTINCT statement is used to return only distinct (different) values.

```
SELECT DISTINCT column1, column2, ...
FROM table_name;
```
### WHERE

- The WHERE clause is used to filter records.

```
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

### ORDER BY

- The ORDER BY keyword is used to sort the result-set in ascending or descending order.
- The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

```
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

### INSERT INTO

- The INSERT INTO statement is used to insert new records in a table. It can be specified in two ways,

1. Specify both the column names and the values to be inserted:
   
   ```
   INSERT INTO table_name (column1, column2, column3, ...)
   VALUES (value1, value2, value3, ...);
   ```   

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows:
   ```
   INSERT INTO table_name
   VALUES (value1, value2, value3, ...);
   ```

### UPDATE

- Updates data in a database.

```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

### CREATE DATABASE

- Creates data in a database.

```
CREATE DATABASE database_name;
```

### ALTER DATABASE

- Modifies a database.

```
CREATE DATABASE database_name;
```

### CREATE TABLE

- Creates a new table.

```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```

### ALTER TABLE

- Modifies a table.

```
ALTER TABLE table_name
ADD column_name datatype;
```

```
ALTER TABLE table_name
DROP COLUMN column_name;
```

### DROP TABLE

- Deletes a table.

```
DROP TABLE table_name;
```

# SQL Joins

### INNER JOIN

- Returns records that have matching values in both tables.

<div style='text-align:center'><img src="https://www.w3schools.com/sql/img_innerjoin.gif" style="background-color:white"></div>


```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

### LEFT (OUTER) JOIN

- Returns all records from the left table and the matched records from the right table.

<div style='text-align:center'><img src="https://www.w3schools.com/sql/img_leftjoin.gif" style="background-color:white"></div>

```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

### RIGHT (OUTER) JOIN

- Returns all records from the right table and the matched records from the left table.

<div style='text-align:center'><img src="https://www.w3schools.com/sql/img_rightjoin.gif" style="background-color:white"></div>

```
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
```

### FULL (OUTER) JOIN

- Returns all records when there is a match in either left or the right table.

<div style='text-align:center'><img src="https://www.w3schools.com/sql/img_fulljoin.gif" style="background-color:white"></div>

```
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

# SQL Aggregate Functions

### AVG()

- Returns the average value of a numeric column.

```
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

### COUNT()

- Returns the number of items in a column.

```
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

### MAX()

- Returns the maximum value in a column.
   
```
SELECT MAX(column_name)
FROM table_name
WHERE condition;
```

### MIN()

- Returns the minimum value in a column.
  
```
SELECT MIN(column_name)
FROM table_name
WHERE condition;
```

### SUM()

- Returns the sum of all or distinct values in a column.

```
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

## Reference Links

- <https://www.w3schools.com/sql/default.asp>



