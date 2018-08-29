## Steps to implement the MiniProject:
-----------------------------------

## Step 1:
	prepare the mysql database

	
- we will use mysql database for both authentication & about
  module data.


Default Password : root

## create the schema
-----------------
> create schema poc;
	- automatically poc schema will be created.


## switch to schema
----------------
> use poc;
	- automatically we can switch to poc schema.

## create the "login_details" table
--------------------------------
> create table login_details(uname varchar(20),upwd varchar(20));
	- automatically "login_details" table will be created.


## insert the data into "login_details" table
------------------------------------------
> insert into login_details values("admin","admin");
	- automatically we can insert the record into table.

## fetch the data from "login_details" table
-----------------------------------------
> select * from login_details;
	- automatically we can fetch the data from "login_details" table


## create the "products" table
---------------------------
> create table products(p_id integer,p_name varchar(20),p_cost integer);
	- automatically "products" table will be created.


## insert the data into "products" table
-------------------------------------
> insert into products values(111,'p_one',10000);
	- automatically we can insert the record into "products"
	  table.

## fetch the data from "products" table
------------------------------------
> select * from products;
	- automatcally we can fetch the data from the products 
	  table

************************************************
host : localhost

user : root

password : root

database : poc

tables   : login_details
	   products
***********************************************
	   


## Step 2:
	prepare MongoDB.

 - MongoDB used for "contact module" data.

 - "MongoDB" is the ligth weigth database compared to other
   databases.

 - "MongoDB" follows the "client server" architecture.

 - "MongoDB" Supports the JSON.

 - As a "MongoDB" developer we can perform the CRUD Operations
   on JSON.


## start the server:
-----------------
> mongod
	- automatically server will start.
	
	- by default server listening the port no.27017.

	- by default server follows the "mongodb" protocol.


## connect to server:
------------------
> mongo
	- automatically we are able to connect to server.


## create and switch to database
-----------------------------
> use poc;
	- automatically we can create and switch to database.



## create the collection:
----------------------
> db.createCollection("products");
	- automatically we are able to create the products
	  collection.



## insert the json object:
-----------------------
> db.products.insert({"p_id":111,"p_name":"p_one","p_cost":10000});
	- automatically we are able to insert the json object



## fetch the data from collection:
-------------------------------
> db.products.find();
	- automatically we can fetch the data from products collection.



## show the databases:
-------------------
> show dbs;
	- automatcally we are able to show the available databases



## drop the database:
------------------
> db.dropDatabase();
	- automatically we are able to drop the database.

	
************************************************
host : localhost

port  : 27017

protocol : mongodb

database : poc

collection : products
**********************************************


## Step 3:
-------
	create the static page 

	- we will use "static page" for portfolio module


*******************************
POC

   static
	 
         sample.json
******************************

sample.json
-----------
[
    {"p_id":111,"p_name":"p_one","p_cost":10000},

    {"p_id":222,"p_name":"p_two","p_cost":20000},

    {"p_id":333,"p_name":"p_three","p_cost":30000}
 
]


## Step 4:
	download the node modules


1) express


2) mysql


3) mongodb@2.2.32


4) body-parser


5) jwt-simple

	- express module used to develop the Rest API.

	- mysql module used to interact with the MySQL database.

	- mongodb module used to interact with the mongodb.

	- body-parser module used to read the post parameters

	- jwt-simple module used to generate the token.

> yarn add express --save

> yarn add mysql --save

> yarn add mongodb@2.2.32 --save

> yarn add body-parser --save

> yarn add jwt-simple --save


 ## Step 5:
	Develop the Following Rest API'S


1) "/login"

2) "/about"

3) "/contact"

4) "/portfolio"


*************************************
POC
   server
        config
	  db_properties.js
	  db_connection.js

	login
	    login.js

	about
	    about.js			  

	contact
	    contact.js

	portfolio
	    portfolio.js

	token
	    generateToken.js

	server.js
******************************************

	- "db_properties.js" used to maintain
	  the db properies.

	- "db_connection.js" used to create
	  the mysql connection object. 

	- "login.js" used to create the login
	  Rest API

	- "about.js" used to create the about
	  Rest API.

	- "contact.js" used to create the contact
	  Rest API.

	- "portfolio.js" used to create the
	  portfolio Rest API.
	
	- "generateToken.js" file used to
	  generate the token to maintain the
	  session.

	
## Step 6:
	start the node server

> node server


## Step 7:
	start the mongo server

> mongod


## Step 8:
	test the following Rest API'S By using
	Postma.


1) http://localhost:8080/login


2) http://localhost:8080/about


3) http://localhost:8080/contact


4) http://localhost:8080/portfolio


## Step 9:
	create the loginService

	- loginService receives the "login_details"
	  from loginComponent and sends to
	  Node Server


*******************************
POC
   src
     app
	services
	    login.service.ts
********************************	
 
Step 10:
	create the "dashboardService"

*********************************
POC
  src
    app
      services
	 dashboard.service.ts
*********************************

Step 11:
	implement the single page application

*******************************************
POC
  src
    app
      components
	 index.component.ts
	 index.component.html

	 login.component.ts
	 login.component.html

	 dashboard.component.ts
	 dashboard.component.html

	 about.component.ts
	 about.component.html

	 contact.component.ts
	 contact.component.html


	 portfolio.component.ts
	 portfolio.component.html
	
       router
	  app.routes.ts

       app.module.ts
   index.html	
********************************************

































































	



































 




























