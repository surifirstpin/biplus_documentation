

<center><h1>SQL Runner </h1></center>

Using SQL Runner you can directly access database and clout the access in variety of ways. it can easily set up the connection, and navigate the tables under your schema. In sql runner you can run the  pre-written SQL queries, view run history and create custom views and perform useful task with them in model section.  

## Navigate To SQL Runner

- To Navigate to SQL Runner section, Login to AcuBi and click on **SQL Runner Section** or,

- In **Analysis Section**, After Creating a report Click on **SQL Tab** to view the SQL query generated on running the report.

![
](https://raw.githubusercontent.com/sv18042016/fp1/8301318bea750b7d048df7f5a8e06607d216dce7/images/navigate_sql.png)


- Select the **Connection and Schema** using a drop-down list based on which you would like to query.

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

## Number of records fetched

Number of records fetched after running a query is displayed at right bottom of the page as shown in the image.

  ![
](https://raw.githubusercontent.com/sv18042016/fp1/b86474022ef60bfa90365160155a02a2254aff13/images/find_sql.png)

**4.**  Once the query is executed it displays the **Query Time**  and **Number of rows** fetched.

**5.** Dialects used while setting up connection will be displayed at top right of the query area,

![
](https://raw.githubusercontent.com/sv18042016/fp1/master/images/commit.png)


**6.** To view the recent history, click on **History tab** available at the top right of the SQL query area. 
- Green colour indicates query has been executed successfully and Red indicates error.

![
](https://raw.githubusercontent.com/sv18042016/fp1/master/images/history%20sql.png)

## Apply Sorting

The query result can be viewed in ascending or descending order by applying sorting. To enable sorting click on column header, to reverse the sorting order click on column header for second time, or else you can write the following code in sql command ;

### Ascending Order
```
ORDER BY STATIONCODE ASC
```
### Descending Order
```
ORDER BY STATIONCODE DSC
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/5f2f6b7d5ed9daf4222fd8da2636ecabbe2cabcd/images/sort_sql.png)

## Derived View

SQL Runner can create a derived view from the query build and at the same time you can use this view in model section too. The dialects used for creating a derived view should be same as in SQL runner.

To get started with derived view, Click on **List icon** and select **Create Derived View.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/cdb0e5ca373edcb312536038651c1b8bbffb1f54/images/list_derived%20view.png)

**Enter the below fields ;**

- **Derived View Name** Enter Label for identification of new derived view.

 - **Projects** Select the dialects from drop down list.
 
 - **Query** the query created in sql runner will be added here.
 
 -  **Field List** On selecting the dialects all the fields used in query are reflected here.

 **Click on Create, to create the New Custom view.** 
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/cdb0e5ca373edcb312536038651c1b8bbffb1f54/images/create_derived_view1.png)

To view the newly created derived view. Navigate to **Model section** under the views list as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/44c6a5e67268522711a49a43c55d04588892b5f0/images/derived_view.png)

## Create Query in Analysis Section

Now, let us see how to create a query in **Analysis Section**.

- Select the fields in analysis section and run the report.

- Click on SQL tab and copy the query build on running the report, then copy it to SQL Runner.

- Once copied **Run** SQL Runner to Query the database. You can also customize the already existing text as per your business needs and run the new query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5b49497f917e7ef704bffb142452286fdec45747/images/sql_Analysis.png)

## Tagged

Tagged section is used to save the pre-written query and use it later as per the business requirement.

All the created tags are visible in tagged section.
**Follow the below steps to create TAG:**

Under query section Click **Tag** Button, it will pop up Create query Tag window :

![
](https://raw.githubusercontent.com/sv18042016/fp1/1a7f8565de46814dd5aab91b5cfe32b61e4252e5/images/tag1.png)

**Enter Below Information :**

**Tag Name** Enter tag name

**Connection** displays the connections established for query.

**Query** displays the query established.

**Info** enter query tag information.

 Finally Hit **Create Tag button**.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/1a7f8565de46814dd5aab91b5cfe32b61e4252e5/images/Tag2.png)


- All the created tags are visible in **Tagged Section**.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI2NzA2OTg1MiwxNDc1NTk3NDAwLC04MT
IwMTQ5MjIsLTIwNjUwODM3ODYsMTk0ODQ4ODQ1LDIxMjg1NjM4
NDAsLTE3ODU3MTM1NzYsMTE0NDQxMzI0MCw5MTgxNjgxNzMsLT
ExNjg2NzYwMDEsLTgxNzQ0ODI4MiwtNTEyNTA1MDkxLC0xOTky
MDA1NDEsNTU3ODE3Mjg5LC0xOTQwNDY0MTUxLDQ2MzE5MDk3Ni
wtNzc4MzAxNzMwLC04MTIyNDg0LC0xMDMzMjUwNDE4LC0xNDIy
NzM0ODZdfQ==
-->