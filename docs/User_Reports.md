<center><h1>How to Create a Report</h1></center> 

BiPlus Reports displays the retrieved the data in the desired combinations as per your business needs and explores particular subject area it self. It provides an ability on how to pull the data and how to modify the report and drill down deeper into the report for more insight.

**1.** Click on **Analyse section.**

**2.** Select Desired **project** and **model** from the drop down list, depending on which you want to extract the data.

**3.**  Select one or more **dimension fields** ( Grey fields) to access and group your data.

**4.** Select one or more **measure fields** (Orange fields) to add information about those groups or data such as Sum, Count, Max, Min and  Avg etc. 

**5.** To retrieve the data based on filters applied , add a **filter** to your report based on that field.
 
 > **Note :**  The data can also be retrieved based on the applied hidden filters, this hidden filters are visible in the list of filter expression but are not visible while retrieving the data in data section. 

 **6.** Click **Run** to extract the data, based on selection made.

>  **Note :** Data retrieved on running a report, is visible in **Data section**( Refer image 1).

 ![
](https://raw.githubusercontent.com/sv18042016/fp1/62c6ac77c1e3a30e83c0718fefd7fd88ae35a203/images/data_retreived_ur.png)**Image 1**

## Order  (Ascending / Descending)

To view the column data in ascending or descending orders , add the column fields in order section to carry out the sorting on the field values.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/sorting1.png) Image 2

## Local Sorting

Local Sorting can be applied directly to the data fetched in the data section. Click on the desired field header to enable sorting.

For **Dimensions**

- Click on upper arrow to enable  ascending order.
- Click on down arrow to enable descending order.  

For **Measures**

- Click on upper arrow to enable  descending order.
- Click on down arrow to enable ascending order.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/local_sorting.png) Image 3

## Display Totals

 By selecting the **Display** check box, it displays total value of the measure field.

 ## Display  Row Limit

  You can limit the rows extracted to 100, 500, 1000, 5000, etc selecting the limit value to your desired number from drop down list.                                                          

## Pivot table

Multiple dimensions in the report data are often easier to look at, when you pivot one of the dimensions horizontally and display group based data for the field to which pivot is applied.

 **You can apply pivot to fields in 2 ways ;**
 
**a.** Apply pivot **After Retrieving** the data. 
**b.** Apply pivot **Before Retrieving** the data.

> **Note :** make sure you have at least one un-pivoted dimension and a measure value. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/ea7e55d6c87283e54b723361f7f20b45452ba847/images/pin_ur.png) **Image 4**

## Pin or Remove Pin

To freeze the column field values while scrolling the data to right or left, click on **Pin** in field drop down provided and to release the same click on **Remove Pin.** **( Refer image 4)**

## Group / Un-Group

you can view the consolidated value of the field by applying values By selecting group option for fields you can group the data and display the consolidated value of the field. To carry out this function click on **Group** in field drop down provided and to release the same click on **Un-Group**. **( Refer image 4)**

## Multi-Level grouping

Using BiPlus, you can apply Multi-level grouping to the data extracted. consider the below example for more detailed description on multi level grouping.

> **For instance** : in the below image grouping has been applied to 2 dimension fields **Station code** and **Whenmade (hour).** In retrieved data on expanding Station code it displays the perspective **Whenmade (hour)** of that station code,on Further Expansion of **Whenmade (hour)** it displays Role of the Employee  as shown in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/4d2a0c1e593e8422f72204368da90bd428545c56/images/multi_level_grouping_ur.png)

## Find

To find the specific data of the field from retrieved list, click on **Find** in the field drop down and enter the specific field value you want to view.**( Refer image 4)**


## Field Visualization On / Off

To hide the specific field in the visualization charts click on **Hide Visualization** in the drop down of field  and to display the same click on **Show visualization****( Refer image 4)**

## Remove

To remove a specific field column from the extracted list click on **Remove** in drop down list of the field.**( Refer image 4)**

## Calculated Column

All the mathematical and logical calculation are carried out in a report using Calculated column

Click on **Calculated column** button to enable table calculations, 

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

**Data Tab** under **Charts Section** is enabled based on the data retrieved for fields. Below are the parameters applicable on the data retrieved.

- **Row Grouping** enables row grouping for fields values based on the field selected as shown in the below image.

- **Explore Enabled** to explore the data which are grouped select check box **Explore Enabled.**

