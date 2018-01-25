
## Create  a connection 


   **Connection** specifies a database connection from which a model can retrieve the data and at a time model can use only one connection. this page provides you with an abstract on what steps to take while setting up connection.
   Getting started:
   1.  From your database administrator, get the contact details for your database such as host name, database or schema name, username, and password.
   2. 2.Enable secure access to your database. You have several choices:
   -  Using an IP Address Whitelist, optionally adding SSL Encryption.
  - Using an SSH Tunnel, which provides an encrypted connection and extra authentication. This is more secure but also is more time-consuming to set up. 
 3. On your database, set it up to work with BiPlus. The instructions may vary different  from dialect to dialect. Typically it includes providing approval to Bi plus to access your database.
 4. In Looker, go to the Admin panel’s Connection page. If you are in a trial, typically you won’t have any connections on that page.
   
  To get started with the process you need to Select the database dialects used in your project and below are the steps to be followed:
 
  **1.** Click on **Database Section** to setup a database connection.

  **2.** Click on **+New connection**  button to start setting up the connection to database. In general, you specify the below mentioned fields:
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png)
  **Name** Specify a name to define connection
  
 **Database(dialect)** choose a appropriate dialect that matches your connection. 
   
>Note: As per your requirement we can include the dialects needed to run the business.

 **Host**  database host path
 
 **Database** name of the database

 **Username and Password** to connect the database

 **Maximum connection** concurrent connection used by database

 **Additional Parameters** include any additional JDBC parameter in this section

   
## SSH 

 if you are connecting BiPlus to your database without using SSH tunnel,you can go ahead with Database Configuration

In case if you are connecting through SSH tunnel with same database host,you need to provide the following information to BiPlus analyst:

- IP address or DNS name of the database server
- SSH port of the database server
- Database port number

if connecting with separate database host then you need to provide following information to your BI Plus analyst:
- IP address or DNS name of the database server as seen from the tunnel server
- Database port number as seen from the tunnel server
- IP address or DNS name of the tunnel server as seen from the public internet
- SSH port of the tunnel server as seen from the public internet
- Username on the tunnel server for the SSH connection (the standard is looker)

**3. Dialects** select the accurate dialect from the list using drop down option.

## Test and Save Connection

**4. Test Connection** click the button to check if the entered information is running accurately.

**5. Add Connection** click the button to establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar

## Edit a connection

   **6.** click on **Edit** option available on right side of your connection name to make changes.

## Delete a connection

**7.** click on **Delete** option available on far right of your connection name to delete the connection from database.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/database%202.png)

##  Dialects supported

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3bbaa9982fbbf193443bb882f359d2b1cf683390/images/dialects.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUzODc0MzQ1NywtODE0NzM1Njk3LC00MT
gxODgwOTQsMTY1NDgzMDg3MSw2OTY4NjQ5MTUsMTM2NDc0Mjcx
MywtMTg0MTQ5OTI5LC03MjQ0NDk3OCwxNjM4MTE3ODgyLC0xMj
cxMDk5NDM2XX0=
-->