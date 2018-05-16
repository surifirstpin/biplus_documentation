
<center><h1>Reports</h1></center>

This Section describes how to retrieves the data in the desired combinations as per your business needs and how to explore particular subject area it self. It has an ability on how to pull the data and modify the report as per the needs and drill down deeper into the report for more better insights across the report.

 To get started with section select **Analyse Section** to start exploring the data.

**1.** All the connection established, databases and tables used for the Reports are defined in **Project**. Depending on your business requirement you can choose project.

**For Example :** If you want to create a project based on oracle connection select the project as **Oracle_Techdoc** from drop down list.

**2.** In Our Model Section we have different type of models developed for Orders, Customers, Delivery Report, Employees, Kitchen Process, Products.

**For Example:** If you want to Analyse about orders, You will probably start Analyzing it by selecting **Bi_Orders** for model using drop down list. 
 
 **3.** To create a new Analysis report click on **Reset Visualization** ( refresh icon). 

The Data in Analyse sections is determined by dimensions and measures. Using Field Picker. Select the dimension and Measures to retrieve the data based on selection. In BiPlus A dimension is derived as group of data and Measures are derived as information about group of data.

 > **Note :** All the dimensions in Biplus appears in Grey colour and all the measures appears in Orange colour in your data table.

## Getting Started

Let us generate a query to displays Stationcode (Dimension) and Order Attendant ID (Dimension) with Quantity Sum for better understanding.

After Selecting dimensions and measures **Run** the report to extract the data.
Here we have selected two dimensions and one measure field in this example.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5097c9d785e4562444bb51ed2695045c47873f8f/images/full_rep1.png)

## Report Filters

Report filters will narrow the reports results while allowing you to view the specific range of data. 

**The following are the various types of filter expressions used.**

| Type | Description |
|--|--|
| String | For fields that contain letters or special characters |
|Numbers|For fields that contain numbers|
|Date|For fields that contain dates|
|Lookup| To view the lookup in Report filters it should be derived under lookup field in model section|

Following are the different types of filters characteristics applicable ;

### String 
|			Example            |						Description                        |                                                                                 
|------------------------------|-----------------------------------------------------------|
|is not null                   | should not be equal to null                               |
|is null                       | equal to null                                             |
|is not empty                  | should not be empty                                       |
|is empty                      | should be empty                                           |
|equal                         | should be equals to specific value                        |
|not equal                     | shouldn't be equal to specific value                      |
|in                            | selection based on combination of filter values           |
|not in                        | excluding set of values                                   |
|begins with                   | finds any value that starts with mentioned substring      |
|doesn’t begins with           | finds a value that doesn't begin with mentioned sub-string|
|Contains                      | contains mentioned sub-string                             |
|doesn’t contain               | finds a value which does not contain mentioned sub-string |
|ends with                     | should end with mentioned sub-string                      |
|doesn’t end with              | should not end with mentioned sub-string                  |

### Integer

|			Example            |						Description                         |                                                                                 
|------------------------------|------------------------------------------------------------|
|is not null                   | should not be equal to null value                          |                
|is null                       | should be equal to null value                              |                                           
|not empty                     | data is not empty                                          |
|is empty                      | data is empty                                              |
|equal                         | data equal to specified value                              |
|not equal                     | data not equal to specified value                          |
|in                            | data equal to specified values                             |
|not in                        | data not equal to specified values                         |
|less                          | data less than specified value                             |
|less or equal                 | data less than or equal to specified value                 |
|greater                       | data greater than specified value                          |
|greater or equal              | data greater than or equal to specified value              |
|between                       | data in between the specified range                        |
|not between                   | data not in between the specified range                    |

### Date 

|			Example            |						Description                         |                                                                                 
|------------------------------|------------------------------------------------------------|
|timeline                      |data from specific time scale                               |
|equal                         |data from specific date                                     |
|not equal                     |data excluding from specific date
|between                       |data in between the specified dates
|not between                   |excluding the data between the specified range
|less or equal                 |data up to specified date 
|greater or equal              |data from the specified date 
|is not null                   |data which is not equal to null
|is null                       |data which is equal to null

> **Note :** To View the **Timeline Filters** in details please go to Timeline filters document.


**4.** The report data is retrieved based on **filter** applied. all the fields selected are visible in filter expression list using which you can apply filters.

> **For Example :** Apply filter expression to measure field **Quantity sum is greater than or equal to 10000** in filter section and data is retrieved on based on the filters applied.

**Run** the report after applying the filters  to extract the data, based on selection made.

> **Note :**  Data retrieved on running a report, is visible in  **Data section**

**5.** Similarly, we can apply **Hidden Filters** to the report data. The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are hidden in data section.

**6.** To Add more filters click on **Add Rule**.

**7.** To Delete the filter applied Click **Ban Icon**.


![
](https://raw.githubusercontent.com/sv18042016/fp1/b0f6dc49657c9a5d48f6810415f48efbe047dc36/images/full_filters.png)

## Order (Ascending / Descending)

**8.** To view the column data in ascending or descending orders , to carry out this function Click On  **Order**  and add the column fields in order section.
 **a.** To add more sorting orders to report click **Add Order**.
 
**b.** To Delete the order sorting for fields click **Ban Icon**.

**9.** To hide the **Filter** or **Order** section Click on angle-double-up icon on to far right of the order section. To unhide click on angle-double-down icon at same location.

## Local Sorting

**10.** Local Sorting can be applied directly to the data obtained for dimension and measure fields in the data section. To enable this Click on the desired field header to enable sorting.

For  **Dimensions**

-   Click on upper arrow to enable ascending order.
-   Click on down arrow to enable descending order.

For  **Measures** its totally opposite in direction.

-   Click on upper arrow to enable descending order.
-   Click on down arrow to enable ascending order.

![
](https://raw.githubusercontent.com/sv18042016/fp1/0c40bcaa8d70982ecbd36c04499e478e0ad2042f/images/full_sort.png)


**11.** The total query time taken to build the query of a report is displayed at top of the report screen.

**12.**  Number of rows fetched while retrieving data is displayed  at top of the report screen.

**13.**  By selecting the  **check box** for totals, the report is displayed with total sum values of the measure fields obtained.

**14.**  You can limit the rows extracted to 100, 500, 1000, 5000, etc. By selecting the limit value to your desired number from drop down list.

## Pivot

Multiple dimensions in the report data are often easier to look at, when you pivot one of the dimensions horizontally and display group based data for the field to which pivot is applied. To **Pivot** a dimension click on pivot for dimension before or after running the query.
> **Note :** you can add more pivots to other dimension fields but make sure you have at least one un-pivoted dimension and a measure value.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc5NTUxODE4NSwtMTU1OTgzNDc2Niw5NT
YzNjkzMTQsLTYwMTgzMTQ1MCwtOTI3Mzc1MzQwXX0=
-->