
<center><h1>Visualization Types and Settings</h1></center>

AcuBi Provides an ability to visualize the data in 11 different types of charts with some standard editing options. Based on priority to view specific information about the data retrieved. Each type of visualization have different setting which can be customized for its appearance. 

**Types of visualization available in AcuBi :**
 - **Line**
 - **Bar**
 - **Pie**
 - **Radar**
 - **Bubble**
 - **Funnel**
 - **Gauge**
 - **Table**             
 - **Widget**
 - **World**
 - **Horizontal Bar**

> **Note :** Some of the options in editing list might be hidden or grayed,  where they would conflict with other settings you have chosen.

## Line Chart

 Emphasize the overall shape of an entire series of values, usually over time.
 
 **1.** Click on **line** tab under **General** section  to compare the data in line chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/6904440c50633ac92f461d7b7f2fd2c2d0e9b7dc/images/line_chart.png)

 ### Editing Options for Line Chart
 
 - **Type** displays the information as a series of data points called markers. Below are the list of markers used in line chart ( spline acts as  default line type), 
   - Line
   - Spline 
   - Step
   - Area
   - Area-Spline
   - Area-Step
   - Scatter
    
- **Points**  will display the data by specifying the points on the chart.

- **Point style** will specify how the data points will appear on chart. Below are the following point styles available in AcuBi.
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

Bar charts are used to compare data across different categories. You can build a bar chart by placing a dimension on rows and measure on columns area.

 **2.** Click on **Bar** tab under **General** section  to compare the data in bar chart.

- **Stacked** Series of values are added on the Y-axis by displaying  each consecutive values above the last. 

- **100% Stacked**  Series of values are presented as percentages stacked on the y-axis, where all values add up to 100%.

 ![
](https://raw.githubusercontent.com/sv18042016/fp1/c21c91b0c8f9e243362fbefc44279936c6021d12/images/bar_chart.png)


## Pie Chart 

This section describes the editing option for Pie chart in visualization. 
 
 **3.**  Click on **Pie** tab under **General** section to compare the data in pie chart.
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/f52c167aa93a715736ed2800ae5ca56675c54e42/images/pie_chart.png)

### Editing Options for Pie Chart
 
- **Show percentage**  on selecting this checkbox, it displays percentage value for each measure in pie chart. if disabled it  displays dimension name. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/6921e2105eb29674d2f727201df80f5be58983d5/images/show_percentage.png)

- **Polar Area** On selecting the polar area **Check Box** it enables the polar view for each dimensions in pie chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/ca8620aee571293baafa06532397667001086ceb/images/polar_area.png)

-  **Donut** donut chart are equal to pie chart. They show relationships of parts to a whole. select **Donut Check Box** to enable donut view.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/donut.png)

## Radar chart 

 Radar charts, are great way to compare members of a dimension in a function of several metrics.  
**For example,** when you want to buy a Laptop, you can use a radar chart to compare several devices across several metrics like battery life, memory, hard drive etc.  

 **4.** Click on **Radar** tab under **General** section  to compare the data in  Radar chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/34c8d8bc129b2e32ded89f8d3f9816b6a8fd1624/images/radar_chart.png)

- **Points** on selecting the checkbox it enables pointers for the data range in line chart.

- **Point style** will specify how the data points will appear on chart. Below are the following point styles available in AcuBi.
  - Circle
  - Triangle
  - Rectangle
  - RectRot
  - Cross
  - CrossRot
  - Star
  - Line
  - Dash
  
- **Reverse scale** on selecting this checkbox it displays the inverse values.
 >**For Instance :** if the chart displays the 10 highest values, on Checking Reverse Scale , it displays 10 lowest values.

- **Show ticklabels** on selecting the checkbox  it enables measure values on y-axis.

- **Show arc lines** on selecting the checkbox it points the dimension fields in radar chart.

- **Arc field** select the dimension field to apply arc lines.

- **Curve** it maximum and minimize the surface area in radar chart.

## Bubble chart 

It is used to display the data in circles. We can define each bubble using any of our Dimension value and size by Measure value.
 
 **5.** Click on **Bubble** tab under **General** section  to compare the data in Bubble chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/d07e80177a8a6fe04619cfb40058e9789b142e88/images/bubble_chart.png)

## Funnel chart 

Funnels helps to visualize a process that has stages and items flow sequentially from one stage to the next. Use a funnel when there is a sequential flow between stages, such as a sales process that starts with inquiry and ends with billing.

**The following section describes the editing option for bubble chart in visualization :**
 
 **6.** Click on **Funnel** tab under **General** section  to compare the data in Funnel chart.
 
 ![
](https://raw.githubusercontent.com/sv18042016/fp1/caca3ad67049c43bc60a5fccae26182c81762732/images/funnel_chart.png)

**Using AcuBi you can view the funnel charts in different formats using the below check boxes :**

 - **Sort** it enables the sorted order for funnel chart.
 
 -  **Top width**  it adjust the width dimension in top view.
 
 - **Bottom Width** it adjust the width dimension in bottom view.
 
 - **Gap** It enables gap between two measure values.

 
##  Gauge Chart 

Gauge chart displays current status in the context of goal.

 
 **7.** Click on **gauge** tab under **General** section  to compare the data in Gauge chart.

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

## Table chart 
 
Table chart displays the data in series making it more feasible for comparing dimensions and measure values.
 
 **8.** Click on **Table** tab under **General** section to compare data in table chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/b6e598ee67160c266bb9d4d30a423f520880bf63/images/table_chart.png)

