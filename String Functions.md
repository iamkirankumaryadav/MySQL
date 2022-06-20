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
