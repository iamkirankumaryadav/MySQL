# `SQL`

<a href=#use>USE</a> | <a href=#select>SELECT</a> | <a href=#top>TOP</a> | <a href=#limit>LIMIT</a> | <a href=#orderby>ORDER BY</a> | <a href=#create>CREATE</a> | <a href=#insert>INSERT INTO</a> | <a href=#update>UPDATE</a> | <a href=#delete>DELETE</a> | <a href=#drop>DROP</a> | <a href=#join>JOIN</a>

### Finding Databases, Tables and Columns:
```mysql
# Databases:
SHOW DATABASES;

# Tables:
USE Enterprise;
SHOW Tables;

# Columns in a table:
DESCRIBE Employee;
```

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

# Count distinct rows of particular column:
SELECT COUNT(DISTINCT City) FROM Employee;
``` 

<h3 name=top><b>3. TOP</b></h3> 

```mysql
SELECT TOP 5 * FROM Employee;
```

<h4 name=top>4. LIMIT</h4> 

The `LIMIT` clause is used to specify the number of records to return.

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

The `ORDER BY` keyword is used to sort the result-set in ascending or descending order.

```mysql
# Order by single column:
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name, Age, Designation, Salary 
FROM Employee
ORDER BY Name;

# Order by multiple columns:
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name, Age, Designation, Salary 
FROM Employee
ORDER BY Name ASC, Age DESC;
```

<h3 name=create><b>6. CREATE</b></h3>

```mysql
CREATE TABLE Employee
(
  EID INT NOT NULL AUTO_INCREMENT,
  Name VARCHAR(50),
  Age INT,
  Designation VARCHAR(50)
);

CREATE TABLE Personal_Details
(
  ID INT NOT NULL AUTO_INCREMENT,
  EID INT,
  Address VARCHAR(50),
  City VARCHAR(55),
  State VARCHAR(55),
  Pincode CHAR(6),
  Role VARCHAR(55),
  Designation VARCHAR(55)
);
```

```sql
# Check Default Constraints:
SHOW CREATE TABLE Employee;
```

<h3 name=insert><b>7. INSERT INTO</b></h3>

The `INSERT INTO` statement is used to insert new records in a table.

```mysql
INSERT INTO Employee (Name, Age, Designation)
VALUES ('Kirankumar Yadav', 26, 'IT Analyst')
```

<h3 name=update><b>8. UPDATE</b></h3>

The `UPDATE` statement is used to modify the existing records in a table.

```mysql
UPDATE Employee
SET Designation = 'Data Scientist'
WHERE Name = 'Kirankumar Yadav';
```

<h3 name=delete><b>9. DELETE</b></h3>

```mysql
# First use SELECT query to select the exact row to be deleted:
SELECT * FROM Employee WHERE Name = 'Kirankumar Yadav';

# Delete: 
DELETE FROM Employee WHERE Name = 'Kirankumar Yadav';
```

<h3 name=drop><b>10. DROP</b></h3>

```mysql
DROP TABLE Employee;

DROP TABLE IF EXISTS Employee;
```

<h3 name=join><b>11. JOIN</b></h3>

```sql
SELECT a.Name AS Employee_Name, a.Age AS Employee_Age, a.Designation AS Employee_Designation,
b.Address, b.salary, b.role
FROM Employee AS a
JOIN Personal_Details AS b
ON a.EID = b.EID
ORDER BY a.Name ASC, b.salary DESC;
```
