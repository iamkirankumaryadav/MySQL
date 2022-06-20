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

### Numeric Conversion:

```mysql
# BIN (Binary):

# OCT Base 8 (Octal):
SELECT OCT(32742);

# HEX Base 16 (Hexadecimal):
SELECT HEX(32742);

# Convert base10 to base16:
SELECT CONV(32742, 10, 16);

# Convert base16 to base10:
SELECT CONV('7FE6', 16, 10);
```
