### Step 1: Start MongoDB Shell

1. Open your terminal.

2. Run the `mongo` command to start the MongoDB shell:

```bash
mongo
```

### Step 2: Switch to a Database

1. To switch to a specific database, use the `use` command followed by the name of the database:

```bash
use mydatabase
```

Replace `mydatabase` with the name of your database.

### Step 3: Show Databases

1. To show all databases available on the MongoDB server, run the following command:

```bash
show databases
```

This command will list all databases, including empty databases.

### Step 4: Show Collections

1. After switching to a database, you can list all collections within that database using the `show collections` command:

```bash
show collections
```

This command will display all collections present in the current database.

### Step 5: Show Data from a Collection

1. To display all documents (data) in a collection, use the `db.collectionName.find()` method. Replace `collectionName` with the name of your collection:

```bash
db.collectionName.find()
```

For example, to display all documents in a collection named `users`:

```bash
db.users.find()
```

2. You can also apply query criteria to filter the results. For example, to find documents where the `age` field is greater than 18:

```bash
db.collectionName.find({ age: { $gt: 18 } })
```

### Step 6: Insert Documents into a Collection

1. To insert documents into a collection, use the `db.collectionName.insertOne()` or `db.collectionName.insertMany()` methods.

For example, to insert a single document into a collection named `users`:

```bash
db.users.insertOne({ name: "John", age: 30 })
```

2. To insert multiple documents into a collection:

```bash
db.users.insertMany([
    { name: "Alice", age: 25 },
    { name: "Bob", age: 35 }
])
```

### Step 7: Update Documents in a Collection

1. To update documents in a collection, use the `db.collectionName.updateOne()` or `db.collectionName.updateMany()` methods.

For example, to update a single document in the `users` collection:

```bash
db.users.updateOne({ name: "John" }, { $set: { age: 31 } })
```

2. To update multiple documents:

```bash
db.users.updateMany({ age: { $lt: 30 } }, { $set: { category: "Young" } })
```

### Step 8: Delete Documents from a Collection

1. To delete documents from a collection, use the `db.collectionName.deleteOne()` or `db.collectionName.deleteMany()` methods.

For example, to delete a single document from the `users` collection:

```bash
db.users.deleteOne({ name: "John" })
```

2. To delete multiple documents:

```bash
db.users.deleteMany({ category: "Young" })
```

### Step 9: Exit MongoDB Shell

1. To exit the MongoDB shell, type `exit` and press Enter:

```bash
exit
```

These commands cover the basic CRUD operations (Create, Read, Update, Delete) in MongoDB from the shell. Adjust the database, collection names, and query criteria as needed for your specific use case.
