 <center><h1>Calculated Column</h1></center>

Table calculations enable you to easily create on-the-fly metrics, which are similar to formulas found in Excel sheets. These extracted columns will be shown up in green colour, in the data table. Using calculated column you can perform mathematical, logical (true/false), lexical (text-based), and date-based calculations on the dimensions, measures, and other table calculations in your query. 

### Functionalities of Calculated Column

- It supports wide variety of arithmetical and logical functions to be applied on the data.

- It is calculated, using the data from external parameters (through "Global parameters") by making reference to the database fields. 

- It controls or access the data with user wise calculations.

- Optimize and transform the data using  **#plugin#**  functionality.

- Define a function or use a global function, to be applied on the required data fields.
 
> **Note:** The functions support JavaScript API.

### Deriving Expression

Click on **Calculated Column** button it will navigate to calculated column window,

![
](https://raw.githubusercontent.com/sv18042016/fp1/9dd01207f083d272ba2269a4c999dfa8976f1914/images/calculate%20column1.png)

Once navigated to Calculated Column Window, Enter the below fields.

- **Field name** unique identifier name to refer calculated column.

- **Label** specify a identifier name to calculated column the way it should be displayed in the data table.

- **Data type** data type format for the result (string,number).

- **Field type** derives whether the result is dimension or measure.

- **Calculation** Derive a expressions, enter $ symbol in calculation window, it will display list of functions and fields available for executing arithmetical & logical expressions in calculated column section or else you can choose your functionality manually by selecting the suitable functions available on right side of the screen.

```
$(Root.BI_DELIVERYREPORT.sum_ORDERVALUE}+2000
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/aff2f17d1b5383de542a7b534df7caeb69c03b3d/images/calculated_col_window.png)


-  **Calculate on Raw data :**   if enabled the calculation is applied on all rows irrespective of grouping and pivot, if disabled calculation applied on abstract values.


![
](https://raw.githubusercontent.com/sv18042016/fp1/f9a2efaca57be8f52d3ff9d6c02291f6be8b2b70/images/calculate%20_expression.png)

- Click **Ok** after deriving an expression,  all the values based on calculation, is shown up in green colour as shown in below image,


![
](https://raw.githubusercontent.com/sv18042016/fp1/394d53042fd86efdc7a2f16a79e69b6434c9260f/images/calcu+result.png)


## Mathematical operation 

Custom made mathematical operations can be performed in **calculated column section.**

**Example 1 :**

 To Calculate **Number of working days** in each month, use the following expression in calculation column window as shown below ;

```
bi.days_in_month(${ROOT.BI_ORDERS.date_month_WHENMADE}) 
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/e7895f0d4e17c8c8cbdccd25330829252949ae5b/images/cal_example.png)


**AcuBi supports following functionalities in calculated column :**

