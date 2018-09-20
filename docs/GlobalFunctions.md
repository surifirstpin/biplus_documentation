<center><h1>Global Function</h1></center>

A common set of statements or operations can be defined globally as a function and it can be retrieved and used in any project. One global function shall be referred from another global function, But it should not be in circular reference.
All the users have privilege to access global functions in calculated column,  but admin and developer has an ability to create, edit and delete a global function.

>**Navigation :  Settings → Global functions** 

**1.** Click on **Add-Functions** to create new function.
 

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/d9712e86a6881444e961d60dfc6aab30bf665172/images/func1.png)

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
                                           * Returns value 3, if we give 1 and 2 in Test*
```

>  **Note :** To undo the changes done for the code established click  **Undo** icon.  To redo the changes done for the code click  **Redo** icon.


**2.** Click on **Test** Button  to run the function.

**3.** Click on **Save** Button to save the function.



![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/2c15dfa03d8ed5eed5cdffdc1335c22ce759300c/images/global_functions.png)

## Ability to adopt Javascript

This functions supports all the native java script supported functions and also refer other global functions using  **bi.function_name** ( param1, param2, paramN).

## Edit Function

**4.**  Enable edit key to **Edit** the function.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/733be26f2d58ffc41ec83bc979234243c5417a2e/images/edit_func.png)

## Delete Function

**5.** Click on delete button to **Delete** the function.


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3e9f75a909b59664ffe91af0ad16c2c9859586cf/images/del_func.png)


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTMwMDU0MTYyNSwxMTg2NTQzNjQ5LC0xNT
I2NTA4NzQsMTQ1NDg3MDA4LC0xMTMzMTYzNTk2LDU3ODQ5MjA4
Myw2NTk2OTMxMjcsMTY1MDUzMjc2MV19
-->