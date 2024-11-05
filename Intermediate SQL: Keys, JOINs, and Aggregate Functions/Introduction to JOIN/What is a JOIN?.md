# What is SQL Join?

- A JOIN clause is used to `combine rows from two or more tables`, based on a related column between them.

## What are the Types of SQL Join?

- There are five main types of join : the`inner join`, which is the most common; the `left outer join`; the `right outer join` the `full outer join` and the `cross join`, also known as the `Cartesian join`.

### Inner Join

- Returns records that have matching values in both tables
![InnerJoin](./join%20image/Inner%20Join.png)

```sql
SELECT * 
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id;
```

### LEFT (OUTER) JOIN

- Returns all records from the left table, and the matched records from the right table
![LEFTJOIN](./join%20image/LEFT%20(OUTER)%20JOIN.png)

```sql
SELECT *
FROM martian
LEFT OUTER JOIN base
  ON martian.base_id = base.base_id;
```

### RIGHT (OUTER) JOIN

- Returns all records from the right table, and the matched records from the left table
![RIGHTJOIN](./join%20image/RIGHT%20(OUTER)%20JOIN.png)

```sql
SELECT *
FROM martian
RIGHT OUTER JOIN base
  ON martian.base_id = base.base_id

```

### FULL (OUTER) JOIN

- Returns all records when there is a match in either left or right table
![FULLJOIN](./join%20image/FULL%20(OUTER)%20JOIN.png)

```sql
SELECT *
FROM martian
FULL OUTER JOIN base
  ON martian.base_id = base.base_id;
```

### Cross Join

- combines every row on the left table with every row on the right table
![CrossJoin](./join%20image/Cross%20Join.png)

```sql
SELECT *
FROM martian
CROSS JOIN base;
```

---

[SQL Joins Explained |¦| Joins in SQL |¦| SQL Tutorial](https://youtu.be/9yeOJ0ZMUYw?si=crDjLLXKl3_5wRKe)

---
