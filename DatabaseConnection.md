## Create  a connection 

 Connection specifies a database connection from which a model can retrieve the data and at time a model can use only one connection. to get started with the process you need to Select the database dialects used in your project and below are the steps to be followed:
 
**1.** Click on Database Section to setup a database connection.

**2.** Click on +New connection button to start setting up the connection to database. in general, you specify the below mentioned fields:
- **Name** Specify a name of the connection to define

## Different Dialects supported

 **Database(dialect)** choose a appropriate dialect that matches your connection.at present Bi Plus is supporting following list of Database.Further to this we can also include the dialect as per the business requirement.
  - MySQL
  - Oracle
  - MS SQL
   - Vertica
  - Rest
  - PSQL
  - MariaDB
  - Amazon Aurora(MySQL)
In the most recent release, Bi Plus also supports following list of dialects;
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
>Note: In case if your database are not available in the above mentioned list, Bi Plus will include the dialects required.|

- **Host** Provides the database host path
- **Database** identifier name of the database used for connection
- **Username and Password** to connect the database
- **Temp database** ( depending on the selected dialects) contains a derived set of tables which can be used as per requirement
- **Maximum connection** maximum number of connection you want to setup
- **Additional Parameters** include any additional JDBC parameter in this section

## SSH Functionality

- **Over SSH** protect the data using a user and access key assigned to it

**3. Dialects** select the accurate dialect from the list using drop down option.

## Test Connection
**4. Test Connection** click the button to check if the entered information is running accurately.

**5. Add Connection**click the button to establish and save the connection.

>After establishing the connection you can see the list of connections names on left side toolbar


## Edit a connection

   **6.** click on **edit** option available on right side of your connection name to make changes.

## Delete a connection


**7.** click on **delete** option available on far right of your connection name to delete the connection from database.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI2ODAxNzY1NV19
-->