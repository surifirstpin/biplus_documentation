
## Create  a connection 


   **Connection** specifies a database connection from which a model can retrieve the data and at  a time model can use only one connection. to get started with the process you need to Select the database dialects used in your project and below are the steps to be followed:
 
 
  **1.** Click on **Database Section** to setup a database connection.

  **2.** Click on **+New connection**  button to start setting up the connection to database. in general, you specify the below mentioned fields:
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png)

  **Name** Specify a name to define connection

   **Database(dialect)** choose a appropriate dialect that matches your connection. at present Bi Plus is supporting following list of Database.Further to this we can also include the dialect as per the business requirement.
   
>Note: In case if your database are not available in the above mentioned list,Bi Plus will include the dialects required.

 **Host** Provides the database host path
 
**Database** identifier name of the database used for connection

**Username and Password** to connect the database

**Temp database** ( depending on the selected dialects) contains a derived set of tables which can be used as per requirement

**Maximum connection** number of connection you want to setup

**Additional Parameters** include any additional JDBC parameter in this section
## Different Dialects supported
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
   
## SSH Functionality

**Over SSH** protect the data using a user and access key assigned to it

**3. Dialects** select the accurate dialect from the list using drop down option.

## Test and Save Connection

**4. Test Connection** click the button to check if the entered information is running accurately.

**5. Add Connection**click the button to establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar

## Edit a connection

   **6.** click on **edit** option available on right side of your connection name to make changes.

## Delete a connection

**7.** click on **delete** option available on far right of your connection name to delete the connection from database.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/screenshot.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDIwNTE0MDAyLC03MjQ0NDk3OCwxNjM4MT
E3ODgyLC0xMjcxMDk5NDM2XX0=
-->