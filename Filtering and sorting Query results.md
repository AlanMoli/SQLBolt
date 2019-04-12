## SQL Lesson 4: Filtering and sorting Query results
### 1. List all directors of Pixar movies (alphabetically), without duplicates
```SQL
SELECT DISTINCT Director 
FROM movies
ORDER BY Director;
```

### 2. List the last four Pixar movies released (ordered from most recent to least)
```SQL
SELECT * 
FROM movies
ORDER BY YEAR DESC
LIMIT 4;
```

### 3. List the first five Pixar movies sorted alphabetically
```SQL
SELECT * 
FROM movies
ORDER BY Title
LIMIT 5;
```

### 4. List the next five Pixar movies sorted alphabetically 
```SQL
SELECT * 
FROM movies
ORDER BY Title
LIMIT 5 OFFSET 5;
```