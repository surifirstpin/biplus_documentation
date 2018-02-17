<center><h1>Global Function</h1></center>

## Definition
 
A common set of statements or operations can be defined globally as a function and it can be retrieved and used in any project.

One global function shall be referred from another global function, But it should not be repeated in endlessly.

**Getting Started :** 

>Path :  Settings-->click on global functions. 
 1. Click on Add-Functions to create new function.
 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/d9712e86a6881444e961d60dfc6aab30bf665172/images/func1.png)

** Syntax : **
```
/* My Custom function*/

/*START*/ 
function myfunction_8(param1,param2)
{
 // Define function body   
   return 0;
}
/*END*/
```
**Example :**
```
/* My Custom function*/

/*START*/ 
function _Addition(param1,param2)
{
 var add =param1+param2;  
  return add;
}
/*END*/
/* Returns value 3, if we provide 1 and 2 in Test*/
```
2. Click on **Test** Button  to run the function.
3. Click on **Save** Button to save the function.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/2c15dfa03d8ed5eed5cdffdc1335c22ce759300c/images/global_functions.png)

## Ability to adopt Javascript

This functions supports all the native java script supported functions and also refer other global functions using " bi.Function_name."

## Edit Function

4. To **Edit** the function enable edit key.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/733be26f2d58ffc41ec83bc979234243c5417a2e/images/edit_func.png)

## Delete Function

5. To **Delete** the function click on delete button.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3e9f75a909b59664ffe91af0ad16c2c9859586cf/images/del_func.png)

## Developer Privileges

All the users have privilege to access global functions in calculated column,  but admin and developer can create, edit and delete a global function.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMzc3OTQ4NTJdfQ==
-->