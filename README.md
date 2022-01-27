
# Database

> __show dbs__ : To list all the database

> __use *db_name*__ : Creates the database if it is not present and use the database. If it is present then use that database.

> __db.dropDatabase()__ : Drop the current database

# Collections

> __show collections__ - Show the list of collections in that database.

# Create
>__db.playerInfo.insertOne({})__ : To insert one document

*Example:*
```
db.playerInfo.insertOne({"player_name":"Lionel Messi","country":"Argentina","country_of_birth":"Argentina","dob":new Date("1987-06-24"),"position":["RW","CF","ST"],"height":170,"age":34,"foot":"left","clubs":[{"club_name":"Barcelona","club_country":"Spain","apps":520,"goals":474,"join_year":2004,"left_year":2021, "role":"Player"} ,{"club_name":"Paris Saint-Germain","club_country":"France","apps":11,"goals":1,"join_year":2021, "role":"Player"}],"national_team":{"apps":158,"goals":80,"start_year":2005}})
```

 > __db.playerInfo.insertMany([{}])__ : To insert mutiple documents as array

*Example:*
 ```
 db.playerInfo.insertMany([{"player_name":"Gianluigi Donnarumma","country":"Italy","country_of_birth":"Italy","dob":new Date("1999-02-25"),"position":["GK"],"height":196,"age":22,"foot":"right","clubs":[{"club_name":"AC Milan","club_country":"Italy","apps":215,"goals":0,"join_year":2015,"left_year":2021,"role":"Player"},{"club_name":"Paris Saint-Germain","club_country":"Spain","apps":9,"goals":0,"join_year":2021,"role":"Player"}],"national_team":{"apps":40,"goals":0,"start_year":2016}},{ "player_name":"Robert Lewandowski","country":"Poland","country_of_birth":"Poland","dob":new Date("1988-08-21"),"position":["ST"],"height":185,"age":33,"foot":"right", "clubs":[{"club_name":"Legia Warsaw II","club_country":"Poland","apps":29,"goals":6,"join_year":2005,"left_year":2006,"role":"Player"}, {"club_name":"Znicz Pruszkow","club_country":"Poland","apps":56,"goals":36,"join_year":2006,"left_year":2008,"role":"Player"}, {"club_name":"Znicz Pruszkow II","club_country":"Poland","apps":2,"goals":6,"join_year":2006,"left_year":2007,"role":"Player"}, {"club_name":"Lech Poznań","club_country":"Poland","apps":58,"goals":32,"join_year":2008,"left_year":2010,"role":"Player"}, {"club_name":"Borussia Dortmund","club_country":"Germany","apps":131,"goals":74,"join_year":2010,"left_year":2014,"role":"Player"}, {"club_name":"Bayern Munich","club_country":"Germany","apps":238,"goals":226,"join_year":2014,"role":"Player"}], "national_team":{"apps":128,"goals":74,"start_year":2008} }, { "player_name":"João Cancelo","country":"Portugal","country_of_birth":"Portugal","dob":new Date("1994-05-27"),"position":["LB","RB"],"height":182,"age":27,"foot":"right", "clubs":[{"club_name":"Benfica B","club_country":"Portugal","apps":51,"goals":3,"join_year":2012,"left_year":2014,"role":"Player"}, {"club_name":"Benfica","club_country":"Portugal","apps":1,"goals":0,"join_year":2014,"left_year":2015,"role":"Player"}, {"club_name":"Valencia","club_country":"Spain","type":"loan","apps":10,"goals":0,"join_year":2014,"left_year":2015,"role":"Player"}, {"club_name":"Valencia","club_country":"Spain","apps":64,"goals":2,"join_year":2015,"left_year":2018,"role":"Player"}, {"club_name":"Inter Milan","club_country":"Italy","type":"loan","apps":26,"goals":1,"join_year":2017,"left_year":2018,"role":"Player"}, {"club_name":"Juventus","club_country":"Italy","apps":25,"goals":1,"join_year":2018,"left_year":2019,"role":"Player"}, {"club_name":"Manchester City","club_country":"England","apps":65,"goals":3,"join_year":2019,"role":"Player"}], "national_team":{"apps":31,"goals":5,"start_year":2016} }, { "player_name":"Rúben Dias","country":"Portugal","country_of_birth":"Portugal","dob":new Date("1997-05-14"),"position":["CB"],"height":187,"age":24,"foot":"right", "clubs":[{"club_name":"Benfica B","club_country":"Portugal","apps":55,"goals":0,"join_year":2015,"left_year":2017,"role":"Player"}, {"club_name":"Benfica","club_country":"Portugal","apps":91,"goals":9,"join_year":2017,"left_year":2020,"role":"Player"}, {"club_name":"Manchester City","club_country":"England","apps":52,"goals":3,"join_year":2020,"role":"Player"}], "national_team":{"apps":37,"goals":2,"start_year":2018} }, { "player_name":"Achraf Hakimi","country":"Morocco","country_of_birth":"Spain","dob":new Date("1998-11-04"),"position":["RM"],"height":181,"age":22,"foot":"right", "clubs":[{"club_name":"Real Madrid Castilla","club_country":"Spain","apps":28,"goals":1,"join_year":2016,"left_year":2017,"role":"Player"}, {"club_name":"Real Madrid","club_country":"Spain","apps":9,"goals":2,"join_year":2017,"left_year":2020,"role":"Player"}, {"club_name":"Borussia Dortmund","club_country":"Germany","type":"loan","apps":54,"goals":7,"join_year":2018,"left_year":2020,"role":"Player"}, {"club_name":"Inter Milan","club_country":"Italy","apps":37,"goals":7,"join_year":2020,"left_year":2021,"role":"Player"}, {"club_name":"Paris Saint-Germain","club_country":"France","apps":18,"goals":3,"join_year":2021,"role":"Player"}], "national_team":{"apps":44,"goals":6,"start_year":2016} }, { "player_name":"Kevin De Bruyne","country":"Belgium","country_of_birth":"Belgium","dob":new Date("1991-06-28"),"position":["CM","CAM"],"height":181,"age":30,"foot":"right", "clubs":[{"club_name":"Genk","club_country":"Belgium","apps":97,"goals":16,"join_year":2008,"left_year":2012,"role":"Player"}, {"club_name":"Chelsea","club_country":"England","apps":3,"goals":0,"join_year":2012,"left_year":2014,"role":"Player"}, {"club_name":"Werder Bremen","club_country":"Germany","type":"loan","apps":33,"goals":10,"join_year":2012,"left_year":2013,"role":"Player"}, {"club_name":"VfL Wolfsburg","club_country":"Germany","apps":37,"goals":7,"join_year":2020,"left_year":2021,"role":"Player"}, {"club_name":"Manchester City","club_country":"England","apps":193,"goals":48,"join_year":2015,"role":"Player"}], "national_team":{"apps":88,"goals":23,"start_year":2010} }, { "player_name":"Jorginho","country":"Italy","country_of_birth":"Brazil","dob":new Date("1991-12-20"),"position":["CM"],"height":180,"age":30,"foot":"right", "clubs":[{"club_name":"Hellas Verona","club_country":"Italy","apps":89,"goals":11,"join_year":2010,"left_year":2014,"role":"Player"}, {"club_name":"Sambonifacese","club_country":"Italy","type":"loan","apps":31,"goals":1,"join_year":2010,"left_year":2011,"role":"Player"}, {"club_name":"Napoli","club_country":"Italy","apps":37,"goals":7,"join_year":2020,"left_year":2021,"role":"Player"}, {"club_name":"Chelsea","club_country":"England","apps":193,"goals":48,"join_year":2018,"role":"Player"}], "national_team":{"apps":42,"goals":5,"start_year":2016} }, { "player_name":"N’Golo Kanté","country":"France","country_of_birth":"France","dob":new Date("1991-03-29"),"position":["CM","CDM"],"height":168,"age":30,"foot":"right", "clubs":[{"club_name":"Boulogne","club_country":"France","apps":38,"goals":3,"join_year":2012,"left_year":2013,"role":"Player"}, {"club_name":"Caen","club_country":"France","apps":75,"goals":4,"join_year":2013,"left_year":2015,"role":"Player"}, {"club_name":"Leicester City","club_country":"England","apps":37,"goals":1,"join_year":2015,"left_year":2016,"role":"Player"}, {"club_name":"Chelsea","club_country":"England","apps":171,"goals":22,"join_year":2016,"role":"Player"}], "national_team":{"apps":51,"goals":2,"start_year":2016} }, { "player_name":"Kylian Mbappé","country":"France","country_of_birth":"France","dob":new Date("1998-12-20"),"position":["ST","LW"],"height":182,"age":23,"foot":"right", "clubs":[{"club_name":"Monaco II","club_country":"France","apps":12,"goals":4,"join_year":2015,"left_year":2016,"role":"Player"}, {"club_name":"Monaco","club_country":"France","apps":41,"goals":16,"join_year":2015,"left_year":2018,"role":"Player"}, {"club_name":"Paris Saint-Germain","type":"loan","club_country":"France","apps":27,"goals":13,"join_year":2017,"left_year":2018,"role":"Player"}, {"club_name":"Paris Saint-Germain","club_country":"France","apps":99,"goals":88,"join_year":2018,"role":"Player"}], "national_team":{"apps":53,"goals":24,"start_year":2017} }, { "player_name":"Marquinhos","country":"Brazil","country_of_birth":"Brazil","dob":new Date("1994-05-14"),"position":["CB"],"height":183,"age":27,"foot":"right", "clubs":[{"club_name":"Corinthians","club_country":"Brazil","apps":14,"goals":0,"join_year":2011,"left_year":2013,"role":"Player"}, {"club_name":"Roma","type":"loan","club_country":"Italy","apps":16,"goals":0,"join_year":2012,"left_year":2013,"role":"Player"}, {"club_name":"Roma","club_country":"Italy","apps":10,"goals":0,"join_year":2013,"left_year":2013,"role":"Player"}, {"club_name":"Paris Saint-Germain","club_country":"France","apps":220,"goals":20,"join_year":2013,"role":"Player"}], "national_team":{"apps":64,"goals":4,"start_year":2013}}])
 ```


