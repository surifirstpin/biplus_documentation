
<center><h1>Visualization Overview</h1></center>

This section describes a basic overview on visualization and its functionality.
> All the features are clearly described in **Visualization Types and Settings** document

Visualization in AcuBi creates impressive graphs and charts based on query result obtained and displays an eye-caching pictorial representation of data obtained. Based on your requirement, you can visualize the data in different chart formats.

**Basic overview on how visualization works ;**

In Analysis section you can configure data and visualization together, So once you share a query user will get a picture and data as well.

**For Instance** : Create a report to fetch customer details.  In this example we will query  **Customer_name, customer_address and order_value_sum.** Apply filter order_value_sum to a limit of less than or equal to 200000. ( Pie chart supports maximum 20 division)

After selecting dimensions and measures, run the report to display the fetched data for customer details.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b8aad43c522f9e3f211ee64e97819bb66b98ff81/images/full_vis1.png)


## Visualization- Adds Life to Data

Click on **Charts** tab, to configure different type of visualization images for your query. 
Under **General** tab, click on the type of chart you want to view.

**For instance :** Consider **Pie Chart,** for better understanding.

![
](https://raw.githubusercontent.com/sv18042016/fp1/eafbc564010f8906e66589373f5039607a0e68b6/images/visu_pie_chart1.png)

As shown in above image there multiple editing options provided to **Pie chart**, Similarly you can also view types of visualization options available in AcuBi.

## Hide Pivot

To hide the first or last column field data  in visualization, Select hide first or hide last check box in Data section.
To carry out this function you need to derive a expression in calculated column.

**For Example :** Apply subtraction for Order Value_Sum and derive the expression in calculated column as follow ;
	
```
pivot_offset(#{ROOT.BI_DELIVERYREPORT.sum_ORDERVALUE} ,0,-1)
```
![
](https://raw.githubusercontent.com/sv18042016/fp1/f5065fab3212580100d2bb0d06de4bd7085f18a7/images/hide_pivot1.png)

The resultant for this expression would be seen in green colour;

![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot2.png)

In the above image you can see, hide_pivot 1st column is seen empty, so in order to hide this you need to select checkbox **pivot hide first** in **Data Section** to hide it in visualization charts. Similarly you can hide last column by selecting the check box pivot hide last. (Applicable only for table chart). 

![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot3.png)


## Refine Visualization

To refine and enhance the data obtained, AcuBi is provided with customizing options. Consider a Pie chart example, and select **Percentage** checkbox, which displays the amount of share, a customer holds in total value and display customers participating, at the bottom of the chart by selecting **Show legend** checkbox.


## Deeper insights in visualization

You can drill deeper into visualization, to get more specific information about the data. In order to carry out this function, click on the data for which you want more deeper insight.

**For Instance**: In below chart, when you click on country it will display the states that fall under that country, for more deeper insight on clicking on State_Name it will display the list of cities that fall under that states as shown clearly in below image.
 
 > **Note:**  To carryout this function you need derive it in model first.

A more detailed explanation on visualization is given in visualization types and settings documents.

![
](https://raw.githubusercontent.com/sv18042016/fp1/bd51433e92663a090ee5049d77c52fdbb36a2fa3/images/drill_visu.png)


<!--stackedit_data:
eyJoaXN0b3J5IjpbNTEwNjE3MjA0LDIxMDk5ODQwNDgsMTE3NT
k5MDI0MywxMzEwMjk0NjYzLDE5NzI4NzIzNTgsMTI3ODEyNDE2
OCw5MTU1MjA1NjQsLTE4MDA0MjI5MCwxODg0MzcyNzMyLDE4Mz
g2MTMxODgsMTkwOTQzMDM4OSw3MDg5MTAxMjAsMzgxNDMzOTI4
LDEzODk2NjQyOTYsLTExMTMyMDQ1MDYsLTgzMzEzNzg2NCwtMT
Q2NTIxMDU1Miw2MTQ1Mjk4MzEsODE5MDQzMTU1LDQyMTEzNjgz
Nl19
-->