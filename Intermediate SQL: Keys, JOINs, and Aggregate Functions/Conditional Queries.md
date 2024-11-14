# Conditional Queries

## The SQL CASE Expression

- CASE WHEN statements evaluate conditions and return a result.
- Similar to if then else statement

```sql
SELECT temperature,
CASE
    WHEN temperature > 65 THEN 'shirt'
    WHEN temperature < 40 THEN 'jacket'
    ELSE 'sweater' END AS clothing
END
FROM daily_weather;
```

- In Case you need to aggregate
  - categorizing data
  - filter your data
  - aggregate data based on the result of a logical test

```sql
SELECT season,
COUNT (CASE
    WHEN home_team_id = 8650 AND
    home_goal > away_goal 
    THEN id END) AS home_wins
FROM match
GROUP BY season;
```

```sql
SELECT season,
COUNT (CASE WHEN home_team_id = 8650 AND home_goal > away_goal 
    THEN id END) AS home_wins,
COUNT (CASE WHEN away_team_id = 8650 AND away_goal > home_goal 
    THEN id END) AS away_wins,
FROM match
GROUP BY season;
```

---

## MySQL IF() Function

- The IF() function returns a value if a condition is TRUE, or another value if a condition is FALSE.

```sql
-- Syntax => IF(condition, value_if_true, value_if_false)

-- Return "MORE" if the condition is TRUE, or "LESS" if the condition is FALSE
SELECT OrderID, Quantity, 
IF(Quantity > 10, "MORE", "LESS")
FROM OrderDetails;
```

---

- [CASE WHEN Statements (SQL) - Conditional Logic (If Then)](https://youtu.be/YoXAPtZOMZk?si=AJrIHCcS6He59tj_)
- [SQL Tutorial: CASE WHEN with aggregate functions](https://youtu.be/ImiEKaEBvjE?si=UqmSGAxi7zF9NciW)
- [How to Use IF and CASE WHEN in MySQL Workbench SQL Tutorial](https://youtu.be/yVEtVbkkVcc?si=eiYhg_UYaAyR_HR5)
