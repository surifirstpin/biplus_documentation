

 <center><h1>Admin Settings</h1></center>
cbhfhf
AcuBi administrative settings allows you to customize AcuBi for your organisation.

Here is how to get started with administrative settings and its features.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d61beb27f6c032b0573919bc8b1806668f9b6d97/images/full_admin1.png)

## Getting started with Administration

Steps to follow;

**1.** To view the existing user profile, Click on Profile section available on left hand side. 

**2.** To change the password Click on **Forgot Password** on left hand side.

**3.** To create a new user click on **Users** and Click **Add user** on top right of the screen. Admin has an ability to **create, edit and delete** the **users.**
 
**Enter the below information once you navigate to user page;**

- **Email** Enter email id for the user.

- **Password** Enter a password to access.

- **FirstName** Enter first-name of the user.

- **LastName** Enter lastname of the user. 

- **Company** Enter name of the company.

- **Role** Select the suitable role from the drop down list ( Admin, Developer, User, Super Admin) .

| User Role |  Access|
|--|--|
| **Admin** | Create,edit,delete users,groups,global parameter,global function |
|**Developer**|Create,edit,delete reports or dashboards and change global parameters and functions|
|**User**|view reports and can edit them if provided access to the specific model|
|**Manager**|view reports and edit them if provided access to the specific model|

- **Enabled** on selecting enabled check box this specific user login is accessed or it will be disabled for login.

- Click on **Save** button to save user.

