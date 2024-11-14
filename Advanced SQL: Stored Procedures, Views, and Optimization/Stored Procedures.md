# Stored Procedures

- A stored procedure in SQL is a group of SQL queries that can be saved and `reused multiple times`. It is very useful as it reduces the need for rewriting SQL queries. It enhances efficiency, reusability, and security in database management.
- Users can also pass parameters to stored procedures so that the stored procedure can act on the passed parameter values.
- Stored Procedures are created to perform one or more DML operations on the Database.

```sql
CREATE PROCEDURE large_salaries()
SELECT * 
FROM employee_salary
WHERE salary >= 50000;
```

```sql
DELIMITER $$
CREATE PROCEDURE large_salaries2()
BEGIN
   SELECT * 
   FROM employee_salary
   WHERE salary >= 50000;
   SELECT * 
   FROM employee_salary
   WHERE salary >= 10000;
END
DELIMITER $$;
```

- [Stored Procedures in MySQL | Advanced MySQL Series](https://youtu.be/7vnxpcqmqNQ?si=nqI8TVcalu8wYQLG)
