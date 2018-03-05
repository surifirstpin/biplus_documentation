---


---

<center><h1>Calculated Column</h1></center>
<h2 id="definition">Definition</h2>
<p>A functionality which allows to manipulate the retrieved data using arithmetical, logical, text-based and date-based functions and then displays it in the required format. Calculated columns will show up as green in the data table, rather than as blue (dimensions), or orange (measures). Just like regular dimensions and measures, calculated columns are controlled from display in visualizations.</p>
<p><strong>Usage :</strong></p>
<ol>
<li>Supports a wide variety of arithmetical and logical functions to be applied on the data.</li>
<li>Calculates using the data from external parameters (through “Global parameters”) by making reference to the database field(s).</li>
<li>Controls or access the data with user wise calculations,</li>
<li>Optimize and transform the data using #plugin# functionality.</li>
<li>Allows to define a function or use a Global function to be applied on the required data fields.</li>
</ol>
<blockquote>
<p>Note: The functions support JavaScript API.</p>
</blockquote>
<h2 id="usage-of-math">Usage of #math#</h2>
<p>Custom made mathematical operations can be added in calculated column section as shown below</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/4a3a039bae7badccb31d41bbc9c5449943045474/images/calculate.png" alt="enter image description here"></p>
<p><strong>Check the number of working days in each month :</strong></p>
<pre><code>#math#
bi.days_in_month
(${ROOT.BI_ORDERS.date_month_WHENMADE}) 
</code></pre>
<p><strong>To calculate the cubical value of the field :</strong></p>
<pre><code>#math#
bi.cube(${ROOT.BI_ORDERS.count_AMOUNT})
</code></pre>
<h3 id="similarly-we-can-use-all-the-below-functionality-using-bi">Similarly we can use all the below functionality Using Bi+:</h3>
<h3 id="general">General</h3>

