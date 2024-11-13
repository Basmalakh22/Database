# Aggregate Functions

## The SQL COUNT() Function

- The COUNT() function returns the number of rows that matches a specified criterion.

```sql
SELECT count(*) 
FROM product;
```

---

## The SQL SUM() Function

-The SUM() function returns the total sum of a numeric column.

```sql
SELECT sum(price) AS total_price
FROM order_line;
```

---

## The SQL MAX() Functions

- The MAX() function returns the largest value of the selected column.

```sql
SELECT max(order_date)
FROM cust_order;
```

---

## The SQL MIN() Functions

- The MIN() function returns the smallest value of the selected column.

```sql
SELECT min(order_date)
FROM cust_order;
```

---

## The SQL AVG() Function

- The AVG() function returns the average value of a numeric column.

```sql
SELECT avg(price)
FROM order_line;
```

---

## The SQL GROUP BY Statement

- The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country".

- The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.

```sql
SELECT customer_id
COUNT(*)
FROM cust_order
GROUP BY customer_id;
```

## Filtering

- The WHERE clause is used to filter records.
- It is used to extract only those records that fulfill a specified condition
- The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions.

```sql
SELECT customer_id
COUNT(*)
FROM cust_order
WHERE order_date > '236784'
GROUP BY customer_id
HAVING COUNT(*) > 1;
```

- [SQL Aggregate Functions: What You Need to Know](https://youtu.be/-Lw649PObq8?si=aAky1gblZ_434AeI)