# Retrieve

> __find(*filterOptions*)__ To retrieve all the documents matching the searchOptions in the collection

*To retrieve all the player data in the collection*
```
db.playerInfo.find()
```

*To retrieve all the players whose playing for the country argentina*
```
db.playerInfo.find({country:"Argentina"})
```

*To retrieve all the records with the search criteria country as Italy and show only the player_name(_id is shown as default)*
```
db.playerInfo.find({country:"Italy"},
                    {player_name:1}
                  )
```

*To retrieve all the records with the search criteria country as Italy and show only the player_name,_id will not be displayed*
```
db.playerInfo.find({country:"Italy"},
                   {player_name:1,_id:0}
                  )
```

*To retrieve all the records with the search criteria country as Italy and show only the player_name,_id will not be displayed and limit the count to 2*
```
db.playerInfo.find({foot:"right"},
                   {player_name:1,_id:0}
                  ).limit(2);
```


# Sort

__db.playerInfo.find().sort({country:1,player_name:1})__ : Sorts the documents based on the country alphabetical order and then player_name alphabetical order. Here (positive)1 is used to sort the documents in alphabetical order (negative)1 used to sort in reverse alphabetical order.

__db.playerInfo.find().sort({country:-1})__ :

__db.playerInfo.find({},{player_name:1,country:1,_id:0}).sort({country:1,player_name:1})__ : Sorts the documents based on the country and player_name, displays only the player_name and country field.

