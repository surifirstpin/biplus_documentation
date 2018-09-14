<center><h1>Database Connection</h1></center>

   **Connection** Specifies a database connection from which a model can retrieve the data.
   
 **To set up database connection, Follow the below steps;**
    
**I.**  Get the connection details for database such as Host name, port, username and password etc from **Database Administrator.**.

**II.** Enable secure access to database, such as :
  -  Using  IP Address Whitelist, optionally adding SSL Encryption.
  - Using SSH Tunnel, which provides a secured and encrypted connection with extra authentication.
  
**III.** Set up database to work with BiPlus. Instructions may vary from dialect to dialect. Typically it includes providing approval to BiPlus to access database.

 ## Set-Up Connection

>**Navigation: Database→ New connection**

 **1.** Click on **Database Section** to setup a database connection.

 **2.** Click on **New Connection**  button to start setting up the connection to database. In general, specify the below mentioned fields:
 
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png)

-  **Name** specify a name to define connection.
 
 - **Database (dialect)** choose appropriate dialect based on  connection. 
>**Note:** As per your requirement, we can include the dialects needed to run the business.

- **Host**  Database host path.

- **Database** Name of the database used.

- **Username and Password** Credentials used to connect the database.

- **Maximum connection** Concurrent connection used by  database.

- **Additional Parameters** Additional JDBC parameter used.

## SSH 

**a)**  To connect BiPlus SSH tunnel with same database host, provide following information to BiPlus analyst :
 
  - IP address or DNS name of the database server
  - SSH port of the database server
  - Database port number
  
**b)** If connecting with separate database host, **provide following information to BiPlus analyst:**
  
  - IP address or DNS name of the database server as seen from the tunnel server.
  - Database port number as seen from the tunnel server.
  - IP address or DNS name of the tunnel server as seen from the public internet.
  - SSH port of the tunnel server as seen from the public internet.
  - Username on the tunnel server for the SSH connection (the standard is looker).
  
**3.** **Dialects** select the accurate dialect from the list using drop down option.

## Test and Save Connection

**4.** **Test Connection** check if the entered information is running accurately.

**5.** **Add Connection** establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar

## Edit a connection

   **6.** Click on **Edit** option to make changes.
   
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/edit_conn.png)

## Delete a connection

**7.** Click on **Delete** option to delete the connection from database.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/del_conn.png)

##  Dialects supported

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3bbaa9982fbbf193443bb882f359d2b1cf683390/images/dialects.png)	

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMjMzNDczNDUsMTMzMzY0MTMzLDM0OD
Q2NjgwNywtMTEyMDQxMTQ5MywxNjUzNDgzMjhdfQ==
-->