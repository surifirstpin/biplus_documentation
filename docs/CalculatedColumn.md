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
|  **Statistics** |  |  |
|  **Name** | **Description** | **Usage & Example** |
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
|  **Date** |  |  |
|  **Name** | **Description** | **Usage & Example** |
|  date_to_week | Returns the week number in the year for the date given | bi.date_to_week(${col_name})<br/>Ex: bi.date_to_week(“2018-02-11”) = 7 |
|  date_to_month | Returns the month number in the year for the date given | bi.date_to_month(${col_name})<br/>Ex: bi.date_to_month(“2018-02-11”) = 2 |
|  date_to_quarter | Returns the quarter number in the year for the date given | bi.date_to_quarter(${col_name})<br/>Ex: bi.date_to_quarter(“2018-02-11”) = 1 |
|  date_to_year | Returns the year for the date given | bi.date_to_year(${col_name})<br/>Ex: bi.date_to_year(“2018-02-11”) = 2018 |
|  date_format | Returns the required format (supported by the database) of a date given | bi.date_format(${col_name}, “required_format”)<br/>Ex: bi.date_format(“2018-02-10 23:59:50”, “YYYY-MM”) = 2018-02 |
|  date_diff | Returns the number of days between two given dates | bi.date_diff(date1,date2) |
|  days_in_month | Returns the total number of days in a month for a given date / time stamp | bi.days_in_month (${Col_name})<br/>Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 28 |
|  days_till_month | Returns the total number of days completed in a month for a given date / time stamp | bi.days_till_month (${Col_name})<br/>Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 1 |
|  **Bit-wise Operators** |  |  |
|  **Name** | **Description** | **Usage & Example** |
|  bitAnd | Bitwise AND two values, x & y. Ex. bit And(x, y) | bi.bitAnd(53, 131) = 1 |
|  bitNot | Bitwise NOT value, ~x. | bi.bitNot(1) = -2, <br/>bi.bitNot([2,-3,4]) = [-3,2,5] |
|  bitOr | Bitwise OR two values, x | y. | bi.bitOr(1,2) = 3, <br/>bi.bitOr([1,2,3],4) = [5,6,7] |
|  bitXor | Bitwise XOR two values, x ^ y. | bi.bitXor(1, 2) = 3, <br/>bi.bitXor([2, 3, 4], 4) = [6,7,0] |
|  leftShift | Bitwise left logical shift of a value x by y number of bits, x << y. | bi.leftShift(1, 2) = 4, <br/>bi.leftShift([1, 2, 3], 4) = [16, 32, 64] |
|  rightArithShift | Bitwise right arithmetic shift of a value x by y number of bits, x >> y. | bi.rightArithShift(4, 2) = 1, <br/>bi.rightArithShift([16, -32, 64], 4) = [1, -2, 3] |
|  rightLogShift | Bitwise right logical shift of value x by y number of bits, x >>> y. | bi.rightLogShift(4, 2) = 1, <br/>bi.rightLogShift([16, -32, 64], 4) = [1, 2, 3] |
|  **Arithmetic :** |  |  |
|  **Name** | **Description** | **Example** |
|  abs | Returns the absolute value of a number<br/>It removed the -ve symbol for a negative value and displays the result as positive value | bi.abs(${Col_name})<br/>Ex: bi.abs(-2) = 2 |
|  add | Returns the value which obtained by adding the given list of values | bi.add(p1,p2,p3,.....)<br/>Ex: bi.add(3,4) = 7 |
|  cbrt | Returns the cuberoot value  of a give value | bi.cbrt(value)<br/>Ex: bi.cbrt(27) = 3 |
|  ceil | Returns the smallest integer greater than or equal to the given number | bi.ceil(value)<br/>Ex: bi.ceil(3.1) = 4 & bi.ceil(-8.5) = -8 |
|  cube | Returns the cube value of given value | bi.cube(value)<br/>Ex: bi.cube(3)=27 |
|  divide | Return the results after divides the two given values | bi.divide(m,n) = m/ n<br/>Ex: bi.divide(6,3) = 2 |
|  fix | Round the integer value for a given value towards zero. | bi.fix(value)<br/>Ex: bi.fix(4.5) = 4, fix(-4.5) = -4 |
|  floor | Round the integer value for given value towards minus infinity. | bi.floor(value)<br/>Ex: floor(2.8) = 2, floor(-7.5) = -8 |
|  dotDivide | Returns the value obtained after dividing two matrices element wise | For   a = [[9, 5], [6, 1]];<br/>       _b = [[3, 2], [5, 2]];<br/>bi.dotDivide(a, b)  returns [[3, 2.5], [1.2, 0.5]] |
|  dotMultiply | Returns the value obtained after multiplying two matrices element wise | For   a = [[9, 5], [6, 1]];<br/>       _b = [[3, 2], [5, 2]];<br/>bi.dotMultiple(a, _b)  returns [[27, 10], [30, 2]] |
|  dotPow | Return value after calculateing the power of x to y element wise. | For a = [[1, 2], [4, 3]];<br/>bi.dotPow(a, 2)   returns  [[1, 4], [16, 9]] |
|  exp | Retunr the exponentinal power of a value. | bi.exp(x)<br/>Ex: bi.exp(2) = 7.3890560989306495 |
|  gcd | Returns  the greatest common divisor for two or more values or arrays. | bi.gcd(a,b) = a.b/Lcm(a,b) <br/>Ex: For a= 8, b = 12 then bi.gcd(a,b) = 4 |
|  hypot | Returns the hypotenusa of a list with values. | bi.hypot = (p1,p2,p3..) <br/>Ex: bi.hypot (3,4) = sqrate_root ( square(3) + square(4) ) = 5 |
|  lcm | Returns the least common multiple for two or more values or arrays | bi.lcm(a,b)<br/>Ex: For a = 4,b = 6 then  bi.lcm(4,6) = 12 |
|  log | Returns the logarithm of a value (e-based). | bi.log(a)<br/>Ex: bi.log(10) = 2.3025850929 |
|  log10 | Returns the logarithm of a value (10-based). | bi.log10(a)<br/>Ex: bi.log10(10) = 1 |
|  mod | Returns the remainder of an integer division of two values(Calculates the modulus) | bi.mod(a,b)<br/>Ex: For a= 17, b= 3 then bi.mod(a,b) = 2 |
|  multiply | Returns the value obtained after multiplying the two or more given values | bi.multiply(p1,p2,p3,....)<br/>Ex: bi.multiply(3,4) = 3*4 =12 |
|  norm | Returns the norm of a number, vector or matrix | bi.norm(a)<br/>Ex: norm(-3.5) = 3.5, norm([[1, 2], [3, 4]], 1) returns 6 |
|  nthRoot | Returns the nth root calculation of given value. | bi.nthRoot(a,b)<br/>Ex: bi.nthRoot(9,2) = (3^2) = 9 |
|  pow | Returns the power value of the first parameter to the second parameter | bi.pow(a,b)<br/>Ex: bi.pow (5,3) = value of 5 to the power 3 = 125 |
|  round | Returns the rounded a value towards the nearest integer. | bi.round(A)<br/>Ex: bi.round(3.2) = 3 |
|  sign | Returns the sign of a value. | bi.sign(A)<br/>Ex: bi.sign (3.4) = 1 , bi.sign(-3,4)= -1 , bi.sign(0) = 0 , 1 when x > 1, -1 when x < 0, 0 when x == 0 |
|  sqrt | Returns the square root of given value. | bi.sqrt(x)<br/>Ex: bi.sqrt(25) = 5 |
|  square | Returns the square of given value. | bi.square(x)<br/>Ex: bi.square(5) = 25 |
|  unaryMinus | Returns the Inverse sign of a value, apply a unary minus operation. | bi.unaryMinus(x)<br/>Ex: bi.unaryMinus(3.5) = -3.5 & bi.unaryMinus(-4.2) = 4.2 |
|  subtract | Returns the value ontained after subtracting two given values | bi.substract(a,b)<br/>Ex: bi.subtract (4,3) = 4-3 = 1 |
|  unaryPlus | Returns the Inverse sign of a value, apply a unary plus operation. | bi.unaryPlus(x)<br/>Ex: bi.unaryPlus(3.44) = 3.44  |
|  xgcd | Returns the extended greatest common divisor for two values. | bi.xgcd(a,b) <br/>For Array type: Returns an array containing 3 integers [div, m, n] where div = gcd(a, b) and a*m + b*n = div<br/>Ex: For bi.xgcd(8,12) = [4,-1,1] |
|  **Matrix :** |  |  |
|  **Name** | **Description** | **Example** |
|  concat | Returns the array or text after concatenating two or more texts or matrices. | bi.concat(a,b)<br/>Ex: bi.concat(“Hello” ,”  World”) = “Hello  World”<br/>For  A = [[1, 2], [5, 6]] & B = [[3, 4], [7, 8]] <br/>bi.concat(A, B) = [[1, 2, 3, 4], [5, 6, 7, 8]] |
|  Cross | Returns the cross product for two vectors in three dimensional space. | cross(A, B) = [ a2 b3 - a3 b2, a3 b1 - a1 b3, a1 b2 - a2b1 ]  |
|  det | Returns the determinant of a matrix. | bi.det([[1, 2], [3, 4]]) = -2 |
|  dot | Returns the dot product of two vectors. | bi.dot(A, B) = a1 b1 + a2 b2 + a3 b3 + … + an bn, <br/>Ex: bi.dot([2, 4, 1], [2, 2, 3]) = 15 |
|  eye | Create a 2-dimensional identity matrix with size m x n or n x n. | eye(3) = [[1, 0, 0], [0, 1, 0], [0, 0, 1]], eye(3, 2) = [[1, 0], [0, 1], [0, 0]] |
|  filter | Filter the items in an array or one dimensional matrix. | filter([6, -2, -1, 4, 3], isPositive) = [6, 4, 3], <br/>Filter(["23", "foo", "100", "55", "bar"], /[0-9]+/) = ["23", "100", "55"] |
|  flatten | Flatten a multi dimensional matrix into a single dimensional matrix. | flatten([[1,2], [3,4]]) = [1, 2, 3, 4] |
|  forEach | Iterate over all elements of a matrix/array, and executes the given callback function. | forEach([1, 2, 3], function(value) { console.log(value);}); = 1,2,3 |
|  inv | Calculate the inverse of a square matrix. | inv(x) = inv(4); 1/4 = 0.25 |
|  kron | Calculates the kronecker product of 2 matrices or vectors. | kron([1,1], [2,3,4]) = [ [ 2, 3, 4, 2, 3, 4 ] ] |
|  map | Create a new matrix or array with the results of the callback function executed on each entry of the matrix/array. | map([1, 2, 3], function(value) { return value * value;}); = [1,4,9] |
|  ones | Create a matrix filled with ones. | ones(3) = [1, 1, 1], ones(3, 2) = [[1, 1], [1, 1], [1, 1]] |
|  partitionSelect | Partition-based selection of an array or 1D matrix. | function sortByLength (a, b) { return a.length - b.length;} partitionSelect(['Langdon', 'Tom', 'Sara'], 2, sortByLength); = 'Langdon' |
|  range | Create an array from a range. | range(2, 6) = [2, 3, 4, 5], <br/>range(2, -3, -1) = [2, 1, 0, -1, -2], <br/>range(2, 6, true) = [2, 3, 4, 5, 6] |
|  reshape | Reshape a multi dimensional array to fit the specified dimensions. | reshape(x, sizes) = var x = matrix([1, 2, 3, 4, 5, 6, 7, 8]);<br/>reshape(x, [2, 2, 2]); = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]] |
|  resize | Resize a matrix | resize(x, size, defaultValue) <br/>Ex: resize([1, 2, 3, 4, 5], [3]) = [1,2,3], <br/>       resize("hello", [8], "!") = 'hello!!!' |
|  size | Calculate the size of a matrix or scalar. | size(x) <br/>Ex: size('hello world') = [11], <br/>For var A = [[1, 2, 3], [4, 5, 6]] then size(A) = [2, 3] |
|  sort | Sort the items in a matrix. | sort(x, compare) = function sortByLength (a, b) {<br/>return a.length - b.length;<br/>} sort(['Langdon', 'Tom', 'Sara'], sortByLength); = ['Tom', 'Sara', 'Langdon'] |
|  squeeze | Squeeze a matrix, remove inner and outer singleton dimensions from a matrix. | squeeze(x) <br/>Ex: For var A = zeros(3, 1); = [[0], [0], [0]] (size 3x1)<br/>squeeze(A); = [0, 0, 0] (size 3) |
|  subset | Get or set a subset of a matrix or string. | subset(value, index, replacement [, defaultValue])<br/>Ex: For var e = [];<br/>var f = subset(e, index(0, [0, 2]), [5, 6]) then  f = [[5, 6]]<br/>var g = subset(f, index(1, 1), 7, 0) then g = [[5, 6], [0, 7]] |
|  trace | Calculate the trace of a matrix: the sum of the elements on the main diagonal of a square matrix. | trace(x) = trace([[1, 2], [3, 4]]); = 5 |
|  transpose | Transpose a matrix. | transpose(x)<br/>Ex: For  var A = [[1, 2, 3], [4, 5, 6]] then transpose(A); = [[1, 4], [2, 5], [3, 6]] |
|  zeros | Create a matrix filled with zeros. | var A = [[1, 2, 3], [4, 5, 6]];<br/>zeros(size(A)); = [[0, 0, 0], [0, 0, 0]] |
|  **Geometry:** |  |  |
|  **Name** | **Description** | **Example** |
|  distance | Results the eucledian distance between two points in 2 and 3 dimensional spaces. | distance([x1, y1], [x2, y2]) = distance([0,0], [4,4]) = 5.6569. |
|  **String:** |  |  |
|  **Name** | **Description** | **Example** |
|  format | Returns string format a value of any type, | bi.format(value) = 'value',<br/>Ex: bi.format(6.4)=’6.4’ & bi.format(21385, 2) = '21000' |
|  print | Return the results after interpolating a value into a string template | bi.print(“String $Value String”,{Value : number})<br/>Ex: bi.print('Lokes is $age years old', {age: 8}) returns<br/> 'Lokesh is 8 years old' |
|  **Relational:** |  |  |
|  **Name** | **Description** | **Example** |
|  compare | Returns -1, 1, 0 after comparing two given values<br/>Syntax: bi.compare(x,y) <br/>Returns -1 if x<y<br/>Returns 1 if x >y<br/>Returns 0 if x=y | bi.compare(6,2) = 1,<br/>bi.compare(2,6) = -1,<br/>bi.compare(6,6) = 0 |
|  compareNatural | Returns -1, 1, 0 after compare two values of any type in a deterministic, natural way. It accepts strings also.<br/>Syntax: bi.compareNatural(x,y) <br/>Returns -1 if x<y<br/>Returns 1 if x >y<br/>Returns 0 if x=y | bi.compareNatural('10', '2') = 1<br/>For var a = math.unit('5 cm');<br/>       var b = math.unit('40 mm');<br/>       bi.compareNatural(a, b) = 1<br/>bi.compareNatural([1, 2], [1, 2]) =0 |
|  deepEqual | Returns true / false after comparing the given values or list | bi.deepEqual(x,y)<br/>Ex: bi.deepEqual(6,8) = false , bi.deepEqual(6,6) = true<br/>For a = [2, 5, 1]  & b = [2, 7, 1] then bi.deepEqual(a, b) = false |
|  equal | Returns true / false after comparing the given values or list | bi.equal(x,y)<br/>Ex:  bi.equal(6,8) = false , bi.equal(6,6) = true<br/>For a = [2, 5, 1]  & b = [2, 7, 1] then bi.equal(a, b) = [true false true] |
|  larger | Returns true / false after validating larger value in the given values:<br/>true    -  if firstvalue is greater than second <br/>false   - if secondvalue is greater than first | bi.larger(x,y)<br/>Ex: bi.larger(2,3) = false,<br/>      bi.larger(4,3) = true |
|  smaller | Returns true / false after validating smaller value in the given values:<br/>true    -  if firstvalue is lesser than second <br/>false   - if secondvalue is lesser than first | bi.smaller(x,y)<br/>Ex: bi.smaller(2,3) = true,<br/>      bi.smaller(4,3) = false |
|  smallerEq | Returns true / false after validating smaller value in the given values: <br/>true    -  if firstvalue is  lesser or equal to the second  <br/>false   - if secondvalue is greater than first | bi.smallerEq(x,y)<br/>Ex: bi.smallerEq(2,3) = true & bi.smallerEq(3,3) = true<br/>      bi.smallerEq(4,3) = false |
|  unequal | Returns true / false after validating equality in the given values: <br/>true    -  if the values are not equal<br/>false   -  if the values are equal | bi.unequal(x,y)<br/>Ex: bi.unequal(2,3) = true & bi.unequal(3,2) = true<br/>      bi.unequal(3,3) = false |
|  **Trignometry:** |  |  |
|  **Name** | **Description** | **Example** |
|  sin | Returns the sine of a value. | bi.sin(value)<br/>Ex: bi.sin(0) = 0,bi.sin(90) = 1 |
|  cos | Returns the cosine of a value. | bi.cos(value)<br/>Ex: bi.cos(60) = 0.5 |
|  sec | Returns the secant of a value, <br/>Defined as sec(x) = 1/cos(x). | bi.sec(value)<br/>Ex: bi.sec(60) = 2 |
|  csc | Returns the cosecant of a value, <br/>Defined as csc(x) = 1/sin(x). | bi.csc(value)<br/>Ex: bi.csc(30) = 2 |
|  tan | Returns the tangent of a value.<br/>Defined as tan(x) = sin(x) / cos(x) | bi.tan(value)<br/>Ex: bi.tan(45) = 1 |
|  cot | Returns the cotangent of a value.<br/>Defined as cot(x) = 1 / tan(x) | bi.cot(value)<br/>Ex: bi.cot(45) = 1 |
|  sinh | Returns the hyperbolic sine of a value, <br/>Defined as sinh(x) = 1/2 * (exp(x) - exp(-x)). | bi.sinh(value)<br/>Ex: bi.sinh(30) = 5343237290762.231 |
|  cosh | Returns the hyperbolic cosine of a value, <br/>Defined as cosh(x) = 1/2 * (exp(x) + exp(-x)) | bi.cosh(value)<br/>Ex: bi.cosh(90) = 6.1020164715892E+38 |
|  sech | Returns the hyperbolic secant of a value, <br/>Defined as sech(x) = 1 / cosh(x). | bi.sech(value)<br/>Ex: sech(65) = 1.1800181083194122e-28 |
|  csch | Returns the hyperbolic cosecant of a value, <br/>Defined as csch(x) = 1 / sinh(x). | bi.csch(value)<br/>Ex: bi.csch(45) = 5.725037161098787e-20 |
|  tanh | Returns the hyperbolic tangent of a value, <br/>Defined as tanh(x) = (exp(2 x) - 1) / (exp(2 x) + 1). | bi.tanh(value)<br/>Ex: bi.tanh(90) = 1 |
|  coth | Returns the hyperbolic cotangent of a value, <br/>Defined as coth(x) = 1 / tanh(x). | bi.coth(value)<br/>Ex: bi.coth(30) = 1 |
|  asin | Returns the inverse sine of a value. | bi.asin(value)<br/>Ex: bi.asin(30) = 0.5 |
|  acos | Returns the inverse cosine of a value. | bi.acos(value)<br/>Ex: bi.acos(0.5) = 1.0471975511965979 &  bi.acos(bi.cos(1.5)) =1.5 |
|  asec | Returns the inverse secant of a value. | bi.asec(value)<br/>Ex: bi.asec(0.5) = 1.0471975511965979 |
|  acsc | Returns the inverse cosecant of a value, <br/>Defined as acsc(x) = asin(1/x). | bi.acsc(value)<br/>Ex: bi.acsc(0.5) = 0.5235987755982989 &, bi.acsc(bi.csc(1.5)) =1.5 |
|  atan | Returns the inverse tangent of a value. | bi.atan(value)<br/>Ex: bi.atan(0.5) = 0.4636476090008061, bi.atan(bi.tan(1.5)) = 1 |
|  acot | Returns the inverse cotangent of a value, <br/>Defined as acot(x) = atan(1/x). | bi.acot(value)<br/>Ex: bi.acot(0.5) = 0.4636476090008061 |
|  atan2 | Returns the inverse tangent function with two arguments, y/x. | bi.atan2(value)<br/>Ex:  |
|  asinh | Returns the hyperbolic arcsine of a value, <br/>Defined as asinh(x) = ln(x + sqrt(x^2 + 1)). | bi.asinh(value)<br/>Ex: bi.asinh(0.5) = 0.48121182505960347 |
|  acosh | Returns the hyperbolic arccos of a value, <br/>Defined as acosh(x) = ln(sqrt(x^2 - 1) + x). | bi.acosh(value)<br/>Ex: bi.acosh(1.5) = 0.9624236501192069 |
|  asech | Returns the hyperbolic arcsecant of a value, <br/>Defined as asech(x) = acosh(1/x) = ln(sqrt(1/x^2 - 1) + 1/x). | bi.asech(value)<br/>Ex: bi.asech(0.5) = 1.3169578969248166 |
|  acsch | Returns the hyperbolic arccosecant of a value, <br/>Defined as acsch(x) = asinh(1/x) = ln(1/x + sqrt(1/x^2 + 1)). | bi.acsch(value)<br/>Ex: bi.acsch(0.5) = 1.4436354751788103 |
|  atanh | Returns the hyperbolic arctangent of a value, <br/>Defined as atanh(x) = ln((1 + x)/(1 - x)) / 2. | bi.atanh(value)<br/>Ex: bi.atanh(0.5) = 0.5493061443340549 |
|  acoth | Returns  the hyperbolic arccotangent of a value, <br/>Defined as acoth(x) = atanh(1/x) = (ln((x+1)/x) + ln(x/(x-1))) / 2. | bi.acoth(value)<br/>Ex: bi.acoth(0.5) = 0.8047189562170503 |
|  **Unit :** |  |  |
|  **Name** | **Description** | **Example** |
|  to | Returns the converted unit value of a given value |  |
|  **Utils:** |  |  |
|  **Name** | **Description** | **Example** |
|  to | Change the unit of a value. | to(x, unit)<br/>Ex: to(math.unit('2 inch'), 'cm') = Unit 5.08 cm, <br/>      to(math.unit(16, 'bytes'), 'bits') = Unit 128 bits |
|  clone | Clone an object. | Clone(x) <br/>Ex: clone(math.complex('2-4i') = 2 - 4i, clone([[1, 2], [3, 4]]) = [[1, 2], [3, 4]] |
|  isInteger | Returns true / false after validating the given value is integer<br/>true if the given value is integer or else false | bi.inInteger(value)<br/>Ex: bi.isInteger(2) = true, <br/>       bi.isInteger(2.5) = false |
|  isNaN | Returns true / false after validating the given value  whether it is NaN (not a number) | bi.isNaN(value)<br/>Ex: bi.isNaN(3) = false, <br/>      bi.isNaN(NaN) = true |
|  isPositive | Returns true / false after validating the given value is positive<br/>true if the given value is integer or else false | bi.isPositive(value)<br/>Ex: bi.isPositive(3) = true, <br/>      bi.isPositive(-3) = false |
|  isNegative | Returns true / false after validating the given value is negative<br/>true if the given value is integer or else false | bi.isNegative(value)<br/>Ex: bi.isNegative(3) = false, <br/>      bi.isNegative(-3) = true |
|  isNumeric | Returns true / flase after validating the given value is numeric or not | bi.isNumeric(value)<br/>Ex: bi.isNumeric(3) = true, <br/>      bi.isNumeric(“string”) = false |
|  isPrime | Results true / false after validating  the given value is  whether a prime number | bi.isPrime(value)<br/>Ex: bi.isPrime(3) = true, <br/>       bi.isPrime(4) = false |
|  isZero | Results true / false after validating  the given value is  whether it is zero | bi.isZero(value)<br/>Ex: bi.isZero(1) = false, <br/>       bi.isZero(0) = true |
|  typeof | Determine the type of a variable. | typeof(3.5) = number, <br/>typeof(math.complex('2-4i')) = complex, <br/>typeof(math.unit('45 deg')) = Unit <br/>Typeof('hello world') = string |
|  **Constant :** |  |  |
|  **Name** | **Description** | **Example** |
|  e, E | Returns the Euler’s number, the base of the natural logarithm | 2.71828182845904 |
|  i | Returns Imaginary unit, defined as i*i = -1. A complex number is described as a + bi, where a is the real part, and b is the imaginary part. | sqrt(-1) |
|  Infinity | Returns Infinity, a number which is larger than the maximum number that can be handled by a floating point number. | Infinity |
|  LN2 | Returns the natural logarithm of 2. | 0.6931471805599451 |
|  LN10 | Returns the natural logarithm of 10. | 2.30258509299404 |
|  LOG2E | Returns the base-2 logarithm of E | 1.44269504088896 |
|  LOG10E | Returns the base-10 logarithm of E. | 0.43429448190325104 |
|  NaN | Not a number. | NaN |
|  null | Value null. | null |
|  phi | Phi is the golden ratio in math this is separately coded has unicode glyph ϕ | 1.61803398874989 |
|  pi, PI | Returns the value of pi which is a mathematical constant that is the ratio of a circle's circumference to its diameter. | 3.14159265358979 |
|  SQRT1_2 | Returns the square root of 1/2. | 0.707106781186547 |
|  SQRT2 | Returns the square root of 2. | 1.41421356237309 |
|  tau | Returns Tau value which is the ratio constant of a circle's circumference to radius, equal to 2 * pi. | 6.28318530717958 |
|  uninitialized | Constant used as default value when resizing a matrix to leave new entries uninitialized. |  |























**General :**
|  Name | Description | Usage & Example |
|  ------ | ------ | ------ |
|  offset | Return the row value of the column mentioned as before or after based on -Ve or +Ve number given | bi.offset(#{col_name}, row_difference) |
|  pivot_offset | Returns the cell value of pivot table based on the Row and Column position given respectively. |  |
|  Row number:  +Ve & -Ve are for below & above positions |  |  |
|  Column number : +Ve and -Ve are for after & before positions | bi.pivot_offset(#{col_name} ,m,n) |  |
|  for Instance: m is row number & n is column number |  |  |
|  contains | Returns true/ false after validating expression given inside | bi.contains(expression) |
|  row_total | Returns the total value in the row for the preceeding measures (before the present column) | bi.row_total ( ) |
|  col_total | Returns the total value of the column given inside () | bi.column_total(#{col_name}) |
|  number | Returns the object argument to a number that represents the object's value. The object may be static or a column name | bi.number(“static”) or bi.number(${col_name}) |
|  Ex: bi.number("1234567") returns  1234567 |  |  |
|  int | Returns only integer values of given number or column | bi.int(number) or bi.int(${col_name}) |
|  Ex: bi.int(74845.9898) = 74845 |  |  |
|  in_globals | It returns the data from Global parameters based on the common reference. The reference can be static or a column. | bi.in_globals(Ref ,”GP_Name.R_Val ”, ”Ref_key” ) |
|  Note: Ref can be a column name or static value or userid |  |  |
|  in_global_keys | It returns the data from Global parameters based on the multiple common references. The references can be static or a column. | bi.in_global_keys([“GP_Rkey1”,”GP_Rkey2”,.....],[Ref1, Ref2,.....],”GP_Name.R_Val”) |
|  Note: Ref1/ Ref2 can be static strings or column names or userid |  |  |
|  calculate_key_group | Returns an aggregated value of a measure based on a dimension with futher mention of Row grouping column name | bi.calculate_key_group(#Ag_col,$Ag_col,#RG_col,$RG_col,$M_col,”agg_type”) |
|  Where Ag= Aggregated & RG for Row Grouping  & M_Col for measure |  |  |
|  and agg_type can be sum, avg, min, max, count |  |  |
|  col_running_total | Returns the running total value for a column in each cell | bi.col_running_total(#{col_name}) |
|  col_running_avg | Returns the average value upto current cell for a column | bi.col_running_avg(#{col_name}) |

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
eyJoaXN0b3J5IjpbMTg0NDY3ODgxOV19
-->