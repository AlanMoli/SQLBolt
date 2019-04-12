## SQL Review: Simple SELECT Queries
### 1. List all the Canadian cities and their populations
```SQL
SELECT City, Population 
FROM north_american_cities
WHERE Country = 'Canada';
```

### 2. Order all the cities in the United States by their latitude from north to south 
```SQL
SELECT * 
FROM north_american_cities
WHERE Country = 'United States'
ORDER BY Latitude DESC;
```

### 3. List all the cities west of Chicago, ordered from west to east 
```SQL
SELECT * 
FROM north_american_cities
WHERE Longitude < (SELECT Longitude
                   FROM north_american_cities
                   WHERE City = 'Chicago')
ORDER BY Longitude;
```

### 4. List the two largest cities in Mexico (by population)
```SQL
SELECT *
FROM north_american_cities
WHERE Country = 'Mexico'
ORDER BY Population DESC
LIMIT 2;
```

### 5. List the third and fourth largest cities (by population) in the United States and their population
```SQL
SELECT *
FROM north_american_cities
WHERE Country = 'United States'
ORDER BY Population DESC
LIMIT 2 OFFSET 2;
```