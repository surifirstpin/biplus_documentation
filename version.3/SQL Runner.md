
<center><h1>SQL Runner </h1></center>

Using SQL Runner, you can directly access the database and clout it in variety of ways. In SQL Runner you can easily set up the connection, and navigate the tables under your schema. **Run** pre-written SQL queries and view the query run history. at the same time create your customs views here and perform useful task with them in model section.  

![
](https://raw.githubusercontent.com/sv18042016/fp1/532dd8b61e94d1e08fe0b89afa6a5961336e8ad2/images/sql_ru.png)

**There two ways to create sql queries in AcuBi.**

- In AcuBi you can directly write the SQL query from scratch and run the same, make sure the dialects used in SQL runner should match the database dialects. 

- Create SQL query using analysis section. 

- Make use of **History** section to pre-run the previous query.

## Create SQL Query in SQL Runner

**1.** After logging into AcuBi, Click SQL Runner section.

**2.**  Type your SQL command in SQL query area.

**3.**  Now **Run** the query.

**4.** The data retrieved below the query area as shown in the image. SQL runner will load up-to limit 5000 records only.

**5.** Click **Download** to download the data retrieved.

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


## SQL Runner History

You have an ability to view all the recent history of all the queries, which have been run in SQL Runner.

To view the recent history, click on history tab available at the top right of the SQL query area. history section displays all the query run on SQL runner. Green colour indicates query is successful and Red colour indicates unsuccessful query due to the error.  

Click on **Run Query** in history section, to re-run the previous query.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5c48d711bf5f6b900a47397cc60d54a507bf0b2b/images/sql_history.png)

## Sorting Query Result

In your query result you can view the data in ascending or descending order by applying sorting. To enable sorting click on column header, to reverse the sorting order click on column header for second time.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5f2f6b7d5ed9daf4222fd8da2636ecabbe2cabcd/images/sort_sql.png)


## Derived View

SQL Runner can create a derived view from the query build at the same time you can use this view in model section. the dialects used for creating a derived view should be same as in SQL runner.

To get started with derived view, Click on list icon and select create Derived View.

![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/derived%201.png)

**Enter the below fields :**

- **Derived View Name** Enter Label for identification of new derived view.

- **Projects** Select the dialects using the drop down button.
 
- **Query** the query created in sql runner will be added here.
 
 -  **Field List** On selecting the dialects all the fields used in query are reflected here.
 
 -  Click  on **Create,** to create a new custom view. 
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/custom_view.png)

To view the newly created derived view. Navigate to Model section under the view list as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/51255d3dbab14ac3607ff6091c095452be43d238/images/model_derived_view.png)

## Tagged

Tagged section is used to save the pre-written query and use it later as per the business requirement.

All the created tags are visible in tagged section.
**Follow the below steps to create TAG:**

Under query section Click **Tag** Button, it will pop up create query Tag window :

![
](https://raw.githubusercontent.com/sv18042016/fp1/1a7f8565de46814dd5aab91b5cfe32b61e4252e5/images/tag1.png)

**Enter Below Information :**

**Tag Name** Enter tag name

**Connection** displays the connections established for query.

**Query** displays the query established.

**Info** enter query tag information.

  Hit **Create Tag button**.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/1a7f8565de46814dd5aab91b5cfe32b61e4252e5/images/Tag2.png)

- All the created tags are visible under **Tagged Section.**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NjQ0MzUwOTgsLTYzNTIxNTY3OCw4OD
cxMDI2NDMsLTEzNjQzMDY3OTcsLTE2NDEzMDE2MTMsMTM4NDYx
MDAxMSw4MTcxMTMzOSwtMTY0MTQ4NDE3MywtMzE1Mjc4MDcsND
g1NjUzNTk0LDE5Nzg4MjA3MzAsNzU5MzI4OTQ2LC00NDgxNDYw
OTYsMTkxMzAxOTQ3NCw0MTkwNDAwNzcsLTY4MzI3OTAzOCwtMT
A4ODMyMzM5MywxODE0MTQyNzcyLDE0NjQxODYyMTEsMTg4Mzk1
NzMxOV19
-->