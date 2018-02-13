<center><h1>Calculated Column</h1></center>

##  Definition

A functionality which allows to manipulate the retrieved data using arithmetical, logical, text-based and date-based functions and then displays it in the required format. Calculated columns will show up as green in the data table, rather than as blue (dimensions), or orange (measures). Just like regular dimensions and measures, calculated columns are controlled from display in visualizations.

**Usage:**

1) Supports a wide variety of arithmetical and logical functions to be applied on the data.
2) Calculates using the data from external parameters (through "Global parameters") by making reference to the database field(s). 
3) Controls or access the data with user wise calculations,
4) Optimize and transform the data using #plugin# functionality.
5) Allows to define a function or use a Global function to be applied on the required data fields.
 
> Note: The functions support JavaScript API.


## Usage of #math# 

Custom made mathematical operations can be added in calculated column section as shown below


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/4a3a039bae7badccb31d41bbc9c5449943045474/images/calculate.png)

**Check the number of working days in each month :**
```
#math#
bi.days_in_month
(${ROOT.BI_ORDERS.date_month_WHENMADE}) 
```
**To calculate the cubical value of the field :**
```
#math#
bi.cube(${ROOT.BI_ORDERS.count_AMOUNT})
```
**Similarly we can use all the below functionality Using Bi+:**
### General
|  **Name** | **Description ** | **Usage & Example** |
|  :------: | :------: | :------: |
|  offset | Return the row value of the column mentioned as before or after based on   -Ve or +Ve number given | bi.offset(#{col_name}, row_difference) |

### Statistics

### Date


### Bitwise Operator

### Arithmetic


### Matrix


### Geometry


### String



### Relational


### Trignometry


### Unit

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  to | Returns the converted unit value of a given value |  |

### Utils

#### Constant

## Usage of #math#plugin# for Grid View

            welcome to Biplus


## Arithmetic & Logical operations on Data Fields

You can perform Arithmetic operation to the desired fields in calculated columns.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/60036e93167331ca3442d5bb10ff48209b021fdd/images/arth_add.png)


## Calculate Custom Functions

it will execute a series of actions on a database record and returns a particular value.
 
 **Syntax**

 ```
 #math#
/*START*/

function Fname(input_param1,input_param2,.....){

Statement 1;
Stetement 2;
......
.....
return Outpur_value;
}
/*END*/
bi._Fname(input_param1, input_param2,.......)
```

## Access Global Parameters
 
 Global parameter is a flat file used to manipulate,control and organize the data which is not available in database and accessed this data in report.
 
 While calculating an expression over a database value using field reference.
 
**Syntax** 

 ```
 bi.in_global_keys(["ParameterColumnName"],["DatabaseValue"],"ParameterName.Field"])
```

- **Parameter Column Name** Refer the key name from global parameter.

-  **Database Value** Refers database value.

- **Parameter Name Field** Returns the field from global parameter it is applicable in 3 different ways;

  
 **1.  Static value** Global parameters refers to a static value.
 
  **Syntax :**
  
 ```
  bi.in_global_keys( ["Parameter_Column_Name "],["Reference string" ],"Global_parameter.field")
```

  **Example :**
```
#math#
bi.in_global_keys( ["Station_Name"],["Station_1" ],"Calc_ONRAW.value")
```

**2. Reference value** Global parameters refers to reference value.
       
  **Syntax :**
```
  bi.in_global_keys( ["Parameter_Column_Name "],["database column" ],"Global_parameter.field")
```
  **Example :**
```
#math#
bi.in_global_keys( ["Station_Name"],[${ROOT.AUTOTEST_ORDERS.STATIONCODE_724} ],"Calc_ONRAW.value")
```

**3. Login Name(User Id)** Provide Access based on Login ID.
   
**Syntax :** 
```
bi.in_global_keys(["ParameterColumnName","ParameterUserID"],["DatabaseField","bi._globals("#userid#")"],"ParameterName.Field"])
```
**Example :**
```
#math#
bi.in_global_keys( ["UserName","Login_name"],[${ROOT.EMPLOYEES.NAME_661} 
,bi._globals("#userid#")],"CalcCol_Stage2.SeizeLimit)

```
## Calculate on Raw functionality

If calculate raw is enabled even after grouping the calculation is applied to each and every record and displays the final result.
If disabled the calculation will be done after the grouping.
```
${ROOT.BI_ORDERS.sum_AMOUNT}+2
```
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/fe0920a5f1e6abcabfab1c22ce5d8a5df08ee789/images/on_ram.png)

## Calculate column with Pivot Offset

Now you want to look at the quantity_sum difference by each month for specific customer then select customer_id,add pivot to  month.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/cfd94b0b9fe7b31888a3c426882590bae7914fc4/images/pivot_offset.png)

We can get quantity_sum difference of each month for specific customer using Pivot_Offset() function.

${ROOT.BI_ORDERS.sum_QUANTITY} -bi.pivot_offset( #{ROOT.BI_ORDERS.sum_QUANTITY} ,0,-1)
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eb64533dd879286986c2b3f4a9f69295ab96da8b/images/pivot_offset2.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY1NzQyNjgwN119
-->