# Distinct

__db.playerInfo.distinct("foot")__ List the distinct values for this field in the collection

# Count

__db.playerInfo.count({foot:"right"})__

__db.playerInfo.countDocuments()__ Shows the number of documents in the collection

# Filter Queries

> __$eq :__ equal

*Return all the players who's position array contains ST*
```
db.playerInfo.find({position:{$eq:"ST"}},
                   {player_name:1,position:1,_id:0}
                  )
```

> __$ne :__ not equal

*Return all the players who's position array does not contains ST*
```
db.playerInfo.find({position:{$ne:"ST"}},
                   {player_name:1,position:1,_id:0}
                  )
```

> __$in :__ in -  _to return the documents which contains the field value listed in the "in" array._
```
db.playerInfo.find({position:{$in:["ST","RB"]}},
                   {player_name:1,position:1,_id:0}
                  )
```

> __$nin :__ not in -  _to return the documents which does not contains the field value listed in the "in" array._
```
db.playerInfo.find({position:{$nin:["ST","RB"]}},
                   {player_name:1,position:1,_id:0}
                  )
```

> __$gt :__ greater than -  _to return the documents for which the field is greater than the given value._
```
db.playerInfo.find({age:{$gt:30}},
                   {player_name:1,age:1,_id:0}
                  )
```

> __$gte :__ greater than or equal to -  _to return the documents for which the field is greater than or equal to the given value._
```
__db.playerInfo.find({age:{$gte:30}},
                     {player_name:1,age:1,_id:0}
                    )
```

