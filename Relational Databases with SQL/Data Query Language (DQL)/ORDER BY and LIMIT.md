# The SQL ORDER BY AND LIMIT

```sql
-- Sort the products by price
SELECT * FROM Products ORDER BY Price;

-- Sort the products from highest to lowest price
SELECT * FROM Products ORDER BY Price DESC;

-- Sort the products alphabetically by ProductName
SELECT * FROM Products ORDER BY ProductName;

-- ORDER BY Several Columns
SELECT * FROM Customers ORDER BY Country, CustomerName;

-- Using Both ASC and DESC
SELECT * FROM Customers ORDER BY Country ASC, CustomerName DESC;

-- LIMIT Examples
SELECT * FROM Customers LIMIT 3;
SELECT * FROM Customers LIMIT 3 OFFSET 3;
SELECT * FROM Customers WHERE Country='Germany' LIMIT 3;
```