<table>
<thead>
<tr>
<th><strong>Name</strong></th>
<th><strong>Description</strong></th>
<th><strong>Usage and  Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Offset</td>
<td>Return the row value of the column mentioned as before or after based on  -Ve or +Ve number given</td>
<td>bi.offset(#{col_name}, row_difference)</td>
</tr>
<tr>
<td>pivot_offset</td>
<td>Returns the cell value of pivot table based on the Row and Column position given respectively.Row number:  +Ve &amp; -Ve are for below &amp; above positions Column number : +Ve and -Ve are for after &amp; before positions</td>
<td>bi.pivot_offset(#{col_name} ,m,n) for instance: m is row number &amp; n is column number</td>
</tr>
<tr>
<td>Contains</td>
<td>Returns true/ false after validating expression given inside</td>
<td>bi.contains(expression)</td>
</tr>
<tr>
<td>row_total</td>
<td>Returns the total value in the row for the preceding measures (before the present column)</td>
<td>bi.row_total ( )</td>
</tr>
<tr>
<td>col_total</td>
<td>Returns the total value of the column given inside ()</td>
<td>bi.column_total(#{col_name})</td>
</tr>
<tr>
<td>number</td>
<td>Returns the object argument to a number that represents the object’s value.The object may be static or a column name</td>
<td>bi.number(“static”) or bi.number(${col_name}) Ex: bi.number(“1234567”) returns  1234567</td>
</tr>
<tr>
<td>int</td>
<td>Returns only integer values of given number or column</td>
<td>bi.int(number) or bi.int(${col_name})Ex: bi.int(74845.9898) = 74845</td>
</tr>
<tr>
<td>in_globals</td>
<td>Returns the data from Global parameters based on the common reference. The reference can be static or a column</td>
<td>bi.in_globals(Ref ,”GP_Name.R_Val ”, ”Ref_key” ) <strong>Note:</strong> Ref can be a column name or static value or userid</td>
</tr>
<tr>
<td>in_global_key</td>
<td>it returns the data from global parameters based on the multiple common references.this references can be static or column</td>
<td>bi.in_global_keys ([“GP_Rkey1”,”GP_Rkey2”,…],[Ref1, Ref2,…], ”GP_Name.R_Val”) Note: Ref1/Ref2 can be static strings or column names or userid</td>
</tr>
<tr>
<td>calculate_key_group</td>
<td>Returns an aggregated value of a measure based on a dimension with further mention of row grouping column name</td>
<td>bi.calculate_key_group (#Ag_col,<span class="katex--inline">KaTeX parse error: Expected 'EOF', got '#' at position 8: Ag_col,#̲RG_col,</span>RG_col,$M_col,”agg_type”) Where Ag= Aggregated &amp; RG for Row Grouping  &amp; M_Col for measure and agg_type can be sum, avg, min, max, count</td>
</tr>
<tr>
<td>col_running_total</td>
<td>Returns the running total value for a column in each cell</td>
<td>bi.col_running_total(#{col_name})</td>
</tr>
<tr>
<td>col_running_avg</td>
<td>Returns the average value upto current cell for a column</td>
<td>bi.col_running_avg(#{col_name})</td>
</tr>
</tbody>
</table><h3 id="statistics">Statistics</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Usage &amp; Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">unequal</td>
<td align="center">Returns true / false if the inputs given are not equal.</td>
<td align="center">bi.unequal(m,n)<br>Returns true if m=n else false</td>
</tr>
<tr>
<td align="center">mad</td>
<td align="center">Returns the Median Absolute Deviation for the inputs</td>
<td align="center">bi.mad(p1,p2,p3,…)<br>Ex: bi.mad(100,200) = 50</td>
</tr>
<tr>
<td align="center">max</td>
<td align="center">Returns the maximum value of a matrix or a list with values.</td>
<td align="center">bi.max(p1,p2,p3,…)<br>Ex: bi.max(100,200,300) = 300</td>
</tr>
<tr>
<td align="center">mean</td>
<td align="center">Returns the mean value of a list of values mentioned</td>
<td align="center">bi.mean(p1,p2,p3)<br>Ex: bi.mean(100,200,300) = 200</td>
</tr>
<tr>
<td align="center">median</td>
<td align="center">Returns the median value of a list of values mentioned</td>
<td align="center">bi.median(p1,p2,p3,…)</td>
</tr>
<tr>
<td align="center">mode</td>
<td align="center">Retruns the values which are repeated in the list mentioned</td>
<td align="center">bi.mode(p1,p2,p3,…)<br>Ex: bi.mode(1,2,1)=1</td>
</tr>
<tr>
<td align="center">prod</td>
<td align="center">Returns the product values of the mentioned values</td>
<td align="center">bi.prod(p1,p2,p3,p4,…)</td>
</tr>
<tr>
<td align="center">Ex: bi.prod(p1,p2,p3) = p1 * p2 * p3</td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr>
<td align="center">quantileSeq</td>
<td align="center">Returns prob order quantile of a matrix or a list with values</td>
<td align="center">bi.quantileSeq(A, prob[, sorted])</td>
</tr>
<tr>
<td align="center">std</td>
<td align="center">Returns the standard deviation of a matrix or a list with values.</td>
<td align="center">bi.std(p1,p2,p3 …)<br>bi.std(A)<br>bi.std(A, normalization)</td>
</tr>
<tr>
<td align="center">sum</td>
<td align="center">Returns the sum of list of values mentioned</td>
<td align="center">bi.sum(p1,p2,p3,…)<br>Ex: bi.sum(p1,p2,p3) = p1 + p2 +p3</td>
</tr>
<tr>
<td align="center">var</td>
<td align="center">Returns the variance of a matrix or a list with values</td>
<td align="center">bi.var(p1,p2,p3)<br>Ex: bi.var(2, 4, 6) = 4</td>
</tr>
</tbody>
</table><h3 id="date">Date</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Usage &amp; Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">date_to_week</td>
<td align="center">Returns the week number in the year for the date given</td>
<td align="center">bi.date_to_week(${col_name})<br>Ex: bi.date_to_week(“2018-02-11”) = 7</td>
</tr>
<tr>
<td align="center">date_to_month</td>
<td align="center">Returns the month number in the year for the date given</td>
<td align="center">bi.date_to_month(${col_name})<br>Ex: bi.date_to_month(“2018-02-11”) = 2</td>
</tr>
<tr>
<td align="center">date_to_quarter</td>
<td align="center">Returns the quarter number in the year for the date given</td>
<td align="center">bi.date_to_quarter(${col_name})<br>Ex: bi.date_to_quarter(“2018-02-11”) = 1</td>
</tr>
<tr>
<td align="center">date_to_year</td>
<td align="center">Returns the year for the date given</td>
<td align="center">bi.date_to_year(${col_name})<br>Ex: bi.date_to_year(“2018-02-11”) = 2018</td>
</tr>
<tr>
<td align="center">date_format</td>
<td align="center">Returns the required format (supported by the database) of a date given</td>
<td align="center">bi.date_format(${col_name}, “required_format”) Ex: bi.date_format(“2018-02-10 235950”, “YYYY-MM”) = 2018-02</td>
</tr>
<tr>
<td align="center">date_diff</td>
<td align="center">Returns the number of days between two given dates</td>
<td align="center">bi.date_diff(date1,date2)</td>
</tr>
<tr>
<td align="center">days_in_month</td>
<td align="center">Returns the total number of days in a month for a given date / time stamp</td>
<td align="center">bi.days_in_month (${Col_name})</td>
</tr>
<tr>
<td align="center">Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 28</td>
<td align="center"></td>
<td align="center"></td>
</tr>
<tr>
<td align="center">days_till_month</td>
<td align="center">Returns the total number of days completed in a month for a given date / time stamp</td>
<td align="center">bi.days_till_month (${Col_name})</td>
</tr>
<tr>
<td align="center">Ex: bi.days_in_month(“2018-02-01 15:32:26”) = 1</td>
<td align="center"></td>
<td align="center"></td>
</tr>
</tbody>
</table><h3 id="bitwise-operator">Bitwise Operator</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Usage &amp; Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">bitAnd</td>
<td align="center">Bitwise AND two values, x &amp; y. Ex. bit And(x, y)</td>
<td align="center">bi.bitAnd(53, 131) = 1</td>
</tr>
<tr>
<td align="center">bitNot</td>
<td align="center">Bitwise NOT value, ~x.</td>
<td align="center">bi.bitNot(1) = -2, <br>bi.bitNot([2,-3,4]) = [-3,2,5]</td>
</tr>
<tr>
<td align="center">bitOr</td>
<td align="center">Bitwise OR two values, x&amp;#124 y.</td>
<td align="center">bi.bitOr(1,2) = 3, <br>bi.bitOr([1,2,3],4) = [5,6,7]</td>
</tr>
<tr>
<td align="center">bitXor</td>
<td align="center">Bitwise XOR two values, x ^ y.</td>
<td align="center">bi.bitXor(1, 2) = 3, <br>bi.bitXor([2, 3, 4], 4) = [6,7,0]</td>
</tr>
<tr>
<td align="center">leftShift</td>
<td align="center">Bitwise left logical shift of a value x by y number of bits, x &lt;&lt; y.</td>
<td align="center">bi.leftShift(1, 2) = 4, <br>bi.leftShift([1, 2, 3], 4) = [16, 32, 64]</td>
</tr>
<tr>
<td align="center">rightArithShift</td>
<td align="center">Bitwise right arithmetic shift of a value x by y number of bits, x &gt;&gt; y.</td>
<td align="center">bi.rightArithShift(4, 2) = 1, <br>bi.rightArithShift([16, -32, 64], 4) = [1, -2, 3]</td>
</tr>
<tr>
<td align="center">rightLogShift</td>
<td align="center">Bitwise right logical shift of value x by y number of bits, x &gt;&gt;&gt; y.</td>
<td align="center">bi.rightLogShift(4, 2) = 1, <br>bi.rightLogShift([16, -32, 64], 4) = [1, 2, 3]</td>
</tr>
</tbody>
</table><h3 id="arithmetic">Arithmetic</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">abs</td>
<td align="center">Returns the absolute value of a number<br>It removed the -ve symbol for a negative value and displays the result as positive value</td>
<td align="center">bi.abs(${Col_name})<br>Ex: bi.abs(-2) = 2</td>
</tr>
<tr>
<td align="center">add</td>
<td align="center">Returns the value which obtained by adding the given list of values</td>
<td align="center">bi.add(p1,p2,p3,…)<br>Ex: bi.add(3,4) = 7</td>
</tr>
<tr>
<td align="center">cbrt</td>
<td align="center">Returns the cuberoot value  of a give value</td>
<td align="center">bi.cbrt(value)<br>Ex: bi.cbrt(27) = 3</td>
</tr>
<tr>
<td align="center">ceil</td>
<td align="center">Returns the smallest integer greater than or equal to the given number</td>
<td align="center">bi.ceil(value)<br>Ex: bi.ceil(3.1) = 4 &amp; bi.ceil(-8.5) = -8</td>
</tr>
<tr>
<td align="center">cube</td>
<td align="center">Returns the cube value of given value</td>
<td align="center">bi.cube(value)<br>Ex: bi.cube(3)=27</td>
</tr>
<tr>
<td align="center">divide</td>
<td align="center">Return the results after divides the two given values</td>
<td align="center">bi.divide(m,n) = m/ n<br>Ex: bi.divide(6,3) = 2</td>
</tr>
<tr>
<td align="center">fix</td>
<td align="center">Round the integer value for a given value towards zero.</td>
<td align="center">bi.fix(value)<br>Ex: bi.fix(4.5) = 4, fix(-4.5) = -4</td>
</tr>
<tr>
<td align="center">floor</td>
<td align="center">Round the integer value for given value towards minus infinity.</td>
<td align="center">bi.floor(value)<br>Ex: floor(2.8) = 2, floor(-7.5) = -8</td>
</tr>
<tr>
<td align="center">dotDivide</td>
<td align="center">Returns the value obtained after dividing two matrices element wise</td>
<td align="center">For   a = [[9, 5], [6, 1]];<br>       _b = [[3, 2], [5, 2]];<br>bi.dotDivide(a, b)  returns [[3, 2.5], [1.2, 0.5]]</td>
</tr>
<tr>
<td align="center">dotMultiply</td>
<td align="center">Returns the value obtained after multiplying two matrices element wise</td>
<td align="center">For   a = [[9, 5], [6, 1]];<br>       _b = [[3, 2], [5, 2]];<br>bi.dotMultiple(a, _b)  returns [[27, 10], [30, 2]]</td>
</tr>
<tr>
<td align="center">dotPow</td>
<td align="center">Return value after calculateing the power of x to y element wise.</td>
<td align="center">For a = [[1, 2], [4, 3]];<br>bi.dotPow(a, 2)   returns  [[1, 4], [16, 9]]</td>
</tr>
<tr>
<td align="center">exp</td>
<td align="center">Retunr the exponentinal power of a value.</td>
<td align="center">bi.exp(x)<br>Ex: bi.exp(2) = 7.3890560989306495</td>
</tr>
<tr>
<td align="center">gcd</td>
<td align="center">Returns  the greatest common divisor for two or more values or arrays.</td>
<td align="center">bi.gcd(a,b) = a.b/Lcm(a,b) Ex: For a= 8, b = 12 then bi.gcd(a,b) = 4</td>
</tr>
<tr>
<td align="center">hypot</td>
<td align="center">Returns the hypotenusa of a list with values.</td>
<td align="center">bi.hypot = (p1,p2,p3…) <br>Ex: bi.hypot (3,4) = sqrate_root ( square(3) + square(4) ) = 5</td>
</tr>
<tr>
<td align="center">lcm</td>
<td align="center">Returns the least common multiple for two or more values or arrays</td>
<td align="center">bi.lcm(a,b)<br>Ex: For a = 4,b = 6 then  bi.lcm(4,6) = 12</td>
</tr>
<tr>
<td align="center">log</td>
<td align="center">Returns the logarithm of a value (e-based).</td>
<td align="center">bi.log(a)<br>Ex: bi.log(10) = 2.3025850929</td>
</tr>
<tr>
<td align="center">log10</td>
<td align="center">Returns the logarithm of a value (10-based).</td>
<td align="center">bi.log10(a)<br>Ex: bi.log10(10) = 1</td>
</tr>
<tr>
<td align="center">mod</td>
<td align="center">Returns the remainder of an integer division of two values(Calculates the modulus)</td>
<td align="center">bi.mod(a,b)<br>Ex: For a= 17, b= 3 then bi.mod(a,b) = 2</td>
</tr>
<tr>
<td align="center">multiply</td>
<td align="center">Returns the value obtained after multiplying the two or more given values</td>
<td align="center">bi.multiply(p1,p2,p3,…)<br>Ex: bi.multiply(3,4) = 3*4 =12</td>
</tr>
<tr>
<td align="center">norm</td>
<td align="center">Returns the norm of a number, vector or matrix</td>
<td align="center">bi.norm(a)<br>Ex: norm(-3.5) = 3.5, norm([[1, 2], [3, 4]], 1) returns 6</td>
</tr>
<tr>
<td align="center">nthRoot</td>
<td align="center">Returns the nth root calculation of given value.</td>
<td align="center">bi.nthRoot(a,b)<br>Ex: bi.nthRoot(9,2) = (3^2) = 9</td>
</tr>
<tr>
<td align="center">pow</td>
<td align="center">Returns the power value of the first parameter to the second parameter</td>
<td align="center">bi.pow(a,b)<br>Ex: bi.pow (5,3) = value of 5 to the power 3 = 125</td>
</tr>
<tr>
<td align="center">round</td>
<td align="center">Returns the rounded a value towards the nearest integer.</td>
<td align="center">bi.round(A)<br>Ex: bi.round(3.2) = 3</td>
</tr>
<tr>
<td align="center">sign</td>
<td align="center">Returns the sign of a value.</td>
<td align="center">bi.sign(A)<br>Ex: bi.sign (3.4) = 1 , bi.sign(-3,4)= -1 , bi.sign(0) = 0 , 1 when x &gt; 1, -1 when x &lt; 0, 0 when x == 0</td>
</tr>
<tr>
<td align="center">sqrt</td>
<td align="center">Returns the square root of given value.</td>
<td align="center">bi.sqrt(x)<br>Ex: bi.sqrt(25) = 5</td>
</tr>
<tr>
<td align="center">square</td>
<td align="center">Returns the square of given value.</td>
<td align="center">bi.square(x)<br>Ex: bi.square(5) = 25</td>
</tr>
<tr>
<td align="center">unaryMinus</td>
<td align="center">Returns the Inverse sign of a value, apply a unary minus operation.</td>
<td align="center">bi.unaryMinus(x)<br>Ex: bi.unaryMinus(3.5) = -3.5 &amp; bi.unaryMinus(-4.2) = 4.2</td>
</tr>
<tr>
<td align="center">subtract</td>
<td align="center">Returns the value ontained after subtracting two given values</td>
<td align="center">bi.substract(a,b)<br>Ex: bi.subtract (4,3) = 4-3 = 1</td>
</tr>
<tr>
<td align="center">unaryPlus</td>
<td align="center">Returns the Inverse sign of a value, apply a unary plus operation.</td>
<td align="center">bi.unaryPlus(x)<br>Ex: bi.unaryPlus(3.44) = 3.44</td>
</tr>
<tr>
<td align="center">xgcd</td>
<td align="center">Returns the extended greatest common divisor for two values.</td>
<td align="center">bi.xgcd(a,b) <br>For Array type: Returns an array containing 3 integers [div, m, n] where div = gcd(a, b) and a<em>m + b</em>n = div<br>Ex: For bi.xgcd(8,12) = [4,-1,1]</td>
</tr>
</tbody>
</table><h3 id="matrix">Matrix</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">concat</td>
<td align="center">Returns the array or text after concatenating two or more texts or matrices.</td>
<td align="center">bi.concat(a,b)<br>Ex: bi.concat(“Hello” ,”  World”) = “Hello  World”<br>For  A = [[1, 2], [5, 6]] &amp; B = [[3, 4], [7, 8]] <br>bi.concat(A, B) = [[1, 2, 3, 4], [5, 6, 7, 8]]</td>
</tr>
<tr>
<td align="center">Cross</td>
<td align="center">Returns the cross product for two vectors in three dimensional space.</td>
<td align="center">Ex:bi.cross(A, B) = [ a2 b3 - a3 b2, a3 b1 - a1 b3, a1 b2 - a2b1 ]</td>
</tr>
<tr>
<td align="center">det</td>
<td align="center">Returns the determinant of a matrix.</td>
<td align="center">bi.det([[1, 2], [3, 4]]) = -2</td>
</tr>
<tr>
<td align="center">dot</td>
<td align="center">Returns the dot product of two vectors.</td>
<td align="center">bi.dot(A, B) = a1 b1 + a2 b2 + a3 b3 + … + an bn, <br>Ex: bi.dot([2, 4, 1], [2, 2, 3]) = 15</td>
</tr>
<tr>
<td align="center">eye</td>
<td align="center">Create a 2-dimensional identity matrix with size m x n or n x n.</td>
<td align="center">Ex: bi.eye(3) = [[1, 0, 0], [0, 1, 0], [0, 0, 1]], <br>       bi.eye(3, 2) = [[1, 0], [0, 1], [0, 0]]</td>
</tr>
<tr>
<td align="center">filter</td>
<td align="center">Filter the items in an array or one dimensional matrix.</td>
<td align="center">Ex: bi.filter([6, -2, -1, 4, 3], isPositive) = [6, 4, 3], <br>       bi.Filter([“23”, “foo”, “100”, “55”, “bar”], /[0-9]+/) = [“23”, “100”, “55”]</td>
</tr>
<tr>
<td align="center">flatten</td>
<td align="center">Flatten a multi dimensional matrix into a single dimensional matrix.</td>
<td align="center">Ex: bi.flatten([[1,2], [3,4]]) = [1, 2, 3, 4]</td>
</tr>
<tr>
<td align="center">forEach</td>
<td align="center">Iterate over all elements of a matrix/array, and executes the given callback function.</td>
<td align="center">Ex: bi.forEach([1, 2, 3],  function(value) { console.log(value);})<br>Return 1,2,3</td>
</tr>
<tr>
<td align="center">inv</td>
<td align="center">Calculate the inverse of a square matrix.</td>
<td align="center">bi.inv(value)<br>Ex: inv(x) = inv(4) = 1/4 = 0.25</td>
</tr>
<tr>
<td align="center">kron</td>
<td align="center">Calculates the kronecker product of 2 matrices or vectors.</td>
<td align="center">bi.kron([1,1], [2,3,4]) = [ [ 2, 3, 4, 2, 3, 4 ] ]</td>
</tr>
<tr>
<td align="center">map</td>
<td align="center">Create a new matrix or array with the results of the callback function executed on each entry of the matrix/array.</td>
<td align="center">Ex: bi.map([1, 2, 3], function(value) { return value * value;})<br>      Returns [1,4,9]</td>
</tr>
<tr>
<td align="center">ones</td>
<td align="center">Create a matrix filled with ones.</td>
<td align="center">Ex: ones(3) = [1, 1, 1], <br>       Ones(3, 2) = [[1, 1], [1, 1], [1, 1]]</td>
</tr>
<tr>
<td align="center">partitionSelect</td>
<td align="center">Partition-based selection of an array or 1D matrix.</td>
<td align="center">Ex: function sortByLength (a, b) { <br>       return a.length – b.length;<br>       } <br>bi.partitionSelect([‘Langdon’, ‘Tom’, ‘Sara’], 2, sortByLength); <br>returns ‘Langdon’</td>
</tr>
<tr>
<td align="center">range</td>
<td align="center">Create an array from a range.</td>
<td align="center">bi.range(m,n)<br>Ex: bi.range(2, 6) = [2, 3, 4, 5], <br>      bi.range(2, -3, -1) = [2, 1, 0, -1, -2]</td>
</tr>
<tr>
<td align="center">reshape</td>
<td align="center">Reshape a multi dimensional array to fit the specified dimensions.</td>
<td align="center">bi.reshape(x, sizes)<br>Ex: For var x = matrix([1, 2, 3, 4, 5, 6, 7, 8]);<br>       bi.reshape(x, [2, 2, 2])  = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]</td>
</tr>
<tr>
<td align="center">resize</td>
<td align="center">Resize a matrix</td>
<td align="center">bi.resize(x, size, defaultValue) <br>Ex: bi.resize([1, 2, 3, 4, 5], [3]) = [1,2,3], <br>       bi.resize(“hello”, [8], “!”) = ‘hello!!!’</td>
</tr>
<tr>
<td align="center">size</td>
<td align="center">Calculate the size of a matrix or scalar.</td>
<td align="center">bi.size(x) <br>Ex: size(‘hello world’) = [11], <br>For var A = [[1, 2, 3], [4, 5, 6]] then size(A) = [2, 3]</td>
</tr>
<tr>
<td align="center">sort</td>
<td align="center">Sort the items in a matrix.</td>
<td align="center">bi.sort(x, compare) <br>Ex:  function sortByLength (a, b) {<br>        return a.length – b.length;<br>        } <br>bi.sort([‘Langdon’, ‘Tom’, ‘Sara’], sortByLength);<br>Returns  [‘Tom’, ‘Sara’, ‘Langdon’]</td>
</tr>
<tr>
<td align="center">squeeze</td>
<td align="center">Squeeze a matrix, remove inner and outer singleton dimensions from a matrix.</td>
<td align="center">bi.squeeze(x) <br>Ex: For var A = zeros(3, 1); = [[0], [0], [0]] (size 3x1)<br>       bi.squeeze(A);  returns  [0, 0, 0] (size 3)</td>
</tr>
<tr>
<td align="center">subset</td>
<td align="center">Get or set a subset of a matrix or string.</td>
<td align="center">bi.subset(value, index, replacement [, defaultValue])<br>Ex: For var e = [];<br>var f = subset(e, index(0, [0, 2]), [5, 6]) then  f = [[5, 6]]<br>var g = subset(f, index(1, 1), 7, 0) then g = [[5, 6], [0, 7]]</td>
</tr>
<tr>
<td align="center">trace</td>
<td align="center">Calculate the trace of a matrix: the sum of the elements on the main diagonal of a square matrix.</td>
<td align="center">bi.trace(x)<br>Ex: bi.trace([[1, 2], [3, 4]]) returns 5</td>
</tr>
<tr>
<td align="center">transpose</td>
<td align="center">Transpose a matrix.</td>
<td align="center">bi.transpose(x)<br>Ex: For  var A = [[1, 2, 3], [4, 5, 6]] then <br>       bi.transpose(A); = [[1, 4], [2, 5], [3, 6]]</td>
</tr>
<tr>
<td align="center">zeros</td>
<td align="center">Create a matrix filled with zeros.</td>
<td align="center">Ex:var A = [[1, 2, 3], [4, 5, 6]];<br>      bi.zeros(size(A)) returns  [[0, 0, 0], [0, 0, 0]]</td>
</tr>
</tbody>
</table><h3 id="geometry">Geometry</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">distance</td>
<td align="center">Results the eucledian distance between two points in 2 and 3 dimensional spaces.</td>
<td align="center">distance([x1, y1], [x2, y2]) = distance([0,0], [4,4]) = 5.6569.</td>
</tr>
</tbody>
</table><h3 id="string">String</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">format</td>
<td align="center">Returns string format a value of any type,</td>
<td align="center">bi.format(value) = ‘value’,<br>Ex: bi.format(6.4)=’6.4’ &amp; bi.format(21385, 2) = ‘21000’</td>
</tr>
<tr>
<td align="center">print</td>
<td align="center">Return the results after interpolating a value into a string template</td>
<td align="center">bi.print(“String $Value String”,{Value : number})<br>Ex: bi.print(‘John is $age years old’, {age: 8}) returns<br> ‘John mark is 8 years old’</td>
</tr>
</tbody>
</table><h3 id="relational">Relational</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">compare</td>
<td align="center">Returns -1, 1, 0 after comparing two given values<br>Syntax: bi.compare(x,y) <br>Returns -1 if x&lt;y<br>Returns 1 if x &gt;y<br>Returns 0 if x=y</td>
<td align="center">bi.compare(6,2) = 1,<br>bi.compare(2,6) = -1,<br>bi.compare(6,6) = 0</td>
</tr>
<tr>
<td align="center">deepEqual</td>
<td align="center">Returns true / false after comparing the given values or list</td>
<td align="center">bi.deepEqual(x,y)<br>Ex: bi.deepEqual(6,8) = false , bi.deepEqual(6,6) = true<br>For a = [2, 5, 1]  &amp; b = [2, 7, 1] then bi.deepEqual(a, b) = false</td>
</tr>
<tr>
<td align="center">equal</td>
<td align="center">Returns true / false after comparing the given values or list</td>
<td align="center">bi.equal(x,y)<br>Ex:  bi.equal(6,8) = false , bi.equal(6,6) = true<br>For a = [2, 5, 1]  &amp; b = [2, 7, 1] then bi.equal(a, b) = [true false true]</td>
</tr>
<tr>
<td align="center">larger</td>
<td align="center">Returns true / false after validating larger value in the given values:<br>true    -  if firstvalue is greater than second <br>false   - if secondvalue is greater than first</td>
<td align="center">bi.larger(x,y)<br>Ex: bi.larger(2,3) = false,<br>      bi.larger(4,3) = true</td>
</tr>
<tr>
<td align="center">smaller</td>
<td align="center">Returns true / false after validating smaller value in the given values:<br>true    -  if firstvalue is lesser than second <br>false   - if secondvalue is lesser than first</td>
<td align="center">bi.smaller(x,y)<br>Ex: bi.smaller(2,3) = true,<br>      bi.smaller(4,3) = false</td>
</tr>
<tr>
<td align="center">smallerEq</td>
<td align="center">Returns true / false after validating smaller value in the given values: <br>true    -  if firstvalue is  lesser or equal to the second  <br>false   - if secondvalue is greater than first</td>
<td align="center">bi.smallerEq(x,y)<br>Ex: bi.smallerEq(2,3) = true &amp; bi.smallerEq(3,3) = true<br>      bi.smallerEq(4,3) = false</td>
</tr>
<tr>
<td align="center">unequal</td>
<td align="center">Returns true / false after validating equality in the given values: <br>true    -  if the values are not equal<br>false   -  if the values are equal</td>
<td align="center">bi.unequal(x,y)<br>Ex: bi.unequal(2,3) = true &amp; bi.unequal(3,2) = true<br>      bi.unequal(3,3) = false</td>
</tr>
</tbody>
</table><h3 id="trigonometry">Trigonometry</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">sin</td>
<td align="center">Returns the sine of a value.</td>
<td align="center">bi.sin(value)<br>Ex: bi.sin(0) = 0,bi.sin(90) = 1</td>
</tr>
<tr>
<td align="center">cos</td>
<td align="center">Returns the cosine of a value.</td>
<td align="center">bi.cos(value)<br>Ex: bi.cos(60) = 0.5</td>
</tr>
<tr>
<td align="center">sec</td>
<td align="center">Returns the secant of a value, <br>Defined as sec(x) = 1/cos(x).</td>
<td align="center">bi.sec(value)<br>Ex: bi.sec(60) = 2</td>
</tr>
<tr>
<td align="center">csc</td>
<td align="center">Returns the cosecant of a value, <br>Defined as csc(x) = 1/sin(x).</td>
<td align="center">bi.csc(value)<br>Ex: bi.csc(30) = 2</td>
</tr>
<tr>
<td align="center">tan</td>
<td align="center">Returns the tangent of a value.<br>Defined as tan(x) = sin(x) / cos(x)</td>
<td align="center">bi.tan(value)<br>Ex: bi.tan(45) = 1</td>
</tr>
<tr>
<td align="center">cot</td>
<td align="center">Returns the cotangent of a value.<br>Defined as cot(x) = 1 / tan(x)</td>
<td align="center">bi.cot(value)<br>Ex: bi.cot(45) = 1</td>
</tr>
<tr>
<td align="center">sinh</td>
<td align="center">Returns the hyperbolic sine of a value, <br>Defined as sinh(x) = 1/2 * (exp(x) - exp(-x)).</td>
<td align="center">bi.sinh(value)<br>Ex: bi.sinh(30) = 5343237290762.231</td>
</tr>
<tr>
<td align="center">cosh</td>
<td align="center">Returns the hyperbolic cosine of a value, <br>Defined as cosh(x) = 1/2 * (exp(x) + exp(-x))</td>
<td align="center">bi.cosh(value)<br>Ex: bi.cosh(90) = 6.1020164715892E+38</td>
</tr>
<tr>
<td align="center">sech</td>
<td align="center">Returns the hyperbolic secant of a value, <br>Defined as sech(x) = 1 / cosh(x).</td>
<td align="center">bi.sech(value)<br>Ex: sech(65) = 1.1800181083194122e-28</td>
</tr>
<tr>
<td align="center">csch</td>
<td align="center">Returns the hyperbolic cosecant of a value, <br>Defined as csch(x) = 1 / sinh(x).</td>
<td align="center">bi.csch(value)<br>Ex: bi.csch(45) = 5.725037161098787e-20</td>
</tr>
<tr>
<td align="center">tanh</td>
<td align="center">Returns the hyperbolic tangent of a value, <br>Defined as tanh(x) = (exp(2 x) - 1) / (exp(2 x) + 1).</td>
<td align="center">bi.tanh(value)<br>Ex: bi.tanh(90) = 1</td>
</tr>
<tr>
<td align="center">coth</td>
<td align="center">Returns the hyperbolic cotangent of a value, <br>Defined as coth(x) = 1 / tanh(x).</td>
<td align="center">bi.coth(value)<br>Ex: bi.coth(30) = 1</td>
</tr>
<tr>
<td align="center">asin</td>
<td align="center">Returns the inverse sine of a value.</td>
<td align="center">bi.asin(value)<br>Ex: bi.asin(30) = 0.5</td>
</tr>
<tr>
<td align="center">acos</td>
<td align="center">Returns the inverse cosine of a value.</td>
<td align="center">bi.acos(value)<br>Ex: bi.acos(0.5) = 1.0471975511965979 &amp;  bi.acos(bi.cos(1.5)) =1.5</td>
</tr>
<tr>
<td align="center">asec</td>
<td align="center">Returns the inverse secant of a value.</td>
<td align="center">bi.asec(value)<br>Ex: bi.asec(0.5) = 1.0471975511965979</td>
</tr>
<tr>
<td align="center">acsc</td>
<td align="center">Returns the inverse cosecant of a value, <br>Defined as acsc(x) = asin(1/x).</td>
<td align="center">bi.acsc(value)<br>Ex: bi.acsc(0.5) = 0.5235987755982989 &amp;, bi.acsc(bi.csc(1.5)) =1.5</td>
</tr>
<tr>
<td align="center">atan</td>
<td align="center">Returns the inverse tangent of a value.</td>
<td align="center">bi.atan(value)<br>Ex: bi.atan(0.5) = 0.4636476090008061, bi.atan(bi.tan(1.5)) = 1</td>
</tr>
<tr>
<td align="center">acot</td>
<td align="center">Returns the inverse cotangent of a value, <br>Defined as acot(x) = atan(1/x).</td>
<td align="center">bi.acot(value)<br>Ex: bi.acot(0.5) = 0.4636476090008061</td>
</tr>
<tr>
<td align="center">atan2</td>
<td align="center">Returns the inverse tangent function with two arguments, y/x.</td>
<td align="center">bi.atan2(value)<br>Ex:</td>
</tr>
<tr>
<td align="center">asinh</td>
<td align="center">Returns the hyperbolic arcsine of a value, <br>Defined as asinh(x) = ln(x + sqrt(x^2 + 1)).</td>
<td align="center">bi.asinh(value)<br>Ex: bi.asinh(0.5) = 0.48121182505960347</td>
</tr>
<tr>
<td align="center">acosh</td>
<td align="center">Returns the hyperbolic arccos of a value, <br>Defined as acosh(x) = ln(sqrt(x^2 - 1) + x).</td>
<td align="center">bi.acosh(value)<br>Ex: bi.acosh(1.5) = 0.9624236501192069</td>
</tr>
<tr>
<td align="center">asech</td>
<td align="center">Returns the hyperbolic arcsecant of a value, <br>Defined as asech(x) = acosh(1/x) = ln(sqrt(1/x^2 - 1) + 1/x).</td>
<td align="center">bi.asech(value)<br>Ex: bi.asech(0.5) = 1.3169578969248166</td>
</tr>
<tr>
<td align="center">acsch</td>
<td align="center">Returns the hyperbolic arccosecant of a value, <br>Defined as acsch(x) = asinh(1/x) = ln(1/x + sqrt(1/x^2 + 1)).</td>
<td align="center">bi.acsch(value)<br>Ex: bi.acsch(0.5) = 1.4436354751788103</td>
</tr>
<tr>
<td align="center">atanh</td>
<td align="center">Returns the hyperbolic arctangent of a value, <br>Defined as atanh(x) = ln((1 + x)/(1 - x)) / 2.</td>
<td align="center">bi.atanh(value)<br>Ex: bi.atanh(0.5) = 0.5493061443340549</td>
</tr>
<tr>
<td align="center">acoth</td>
<td align="center">Returns  the hyperbolic arccotangent of a value, <br>Defined as acoth(x) = atanh(1/x) = (ln((x+1)/x) + ln(x/(x-1))) / 2.</td>
<td align="center">bi.acoth(value)<br>Ex: bi.acoth(0.5) = 0.8047189562170503</td>
</tr>
</tbody>
</table><h3 id="constant">Constant</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">e, E</td>
<td align="center">Returns the Euler’s number, the base of the natural logarithm</td>
<td align="center">2.71828182845904</td>
</tr>
<tr>
<td align="center">i</td>
<td align="center">Returns Imaginary unit, defined as i*i = -1. A complex number is described as a + bi, where a is the real part, and b is the imaginary part.</td>
<td align="center">sqrt(-1)</td>
</tr>
<tr>
<td align="center">Infinity</td>
<td align="center">Returns Infinity, a number which is larger than the maximum number that can be handled by a floating point number.</td>
<td align="center">Infinity</td>
</tr>
<tr>
<td align="center">LN2</td>
<td align="center">Returns the natural logarithm of 2.</td>
<td align="center">0.6931471805599451</td>
</tr>
<tr>
<td align="center">LN10</td>
<td align="center">Returns the natural logarithm of 10.</td>
<td align="center">2.30258509299404</td>
</tr>
<tr>
<td align="center">LOG2E</td>
<td align="center">Returns the base-2 logarithm of E</td>
<td align="center">1.44269504088896</td>
</tr>
<tr>
<td align="center">LOG10E</td>
<td align="center">Returns the base-10 logarithm of E.</td>
<td align="center">0.43429448190325104</td>
</tr>
<tr>
<td align="center">NaN</td>
<td align="center">Not a number.</td>
<td align="center">NaN</td>
</tr>
<tr>
<td align="center">null</td>
<td align="center">Value null.</td>
<td align="center">null</td>
</tr>
<tr>
<td align="center">phi</td>
<td align="center">Phi is the golden ratio in math this is separately coded has unicode glyph ϕ</td>
<td align="center">1.61803398874989</td>
</tr>
<tr>
<td align="center">pi, PI</td>
<td align="center">Returns the value of pi which is a mathematical constant that is the ratio of a circle’s circumference to its diameter.</td>
<td align="center">3.14159265358979</td>
</tr>
<tr>
<td align="center">SQRT1_2</td>
<td align="center">Returns the square root of 1/2.</td>
<td align="center">0.707106781186547</td>
</tr>
<tr>
<td align="center">SQRT2</td>
<td align="center">Returns the square root of 2.</td>
<td align="center">1.41421356237309</td>
</tr>
<tr>
<td align="center">tau</td>
<td align="center">Returns Tau value which is the ratio constant of a circle’s circumference to radius, equal to 2 * pi.</td>
<td align="center">6.28318530717958</td>
</tr>
<tr>
<td align="center">uninitialized</td>
<td align="center">Constant used as default value when resizing a matrix to leave new entries uninitialized</td>
<td align="center">-</td>
</tr>
</tbody>
</table><h3 id="unit-">Unit	:</h3>

<table>
<thead>
<tr>
<th>Name</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td>to</td>
<td>Returns the converted unit value of a given value</td>
<td>Ex: bi.unit(“2 inch”).to(“cm”)</td>
</tr>
</tbody>
</table><h3 id="utils-">Utils :</h3>

<table>
<thead>
<tr>
<th align="center"><strong>Name</strong></th>
<th align="center"><strong>Description</strong></th>
<th align="center"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">to</td>
<td align="center">Returns the converted unit value of a given value</td>
<td align="center">bi.unit(“x unit1”).to(“unit2”)<br>Ex: bi.number(bi.unit(“2 inch”).to(“cm”),“cm”) = 5.08 <br>       bi.number(bi.unit(“16 bytes”).to(“bits”),“bits”) = 128</td>
</tr>
<tr>
<td align="center">clone</td>
<td align="center">Clone an object.</td>
<td align="center">bi.clone(x) <br>Ex: bi.clone(“3.5”) = 3.5</td>
</tr>
<tr>
<td align="center">isInteger</td>
<td align="center">Returns true / false after validating the given value is integer<br>true if the given value is integer or else false</td>
<td align="center">bi.inInteger(value)<br>Ex: bi.isInteger(2) = true, <br>       bi.isInteger(2.5) = false</td>
</tr>
<tr>
<td align="center">isNaN</td>
<td align="center">Returns true / false after validating the given value  whether it is NaN (not a number)</td>
<td align="center">bi.isNaN(value)<br>Ex: bi.isNaN(3) = false, <br>      bi.isNaN(NaN) = true</td>
</tr>
<tr>
<td align="center">isPositive</td>
<td align="center">Returns true / false after validating the given value is positive<br>true if the given value is integer or else false</td>
<td align="center">bi.isPositive(value)<br>Ex: bi.isPositive(3) = true, <br>      bi.isPositive(-3) = false</td>
</tr>
<tr>
<td align="center">isNegative</td>
<td align="center">Returns true / false after validating the given value is negative<br>true if the given value is integer or else false</td>
<td align="center">bi.isNegative(value)<br>Ex: bi.isNegative(3) = false, <br>      bi.isNegative(-3) = true</td>
</tr>
<tr>
<td align="center">isNumeric</td>
<td align="center">Returns true / flase after validating the given value is numeric or not</td>
<td align="center">bi.isNumeric(value)<br> Ex: bi.isNumeric(3) = true, <br>      bi.isNumeric(“string”) = false</td>
</tr>
<tr>
<td align="center">isPrime</td>
<td align="center">Results true / false after validating  the given value is  whether a prime number</td>
<td align="center">bi.isPrime(value)<br> Ex: bi.isPrime(3) = true, <br>       bi.isPrime(4) = false</td>
</tr>
<tr>
<td align="center">isZero</td>
<td align="center">Results true / false after validating  the given value is  whether it is zero</td>
<td align="center">bi.isZero(value)<br> Ex: bi.isZero(1) = false, <br>       bi.isZero(0) = true</td>
</tr>
<tr>
<td align="center">typeof</td>
<td align="center">Determine the type of a variable.</td>
<td align="center">bi.typeof(3.5) = number, <br>bi.typeof(math.complex(‘2-4i’)) = complex,<br>bi.typeof(‘hello world’) = string</td>
</tr>
</tbody>
</table><h2 id="usage-of-mathplugin-for-grid-view">Usage of #math#plugin# for Grid View</h2>
<p>Plugin operators provides complete authority on creation,edition and deletion of raw data. It allows customization of data using JavaScript API language  as per the business requirement.</p>
<ul>
<li><strong>_biCalculation.pluginData.raw</strong>  holds the Raw JSON data and can be transformed as per the requirement.</li>
</ul>
<pre><code>#math#plugin#

/*START*/
function localFunction(param1,param2,...)
{ 
 // update raw data 
for(var i =0 ; i &lt; _biCalculation.pluginData.raw.length; i++)
    {
         var item = biCalculation.pluginData.raw[i];
         
    }

.................................
................................

return x;
}
/*END*/
</code></pre>
<h2 id="arithmetic-">Arithmetic &amp;</h2>
<p>Logical operations on Data Fields</p>
<p>Perform Arithmetic operation on desired fields in calculated columns.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/60036e93167331ca3442d5bb10ff48209b021fdd/images/arth_add.png" alt="enter image description here"></p>
<h2 id="calculate-custom-functions">Calculate Custom Functions</h2>
<p>it will execute a series of actions on a database record and returns a particular value.</p>
<p><strong>Syntax</strong></p>
<pre><code>#math#
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
</code></pre>
<h2 id="access-global-parameters">Access Global Parameters</h2>
<p>Global parameter is a flat file used to manipulate,control and organize the data which is not available in database and accessed this data in report.</p>
<p>While calculating an expression over a database value using field reference.</p>
<p><strong>Syntax</strong></p>
<pre><code>bi.in_global_keys(["ParameterColumnName"],["DatabaseValue"],"ParameterName.Field"])
</code></pre>
<ul>
<li><strong>Parameter Column Name</strong> Refer the key name from global parameter.</li>
<li><strong>Database Value</strong> Refers database value.</li>
<li><strong>Parameter Name Field</strong> Returns the field from global parameter it is applicable in 3 different ways ;</li>
</ul>
<p><strong>1.  Static value</strong> Global parameters refers to a static value.</p>
<p><strong>Syntax :</strong></p>
<pre><code> bi.in_global_keys( ["Parameter_Column_Name "],["Reference string" ],"Global_parameter.field")
</code></pre>
<p><strong>Example :</strong></p>
<pre><code>#math#
bi.in_global_keys( ["Station_Name"],["Station_1" ],"Calc_ONRAW.value")
</code></pre>
<p><strong>2. Reference value</strong> Global parameters refers to reference value.</p>
<p><strong>Syntax :</strong></p>
<pre><code>  bi.in_global_keys( ["Parameter_Column_Name "],["database column" ],"Global_parameter.field")
</code></pre>
<p><strong>Example :</strong></p>
<pre><code>#math#
bi.in_global_keys( ["Station_Name"],[${ROOT.AUTOTEST_ORDERS.STATIONCODE_724} ],"Calc_ONRAW.value")
</code></pre>
<p><strong>3. Login Name(User Id)</strong> Provide Access based on Login ID.</p>
<p><strong>Syntax :</strong></p>
<pre><code>bi.in_global_keys(["ParameterColumnName","ParameterUserID"],["DatabaseField","bi._globals("#userid#")"],"ParameterName.Field"])
</code></pre>
<p><strong>Example :</strong></p>
<pre><code>#math#
bi.in_global_keys( ["UserName","Login_name"],[${ROOT.EMPLOYEES.NAME_661} 
,bi._globals("#userid#")],"CalcCol_Stage2.SeizeLimit)

</code></pre>
<h2 id="calculate-on-raw-functionality">Calculate on Raw functionality</h2>
<p>If calculate raw is enabled even after grouping the calculation is applied to each and every record and displays the final result.<br>
If disabled the calculation will be done after the grouping.</p>
<pre><code>${ROOT.BI_ORDERS.sum_AMOUNT}+2
</code></pre>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/fe0920a5f1e6abcabfab1c22ce5d8a5df08ee789/images/on_ram.png" alt="enter image description here"></p>
<h2 id="calculate-column-with-pivot-offset">Calculate column with Pivot Offset</h2>
<p>For Instance, to look at the quantity_sum difference by each month for specific customer then select customer_id,add pivot to  month.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/cfd94b0b9fe7b31888a3c426882590bae7914fc4/images/pivot_offset.png" alt="enter image description here"></p>
<p>We can get quantity_sum difference of each month for specific customer using Pivot_Offset() function.</p>
<p>${ROOT.BI_ORDERS.sum_QUANTITY} -bi.pivot_offset( #{ROOT.BI_ORDERS.sum_QUANTITY} ,0,-1)</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/eb64533dd879286986c2b3f4a9f69295ab96da8b/images/pivot_offset2.png" alt="enter image description here"></p>
<h2 id="defining-local-function">Defining Local Function</h2>
<p>Custom function is a block of code (series of statements which intended to a particular task) with submitted inputs and derivable output.<br>
It will ease-up the process of calculations When a series of statements or actions to be repeated on a set of values and output to be derived. Bi+ supports local function which can be written inside the dialog box as follows:</p>
<pre><code>/*START*/
function fname(param1, param2, param3 ...){

statement 1;
statement 2;                                     // Function body
statement 3;
...........
...........

return `;   
}
/*END*/
fname(value1, value2, value3, .....)    //Call Function
</code></pre>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/52b7c4357f0c07e4a89b14f018cf3d877a5ba4f3/images/cal_local_fucntion.png" alt="enter image description here"></p>
<blockquote>
<p><strong>Note :</strong>  it returns value 6.</p>
</blockquote>

