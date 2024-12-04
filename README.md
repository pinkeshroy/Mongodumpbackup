# mongodumpbackup

**Take a MongoDB dump using the mongodump command.**
Below is the syntax:

mongodump --uri="mongodb+srv://<username>:<password>@<cluster-url>/<database>" --out=<output-directory-path>

Example Command:
 `mongodump --uri="mongodb+srv://user123:password123@cluster0.mongodb.net/myDatabase" --out=./backup
`
**Basic mongorestore command syntax**

mongorestore --uri="mongodb+srv://<username>:<password>@<cluster-url>/<database>" <dump-folder-path>

Example:
Restore a local dump to a remote MongoDB server:
  `mongorestore --uri="mongodb+srv://user123:password123@cluster0.mongodb.net/myDatabase" ./backup
`
Restore a local dump to a local MongoDB server:

 `mongorestore --db=myDatabase ./backup/myDatabase`

Restore Specific Collections:
 `mongorestore --uri="mongodb+srv://user123:password123@cluster0.mongodb.net/myDatabase" --collection=myCollection ./backup/myDatabase/myCollection.bson
`

Options for Overwriting Existing Data:
 Drop Existing Data: Use the --drop flag to delete existing data in the database before restoring:
 `mongorestore --drop --uri="mongodb+srv://user123:password123@cluster0.mongodb.net/myDatabase" ./backup
`
