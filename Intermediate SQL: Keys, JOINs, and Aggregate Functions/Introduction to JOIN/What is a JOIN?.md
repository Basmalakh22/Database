# What is SQL Join?

- A JOIN clause is used to `combine rows from two or more tables`, based on a related column between them.

## What are the Types of SQL Join?

- There are five main types of join : the`inner join`, which is the most common; the `left outer join`; the `right outer join` the `full outer join` and the `cross join`, also known as the `Cartesian join`.

### Inner Join

- Returns records that have matching values in both tables
![InnerJoin](./Inner%20Join.png)

```sql
SELECT * 
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id;
```

### LEFT (OUTER) JOIN

- Returns all records from the left table, and the matched records from the right table
![LEFTJOIN](./LEFT%20(OUTER)%20JOIN.png)

### RIGHT (OUTER) JOIN

- Returns all records from the right table, and the matched records from the left table
![RIGHTJOIN](./RIGHT%20(OUTER)%20JOIN.png)

### FULL (OUTER) JOIN

- Returns all records when there is a match in either left or right table
![FULLJOIN](./FULL%20(OUTER)%20JOIN.png)

### Cross Join

- combines every row on the left table with every row on the right table
![CrossJoin](./Cross%20Join.png)

[SQL Joins Explained |¦| Joins in SQL |¦| SQL Tutorial](https://youtu.be/9yeOJ0ZMUYw?si=crDjLLXKl3_5wRKe)
