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
|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  offset | Return the row value of the column mentioned as before or after based on -Ve or +Ve number given | bi.offset(#{col_name}, row_difference) |
|  pivot_offset | Returns the cell value of pivot table based on the Row and Column position given respectively.<br/>Row number:  +Ve & -Ve are for below & above positions<br/>Column number : +Ve and -Ve are for after & before positions | bi.pivot_offset(#{col_name} ,m,n)<br/>for Instance: m is row number & n is column number |
|  contains | Returns true/ false after validating expression given inside | bi.contains(expression) |
|  row_total | Returns the total value in the row for the preceeding measures (before the present column) | bi.row_total ( ) |
|  col_total | Returns the total value of the column given inside () | bi.column_total(#{col_name}) |
|  number | Returns the object argument to a number that represents the object's value. The object may be static or a column name | bi.number(“static”) or bi.number(${col_name})<br/>Ex: bi.number("1234567") returns  1234567 |
|  int | Returns only integer values of given number or column | bi.int(number) or bi.int(${col_name})<br/>Ex: bi.int(74845.9898) = 74845 |
|  in_globals | It returns the data from Global parameters based on the common reference. The reference can be static or a column.  | bi.in_globals(Ref ,”GP_Name.R_Val ”, ”Ref_key” )<br/>Note: Ref can be a column name or static value or userid |
|  in_global_keys | It returns the data from Global parameters based on the multiple common references. The references can be static or a column.  | bi.in_global_keys([“GP_Rkey1”,”GP_Rkey2”,.....],[Ref1, Ref2,.....],”GP_Name.R_Val”)<br/>Note: Ref1/ Ref2 can be static strings or column names or userid |
|  calculate_key_group | Returns an aggregated value of a measure based on a dimension with futher mention of Row grouping column name | bi.calculate_key_group(#Ag_col,$Ag_col,#RG_col,$RG_col,$M_col,”agg_type”)<br/>Where Ag= Aggregated & RG for Row Grouping  & M_Col for measure<br/>and agg_type can be sum, avg, min, max, count |
|  col_running_total | Returns the running total value for a column in each cell | bi.col_running_total(#{col_name}) |
|  col_running_avg | Returns the average value upto current cell for a column | bi.col_running_avg(#{col_name}) |

### Statistics
|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  unequal | Returns true / false if the inputs given are not equal. | bi.unequal(m,n)<br/>Returns true if m=n else false |
|  mad | Retruns the Median Absolute Deviation for the inputs | bi.mad(p1,p2,p3,......)<br/>Ex: bi.mad(100,200) = 50 |
|  max | Returns the maximum value of a matrix or a list with values. | bi.max(p1,p2,p3,.....)<br/>Ex: bi.max(100,200,300) = 300 |
|  mean | Returns the mean value of a list of values mentioned | bi.mean(p1,p2,p3)<br/>Ex: bi.mean(100,200,300) = 200 |
|  median | Returns the median value of a list of values mentioned | bi.median(p1,p2,p3,.....) |
|  mode | Retruns the values which are repeated in the list mentioned | bi.mode(p1,p2,p3,.....)<br/>Ex: bi.mode(1,2,1)=1 |
|  prod | Returns the product values of the mentioned values | bi.prod(p1,p2,p3,p4,....)<br/>Ex: bi.prod(p1,p2,p3) = p1 * p2 * p3 |
|  quantileSeq | Returns prob order quantile of a matrix or a list with values | bi.quantileSeq(A, prob[, sorted]) |
|  std | Returns the standard deviation of a matrix or a list with values. | bi.std(p1,p2,p3 ...)<br/>bi.std(A)<br/>bi.std(A, normalization) |
|  sum | Returns the sum of list of values mentioned | bi.sum(p1,p2,p3,.....)<br/>Ex: bi.sum(p1,p2,p3) = p1 + p2 +p3 |
|  var | Returns the variance of a matrix or a list with values | bi.var(p1,p2,p3)<br/>Ex: bi.var(2, 4, 6) = 4 |
 
### Date

|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  date_to_week | Returns the week number in the year for the date given | bi.date_to_week(${col_name})<br/>Ex: bi.date_to_week(“2018-02-11”) = 7 |
|  date_to_month | Returns the month number in the year for the date given | bi.date_to_month(${col_name})<br/>Ex: bi.date_to_month(“2018-02-11”) = 2 |
|  date_to_quarter | Returns the quarter number in the year for the date given | bi.date_to_quarter(${col_name})<br/>Ex: bi.date_to_quarter(“2018-02-11”) = 1 |
|  date_to_year | Returns the year for the date given | bi.date_to_year(${col_name})<br/>Ex: bi.date_to_year(“2018-02-11”) = 2018 |
|  date_format | Returns the required format (supported by the database) of a date given | bi.date_format(${col_name}, “required_format”)<br/>Ex: bi.date_format(“2018-02-10 23:59:50”, “YYYY-MM”) = 2018-02 |
|  date_diff | Returns the number of days between two given dates | bi.date_diff(date1,date2) |
|  days_in_month | Returns the total number of days in a month for a given date / time stamp | bi.days_in_month (${Col_name})<br/>Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 28 |
|  days_till_month | Returns the total number of days completed in a month for a given date / time stamp | bi.days_till_month (${Col_name})<br/>Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 1 |
### Bitwise Operator
|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  bitAnd | Bitwise AND two values, x & y. Ex. bit And(x, y) | bi.bitAnd(53, 131) = 1 |
|  bitNot | Bitwise NOT value, ~x. | bi.bitNot(1) = -2, <br/>bi.bitNot([2,-3,4]) = [-3,2,5] |
|  bitOr | Bitwise OR two values, x | y. | bi.bitOr(1,2) = 3, <br/>bi.bitOr([1,2,3],4) = [5,6,7] |
|  bitXor | Bitwise XOR two values, x ^ y. | bi.bitXor(1, 2) = 3, <br/>bi.bitXor([2, 3, 4], 4) = [6,7,0] |
|  leftShift | Bitwise left logical shift of a value x by y number of bits, x << y. | bi.leftShift(1, 2) = 4, <br/>bi.leftShift([1, 2, 3], 4) = [16, 32, 64] |
|  rightArithShift | Bitwise right arithmetic shift of a value x by y number of bits, x >> y. | bi.rightArithShift(4, 2) = 1, <br/>bi.rightArithShift([16, -32, 64], 4) = [1, -2, 3] |
|  rightLogShift | Bitwise right logical shift of value x by y number of bits, x >>> y. | bi.rightLogShift(4, 2) = 1, <br/>bi.rightLogShift([16, -32, 64], 4) = [1, 2, 3] |
###

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
eyJoaXN0b3J5IjpbLTYyMzE4ODQyMF19
-->