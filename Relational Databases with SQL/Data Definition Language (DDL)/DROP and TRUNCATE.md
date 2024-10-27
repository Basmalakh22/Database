# DROP and TRUNCATE in SQL

- DROP and TRUNCATE in SQL remove data from the table. The main difference between DROP and TRUNCATE commands in SQL is that DROP `removes the table or database completely`, while TRUNCATE only `removes the data, preserving the table structure`.

## What is DROP Command?

- DROP command in SQL is used to delete a whole database or a table.
- DROP statement deletes objects like an existing database, table, index, or view.

```sql
-- DROP Table
DROP TABLE Persons;

-- DROP database
DROP DATABASE Workers;
```

## What is TRUNCATE Command?

- TRUNCATE statement is a Data Definition Language (DDL) operation that is used to mark the extent of a table for deallocation (empty for reuse). The result of this operation quickly removes all data from a table, typically bypassing several integrity-enforcing mechanisms.

```sql
TRUNCATE TABLE  Student;
```

## Differences Between DROP and TRUNCATE

|DROP|TRUNCATE|
|:---|:---|
|In the drop table data and its definition is deleted with their full structure.| It preserves the structure of the table for further use exist but deletes all the data.|
|Drop is used to eliminate existing complications and fewer complications in the whole database from the table.| Truncate is used to eliminate the tuples from the table.|
|Integrity constraints get removed in the DROP command.| Integrity constraint doesn’t get removed in the Truncate command.|
|Since the structure does not exist, the View of the table does not exist in the Drop  command.|Since the structure exists, the View of the table exists in the Truncate command.|
|Drop query frees the table space complications from memory.| This query does not free the table space from memory.|
|It is slow as there are so many complications compared to the TRUNCATE command.| It is fast as compared to the DROP command as there are fewer complications.|
