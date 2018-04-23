<center><h1>Analysis</h1></center>

Analysis section is  starting point for building the query.  it is designed in such a way, that it retrieves the data in the desired combinations as per your business needs and explores particular subject area it self. It also provides an ability on how to pull the data and how to modify the report and drill down deeper into the report for more insight.
 
**Let see in detail how BiPlus helps you in retrieving data as per your business needs ;**
 
**1.** Click on **Analysis section** and select the desired **Project** and **Model** based on which the data is retrieved.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d2a240b7943427822dbd1280f1555acc64d6800e/images/analysis.png)


## Add Dimension and Measure

A **Dimension** is a group of data and **Measure** is a information about group of data and they collectively acts as fundamental building blocks for a query.

> For Example **Name of the Employee** is defined as dimension and **Salary of the Employee** is defined as Measure.
 
 To retrieve the data in analysis section follow the below steps,
 
**2.**  Select one or more dimension fields ( Grey fields) to access the data. It supports strings and date types.

**3.** Select one or more measure fields (Orange fields) to access numeric values, such as Sum, Count, Max, Min and  Avg etc. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/fc61997d3a6999b632b7b6e9dfdfdcd3f93b5507/images/analysis1.png)
                                                                                                                                                                                                                        
## Filters 

Filters removes all the data except the one you want to retrieve. filter expressions are the advanced way to limit the data and it is a optional list of filter expression applied to measure calculation, the following are the various types of filter expressions used.

| Type | Description |
|--|--|
| String | For fields that contain letters or special characters |
|Numbers|For fields that contain numbers|
|Date|For fields that contain dates|
|Lookup| To view the lookup in Report filters it should be derived under lookup field in model section|

Following are the different types of filters characteristics applicable ;

### String :
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

### Integer:

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

### Date :

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

**4.**  Click on **Filter** to apply the filters and extract the data based on filter applied.


![
](https://raw.githubusercontent.com/sv18042016/fp1/451979e37dcbf9fc459308e68773450b4452ed0f/images/filter_analysis.png)

## Hidden Filters

The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are not visible while retrieving the data in data section. To carry out this function you can follow the following steps;

**a.** Apply hidden filters to data fields in dimensions.

**b.** Fields to which hidden filters applied are visible in filter expression of filter section.

**c.** The data is retrieved, based on the applied hidden filters.

![ image 1](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/hidden_filter.png)

**5.**  Click on **Run** to display the data retrieved ( refer image 3).

## Order  (Ascending / Descending)

To view the column data in ascending or descending orders , add the column fields in order section to carry out the sorting on the field values.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/sorting1.png)

## Local Sorting

Local Sorting can be applied directly to the data obtained for dimension and measure fields in the data section. Click on the desired field header to enable sorting.

For **Dimensions**

- Click on upper arrow to enable  ascending order.
- Click on down arrow to enable descending order.  

For **Measures**

- Click on upper arrow to enable  descending order.
- Click on down arrow to enable ascending order.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/local_sorting.png)


## Query Time

**6.** Total time taken to build the query of a report.

## Display number of rows

**7.** Number of rows fetched while retrieving data.


## Display Totals

**8.**  By selecting the **check box** it displays the total values of the measure fields obtained.

 ## Display  Row Limit

**9.**  You can limit the rows extracted to 100, 500, 1000, 5000, etc selecting the limit value to your desired number from drop down list.                                                          

![
](https://raw.githubusercontent.com/sv18042016/fp1/61de99f8d763cf180029d192cc9b991ed454a35a/images/query_time.png)

## Pivot table

Multiple dimensions in the report data are often easier to look at, when you pivot one of the dimensions horizontally and display group based data for the field to which pivot is applied. Each value in the dimension will become a column in your report data by making your information more clear to consume visually, and reduces the need to scroll down to find data.

To **Pivot** a dimension click on pivot for dimension before or after running the query, you can add more pivots to other dimension but make sure you have at least one un-pivoted dimension and a measure value.

>For instance, if you want to view the number of order received  based on the month  it displays in following way:

| Order Received  |year  |month|Region|Name|
|--|--|--|--|--|
| 100 |2000  |January|north|john|
|200|2001|February|south|Steve|
|300|2002 |march|east|Bob|
|400|2003|April|west|Mecker|

>On Applying pivot on month, it displays;
  
  |January|February|March|April|
  |--|--|--|--|
|100|200|300|400|
|2000|2001|2002|2003|
|North|south|east|west|
|john|steve|bob|Mecker|

 You can apply pivot to fields in 2 ways ;
 
**a.** Apply pivot **After Retrieving** the data by selecting the pivot in drop down of the field.
 
**b.** Apply pivot **Before Retrieving** the data while selecting the fields by clicking on pivot icon.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/0bc648227810e628f97baa8e8ade9bdeb782ca04/images/pivot.png)

