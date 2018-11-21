

<center><h1>Dashboard</h1></center>

Dashboard provides access to view multiple reports in single dashboard layout, in this way it provides a quick view on related data. In order to make it more feasible to users, it is provided with set of global filters by making dashboard more interactive and can re-arrange the titles. After configuring a dashboard to your interest, you can share it with your team. You can create as many dashboards as you want, so you can alter each dashboard to the specific needs of the people who use it.

## View Dashboard

After login into AcuBi Home Page, Click on Dashboard section.
 it consist of list of dashboards and reports saved under Tag Structure.

 - To view the existing dashboard click on, Dashboard name from the available list. it consist of number of layouts used and global filters used for the same dashboard reports.
 
> **Note** : Dashboard are identified with **Tachometer icon.**

## Create Dashboard

**1.** Click    **Dashboard Section**    then Click on **New Dashboard** Button on top right of the screen. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_1.png)

**2.** Select the suitable **layout** from available layout options on left side of the screen.

   **Layout formats are categorized in 2 ways,**
   
- **Flow Layout** This layout is provided with a scroll bar option to define your layout appropriately.

- **Fixed Layout** All the reports in this layout will fit into single screen.

**3.** Click on **Update Report** to add reports to the selected layout. 

   **There are 2 ways you can add reports to the layout;**

   **a)** Click on report layout section and select the report you want to **add** to the layout.

   **b)** Click on **add** link available at right side of the saved report. 

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_2.png)

**4.**  Click **Apply Filters** button it will navigate to  global dashboard filters and lookup section.

 **5.** **Dashboard global Filters** allows user to view limited data by applying filters on dashboard reports and it supports following filter types string, number, date and lookup.
 
|  **Type** | **Description** |
|  ------ | ------ |
|  String | For fields that contain letters or special characters. |
|  Number | For fields that contain numbers. |
|  Date | For fields that contain dates. |
|  Lookup | To view the lookup in dashboard filters it should be defined in lookup section. |

**Fill up the dashboard global section;**

  -   **Filter Name**  identifier name to the filter applicable.

  -   **Filter Type**  type of filter used ( Eg: string, date, number).

  -   **Operator**  filter operation that are applicable.

**6.** Adding lookup to dashboard will refer set of query or list of items in filters.

**Fill up the lookup section ;**

   -   **Lookup name**  name of the lookup field.
   
    -   **Lookup Type**  refers to item or query type.
   
    -   **Test Lookup**  to test the lookup.
   
    -   **Multiple Selections**  enables the selection of list, for multiple data.

   
## Dependency Filters

You can refer the existing lookup, based on which a new lookup is created to retrieve the data based on referred lookup. In this way  you can extract the data depending on referred lookup field.

   -   **Referred** on selecting the referred checkbox the following lookup will extract the data based on the previously created lookup for which the referred checkbox is enabled.
 
**7.** **Report Listeners** 

The Listeners option allows to register callbacks to be notified when an event is detected on a specific label.
**For instance** if a filter is defined for dashboard containing 2 reports and listener is added on particular field for report_1 it results in filter applied on report_1 it self and report_2 will remain unaffected.

**Fill Up Report Listener Section ;**

   -  **Add Listener**  adds multiple filters to reports.

   -   **Dashboard Report**  selects reports to add filters.
    
   -   **Listen Filter**  refers to filter option available.
    
   -   **Apply to field**  applies filter options to field column in a report.
    
**8.** Finally Click **Save** It will navigate to **Save Dashboard** section.

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_3.png)

****Fill up save dashboard section :****

   -   **Name**  name identifier for dashboard created.
                              
   -   **Title**  title to refer the dashboard.
    
   -   **Info**  summary information of the dashboard created.
    
   -   **Privacy**  you can save the report in any one of the following privacy option.
    
       -  **Private()** It enable access for user itself.
  
       -  **Public()**   It enable access for all the users. 
  
       -  **Share()** It enable access for specific set of users.
  
Select the tag in which you want to save **Dashboard Reports** and click on **Save.**

![
](https://raw.githubusercontent.com/sv18042016/fp1/90511a882ffd694c16d44cb8f74b6f97e9db823e/images/create_dash_ur_4.png) 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg4MTkxNTcyMywxNDM4MjkzMTQwLDEwND
UxNTUwOTIsMTc4NDA0NDgyLDgyMjQzOTA3NCwyMDI4NjgxMzc4
LDU4MTE3NTQ5MCw4NDM5MjA1MTQsLTE4MjUyNzI1MDUsMzg1OT
gzMzgxLDM2ODU5NzQyOSwxMzk2NjI3MTMzLDE5MjIyOTE4MzIs
MTY3NTg4ODUwMCwtMjEwNDc5MjEyLDUwODU1MzUsMjIyMDcyNz
IxXX0=
-->