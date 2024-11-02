# primary key

- A primary key, also called a primary keyword, is a column in a relational database table that's distinctive for each record. It's a `unique identifier`, such as a driver's license number, telephone number with area code or vehicle identification number (VIN). A relational database must `have only one primary key`. Every row of data must have a primary key value and `none of the rows can be null`.

```sql
CREATE TABLE transactions (
    transaction_id INT PRIMARY KEY,
    amount DECIMAL(5, 2)
);
```

```sql
ALTER TABLE transactions
ADD CONSTRAINT
PRIMARY KEY (transaction_id);
```

```sql
ALTER TABLE transactions
DROP CONSTRAINT transaction_id;
```

[MySQL: PRIMARY KEYS](https://youtu.be/620DzFVz41o?si=Qsp_t5vWMBhUeJNq)
