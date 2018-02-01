Calculation is a statement or expression or a function operator which can be used to derive the column values, lets get deep into calculated column function.

## Usage of #math# 

Custom made mathematical operations.

### Syntax for using math functionality :

```
Check the number of working days in each month:

#math#
bi.days_in_month
(${ROOT.BI_ORDERS.date_month_WHENMADE}) 
```
```
To calculate the cubical value of the field

#math#
bi.cube(${ROOT.BI_ORDERS.count_AMOUNT})
```
**Similarly we can use all the below functionality Using Bi+:**
**General :**

|  **Name** | **Description** | **Example** |
|  ------ | ------ | ------ |
|  offset | Return the row value of the column mentioned as before or after based on -Ve or +Ve number given | offset(#{col_name}, row_difference) |
|  pivot_offset | Returns the total value in the row for the preceeding measures (before the present column) | pivot_offset(reference of given Column ,col_no,row_no) |
|  contains | Returns true if the Column mentioned contains the followed ‘Sub-String’, else it returns false | contains(given any name from the table like reference = "prabhas",if it is  present in the given col it gives true or else false) |
|  row_total | Returns the total value in the row for the preceeding measures (before the present column) | row_total ( ) |
|  col_total | Returns the total value of the column given inside () | column_total(#{col_name}) |
|  number | Returns number value of a string | number("1234567") it returns =1234567 |
|  int | Returns only integer values  | int(74845.9898) = 74845 |
|  in_globals | It returns the data from Global parameters  | in_globals(${colname}, #globalParameter.Requiredparam# ,"param") |
|  in_global_keys | It returns the data from Global parameters with  two or more references | in_global_keys(["param1","param2"], [reference1,reference2], "globalParameter.Requiredparam") |
|  calculate_key_group | Aggregates a measure value with respect to a dimension and futher allowing another dimension for Row Gouping. | calculate_key_group(colmun1, column2, column3, "aggregate function")   i.e agg_fun like = sum,avg etc |
|  col_running_total | You can use the SUM() formula combined with a clever use of absolute and relative references | col_running_total(#{col_name}) |
|  col_running_avg | You use the AVERAGE function. The only trick you need to apply is to make your range changing continuously. | col_running_avg(#{col_name}) |

**Constant :**
|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  e, E | Euler’s number, the base of the natural logarithm | 2.71828182845904 |
|  i | Imaginary unit, defined as i*i = -1. A complex number is described as a + bi, where a is the real part, and b is the imaginary part. | sqrt(-1) |
|  Infinity | Infinity, a number which is larger than the maximum number that can be handled by a floating point number. | Infinity |
|  LN2 | Returns the natural logarithm of 2. | 0.693147180559945 |
|  LN10 | Returns the natural logarithm of 10. | 2.30258509299404 |
|  LOG2E | Returns the base-2 logarithm of E | 1.44269504088896 |
|  LOG10E | Returns the base-10 logarithm of E. | 0.434294481903251 |
|  NaN | Not a number. | NaN |
|  null | Value null. | null |
|  phi | Phi is the golden ratio in math this is separately coded has unicode glyph ϕ | 1.61803398874989 |
|  pi, PI | The number pi is a mathematical constant that is the ratio of a circle's circumference to its diameter. | 3.14159265358979 |
|  SQRT1_2 | Returns the square root of 1/2. | 0.707106781186547 |
|  SQRT2 | Returns the square root of 2. | 1.41421356237309 |
|  tau | Tau is the ratio constant of a circle's circumference to radius, equal to 2 * pi. | 6.28318530717958 |
|  uninitialized | Constant used as default value when resizing a matrix to leave new entries uninitialized. |  |
## Usage of #math#plugin# for Grid View

            welcome to Biplus


## Arithmetic & Logical operations on Data Fields

            welcome to Biplus


## Usage of Global Functions with paramerts from Data Fields

            welcome to Biplus


## Usage of Global Parameters with reference from Data Field values

            welcome to Biplus


## Usage of Global Parameters with reference from Data Field values & Login Control

            welcome to Biplus


## Calculate on Raw functionality

            welcome to Biplus
 

## Calc column with Pivot Option On /Off

            welcome to Biplus

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjkzNDU0NjcxXX0=
-->