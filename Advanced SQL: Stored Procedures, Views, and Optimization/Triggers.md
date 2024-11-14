# Triggers

- In SQL, a trigger is a database object containing SQL logic that is automatically executed when a specific database event occurs. In other words, a database trigger is "triggered" by a particular event.
- Trigger = when an event happens,do something ex.(INSERT, UPDATE, or DELETE ) checks data ,handle errors ,auditing tables

- Types of SQL Triggers
  - Row-level triggers
  - Statement-level triggers

- Row-Level Triggers
  - A row-level trigger is executed once for each row affected by the triggering event, which is typically an INSERT, UPDATE, or DELETE statement.

- Statement-Level Triggers
  - A statement-level trigger is executed once for the entire triggering event, instead of once for each row affected by the event. Statement-level triggers are useful to perform an action based on the overall effect of an INSERT, UPDATE, or DELETE statement, rather than on individual rows.

```sql
CREATE TRIGGER before_hourly_pay_update
BEFORE UPDATE ON employees 
FOR EACH ROW
SET NEW.salary = (NEW.hourly_pay * 2080);
```

```sql
CREATE TRIGGER before_hourly_pay_insert
BEFORE INSERT ON employees 
FOR EACH ROW
SET NEW.salary = (NEW.hourly_pay * 2080);
```

```sql
CREATE TRIGGER after_salary_delete
AFTER DELETE ON employees 
FOR EACH ROW
UPDATE expenses
SET expense_total = expense_total - OLD.salary
WHERE expense_name = "salaries";
```

```sql
CREATE TRIGGER after_salary_insert
AFTER INSERT ON employees 
FOR EACH ROW
UPDATE expenses
SET expense_total = expense_total + NEW.salary
WHERE expense_name = "salaries";

```

```sql
CREATE TRIGGER after_salary_update
AFTER UPDATE ON employees 
FOR EACH ROW
UPDATE expenses
SET expense_total = expense_total + (NEW.salary - OLD.salary)
WHERE expense_name = "salaries";
```

- [MySQL: TRIGGERS](https://youtu.be/jVbj72YO-8s?si=_NwWPZMHp5yca2eo)
