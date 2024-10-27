# The SQL SELECT Statement

- The SELECT DISTINCT statement is used to return only distinct (different) values.

```sql
-- SELECT ALL
SELECT * FROM Persons;

SELECT LastName, City FROM Persons;

SELECT DISTINCT City FROM Persons;

SELECT PersonID AS ID FROM Persons;

SELECT COUNT(DISTINCT City) FROM Persons;

SELECT Count(*) AS DistinctCities FROM (SELECT DISTINCT City FROM Persons);
```
