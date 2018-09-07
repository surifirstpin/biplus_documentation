

<center><h1>SQL Runner </h1></center>

Using SQL Runner you can directly Access your database and clout that access in variety of ways. it can easily set up the connection, and navigate the tables under your schema. You can run pre-written SQL queries, view the query, run history. using sql runner can create your customs views and perform useful task with them in model section.  

## Navigate To SQL Runner

- To Navigate to SQL Runner, Login to BiPlus homepage and click on **SQL Runner Section** or,

- In **Analysis Section**, After Creating a report Click on **SQL Tab** to view the SQL query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/8301318bea750b7d048df7f5a8e06607d216dce7/images/navigate_sql.png)



- Select the **Connection and Schema** using a drop-down based on which you would like to query.

- Select the desired **Table** using drop-down.

- **Fields** displays number of fields available in the table selected.


![
](https://raw.githubusercontent.com/sv18042016/fp1/532dd8b61e94d1e08fe0b89afa6a5961336e8ad2/images/sql_ru.png)

- You can directly write the SQL query from scratch and run it, but make sure the dialects used in SQL runner should match the database dialects or,

- Make use of **History** section to Pre-run the previous query.

## Create SQL Query in SQL Runner

**1.** To create a SQL query from scratch, click on SQL Runner section.

**2.** Type your SQL command in SQL query area.

```
select STATIONCODE,AMOUNT FROM ORDERS
```

- To undo the SQL Command written, click on **Undo** Icon specified in SQL Area.

- To Redo the last written command, click on **Redo** Icon specified in SQL Area.

- To adjust the query according to Syntax, select **Text Wrap** button. 
![
](https://raw.githubusercontent.com/sv18042016/fp1/acd887b4aec5663dca6969ad0004c73f4b351dc3/images/undo_sql.png)


**3.**  Hit **Run** button to run the SQL command written. It displays the data retrieved below the query area as shown in the image. 

> **Note :** SQL runner can fetch a maximum limit of 5000 records only.

## Find
To view a specific value from the data retrieved, select **Find** from drop-down list of the field header.

## Group

 To apply grouping for the data retrieved, select **Group** from drop-down list of the field header, or else, you can directly group it by writing following code in sql command.

```
SELECT STATIONCODE,SUM(AMOUNT) FROM ORDERS GROUP BY STATIONCODE
```
## Pin

   To Pin the the data, select **Pin** from drop-down list of the field header.

## Download

To download the data retrieved click on **Download** Icon as explained in below image.

## Number of records
Number of reco
  ![
](https://raw.githubusercontent.com/sv18042016/fp1/b86474022ef60bfa90365160155a02a2254aff13/images/find_sql.png)

**4.**  Once the query is executed it displays the **Query Time**  and **Number of rows** fetched.

**5.** Dialects used while setting up connection will be displayed at top Right of the query area,

![
](https://raw.githubusercontent.com/sv18042016/fp1/master/images/commit.png)


**6.** To view the recent history, click on **History tab** available at the top right of the SQL query area. 
- Green colour indicates query has been executed successfully and Red colour indicates error.
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
eyJoaXN0b3J5IjpbMjEyMzk3Njg2NCwtNTEyNTA1MDkxLC0xOT
kyMDA1NDEsNTU3ODE3Mjg5LC0xOTQwNDY0MTUxLDQ2MzE5MDk3
NiwtNzc4MzAxNzMwLC04MTIyNDg0LC0xMDMzMjUwNDE4LC0xND
IyNzM0ODYsLTY4NjUyNzE1MiwtMTgwNjY1NTIzNiwtMTg1MjY3
MTI2OCwtNTQwNTExNjM0LC0xODUyNjcxMjY4LC0xNTM0MDMwOT
MwLC04ODY5Mzg3MDQsLTgwMTYwODgwMiwxMDMyODA4NDI0LDc4
OTcxNDZdfQ==
-->