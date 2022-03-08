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


