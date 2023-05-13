Facts about MongoDB:

1. MongoDB is a NoSQL database(not only SQL) is not true, MongoDB can use SQL

2. MongoDB is a non-relational database is not true,you can store relational data in mongo db. It just stored differently than relational database
3. Document database, data is stored in BSON(binary JSON) under the hood but is represented as JSON

Schema in MongoDB: optional and flexible

JSON is structured as objects containing key value pairs

MongoDB Atlas - cloud database
1. Install MongoDB community edition

MongoDB + mongosh installation process: https://www.golinuxcloud.com/install-mongodb-rocky-linux/


$ mongosh
>test : test database by default

collections: are like tables inside of a database
mongodb syntax is very similar to javascript

every single object{} you store inside of a database in mongodb is called document.
documents live in collections
collections live inside of databases

doesn't need any semicolon(;) for ending of the query like SQL.


test> db.users.insertOne({name: "kyle"})

test> db.users.insertOne({name: "walker", age: 23, address: {street: "park street", road: 34}, hobbies: ["Running","Travelling","Learning new technologies"]})
