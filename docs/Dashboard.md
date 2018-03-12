<center><h1>Dashboard</h1></center>

Dashboard provides access to view multiple reports in single dashboard layout, in this way it provides a quick view on related data. In order to make it more feasible to users, it is provided with set of global filters by making dashboard more interactive.

## View Dashboard

 To view the dashboard report created click on specific dashboard in dashboard section and it will navigate to the dashboard created.  
**1.**  Set the dashboard to home page by clicking on **Set on homepage** icon.

**2.** Edit the dashboard by clicking on **Edit** icon.

**3.** Delete the dashboard by clicking on **Delete** icon.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/b56b16b1de0a7088433221a92efcb565b3baae2e/images/view%20-dash.png)

## Create Dashboard

> Navigation : Dashboard→New Dashboard

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/20367797e10c5eabfec8ab65d23699fb34843101/images/dash.png)

 ## Step 1:  Customize Layout 
  
AcuBi has ability to create multiple report layouts, depending on the requirement. There layout formats are categorized in 2 ways.
- **Flow Layout** in this layout it is provided with a scroll bar option to define your layout appropriately.
- **Fixed Layout** in this layout all the reports will fit into single screen.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/4c3c6dabd96221095d0b54d5b2df37c49a919276/images/layout.png)

## Step 2: Add Reports

You can add different reports to the layout selected, depending on the requirement.

**4.** Click on **Update report** to add reports to layout.

**5.**  Click on **Apply Filters**  to add global filters and lookups.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ac1da552c0d05c08fa1aad5c0c1d07df190fd388/images/add_rep%5Borts.png)

## Step 3: Global Filters

Global filters are applicable on fields , which are applicable on reports.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ac1da552c0d05c08fa1aad5c0c1d07df190fd388/images/dash_filters.png)

## Dashboard filters

This Filters are applicable on dashboard reports and it supports the following filter types string, number, date, lookup.
**String** For fields that contain letters or special characters.
**Number** For fields that contain numbers.
**Date** For fields that contain dates.
**Lookup** to view the lookup in dashboard filters it should be defined in lookup section.

**6.**  **Dashboard Filters** allow user to view limited data.

-   **Filter Name**  identifier name to the filter applicable.
-   **Filter Type**  type of filter user (eg: string,date,number).
-   **Operator**  filter operation that are applicable.

## Lookup   

  **7.**   **Lookup** is a set of keys defined to filter the reports.they can be defined manually from a query or global parameters. Lookup can also be refereed based on the data provided.
   -   **Lookup name**  name of the lookup field.
   -   **Lookup Type**  refers to item or query type.
   -   **Test Lookup**  to test the lookup.
   -   **Multiple Selections**  refers to selection of list of multiple data.
    -   **Referred** The changes made on single lookup will be reflected on all the following reports based on it.
  >  For Example if we want to refer to country A then all states falling under that country will be updated based on the selection made.

  ## Report Listeners    
 
 8.  **Report Listeners**  Acubi has an ability to map global filters to report fields. on applying the global filters ,the filters will be reflected in the mapped fields in reports. at the same time you can apply multiple global filters on same fields or multiple fields.
   -  **Dashboard Report**  selects reports to add filters.
    -   **Listen Filter**  refers to filter option available.
    -   **Apply to field**  applies filter options to available field list in report.
     - **Add Listener**  adds multiple filters to reports.
     
9.  Click on  **Save Button**  to save the dashboard.
 
## Step 4: Privacy & Share option for Dashboards

Select the tag in which you want to save  **Dashboard Reports**  and click on  **Save.**
-   **Name**  name identifier for dashboard created.
-   **Title**  title to refer the dashboard.
-   **Info**  summary information of the dashboard created.
-   **Private ()**  report saved in private section and accessed by the user itself.
-   **Public ()**  the report is saved in public section and accessed by all the users.
-   **Share ()**  the report saved under share section and accessed by specific set of users.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/0fb2c0fe9fbc99b6ac2cd3d818fe7533a74872b8/images/2018-02-06_16-09-56.png)
## Edit / Delete Dashboard

10. Click  **Edit**  Button to make any changes to dashboard created.

11. Click on  **Delete icon**  to delete the dashboard created.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ac1da552c0d05c08fa1aad5c0c1d07df190fd388/images/dashboard.png)
## Dependency Filters

Dependency filters are used to retrieve set of filter values based on previous filter selection. the dependency should be mentioned in the filter query with a reference key from the previous filter.

## Listeners On / Off

If the listener is  **ON**  filter is applied and if it is  **OFF**  filters are not applicable. to carry out this function use  **Add Listener** Parameter.

## Maximize a Contained Report

12.  Click on  **Maximize icon**  in report tool bar.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI5MzA3NjIyXX0=
-->
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2NjcxMjk0OSw3NTEwNzY4OTIsMzM4OT
M0NTAsMTU0OTE4ODE1MywzMzg5MzQ1MF19
-->