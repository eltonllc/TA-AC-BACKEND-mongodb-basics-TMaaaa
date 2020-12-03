writeCode

Write code to:-

- create a database named `mountains`
 - use mountains
- a collection inside that database named `himalayas`
 - db.createCollection ("mountains")
- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`
 - db.mountains.insert({name: 'Dhauldhar range', height: '4000 mtrs'}) 
- insert multiple document using insertMany command
 - db.mountains.insertMany([
     {name: 'Dhauldhar range', height: '4000 mtrs'},
     {name: 'Potato range', height: '5000 mtrs'}
 ]) 
- find all documents from himalayas
 - db.himalayas.find()
- find a single document using name
 - db.COLLECTION_NAME.find({name :'Dhauldhar range' })