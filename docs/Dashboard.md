<center><h1>Dashboard</h1></center>

Dashboard provides access to view multiple reports in single dashboard layout, in this way it provides a quick view on related data. In order to make it more feasible to users, it is provided with set of global filters by making dashboard more interactive and can re-arrange the titles. After configuring a dashboard to your interest, you can share it with your team. You can create as many dashboards as you want, so you can alter each dashboard as per your business requirement.

## View Dashboard

 To view a saved dashboard report navigate to dashboard section and select the dashboard report to open it.
   
**1.**  To set the dashboard to home page click on **Set on homepage** icon.

**2.** To edit dashboard click on **Edit** icon.

**3.** To delete dashboard click on **Delete** icon.


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/b56b16b1de0a7088433221a92efcb565b3baae2e/images/view%20-dash.png)
 **Image 1**
## Create Dashboard

> **Navigation : Dashboard→ New Dashboard**


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/20367797e10c5eabfec8ab65d23699fb34843101/images/dash.png)
**Image 2**

 ## Step 1:  Customize Layout 
   
AcuBi has ability to create multiple report layouts, depending on the requirement. There layout formats are categorized in 2 ways.
- **Flow Layout** in this layout it is provided with a scroll bar option to define your layout appropriately.
- **Fixed Layout** in this layout all the reports will fit into single screen.
**a.** To navigate to next page click right arrow.
**b.** To navigate to previous page click left arrow.

![
](https://raw.githubusercontent.com/sv18042016/fp1/df105942aecfbe1db3c5c4504b45a3444323caf9/images/layout.png)
**Image 3**

## Step 2: Add Reports

You can add different reports to the layout selected, depending on the requirement.

**4.** Click **Update Report** to add reports to layout. You can add reports to layout in 2 ways.(refer image 4)

   **a.** Click on report layout section then select the report you want to add in layout.

   **b.** Click **add** to add new layout to existing one.
   

![
](https://raw.githubusercontent.com/sv18042016/fp1/dd00678604bb2220939239b3abcd5e2e359936b3/images/dashboard_layout.png)

**Image 4**

## Step 3: Dashboard Global Filters

**5.**  Click on **Apply Filters** to add global dashboard filters and lookups. **(Refer image 4)**
 
 **6.** **Dashboard global Filters** allows user to view limited data by applying filters on dashboard reports. **(Refer Image 5)**
-   **Filter Name**  identifier name for the filter applicable.

-   **Filter Type**  type of filter used (String,date,number).

    - **String** For fields that contain letters or special characters.

    - **Number** For fields that contain numeric values.

    - **Date** For fields that contain dates.

    - **Lookup** to view the lookup in dashboard filters it should be defined in lookup section. **( Refer point 7)**
   
    -   **Operator**  filter operation applicable on data.

**7.**   **Lookup**  Adding lookup to dashboard will refer set of query or list of items in filters.**( Refer image 5)**

   -   **Lookup name**  name of the lookup field.
   
   -   **Lookup Type**  refers to item or query type.
   
   -   **Test Lookup**  to test the lookup.
   
   -   **Multiple Selections**  enables the selection of list of multiple data.

## Dependency Filters

You can refer the existing lookup and create a new lookup to retrieve the data data based of the referred lookup.

   -   **Referred** on selecting the referred checkbox the following lookup will extract the data based on the previously created lookup for which the referred checkbox is enabled.
   
   
  >  **For Instance** if we want to refer to country A then all states falling under that country will be updated based on the selection made.

**8.**     **Report Listeners** **( Refer image 5)**

The Listeners option allows to register callbacks to be notified when an event is detected on a specific label.
 
  AcuBi has an ability to assign a defined filters to report column (fields of views based on which the report is created). For suppose if a filter is defined for dashboard containing 2 reports and listener is added on particular field for report 1, it is applicable only on report 1 and report 2 will remain unaffected.

   -  **Dashboard Report**  selects reports to add filters.
   
   -   **Listen Filter**  refers to filter option available.
   
   -   **Apply to field**  applies filter options to available field list in report.
   
   - **Add Listener**  adds multiple filters to reports.
   
**9.**    Click **Save Button**  to save the dashboard
 **( Refer image 5).**


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ac1da552c0d05c08fa1aad5c0c1d07df190fd388/images/dash_filters.png)
**Image 5**

## Step 4: Privacy & Share option for Dashboards 

Select the tag in which you want to save  **Dashboard Reports**  and click on  **Save.** **(Refer image 6)**

-   **Name**  name identifier for dashboard created.

-   **Title**  title to refer the dashboard.

-   **Info**  summary information of the dashboard created.

- **Privacy**  you can save the report in any one of the following privacy option.

  -   **Private**  Dashboard saved in private section and accessed by the user itself.

  -   **Public**  Dashboard saved in public section and accessed by all the users.

  -   **Share**  Dashboard saved under share section and accessed by specific set of users.


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/0fb2c0fe9fbc99b6ac2cd3d818fe7533a74872b8/images/2018-02-06_16-09-56.png)
 **Image 6**
 
## Edit / Delete Dashboard

**10.** Click  **Edit**  Button to make changes to dashboard created.

> **Note :** After editing the dashboard click on **update** button to save the changes made.

**11.** Click on  **Delete icon**  to delete the dashboard created.

**12.** To create a new dashboard report click on **New Dashboard** icon.

**13.** To set dashboard to full screen , Choose **Full screen** from the list.

> **Note :** You can also edit, delete or create new dashboard  using **Bars icon** 

![
](https://raw.githubusercontent.com/sv18042016/fp1/5b86a054406ca26550a23a1c524c998d71b60505/images/dashboard_fullscreen.png)
**Image 7**

## Dashboard for Mobile Device

AcuBi make it easier to view the dashboard list, in mobile devices easily and it consist of following features;

- Displays dashboard list.
- Displays dashboard report data.
- You can add more filters to report.

![
](https://raw.githubusercontent.com/sv18042016/fp1/a11e40d845baa1742caa99ef8bec4ed3db8eed14/images/mobile_device.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5ODc0MzI3MDYsLTk2ODg4MzQ5LDU4Nj
U0MzE4MiwxMTc1MTk0NDU5LC0xMDcyMjE2ODIxLC0xNzI0NTY2
MjAzLDEzNzQ1MDc5NjMsMTc3MDkwNzk0NywxODY1ODEzNDksLT
M3MDM5OTIxNiwxNTE4ODgxOTIxLDEyOTM3NzExMDgsMjE0NDcx
MTk5NCwxNTQzOTI5MjcyLC0xNjk2NDM2NzgxLDE1NzEyMjM1MT
csLTE4MDgzOTM5ODUsNzkxMTMwOTQwLDg2NjUxMzIzMCwxNzM5
NzY0NDU0XX0=
-->