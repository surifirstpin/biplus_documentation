<center><h1>Analysis</h1></center>

Analysis is the starting point for building the query, it is designed in such a way that it retrieves the data in the desired combinations as per your business needs and explores particular subject area it self. It provides an ability on how to pull the data and how to modify the report and drill down deeper into the report for more insight.
 
**Let see in detail how Acubi helps you in retrieving data as per your business needs ;**
 
**1.** Click on **Analysis section** and select the desired **project** and **model** depending on which you can explore and retrieve the data.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d2a240b7943427822dbd1280f1555acc64d6800e/images/analysis.png)


## Adding Dimension and Measure

A **Dimension** is a group of data and **Measure** is a information about group of data and they collectively acts as fundamental building blocks for a query.

> For Example **Name of the Employee** is defined as dimension and **Salary of the Employee** is defined as Measure.
 
 Now let us see how to retrieve the data in analysis section.
 
**2.**  Select one or more dimension fields ( Grey fields) to access the data.

**3.** Select one or more measure fields (Orange fields) to access numeric values, such as Sum, Counts, Max, Avg etc. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/fc61997d3a6999b632b7b6e9dfdfdcd3f93b5507/images/analysis1.png)
                                                                                                                                                                                                                        
## Filters 

Filters removes all the data except the one you want to retrieve. filter expressions are the advanced way to limit the data and it is a optional list of filter expression applied to measure calculation, the following are the  various types on which filters are applied.

| Type | Description |
|--|--|
| String | For fields that contain letters or special characters |
|Numbers|For fields that contain numbers|
|Date|For fields that contain dates|
|Lookup| To view the lookup in Report filters it should be derived under lookup field in model section|

Following are the different types of filters characteristics applicable using **AcuBi ;**

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

The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are not visible while retrieving the data in data section. To carry out this function you can follow the following steps,

**a.** Apply hidden filters to data fields in dimensions.

**b.** Fields to which hidden filters applied are visible in filter expression of filter section.

**c.** The data is retrieved is based on the applied hidden filters.

![ image 1](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/hidden_filter.png)

**5.**  Click on **Run** to display the data retrieved ( refer image 3).

## Calculated column 


Table calculations enable you to easily create on-the-fly metrics, which are similar to formulas found in Excel sheets. These extracted columns will show up as green in the data table. Using calculated column you can perform mathematical, logical (true/false), lexical (text-based), and date-based calculations on the dimensions, measures, and other table calculations in your query.

Click on Calculated column button to enable table calculations as shown in below image,

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

**Run** the report after deriving calculated column, all the values obtained by applying calculation column is visible in green colour.

> the retrieved data based on mathematical calculation appears in green colour as shown in below image,
> 
![
](https://raw.githubusercontent.com/sv18042016/fp1/394d53042fd86efdc7a2f16a79e69b6434c9260f/images/calcu+result.png)

## Order  (Ascending / Descending)

Perform sorting on data retrieved, to view the data in ascending and descending orders.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/sorting1.png)

## Local Sorting

Local Sorting can be applied directly to the data obtained for dimension and measure fields in the data section. Click on the desired field header to enable sorting.

For **Dimensions**,

- Click on upper arrow to enable  ascending order.
- Click on down arrow to enable descending order.  

For **Measures,**

- Click on upper arrow to enable  descending order.
- Click on down arrow to enable ascending order.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/local_sorting.png)

## Row Limitation and Query Time

**5.** **Totals** display the total for measure value.
 
**6.** **Limit** displays data, based on row limitation.

- **Query time** display the total time taken to build the query of a report.

- **Rows** displays number of rows fetched while retrieving data.

![
](https://raw.githubusercontent.com/sv18042016/fp1/38e6202832d95449080cc72b7361b8ca5cf22b8a/images/query_time.png)

## Pivot table

Multiple dimensions in the report data are often easier to look at when you pivot one of the dimensions horizontally. Each value in the dimension will become a column in your report data by making your information more clear to consume visually, and reduces the need to scroll down to find data.

To **Pivot** a dimension click on pivot for dimension before running the query, you can add more pivots to other dimension but make sure you have at least one un-pivoted dimension and a measure.

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

>In AcuBi **Pivot** checks each dimension horizontally and displays group based data for the field to which pivot is applied.
  
 You can apply pivot to fields in 2 ways;
 
**a.** Apply pivot after retrieving the data directly by clicking on down arrow beside the field header.
 
**b.** Apply pivot while selecting the fields to retrieve the data.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/0bc648227810e628f97baa8e8ade9bdeb782ca04/images/pivot.png)