- **Stacked** Series values are added on the y-axis, so each consecutive series appears above the last. Be sure that the units of all series match.

- **Datasets** this section enables you to perform alignment, set currency formats, group aggregates ( Sum, Avg, Max, Min, Count ) on the consolidated values of the field.

- **Legend** it will enable you to change the label for measure value in visualization charts as shown below.

![
](https://raw.githubusercontent.com/sv18042016/fp1/49bb2a07efd42d5b6f9a7f648e8f705e5f63bc4d/images/legend_label.png)

##  Format

At the same time the **Format** Tab is enabled by allowing different type of number format to measure field value. Following are the list of number formats supported by BiPlus ;

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

## Currency

BiPlus will enable you to check the field values of the measure in the following currency formats $,   ₹  ,   €  ,  £.

## Charts 

To view the Visualization images of Retrieved data, Click on **Chart** Section.

At Present there are 10 type of visualization images available in BiPlus, To view them click on **General section.** 

**Let us see them in detail,**

 - Line
 - Bar
 - Pie
 - Radar
 - Bubble
 - Funnel
 - Gauge
 - Table 
 - Widget
 - World
 
## Line Chart
 
**1.** Click on **line** tab under **General** section  to compare the data in line chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/6904440c50633ac92f461d7b7f2fd2c2d0e9b7dc/images/line_chart.png)


 ### Editing Options for Line Chart
 
 - **Line type** displays the information as a series of data points called markers. Below are the list of markers used in line chart ( spline acts as  default line type), 
   - Line
   - Spline 
   - Step
   - Area
   - Area-Spline
   - Area-Step
   - Scatter
    
- **Points**  will display the the data by specifying the points on the chart.

- **Point style** will specify how the data points will appear on chart. below are the following options available. 
  - Circle
  - Triangle
  - Rectangle
  - RectRot
  - Cross
  - CrossRot
  - Star
  - Line
  - Dash

## Bar Chart 

Bar charts are used to compare data across different categories. You can build a bar chart by placing a dimension on the Rows and a measure on the Columns area.

 **2.** Click on **Bar** tab under **general** section  to compare the data in Bar chart.
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/c21c91b0c8f9e243362fbefc44279936c6021d12/images/bar_chart.png)


## Pie Chart :

This section describes the editing option for Pie chart in visualization. 
 
 **3.**  Click on **Pie** tab under **general** section to compare the data in pie chart.
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/f52c167aa93a715736ed2800ae5ca56675c54e42/images/pie_chart.png)

### Editing Options for Line Chart
 
- **Show percentage**  displays percentage for each measure value in pie chart. To enable it select the **Check Box** show percentage as shown below;

![
](https://raw.githubusercontent.com/sv18042016/fp1/6921e2105eb29674d2f727201df80f5be58983d5/images/show_percentage.png)

- **Polar Area** On selecting the polar area **Check Box** it enables the polar view for each dimensions in pie chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/ca8620aee571293baafa06532397667001086ceb/images/polar_area.png)

-  **Donut** donut chart are equal to pie chart. they show relationships of parts to a whole. select **Check Box** to enables the donut view.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/donut.png)

## Radar chart 

 Radar charts are a great way to compare members of a dimension in a function of several metrics.  
For example, when you want to buy a Laptop, you can use a radar chart to compare several devices across several metrics like battery life, memory, hard drive etc.  

 **4.** Click on **Radar** tab under **general** section  to compare the data in  Radar chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/34c8d8bc129b2e32ded89f8d3f9816b6a8fd1624/images/radar_chart.png)

- **Points** on selecting this checkbox it enables pointers for the data range in line chart.

- **Point style** it will specify the way that data points should appear on chart. 
**Options available for point style;** 
  - Circle
  - Triangle
  - Rectangle
  - RectRot
  - Cross
  - CrossRot
  - Star
  - Line
  - Dash
  
- **Reverse scale** on selecting this checkbox the values shown in the chart will be reversed, i.e. if the 10 highest values are shown and if reversed scale is checked, then chart will  show the 10 lowest values.

- **Show ticklabels** on selecting this checkbox  it enables measure values on y-axis.

- **Show arc lines** on selecting this checkbox it points the dimension fields in radar chart.

- **Arc field** select the dimension field to apply arc lines.

- **Curve** it maximize and minimize the surface area in radar chart.