### Hide Pivot

To hide the first or last column field values in visualization, Select hide first or hide last check box in Data section, to carry out this function you need to derive a expression in calculated column.

>**For Example :**  Apply subtraction for OrderValue_Sum and derive the expression in calculated column as follow;

```
pivot_offset(#{ROOT.BI_DELIVERYREPORT.sum_ORDERVALUE} ,0,-1)
```
![
](https://raw.githubusercontent.com/sv18042016/fp1/f5065fab3212580100d2bb0d06de4bd7085f18a7/images/hide_pivot1.png)

The resultant for this expression would be seen in green colour;

![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot2.png)

In the above image you can see, hide_pivot 1st column is seen empty, so in order to hide this you need to select checkbox **Pivot Hide First** in **Data Section** to hide it in visualization charts. Similarly you can hide last column by selecting the check box pivot hide last ( Applicable only for table chart). 
![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot3.png)



## Widget chart 

It displays one or more data series as a data graph. Widget chart is used to display the number of records created recently. Number of Incidents by status or department.

 **9.** Click **Widget** tab under **General** section to display the total record of the data in widget chart.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/0fffbbc444991a973205bc030a0485bfc9ef592a/images/widget_chart.png)

- **Value** select the measure to display in widget. you can use this field to specify the measure field if you have multiple measure value defined in the underlying step.

- **Format** select the number format for the measure field.

- **Previous value** select the second measure value for widget.

- **Change** specify the conditions for selected measures such as difference, growth, none.

- **Show growth** displays the growth rate of selected measures.

- **Title** specify widget title.

- **Label** specify the widget identifier name.

- **Style** specify a status indicator for measure value such as default, primary, success, warning, info, danger.

##  World chart 

 It displays the data grouped by specific country and at the same time the grouped data regions are highlighted in the map.
 
**10.** To view the **World chart** click on **world** tab under **General** section.

 > **Note :** The data you want to define in world chart, should be defined in model section first. On deriving in model section, data field values will be displayed here.  