![
](https://raw.githubusercontent.com/sv18042016/fp1/cdd2483566966ccdd9bf8fdb0404076c90a7fc09/images/full_userd.png)

## Edit or Delete User

To Edit or Delete already existing user as per your business requirement, Go back to Users main screen ( Which display list of user existing )  and select **Edit** to make any changes to user profile  or click **Delete** Icon to permanently delete a user from database.

![
](https://raw.githubusercontent.com/sv18042016/fp1/1f49ce0c89ffb5873eef9fcb340937f15e101560/images/full_edit_user.png)

## Groups

 For providing access to particular content in database, for set of people in the the organisation, we need to create group with all the users falling under that particular group.

Here are the steps to follow;
To create a group click on **Add Group**, and mention below details;

**Enter the below information :**

- **Group Name** name identifier for group name.

- **Users** select  users for group.

- Click **Save** button to save group.

![
](https://raw.githubusercontent.com/sv18042016/fp1/3114f27feb369a1d0df91c6dd0e8dab965a0b6da/images/full_group.png)

## Edit or Delete Group

To Edit or Delete already existing group as per your business requirement, Go back to groups main screen (Which display list of groups existing)  and select **Edit** icon to make changes to already existing group or click **Delete** to permanently delete the group from database.

## Global Parameters

AcuBi allows you to provide additional key values to manipulate the data in calculations column, control data etc. 

 **Existing Features of Global Parameters;**
- Control data access based on login.
- Provide access to predefined list of filter values based on login.
- Manipulate data with external parameter based on a common reference.
- View and manipulate data based on login.
- Use global parameters in calculated column to perform mathematical calculations on existing data.

**Steps to Create Global Parameters :**

To create a global parameters Click **Global Parameters**, and Click on **Add Key.** Enter specific **key name** as shown in the pop-up screen below, then Click **OK** button.

![
](https://raw.githubusercontent.com/sv18042016/fp1/358cf93ac803463e1de7a9de99fda806615ab45d/images/full_global_para.png)
 
 - Click on **Add column** to add table data ( strings or Numbers).
 - Click on **Add Row** to increase the table rows.
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/0972156040148c1e863bc4456d9705e52cf046b5/images/full_global_para1.png)

 **For Instance:**

|Test  |Test1  |
|--|--|
| Abc | 1 |
|Pqr  | 2 |

![
](https://raw.githubusercontent.com/sv18042016/fp1/0972156040148c1e863bc4456d9705e52cf046b5/images/add_column.png)

- Click on **Browse** to import external data using excel sheet.

![
](https://raw.githubusercontent.com/sv18042016/fp1/315833fba561101dcd95aa6d0ad9560694aeff02/images/browse_gp.png)

>**Note :** By default all the columns in uploaded file will be saved as string type. 

- Select the column name and click on **Edit** button to change column name as shown in image below.

![
](https://raw.githubusercontent.com/sv18042016/fp1/315833fba561101dcd95aa6d0ad9560694aeff02/images/upload_gp.png) 

 Change the column name and column type as per your business requirement as shown in below image :
 
![
](https://raw.githubusercontent.com/sv18042016/fp1/d9f487e8bcb13f913640bdce2a7030f7b519167a/images/para2.png)

Similarly edit column cell value by clicking on specific cell as shown below.

![
](https://raw.githubusercontent.com/sv18042016/fp1/90ce2c5c848ba57722a38cdfb7623b6037e12058/images/para3.png)

By clicking on **Code View**, The uploaded file displays the data in JSON Format.

![
](https://raw.githubusercontent.com/sv18042016/fp1/7ca7febb2aec49c8c334dbe0ba8301fc146905ca/images/Json.png)

- Click on **Save** button to save global parameters.

## check case

If **check case** is enabled, global parameters become case sensitive for key mapping in calculated column.

- To edit global parameters click on **Edit** button.
- To delete global parameter click on **Delete** button.

![
](https://raw.githubusercontent.com/sv18042016/fp1/b1569c9d8cc1d909d7b645a3e6e2ec3c21453852/images/checkcase.png)

## Global Functions

A common set of statements or operations can be defined globally as a function. it can be retrieved and used in any project. One global function shall be referred from another global function, But it should not be in circular reference.  

All the users have privilege to access global functions in calculated column, but admin and developer has an ability to create, edit and delete a global function.

To create a global function Click on **Global function** section available.

**1.**  Click on **Add-Functions** to create a new custom global function.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d9712e86a6881444e961d60dfc6aab30bf665172/images/func1.png)

```
                                  * My Custom function *
/*START*/ 

function myfunction(param1,param2,ParamN)
{
                                * Define function body *  
   return 0;
   
}
/*END*/
```
> **Note :** You can add your code in function body only.

 **For Instance**  Create a custom function for adding 2 parameters


```
                                  * My Custom function *
/*START*/ 

function _Addition(param1,param2)

{
 var add =param1+param2;  
  return add;
}
/*END*/
```
 **Note** : Provide 1 and 2 in **Test** section, it results **3** as shown in below image.

**2.** Click on **Test** Button  to run the function.

**3.** Click on **Save** Button to save the function.

![
](https://raw.githubusercontent.com/sv18042016/fp1/2c15dfa03d8ed5eed5cdffdc1335c22ce759300c/images/global_functions.png)

Global functions supports all the native java script supported functions and also refer other global functions using  **bi.function_name** ( param1, param2, ...., paramN).

**4.**  Enable edit key to **Edit** the function as per your requirements.

**5.** Click  delete button to **Delete** the function.

![
](https://raw.githubusercontent.com/sv18042016/fp1/d82a8c27ff4c376dad7db79873f75867a4e49aca/images/edit_func.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTcwMzIyMDI4Miw1MzQzNTMxNDEsMTM0NT
g2NTcxNywtOTM5MjYyMDczLDIxMTg0NjM0ODEsMjAxNjQ0MTM2
OSwxNDczNzAwMDMwLC0yMDkzNTgxNDIzLDM5ODMxMzQ5NiwtMT
QzMjQ0MzMyMywyMDY5NTc2NDYsMTk5NzY5MDkwOCwtMTQwNTg5
NDgyNSwxNDMxNTYwNTY0LDE2NDMxNDY4ODYsLTE5NDAxMzk2OT
QsLTE2MTExMTQyNjksMTcxNjUzNzE2MywtMjAzMjc5MDkwMyw1
MzYyMTY4MjJdfQ==
-->