## Bubble chart :

It is used to display the data in circles. We can define each bubble using any of our Dimension value and size by Measure value.
 
 **5.** Click on **Bubble** tab under **general** section  to compare the data in Bubble chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/d07e80177a8a6fe04619cfb40058e9789b142e88/images/bubble_chart.png)

## Funnel chart :

Funnels helps to visualize a process that has stages and items flow sequentially from one stage to the next. Use a funnel when there is a sequential flow between stages, such as a sales process that starts with inquiry and ends with billing.
 
 **6.** Click on **Funnel** tab under **general** section  to compare the data in Funnel chart.
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/caca3ad67049c43bc60a5fccae26182c81762732/images/funnel_chart.png)

Using AcuBi you can view the funnel charts in different formats using the below check boxes:

 - **Sort** on selecting this check box, it enables data in the sorted order in funnel chart.
  
 - **Curved** on selecting this check box, it will display the funnel chart in curved view.
 
 - **Pinched** on selecting this check box, it will display the compressed view of the funnel chart.
  
 - **Inverted** on selecting this check box it will display the funnel chart in reversed or bottom up position.
 
 - **Highlight on Hover**  on selecting this check box, it will highlight each section by placing a cursor on it.
 
 - **Dynamic Height** on selecting this check box it will display the height as per the values in funnel chart. For example higher value is referred with more height and lower value is referred with low height.
 
 - **Dynamic Slope** on selecting this checkbox it will display the potential covered based on the value.For example higher value is referred with bigger slope and lower value is referred with smaller slope.

 - **Load Animation** on selecting this check box the column values in funnel chart will appear as moving image.


##  Gauge Chart :

Gauge chart displays current status in the context of goal.

 
 **7.** Click on **gauge** tab under **general** section  to compare the data in Gauge chart.

- **Green** colour in gauge chart indicates the value attained is closer to target.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d48b5330b04434d91eb267dac601af036d2ccb8a/images/guage.png)

- **Orange** colour indicates the maximum value attained is half the way to target and **Red** colour indicates the maximum value attained is at initial state or lower side of the target. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/274ea8e6aa7a779c79c78d56c4722a5dbdf2a26c/images/guage2.jpg)

- **Value** select one of the available measure values from the drop down.

- **Min** specifies the minimum value of the gauge this corresponds to bottom position of the gauge.

- **Max**  specifies the maximum value of the gauge this corresponds to top position of the gauge.

- **Title** specify a title.

- **Label** specify a identifier name to display in the chart.

- **Donut** displays total measure value.

- **Counter** displays minimum and maximum values of the measure.

- **Reverse** displays the measure values in reversal direction maximum to minimum.

- **Hide Minmax**  hides min and maximum values in gauge target.

## Table chart :
 
Table chart displays the data in series making it more feasible for comparing dimensions and measure values.
 
 **8.** Click on **Table** tab under **general** section to compare data in table chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/b6e598ee67160c266bb9d4d30a423f520880bf63/images/table_chart.png)

## Widget chart :

It displays one or more data series as a data graph. Widget chart is used to display the number of records created today. number of Incidents by status or department.

 **9.** Click on **widget** tab under **general** section to display the total record of the data in widget chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/0fffbbc444991a973205bc030a0485bfc9ef592a/images/widget_chart.png)

- **Value** select the measure to show in the widget. you can use this field to specify the measure field if you have multiple measure value defined in the underlying step.

- **Format** select the number format for the measure field.

- **Previous value** select the second measure value for widget.

- **Change** specify the conditions for selected measures such as difference, growth, none.

- **Show growth** displays the growth rate of selected measures.

- **Title** specify widget title.

- **Label** specify the widget label.

- **Style** specify a status indicator for measure value such as default, primary, success, warning, info, danger.

##  World chart :

 It displays the data grouped by specific country and at the same time the grouped data regions are highlighted in the map.
 
**10.** To view the **World chart** click on **world** tab under **General** section.
 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/fa5a5ec1ca971ffeed2d834874ab8905fc50bd31/images/world.png)

- **Title** specify a title for world map.
- 
- **Flat Map** displays a flat view or "2D" vision of the map.

- **Default** set default colour to display specific countries.

- **Over Border** colour the border of a map region.

- **Data Field** choose the data field to display it on map.	

- **Tip Fields** select numbers of data fields to be displayed on map.