### General
| **Name**| **Description**  | **Usage and  Example**|
|--|--|--|
|Offset  |Return the row value of the column mentioned as before or after based on  -Ve or +Ve number given  | bi.offset(#{col_name}, row_difference) |
|pivot_offset|Returns the cell value of pivot table based on the Row and Column position given respectively.Row number:  +Ve & -Ve are for below & above positions Column number : +Ve and -Ve are for after & before positions|bi.pivot_offset(#{col_name} ,m,n) for Example: m is row number & n is column number|
|Contains|Returns true/ false after validating expression given inside|bi.contains(expression)|
|row_total|Returns the total value in the row for the preceding measures (before the present column) |bi.row_total ( )|
|col_total|Returns the total value of the column given inside ()|bi.column_total(#{col_name})|
|number|Returns the object argument to a number that represents the object's value.The object may be static or a column name|bi.number(“static”) or bi.number(${col_name}) Ex: bi.number("1234567") returns  1234567|
|int|Returns only integer values of given number or column|bi.int(number) or bi.int(${col_name})Ex: bi.int(74845.9898) = 74845|
|in_globals|Returns the data from Global parameters based on the common reference. The reference can be static or a column|bi.in_globals(Ref ,”GP_Name.R_Val ”, ”Ref_key” ) **Note:** Ref can be a column name or static value or userid|
|in_global_key|it returns the data from global parameters based on the multiple common references.this references can be static or column|bi.in_global_keys ([“GP_Rkey1”,”GP_Rkey2”,.....],[Ref1, Ref2,.....], ”GP_Name.R_Val”) Note: Ref1/Ref2 can be static strings or column names or userid|
|calculate_key_group|Returns an aggregated value of a measure based on a dimension with further mention of row grouping column name|bi.calculate_key_group (#Ag_col,$Ag_col,#RG_col,$RG_col,$M_col,”agg_type”) Where Ag= Aggregated & RG for Row Grouping  & M_Col for measure and agg_type can be sum, avg, min, max, count|
|col_running_total|Returns the running total value for a column in each cell|bi.col_running_total(#{col_name})|
|col_running_avg|Returns the average value up to current cell for a column|bi.col_running_avg(#{col_name})|

### Statistics
|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  unequal | Returns true / false if the inputs given are not equal. | bi.unequal(m,n)<br/>Returns true if m=n else false |
|  mad | Returns the Median Absolute Deviation for the inputs | bi.mad(p1,p2,p3,......)<br/>Ex: bi.mad(100,200) = 50 |
|  max | Returns the maximum value of a matrix or a list with values. | bi.max(p1,p2,p3,.....)<br/>Ex: bi.max(100,200,300) = 300 |
|  mean | Returns the mean value of a list of values mentioned | bi.mean(p1,p2,p3)<br/>Ex: bi.mean(100,200,300) = 200 |
|  median | Returns the median value of a list of values mentioned | bi.median(p1,p2,p3,.....) |
|  mode | Returns the values which are repeated in the list mentioned | bi.mode(p1,p2,p3,.....)<br/>Ex: bi.mode(1,2,1)=1 |
|  prod | Returns the product values of the mentioned values |bi.prod(p1,p2,p3,p4,....) Ex: bi.prod(p1,p2,p3) = p1 * p2 * p3|
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
|  date_format | Returns the required format (supported by the database) of a date given |bi.date_format(${col_name}, “required_format”) Ex: bi.date_format(“2018-02-10 235950”, “YYYY-MM”) = 2018-02 |
| date_diff | Returns the number of days between two given dates | bi.date_diff(date1,date2) |
| days_in_month | Returns the total number of days in a month for a given date / time stamp | bi.days_in_month (${Col_name}) Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 28 |
| days_till_month | Returns the total number of days completed in a month for a given date / time stamp | bi.days_till_month (${Col_name})Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 1 |

### Bitwise Operator

|  **Name** | **Description** | **Usage & Example** |
|  :------: | :------: | :------: |
|  bitAnd | Bitwise AND two values, x & y. Ex. bit And(x, y) | bi.bitAnd(53, 131) = 1 |
|  bitNot | Bitwise NOT value, ~x. | bi.bitNot(1) = -2, <br/>bi.bitNot([2,-3,4]) = [-3,2,5] |
|  bitOr | Bitwise OR two values, x&#124 y.| bi.bitOr(1,2) = 3, <br/>bi.bitOr([1,2,3],4) = [5,6,7] |
|  bitXor | Bitwise XOR two values, x ^ y. | bi.bitXor(1, 2) = 3, <br/>bi.bitXor([2, 3, 4], 4) = [6,7,0] |
|  LeftShift | Bitwise left logical shift of a value x by y number of bits, x << y. | bi.leftShift(1, 2) = 4, <br/>bi.leftShift([1, 2, 3], 4) = [16, 32, 64] |
|  RightArithShift | Bitwise right arithmetic shift of a value x by y number of bits, x >> y. | bi.rightArithShift(4, 2) = 1, <br/>bi.rightArithShift([16, -32, 64], 4) = [1, -2, 3] |
|  RightLogShift | Bitwise right logical shift of value x by y number of bits, x >>> y. | bi.rightLogShift(4, 2) = 1, <br/>bi.rightLogShift([16, -32, 64], 4) = [1, 2, 3] |

### Arithmetic

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  abs | Returns the absolute value of a number<br/>It removes negative symbol for a negative value and displays the result as positive value | bi.abs(${Col_name})<br/>Ex: bi.abs(-2) = 2 |
|  add | Returns the value which obtained by adding the given list of values | bi.add(p1,p2,p3,.....)<br/>Ex: bi.add(3,4) = 7 |
|  cbrt | Returns the cuberoot value  of a give value | bi.cbrt(value)<br/>Ex: bi.cbrt(27) = 3 |
|  ceil | Returns the smallest integer greater than or equal to the given number | bi.ceil(value)<br/>Ex: bi.ceil(3.1) = 4 & bi.ceil(-8.5) = -8 |
|  cube | Returns the cube value of given value | bi.cube(value)<br/>Ex: bi.cube(3)=27 |
|  divide | Return the results after dividing two given values | bi.divide(m,n) = m/ n<br/>Ex: bi.divide(6,3) = 2 |
|  fix | Round the integer value for a given value towards zero. | bi.fix(value)<br/>Ex: bi.fix(4.5) = 4, fix(-4.5) = -4 |
|  floor | Round the integer value for given value towards minus infinity. | bi.floor(value)<br/>Ex: floor(2.8) = 2, floor(-7.5) = -8 |
|  dotDivide | Returns the value obtained after dividing two matrices element wise | For   a = [[9, 5], [6, 1]];<br/>       _b = [[3, 2], [5, 2]];<br/>bi.dotDivide(a, b)  returns [[3, 2.5], [1.2, 0.5]] |
|  dotMultiply | Returns the value obtained after multiplying two matrices element wise | For   a = [[9, 5], [6, 1]];<br/>       _b = [[3, 2], [5, 2]];<br/>bi.dotMultiple(a, _b)  returns [[27, 10], [30, 2]] |
|  dotPow | Return value after calculating the power of x to y element wise. | For a = [[1, 2], [4, 3]];<br/>bi.dotPow(a, 2)   returns  [[1, 4], [16, 9]] |
|  exp | Return the exponential power of a value. | bi.exp(x)<br/>Ex: bi.exp(2) = 7.3890560989306495 |
|  gcd | Returns  the greatest common divisor for two or more values or arrays. | bi.gcd(a,b) = a.b/Lcm(a,b) Ex: For a= 8, b = 12 then bi.gcd(a,b) = 4 |
|  hypot | Returns the hypotenuse of a list with values. | bi.hypot = (p1,p2,p3..) <br/>Ex: bi.hypot (3,4) = sqrate_root ( square(3) + square(4) ) = 5 |
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

### Matrix

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  concat | Returns the array or text after concatenating two or more texts or matrices. | bi.concat(a,b)<br/>Ex: bi.concat(“Hello” ,”  World”) = “Hello  World”<br/>For  A = [[1, 2], [5, 6]] & B = [[3, 4], [7, 8]] <br/>bi.concat(A, B) = [[1, 2, 3, 4], [5, 6, 7, 8]] |
|  Cross | Returns the cross product for two vectors in three dimensional space. | Ex:bi.cross(A, B) = [ a2 b3 - a3 b2, a3 b1 - a1 b3, a1 b2 - a2b1 ]  |
|  det | Returns the determinant of a matrix. | bi.det([[1, 2], [3, 4]]) = -2 |
|  dot | Returns the dot product of two vectors. | bi.dot(A, B) = a1 b1 + a2 b2 + a3 b3 + … + an bn, <br/>Ex: bi.dot([2, 4, 1], [2, 2, 3]) = 15 |
|  eye | Create a 2-dimensional identity matrix with size m x n or n x n. | Ex: bi.eye(3) = [[1, 0, 0], [0, 1, 0], [0, 0, 1]], <br/>       bi.eye(3, 2) = [[1, 0], [0, 1], [0, 0]] |
|  filter | Filter the items in an array or one dimensional matrix. | Ex: bi.filter([6, -2, -1, 4, 3], isPositive) = [6, 4, 3], <br/>       bi.Filter(["23", "foo", "100", "55", "bar"], /[0-9]+/) = ["23", "100", "55"] |
|  flatten | Flatten a multi dimensional matrix into a single dimensional matrix. | Ex: bi.flatten([[1,2], [3,4]]) = [1, 2, 3, 4] |
|  forEach | Iterate over all elements of a matrix/array, and executes the given callback function. | Ex: bi.forEach([1, 2, 3],  function(value) { console.log(value);})<br/>Return 1,2,3 |
|  inv | Calculate the inverse of a square matrix. | bi.inv(value)<br/>Ex: inv(x) = inv(4) = 1/4 = 0.25 |
|  kron | Calculates the kronecker product of 2 matrices or vectors. | bi.kron([1,1], [2,3,4]) = [ [ 2, 3, 4, 2, 3, 4 ] ] |
|  map | Create a new matrix or array with the results of the callback function executed on each entry of the matrix/array. | Ex: bi.map([1, 2, 3], function(value) { return value * value;})<br/>      Returns [1,4,9] |
|  ones | Create a matrix filled with ones. | Ex: ones(3) = [1, 1, 1], <br/>       Ones(3, 2) = [[1, 1], [1, 1], [1, 1]] |
|  partitionSelect | Partition-based selection of an array or 1D matrix. | Ex: function sortByLength (a, b) { <br/>       return a.length – b.length;<br/>       } <br/>bi.partitionSelect(['Langdon', 'Tom', 'Sara'], 2, SortByLength); <br/>returns 'Langdon' |
|  range | Create an array from a range. | bi.range(m,n)<br/>Ex: bi.range(2, 6) = [2, 3, 4, 5], <br/>      bi.range(2, -3, -1) = [2, 1, 0, -1, -2] |
|  reshape | Reshape a multi dimensional array to fit the specified dimensions. | bi.reshape(x, sizes)<br/>Ex: For var x = matrix([1, 2, 3, 4, 5, 6, 7, 8]);<br/>       bi.reshape(x, [2, 2, 2])  = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]] |
|  resize | Resize a matrix | bi.resize(x, size, defaultValue) <br/>Ex: bi.resize([1, 2, 3, 4, 5], [3]) = [1,2,3], <br/>       bi.resize("hello", [8], "!") = 'hello!!!' |
|  size | Calculate the size of a matrix or scalar. | bi.size(x) <br/>Ex: size('hello world') = [11], <br/>For var A = [[1, 2, 3], [4, 5, 6]] then size(A) = [2, 3] |
|  sort | Sort the items in a matrix. | bi.sort(x, compare) <br/>Ex:  function sortByLength (a, b) {<br/>        return a.length – b.length;<br/>        } <br/>bi.sort(['Langdon', 'Tom', 'Sara'], SortByLength);<br/>Returns  ['Tom', 'Sara', 'Langdon'] |
|  squeeze | Squeeze a matrix, remove inner and outer singleton dimensions from a matrix. | bi.squeeze(x) <br/>Ex: For var A = zeros(3, 1); = [[0], [0], [0]] (size 3x1)<br/>       bi.squeeze(A);  returns  [0, 0, 0] (size 3) |
|  subset | Get or set a subset of a matrix or string. | bi.subset(value, index, replacement [, defaultValue])<br/>Ex: For var e = [];<br/>var f = subset(e, index(0, [0, 2]), [5, 6]) then  f = [[5, 6]]<br/>var g = subset(f, index(1, 1), 7, 0) then g = [[5, 6], [0, 7]] |
|  trace | Calculate the trace of a matrix: the sum of the elements on the main diagonal of a square matrix. | bi.trace(x)<br/>Ex: bi.trace([[1, 2], [3, 4]]) returns 5 |
|  transpose | Transpose a matrix. | bi.transpose(x)<br/>Ex: For  var A = [[1, 2, 3], [4, 5, 6]] then <br/>       bi.transpose(A); = [[1, 4], [2, 5], [3, 6]] |
|  zeros | Create a matrix filled with zeros. | Ex:var A = [[1, 2, 3], [4, 5, 6]];<br/>      bi.zeros(size(A)) returns  [[0, 0, 0], [0, 0, 0]] |

### Geometry
|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  distance | Results the euclidean distance between two points in 2 and 3 dimensional spaces. | distance([x1, y1], [x2, y2]) = distance([0,0], [4,4]) = 5.6569. |

### String

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  format | Returns string format a value of any type, | bi.format(value) = 'value',<br/>Ex: bi.format(6.4)=’6.4’ & bi.format(21385, 2) = '21000' |
|  print | Return the results after interpolating a value into a string template | bi.print(“String $Value String”,{Value : number})<br/>Ex: bi.print('John is $age years old', {age: 8}) returns<br/> 'John mark is 8 years old' |

### Relational
|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  compare | Returns -1, 1, 0 after comparing two given values<br/>Syntax: bi.compare(x,y) <br/>Returns -1 if x<y<br/>Returns 1 if x >y<br/>Returns 0 if x=y | bi.compare(6,2) = 1,<br/>bi.compare(2,6) = -1,<br/>bi.compare(6,6) = 0 |
|  deepEqual | Returns true / false after comparing the given values or list | bi.deepEqual(x,y)<br/>Ex: bi.deepEqual(6,8) = false , bi.deepEqual(6,6) = true<br/>For a = [2, 5, 1]  & b = [2, 7, 1] then bi.deepEqual(a, b) = false |
|  equal | Returns true / false after comparing the given values or list | bi.equal(x,y)<br/>Ex:  bi.equal(6,8) = false , bi.equal(6,6) = true<br/>For a = [2, 5, 1]  & b = [2, 7, 1] then bi.equal(a, b) = [true false true] |
|  larger | Returns true / false after validating larger value in the given values:<br/>true    -  if First value is greater than second <br/>false   - if second value is greater than first | bi.larger(x,y)<br/>Ex: bi.larger(2,3) = false,<br/>      bi.larger(4,3) = true |
|  smaller | Returns true / false after validating smaller value in the given values:<br/>true    -  if firstvalue is lesser than second <br/>false   - if secondvalue is lesser than first | bi.smaller(x,y)<br/>Ex: bi.smaller(2,3) = true,<br/>      bi.smaller(4,3) = false |
|  smallerEq | Returns true / false after validating smaller value in the given values: <br/>true    -  if firstvalue is  lesser or equal to the second  <br/>false   - if secondvalue is greater than first | bi.smallerEq(x,y)<br/>Ex: bi.smallerEq(2,3) = true & bi.smallerEq(3,3) = true<br/>      bi.smallerEq(4,3) = false |
|  unequal | Returns true / false after validating equality in the given values: <br/>true    -  if the values are not equal<br/>false   -  if the values are equal | bi.unequal(x,y)<br/>Ex: bi.unequal(2,3) = true & bi.unequal(3,2) = true<br/>      bi.unequal(3,3) = false |

### Trigonometry

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
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
|  tanh | Returns the hyperbolic tangent of a value, <br/>Defined as tanh(x) = (exp(2 x) - 1) / (exp(2 x) + 1). | bi.tanh(value)<br/>Ex: bi.tanh(90) = 1 |
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

### Constant

|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
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
|  uninitialized | Constant used as default value when resizing a matrix to leave new entries uninitialized | - |
### Unit	
|Name|Description|Example|
|--|--|--|
|to|Returns the converted unit value of a given value|Ex: bi.unit("2 inch").to("cm") |

### Utils 	
|  **Name** | **Description** | **Example** |
|  :------: | :------: | :------: |
|  to | Returns the converted unit value of a given value | bi.unit("x unit1").to("unit2")<br/>Ex: bi.number(bi.unit("2 inch").to("cm"),"cm") = 5.08 <br/>       bi.number(bi.unit("16 bytes").to("bits"),"bits") = 128 |
|  clone | Clone an object. | bi.clone(x) <br/>Ex: bi.clone(“3.5”) = 3.5 |
|  isInteger | Returns true / false after validating the given value is integer<br/>true if the given value is integer or else false | bi.inInteger(value)<br/>Ex: bi.isInteger(2) = true, <br/>       bi.isInteger(2.5) = false |
|  isNaN | Returns true / false after validating the given value  whether it is NaN (not a number) | bi.isNaN(value)<br/>Ex: bi.isNaN(3) = false, <br/>      bi.isNaN(NaN) = true |
|  isPositive | Returns true / false after validating the given value is positive<br/>true if the given value is integer or else false | bi.isPositive(value)<br/>Ex: bi.isPositive(3) = true, <br/>      bi.isPositive(-3) = false |
|  isNegative | Returns true / false after validating the given value is negative<br/>true if the given value is integer or else false | bi.isNegative(value)<br/>Ex: bi.isNegative(3) = false, <br/>      bi.isNegative(-3) = true |
|  isNumeric | Returns true / flase after validating the given value is numeric or not | bi.isNumeric(value)<br/> Ex: bi.isNumeric(3) = true, <br/>      bi.isNumeric(“string”) = false |
|  isPrime | Results true / false after validating  the given value is  whether a prime number | bi.isPrime(value)<br/> Ex: bi.isPrime(3) = true, <br/>       bi.isPrime(4) = false |
|  isZero | Results true / false after validating  the given value is  whether it is zero | bi.isZero(value)<br/> Ex: bi.isZero(1) = false, <br/>       bi.isZero(0) = true |
|  typeof | Determine the type of a variable. | bi.typeof(3.5) = number, <br/>bi.typeof(math.complex('2-4i')) = complex,<br/>bi.typeof('hello world') = string |


## Arithmetic & Logical operations on Data Fields

Perform Arithmetic operation on desired fields in calculated columns.

 **For Example:**
 To add an amount 2000 to the column field **order value sum**, derive the following expression in calculated column screen.
 ```
bi.add(${ROOT.BI_DELIVERYREPORT.sum_ORDERVALUE},2000)
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/8482aac4e08d59dd60a2b28e6d34302df3357ebd/images/calculated1.png)

## Usage of #plugin# for Grid View

Plugin operators provides complete authority on creation, editing and deleting of raw data. It allows customization of data using JavaScript API language  as per the business requirement.

 **biCalculation.pluginData.raw**  holds the Raw JSON data and can be transformed as per the requirement.

```
#plugin#

/*START*/
function localFunction(param1,param2,...ParamN)
{ 
                                                                            * update raw data *
for(var i =0 ; i < _biCalculation.pluginData.raw.length; i++)
    {
         var item = biCalculation.pluginData.raw[i];
         
    }

return item;
}
/*END*/
```

## Calculate Custom Functions

It will execute a series of actions on a database record and returns a particular value.
 
 
 ```
/*START*/

function Fname(input_param1,input_param2,..input_ParamN)
{

Statement 1;
Statement 2;
......
Statement N;
return Output_value;
}
/*END*/
bi._Fname(input_param1, input_param2,..input_paramN)
```

## Access Global Parameters
 
 Global parameter is a flat file used to manipulate, control and organize the data which is not available in database and can be accessed in report.
 ```
 bi.in_global_keys(["ParameterColumnName"] ["DatabaseValue"],"ParameterName.Field"])
```

- **Parameter Column Name** Refer the key name from global parameter.

-  **Database Value** Refers database value.

- **Parameter Name Field** Returns the field from global parameter it is applicable in 3 different ways ;

 **1.**  **Static value** Global parameters refers to a static value.

 ```
  bi.in_global_keys( ["Parameter_Column_Name "],["Reference string" ],"Global_parameter.field")
```

>**For Example:**
``` 
bi.in_global_keys( ["Station_Name"],["Station_1" ],"Calc_ONRAW.value")
```

**2.** **Reference value** Global parameters refers to reference value.

```
  bi.in_global_keys( ["Parameter_Column_Name "],["database column" ],"Global_parameter.field")
```

>**For Example:** 
```
bi.in_global_keys( ["Station_Name"],[${ROOT.AUTOTEST_ORDERS.STATIONCODE_724} ],"Calc_ONRAW.value")
```

**3. Login Name(User Id)** Provide Access based on Login ID.

```
bi.in_global_keys(["ParameterColumnName","ParameterUserID"],["DatabaseField","bi._globals("#userid#")"],"ParameterName.Field"])
```

>**For Example:** 
```
bi.in_global_keys( ["UserName","Login_name"],[${ROOT.EMPLOYEES.NAME_661} 
,bi._globals("#userid#")],"CalcCol_Stage2.SeizeLimit)
```

## Calculate on Raw functionality

By enabling the field **Calculate on Raw**, the calculation is applied on all the rows irrespective of grouping and pivot settings, if disabled calculation applied on abstract values only.
 
>**For Instance:**  consider the below image, which represents calculated data with disabling calculate on raw.

```
bi.add(${ROOT.BI_DELIVERYREPORT.sum_ORDERVALUE},2)
```

![
](https://raw.githubusercontent.com/sv18042016/fp1/457490d3185941046566d493017e4f95c2b8b18a/images/calculate_on_raw.png)

## Calculate Column with Pivot Offset

>**For Instance:** To view the order-value sum and average w.r.t each station code, then apply pivot to station-code and run the report.

![
](https://raw.githubusercontent.com/sv18042016/fp1/5993c1fa2683f7ecb11c313b45e40254e525f625/images/pivot_stationcoed.png)

We can get quantity_sum difference of each month for specific customer using Pivot_Offset() function.

${ROOT.BI_ORDERS.sum_QUANTITY} -bi.pivot_offset( #{ROOT.BI_ORDERS.sum_QUANTITY} ,0,-1)

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/eb64533dd879286986c2b3f4a9f69295ab96da8b/images/pivot_offset2.png)

## Local Function

Custom function is a block of code (Series of statements which intended to a particular task) with submitted inputs and derivable output. It will ease-up the process of calculations when a series of statements or actions to be repeated on a set of values and output to be derived. AcuBi supports local function which can be written inside the function body:
```
/*START*/
function fname(param1, param2, param3 ..ParamN)
{
statement 1;
statement 2;                                     * Function body *
statement 3;

Statement N;
return ;   
}
/*END*/
fname(value1, value2, value3, ..valueN)         * Call Function *
```

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/52b7c4357f0c07e4a89b14f018cf3d877a5ba4f3/images/cal_local_fucntion.png)

> **Note :**  it returns value 6.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2NjQwNTI5NywtODE1Mjk4MjQzLC05OD
Q1ODI2ODksNTMxMDk4NjM3LC05ODQ1ODI2ODksNTMxMDk4NjM3
LC03NTAzMTM0NTksLTE3MTg3MjE1MjcsMTk5MDI4NTMzMywtMT
I4MDc0ODUzNywtODk0NDAyNDI2LC0xNDc5MDQ4MTY5LC0zMDA1
MzIzODcsMzI5Njg2ODc3LDY1Nzc1NjEyNywxNjA2MjY3ODM5LC
0xNjI0NjY1MjI3LC0xOTkyODA5MTksMTAzNTU0NjUwNywtODU0
ODI4ODE3XX0=
-->