> __$lt :__ lesser than -  _to return the documents for which the field is lesser than the given value._
```
db.playerInfo.find({age:{$lt:30}},
                   {player_name:1,age:1,_id:0}
                  )
```

> __$lte :__ lesser than or equal to -  _to return the documents for which the field is lesser than or equal to the given value._
```
__db.playerInfo.find({age:{$lte:30}},
                     {player_name:1,age:1,_id:0}
                    )
```

> __$lt and $gt :__
```
db.playerInfo.find({dob:{$gt: new Date('1990-01-01'), $lt: new Date('1995-01-01')}},
                   {player_name:1,age:1,_id:0}
                  )
```

> __$elemMatch:__ _Match an element in the object array_
```
__db.playerInfo.find({clubs: {$elemMatch: {club_name:"Paris Saint-Germain"}}},
                     {player_name:1,_id:0}
                    )
```

> __$exists:__ _To check if the field exists (even if the field vlaue is null it is considered as exists)_
```
__db.playerInfo.find({clubs: {$elemMatch: {left_year:{$exists:false}}}},
                      {_id: 0, player_name:1, clubs: {$elemMatch: {left_year: {$exists:false}}}}
                    )
```

> __$expr:__
```
__db.playerInfo.find({$expr:{$ne:["$country","$country_of_birth"]}})
```

> __$or:__
```
db.playerInfo.find({$or: [{country:"France"},{age:{$gt:30}}]},
                   {player_name:1,age:1,country:1,_id:0})
```

> __$not:__
```
__db.playerInfo.find({country:{$not:{$eq:"France"}}},
                     {player_name:1,country:1,_id:0})
```

>  __$and:__
```
db.playerInfo.find({$and: [{country:"France"},{age:{$gte:30}}]},
                   {player_name:1,age:1,country:1,_id:0}
                   )
db.playerInfo.find({country:"France",age:{$gte:30}},
                   {player_name:1,age:1,country:1,_id:0}
                  )
```

# Update

### updateOne

> __$set:__
```
db.playerInfo.updateOne({"player_name":"Lionel Messi"},
                        {$set: {"player_name":"Lionel Andrés Messi"}}
                       )
```

### updateMany

> __$currentDate:__
```
db.playerInfo.updateMany({},{$currentDate:{lastUpdate:true}})
db.playerInfo.find({},{player_name:1,lastUpdate:1,_id:0})
```

### replaceOne

```
db.playerInfo.replaceOne(
   { "player_name" : "Lionel Andrés Messi" },
   {"player_name":"Lionel Messi","country":"Argentina","country_of_birth":"Argentina","dob":new Date("1987-06-24"),"position":["RW","CF","ST"],"height":170,"age":34,"foot":"left","clubs":[{"club_name":"Barcelona","club_country":"Spain","apps":520,"goals":474,"join_year":2004,"left_year":2021, "role":"Player"} ,{"club_name":"Paris Saint-Germain","club_country":"France","apps":11,"goals":1,"join_year":2021, "role":"Player"}],"national_team":{"apps":158,"goals":80,"start_year":2005}}
);
```

```
db.playerInfo.replaceOne(
   { "player_name" : "Erling Haaland" },
   {"player_name":"Erling Haaland","country":"Norway","country_of_birth":"United Kingdom","dob":new Date("2000-07-21"),"position":["ST"],"height":194,"age":21,"foot":"left","clubs":[{"club_name":"Bryne 2","club_country":"Norway","apps":14,"goals":18,"join_year":2015,"left_year":2016, "role":"Player"},{"club_name":"Bryne","club_country":"Norway","apps":16,"goals":0,"join_year":2016,"left_year":2017, "role":"Player"},{"club_name":"Molde","club_country":"Norway","apps":43,"goals":16,"join_year":2017,"left_year":2019, "role":"Player"},{"club_name":"	Red Bull Salzburg","club_country":"Austria","apps":16,"goals":17,"join_year":2019,"left_year":2020, "role":"Player"},{"club_name":"Borussia Dortmund","club_country":"Germany","apps":67,"goals":56,"join_year":2020, "role":"Player"}],"national_team":{"apps":15,"goals":12,"start_year":2019}},
   { upsert: true }
);
```

### Update Queries

