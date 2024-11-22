# Basic Operations and Data Modeling

- [MongoDB Schema Design Best Practices](https://youtu.be/QAqK-R9HUhc?si=ZV3a2FuvSfvfqDCe)

## Create Database

- MongoDB `use DATABASE_NAME` is used to create database.
  - use mydb
- To check your currently selected database, use the command `db`.
- If you want to check your databases list, use the command `show dbs`.

## Drop Database

- MongoDB `db.dropDatabase()` command is used to drop a existing database.

## Create Collection

- MongoDB `db.createCollection(name, options)` is used to create collection.

```json
 db.createCollection("mycol", { capped : true, autoIndexID : true, size : 6142800, max : 10000 } ){
"ok" : 0,
"errmsg" : "BSON field 'create.autoIndexID' is an unknown field.",
"code" : 40415,
"codeName" : "Location40415"
}
```

## Drop Collection

- MongoDB's `db.collection.drop()` is used to drop a collection from the database.
  - db.mycollection.drop()

## Datatypes

- String − This is the most commonly used datatype to store the data. String in MongoDB must be UTF-8 valid.

- Integer − This type is used to store a numerical value. Integer can be 32 bit or 64 bit depending upon your server.

- Boolean − This type is used to store a boolean (true/ false) value.

- Double − This type is used to store floating point values.

- Min/ Max keys − This type is used to compare a value against the lowest and highest BSON elements.

- Arrays − This type is used to store arrays or list or multiple values into one key.

- Timestamp − ctimestamp. This can be handy for recording when a document has been modified or added.

- Object − This datatype is used for embedded documents.

- Null − This type is used to store a Null value.

- Symbol − This datatype is used identically to a string; however, it's generally reserved for languages that use a specific symbol type.

- Date − This datatype is used to store the current date or time in UNIX time format. You can specify your own date time by creating object of Date and passing day, month, year into it.

- Object ID − This datatype is used to store the document’s ID.

- Binary data − This datatype is used to store binary data.

- Code − This datatype is used to store JavaScript code into the document.

- Regular expression − This datatype is used to store regular expression.
