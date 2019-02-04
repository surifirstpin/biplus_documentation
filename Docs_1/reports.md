
<center><h1> Analysis </h1></center>

Analysis section describes how to retrieves the data in the desired combinations as per your business needs and how to explore particular subject area it self. It has an ability on how to pull the data and modify the report as per the needs and drill down deeper into the report for more better insights across the report.

 To create a report, Click on **Analyse Section.**

**1.**  All the connection established, databases and tables used for the Reports are defined under **Project.** Depending on your business requirement you can choose appropriate project.

**For Example :** If you want to create a project based on oracle connection select project **Oracle_Techdoc** from drop down list.

**2.** Model Section has different set of models developed  for Orders, Customers, Delivery, Employees, Kitchen Process and Products.

**For Example:** to create a report for order based details, Select **Bi_Orders** for model using drop down list. 
 
 **3.** To start with **New Analysis Report** click on **Reset Visualization** ( refresh icon). 

The data in analyse sections is determined by dimensions and measures. Using **Field Picker**, select Dimensions and Measures to retrieve the data. In AcuBi a dimension is derived as group of data and Measure is derived as information about group of data.

 > **Note :** All the dimensions appear in Grey colour and all the measures appear in Orange colour in your data table.

## Getting Started

Let us generate a query to display Stationcode (Dimension) and Order Attendant ID (Dimension) with Quantity Sum. 
After Selecting dimensions and measures **Run** the report to extract the data.
In the following example we have selected **Two Dimensions and One Measure Field.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/5097c9d785e4562444bb51ed2695045c47873f8f/images/full_rep1.png)

**Note :** To hide the Explore /visualize section that displays dimensions and measure click on  **angle double left** icon. to display the explore/visualize section click ** angle double right** icon available near dimensions and measure field list.

## Report Filters

Report filters will narrow the reports results while allowing you to view the specific range of data. 

**The following are the various types of filter expressions used.**

| Type | Description |
|--|--|
| **String** | For fields that contain letters or special characters |
|**Numbers**|For fields that contain numeric
|
|**Date**|For fields that contain dates|
|**Lookup**| To view the lookup in Report filters it should be derived under lookup field in model section|


**Following are the different types of filters characteristics applicable :**

## String 
|			**Example**            |						**Description**                        |                                                                                 
|------------------------------|-----------------------------------------------------------|
|**is not null**                   | should not be equal to null                               |
|**is null**                       | equal to null                                             |
|**is not empty**                  | should not be empty                                       |
|**is empty**                      | should be empty                                           |
|**equal**                         | should be equals to specific value                        |
|**not equal**                     | shouldn't be equal to specific value                      |
|**in**                            | selection based on combination of filter values           |
|**not in**                        | excluding set of values                                   |
|**begins with**                   | finds any value that starts with mentioned sub string      |
|**doesn’t begins with**           | finds a value that doesn't begin with mentioned sub-string|
|**contains**                      | contains mentioned sub-string                             |
|**doesn’t contain**               | finds a value which does not contain mentioned sub-string |
|**ends with**                     | should end with mentioned sub-string                      |
|**doesn’t end with**              | should not end with mentioned sub-string                  |

## Integer

|			**Example**            |						**Description**                         |                                                                                 
|------------------------------|------------------------------------------------------------|
|**is not null**                   | should not be equal to null value                          |                
|**is null**                       | should be equal to null value                              |                                           
|**not empty**                     | data is not empty                                          |
|**is empty**                      | data is empty                                              |
|**equal**                         | data equal to specified value                              |
|**not equal**                     | data not equal to specified value                          |
|**in**                            | data equal to specified values                             |
|**not in**                        | data not equal to specified values                         |
|**less**                          | data less than specified value                             |
|**less or equal**                 | data less than or equal to specified value                 |
|**greater**                       | data greater than specified value                          |
|**greater or equal**              | data greater than or equal to specified value              |
|**between**                       | data in between the specified range                        |
|**not between**                   | data not in between the specified range                    |

