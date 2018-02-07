Calculation is a statement or expression or a function operator which can be used to derive the column values, lets get deep into calculated column function.

## Usage of #math# 

Custom made mathematical operations can be added in calculated column section as shown below


![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/4a3a039bae7badccb31d41bbc9c5449943045474/images/calculate.png)

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

**Statistics**

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  unequal | Test whether two values are unequal. | math.unequal(2 + 2, 3) = true, math.unequal(2+3,5) = false;  |
|  mad | Compute the median absolute deviation of a matrix or a list with values. | math.mad(10, 20, 30); mean = 20,math.mad = <code>&amp;#124;</code>10-20<code>&amp;#124;</code>,<code>&amp;#124;</code>20-20<code>&amp;#124;</code><code>&amp;#124;</code>30-20<code>&amp;#124;</code> = 20/3 = 6.666 |
|  max | 	Compute the maximum value of a matrix or a list with values. | math.max(2, 1, 4, 3) = 4,math.min(2.6, 7.1, -4.5, 2.0, 4.1) = -4.5,math.max(2.4,7.1,-2.8,5.4) = 7.1  |
|  mean | Compute the mean value of matrix or a list with values. | math.mean(2, 1, 4, 3) = 2+1+4+3/4 = 10/4 = 2.5, |
|  median | Compute the median of a matrix or a list with values. | math.median(5, 2, 7) = 5,math.median([3, -1, 5, 7]) = 4 |
|  mode | Computes the mode of a set of numbers or a list with values(numbers or characters). | math.mode(2, 1, 4, 3, 1) = 1,No of times Repeated Number |
|  prod | Compute the product of a matrix or a list with values. | math.prod(2, 3) = 6,math.prod(2,3,4) = 24; |
|  quantileSeq | Compute the prob order quantile of a matrix or a list with values. | math.quantileSeq(2,4,4,5,5,6,7,8,9), mean = 5, LowerQua = 4+4/2 = 4, HigherQua = 7+8/2 = 7.5, Q = HQ-LQ = 3.5 |
|  std | Compute the standard deviation of a matrix or a list with values. | x = (6,2,3,1),xbar = 6+2+3+1/4 = 3,​SD = root<code>&amp;#124;</code>x-xbar<code>&amp;#124;</code>^2/n,SD = 1.87<br/>xbar = mean |
|  sum | Compute the sum of a matrix or a list with values. | sum(2, 1, 4, 3) = 10 |
|  var | Compute the variance of a matrix or a list with values. | var(2, 4, 6) = 4, var([2, 4, 6, 8], 'uncorrected') = 5, |

**Date**

|  **Name** | **Description** | **Example** |
|  ------ | ------ | ------ |
|  date_to_week | Returns the number of current day week in the year | date_to_week(Give reference to month_date)   |
|  date_to_quarter | Returns the Quarter number for current date or the month parameter given inside () | date_to_quarter-> it returns quarter number like Q1,Q2,Q3,Q4 |
|  date_to_year | Returns the Year value for current date or the month parameter given inside () | date_to_year("2017-10-22")   it returns  only  year = 2017 |
|  date_to_month | Returns the Month Number for current date or the month parameter given inside () | date_to_month("2017-10-23")--> it returns month number = 10 |
|  date_format | Returns the required format of a date parameter mentioned after it & inside () | date_format(To_date,'YYYY-MM-DD') |
|  date_diff | Returns the number of days between two dates given inside () | date_diff("2017-10-20" to "2017-10-23") = 3 |
|  days_in_month | Returns the total number of days completed in the present month including today | days_in_month (january) = 31 |
|  days_till_month | Returns the total number of days completed in the present month including today | days _till_month(october) = 23 it shows  how many days completed in given month |

**Bit-wise Operators**

