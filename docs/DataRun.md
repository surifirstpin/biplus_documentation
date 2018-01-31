

Visualization access the data and allows you to perform data analysis with slice and dice of report information with pictorial representation.

## Selecting Fields from different mapped views

Under visualization section, Select the project and model for which you want to explore the data.

Visualisation sections contains Dimension and measures which acts as fundamental building blocks for a query.

**1.** Select the data fields from the list to create a visualisation.
**2.** Click on Run Button.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/visu_run.png)

## Search option for getting fields

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

## Row Limitation and Runtime display

Using Bi+ you can limit the display of field values by using Limit option and check the Query runtime as shown in the image below;
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/row_limit.png)

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



## Global Sorting (Ascending / Descending)
Using BI+ you can perform sortin
         Order to view the data in ascending or descending order.

## Local Sorting

                  welcome to biplus

## Hidden filter option

                  welcome to biplus

## Filed Visualization On / Off

                  welcome to biplus

## Number Format & Currency option for Fields

                  welcome to biplus

## Group aggregate option

                  welcome to biplus

## Format based on Logic

                  welcome to biplus

## Row Grouping

                  welcome to biplus

## Pivot table


                welcome to biplus
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTExMDI4ODY1LC04MzA5ODE4NV19
-->