## Date 

|			Example            |						Description                         |                                                                                 
|------------------------------|------------------------------------------------------------|
|**timeline**                      |data from specific time scale                               |
|**equal**                         |data from specific date                                     |
|**not equal**                     |data excluding from specific date
|**between**                       |data in between the specified dates
|**not between**                   |excluding the data between the specified range
|**less or equal**                 |data up to specified date 
|**greater or equal**              |data from the specified date 
|**is not null**                   |data which is not equal to null
|**is null**                       |data which is equal to null

> **Note :** To view the **Timeline Filters** in details please go to Timeline filters document.


**4.** The report data is retrieved based on **filter** applied. all the fields selected are visible in filter expression list using which you can apply filters.

> **For Example :** Apply filter expression to measure field **Quantity sum is greater than or equal to 10000** in filter section and data is retrieved on based on the filters applied.

**Run** the report after applying the filters  to extract the data, based on selection made.

> **Note :**  Data retrieved on running a report, is visible in  **Data section**

**5.** Similarly, we can apply **Hidden Filters** to the report data. The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are hidden in data section.

![
](https://raw.githubusercontent.com/sv18042016/fp1/603d0055942c97790066aa8195ad659038778ad2/images/hidden_filter.png)


**6.** To Add more filters click on **Add Rule**.

**7.** To Delete the filter applied Click **Ban Icon** as shown in the image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b0f6dc49657c9a5d48f6810415f48efbe047dc36/images/full_filters.png)

## Order (Ascending / Descending)

**8.** To view the column data in ascending or descending orders, click on  **Order**  and add the column fields in order section.
         **a.** To add more sorting orders to a report click **Add Order**.
         **b.** To delete, sorting for fields click **Ban Icon.**

**9.** To hide the **Filter** or **Order** sections, click on angle-double-up icon on to far right of the order section. To un-hide the same click on angle-double-down icon.

## Local Sorting

**10.** Sorting can also be applied after data is retrieved in data section, you can simply click on desired field header to enable sorting.

For  **Dimensions**

-   Click on upper arrow to enable ascending order.
-   Click on down arrow to enable descending order.

For  **Measures** use opposite direction.

-   Click on upper arrow to enable descending order.
-   Click on down arrow to enable ascending order.