|  **Name** | **Description** | **Example** |
|  ------ | ------ | ------ |
|  bitAnd | Bitwise AND two values, x & y. Ex. bit And(x, y) | bitAnd(53, 131) = 1 |
|  bitNot | 	Bitwise NOT value, ~x. | bitNot(1) = -2, bitNot([2,-3,4]) = [-3,2,5] |
|  bitOr | Bitwise OR two values, x <code>&amp;#124;</code> y. | bitOr(1,2) = 3, bitOr([1,2,3],4) = [5,6,7] |
|  bitXor      | Bitwise XOR two values, x ^ y. | bitXor(1, 2) = 3, bitXor([2, 3, 4], 4) = [6,7,0] |
|  leftShift | Bitwise left logical shift of a value x by y number of bits, x << y. | leftShift(1, 2) = 4, leftShift([1, 2, 3], 4) =  [16, 32, 64] |
|  rightArithShift | Bitwise right arithmetic shift of a value x by y number of bits, x >> y. | rightArithShift(4, 2) = 1, rightArithShift([16, -32, 64], 4) = [1, -2, 3] |
|  rightLogShift | Bitwise right logical shift of value x by y number of bits, x >>> y. | rightLogShift(4, 2) = 1, rightLogShift([16, -32, 64], 4) = [1, 2, 3] |

**Arithmetic :**

|  **Name** | **Description** | **Example** |
|  ------ | ------ | ------ |
|  abs | Calculate the absolute value of a number | abs(-12) = 12 |
|  add | Add two or more values, x + y | add(3,4) = 7 |
|  cbrt | Calculate the cubic root of a value. | cbrt(27) = 3 |
|  ceil | The smallest integer greater than or equal to the given number | ceil(3.1) = 4,ceil(-8.5) = -8 |
|  cube | Compute the cube of a value, x * x * x. | cube(7) = 343 |
|  divide | Divides the two values | divide(6,3) = 2 |
|  fix | Round a value towards zero. | fix(4.5) = 4, fix(-4.5) = -4 |
|  floor | Round a value towards minus infinity. | floor(2.8) = 2, floor(-7.5) = -8 |
|  dotDivide         | Divide two matrices element wise. | dotDivide(x, y) dotDivide(2, 4) = 0.5 |
|  dotMultiple | Multiply two matrices element wise | dotMultiply(x, y) dotMultiply(2, 4) = 8 |
|  dotPow | Calculates the power of x to y element wise. | dotPow(x, y) var a = [[1, 2], [4, 3]], dotPow(a, 2) = [[1, 4], [16, 9]] |
|  exp | Calculate the exponent of a value. | exp(x), exp(2) = 7.3890560989306495 |
|  gcd | Calculate the greatest common divisor for two or more values or arrays. | gcd(a,b) = a.b/Lcm(a,b) where a,b = (8,12) , gcd = 4 |
|  hypot | Calculate the hypotenusa of a list with values. | hypot = (v1,v2,v3..vn) = Vi square = square root of (v1 square + v2 square) = hypot (3,4) = 5 |
|  lcm | Calculate the least common multiple for two or more values or arrays | lcm(a,b) = abs(a*b)/gcd(a,b) = where a,b = (4,6), lcm = 12 |
|  log | Calculate the logarithm of a value. | log(-1) = NaN, log(0) = -Infinity, log(1) = 0, log(10) = 2.3025850929 |
|  log10 | Calculate the 10-base logarithm of a value. | log10 = log10 // function(x) { return log(x) *LOG10E; }; log10(1) = 0 |
|  mod | Calculates the modulus, the remainder of an integer division. | 17 mod 3 = 2 because 17/3 = 5 rem 2 which is 17 = 3*5+2 |
|  multiply | Multiply two or more values, x * y. | multiply = 3*4 =12 |
|  norm |  Calculate the norm of a number, vector or matrix | abs(-3.5) = 3.5, norm(-3.5) = 3.5, norm([[1, 2], [3, 4]], 1) = returns 6 |
|  nthRoot | Calculate the nth root of a value. | nthRoot(9,2) = (3^2) = 9 |
|  pow |  pow(x, y), pow(2, 3) = 8. | pow (5,3) = 125   where x = 5 and y = 3  and  pow = The value of x to the power y  |
|  round | Round a value towards the nearest integer. | round(3.2) = 3,round(3.8) = 4, round(-4.2) = -4 |
|  sign | Compute the sign of a value. |  sign (3.4) = 1 , (-3,4)= -1 , (0) = 0  ,  1 when x > 1, -1 when x < 0,  0 when x == 0  |
|  sqrt | Calculate the square root of a value. | sqrt(25) = 5, square(5) = 25, sqrt(-4) = Complex 2i |
|  square | Compute the square of a value, x * x | square([1, 2, 3, 4]);  returns Array [1, 4, 9, 16] |
|  unaryMinus | Inverse the sign of a value, apply a unary minus operation. | unaryMinus(x) = unaryMinus(3.5) = -3.5, unaryMinus(-4.2) = 4.2 |
|  subtract | Subtract two values, x - y. |  subtract (4-3) = 1 |
|  unaryPlus | Unary plus operation. | unaryPlus(3.44) = 3.44 , unary Plus(40 - 6) = 34 |
|  xgcd | Calculate the extended greatest common divisor for two values. | xgcd(a,b) where div = gcd(a,b) and a*m + b*n = div, xgcd(8,12) = [4,-1,1], gcd(8,12) = 4 |

