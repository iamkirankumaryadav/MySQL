# `SQL`

<a href=#use>USE</a> | <a href=#select>SELECT</a> | <a href=#top>TOP</a> | <a href=#limit>LIMIT</a>


<h4 name=use>1. USE</h4> 

Select database

```mysql
# Database name:
USE Enterprise;
```


<h4 name=select>2. SELECT</h4> 

Select | Read table.

```mysql
# Select string or integer:
SELECT 'Kirankumar Yadav';
SELECT 1 * 7;

# Select Table ( All the rows and columns )
SELECT * FROM Employee;

# Select required columns from table:
SELECT 
'Kirankumar' || ' ' || 'Yadav' AS Name, 
Age, 
Designation, 
Salary 
FROM Employee;

# Select total rows of table:
SELECT COUNT(*) FROM Employee;
``` 

<h4 name=top>3. TOP</h4> 

```mysql
SELECT TOP 5 * FROM Employee;
```

<h4 name=top>4. LIMIT</h4> 

```mysql
SELECT 
Name, 
Designation
FROM Employee
LIMIT 5;

```
