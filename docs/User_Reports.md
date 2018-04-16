 BiPlus Reports displays the retrieved the data in the desired combinations as per your business needs and explores particular subject area it self. It provides an ability on how to pull the data and how to modify the report and drill down deeper into the report for more insight.

## Getting Started

Use this link http://52.29.248.194:8081/biplus in your url and Click on enter, it will navigate to BiPlus login page. 

-  In this page enter **Username** and **Password** then click on **login** to navigate to BiPlus Homepage. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/master/images/biplus_login.png)
Image 1 :

> **Note :** BiPlus Home page immediately displays the dashboard or Report set by other users on homepage ( Shown in Below image).

**1.** Click on **Analyse section** to explore a report.

**2.** Select Desired **project** and **model** from the drop down list, depending on which you want to extract the data.

**3.**  Select one or more **dimension fields** ( Grey fields) to access and group your data.

**4.** Select one or more **measure fields** (Orange fields) to add information about those groups or data such as Sum, Count, Max, Min and  Avg etc. 

**5.** To retrieve the data based on filters applied , add a **filter** to your report based on that field.
 
 > **Note :**  The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are not visible while retrieving the data in data section. 

 **6.** Click **Run** to extract the data, based on selection made.

>  **Note :** Data retrieved on running the report are visible in **Data section**( Refer image 2).

 ![
](https://raw.githubusercontent.com/sv18042016/fp1/62c6ac77c1e3a30e83c0718fefd7fd88ae35a203/images/data_retreived_ur.png)Image 2

All the mathematical and logical calculation are carried out in a report using Calculated column

Click on **Calculated column** button to enable table calculations as shown in below image,

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

## Order  (Ascending / Descending)

To view the column data in ascending or descending orders , add the column fields in order section to carry out the sorting on the field values.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/sorting1.png)

## Local Sorting

Local Sorting can be applied directly to the data fetched in the data section. Click on the desired field header to enable sorting.

For **Dimensions**

- Click on upper arrow to enable  ascending order.
- Click on down arrow to enable descending order.  

For **Measures**

- Click on upper arrow to enable  descending order.
- Click on down arrow to enable ascending order.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/local_sorting.png)

## Display Totals

 By selecting the **display** check box, it displays total value of the measure field.

 ## Display  Row Limit

  You can limit the rows extracted to 100, 500, 1000, 5000, etc selecting the limit value to your desired number from drop down list.                                                          

![
]

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

you can view the consolidated value of the field by applying values By selecting group option for fields you can group the data and display the consolidated value of the field. To carry out this function click on **Group** in field drop down provided and to release the same click on **Un-Group**. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/group.png)

The below image shows , the consolidated values after grouping is applied on fields.

![
](https://raw.githubusercontent.com/sv18042016/fp1/93c8d204507e325aea691be5e8a6e7662975fd3c/images/after_grouping.png)

## Multi-Level grouping

Using AcuBi you can apply Multi-level grouping to the data extracted. consider the below example for more details description on multi level grouping.

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
eyJoaXN0b3J5IjpbNTU1MjA5MjgzLDU3NDc0MzI3NSw0NzEyND
IxNjYsMTg3Njc3NTkwNywxOTQ3MjgzNTQ5LC01NzUyMDA1NjQs
LTEwODAzMTM2NDIsLTU4Njk3NDIxNiwtMTk5NzcxODg0NiwtNT
QwODY4MzEsNjM0OTQ1OTgxLDE5NDk3MTQ0NzUsLTExODc2NTM1
MTMsLTkxNDY3NDQ4NywyMTQ3MTcwOTA4LDI5NDY1NTE0NiwxMz
g1MjE0Mzc2LDk0NDI3NTA5OCwxNDY4NTcyOTgwLC03NjA0MTcx
MThdfQ==
-->