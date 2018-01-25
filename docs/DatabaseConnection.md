
## Create  a connection 


   **Connection** specifies a database connection from which a model can retrieve the data and at  a time model can use only one connection. to get started with the process you need to Select the database dialects used in your project and below are the steps to be followed:
 
  **1.** Click on **Database Section** to setup a database connection.

  **2.** Click on **+New connection**  button to start setting up the connection to database. in general, you specify the below mentioned fields:
  
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png)

  **Name** Specify a name to define connection
  
   **Database(dialect)** choose a appropriate dialect that matches your connection. at present Bi Plus is supporting following list of Database.Further to this we can also include the dialect as per the business requirement.
   
>Note: In case if your database are not available in the above mentioned list,Bi Plus will include the dialects required.

 **Host** Provides the database host path
 
**Database** name of the database

**Username and Password** to connect the database

**Maximum connection** concurrent connection used by database

**Additional Parameters** include any additional JDBC parameter in this section

   
## SSH 

**Over SSH** to acsess ne

**3. Dialects** select the accurate dialect from the list using drop down option.

## Test and Save Connection

**4. Test Connection** click the button to check if the entered information is running accurately.

**5. Add Connection** click the button to establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar

## Edit a connection

   **6.** click on **Edit** option available on right side of your connection name to make changes.

## Delete a connection

**7.** click on **Delete** option available on far right of your connection name to delete the connection from database.

##  Dialects supported

 - MySQL
 - Oracle
 - Vertica
 - Rest
 - PSQL
 - MariaDB
 - Amazon Aurora(MySQL)  
 - Amazon Redshift
 - Google BigQuery
 - Snowflake
 - PostgreSQL
 - Teradata
 - Apache Spark
 - Impala
 - Amazon Athena
 - Druid
 - Cloud Spanner
 - MemSQL
 - Hive
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/screenshot.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NDY3MTc3NDIsNDM4NzQ2MDczLDIxMD
Q3MDIwNCwtMTM5NzY5MzQyNiwtMTc1MDI4NzY1M119
-->