# CRUD Operations

![CRUD Operations](./image/CRUD%20Operations.png)

- The create operation is used to insert new documents in the MongoDB database.
- The read operation is used to query a document in the database.
- The update operation is used to modify existing documents in the database.
- The delete operation is used to remove documents from the database.

## How to perform CRUD operations

![CRUD Operations](./image/CRUD%20Operation2.png)

### Create operation

- db.collection.insertOne()
- db.collection.insertMany()

```json
db.RecordsDB.insertOne({
    name: "Marsh",
    age: "6 years",
    species: "Dog",
    ownerAddress: "380 W. Fir Ave",
    chipped: true
})
```

```json
db.RecordsDB.insertMany([{
    name: "Marsh",
    age: "6 years",
    species: "Dog",
    ownerAddress: "380 W. Fir Ave",
    chipped: true},
      {name: "Kitana", 
      age: "4 years", 
      species: "Cat", 
      ownerAddress: "521 E. Cortland", 
      chipped: true}])
```

### Read operations

- db.collection.find()
- db.collection.findOne()

### Update operations

- db.collection.updateOne()
- db.collection.updateMany()
- db.collection.replaceOne()

### Delete operations

- db.collection.deleteOne()
- db.collection.deleteMany()
