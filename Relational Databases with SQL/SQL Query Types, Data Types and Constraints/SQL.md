# What is SQL (Structured Query Language)?

## What is SQL?

- Structured query language (SQL) is a programming language for storing and processing information in a relational database. A relational database stores information in tabular form, with rows and columns representing different data attributes and the various relationships between the data values. You can use SQL statements to store, update, remove, search, and retrieve information from the database. You can also use SQL to maintain and optimize database performance.

## What are the components of a SQL system?

- Relational database management systems use structured query language (SQL) to store and manage data. The system stores multiple database tables that relate to each other. MS SQL Server, MySQL, or MS Access are examples of relational database management systems. The following are the components of such a system.
  - SQL table:
A SQL table is the basic element of a relational database. The SQL database table consists of rows and columns. Database engineers create relationships between multiple database tables to optimize data storage space.

  - SQL statements:
SQL statements, or SQL queries, are valid instructions that relational database management systems understand. Software developers build SQL statements by using different SQL language elements. SQL language elements are components such as identifiers, variables, and search conditions that form a correct SQL statement.

  - Stored procedures:
Stored procedures are a collection of one or more SQL statements stored in the relational database. Software developers use stored procedures to improve efficiency and performance. For example, they can create a stored procedure for updating sales tables instead of writing the same SQL statement in different applications.

## What are SQL commands?

- Structured query language (SQL) commands are specific keywords or SQL statements that developers use to manipulate the data stored in a relational database. You can categorize SQL commands as follows.

  - Data definition language:
Data definition language (DDL) refers to SQL commands that design the database structure. Database engineers use DDL to create and modify database objects based on the business requirements. For example, the database engineer uses the CREATE command to create database objects such as tables, views, and indexes.

  - Data query language:
Data query language (DQL) consists of instructions for retrieving data stored in relational databases. Software applications use the `SELECT command` to filter and return specific results from a SQL table.

  - Data manipulation language:
Data manipulation language (DML) statements write new information or modify existing records in a relational database. For example, an application uses the `INSERT command` to store a new record in the database.

  - Data control language:
Database administrators use data control language (DCL) to manage or authorize database access for other users. For example, they can use the `GRANT command` to permit certain applications to manipulate one or more tables.

  - Transaction control language:
The relational engine uses transaction control language (TCL) to automatically make database changes. For example, the database uses the `ROLLBACK command` to undo an erroneous transaction.

## What is SQL injection?

- SQL injection is a `cyberattack` that involves tricking the database with SQL queries. Hackers use SQL injection to retrieve, modify, or corrupt data in a SQL database. For example, they might fill in a SQL query instead of a person's name in a submission form to carry out a SQL injection attack.

## What is MySQL?

- MySQL is an open-source relational database management system offered by Oracle. Developers can download and use MySQL without paying a licensing fee. They can install MySQL on different operating systems or cloud servers. MySQL is a popular database system for web applications.

  - SQL vs. MySQL
    - Structured query language (SQL) is a standard language for database creation and manipulation. MySQL is a relational database program that uses SQL queries. While SQL commands are defined by international standards, the MySQL software undergoes continual upgrades and improvements.

## What is NoSQL?

- NoSQL refers to non-relational databases that don't use tables to store data. Developers store information in different types of NoSQL databases, including graphs, documents, and key-values. NoSQL databases are popular for modern applications because they are horizontally scalable. Horizontal scaling means increasing the processing power by adding more computers that run NoSQL software.

  - SQL vs. NoSQL
    - Structured query language (SQL) provides a uniform data manipulation language, but NoSQL implementation is dependent on different technologies. Developers use SQL for transactional and analytical applications, whereas NoSQL is suitable for responsive, heavy-usage applications.
