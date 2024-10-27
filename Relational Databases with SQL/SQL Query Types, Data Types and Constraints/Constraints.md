# SQL Constraints

- In a database table, we can add rules to a column known as constraints. These rules control the data that can be stored in a column.

|Constraint|Description|
|:---|:---|
|NOT NULL |values cannot be null|
|UNIQUE |values cannot match any older value|
|PRIMARY KEY |used to uniquely identify a row|
|FOREIGN KEY |references a row in another table|
|CHECK |validates condition for new value|
|DEFAULT |set default value if not passed|
|CREATE INDEX |used to speedup the read process|

## NOT NULL Constraint

```sql
CREATE TABLE Colleges (
  college_id INT NOT NULL,
  college_code VARCHAR(20) NOT NULL,
  college_name VARCHAR(50)
);
```

## UNIQUE Constraint

```sql
CREATE TABLE Colleges (
  college_id INT NOT NULL UNIQUE,
  college_code VARCHAR(20) UNIQUE,
  college_name VARCHAR(50)
);
```

## PRIMARY KEY Constraint

```sql
CREATE TABLE Colleges (
  college_id INT PRIMARY KEY,
  college_code VARCHAR(20) NOT NULL,
  college_name VARCHAR(50)
);
```

## FOREIGN KEY Constraint

```sql
CREATE TABLE Orders (
  order_id INT PRIMARY KEY,
  customer_id int REFERENCES Customers(id)
);
```

## CHECK Constraint

```sql
CREATE TABLE Orders (
  order_id INT PRIMARY KEY,
  amount int CHECK (amount >= 100)
);
```

## DEFAULT Constraint

```sql
CREATE TABLE College (
  college_id INT PRIMARY KEY,
  college_code VARCHAR(20),
  college_country VARCHAR(20) DEFAULT 'US'
);
```

## CREATE INDEX Constraint

```sql
-- create table
CREATE TABLE Colleges (
  college_id INT PRIMARY KEY,
  college_code VARCHAR(20) NOT NULL,
  college_name VARCHAR(50)
);

-- create index
CREATE INDEX college_index
ON Colleges(college_code);
```
