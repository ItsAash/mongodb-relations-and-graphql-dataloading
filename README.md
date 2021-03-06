## In this exercise
 - [x] Creating One to One Relationship using Typegoose. (Media.uploadedBy => User)
 - [x] Creating One to Many Relationship using Typegoose. (User.medias => Media)
 - [x] Inserting datas into the db by maintaining the relationship.
 - [x] Querying users and also populating medias. (With N+1 GraphQL problem)
 - [x] Querying medias and also populating users. (With N+1 GraphQL problem)
 - [x] DataLoader for User(uploadedBy) while Querying Media. (N+1 Fixed for users)


## To get started
 Insert users into the database (http://localhost:27017/Test) (collectionName: "users")
 ```json
 [{
  "_id": {
    "$oid": "620b47b00ca297a44127e011"
  },
  "name": {
    "firstName": "John",
    "lastName": "Doe",
    "fullName": "John Doe"
  },
  "medias": [
    {
      "$oid": "620b47b00ca297a44127e012"
    },
    {
      "$oid": "620bce7087c29d95a6d97eec"
    },
    {
      "$oid": "620b47b10ca297b69121e012"
    }
  ],
  "__v": 0
},{
  "_id": {
    "$oid": "620bd2ccfe0f055d4e4873fb"
  },
  "name": {
    "firstName": "Jeff",
    "lastName": "Martin",
    "fullName": "Jeff Martin"
  },
  "medias": [
    {
      "$oid": "620bd2dcfe0f159d4e4873fc"
    }
  ],
  "__v": 0
}]
 ```
 
 
 also add medias to the db (collectionName: "medias")
```json
[{
  "_id": {
    "$oid": "620b47b00ca297a44127e012"
  },
  "title": {
    "romanji": "Shingeki no Kyojin",
    "english": "Attack on Titan",
    "native": "Chixuixau",
    "userPreferred": "Shingeki no Kyojin"
  },
  "releasedDate": {
    "year": 2022,
    "month": 1,
    "day": 2
  },
  "uploadedBy": {
    "$oid": "620b47b00ca297a44127e011"
  },
  "__v": 0
},{
  "_id": {
    "$oid": "620bce7087c29d95a6d97eec"
  },
  "title": {
    "romanji": "Naruto",
    "english": "Naruto",
    "native": "na ru to",
    "userPreferred": "Naruto"
  },
  "releasedDate": {
    "year": 2022,
    "month": 1,
    "day": 2
  },
  "uploadedBy": {
    "$oid": "620b47b00ca297a44127e011"
  },
  "__v": 0
},{
  "_id": {
    "$oid": "620b47b10ca297b69121e012"
  },
  "title": {
    "romanji": "JOJO",
    "english": "JOJO",
    "native": "jo jo",
    "userPreferred": "JOJO"
  },
  "releasedDate": {
    "year": 2010,
    "month": 1,
    "day": 2
  },
  "uploadedBy": {
    "$oid": "620b47b00ca297a44127e011"
  },
  "__v": 0
},{
  "_id": {
    "$oid": "621bcf7097c29e95a6d97fed"
  },
  "title": {
    "romanji": "Black Clover",
    "english": "Black Clover",
    "native": "black clover",
    "userPreferred": "Black Clover"
  },
  "releasedDate": {
    "year": 2022,
    "month": 1,
    "day": 2
  },
  "uploadedBy": {
    "$oid": "620bd2ccfe0f055d4e4873fb"
  },
  "__v": 0
}]
```

*Ignore my studip titles*
