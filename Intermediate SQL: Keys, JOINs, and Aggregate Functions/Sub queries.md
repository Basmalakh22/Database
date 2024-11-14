# Sub queries

- Subqueries (also known as inner queries or nested queries) are a tool for performing operations in multiple steps.

```sql
SELECT first_name, last_name, hourly_pay, 
    (SELECT AVG(hourly_pay) FROM employees) AS avg_pay
FROM employees;
```

```sql
SELECT first_name, last_name
FROM customers
WHERE customer_id IN 
(SELECT DISTINCT customer_id FROM transactions WHERE customer_id IS NOT NULL);
```

- [MySQL: SUBQUERIES](https://youtu.be/i5acg3Hvu6g?si=ocgG4OfMSd8imgmx)
