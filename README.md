# MongoDb
<!--I used Mongo DB Compass tool to run the commands -->
```javascript
use example
switched to db example
db.todo_table.insertOne({task : "Play",
status:"Not done"})
{
  acknowledged: true,
  insertedId: ObjectId('6837e49c9192cb2f4a1e279b')
}
db.todo_table.insertMany([
  {task : 'dance',status: "Not done"},
  {task : 'sing',status :" Not done"},
  {task : 'Study',status : "Done"}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6837e5d79192cb2f4a1e279c'),
    '1': ObjectId('6837e5d79192cb2f4a1e279d'),
    '2': ObjectId('6837e5d79192cb2f4a1e279e')
  }
}
db.todo_table.updateMany({status : "Done"},
                         {$set : {status:true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: 'Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: 'Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : "Not Done"},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: 'Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: 'Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : "Not done"},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : ' Not done'},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.insertMany([
  {task : 'shopping',status: true},
  {task : 'go for a walk',status :false},
  {task : 'chill with friends',status : true}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6837e67b9192cb2f4a1e279f'),
    '1': ObjectId('6837e67b9192cb2f4a1e27a0'),
    '2': ObjectId('6837e67b9192cb2f4a1e27a1')
  }
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true
}
db.todo_table.insertMany([
  {task : 'Eat',status: false},
  {task : 'Sleep',status :true},
  {task : 'Talk to parents',status : true}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6837e6999192cb2f4a1e27a2'),
    '1': ObjectId('6837e6999192cb2f4a1e27a3'),
    '2': ObjectId('6837e6999192cb2f4a1e27a4')
  }
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a2'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a3'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a4'),
  task: 'Talk to parents',
  status: true
}
db.todo_table.updateMany(
  { status: { $exists: false } },
  { $set: { status: false } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.insertOne([
  {task : 'Clockout'}
])
{
  acknowledged: true,
  insertedId: ObjectId('6837e6c39192cb2f4a1e27a5')
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a2'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a3'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a4'),
  task: 'Talk to parents',
  status: true
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6837e6c39192cb2f4a1e27a5')
}
db.todo_table.updateOne([
  {_id : '6836e8fe31485535101b3925'},
  {$set : {status : true}}
])
MongoInvalidArgumentError: Update document requires atomic operators
db.todo_table.updateOne([
  {_id : ObjectId('6836e8fe31485535101b3925')},
  {$set : {status : true}}
])
MongoInvalidArgumentError: Update document requires atomic operators
db.todo_table.updateOne(
  {_id : ObjectId('6836e8fe31485535101b3925')},
  {$set : {status : true}}
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a2'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a3'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a4'),
  task: 'Talk to parents',
  status: true
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6837e6c39192cb2f4a1e27a5')
}
db.todo_table.updateMany(
  { status: { $exists: true } },
  { $push: { updateAt: new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 10,
  upsertedCount: 0
}
db.todo_table.updateMany(
  { status: { $exists: true } },
  { $push: { createdAt: new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 10,
  upsertedCount: 0
}
db.runCommand({
  collMod: "todo_table",
  validator: {
    $jsonSchema: {
      bsonType: "object",
      properties: {
        priority: {
          enum: ["low", "medium", "high"]
        }
      }}}})
{ ok: 1 }
db.todo_table.updateMany(
  { name: { $exists: true } },
  { $set: { priority : "medium" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.updateMany(
   { name: { $exists: true } },
  { $set: { priority : "medium" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a2'),
  task: 'Eat',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a3'),
  task: 'Sleep',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a4'),
  task: 'Talk to parents',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ]
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6837e6c39192cb2f4a1e27a5')
}
db.todo_table.updateMany(
  { priority: { $exists: false } },  
  { $set: { priority: "low" } }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.todo_table.updateMany(
  { task : 'Clock in'},  
  { $set: { priority: "low" } }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.insertOne(
  { task : 'Clock in',status : 'false'}      
);
{
  acknowledged: true,
  insertedId: ObjectId('6837efb39192cb2f4a1e27a6')
}
db.todo_table.updateOne(
  { task : 'Clock in'},  
  { $set: { status: true ,updatedAt : new Date()} }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6837e49c9192cb2f4a1e279b'),
  task: 'Play',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279c'),
  task: 'dance',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279d'),
  task: 'sing',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e5d79192cb2f4a1e279e'),
  task: 'Study',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e279f'),
  task: 'shopping',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a0'),
  task: 'go for a walk',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e67b9192cb2f4a1e27a1'),
  task: 'chill with friends',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a2'),
  task: 'Eat',
  status: false,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a3'),
  task: 'Sleep',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6837e6999192cb2f4a1e27a4'),
  task: 'Talk to parents',
  status: true,
  updateAt: [
    2025-05-29T04:49:22.723Z
  ],
  createdAt: [
    2025-05-29T04:49:36.220Z
  ],
  priority: 'low'
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6837e6c39192cb2f4a1e27a5'),
  priority: 'low'
}
{
  _id: ObjectId('6837efb39192cb2f4a1e27a6'),
  task: 'Clock in',
  status: true,
  updatedAt: 2025-05-29T05:25:25.046Z
}
db.todo_table.updateMany(
  { task: { $exists: true } },
  { $set: { dueDate : new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.todo_table.find(
  {dueDate : {$eq : new Date()}}
);
db.todo_table.find(
  {dueDate : {$eq : new Date(28)}}
);
```
