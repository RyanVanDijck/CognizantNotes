# SQL
## Basics
Find all information about all users:
```SQL
SELECT * 
FROM USERS
```

Find specific information about users:
```SQL
SELECT
  email,
  signup_date,
  created_at
FROM users
```

Add a comment to SQL:
```SQL
-- This is a comment
SELECT *
FROM users
```

## Sorting
Sort Users by signup date in descending order:
```SQL
SELECT *
FROM users
ORDER BY signup_date DESC
```

Sort users by first name in ascending order:
```SQL
SELECT *
FROM users
ORDER BY first_name ASC
```

Sort with country and then with signup date:
```SQL
SELECT *
FROM users
ORDER BY country ASC, signup_date DESC
```

## Limiting
Find the first five records of users:
```SQL
SELECT *
FROM users
LIMIT 5
```

Find the five latest orders: 
```SQL
SELECT *
FROM users
ORDER BY created_at DESC
LIMIT 5
```

## Filtering
Filter for German users:
```SQL
SELECT *
FROM users
WHERE
  country = 'de'
```

## Aggregate functions
These give us a single value from multiple rows of data. 
<br>
Count German Users:
```SQL
SELECT 
  COUNT(*)
FROM users
WHERE
  country = 'de'
```

Find the Youngest German user
```SQL
SELECT 
  MIN(age)
FROM users
WHERE
  country = 'de'
```
