# SQL Quizes 

## Chapter 12 - Exercise 1
### Solution
```SQL
SELECT email
FROM users
	WHERE users.id=2404
```
### Answer
`ben@mgail.com`

## Chapter 14 - Exercise 2 
### Solution
```SQL
SELECT COUNT(*)
FROM users
WHERE
  users.country = 'us'
```
### Answer
`1841`

## Chapter 15 - Exercise 3 
### Solution
```SQL
SELECT COUNT(*)
FROM users
```
### Answer
`6082`


## Chapter 19 - Exercise 4 
### Solution 
```SQL
SELECT COUNT(*)
FROM users
WHERE
  signup_date < '2018-1-8'
```

### Answer
`21`

## Chapter 20 - Exercise 5 
### Solution
```SQL 
SELECT COUNT(*)
FROM users
WHERE
  signup_date < '2018-1-8'
  AND status = 'customer'
```
### Answer
`6`

## Chapter 21 - Exercise 6 
### Solution
```SQL 
SELECT COUNT(*)
FROM users
WHERE
  country='us'
  and status = 'customer'
```

### Answer
`226`

## Chapter 23 - Exercise 8 
### Solution
```SQL 
SELECT 
  COUNT(*)
FROM users
WHERE
  status = 'customer'
  AND signup_date BETWEEN '2018-01-01' AND '2018-01-31'
```

### Answer
`31`

## Chapter 29 - Exercise 9
### Solution
```SQL
SELECT 100 * COUNT(CASE WHEN status = 'customer' THEN id END) / COUNT(*) as Purchase_Rate
FROM users
WHERE
  signup_date BETWEEN '2018-01-01' AND '2018-01-07'
  and country = 'in'
```

### Answer 
`25`

## Chapter 30 - Exercise 10
### Solution
```SQL
SELECT COUNT(*)
FROM users
WHERE 
  status = 'customer'
  and country = 'in'
  and signup_date BETWEEN '2018-01-01' and '2018-01-31'
```

### Answer
`12`
## Chapter 30 - Exercise 11
### Solution
```SQL
SELECT COUNT(*)
FROM books
```
### Answer
`742`