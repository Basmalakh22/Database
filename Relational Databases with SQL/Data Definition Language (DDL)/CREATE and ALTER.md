# The SQL CREATE AND ALTER TABLE Statement

## The SQL CREATE TABLE Statement

```sql
CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);
```

## SQL ALTER TABLE Statement

- The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

- The ALTER TABLE statement is also used to add and drop various constraints on an existing table.

```sql
-- ALTER TABLE - ADD Column
ALTER TABLE Persons
ADD Email varchar(255);

-- ALTER TABLE - DROP COLUMN
ALTER TABLE Persons
DROP COLUMN Email;

-- ALTER TABLE - RENAME COLUMN
ALTER TABLE Persons
RENAME COLUMN Persons to Customers;
```
