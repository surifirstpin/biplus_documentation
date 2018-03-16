<center><h1>Visualization</h1></center>


AcuBi has an ability to create graphics and charts based on the result obtained from a query. Visualization sections displays different type of pictorial representation of the data with better understanding. In Acubi the query result and visualization configuration seen together 

## Types of Visualization

Bi+ has an ability to show the data in 9 different chart types with some standard editing options.

**01. General Section :**

- **Title** label for chart and align them in top,bottom,left,right position.
- **Padding** sets the spacing at the top,bottom,left and right side of the charts.

**02.  X-Axis :**

- **Axis type** type of axis used in the charts, for instance Indexed is used to refer the numeric values starting from zero, category refer to the field values of the column and timeframe refer to the time-format of the data.
- **Label field** label the field name in x-axis using grid display.
- **Axis label** provides label to x-axis.
- **Reference Line** is used to refer specific values by applying colors to it.

**03. Y-Axis :**

- **Axis type** type of axis used in charts.
- **Label field** label the field name in Y-axis using grid display, including or excluding zero and aligning left or right position to y-axis.
- **Reference Line**  is used to refer specific values by applying colors to it.

## Format   

**4. Format Section :**        

- **Condition** Select the condition to apply on specific field.
- **Format on** enables the format on specific measure.
- **Value** Specify a value to which condition should be applied. 
- **BG (background colour)** Select the background colour for the data which is retrieved using condition.
- **Font** Select the font colour for the data retrieved based on condition.
- **Icon** Select a icon for the data retrieved based on condition.
- **Before number** Align the icon before or after the data.

## Line Chart in visualization menu:
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/line_chart.png)
 
 - Line type displays the information as a series of data points called markers.
Below are the list of markers used in Bi+ (uses spline as default line type), 
   - Spline 
   - Step
   - Area
   - Area-Spline
   - Area-Step
   - Scatter 

## Bar Chart 

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/bar_chart.png)

## Pie Chart :

- **Show percentage**  displays measure percentage in pie chart

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/pie_chart.png)


## Polar Area

Displays polar area of the dimensions

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/polar_area.png)

## Donut 

Bi+ has an ability to view the data of a pie chart into donut.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/donut.png)

## Radar chart 

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/radar_chart.png)

- **Tooltips** points the first measure value of the column field.
- **Grouped Tooltips** points all the measure values of the column field.
- **Points** enables pointers at the field values using the following point styles ;
    - Circle
  -  Triangle
  - Reet
  - RectRot
  - Cross
  - Cross Rot
  - Star
  - Line
  - Dash
- **Show legend** displays the measures values of the chart.
- **Position** Align the legend at top,bottom,left and right side of the chart.
- **Reverse scale** it displays the reversible scale values of the radar chart.
- **Show ticklabels** displays the points in y-axis.
- **Show arc lines** points the dimension fields in radar chart.
- **Arc field** select the dimension field to apply arc lines.
- **Curve** it maximum and minimize the measure values.

## Bubble chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/bubble_chart.png)

### X-axis for bubble chart :

- **Axis type** enables x-axis with indexed values or categorized dimension value and in time series format.
- **X-Axis** enables you to display dimensions values in x-axis. 
- **Show Grid** enables the grid display in bubble chart.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/6ea6b74b687735d18f0b1009219c5a3de903411a/images/bubble_chart2.png)

### Y-axis for bubble chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ca6272443bb686c3c41aa07bbd28a407c2238688/images/bubble_chart3.png)

- **Axis** select the measures values in y-axis  to enable
editing options for y-axis in bubble chart.
- **Format** enables number format for measure values.
- **Currency** enables the currency format for measures values in y-axis.
- **Y-Axis** display measure values in Y-axis. 
- **Show Grid** enables the grid display for measures in y-axis.
- **Include Zero** displays values in y-axis starting from zero.

### Reference lines in bubble chart :
  ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ca6272443bb686c3c41aa07bbd28a407c2238688/images/bubble_chart4.png)

  - **Name** Provide a reference name.
  - **Type** specifies how y-axis scale is calculated and displayed, below are the options available to enable the scale type.
    - Linear
    - Polynomial
    - Exponential
    - Logarithmic
    - Average
    - Median
    - Min
    - Max
    - Deviation
    - Variance 
    - Custom Line
    - Custom Area
    
- **Data Field** select the measure value which is to be referred.
- **Theme** choose the color for reference lines.

## Funnel chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/funnel_chart.png)

Bi+ provides an opportunity to view the funnel charts in different formats :**
 - Sort 
 - Curved
 - Pinched 
 - Inverted
 - Highlight on Hover 
 - Dynamic Height   
 - Dynamic Slop 
 - Load Animation

##  Gauge Chart :

Green color indicates the value attained is closer to target.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3ab8a101cb46871444f60f0e5b10e81a6785a826/images/guage.png)

Orange color indicates the value attained is half the way to target.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/671476ecbe2c70dcf89cc72f25b75ba5b4dafe41/images/guage_mediN.png)

Red color indicates the value attained is initial state or low. 

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/671476ecbe2c70dcf89cc72f25b75ba5b4dafe41/images/GUAGE_LOW.png)

- **Value** select the field value to carry out the operations.
- **Min** displays minimum value measure field.
- **Max** displays maximum value of measure field.
- **Donut** displays total measure value.
- **Counter** displays all the values starting from minimum to maximum.
- **Reverse** displays maximum to minimum value.
- **Hide Minmax**  hides min and maximum value.

## Table chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/table_chart.png)


## Widget chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/931940aa7f830b84487e8ea4b873c0857bbfa3e9/images/widget_chart.png)


- **Value** select the 1st measure value to apply the conditions.
- **Format** select the number format.
- **Previous value** select the 2nd measure value to apply conditions.
- **Change** choose the condition (difference,growth,none).
- **Show growth** displays the growth rate of selected measure fields.
- **Style** set different style formats from the option provided.

##  World chart :

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/fa5a5ec1ca971ffeed2d834874ab8905fc50bd31/images/world.png)

- **Title** provides name identifier to world chart.
- **Flat Map** enables the "2D" vision of the chart.
- **Default** set default colour to display specific countries.
- **Over Border** apply colour to the border.
- **Data Field** display the data field value on map.	
- **Tip Fields** select numbers of data fields to be displayed on map.
- **Colour Field** enable colouring to data field.
- **Colour** select the colour to be applied.
- **From & To** select the data field range to be colored.
- **Negative Cutoff** enabled when negatives values are applicable.
- **Negative colour-from & to** Specify colour for negative values.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1OTEwNDY5MDksLTExOTYwMTY4MzIsLT
E5NDgyMzIyNTUsNDY3OTA2MjI0XX0=
-->
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk2MTA3NjY2MywtNDYyNzY2MjM1LDEyNT
I5MDQxMjVdfQ==
-->