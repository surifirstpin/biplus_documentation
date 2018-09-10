
<center><h1>Visualization Overview</h1></center>

Visualization in BiPlus creates impressive graphs and charts based on query result obtained. This section describes the data visualization and displays an eye-caching pictorial representation of the data obtained. Depending on your requirement you can visualize the data in different chart types. Now let us see in detail how does visualization works in BiPlus.

In BiPlus analysis section you can configure data and visualization together, So once you share a query user will get a picture and data as well.
**For Instance** : Let us create a pictorial representation for Customer details dashboard for better understanding. In this example we will query  **Customer_name, customer_address and order_value_sum.** Let us filter order_value_sum to limit our result less than or equal to 200000. ( Pie chart supports maximum 20 division)

After selecting dimensions and measure run the report to display the fetched data for customer details.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b8aad43c522f9e3f211ee64e97819bb66b98ff81/images/full_vis1.png)


## Visualization Adds Life to Data

On Analysis page Click on **charts** tab to configure different type of visualization images for your query. Select the suitable chart that matches your data requirement.
Under **General** tab click on the type of chart you want to view.

**For instance** : Let us take **Pie Chart**, for better understanding.

![
](https://raw.githubusercontent.com/sv18042016/fp1/eafbc564010f8906e66589373f5039607a0e68b6/images/visu_pie_chart1.png)


As shown in above image there multiple editing options provided to **Pie chart**, Similarly you can also view types of visualization available in BiPlus.

## Hide Pivot

To hide the first or last column field values in Visualization, Select hide first or hide last check box in Data section.
To carry out this function you need to derive a expression in calculated column.

For Example : Apply substraction for OrderValue_Sum and derive the exptression in calculated column as follow;

```
pivot_offset(#{ROOT.BI_DELIVERYREPORT.sum_ORDERVALUE} ,0,-1)
```
![
](https://raw.githubusercontent.com/sv18042016/fp1/f5065fab3212580100d2bb0d06de4bd7085f18a7/images/hide_pivot1.png)

The resultant for this expression would be seen in green colour;

![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot2.png)

In the above image you can see, hide_pivot 1st column is seen empty, so in order to hide this you need to select checkbox **pivot hide first** in **Data Section** to hide it in visualization charts. ( Applicable only for table chart). 
![
](https://raw.githubusercontent.com/sv18042016/fp1/3be153bc7e175559809c6c873dcb281c2a8e5783/images/hide_pivot3.png)


## Build Visualization to Refine

For better understanding of a user,
 BiPlus has provided some customizing options. Let us go with Pie chart and select percentage checkbox, which displays the amount of share a customer holds in total value and also we can display customers participating at the bottom of the chart by selecting show legend checkbox.

## Deeper insights of visualisation

Using BiPlus you can drill deeper into visualisation, to get more specific information about the data. To carry out this just click on the data point for which you want more deeper insight.

**For Instance**: In below chart, when you click on country it will display the states that fall under that country, for more deeper insight on clicking on State_Name it will display the list of cities that fall under that states as shown clearly in below image.

![
](https://raw.githubusercontent.com/sv18042016/fp1/bd51433e92663a090ee5049d77c52fdbb36a2fa3/images/drill_visu.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1NjI3MjMyMywtMzk5OTU5MDcsMTU1Mz
I5ODM1LC02NDE4NDIyMjMsMjM1MDYxOTIzLC0xNzAzMzE5MDEz
XX0=
-->