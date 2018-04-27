

<center><h1>How to Ceate a Dashboard</h1></center>

> Written with [StackEdit](https://stackedit.io/).

Dashboard provides access to view multiple reports in single dashboard layout, in this way it provides a quick view on related data. In order to make it more feasible to users, it is provided with set of global filters by making dashboard more interactive.

## Getting Started


**1.** Select **Dashboard section** and Click on **New Dashboard** Button on top right of the screen. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_1.png)

**2.** Select the suitable **layout** as per your requirement from layout options available on left, to add reports to it.

 Layout formats are categorized in 2 ways.
- **Flow Layout** in this layout it is provided with a scroll bar option to define your layout appropriately.
- **Fixed Layout** in this layout all the reports will fit into single screen.

**3.** Click on **Update report** to add reports to the selected layout. 

There are 2 ways you can add reports to the layout;

a. Click on report layout section and select the report you want to **add** to the layout.

b. Click on **add** link available at right side of the saved report. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_2.png)

**4.**  Click on **Apply Filters** button it will navigate to  global dashboard filters and lookups section.

 **5.** **Dashboard global Filters** allows user to view limited data by applying filters on dashboard reports and it supports following filter types string, number, date and lookup.
 
|  **Type** | **Description** |
|  ------ | ------ |
|  String | For fields that contain letters or special characters. |
|  Number | For fields that contain numbers. |
|  Date | For fields that contain dates. |
|  Lookup | To view the lookup in dashboard filters it should be defined in lookup section. |

Fill up the dashboard global section;

-   **Filter Name**  identifier name to the filter applicable.

-   **Filter Type**  type of filter user (eg: string,date,number).

-   **Operator**  filter operation that are applicable.

**6.** Adding lookup to dashboard will refer set of query or list of items in filters.

Fill up the lookup section;
  -   **Lookup name**  name of the lookup field.
   
   -   **Lookup Type**  refers to item or query type.
   
   -   **Test Lookup**  to test the lookup.
   
   -   **Multiple Selections**  refers to selection of list of multiple data.
   
   -   **Referred** The changes made on single lookup will be reflected on all the following reports based on the referred data.
  > **For Instance**  if we want to **refer** to country A then all states falling under that country will be updated based on the selection made.

**7.** **Report Listeners** are used to assign a defined filters to report column (fields of views based on which the report is created). 
**For instance** if a filter is defined for dashboard containing 2 reports and listener is added on particular field for report1 it results in filter applied on report1, it self and report2 will remain unaffected.

Fill up Report Listener section;

-   **Add Listener**  adds multiple filters to reports.

-   **Dashboard Report**  selects reports to add filters.
    
-   **Listen Filter**  refers to filter option available.
    
-   **Apply to field**  applies filter options to field column in a report.
    
**8**. Finally Click **Save** It will navigate to **save dashboard** section.

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_3.png)

Fill up save dashboard section;

-   **Name**  name identifier for dashboard created.
    
-   **Title**  title to refer the dashboard.
    
-   **Info**  summary information of the dashboard created.
    
-   **Privacy**  you can save the report in any one of the following privacy option.
    
    -   **Private ()**  Dashboard saved in private section and accessed by the user itself.
        
    -   **Public ()**  Dashboard saved in public section and accessed by all the users.
        
    -   **Share ()**  Dashboard saved under share section and accessed by specific set of users.

Select the tag in which you want to save **Dashboard Reports** and click on **Save.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_4.png) 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjc4Nzc1NjksMjIyMDcyNzIxXX0=
-->