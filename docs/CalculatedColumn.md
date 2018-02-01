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


**Trignometry:**
|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  acos | Calculate the inverse cosine of a value. | acos(0.5) = 1.0471975511965979, acos(cos(1.5)) =1.5 |
|  acosh | Calculate the hyperbolic arccos of a value, defined as acosh(x) = ln(sqrt(x^2 - 1) + x). | acosh(1.5) = 0.9624236501192069, acosh(x) = ln(sqrt(x^2 - 1) + x), where x = 1.5 |
|  acot | Calculate the inverse cotangent of a value, defined as acot(x) = atan(1/x). | acot(0.5) = 0.4636476090008061 |
|  acoth | Calculate the hyperbolic arccotangent of a value, defined as acoth(x) = atanh(1/x) = (ln((x+1)/x) + ln(x/(x-1))) / 2. | acoth(0.5) = 0.8047189562170503, acoth(x) = atanh(1/x) = (ln((x+1)/x) + ln(x/(x-1))) / 2.where x = 0.5 |
|  acsc | Calculate the inverse cosecant of a value, defined as acsc(x) = asin(1/x). | acsc(0.5) = 0.5235987755982989, acsc(math.csc(1.5)) =1.5<br/> |
|  acsch | Calculate the hyperbolic arccosecant of a value, defined as acsch(x) = asinh(1/x) = ln(1/x + sqrt(1/x^2 + 1)). | acsch(0.5) = 1.4436354751788103, acsch(x) = asinh(1/x) = ln(1/x + sqrt(1/x^2 + 1)), where x = 0.5 |
|  asec | Calculate the inverse secant of a value. | asec(0.5) = 1.0471975511965979 |
|  asech | Calculate the hyperbolic arcsecant of a value, defined as asech(x) = acosh(1/x) = ln(sqrt(1/x^2 - 1) + 1/x). | asech(0.5) = 1.3169578969248166, asech(x) = acosh(1/x) = ln(sqrt(1/x^2 - 1) + 1/x), where x = 0.5 |
|  asin | Calculate the inverse sine of a value. | asin(30) = 0.5, asin(45) = 0.7071068 |
|  asinh | Calculate the hyperbolic arcsine of a value, defined as asinh(x) = ln(x + sqrt(x^2 + 1)). | asinh(0.5) = 0.48121182505960347, asinh(x) = ln(x + sqrt(x^2 + 1)), where x = 0.5 |
|  atan | Calculate the inverse tangent of a value. | atan(0.5) = 0.4636476090008061, atan(math.tan(1.5)) = 1. |
|  atan2 | Calculate the inverse tangent function with two arguments, y/x. | atan2(2, 2) / math.pi = 0.25 |
|  atanh | Calculate the hyperbolic arctangent of a value, defined as atanh(x) = ln((1 + x)/(1 - x)) / 2. | atanh(0.5) = 0.5493061443340549, tanh(x) = ln((1 + x)/(1 - x)) / 2, where x = 0.5 |
|  cos | Calculate the cosine of a value. | cos(60) = 1/2 |
|  cosh | Calculate the hyperbolic cosine of a value, defined as cosh(x) = 1/2 * (exp(x) + exp(-x)) | cosh(90) = 6.1020164715892E+38, cosh(x) = 1/2 * (exp(x) + exp(-x))  where x = 90 |
|  cot | Calculate the cotangent of a value. | cot(45) = 1 |
|  coth | Calculate the hyperbolic cotangent of a value, defined as coth(x) = 1 / tanh(x). | coth(30) = 1, coth(x) = 1/tanh(x)  where x = 30  |
|  csc | Calculate the cosecant of a value, defined as csc(x) = 1/sin(x). | csc(30) = 2 |
|  csch | Calculate the hyperbolic cosecant of a value, defined as csch(x) = 1 / sinh(x). | csch(45) = 5.725037161098787e-20 .csch(x) = 1/sinh(x)  where x = 45 |
|  sec | Calculate the secant of a value, defined as sec(x) = 1/cos(x). | sec(60) = 2 |
|  sech | Calculate the hyperbolic secant of a value, defined as sech(x) = 1 / cosh(x). | sech(65) = 1.1800181083194122e-28, sech(x) = 1/cosh(x)  where  x = 65 |
|  sin |  Calculate the sine of a value. | sin(0) = 0,sin(90) = 1 |
|  sinh | Calculate the hyperbolic sine of a value, defined as sinh(x) = 1/2 * (exp(x) - exp(-x)). | sinh(30) = 5343237290762.231 sinh(x) = 1/2 * (exp(x) - exp(-x)) where  x = 30 |
|  tan | Calculate the tangent of a value. | tan(45) = 1 |
|  tanh | Calculate the hyperbolic tangent of a value, defined as tanh(x) = (exp(2 * x) - 1) / (exp(2 * x) + 1). | tanh(90) = 1,  tanh(90) = (exp(2 * x) - 1) / (exp(2 * x) + 1).  where x = 90 |
 
 **Utils**

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  to | Change the unit of a value. | to(x, unit) = to(math.unit('2 inch'), 'cm') = Unit 5.08 cm, to(math.unit(16, 'bytes'), 'bits') =  Unit 128 bits |
|  clone | Clone an object. | Clone(x) = Clone(math.complex('2-4i') = 2 - 4i, clone([[1, 2], [3, 4]]) = [[1, 2], [3, 4]] |
|  isInteger | Test whether a value is an integer number. | isInteger(2) = true, isInteger(0.5) = false, isInteger(math.complex('2-4i') = throws an error |
|  isNaN | Test whether a value is NaN (not a number). | isNaN(3) = false, isNaN(NaN) = true |
|  isNegative | Test whether a value is negative: smaller than zero. | isNegative(3) = false, isNegative(-2) = true |
|  isNumeric | Test whether a value is an numeric value. | isNumeric(2) = true, isNumeric([2.3, 'foo', false]) =  [true, false, true] |
|  isPositive | Test whether a value is positive: larger than zero. | isPositive(3) = true, isPositive([2, 0, -3]') = [true, false, false] |
|  isPrime | Test whether a value is prime: has no divisors other than itself and one. | <br/>isPrime(3) = true, isPrime([2, 17, 100]') = [true, true, false] |
|  isZero | Test whether a value is zero. | isZero(0) = true, isZero([2, 0, -3]') =  [false, true, false] |
|  typeof | Determine the type of a variable. | typeof(3.5) = number, typeof(math.complex('2-4i')) = complex, typeof(math.unit('45 deg')) = Unit, typeof('hello world') = string |
 
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
eyJoaXN0b3J5IjpbLTg0MDMwMDEwM119
-->