> __$set and $unset:__
```
db.playerInfo.updateOne({"player_name":"Marquinhos"},[{$set:{temp_country:"$country"}},{$unset: ["country"]}])
db.playerInfo.updateOne({"player_name":"Marquinhos"},[{$set:{country:"$temp_country"}},{$unset: ["temp_country"]}])
```

> __$rename:__
```
db.playerInfo.updateOne({"player_name":"Marquinhos"},{$rename:{"country":"temp_country"}})
db.playerInfo.updateOne({"player_name":"Marquinhos"},{$rename:{"temp_country":"country"}})
```

> __$inc:__
```
db.playerInfo.find({"player_name":"Lionel Andrés Messi"},{clubs:1});
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $inc: { "clubs.1.apps": 1, "clubs.1.goals": 1 } }
)
```

### Update Array Queries

> __$pop:__  remove an element from first or last of an array.
```
db.playerInfo.find({"player_name":"Lionel Andrés Messi"},{player_name:1,position:1,_id:0});
//Removes first element in the position array
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $pop: { position: -1 } }
)
//Removes last element in the position array
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $pop: { position: 1 } }
)
```

> __$push:__ appends a specified value to an array.
```
db.playerInfo.find({"player_name":"Lionel Andrés Messi"},{player_name:1,position:1,_id:0});
//Appends "RW" to the position array
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $push: { position: "RW" } }
)
//Appends "ST" to the position array
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $push: { position: "ST" } }
)
```

> __$pull:__ Remove All the elements that Match a Specified $pull Condition
```
db.playerInfo.updateOne({"player_name":"Marquinhos"},[{$set:{country:"$temp_country"}},{$unset: ["temp_country"]}])
db.playerInfo.find({"player_name":"Lionel Andrés Messi"},{player_name:1,position:1,_id:0});
//Removes RW and ST,(if present)
db.playerInfo.updateOne(
   {"player_name":"Lionel Andrés Messi"},
   { $pull: { position: {$in: [ "RW", "ST" ]} } }
)
```

> __$addToSet:__ Remove All the elements that Match a Specified $pull Condition
```
db.playerInfo.updateOne(
   { "player_name":"Lionel Andrés Messi" },
   { $addToSet: { position: "ST" } }
)
db.playerInfo.updateOne(
   { "player_name":"Lionel Andrés Messi" },
   { $addToSet: { position: "RW" } }
)
db.playerInfo.updateOne(
   { "player_name":"Lionel Andrés Messi" },
   { $addToSet: { position: "CF" } }
)
```

# Aggregation

To process the data record to get some meaningful insights

> __$group__
```
db.playerInfo.aggregate([{$group:{_id:"$country",average_age:{$avg:"$age"}}}])
```

> __$unwind__
```
db.playerInfo.aggregate([{$unwind:{path: "$clubs",includeArrayIndex: "arrayIndex"}}])
```

> __$unwind and $group__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}}])
```
> __$sort__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}},{$sort:{club_total_goals:-1}}])
```

> __$limit__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}},{$sort:{club_total_goals:-1}},{$limit:3}])
```

> __$skip__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}},{$sort:{club_total_goals:-1}},{$skip:1}])
```

> __$limit and $skip__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}},{$sort:{club_total_goals:-1}},{$limit:3},{$skip:1}])
```

> __$match__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$match:{country:{$in: ["France","Argentina"]}}},{$group:{_id:"$player_name",club_total_apperance:{$sum:"$clubs.apps"},club_total_goals:{$sum:"$clubs.goals"}}}])
```
> __$project__
```
db.playerInfo.aggregate([{$unwind: "$clubs"},{$project:{player_name:1,country:1,age:1,"clubs.club_name":1}}])
```

> __$project and $filter__
```
db.playerInfo.aggregate([{$project: {player_name:1,clubs:{$filter:{ input:"$clubs",as:"club",cond:{$gte:["$$club.goals",100]}}}}}])
db.playerInfo.aggregate([{$unwind: "$clubs"},{$sort:{{$getField:"clubs.join_year"}:1}},{$group:{_id:"$player_name",first_joined_club:{$first:"$clubs.join_year"}}}])
```

# Delete

>__deleteOne(deleteFilter)__
*Delete the first document in the collection which matches the deleteFilter*
```
db.playerInfo.__deleteOne()
```

> __deleteMany(deleteFilter)__
*Delete all the documents in the collection which matches the deleteFilter*
```
db.playerInfo.deleteMany({})
```
