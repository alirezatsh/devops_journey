# MongoDB Basic Commands

This file contains basic MongoDB commands for managing databases, collections, and documents.



## Connect to mongodb

Connect to MongoDB server and databases

```bash

mongosh -u <username> -p <password> --host <host>
mongosh "mongodb://user:password@ip:port"   
docker exec -it mongo-container-name mongosh -u root -p 1234


```

## Manage database

Create, drop, and switch databases

```bash

show dbs
db
db.dropDatabase()
db.copyDatabase("oldDB", "newDB")
use databasename
db.createUser({user:"user1", pwd:"pass", roles:["readWrite"]})
db.dropUser("user1")
db.stats()

```

## Manage collection

Create, drop, index, and list collections

```bash

show collections
db.createCollection("users")
db.users.drop()
db.users.createIndex({name:1})
db.users.getIndexes()
db.users.listIndexes()
db.users.countDocuments()

```

## Manage document

Insert, update, delete, query documents

```bash

db.users.insertOne({name: "name", age: age})
db.users.insertMany([
  {name: "name1", age: age1},
  {name: "name2", age: age2}
])
db.users.find()
db.users.find().pretty()
db.users.find({age: 25})
db.users.find({name: /^A/})
db.users.updateOne({name: "Alireza"}, {$set: {age: 26}})
db.users.updateMany({age: {$lt: 30}}, {$set: {status: "young"}})
db.users.deleteOne({name: "Alireza"})
db.users.deleteMany({age: {$lt: 25}})
db.users.find().limit(5)
db.users.find().sort({age: -1})