- **Colour Field** specifies which field to be coloured.

- **Colour From & To** specify the colour specific range of values in map region.

- **Negative Cutoff** enabled when negatives values are applicable.

- **Negative colour-from & to** Specify colour for specific range of negative values.

## Standard Editing Option in Charts

##  General Section :

- **Title** specify title for the chart selected.

- **Position** align title to top,bottom,left,right position.

- **Label** Specify label text.

- **Padding** specifies spacing at the top,bottom,left and right side of the charts.

- **Tooltips** points the first measure value of the column field.

- **Grouped Tooltips** points all the measure values of the column field.

- **Show legend** on selecting this checkbox it displays the measures fields used at the bottom of the chart, you can display or hide specific measure field values on chart by clicking on the measure field.

- **Position** Align the legend at top,bottom,left and right side of the chart.

## X-Axis Menu Options

- **Axis type** specifies the how x-axis scale for Line, Bar,Bubble is calculated and displayed.

  - **Indexed** specifies the data to be plotted in numeric values starting from zero on x-axis.
   
  - **Category** specifies the data to be plotted as category group on x-axis.
  
  - **Timeseries** specify the data to be plotted as time values. The x-axis is labeled with appropriate time increments.
 
- **Label field**  specify a dimension field to be displayed on X-axis.

- **Show Grid** enables the grid display for dimension fields on x-axis.

- **Axis label** Text label for x-axis.

### Reference Lines

**Reference Lines** enables the creation of reference lines in a chart.

 - **Reference** specify a indicator name. 
  
 - **Type** specify reference type as line or  area.
  
 -  **From & to** specify the reference line for specific range of dimensions.

 - **Theme** enables colour for reference line.
 
 > **Note:**  X-Axis is enabled only for Line, Bar and Bubble chart only.

## Y-Axis

- **Axis** select the measures values on y-axis  to enable
editing options for y-axis in Line, Bar and bubble chart.

- **Axis label** Text label for x-axis.

- **Format** it enables number format for numeric values.

- **Currency** Using this field, you can specify the formatting for currency as of now AcuBi supports $,   ₹  ,   €  ,  £.

- **Y-Axis** display measure values on Y-axis. 

- **Show Grid** enables the grid display for measures on y-axis.

- **Include Zero** displays measure values starting from zero.

- **Position** you can can align the y-axis to left or right side of the chart.

### Reference Lines

**Reference Lines** enables the creation of reference lines in a chart.

- **Name** specify a reference name for specific information on y-axis.
  
 - **Type** specify  Linear, Polynomial, Exponential, Logarithmic, Average, Median, Minimum, Maximum, Deviation, Variance, Custom Line, Custom Area on Y-axis.
  
 -  **From & to** specify the reference line for specific range of measure values.

 - **Theme** enables colour for reference line.
 
 > **Note:**  Y-Axis is enabled only for Line, Bar and Bubble chart only.
 
## Format   
      
- **Condition** Specify any of the following condition types Greater than, Less than, Between, Not Between, equal to, duplicates values, Top 10 Items, Bottom 10 Items, Above Average, Below Average for the fields.

- **Format on** Specify a measure field on which you want to apply format.

- **Value** Specify a value to measure the condition.

- **BG (background colour)** Select the background colour for the data which is retrieved using condition.

- **Font** Select the font colour for the data retrieved based on condition.

- **Icon** Select a icon for the data retrieved based on condition.

- **Before number** Align the icon before or after the data.





## SQL Query 

To view the SQL query built on running the report, click on **SQL** Tab in Analysis Section.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png)


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg5NDQyMzgxNywtMTg1NjE0Mzc3NSwzMD
UxMzg0NCwxMjkxMjYwMTcyLDQzMTg1MDczMiwtMTMzMzg3Njkz
MCw0NTE1MTUzMDYsLTE4Njk0NDUwMzEsLTEwNTE4Njg2NjcsNz
c4NTc3NDQ1LDE3NDI3ODAzMjEsLTI3NTMyMjUxMCwyNTg2MTQw
ODksLTc1MDA2MDI5NCwtMTkxMjg2NjczOCwtNTA2NzA5MTgwLD
EwMTc3MjQ0MTcsODIyNDQyODUyLDE4MDYzNjcwOTQsLTExOTM2
NDAzNzZdfQ==
-->