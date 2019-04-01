## SQL Lesson 3: Queries with constraints (Pt. 2)
### 1. Find all the Toy Story movies
```SQL
SELECT * 
FROM movies
WHERE Title LIKE 'Toy Story%';
```

### 2. Find all the movies directed by John Lasseter
```SQL
SELECT * 
FROM movies
WHERE Director = 'John Lasseter';
```

### 3. Find all the movies (and director) not directed by John Lasseter
```SQL
SELECT * 
FROM movies
WHERE Director != 'John Lasseter';
```

### 4. Find all the WALL-* movies
```SQL
SELECT * 
FROM movies
WHERE Title LIKE 'WALL-%';
```