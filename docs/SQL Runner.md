
<center><h1>SQL Runner </h1></center>

Using SQL Runner you can directly Access your database and clout that access in variety of ways. In SQL Runner you can easily set up the connection, and navigate the tables under your schema. You can **Run** pre-written SQL queries and also view the query run history. You can create your customs views here and perform useful task with them in model section.  

![
](https://raw.githubusercontent.com/sv18042016/fp1/532dd8b61e94d1e08fe0b89afa6a5961336e8ad2/images/sql_ru.png)

- You can directly write the SQL query from scratch and run it make sure the dialects used in SQL runner should match the database dialects. 

- You can also create SQL query in analysis section. 

- Make use of **History** section to Pre-run the previous query.

## Create SQL Query in SQL Runner

**1.** After logging into AcuBi homepage, Click on SQL Runner section.

**2.**  Type your SQL command in SQL query area.

**3.**  Now **Run** the query.

**4.** The data is retrieved below the query area as shown in the image. SQL runner will load up-to limit 5000 records only.

**5.** Click on **Download** to download the data retrieved.

**6.** After Running the query it displays the **Query Time** taken to run the query and **Number of rows** fetched.

**7.** A maximum **Record limit** of 5000 can be fetched at a time.


![
](https://raw.githubusercontent.com/sv18042016/fp1/ce8e9fc79b080f9de55ebc3627f8c1f071efd6d5/images/sql_runner.png)



## Create SQL Query in Analysis

You can make use of **Analysis Section** to create a query.

- Select the text from SQL area in Analysis and copy it SQL Runner.

- Once the Text is added to SQL area in SQL Runner, **Run** the SQL Runner to Query the database. You can also customize the text as per your business needs and run the new query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5b49497f917e7ef704bffb142452286fdec45747/images/sql_Analysis.png)


## SQl Runner History

You have an ability to view all the recent history of all the queries, which have been run in SQL Runner.

To View the recent history, click on History tab available at the top right of the SQL query area. history section displays all the query run on SQL runner. Green colour indicates successfully query and Red colour indicates query that did not run successfully due to the error.  

Click on **Run Query** in history section, to re-run the previous query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5c48d711bf5f6b900a47397cc60d54a507bf0b2b/images/sql_history.png)

## Sorting Query Result

In your query result you can view the data in ascending or descending order by applying sorting. To enable sorting Click on column header, to reverse the sorting order click on column header for second time.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5f2f6b7d5ed9daf4222fd8da2636ecabbe2cabcd/images/sort_sql.png)


## Derived View

SQL Runner can create a derived view from the query build at the same time you can use this view in model section. the dialects used for creating a derived view should be same as in SQL runner.

To get started with derived view, Click on List icon and Select Create Derived View.

![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/derived%201.png)

**Enter the below fields ;**

- **Derived View Name** Enter Label for identification to the new derived view.

- **Projects** Select the dialects using the drop down button.
 
- **Query** the query created in sql runner will be added here.
 
 -  **Field List** On selecting the dialects all the fields used in query are reflected here.
 Click on Create, to create the New Custom view. 
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/custom_view.png)

To view the newly created derived view. Goto Model section under the views list as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/model_derived_view.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk3ODgyMDczMCw3NTkzMjg5NDYsLTQ0OD
E0NjA5NiwxOTEzMDE5NDc0XX0=
-->