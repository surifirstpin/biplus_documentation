

<center><h1>SQL Runner </h1></center>

Using SQL Runner you can directly Access your database and clout that access in variety of ways. In SQL Runner you can easily set up the connection, and navigate the tables under your schema. You can run pre-written SQL queries view the query run history. You can create your customs views here and perform useful task with them in model section.  

- Select the **Connection and Schema** you would like to Query.
- Select the **Table** using using drop-down list, to display the number of columns available in particular table.
- **Fields** Sections displays the Fields that fall under selected table.


![
](https://raw.githubusercontent.com/sv18042016/fp1/532dd8b61e94d1e08fe0b89afa6a5961336e8ad2/images/sql_ru.png)

- You can directly write the SQL query from scratch and run it but you need to make sure the dialects used in SQL runner should match the database dialects or,

- You can also create SQL query in analysis section. 

- Make use of **History** section to Pre-run the previous query.

## Navigate To SQL Runner

- To Navigate to SQL Runner, Login to BiPlus homepage and click on **SQL Runner Section** or,

- In **Analysis Section**, After Creating a report Click on **SQL Tab** to view the SQL query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/8301318bea750b7d048df7f5a8e06607d216dce7/images/navigate_sql.png)

## Create SQL Query in SQL Runner

**1.** To create a SQL query from scratch click on SQL Runner section after Logging into BiPlus homepage.

**2.** Type your SQL command in SQL query area.

```
select STATIONCODE,AMOUNT FROM ORDERS
```

- To undo the SQL Command written Click on **Undo** Icon specified in SQL Area.

- To Redo the last written command click on **Redo** Icon specified in SQL Area.

- To adjust the query according to Syntax select **Text Wrap** button. 
![
](https://raw.githubusercontent.com/sv18042016/fp1/acd887b4aec5663dca6969ad0004c73f4b351dc3/images/undo_sql.png)


**3.**  Click on **Run** button to run the SQL command written. On running the sql command, it displays the data retrieved below the query area as shown in the image. 

> **Note :** SQL runner can fetch a maximum limit of 5000 records only.

   - From the data retrieved to view the particular field value click **Find** option available in the field column header drop-down list.

    -  To group the data retrieved click on **Group** option available in drop down list of column header similarly, or else,

**You can directly group it by writing following code in sql command this way;**

```
SELECT STATIONCODE,SUM(AMOUNT) FROM ORDERS GROUP BY STATIONCODE
```

 -  To Pin the the column values select **Pin** option available in the same list.
  ![
](https://raw.githubusercontent.com/sv18042016/fp1/b86474022ef60bfa90365160155a02a2254aff13/images/find_sql.png)

**4.**  After Running the query it displays the **Query Time** taken to run the query and **Number of rows** fetched.

**5.** Dialects used while setting up connection will be displayed at top Right of the query area,

![
](!%5B%20%5D%28https://raw.githubusercontent.com/sv18042016/fp1/163409615d153a964fefc66224c6378d51e14661/images/commit.png%29)

**6.** To View the recent history, click on **History tab** available at the top right of the SQL query area. 
- Green colour indicates successfully query and Red colour indicates query that did not run successfully due to the error.  
![
](https://raw.githubusercontent.com/sv18042016/fp1/master/images/history%20sql.png)

## Apply Sorting


In your query result you can view the data in ascending or descending order by applying sorting. To enable sorting Click on column header, to reverse the sorting order click on column header for second time **or,**

Write the following code in sql command this way;
```
ORDER BY STATIONCODE ASC
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/5f2f6b7d5ed9daf4222fd8da2636ecabbe2cabcd/images/sort_sql.png)

## Derived View

SQL Runner can create a derived view from the query build at the same time you can use this view in model section. the dialects used for creating a derived view should be same as in SQL runner.

To get started with derived view, Click on **List icon** and Select **Create Derived View.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/cdb0e5ca373edcb312536038651c1b8bbffb1f54/images/list_derived%20view.png)

**Enter the below fields ;**

- **Derived View Name** Enter Label for identification to the new derived view.

 - **Projects** Select the dialects using the drop down button.
 
 - **Query** the query created in sql runner will be added here.
 
 -  **Field List** On selecting the dialects all the fields used in query are reflected here.

 **Click on Create, to create the New Custom view.** 
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/cdb0e5ca373edcb312536038651c1b8bbffb1f54/images/create_derived_view1.png)

To view the newly created derived view. Go to Model section under the views list as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/44c6a5e67268522711a49a43c55d04588892b5f0/images/derived_view.png)

## Create Query in Analysis Section

You can also make use of **Analysis Section** to create a query.

- Select the text from SQL area in Analysis section after running a reports
-  and copy it to SQL Runner.

- Copy paste the text to SQL area  and **Run** the SQL Runner to Query the database. You can also customize the already existing text as per your business needs and run the new query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5b49497f917e7ef704bffb142452286fdec45747/images/sql_Analysis.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY4NjUyNzE1MiwtMTgwNjY1NTIzNiwtMT
g1MjY3MTI2OF19
-->