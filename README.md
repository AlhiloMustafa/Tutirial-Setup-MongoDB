# Tutirial-Setup-MongoDB
###### Because I believe nothing can stop what we can do when we work together, I share what I learned with others.

## After completing the tutorial you will be able to:

- Connect to MongoDB using MongoDB shell 
- Conncect to MongoDB from app.js

## Prerequisite

- Mongo shell installed already [install mongo shell](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
- Simple Web-App with simple interface to implement CRUD functionality on the database (For example simple node.js Web-App)

## let's get it started :

- Sing up for MongoDB Atlas [Account]( https://www.mongodb.com/cloud/atlas)
      o	Try Free -> Sign in -> Shared Clusters (Free)
      o	I Will go with AWS(Free), you can do Google Cloud too (Free too)
      o	N. Virginia (us-east-1) (Free) -> Cluster Tier (M0 Sandbox- Free forever)
      o	Cluster name can change it or just keep it Cluster0 (By default)
      o	Finally click Create Cluster -> It will take 1-3 min provision 
      
- MongoDB Users: Under Security we currently have no users (lets create new user):

      o	Add New Database User
      o	Password Authentication (Save them because we are going to use them)
      o	Username (admin-mustafa)
      o	Password (*****)
      o	Change Database User Privileges to Atlas admin instead or (read and write to database)
      o	Finally click Add User (It is going to added it to a list of MongoDB Users)
##### Note: This MongoDB users have the credentials which will need to communicate with our database on MongoDB Atlas and using username and password to keep our database more secure. 

- IP Whitelist:

      o	Go to Network Access -> ADD IP Address
      o	In Add IP Whitelist Entry 
      o	Chose ALLOW ACCESS FROM ANYWHERE and then Confirm (it will take some time)
      
- Connect to our cluster:

      o	Go to All Clusters on Top right of the page, and Click on Cluster 0 (the one we create already)
      o	Click on the connect button on the right side of the page
      o       Chose the first option “Connect with mongo shell” and you should have mongo shell installed already if not go to[Install Mongo shell](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
      o	Click “I have the mongo shell installed” and chose the version you have open in mongo shell run ($ mongo –version) to see which version you have. 
      o	On Select your mongo shell version select the version that you have.(in my case 4.2)
      o	Now on “Run your connection string in your command line” it gives A URL to connect to MongoDB Cluster  
      o	Copy the URL and past it in the command line no matter in which directory and hit ENTER use “test” instead of <dbname>  in the URL. 
      o	It will ask for password that we entered already for the admin-mustafa.
      o	I hop there is no error , but if there is an error go to [Troubleshooting Connection Issue](https://docs.atlas.mongodb.com/troubleshoot-connection/)
      o	Now we have active session with the MongoDB shell running on Atlas cluster and we can start using Mongo commands for example, “show dbs↵”
      
- Test the connection MongoDB shell:

      o	In the Cluster0 -> click on COLLECTIONS -> Add My Own Data -> DATABASE NAME: test, and COLLECTION NAME : test -> Create
      o	Now we add new data to the collection by clicking on “INSERT DOCUMENT” It is on the right side or the window.
      o	Like this ( 2- new data : “this is our database”) -> Click Insert
      o	We can access it from MongoDb shell using “show dbs↵ “ and “use test↵”we see our collection and “db.test.find()↵“ to see the document. 
      
- Now Connect to MongoDB cluster to save data in cloud MongoDB Atlas:

      o	In the Cluster0 -> Connect Your Application --> SRV connection string Copy the URL  past it in the app.js and replace the local connection with this new URL. 
      o	Note: add you the database password and the name of the database it is up to you. For example, mongodb+srv://admin-mustafa:12345@cluster0.feuuv.mongodb.net/mydata
      o	In mongo shell run app.js connected on port 3000 
      o	On chrome go to http://localhost:3000/ 
      o	Now it is connected to MongoDB database you can do CRUD. 




## References

- https://docs.atlas.mongodb.com/troubleshoot-connection/
- https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/
 


[Back To The Top](#Tutirial-Setup-MongoDB)

---

## License

Copyright (c) [2020] [Mustafa Alhilo]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.



[Back To The Top](#Tutirial-Setup-MongoDB)

---

## Author Info

- LinkedIn- [Mustafa Alhilo](https://www.linkedin.com/in/mustafa-alhilo-08736214b/)

[Back To The Top](#Tutirial-Setup-MongoDB)
