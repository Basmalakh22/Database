# Logical Operators (AND, OR, NOT, BETWEEN, IN, NOT IN, LIKE)

```sql
-- Select all customers from Spain that starts with the letter 'G'
SELECT * FROM Customers WHERE Country = 'Spain' AND CustomerName LIKE 'G%';

-- All Conditions Must Be True
SELECT * FROM Customers WHERE Country = 'Germany' AND City = 'Berlin' AND PostalCode > 12000;

-- Select all customers from Germany or Spain:
SELECT * FROM Customers WHERE Country = 'Germany' OR Country = 'Spain';

-- At Least One Condition Must Be True
SELECT * FROM Customers WHERE City = 'Berlin' OR CustomerName LIKE 'G%' OR Country = 'Norway';

-- Select all Spanish customers that starts with either "G" or "R"
SELECT * FROM Customers WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');

-- Select only the customers that are NOT from Spain
SELECT * FROM Customers WHERE NOT Country = 'Spain';

--  Select customers that does not start with the letter 'A'
SELECT * FROM Customers WHERE CustomerName NOT LIKE 'A%';

-- NOT BETWEEN
SELECT * FROM Customers WHERE CustomerID NOT BETWEEN 10 AND 60;

-- NOT IN
SELECT * FROM Customers WHERE City NOT IN ('Paris', 'London');

-- NOT Greater Than
SELECT * FROM Customers WHERE NOT CustomerID > 50;

-- NOT Less Than
SELECT * FROM Customers WHERE NOT CustomerId < 50;

-- Selects all products with a price between 10 and 20
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20;

-- BETWEEN with IN
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20 AND CategoryID IN (1,2,3);

-- BETWEEN Text Values
SELECT * FROM Products WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;

-- BETWEEN Dates
SELECT * FROM Orders WHERE OrderDate BETWEEN #07/01/1996# AND #07/31/1996#;

-- IN Operator
SELECT * FROM Customers WHERE Country IN ('Germany', 'France', 'UK');

-- NOT IN
SELECT * FROM Customers WHERE Country NOT IN ('Germany', 'France', 'UK');

-- IN (SELECT)
SELECT * FROM Customers WHERE CustomerID IN (SELECT CustomerID FROM Orders);

-- Select all customers that starts with the letter "a"
SELECT * FROM Customers WHERE CustomerName LIKE 'a%';

-- Return all customers from a city that contains the letter 'L'
SELECT * FROM Customers WHERE city LIKE '%L%';

-- Return all customers that starts with 'La'
SELECT * FROM Customers WHERE CustomerName LIKE 'La%';

-- Return all customers that starts with 'a' or starts with 'b'
SELECT * FROM Customers WHERE CustomerName LIKE 'a%' OR CustomerName LIKE 'b%';

-- Return all customers that ends with 'a'
SELECT * FROM Customers WHERE CustomerName LIKE '%a';

-- Return all customers that starts with "b" and ends with "s"
SELECT * FROM Customers WHERE CustomerName LIKE 'b%s';

-- Return all customers that contains the phrase 'or'
SELECT * FROM Customers WHERE CustomerName LIKE '%or%';

-- Return all customers that starts with "a" and are at least 3 characters in length
SELECT * FROM Customers WHERE CustomerName LIKE 'a__%';

-- Return all customers from Spain
SELECT * FROM Customers WHERE Country LIKE 'Spain';
```