**Matrix :**

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  Concat | Concatenate two or more matrices. | var A = [[1, 2], [5, 6]], var B = [[3, 4], [7, 8]]  concat(A, B) = [[1, 2, 3, 4], [5, 6, 7, 8]] |
|  Cross | Calculate the cross product for two vectors in three dimensional space. | cross(A, B) = [ a2 * b3 - a3 * b2, a3 * b1 - a1 * b3, a1 * b2 - a2 * b1 ] , cross([1, 1, 0],   [0, 1, 1]) = [1, -1, 1] |
|  det | Calculate the determinant of a matrix. | det([[1, 2], [3, 4]]) = -2 |
|  dot | Calculate the dot product of two vectors. | dot(A, B) = a1 * b1 + a2 * b2 + a3 * b3 + … + an * bn, dot([2, 4, 1], [2, 2, 3]) = 15 |
|  eye | Create a 2-dimensional identity matrix with size m x n or n x n. | eye(3) = [[1, 0, 0], [0, 1, 0], [0, 0, 1]], eye(3, 2) = [[1, 0], [0, 1], [0, 0]] |
|  filter | Filter the items in an array or one dimensional matrix. | filter([6, -2, -1, 4, 3], isPositive) = [6, 4, 3], filter(["23", "foo", "100", "55", "bar"], /[0-9]+/) = ["23", "100", "55"] |
|  flatten | Flatten a multi dimensional matrix into a single dimensional matrix. | flatten([[1,2], [3,4]]) = [1, 2, 3, 4] |
|  forEach | Iterate over all elements of a matrix/array, and executes the given callback function. | forEach([1, 2, 3], function(value) { console.log(value);}); = 1,2,3 |
|  inv | Calculate the inverse of a square matrix. | inv(x) = inv(4); 1/4 = 0.25 |
|  kron | Calculates the kronecker product of 2 matrices or vectors. | kron([1,1], [2,3,4]) = [ [ 2, 3, 4, 2, 3, 4 ] ] |
|  map | Create a new matrix or array with the results of the callback function executed on each entry of the matrix/array. | map([1, 2, 3], function(value) { return value * value;}); = [1,4,9] |
|  ones | Create a matrix filled with ones. | ones(3) = [1, 1, 1], ones(3, 2) = [[1, 1], [1, 1], [1, 1]] |
|  partitionSelect | Partition-based selection of an array or 1D matrix. | function sortByLength (a, b) { return a.length - b.length;} partitionSelect(['Langdon', 'Tom', 'Sara'], 2, sortByLength); = 'Langdon' |
|  range | Create an array from a range. | range(2, 6) = [2, 3, 4, 5], range(2, -3, -1) = [2, 1, 0, -1, -2], range(2, 6, true) = [2, 3, 4, 5, 6] |
|  reshape | Reshape a multi dimensional array to fit the specified dimensions. | <br/>reshape(x, sizes) = var x = matrix([1, 2, 3, 4, 5, 6, 7, 8]);reshape(x, [2, 2, 2]); = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]] |
|  resize | Resize a matrix | resize(x, size, defaultValue) = resize([1, 2, 3, 4, 5], [3]) = [1,2,3], resize("hello", [8], "!") = 'hello!!!' |
|  size | Calculate the size of a matrix or scalar. | size(x) = size('hello world') =  [11], var A = [[1, 2, 3], [4, 5, 6]];size(A); = [2, 3] |
|  sort | Sort the items in a matrix. | sort(x, compare) = function sortByLength (a, b) {<br/>  return a.length - b.length;<br/>} sort(['Langdon', 'Tom', 'Sara'], sortByLength); = ['Tom', 'Sara', 'Langdon'] |
|  squeeze | Squeeze a matrix, remove inner and outer singleton dimensions from a matrix. | squeeze(x) = var A = zeros(3, 1); = [[0], [0], [0]] (size 3x1)<br/>squeeze(A); = [0, 0, 0] (size 3) |
|  subset | Get or set a subset of a matrix or string. | subset(value, index, replacement [, defaultValue]) = var e = [];<br/>var f = subset(e, index(0, [0, 2]), [5, 6]);  f = [[5, 6]]<br/>var g = subset(f, index(1, 1), 7, 0);  g = [[5, 6], [0, 7]] |
|  trace | Calculate the trace of a matrix: the sum of the elements on the main diagonal of a square matrix. | trace(x) =  trace([[1, 2], [3, 4]]); = 5 |
|  transpose | Transpose a matrix. | transpose(x) = var A = [[1, 2, 3], [4, 5, 6]]; = transpose(A); = [[1, 4], [2, 5], [3, 6]] |
|  zeros | 	Create a matrix filled with zeros. | var A = [[1, 2, 3], [4, 5, 6]];<br/>zeros(size(A)); = [[0, 0, 0], [0, 0, 0]] |

