# The SQL UPDATE AND DELETE Statement

## The SQL UPDATE Statement

- The UPDATE statement is used to modify the existing records in a table.

```sql
UPDATE Persons
SET LastName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE PersonID = 1;
```

## The SQL DELETE Statement

- The DELETE statement is used to delete existing records in a table.

```sql
DELETE FROM Persons WHERE PersonID = 1;
```
