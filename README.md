### Facts about MongoDB:
---

- MongoDB is a NoSQL database(not only SQL) is not true, `MongoDB can use SQL`
- MongoDB is a non-relational database is not true, `you can store relational data in mongo db.` It just stored differently than relational database.
- Document database, `data is stored in BSON(binary JSON) under the hood but is represented as JSON`
- Schema in MongoDB is optional and flexible.
- MongoDB syntax is `very similar to JavaScript.`
- Doesn't need any semicolon(;) for ending of the query like SQL.

JSON is structured as objects containing key value pairs
MongoDB Atlas - cloud database

### Terminology:
---

***Collection:*** A grouping of documents inside of a database. This is the **same as a table in
SQL** and usually each type of data (users, posts, products) will have its own
collection.

***Document:*** A record inside of a collection. This is the **same as a row in SQL** and usually
there will be one document per object in the collection. A document is also
essentially just a JSON object.

***Field:*** A key value pair within a document. This is the **same as a column in SQL.**
Each document will have some number of fields that contain information
such as name, address, hobbies, etc. An important difference between SQL
and MongoDB is that a field can contain values such as JSON objects, and
arrays instead of just strings, number, booleans, etc.

### Install MongoDB community edition
---

[MongoDB + mongosh installation process](https://www.golinuxcloud.com/install-mongodb-rocky-linux/)

```
$ mongosh
>test : test database by default
```

AT LAST, Read the 'Cheat Sheet' along with this readme.md file which name is `Light.pdf`
