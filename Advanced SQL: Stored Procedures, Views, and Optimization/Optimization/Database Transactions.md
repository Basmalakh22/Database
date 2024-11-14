# Database Transactions

- The purpose of a transaction is to ensure that all the database operations within that transaction are treated as a single, atomic operation. This means that either all the operations within the transaction are completed successfully, or none of them are. If an error occurs during the transaction, all the changes made up to that point will be rolled back, meaning that the database will be restored to its previous state.

![Transactions](./Transactions.webp)

- BEGIN TRANSACTION: This statement begins a new transaction. Any SQL statements that follow this statement are treated as part of the transaction until the transaction is either committed or rolled back.
- COMMIT TRANSACTION: This statement saves the changes made during the transaction to the database. If the transaction completes successfully, the changes are permanent.
- ROLLBACK TRANSACTION: This statement cancels the changes made during the transaction and restores the database to its previous state.

```sql
BEGIN TRANSACTION;

-- update the orders table
UPDATE orders 
SET status = 'shipped' 
WHERE order_id = 123;

--update the inventory table
UPDATE inventory 
SET quantity = quantity - 1 
WHERE product_id = 456;

COMMIT TRANSACTION;
```

```sql
BEGIN TRANSACTION;

-- update employee salary in salaries table
UPDATE salaries
SET salary = 75000
WHERE employee_id = 123;

-- update employee information in employees table
UPDATE employees
SET last_name = 'Doe'
WHERE employee_id = 123;

-- check if both updates were successful
IF @@ROWCOUNT = 1
BEGIN
  COMMIT TRANSACTION;
  PRINT 'Employee salary and information updated successfully';
END
ELSE
BEGIN
  ROLLBACK TRANSACTION;
  PRINT 'Error: failed to update employee salary and information';
END
```
