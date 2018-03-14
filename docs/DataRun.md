<center><h1>Analysis</h1></center>

USiAnalysis section helps in retrieving the data in the desired combinations by allowing slice and dice of the data information, AcuBi provides you an ability to explore the data by applying following functions Filters, Order, Sorting, Mathematical Calculations etc.
 
**Let see in detail how Acubi helps you in retrieving data as per your business needs ;**
 
Under data analysis section, select the desired **project** and **model** ( refer image 1) depending on which you can explore and retrieve the data. Analysis section contains list of dimension and measures which acts as fundamental building blocks for a query.

## Adding Dimension and Measure

Select set of fields, from dimension ( Grey fields) or measure (Orange fields) to build a query.

**1.**  Select one or more dimension fields to access the data.

**2.** Select one or more measure fields to access numeric values, such as totals and counts. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/2747be6cc024840c73a089a67c7f9f9be6419617/images/analysis_img1.png)
                                                                                                                                                                                                                        
## Filters 

Filters removes all the data except the one you want to retrieve. Filter expressions are the advanced way to limit the data and it is a optional list of filter expression applied to measure calculation, the following are the  various types on which filters are applied.

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

**3.**  Click on **Filter** to apply the filters and extract the data based on filter applied.

![
](https://raw.githubusercontent.com/sv18042016/fp1/c07023b25efd621ec0d7af513f4231d71cbfd0a3/images/analysis_filters.png)
## Hidden Filters

The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are not visible while retrieving the data in data section. To carry out this function you can follow the following steps,

**a.** Apply hidden filters to data fields in dimensions.

**b.** Fields to which hidden filters applied are visible in filter expression of filter section.

**c.** The data is retrieved is based on the applied hidden filters.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/hidden_filter.png)

**4.**  Click on **Run** to display the data retrieved ( refer image 1).

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


- **Query time** display the total time taken to build the query of a report.

- **Rows** displays number of rows fetched while retrieving data.

5. **Totals** display the total for measure value.
 
6. **Limit** displays data, based on row limitation.

![
](https://raw.githubusercontent.com/sv18042016/fp1/38e6202832d95449080cc72b7361b8ca5cf22b8a/images/query_time.png)

## Pivot table

-  **Pivot** checks each dimension horizontally and reduces the effect of scrolling down the data.
  
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/78c46d819c716135d45ff60b9a71b15dd9e7a97f/images/pivot.png)

> Note : You can directly apply pivot option in data output field by selecting **pivot** option from drop down.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/1bae129344332eabae71b594bd320f0f5c5b4a68/images/pivot2.png)



## Group / Un-Group

 Select **Group** options to group fields and select **Un-Group** to release the same.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/12c2bc69fcf082dc620f2819ae901ae9c7a962a7/images/group.png)

## Calculated column 

Calculated column is statement or expression or a function operator which can be used to derive the column values.

- **Field name** unique identifier name to refer calculated column.
- **Label** labeling the calculated column.
- **Data type** data type used (string,number).
- **Field type** derives dimension or measure.
- **Calculation** derive arithmetical & logical expressions.
- **Calculate on the raw data** this function is applied directly on the retrieved value of the fields, initially before pivot or grouping options are applied.
 
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/c383b6e32c490bd5f0a32eb8cf2dcd4bb1fbfa9d/images/calculate%20column1.png)

**Run** the report after deriving calculated column, all the values obtained by applying calculation column is visible in green colour.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/c383b6e32c490bd5f0a32eb8cf2dcd4bb1fbfa9d/images/calculate%20column2.png)

## Pin or Remove Pin

To freeze the field values click on ** Pin** options in drop down and click on **Remove Pin** to release it.
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/b001b2f2f386a9730f3be339c38c54b73c69c5b9/images/pin.png)

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/f14d690d76bb1f0feacaf24259f67d1b9b55ea52/images/unpin.png)

## Field Visualization On / Off

 To hide field values click  **Hide Visualization** option in the drop down option.
 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/bee13bc200cda9988be61a3c7b58de502a4915fa/images/hide_visu.png)

## Data 
Depending on selection of fields, data section is enabled.
- **Row Grouping** enables grouping for column fields and it is applied for first column field only.
- **Explore Enabled** to explore data which are grouped.
- **Stacked** are used whether to stack the values at y-axis.
- **Datasets** specifies the alignment, formats, currency, number of y-axis and grouping of aggregates for the legends used in the visualization menu.
- **Calculate on Raw data** Calculates the field values before applying grouping, pivot or other parameters.

### Group aggregate
  It displays consolidated values of grouped fields.
  
**a.** Enable row grouping by selecting the checkbox.

**b.** Explore the primary column fields data individually, which are grouped under the column field. 

**c.** Select the field to perform row grouping.

  ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/657b29d2f18b269f2964e8150a3670df8db7869c/images/group_aggregate.png)


### Number Format & Currency option for fields

Apply different number formats and currency options to measures.
**a.**  Select required number format from list.
**b.**  Select currency you would like to view.

![
](https://raw.githubusercontent.com/sv18042016/fp1/a289a74e21b8055ac795aa2bb25d4cb945bc02b0/images/number_format.png)

####  list of number formats applicable on measures :


| A|B
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

####  Currency applicable on measures :

The following are the currency formats supported by AcuBi  $,   ₹  ,   €  ,  £.


## SQL Query 

Selected fields will build a SQL query in data analysis :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAzMjU5MTg3MywtMTkxMjg4NDQ3OCw0Mj
k2NDQ0MDEsMjEzODM4NTcwMF19
-->