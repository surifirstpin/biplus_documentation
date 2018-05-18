
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

 **You can apply pivot to fields in 2 ways :**
 
**a.** Apply pivot **After Retrieving** the data by selecting the pivot in drop down of the field.
 
**b.** Apply pivot **Before Retrieving** the data while selecting the fields by clicking on pivot icon.

![
](https://raw.githubusercontent.com/sv18042016/fp1/e7d0e669ada7758b57dd89fdaa4442918156255f/images/full%20pivot.png)

> **Note :** you can add more pivots to other dimension fields but make sure you have at least one un-pivoted dimension and a measure value.

**For Example** : if you want to view quantity sum based on station code then apply pivot for station code (Dimension).

![
](https://raw.githubusercontent.com/sv18042016/fp1/f7de77576b380d0f00383c9e9212b895f66d1544/images/pivot_result.png)


## Pin or Remove Pin

**15.** To freeze the column field values while scrolling the data to right or left, click on **Pin** in field drop down provided and to release the same click on **Remove Pin.**

## Group / Un-Group

By selecting group option for fields you can group the data and display the consolidated value of the field. 

**16.** To carry out this function click on **Group** in field drop down provided and to release the same click on **Un-Group**. 

## Multi-Level grouping

To carry out Multi-level grouping on the data extracted. Select group option for 2 dimension fields in field drop down list. 

> For Example : To get it clear on multi grouping, i am adding one more dimension fields **Payment_mode** to report  for better understanding. Apply group option to **Stationcode** and **Order_attendant_ID.** Now on expanding Stationcode_2 which, it displays corresponding Order_attendant_ID on further expanding it, displays the payment mode for the records.

![
](https://raw.githubusercontent.com/sv18042016/fp1/883d9bf88b00686fda140fdb1538ed72a8ff5ebf/images/multi_group_f.png)


**17.**  To find the specific field value from the data extracted click on **Find** in the  field drop down.


**18.**  To hide the specific field in the visualization charts click on **Hide Visualization** in the drop down of field  and to display the same click on **Show visualization**.

**19.**  To remove a specific field column from the extracted list click on **Remove** in drop down list of the field.

![
](https://raw.githubusercontent.com/sv18042016/fp1/276cae284c8c3760cc4056a88b970694ba9d7d39/images/pin_full;.png)

## Calculated column

Calculated column is a functionality that allows to manipulate the retrieved data using arithmetical, logical, text-based and date-based functions and then displays it in the required format. the data extracted using calculated column will show up in green colour in the data table. Just like regular dimensions and measures, calculated columns are controlled from display in visualizations.

> **Note :** To understand the total functionality of Calculated column, **Refer Calculated Column document.**

Click on  **Calculated column**  button to enable table calculations as shown in below image,

![
](https://raw.githubusercontent.com/sv18042016/fp1/3fb590c409cd0e47262a69c18bbde38f424ca714/images/calculated_col.png)

> **Note :** in the below example we are multiplying measure field quantity_sum by 2.

After navigating to calculated column, enter below fields;

-   **Field name**  unique identifier name to refer calculated column.
    
-   **Label**  labeling the calculated column.
    
-   **Data type**  data type used (string,number).
    
-   **Field type**  derives dimension or measure.
    
-   **Calculation**  derive arithmetical & logical expressions.
    
-   **Calculate on the raw data**  this function is applied directly on the retrieved value of the fields, initially before pivot or grouping options are applied.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b10da52fba77e866f8f30ae57fabe5c0d0f8c142/images/ful_calculated.png)

 Click **ok** after deriving the expression,  all the values based on calculation is shown up in green colour as shown in below image,

![
](https://raw.githubusercontent.com/sv18042016/fp1/d04e6cf056ed45cc004f6c0efcf0ceef32db9388/images/ful_calculated2.png)

## Data 

Data section under visualization is enabled based on the data retrieved for fields.

 **Below are the parameters applicable on the data retrieved;**

- **Row Grouping** enables row grouping for fields values based on the field selected as shown in the below image.

- **Explore Enabled** to explore the data which are grouped select the check box **Explore Enabled.**

- **Stacked** Series values are added on the y-axis, so each consecutive series appears above the last. Be sure that the units of all series match.

- **Datasets** this section enables you to perform alignment, set currency formats, group aggregates ( Sum, Avg, Max, Min, Count ) on the consolidated values of the field.

- **Legend** it will enable you to change the label for measure value in visualization charts as shown below.


##  Format

 **Format** enables different type of number format to the measure field value. Following are the list of number formats supported by BiPlus :

|  Example | Description |
|  ------ | :------ |
|  #  | Number(1234) |
|  #.0  | Number with exactly one decimal(1234.0) |
|  #.00  | Number with exactly two decimal(1234.00) |
|  #.000 | Number with exactly three decimal(1234.000) |
|  #,##0 | Number with comma between thousands(1,234) |
|  #,##0.0 | Number with comma between thousands with and one decimal(1,234.0) |
|  #,##0.00 | Number with comma between thousands and two decimal(1,234.00) |
|  #,##0.000 | Number with comma between thousands and three decimal(1,234.000) |
|  ###,###.0 | Number with comma between hundreds and one decimal(123,456.0) |
|  ###,###.00 | Number with comma between hunderds and two decimal(123,456.00) |
|  ###,###.000 | Number with comma between hunderds and three decimal(123,456.000) |
|  ###.###,0 | Number with dot between hundreds and comma one decimal(123.456,0) |
|  ###.###,00 | Number with dot between hundreds and comma two decimal(123.456,00) |
|  ###.###,000 | Number with dot between hundreds and comma three decimal(123.456,0) |
|  ### ###   | Number with space between hundreds(123 456) |
|  #% | Percent with 0 decimals (1%). Please note multiplication by 100 happens automatically |
|  #.0% | Percent with one decimals (1.0%). Please note multiplication by 100 happens automatically |
|  #.00% | Percent with two decimals (1.00%). Please note multiplication by 100 happens automatically |
|  #.000% | Percent with three decimals (1.000%). Please note multiplication by 100 happens automatically |
|  # k | Number in thousand (1.234 k). Please note division by 1 thousand happens automatically |
|  # M | Number in Millions (0.001234 M).please note division by 1 million happens automatically |
|  *00#  | Number zeropadded to 3 places (001) |
|  *00#.00 | Number zeropadded to 3 places and exactly 2 decimals |
|  $# | Dollar with 0 decimal |
|  $#.00  | Dollar with 2 decimal |
|  $#,##0.00 | Dollars with comma between thousands and 2 decimals ($1,234.00) |


- **Currency** you can check the field values of the measure by applying different types of currency formats, BiPlus supports $,   ₹  ,   €  ,  £.


![
](https://raw.githubusercontent.com/sv18042016/fp1/2300d0f85947e474f369d3b074655040658bd753/images/full_datasection.png)

## SQL Query 

To View the SQL query built on retrieving data in report, click on **SQL** section.

![
](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTkwMjc0ODc1MSwtMTgzNDI5OTgwNiwxMj
UxOTA4MzYxLDUyNTM4MDE4NywxNjUwNTQzMzYzLDEyMTMxNTE3
OTMsLTQ0MTkwNDYwMyw4MDQ5NzY2MjAsNTU4MTQxMjkwLDE3Nz
IzODIzMjIsNzM4MzY1MDA2LC03ODE4NjU0MzAsLTE2ODY1NDk1
MTQsLTExOTQ4OTc4MDcsNzMwMTkyMTcyLC03OTU1MTgxODUsLT
E1NTk4MzQ3NjYsOTU2MzY5MzE0LC02MDE4MzE0NTAsLTkyNzM3
NTM0MF19
-->