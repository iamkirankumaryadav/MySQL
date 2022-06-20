# `String` Functions

### `_`: Single Character Wildcard.
### `%`: Multi Character Wildcard.

```mysql
# Select all the Names with second character as 'a':
SELECT Name 
FROM Country
WHERE Name LIKE '_a%' 
ORDER BY Name;

# Select all country names ending with y using Regular Expression:
SELECT Name
FROM Country
WHERE Name RLIKE 'y$' 
ORDER BY Name;
```      

### String Concatenation:

```mysql
SELECT 'Kirankumar' || ' ' || 'Yadav' AS Name;

SELECT CONCAT('Kirankumar', ' ', 'Yadav') AS Name;
```

### Numeric Conversion:

```mysql
# BIN (Binary):
SELECT BIN(32742)

# OCT Base 8 (Octal):
SELECT OCT(32742);

# HEX Base 16 (Hexadecimal):
SELECT HEX(32742);

# Convert base10 to base16:
SELECT CONV(32742, 10, 16);

# Convert base16 to base10:
SELECT CONV('7FE6', 16, 10);
```

### Trimming and Padding:

```mysql
# TRIM(): Remove whitespace from the leading and trailing ends.
SELECT TRIM(' Kirankumar      ') AS Name;

SELECT * 
FROM Customer
WHERE Name Like TRIM('  Bill Smith ');

SELECT CONCAT(TRIM('x' FROM 'xxxKirankumarxxx'), ' ', TRIM('x' FROM 'xxxYadavxxx')) AS Name;

# PAD(): Add characters at end:
SELECT RPAD('Kirankumar', 15, '.') AS Name;
# e.g. Kirankumar.....
```

### Case Conversion:

```mysql
# Uppercase:
SELECT UPPER(Name) FROM Employee;
SELECT UCASE(Name) FROM Employee;

# Lowercase:
SELECT LOWER(Name) FROM Employee;
SELECT LCASE(Name) FROM Employee;
```

### Substring:

```mysql
SELECT SUBSTRING('Kirankumar Yadav, 12') AS Last_Name;
SELECT SUBSTR('Kirankumar Yadav', 12) AS Last_Name;

# All the characters till first delimiter:
SELECT SUBSTRING_INDEX('My Name is Kirankumar', ' ', 1)
# e.g. My

# String after last delimiter:
SELECT SUBSTRING_INDEX('My Name is Kirankumar', ' ', -1)
# e.g. Kirankumar
```

### SOUNDEX: Find similar sounding words.

```mysql
SELECT SOUNDEX('Bill'), SOUNDEX('Bell');
SELECT SOUNDEX('Ache'), SOUNDEX('Ack');
```

