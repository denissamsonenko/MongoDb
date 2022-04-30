## Mongo container using DockerCompose

### Commands:

* docker compose down
* docker compose up -d
* mongo mongodb://localhost:27017 -u root -p root - connect to shell mongo

#### The examples interacting with mongo in shell

* show dbs; - show db
* use name; - 
* db.getName();
* db.createCollection("hello");
* db.dropDatabase();
* db.help();
* show collections
* db.person.stats()
* db.person.drop()
* db.student.insert(student)
* db.student.count();
* db.student.find()
* db.student.find().pretty()
* db.student.insertMany(students)
* db.student.find({firstName: "Bred"}, {firstName: 1, lastName: 1}).pretty()
* db.student.find({firstName: "Bred"}, {firstName: 0, lastName:0, gender: 0}).pretty() - 0 exclude fields
* db.student.find({}, {firstName: 1, lastName: 1}).pretty()
* db.student.update({_id: ObjectId("626d1fd7dddb5660e104395b")},{$set: {firstName: "Vadim", lastName: "Hulio", email: "vadim@mail.ru"}}) - update command
* db.student.update({_id: ObjectId("626d1fd7dddb5660e104395b")},{$unset: {favoriteSubjects: 1}}) - delete param at all
* db.student.update({_id: ObjectId("626d1fd7dddb5660e104395f")}, {$inc: {totalSpentInBooks:100}}) - increment
* db.student.update({_id: ObjectId("626d1fd7dddb5660e104395f")}, {$pull: {favoriteSubjects: "it"}}) - delete element from array
* db.student.update({_id: ObjectId("626d1fd7dddb5660e104395f")}, {$push: {favoriteSubjects: "it"}}) - add element to array
* db.student.updateMany({}, {$inc: {totalSpentInBooks:100}})
* db.student.deleteOne({_id: ObjectId("626d1db0dddb5660e104395a")})
* db.student.deleteMany({gender: "F"})


