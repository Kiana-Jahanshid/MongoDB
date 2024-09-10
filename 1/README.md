# MongoDB 


# how to create MongoDB Image ?

+ ## 1.
```
docker pull mongodb
```
+ ## 2.
```
docker run --name mongo2 -d  mongo:latest
```

+ ## 3.
```
- docker exec -it mongo2 mongosh

  or 

- docker exec -it container-ID /bin/bash
- mongosh
```
<br>
<br>
<br>

# Used COMMANDS ( INSIDE the container ) :
for show all existing databases :
+ ``` show dbs ```

for creating a DB and switching to it :
+ ``` use db```

for showing all DB's collections :
+ ``` show collections```

<br>

# insert into db :

``` 
db.collection1.insertOne({"firstname":"brad" , "lastname":"pit" , "role":"guest" , "gender":"male" , "partner":"-"})
```

# show all objects of collection  :
```
db.collection1.find()
```

## Select casts with length of name less than 5 :
```
db.collection1.find({ "firstname" : { "$regex": "^.{1,4}$" } } ,{"_id":0 , "firstname":1 , "role":1 , "gender":1 , "partner":1})
```