## Pin or Remove Pin

To freeze the column field values while scrolling the data to right or left, click on **Pin** in field drop down provided and to release the same click on **Remove Pin.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/83983da3cd4f0b19f0ed84550fc2151b0619fc36/images/pin.png)

## Group / Un-Group

By selecting group option for fields you can group the data and display the consolidated value of the field. To carry out this function click on **Group** in field drop down provided and to release the same click on **Un-Group**. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/group.png)

The below image shows , the consolidated values after grouping is applied on fields.

![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/after_grouping.png)

## Multi-Level grouping

**Using AcuBi you can apply Multi-level grouping to the data extracted. consider the below example for more details description on multi level grouping.**

> **For instance** : in the below image grouping has been applied to 2 dimension fields Country Name and  State Name. In retrieved data on expanding Country Name it displays the perspective State Names that fall under specific country and on Further Expansion it displays City Names that fall under the specific state  as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/a07734d0424a3c19e040fdd95a93464d057df5f3/images/multi_level_grouping.png) 



## Find

To find the specific field value from the data extracted click on **Find** in the  field drop down.

![
](https://raw.githubusercontent.com/sv18042016/fp1/0c61b3a711f6de1821fa63350eaa8f2e11e84486/images/find.png)

## Field Visualization On / Off

To hide the specific field in the visualization charts click on **Hide Visualization** in the drop down of field  and to display the same click on **Show visualization**

![
](https://raw.githubusercontent.com/sv18042016/fp1/75f9c50ef12a1aa2ff5c43aaafefa2fd1140597d/images/hide_visualisation.png)

## Remove

To remove a specific field column from the extracted list click on **Remove** in drop down list of the field.

## Calculated column 

Table calculations enable you to easily create on-the-fly metrics, which are similar to formulas found in Excel sheets. These extracted columns will show up as green in the data table. Using calculated column you can perform mathematical, logical (true/false), lexical (text-based), and date-based calculations on the dimensions, measures, and other table calculations in your query. 

Click on **Calculated column** button to enable table calculations as shown in below image,

![
](https://raw.githubusercontent.com/sv18042016/fp1/9dd01207f083d272ba2269a4c999dfa8976f1914/images/calculate%20column1.png)

- **Field name** unique identifier name to refer calculated column.
- **Label** labeling the calculated column.

- **Data type** data type used (string,number).

- **Field type** derives dimension or measure.

- **Calculation** derive arithmetical & logical expressions.

- **Calculate on the raw data** this function is applied directly on the retrieved value of the fields, initially before pivot or grouping options are applied.

![
](https://raw.githubusercontent.com/sv18042016/fp1/f9a2efaca57be8f52d3ff9d6c02291f6be8b2b70/images/calculate%20_expression.png)

- **Run** the report after deriving the calculation all the values based on calculation is shown up in green colour as shown in below image,


![
](https://raw.githubusercontent.com/sv18042016/fp1/394d53042fd86efdc7a2f16a79e69b6434c9260f/images/calcu+result.png)

## Data 

Data section under visualization is enabled based on the data retrieved for fields. Below are the parameters applicable on the data retrieved.

- **Row Grouping** enables row grouping for fields values based on the field selected as shown in the below image.

- **Explore Enabled** to explore the data which are grouped select the check box **Explore Enabled.**

- **Stacked** Series values are added on the y-axis, so each consecutive series appears above the last. Be sure that the units of all series match.

- **Datasets** this section enables you to perform alignment, set currency formats, group aggregates ( Sum, Avg, Max, Min, Count ) on the consolidated values of the field.

- **Legend** it will enable you to change the label for measure value in visualization charts as shown below.

![
](https://raw.githubusercontent.com/sv18042016/fp1/49bb2a07efd42d5b6f9a7f648e8f705e5f63bc4d/images/legend_label.png)

##  Format

  - **Format** enables different type of number format to the measure field value. Following are the list of number formats supported by AcuBi ;

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


- **Currency** you can check the field values of the measure by applying different types of currency formats, AcuBi supports $,   ₹  ,   €  ,  £.

![
](!%5B%20%5D%28https://raw.githubusercontent.com/sv18042016/fp1/e1bd201419a03bfb1375b64b9e74fb8e06830061/images/data_section_analysis.png%29)

## SQL Query 

To view the SQL query built  in analysis section click on **SQL** section.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA1MTQ0NDYwOCw0MzYxMjg4MzYsLTk5MT
UyNjQ2MiwtMTkxMjg4NDQ3OCw0Mjk2NDQ0MDEsMjEzODM4NTcw
MF19
-->