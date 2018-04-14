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

Local Sorting can be applied directly to the data obtained for dimension and measure fields in the data section. Click on the desired field header to enable sorting.

For **Dimensions**

- Click on upper arrow to enable  ascending order.
- Click on down arrow to enable descending order.  

For **Measures**

- Click on upper arrow to enable  descending order.
- Click on down arrow to enable ascending order.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/7c178d95ca9160ecb5b41289894133fd10ce37cd/images/local_sorting.png)

## Display Totals

**8.**  By selecting the **check box** it displays the total values of the measure fields obtained.

 ## Display  Row Limit

**9.**  You can limit the rows extracted to 100, 500, 1000, 5000, etc selecting the limit value to your desired number from drop down list.                                                          

![
]

**7.** Click **Save** to Save the report, it will navigate to Save explore dialog box, Enter the below details : 
 
- **Report Name** Name identifier for a report. ( BiPlus allows  special character but does not  support any spaces )

- **Title** label for the report the way you want it to appear.

- **Info** displays any specific information about the report.

- **Privacy** you can save the report in any one of the following privacy option.

  - **Private ()** report saved in private section and accessed by the user itself.
  - **Public ()** the report is saved in public section and accessed by all the users.
  -  **Share ()** the report saved under share section and accessed by specific set of users.

 - **Filter** added in this section is automatically reflected in the filter section of reports in dashboard section.
 
 Finally click save to save the report.  

![
](https://raw.githubusercontent.com/sv18042016/fp1/62c6ac77c1e3a30e83c0718fefd7fd88ae35a203/images/save_ur.png)
Image 3 


**8.** If desired, you can view the visualization charts such as pie, bar, line etc. by clicking on **Charts** tab.

**9.** If desired to view the sql generated for the data retreived click on **SQL** tab. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/46d3025a6f09a3315a1b43392e6f77f12a74cce8/images/visual_ur.png)Image 4
All above explained points are the basics, to view the additional features of reports such as **Hidden filter**, **Pivoting**,  **totals**, **run time**,**order** and **Calculations**. You can check them in detail in **Data Analysis** document of BiPlus.
 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjQ4MzUxMTE0LC0xODg2MDU3MzIxLDQ3MT
I0MjE2NiwxODc2Nzc1OTA3XX0=
-->