![
](https://raw.githubusercontent.com/sv18042016/fp1/0c40bcaa8d70982ecbd36c04499e478e0ad2042f/images/full_sort.png)


**11.** The total time taken to build a query for a report is displayed at top of the report screen.

**12.** The total number of rows fetched displayed just below that.
  
**13.**  Select the  **check box** for totals, to display total sum values of the measure fields.

**14.**  You can **limit** the rows to 100, 500, 1000, 5000, etc using given drop down list.

## Pivot

Multiple dimensions in a report data are often easier to look at, when you pivot one of the dimensions horizontally and display group based data for the field to which pivot is applied. To **Pivot** a dimension click pivot for a dimension field.

**Pivot can be applied in 2 ways :**
 
**a.** Apply pivot **After Retrieving** the data by selecting the pivot option using field header drop down.
 
**b.** You can also apply pivot **Before Retrieving** the data, just click on pivot icon during field selection.

![
](https://raw.githubusercontent.com/sv18042016/fp1/e7d0e669ada7758b57dd89fdaa4442918156255f/images/full%20pivot.png)

> **Note :** incase if you are using more than one pivot, make sure you have at least one un-pivoted dimension and a measure value.

**Pivot Example** : if you want to view quantity sum based on station code then apply pivot for station code (Dimension) as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/f7de77576b380d0f00383c9e9212b895f66d1544/images/pivot_result.png)


## Hide data in pivot 

To hide pivoted data in report output, choose pivot hide first ( hides 1st column data in list) or choose pivot hide last (hides last column data in a list) in data section under datasets.


## Pin or Remove Pin

**15.** To freeze the column field values while scrolling the data to right or left, select **Pin** option in field drop down and to release the same select **Remove Pin.**

## Group / Un-Group

By selecting group option for a field you can display the consolidated value of the field. 

**16.** To carry out this function select  **Group** in field drop down and to release the same select **Un-Group**. 

## Multi-Level grouping

To carry out Multi-level grouping on the data extracted. Select group option for two dimension fields in drop down list. 

> **For Example** : To get it clear on multi grouping, i am adding one more dimension fields **Payment_mode** to the report. Select group option for **Stationcode** and **Order_attendant_ID.** Now on expanding Stationcode_2, it displays corresponding **Order_attendant_ID** on further expanding, it displays the **payment mode** for the records as shown in the image below.

![
](https://raw.githubusercontent.com/sv18042016/fp1/883d9bf88b00686fda140fdb1538ed72a8ff5ebf/images/multi_group_f.png)


**17.**  To find the specific field value, from the data extracted select **Find** in the field drop down.


**18.**  To hide the specific field in the visualization charts select **Hide Visualization** in the drop down list  and to display the same select **Show visualization.**

**19.**  To remove a specific field column from the extracted list, select **Remove** in drop down list.

![
](https://raw.githubusercontent.com/sv18042016/fp1/276cae284c8c3760cc4056a88b970694ba9d7d39/images/pin_full;.png)

## Calculated column

Calculated column functionality allows you to manipulate the retrieved data, using arithmetical, logical, text-based and date-based functions and then displays it in the required format. 

> **Note :** To understand the total functionality of Calculated column, **"Refer Calculated Column Document".**

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
    
-   **Calculate on raw data**  By enabling the field **Calculate on Raw** the calculation is applied on all the rows irrespective of grouping and pivot settings, if disabled calculation applied on abstract values only.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b10da52fba77e866f8f30ae57fabe5c0d0f8c142/images/ful_calculated.png)

 Click **ok** after deriving the expression, all the values based on calculation is shown up in green colour as shown in below image,

![
](https://raw.githubusercontent.com/sv18042016/fp1/d04e6cf056ed45cc004f6c0efcf0ceef32db9388/images/ful_calculated2.png)

## Data 

Data section under visualization is enabled based on the data retrieved on running a report.

 **Below are the parameters applicable on the data retrieved;**

- **Row Grouping** enables row grouping for field values based on the field selected as shown in the below image.

- **Explore Enabled** to explore the data which are grouped select the check box **Explore Enabled.**

- **Stacked** Series values are added on the y-axis, so each consecutive series appears above the last. Be sure that the units of all series match.

- **Datasets** this section enables you to perform alignment, set currency formats, group aggregates ( Sum, Avg, Max, Min, Count ) on the consolidated values of the field.

- **Legend** it will enable you to change the label for measure value in visualization charts as shown below.

##  Format

 **Format** enables different type of number format to measure a field value. Following are the list of number formats supported by AcuBi:

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
|  ###,###.00 | Number with comma between hundreds and two decimal(123,456.00) |
|  ###,###.000 | Number with comma between hundreds and three decimal(123,456.000) |
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


- **Currency** AcuBi supports following currency formats $,   ₹  ,   €  ,  £.

![
](https://raw.githubusercontent.com/sv18042016/fp1/2300d0f85947e474f369d3b074655040658bd753/images/full_datasection.png)

## SQL Query 

To view the SQL query built on retrieving data in report, click on **SQL** section.

![
](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA3NzAzOTExLDk4MTA0MDA0MiwyMDc3MD
M5MTEsMjA3NzAzOTExLC0xMjczMDI4MDksOTgxNTEzMzE5LC0x
ODA0NzE4NTEwLDE5ODAzNDI2NjYsMTQwMTcyNzMwNiw3MTYxOD
AyOTgsMTI4NTk1MjA1MSwtMjA3NTkzNzk3NV19
-->