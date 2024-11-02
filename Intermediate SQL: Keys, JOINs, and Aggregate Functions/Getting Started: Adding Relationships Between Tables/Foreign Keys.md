# FOREIGN KEYS

- Foreign keys link data in one table to the data in another table.foreign key column in a table points to a column with unique values in another table (often the primary key column) to create a way of cross-referencing the two tables.

```sql
CREATE TABLE customers (
    customer_id INT PRIMARY KEY AUTO_INCREMENT,
     first_name VARCHAR(50),
     last_name VARCHAR(50)
);
```

```sql
-- Add a named foreign key constraint to a new table
CREATE TABLE transactions (
    transaction_id INT PRIMARY KEY,
    amount DECIMAL(5, 2)
    customer_id INT,
    FOREIGN KEY(customer_id)REFERENCES customers(customer_id),
);
```

```sql
-- Add a named foreign key constraint to an existing table
ALTER TABLE customers
ADD CONSTRAINT fk_customer_id
FOREIGN KEY (customer_id) REFERENCES customers(customer_id);

```

```sql
ALTER TABLE transactions
AUTO_INCREMENT = 1000;
```

[MySQL: FOREIGN KEYS](https://youtu.be/rFssfx37UJw?si=30KSG_VvFoBRDZwC)
