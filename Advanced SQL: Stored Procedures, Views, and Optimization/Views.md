# Views

- view is a virtual table based on the result-set of an SQL statement.
- A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database.
- You can add SQL statements and functions to a view and present the data as if the data were coming from one single table.

```sql
CREATE VIEW full_emps_depts AS 
SELECT c.emp_no ,first_name ,last_name ,gender ,hire_date ,dept_name
FROM employees e
JOIN current_dept_emp c ON e.emp_no = c.emp_no
JOIN department d ON c.dept_no = d.dept_no
```

- [SQL Views In 4 Minutes: Super Useful! Wow! Crazy! Amazing! I'm Crying Tears Of SQL Joy.](https://youtu.be/vLLkNI-vkV8?si=BtV6weiJ-UTJPzlT)
- [SQL VIEWS + Complex Queries, Cross Joins, Unions, and more! |¦| SQL Tutorial](https://youtu.be/8jU8SrAPn9c?si=Y7-0vczN99IVDkGP)
