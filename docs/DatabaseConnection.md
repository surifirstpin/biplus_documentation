<center><h1>Database Connection</h1></center>

## Definition 

   **Connection** specifies a database connection from which a model can retrieve the data. Following are the steps to be followed to set up database connection.
    
**I.**  Get the connection details for database such as Host name, port, username and password etc.           

  **Database Administrator**.

**II.** Enable secure access to your database. You have several choices:
  -  Using an IP Address Whitelist, optionally adding SSL Encryption.
  - Using an SSH Tunnel, which provides a secured and encrypted connection with extra authentication
  
**III.** Set up your database to work with BiPlus. The instructions may vary from dialect to dialect. Typically it includes providing approval to BiPlus to access your database.

 ## Create Connection
 
**Getting started :**
>Path : Database-->New connection

  To get started with the process you need to Select the database dialects used in your project and below are the steps to be followed:
 
 **1.** Click on **Database Section** to setup a database connection.

 **2.** Click on **+New connection**  button to start setting up the connection to database. In general, you specify the below mentioned fields:
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png)

 **Name** specify a name to define connection
 **Database(dialect)** choose a appropriate dialect that matches your connection. 
>Note: As per your requirement we can include the dialects needed to run the business.

**Host**  database host path.
**Database** name of the database.
**Username and Password** to connect the database.
**Maximum connection** concurrent connection used by  database.
**Additional Parameters** include any additional JDBC parameter in this section.

## SSH 

 **If you want to connect Bi+ SSH tunnel with same database host,you need to provide the following information to BiPlus analyst:**
 
  - IP address or DNS name of the database server
  - SSH port of the database server
  - Database port number
  
**If connecting with separate database host then you need to provide following information to your BI Plus analyst:**
  
  - IP address or DNS name of the database server as seen from the   tunnel server
  - Database port number as seen from the tunnel server
  - IP address or DNS name of the tunnel server as seen from the public internet
  - SSH port of the tunnel server as seen from the public internet
  - Username on the tunnel server for the SSH connection (the standard is looker)
  
**3. Dialects** select the accurate dialect from the list using drop down option.

## Test and Save Connection

**4. Test Connection** Checks if the entered information is running accurately.

**5. Add Connection** establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar

## Edit a connection

   **6.** click on **Edit** option available on right side of your connection name to make changes.
   
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/edit_conn.png)

## Delete a connection

**7.** Click on **Delete** option available on far right of your connection name to delete the connection from database.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/del_conn.png)

##  Dialects supported

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3bbaa9982fbbf193443bb882f359d2b1cf683390/images/dialects.png)	

### Next Steps

Once you have Setup the Database connection you can further take up the process by following below steps :

  - **Create Project** to control data in model.
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkxNjM4MzA3OSwtMjQ0OTYxNDE2LDE1Mz
E5NDU2MDEsMjEwNDcwMjA0LC0xMzk3NjkzNDI2LC0xNzUwMjg3
NjUzXX0=
-->