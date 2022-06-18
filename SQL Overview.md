# `SQL`

<a href=#use>USE</a> | <a href=#select>SELECT</a>


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