## Pin or Remove Pin

To Freeze the column field values while scrolling the data to right or left click **Pin** for the dimension option by clicking on down arrow of the field header  to release the same click on **Remove Pin.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/83983da3cd4f0b19f0ed84550fc2151b0619fc36/images/pin.png)

## Group / Un-Group

Group will display the consolidated or a grouped value of the field. To carry out this function Click on the down arrow of the field header and select **Group** to group fields and to release the same Click on **Un-Group** option. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/group.png)

The below image shows , the consolidated values after grouping is applied on fields.
![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/after_grouping.png)

## Multi-Level grouping

Using AcuBi you can view the Multi-level grouped values. 

**Consider the below example for more details description on multi level grouping.**

We have selected Country Name and  State Name and City Name,Total_Employees Sum and Average and apply grouping on Country Name and State Name. In retrieved data on expanding Country Name it displays State Name and on Further Expansion it displays City Name that falls under the states as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/a07734d0424a3c19e040fdd95a93464d057df5f3/images/multi_level_grouping.png) 



## Find

To find the specific field value in the retrieved list select **Find** in the down arrow list of the specific field header.
![
](https://raw.githubusercontent.com/sv18042016/fp1/0c61b3a711f6de1821fa63350eaa8f2e11e84486/images/find.png)

## Field Visualization On / Off

You can hide the field values in  the visualization charts by selecting **Hide Visualization** for the specific field by clicking on the down arrow in the field header. To display the same in visualization chart select **Show visualization**

![
](https://raw.githubusercontent.com/sv18042016/fp1/75f9c50ef12a1aa2ff5c43aaafefa2fd1140597d/images/hide_visualisation.png)

![
](https://raw.githubusercontent.com/sv18042016/fp1/75f9c50ef12a1aa2ff5c43aaafefa2fd1140597d/images/hide_visualisation1.png)

## Data 

Data section under visualization is enabled based on the data retrieved for fields. Below are the parameters applicable on the data retrieved.

- **Row Grouping** enables grouping for column fields based on the field selected.

- **Explore Enabled** to explore the data which are grouped.

- **Stacked** Series values are added on the y-axis, so each consecutive series appears above the last. Be sure that the units of all series match.


- **Datasets** enables you to perform alignment, set currency formats for measure values and calculation column value and perform group aggregates ( Sum, Avg, Max, Min, Count ) on the consolidated values of the field.

![
](https://raw.githubusercontent.com/sv18042016/fp1/8e769a4f2914fa97d5f4672fd4e542ed2f88a246/images/row_grouping.png)

**a.** Enable row grouping by selecting the checkbox.

**b.** Explore the primary column fields data individually, which are grouped under the column field. 

**c.** Select the field on which you want to perform row grouping.

  ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/657b29d2f18b269f2964e8150a3670df8db7869c/images/group_aggregate.png)

- **Legend** displays the measure value to which format, currency, group aggregated are applied.

- **Format** using format option you can apply different type of number format to the measure field value.

| A|B|
|  ------ | ------ |
| #                 |  ###,###.00          |
|  #.00               |  ####,####.000       |
|  #.000              |  ###.###,0           |
|  #,##0              |  ###.###,00          |
|  #,##0.0            |  ###.###,000         |
|   #,##0.00            |  ### ###             |
|   #,##0.00            |  #%                  |
|   #,##0.000           |  #.0%                |
|   ###,###             |  #.00%               |
|   ###,###.0           |  #.000%              |
|   ###,#»#.00          |  #K                  |
|   ###,###.000         |  #M |
|   ###.###,o           |  |

- **Currency** you can check the field values of the measure by applying different types of currency formats, AcuBi supports $,   ₹  ,   €  ,  £.


## SQL Query 

Selected fields will build a SQL query in data analysis :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQxMDc0OTc5OCwtMTkxMjg4NDQ3OCw0Mj
k2NDQ0MDEsMjEzODM4NTcwMF19
-->