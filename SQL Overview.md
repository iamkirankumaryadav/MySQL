# `SQL`

<a href=#use>USE</a> | <a href=#select>SELECT</a> | <a href=#top>TOP</a> | <a href=#limit>LIMIT</a> | <a href=#orderby>ORDER BY</a> | <a href=#insert>INSERT</a> | <a href=#update>UPDATE</a>


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

# Select columns from table:
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name, Age, Designation, Salary 
FROM Employee;

# Count total rows of table:
SELECT COUNT(*) FROM Employee;

# Count rows of particular column:
SELECT COUNT(Name) FROM Employee;
``` 

<h4 name=top>3. TOP</h4> 

```mysql
SELECT TOP 5 * FROM Employee;
```

<h4 name=top>4. LIMIT</h4> 

```mysql
SELECT Name, Designation
FROM Employee
LIMIT 5;

# Offset
SELECT Name, Designation
FROM Employee
LIMIT 10, 5;
```

<h4 name=orderby>5. ORDER BY</h4>

```mysql
# Order by single column:
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name, Age, Designation, Salary 
FROM Employee
ORDER BY Name;

# Order by multiple columns:
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name, Age, Designation, Salary 
FROM Employee
ORDER BY Name ASC Age DESC;
```

<h4 name=insert>6. INSERT</h4>

```mysql
INSERT INTO Employee (Name, Age, Designation)
VALUES ('Kirankumar Yadav', 26, 'IT Analyst')
```

<h4 name=update>7. UPDATE</h4>

```mysql
UPDATE Employee
SET Designation = 'Data Scientist'
WHERE Name = 'Kirankumar Yadav';
```
