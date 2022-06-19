# `SQL`

<a href=#use>USE</a> | <a href=#select>SELECT</a> | <a href=#top>TOP</a> | <a href=#limit>LIMIT</a> | <a href=#orderby>ORDER BY</a> | <a href=#insert>INSERT INTO</a> | <a href=#update>UPDATE</a>


<h3 name=use><b>1. USE</b></h3> 

Select database

```mysql
# Database name:
USE Enterprise;
```


<h3 name=select><b>2. SELECT</b></h3> 

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

<h3 name=top><b>3. TOP</b></h3> 

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

<h3 name=orderby><b>5. ORDER BY</b></h3>

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

<h3 name=insert><b>6. INSERT INTO</b></h3>

The `INSERT INTO` statement is used to insert new records in a table.

```mysql
INSERT INTO Employee (Name, Age, Designation)
VALUES ('Kirankumar Yadav', 26, 'IT Analyst')
```

<h3 name=update><b>7. UPDATE</b></h3>

The `UPDATE` statement is used to modify the existing records in a table.

```mysql
UPDATE Employee
SET Designation = 'Data Scientist'
WHERE Name = 'Kirankumar Yadav';
```
