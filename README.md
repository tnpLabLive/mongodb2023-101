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
###### 1. Switch/Create database
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
###### 6. Update document

```
db.yourCollectionName.updateOne({_id: ObjectId('64a6ee61a65d8a5eb71b8034')}, {$set:{name:"sm"}});

```
### Data modelling

![datamodeliing (1)](https://github.com/tnpLabLive/mongodb2023-101/assets/48873989/0760b955-95b4-4b45-8781-632ca6672144)

###### One to One(embedded)
```
db.user.insertOne({name:"sachin", email:"s@s.com", p_add: {pincode: 462036, city: "Bhopal"}})
```
###### One to Many(embedded)
```
db.user.insertOne({name:"Deepak", address: [{add_name:"Hometown", pinocde: 21212}, {add_name:"parmanent", pincode: 462036}]})

db.user.insertOne({name:"Deepak", hobby: ["photography", "reading tech news"]})
```

###### One to Many
```
db.user.insertOne({_id: 1 ,name:"Deepak"})

db.address.insertOne({UserId: 1, add_name:"Hometown", pinocde: 21212})
db.address.insertOne({UserId: 1, add_name:"parmanent", pincode: 462036})

```

###### Many to Many(embedded)
```
db.classes.insertOne({_id:1, name: "React Js"})
db.classes.insertOne({_id:2, name: "Mongodb"})

db.user.insertOne({name:"Deepak", enrollment: [{classes_id: 1}, {classes_id: 2}]})

```
###### Many to Many
```
db.classes.insertOne({_id:"classes1", name: "React Js"})
db.classes.insertOne({_id:"classes2", name: "Mongodb"})

db.user.insertOne({_id: "user1", name:"Deepak"})

db.enrollment.insertOne({UserID:"user1", ClassesID: "classes1"})
db.enrollment.insertOne({UserID:"user1", ClassesID: "classes2"})

```















