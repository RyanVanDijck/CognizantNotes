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

Find the Youngest German user:
```SQL
SELECT 
  MIN(age)
FROM users
WHERE
  country = 'de'
```

## Comparison
Find number of users who signed up after 1st January 2018:
```SQL
SELECT COUNT(*)
FROM users
WHERE
  signup_date > '2018-01-01'
```

Find number of users who signed up on or after 1st January 2018:
```SQL
SELECT COUNT(*)
FROM users
WHERE
  signup_date >= '2018-01-01'
```

## Combining Filters 

Find the number of users from the US who signed up on or after 1st January 2018:
```SQL
SELECT COUNT(*)
FROM users
WHERE
  country = 'us'
  AND signup_date >= '2018-01-01'
```

Find the number of customers  from the US who signed up on or after 1st January 2018:
```SQL
SELECT COUNT(*)
FROM users
WHERE
  country = 'us'
  AND signup_date >= '2018-01-01'
  AND status = 'customer'
```

## Ranges 
Find the number of signups between the 1st of January and the 7th of January inclusively:
```SQL
SELECT COUNT(*)
FROM users
WHERE
  signup_date BETWEEN '2018-01-01' AND '2018-01-07'
```

## Aliases
Change the name of the created_at field to signup_timestamp in the query result:
```SQL
SELECT
  id,
  signup_date,
  created_at AS signup_timestamp
FROM users
```


## Case Statement
Case statement template:
```SQL
CASE
  WHEN condition_1 THEN result_1
  WHEN condition_2 THEN result_2
  WHEN condition_n THEN result_n
  ELSE default_result
END
```

Segregate ages into age groups:
```SQL
SELECT 
  CASE 
    WHEN age <= 16 THEN 'youth'
    WHEN age BETWEEN 17 AND 25 THEN 'young_adult'
    WHEN age BETWEEN 26 AND 35 THEN 'adult'
    WHEN age BETWEEN 36 AND 45 THEN 'middle_aged'
    ELSE 'aged'
  END AS age_group,
  *
FROM users
```

Show total users and total customers between date range:

```SQL
SELECT
  COUNT(*) AS total_users_count,
  COUNT(CASE WHEN status = 'customer' THEN id END) AS total_customers_count
FROM users
WHERE
  signup_date BETWEEN '2018-01-01' AND '2018-01-07'
```

Calculate purchase rate:
```SQL
SELECT
  100 * COUNT(CASE WHEN status = 'customer' THEN id END) / COUNT(*) AS purchase_rate
FROM users
WHERE
  signup_date BETWEEN '2018-01-01' AND '2018-01-07'
```
More precise purchase rate(using float):
```SQL
SELECT
  100.0 * COUNT(CASE WHEN status = 'customer' THEN id END) / COUNT(*) AS purchase_rate,
  COUNT(CASE WHEN status = 'customer' THEN id END) AS customers_count
FROM users
WHERE
  signup_date BETWEEN '2018-01-01' AND '2018-01-07'
```

## Subqueries

Basic Subquery:

```SQL
SELECT *
FROM (
  SELECT *
  FROM users
  WHERE
    country = 'us'
) us_users
```

Basic Subquery using `as` keyword for readability

```SQL
WITH us_users AS (
  SELECT *
  FROM users
  WHERE
    country = 'us'
), us_customers AS (
  SELECT *
  FROM us_users
  WHERE 
    status = 'customer'
)

SELECT 
  COUNT(*)
FROM us_customers
```

## Relational Model 

There are 3 types of relations in SQL:

*   one to one (a country has one capital, a book has one publisher, etc)
*   one to many (a user has many purchases)
*   many to many (users have many books)

### One to many
* A foreign key is often used to point to a single item. 
* That item can have more than one things pointing at it. 
* For example: A customer can have multiple purchases. 

### One to one
* Foreign Key also used.
* Only one associated record.
* Often used to break down big tables.

### Many to Many 
* When many items can have many things pointing at it, and vice versa. 
* For example, a user can have many books, and a book can have many users. 
* A join table is often used with foreign keys to primary keys to the two other tables.

### Relational Diagrams
#### One to One 
![Diagram of One to One relationship](./OneToOne.png)

#### One to Many
![Diagram of One to Many relationship](./OneToMany.png)

#### Many to Many 
![Diagram of Many to Many relationship](./ManyToMany.png)

