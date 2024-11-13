# What is SQL Join?

- A JOIN clause is used to `combine rows from two or more tables`, based on a related column between them.

## What are the Types of SQL Join?

- There are five main types of join : the`inner join`, which is the most common; the `left outer join`; the `right outer join` the `full outer join` and the `cross join`, also known as the `Cartesian join`.

---

### Inner Join

- Returns records that have matching values in `both tables`
- INNER JOIN = matching records only

![InnerJoin](./join%20image/Inner%20Join.png)

```sql
-- Fetch the employee name and department name they belong to
SELECT e.emp_name, d.dept_name
FROM employee e
INNER JOIN department d ON e.dept_id = d.dept_id;
```

---

### LEFT (OUTER) JOIN

- Returns all records from the left table, and the matched records from the right table
- LEFT JOIN = INNER JOIN + any additional records in the left table

![LEFTJOIN](./join%20image/LEFT%20(OUTER)%20JOIN.png)

```sql
-- Fetch all the employee name and department name they belong to
SELECT e.emp_name, d.dept_name
FROM employee e
LEFT JOIN department d ON e.dept_id = d.dept_id;
```

---

### RIGHT (OUTER) JOIN

- Returns all records from the right table, and the matched records from the left table
- RIGHT JOIN = INNER JOIN + any additional records in the right table

![RIGHTJOIN](./join%20image/RIGHT%20(OUTER)%20JOIN.png)

```sql
SELECT e.emp_name, d.dept_name
FROM employee e
RIGHT JOIN department d ON e.dept_id = d.dept_id;
```

---
---
---

```sql
-- Fetch details of All employee , their manager , their department and the project they work in
SELECT e.emp_name, d.dept_name, m.manager_name, p.project_name
FROM employee e
LEFT JOIN department d ON e.dept_id = d.dept_id;
INNER JOIN manager m ON m.manager_id = e.manager_id
LEFT JOIN project p ON p.team_member_id = e.emp_id
```

---
---
---

### FULL (OUTER) JOIN

- Returns all records when there is a match in either left or right table
- FULL JOIN = INNER JOIN + any remaining records in the right table + any remaining records in the left table

![FULLJOIN](./join%20image/FULL%20(OUTER)%20JOIN.png)

```sql
SELECT e.emp_name, d.dept_name
FROM employee e
FULL JOIN department d ON e.dept_id = d.dept_id;
```

---

### Cross Join

- combines every row on the left table with every row on the right table
- returns cartesian product

![CrossJoin](./join%20image/Cross%20Join.png)

```sql
SELECT e.emp_name, d.dept_name
FROM employee e
CROSS JOIN department d;
```

---
---
---

```sql
-- write query to fetch employee name and their corresponding department name
-- also make sure to display the company name and company location corresponding to each employee 
SELECT e.emp_name, d.dept_name, c.company_name, c.company_location
FROM employee e
INNER JOIN department d ON e.dept_id = d.dept_id
CROSS JOIN company c;
```

---
---
---

## NATURAL Join

- A natural join in SQL combines rows from two or more tables based on the common column(s) between them. The common columns on which the tables are joined must have the same name and data type across the tables. The SQL database performs the join based on these naturally matching columns when a natural join is used.

- A natural join is a type of equijoin, which means it works by matching equal values in common columns. Unlike other joins, we do not need to explicitly specify the column for joining, as SQL automatically takes care of finding the common column names and data types and joins the data.

![NATURALJoin](./join%20image/sql_natural_join.png)

```sql
SELECT e.emp_name, d.dept_name
FROM employee e
NATURAL JOIN department d
ALTER TABLE department RENAME COLUMN dept.id To id;
```

---

## SELF Join

- A self join is a regular join, but the table is joined with itself.

![SELFJoin](./join%20image/sql_self_join.png)

```sql
-- write a query to fetch the child name and their age corresponding to their parent name and parent age
SELECT child.name AS child_name,
child.age AS child_age,
parent.name AS parent_name
parent.age AS parent_age
FROM family as child
SELF JOIN family as parent ON child.parent_id = parent.member_id;
```

---

- [SQL Joins Explained |¦| Joins in SQL |¦| SQL Tutorial](https://youtu.be/9yeOJ0ZMUYw?si=crDjLLXKl3_5wRKe)

- [SQL JOINS Tutorial for beginners | Practice SQL Queries using JOINS - Part 1](https://youtu.be/0OQJDd3QqQM?si=mmWAGVO5Ao7bT8e4)

- [SQL JOINS Tutorial for beginners | Practice SQL Queries using JOINS - Part 2](https://youtu.be/RehbnzKHS28?si=2OyJDOlkqDZkY9Fh)

---
