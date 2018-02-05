
## Data Analysis

Data Analysis Retrieve the  data  perform data exploration with slice and dice of report information providing pictorial representation.

## Build Query

Under visualization section, Select the project and model for which you want to explore the data.

Visualisation sections contains Dimension and measures which acts as fundamental building blocks for a query.

**1.** Select the data fields from the list to create a visualisation.
**2.** Click on Run Button.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/visu_run.png)

Views contain some set of fields, mostly dimensions and measures and they act as fundamental building blocks for Bi+ queries.
Dimensions are list of fields that can be used for applying filter options, for instance:
- An **Attribute**, which has a direct association to a column in an primary table.
- A **Numerical value**.
- A **Derived value,** computed based on the values of other fields in a single row.

> For example, Dimensions for "Customer" view includes customer name,customer phone number and customer email etc.

A measure is a list of fields that uses a SQL aggregate function, such as COUNT, SUM, AVG, MIN or MAX. any field that is counted based on the values is refereed as measure. Measures can be used to filter grouped values. 

>For example, measures for a “Amount” is Amount_sum, Amount_avg, Amount_min, Amount_max etc.

Using the search option provided in the visualization section you can select the fields for which you want to carryout the field values and apply filter options as shown in below image:

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/visu_fields.png)

## Filters (String , Integer and Date)

Filters is a optional list of filter expression applied to measure calculation,below are the available operations that can be applied for String , Integer and Date.

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

## Hidden Filters

On applying hidden filters the column fields are visible in the list of filter expression specified and displays the data depending on the filters applied.
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/e777906f8a8aafdb323a64c65c2a1c9e69cb01b1/images/hidden_filter.png)


## Order Sorting (Ascending / Descending)

Using BI+ you can perform sorting on data retreived by applying ascending and decending orders.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3a66bec34562013987acc9ca17385d78b2741ac4/images/sorting.png)

## Local Sorting

Sorting can be applied locally to the column field.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/c6f7269afe640dd6c16f4fd1d4423aa394bdf2b4/images/local_sorting.png)

## Row Limitation and Query Time

Using Bi+ you can limit the display of field values by using **Limit** option and check the **Query run-time** as shown in the image below ;

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/row_limit.png)

## Pivot table

-   Pivot  checks each dimension horizontally and reduces the effect of scrolling down the data.
  
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/78c46d819c716135d45ff60b9a71b15dd9e7a97f/images/pivot.png)

- You can directly apply pivot option in data output field by selecting **pivot** option from drop down.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/1bae129344332eabae71b594bd320f0f5c5b4a68/images/pivot2.png)

## Row Grouping

Using Bi+ you can group the rows of the fields by selection **group** options from the drop down. 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/12c2bc69fcf082dc620f2819ae901ae9c7a962a7/images/group.png)

## Pin or Remove Pin

To freeze the field values click on ** Pin** options in drop down and click on **Remove Pin** to release it.
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/b001b2f2f386a9730f3be339c38c54b73c69c5b9/images/pin.png)

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/f14d690d76bb1f0feacaf24259f67d1b9b55ea52/images/unpin.png)

## Field Visualization On / Off

 To hide field values click on **Hide Visualization** option in the drop down option.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/bee13bc200cda9988be61a3c7b58de502a4915fa/images/hide_visu.png)

## Group aggregate

  it helps you to display the consolidated values to the fields which are grouped.
  **a.** enable row grouping by selecting the checkbox.
  **b.** you can explore the primary column fields data individually, which are grouped under the column field. 
  **c.** Select the field for which you want to perform row grouping.
  
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/657b29d2f18b269f2964e8150a3670df8db7869c/images/group_aggregate.png)

## General 

- **Title**  provides a label or identifier title for chart, align them on any side of the chart. 
- **Padding** sets the spacing in any side of the chart.

## Data 

- **Row Grouping** are used to cluster the field value side-by-side in charts.
- **Explore Enabled**
- **Stacked** are used whether to stack the values at y-axis.
- **Datasets** specifies the alignment,formats,currency,number of y-axis and grouping of aggregates for the legends used in the visualization menu.

## X- Axis functionality

- **Axis type** type of axis used in the charts for instance Indexed is used to refer the numeric values starting from zero,category refer to the field values of the column,timeframe refer to the time-format of the data.
- **Label field** select the field name for which you want to display the field values in x-axis.
- **Show grid** enables grid display for the field values selected. 
- **Axis label** provide label option in x-axis of the chart.
- **Reference Line** allows you to refer specific range of values by applying colours and label to the same.

##  Y- Axis functionality

-**Axis type** refer to type of axis used in charts.
-**Label field** select the field name for which you want to display the field values in Y-axis.
- **Reference Line** allows you to refer specific range of values by applying colours and label to the same.

## Number Format & Currency option for Fields

You can apply different number formats and currency options to measures.
**a.** select the required number format from the list
**b.** select the currency you would like to view

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/a289a74e21b8055ac795aa2bb25d4cb945bc02b0/images/number_format.png)

####  list of number formats applicable on measures :

|   Number formats | 
|------------------|
|#                 |        
|#.00              |
|#.000             |
|#,##0             |
|#,##0.0           |
|#,##0.00          |
|#,##0.00          |
|#,##0.000         |
|###,###           |
|###,###.0         |
|###,#»#.00        |
|###,###.000       |
|###.###,o         |
|###,###.00        |
|####,####.000     |
|###.###,0         |
|###.###,00        |
|###.###,000       |
|### ###           |
|#%                |
|#.0%              |  
|#.00%             |
|#.000%            |
|#K                |
|#M                |

####  list of currency applicable on measures :
|    Currency      |
|------------------|
|         $        |
|         ₹        |
|         €        |
|         £        |

## Format based on Logic

Using Bi+ you can add different logic's individually as explained below:
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/959d41865fdc807c1a289904b3e14415443e0cd7/images/logic_format.png)

- **Condition** Select the condition you want to apply on the field.
- **Format on** Select the measure for which you want to set the format.
- **Value** Specify a value to which you want to apply condition. 
- **BG (background colour)** Select the background colour for the data - which is retrieved using condition.
- **Font** Select the font colour for the data retrieved based on condition.
- **Icon** Select a icon for for the data retrieved based on condition.
- **Before number** Align the icon before or after the data.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5NDAxNDU4NV19
-->