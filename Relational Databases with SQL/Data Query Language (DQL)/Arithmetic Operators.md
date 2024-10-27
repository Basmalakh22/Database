# Arithmetic Operators

```sql
--  addition of 2 columns
SELECT employee_id, employee_name, salary, salary + employee_id
   AS "salary + employee_id" FROM addition;

-- subtraction of 2 columns
SELECT employee_id, employee_name, salary, salary - employee_id
    AS "salary - employee_id" FROM subtraction;

-- multiplication of 2 columns:
SELECT employee_id, employee_name, salary, salary * employee_id
     AS "salary * employee_id" FROM addition;

-- modulus operation between 2 columns:
SELECT employee_id, employee_name, salary, salary % employee_id
    AS "salary % employee_id" FROM addition;

```