![
](https://raw.githubusercontent.com/sv18042016/fp1/40b704503bb7342aa38ccd68e7c30a0708959f27/images/world.png)
 
- **Title** specify a title for world map.

- **Flat Map** displays a flat view or "2D" vision of the map.

- **Default** set default colour to display specific countries.

- **Over Border** colour the border of a map region.

- **Data Field** choose the data field to display it on map.	

- **Tip Fields** select numbers of data fields to be displayed on map.

- **Colour Field** specifies which field to be coloured.

- **Colour From & To** specify the colour specific range of values in map region.

- **Negative Cutoff** enabled when negatives values are applicable.

- **Negative colour-from & to** Specify colour for specific range of negative values.


## Horizontal Bar

Horizontal Bar charts are used to compare data across different categories horizontally. You can build a bar chart by placing a dimension on the Y-axis and a measure on X-axis.

## Standard Settings

### General Section 

- **Title** specify title for chart selected.

- **Position** align title to top, bottom, left, right position.

- **Label** specify label text.

- **Padding** specifies spacing at the top, bottom, left and right side of the charts.

- **Tooltips** on moving the cursor over the charts it displays the measure value of the specific section.

- **Grouped Tooltips** if the underlying field defines a description for a field, that description id displayed on moving the hover over the column name.

- **Show legend** on selecting the checkbox it displays the measures fields used at the bottom of the chart, you can display or hide specific measure field values on chart by clicking on the measure field.

- **Include Nulls** on selecting this checkbox it displays **Null Values** retrieved in Charts section.

- **Display Labels** on selecting this checkbox, it displays the data value obtained for the fields.

- **Background Enabled**  it enables background colour for labels.

- **Font Weight**  Set the label font to normal ( default) or Bold text.

- **Font Size** Enable font size for label.

- **Border radius** Set the label border radius to a given range.

- **Rotation** This option controls the clockwise rotation angle (in degrees) of the label, the rotation center point being the label center. The default value is 0 (no rotation).

-  **Align**   it defines the position of the label relative to the anchor point position and direction. Its value can be expressed by one of the following string presets:

   -   **start** the label is positioned before the anchor point, following the same direction
   -   **end** the label is positioned after the anchor point, following the same direction
   -   **center (default)** the label is centered on the anchor point
   -   **right** the label is positioned to the right of the anchor point (0°)
   -   **bottom** the label is positioned to the bottom of the anchor point (90°)
      -   **left** the label is positioned to the left of the anchor point (180°)
   -   **top** the label is positioned to the top of the anchor point (270°)
  - **Anchor** The label position is calculated based on the anchor option. AcuBi supports Following positioning.

    -   **Center  (default)** aligns the Label in center.
    -   **Start** aligns the the label at lowest boundary.
    -   **End** aligns the label at highest boundary.
    
- **Align Negative** It will enable the negative values to be displayed below range  `0`.
 
### Data 

- **Row Grouping** displays the grouped value of the duplicate fields.

- **Explore Enabled** on selecting the checkbox, it allows you to view the  data which has been grouped or else it displays only the consolidated value.

- **Legend** displays the measure.

- **Format** Choose the number format for measure value.

- **Currency**  Cheese the currency format for  measure value.

- **Y Axis** Choose the measure values to be displayed on chart.

- **Column Aggregate ( Table View)** Type of aggregate value to be displayed for a measure.

- **Custom Tooltip** on moving the hover on the column it displays the customized new value. 

> **Example :**  in case if we are taking two measures than you can interchange the measure fields values on the column as per the requirement. 

- **Custom Label** It displays customized label for the column field value and at the same time you can add a prefix or suffix at starting or ending position of the label value.

**For Instance** : Consider label value 123000( Sum_Rate), now assign a prefix to the already existing value at the starting position, 
##{start:00}#{sum_rate}--> it results in 00123000, 
##{End:11}#{sum_rate}--> it results in 12300011, 

```
##{start:TEXT/NUMBER }#{sum_rate} as of
 #{sum_amount}##{end:TEXT/NUMBER }
```

- **Bubble Size( Bubble Chart)** Depending on measure values, it varies in size.

### X-Axis Editing Options

 > **Note:**  X-Axis is enabled only for Line, Bar and Bubble chart only.
 
- **Axis type** specifies the how x-axis scale for Line, Bar, Bubble is calculated and displayed.

  - **Indexed** specifies the data to be plotted in numeric values starting from zero on x-axis.
   
  - **Category** specifies the data to be plotted as category group on x-axis.
  
  - **Time series** specify the data to be plotted as time values. The x-axis is labeled with appropriate time increments.
 
 - **X-Grid Color** display specific color on X-axis.

- **X-Axis Font Color** Enables different color option for the values on X-axis.

- **Label field**  specify a dimension field to be displayed on x-axis.

- **Show Grid** enables the grid display for dimension fields on x-axis.

- **Axis label** Text label for x-axis.

**Reference Lines** enables the creation of reference lines in a chart.

 - **Reference** specify a indicator name. 
  
 - **Type** specify reference type as line or  area.
  
 -  **From & to** specify the reference line for specific range of dimensions.

 - **Theme** enables colour for reference line.
 
### Y-Axis Editing Options

 > **Note:**  Y-Axis is enabled only for Line, Bar and Bubble chart only.
 
- **Axis** select the measures values on y-axis  to enable
editing options for y-axis in Line, Bar and bubble chart.

- **Axis label** Text label for x-axis.

- **Format** it enables number format for numeric values.

-  **Y-Grid Color** display different color on Y-axis.

- **Y-Axis Font Color** Enables different colors for the dimensions ( Horizontal Bar) or Measures on Y-axis.

- **Y-Axis** display measure values on Y-axis. 

- **Show Grid** enables the grid display on y-axis.

- **Include Zero** displays measure values starting from zero.

- **Position** you can can align the y-axis to left or right side of the chart.

**Reference Lines** enables the creation of reference lines in a chart.

- **Name** specify a reference name, for specific information on y-axis.
  
 - **Type** specify  Linear, Polynomial, Exponential, Logarithmic, Average, Median, Minimum, Maximum, Deviation, Variance, Custom Line, Custom Area on Y-axis.
  
 -  **From & to** specify the reference line for specific range of measure values.

 - **Theme** enables colour for reference line.
 
 
## Format   
      
- **Condition** Specify any of the following condition types Greater than, Less than, Between, Not Between, equal to, duplicates values, Top 10 Items, Bottom 10 Items, Above Average, Below Average for the fields.

- **Format on** Specify a measure field on which you want to apply format.

- **Value** Specify a value to measure the condition.

- **BG ( background colour )** Select the background colour for data which is retrieved using condition.

- **Font** Select the font colour for the data retrieved based on condition.

- **Icon** Select a icon for data retrieved based on condition.

- **Before number** Align the icon at before or after data value.

**For Example :** Consider below image, which displays the format section for table chart.

![
](https://raw.githubusercontent.com/sv18042016/fp1/9bb64e7b3a5912162ec782e349b90edcdaa8fa0c/images/formar.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NjkyMDI3ODQsMTU3OTUyNTU2OCwxNz
M4NDAyNjU3LDE4NjQyNzQ2NzUsMTAzNjAwMDUxNywtMTY3MDg4
MzI5LC04MzYwOTczODUsMTA4MDA0NTIyMCwtMTcwOTQ1NzEwLD
E1NzI0ODA3NzQsMjQxMjc1NTcxLC01NjIzODQzNDYsLTIxMTUw
NDI4ODEsNjE2NzI3MDUwLDEzMjQ5MTU5NjEsMTI2NjYxNDA2MC
wxOTIyNTgyOTYyLDE2MDAxOTkzNDYsLTEzMjMxMTAzMDYsLTg4
ODg2MTk1NF19
-->