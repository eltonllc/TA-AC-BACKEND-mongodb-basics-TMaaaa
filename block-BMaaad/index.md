writeCode

Write command to

- List collections from a database.
 - show collections
- create a new collection in your country database which you created recently.
 - use India
 - db.createCollection('States')

Write code to:-

- crate a database named `weather`
 - use weather
- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.
 - db.createCollection('temperature', {size: 500, capped: true, max: 3})
  - db.temperature.insert(
      [
          {"date": "18-11-2020", "temp": "32"}, {"date": "19-11-2020", "temp": "38"}, {"date": "20-11-2020", "temp": "2"}
          ]
          )
- create a simple collection named `humidity`
 - db.createCollection('humidity')
- check whether `temperature` collection is capped or not ?
 - db.temperature.isCapped()
- Delete `humidity` collection and then the entire database(weather).
 - db.humidity.drop
 - db.dropDatabase()