**Geometry**:

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  distance | Calculates: The eucledian distance between two points in 2 and 3 dimensional spaces. | distance([x1, y1], [x2, y2]) = distance([0,0], [4,4]) = 5.6569. |

**String:**

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  format | Format a value of any type into a string. | format(6.4) = '6.4',format(21385, 2) = '21000' |
|  print | Interpolate values into a string template | print('Lokes is $age years old', {age: 8}); 'Lokesh is 8 years old' |

**Relational**

|  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  compare | Compare two values. | compare(6> 1) = 1,compare(2 < 3) = -1,compare(7 = 7) = 0,it returns only 1,-1,0 |
|  compareNatural | Compare two values of any type in a deterministic, natural way. | it is also same as Compare but compareNatural('10' > '2') = 1,compareNatural([1, 2, 4], [1, 2, 3]); return 1 |
|  deepEqual | Test element wise whether two matrices are equal. | math.deepEqual(6, 8) = false,a = [2 3 4],b = [2 5 4]; math.deepEqual(a,b) = false; |
|  equal | Test whether two values are equal. | math.Equal(2+4,6) = true,a = [2 3 4],b = [2 5 4]; math.Equal(a,b) = [true false true]; |
|  larger | Test whether value x is larger than y. | math.larger(2, 3) = math.larger(2>3) = false,math.larger(2+5,4) = math.larger(6>4) = true; |
|  smaller | Test whether value x is smaller than y. | math.smaller(2, 3) = math.smaller(2 < 3) = true,math.smaller(5, 2 * 2) = math.smaller(5 < 4) = false; |
|  smallerEq | Test whether value x is smaller or equal to y. | math.smallerEq(1 + 2, 3) = math.smallerEq(3 <= 3) = true; |
|  unequal | Test whether two values are unequal. | math.unequal(2 + 2, 3) = true, math.unequal(2+3,5) = false;  |

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
 
 **Unit :**

 |  Name | **Description** | **Example** |
|  ------ | ------ | ------ |
|  to | Change the unit of a value. | to(x, unit) = to(math.unit('2 inch'), 'cm') = Unit 5.08 cm, to(math.unit(16, 'bytes'), 'bits') =  Unit 128 bits |

 **Utils:**

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

You can perform Arithmetic operation to the desired fields in calculated columns.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/60036e93167331ca3442d5bb10ff48209b021fdd/images/arth_add.png)


## Usage of Global Functions with parameters from Data Fields



## Usage of Global Parameters with reference from Data Field values & Login Control
 
 Global parameter is a flat file used to manipulate,control and organised the data retrieved from database.it can be used in three ways:
 1. 


## Calculate on Raw functionality


## Calc column with Pivot Option On /Off

            welcome to Biplus

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMzkyMDA5NzJdfQ==
-->