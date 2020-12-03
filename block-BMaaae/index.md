writeCode

Write code to:-

- create a database named `sports`.
 - use sports
- list all databases present in local mongod server.
 - show dbs
- create 3 collections named `cricket`, `football`, `TT` in sports databse.
 - db.createCollection('cricket')
 - db.createCollection('football')
 - db.createCollection('TT')
- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
 -  db.cricket.insertMany([{"name": "Elliot Alderson", "age": 27, "email": "ea@protonmail.com", "bid_price": 300},{"name": "Darlene Alderson", "age": 23, "email": "da@protonmail.com", "bid_price": 123},{"name": "Angela Moss", "age": 27, "email": "amoss@gmail.com", "bid_price": 150}])

db.football.insertMany([{"name": "Darlene Alderson", "age": 23, "email": "da@protonmail.com", "bid_price": 123},{"name": "Angela Moss", "age": 27, "email": "amoss@gmail.com", "bid_price": 150},{"name": "Elliot Alderson", "age": 27, "email": "ea@protonmail.com", "bid_price": 300}])

db.tt.insertMany([{"name": "Angela Moss", "age": 27, "email": "amoss@gmail.com", "bid_price": 150}],{"name": "Elliot Alderson", "age": 27, "email": "ea@protonmail.com", "bid_price": 300},{"name": "Darlene Alderson", "age": 23, "email": "da@protonmail.com", "bid_price": 123})
- list all collections in sports database.
 - show collections
- rename `TT` collection to `tennis`.
 - db.tt.renameCollection("tennis")
- create a capped collection called `khokho` which should have max 3 documents.
 - db.createCollection("khokho", {capped: true, size: 1024, max: 3})
  - db.khokho.insertMany([{"name": "Elliot", "age": 27, "email": "ea@protonmail.com", "bid_price": 300},
{"name": "Darlene Alderson", "age": 23, "email": "da@protonmail.com", "bid_price": 123},
{"name": "Angela Moss", "age": 27, "email": "am@gmail.com", "bid_price": 150}])
  Try inserting more than 3 and see what happens?
  - db.khokho.insert({"name": "Dominique D'Piero", "age": 30, "email": "DD@gmail.com", "bid_price": 600})
- check whether a collection is capped or not?
 - db.khokho.isCapped() // true
db.football.isCapped() // false
- drop all documents from `football` collection.
 - db.football.drop()
- delete cricket collection completely.
 - db.cricket.remove({})
- delete sports database.
 - db.dropDatabase()
- check which database you are connected to ?
 - db
- connect to test database
 - use test
