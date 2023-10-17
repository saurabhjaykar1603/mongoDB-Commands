# mongoDB Commands

## **Show Database :**

> When we show our All Databases then we can use the `show db`
> command.

**Syntax :**

```js
show db
```

## **Use Database or Create Database :**

> When we Want to Perform an operation or Create a database, we can `use db` command.

**Syntax :**

```js
use db
```

**Example :**

```js
use teachers
```

## **Create Collection :**

> To create a collection, you can use the `createCollection()` method in MongoDB.

**Example :**

```
db.createCollection("myCollection")
```

This will create a collection named `"myCollection"` in the current database.

## **insert One Document :**

> If we want to _insert only one document_ then we can used `insertOne()` command.

**Syntax :**

```js
insertOne();
```

**Example :**

```js
db.teachers.insertOne({
  name: "suraj shende",
  subject: "full stack Development",
});
```

## **Insert Multiple Document :**

> If we want to _insert only multiple
> document_ then we can used `insertMany()` command.

**Syntax :**

```js
insertMany();
```

**Example :**

```js
db.teachers.insertMany([
  {
    name: "suraj shende",
    subject: "full stack Development",
  },
  {
    name: "pinki hole",
    subject: "python programming",
  },
]);
```

## **Find Documents From Collections :**

> The `find()` Method is used to serach for documents within a specific range according to some criteria.

**Syntax :**

```js
db.find();
```

**Examples :**

```js
db.teachers.find({ name: "pinki hole" });
```

## **Update Document In A Collection :**

> You can update existing document using `updateOne()`, `updateMany()` methods.

- `updateOne()` :

* Updates only one matching record in collection, if no records are matched then it does not perform any operation and returns an error message.

**Syntax :**

```js
updateOne({ key: value }, { $set: { key: value } });
```

**Examples :**

```js
// update one Teacher in a collection
db.updateOne({ name: "suraj shende" },$set: {adress: "nagpur"});
```

- `updateMany()`

> The `updateMany()` method updates all documents that match the specified filter.

**Syntax :**
