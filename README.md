# mongodb2023-101

###### SQL vs NoSQL
![image](https://github.com/tnpLabLive/mongodb2023-101/assets/48873989/51fd5480-a8d1-4bbe-9291-b98c1d57a40d)

###### Scalability
![image](https://github.com/tnpLabLive/mongodb2023-101/assets/48873989/079672ce-cb62-43a1-9c55-b98d4c0f15ef)
[Video tutorial](https://www.youtube.com/watch?v=xpDnVSmNFX0)

 ###### Why Mongodb not MySQL/PostgreSQL
 1. Scalability
 2. NoSQL(Schema Less)
 3. Geospatial Support in MongoDB (Mysql can do also but It's complex to achieve).
 4. Many more...

[Features of MongoDB, Advantages of MongoDB, Disadvantages of MongoDB](https://www.geeksforgeeks.org/what-is-mongodb-working-and-features/)

[DataTypes in MongoDB](https://www.geeksforgeeks.org/datatypes-in-mongodb/)

[MongoDB Internal Architecture video](https://www.youtube.com/watch?v=ONzdr4SmOng)

### Commands
###### 1. Switch/Create dababase
```
use database_name
```
###### 2. create collection
```
db.createCollection("your collection name")

```
###### 3. Insert data into collection
```
db.yourCollectionName.insertOne({name:"Deepak", pincode: 462036})

```
###### 4. find all documents
```
db.yourCollectionName.find()

```
###### 4. find specific document
```
db.yourCollectionName.findOne({_id: ObjectId("64a6ee61a65d8a5eb71b8034")})

```
###### 5. Delete document

```
db.yourCollectionName.deleteOne({_id: ObjectId("64a6ee61a65d8a5eb71b8034")})

```


