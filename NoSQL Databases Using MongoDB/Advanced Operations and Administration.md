# Advanced Operations and Administration

- [MongoDB sorting and limiting explained](https://youtu.be/3mV2KMzNxLE?si=YVJ775Cvsc90Xpj8)
  - db.students.find()
  - db.students.find().sort({name: 1})
  - db.students.find().sort({name: -1})
  - db.students.find().sort({gpa: 1})
  - db.students.find().sort({gpa: -1})
  - db.students.find().limit(1) => return 1 decument
  - db.students.find().limit(3)
  - db.students.find().sort({gpa: -1}).limit(1)
  - db.students.find().sort({gpa: -1}).limit(3)

- [MongoDB indexes explained](https://youtu.be/ZoxmVjc4Xdg?si=5_5KnwqSFnUmhJyM)
  - db.students.createIndex({name: 1})
  - db.students.getIndexes()
  - db.students.dropIndex("name_1")
