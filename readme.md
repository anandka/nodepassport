Prerequisites

Make sure you have mongodb installed.


Follow the following steps to make database and to add entries to it


Creating a MongoDB Data Store

Start the mongod server using the following command:
mongod --config /etc/mongodb.conf



From another terminal launch the Mongo shell:
mongo


Within the shell, issue the following commands:

use MyDatabase;

db.userInfo.insert({'username':'admin','password':'admin'});

The first command creates a data store named MyDatabase.
The second command creates a collection named userInfo and inserts a record. 



Let’s insert a few more records:

db.userInfo.insert({'username':'jay','password':'jay'});
db.userInfo.insert({'username':'roy','password':'password'});



Retrieving Stored Data
We can view the data we just added using the following command:

db.userInfo.find();
The resulting output is shown below:

{ "_id" : ObjectId("5321cd6dbb5b0e6e72d75c80"), "username" : "admin", "password" : "admin" }
{ "_id" : ObjectId("5321d3f8bb5b0e6e72d75c81"), "username" : "jay", "password" : "jay" }
{ "_id" : ObjectId("5321d406bb5b0e6e72d75c82"), "username" : "roy", "password" : "password" }




Running the project

type the command - node app.js

open - http://localhost:3000/login

expected output - You should see a small form which will ask for credentials

on correct credentials - it will show Successfully authenticated
on incorrect credentials - it will show Failed to authenticate





Tutorial followed:
http://www.sitepoint.com/local-authentication-using-passport-node-js/