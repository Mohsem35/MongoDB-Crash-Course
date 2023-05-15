### Facts about MongoDB:

- MongoDB is a NoSQL database(not only SQL) is not true, MongoDB can use SQL

- MongoDB is a non-relational database is not true,you can store relational data in mongo db. It just stored differently than relational database
- Document database, data is stored in BSON(binary JSON) under the hood but is represented as JSON

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

1.
{ $in: ["Kyle", "Sally"]
if the name is in this list of names. is the name 'kyle' or is the name 'sally'

$nin: not in(the reverse of $in)

2.
test> db.users.find({age: {$exists: true}})
show the list with age objects

test> db.users.find({age: {$exists: false}})
show the list without age objects

3.
test> db.users.find({age: {$gte: 20, $lte:40}})
show the objects, where age is greater than 20 and less than 40

4.
$and = pretend that we are doing another find and we are just combining all the things inside the 'and'. 'and' takes an array
test> db.users.find({$and: [{age:23},{name:"walker"}]})

Get all users that have an age of 12 and the name Kyle

$or = Get all users with a name of Kyle or an age of 12
test> db.users.find({$or: [{age: {$lte:20}},{name:"walker"}]})

Note: both 'and','or' uses 3rd bracket []

5.
db.users.find({age: {$not: {$lte: 20}}})
Get all users whose age is not less than 20

6. in order to compare 2 differnt properties on an object, we need to use the dollar $expr
db.users.find({$expr: {$gt:["debt","balance"]}})

'debt' is greater than 'balance'
