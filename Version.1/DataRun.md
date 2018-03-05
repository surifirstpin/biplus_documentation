---


---

<center><h1>Analysis</h1></center>
<h2 id="definition">Definition</h2>
<p>Using data analysis user can retrieve the data and build the query applying data exploration by slice and dice of report information.</p>
<h2 id="build-query">Build Query</h2>
<p>Under data analysis section, select the project and model for which you want to explore the data. Data analysis section contains list of dimension and measures which acts as fundamental building blocks for a query.</p>
<p><strong>Getting Started :</strong></p>
<p>From the list of dimensions and measures, select set of fields to access the information.</p>
<ol>
<li>Select one or more grey fields(Dimensions) to group your data.</li>
<li>Click one or more orange fields(Measures) to add information about those groups, such as totals and counts.</li>
</ol>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/92e1e1b322bed3026eedfd1a2dca2bc3c3dfea78/images/visu_run.png" alt="enter image description here"></p>
<p><strong>Dimensions</strong> are list of fields that can be used for applying filter options, for instance:</p>
<ul>
<li>An <strong>Attribute,</strong> which has a direct association to a column in an primary table.</li>
<li>A <strong>Fact or a numerical value</strong>.</li>
<li>A <strong>Derived value,</strong> computed based on the values of other fields in a single row.</li>
</ul>
<blockquote>
<p><strong>Example :</strong> Dimensions for “Customer” view includes customer name,customer phone number and customer email etc.</p>
</blockquote>
<p><strong>Measure</strong> is a list of fields that uses a SQL aggregate function, such as COUNT, SUM, AVG, MIN or MAX. Any field that is counted based on the values is referred as measure. Measures can be used to filter grouped values.</p>
<blockquote>
<p><strong>Example :</strong> measures for a “Amount” is Amount_sum, Amount_avg, Amount_min, Amount_max etc.</p>
</blockquote>
<p>Select the fields from the list to retrieve field values and apply filter options :</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/visu_fields.png" alt="enter image description here"></p>
<h2 id="filters-hidden-filters">Filters /Hidden Filters</h2>
<ol start="3">
<li>Click on <strong>Filter</strong> to add filter to your report.</li>
</ol>
<p>Filters is a optional list of filter expression applied to measure calculation, below are the available operations that can be applied for String , Integer and Date.</p>
<h3 id="string-">String :</h3>

<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>is not null</td>
<td>should not be equal to null</td>
</tr>
<tr>
<td>is null</td>
<td>equal to null</td>
</tr>
<tr>
<td>is not empty</td>
<td>should not be empty</td>
</tr>
<tr>
<td>is empty</td>
<td>should be empty</td>
</tr>
<tr>
<td>equal</td>
<td>should be equals to specific value</td>
</tr>
<tr>
<td>not equal</td>
<td>shouldn’t be equal to specific value</td>
</tr>
<tr>
<td>in</td>
<td>selection based on combination of filter values</td>
</tr>
<tr>
<td>not in</td>
<td>excluding set of values</td>
</tr>
<tr>
<td>begins with</td>
<td>finds any value that starts with mentioned substring</td>
</tr>
<tr>
<td>doesn’t begins with</td>
<td>finds a value that doesn’t begin with mentioned sub-string</td>
</tr>
<tr>
<td>Contains</td>
<td>contains mentioned sub-string</td>
</tr>
<tr>
<td>doesn’t contain</td>
<td>finds a value which does not contain mentioned sub-string</td>
</tr>
<tr>
<td>ends with</td>
<td>should end with mentioned sub-string</td>
</tr>
<tr>
<td>doesn’t end with</td>
<td>should not end with mentioned sub-string</td>
</tr>
</tbody>
</table><h3 id="integer">Integer:</h3>

<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>is not null</td>
<td>should not be equal to null value</td>
</tr>
<tr>
<td>is null</td>
<td>should be equal to null value</td>
</tr>
<tr>
<td>not empty</td>
<td>data is not empty</td>
</tr>
<tr>
<td>is empty</td>
<td>data is empty</td>
</tr>
<tr>
<td>equal</td>
<td>data equal to specified value</td>
</tr>
<tr>
<td>not equal</td>
<td>data not equal to specified value</td>
</tr>
<tr>
<td>in</td>
<td>data equal to specified values</td>
</tr>
<tr>
<td>not in</td>
<td>data not equal to specified values</td>
</tr>
<tr>
<td>less</td>
<td>data less than specified value</td>
</tr>
<tr>
<td>less or equal</td>
<td>data less than or equal to specified value</td>
</tr>
<tr>
<td>greater</td>
<td>data greater than specified value</td>
</tr>
<tr>
<td>greater or equal</td>
<td>data greater than or equal to specified value</td>
</tr>
<tr>
<td>between</td>
<td>data in between the specified range</td>
</tr>
<tr>
<td>not between</td>
<td>data not in between the specified range</td>
</tr>
</tbody>
</table><h3 id="date-">Date :</h3>

<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>timeline</td>
<td>data from specific time scale</td>
</tr>
<tr>
<td>equal</td>
<td>data from specific date</td>
</tr>
<tr>
<td>not equal</td>
<td>data excluding from specific date</td>
</tr>
<tr>
<td>between</td>
<td>data in between the specified dates</td>
</tr>
<tr>
<td>not between</td>
<td>excluding the data between the specified range</td>
</tr>
<tr>
<td>less or equal</td>
<td>data up to specified date</td>
</tr>
<tr>
<td>greater or equal</td>
<td>data from the specified date</td>
</tr>
<tr>
<td>is not null</td>
<td>data which is not equal to null</td>
</tr>
<tr>
<td>is null</td>
<td>data which is equal to null</td>
</tr>
</tbody>
</table><p><strong>Hidden Filters :</strong></p>
<p>On applying hidden filters, the column fields are visible in the list of filter expression specified and displays the data depending on the filters applied.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/e777906f8a8aafdb323a64c65c2a1c9e69cb01b1/images/hidden_filter.png" alt="enter image description here"></p>
<ol start="4">
<li>Click on <strong>Run.</strong></li>
</ol>
<h2 id="order--ascending--descending">Order  (Ascending / Descending)</h2>
<p>Perform sorting on data retrieved by applying ascending and descending orders.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/3a66bec34562013987acc9ca17385d78b2741ac4/images/sorting.png" alt="enter image description here"></p>
<h2 id="local-sorting">Local Sorting</h2>
<p>Local Sorting can be applied directly in the column field.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/c6f7269afe640dd6c16f4fd1d4423aa394bdf2b4/images/local_sorting.png" alt="enter image description here"></p>
<h2 id="row-limitation-and-query-time">Row Limitation and Query Time</h2>
<ul>
<li><strong>Limit</strong> allows row limitation while displaying data.</li>
<li><strong>Query time</strong> of the report is displayed on top of the analysis section.</li>
</ul>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/row_limit.png" alt="enter image description here"></p>
<h2 id="pivot-table">Pivot table</h2>
<ul>
<li><strong>Pivot</strong> checks each dimension horizontally and reduces the effect of scrolling down the data.</li>
</ul>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/78c46d819c716135d45ff60b9a71b15dd9e7a97f/images/pivot.png" alt="enter image description here"></p>
<blockquote>
<p>Note : You can directly apply pivot option in data output field by selecting <strong>pivot</strong> option from drop down.</p>
</blockquote>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/1bae129344332eabae71b594bd320f0f5c5b4a68/images/pivot2.png" alt="enter image description here"></p>
<h2 id="data">Data</h2>
<p>Depending on selection of fields, data section is enabled.</p>
<ul>
<li><strong>Row Grouping</strong> enables grouping for column fields and it is applied for first column field only.</li>
<li><strong>Explore Enabled</strong> to explore data which are grouped.</li>
<li><strong>Stacked</strong> are used whether to stack the values at y-axis.</li>
<li><strong>Datasets</strong> specifies the alignment, formats, currency, number of y-axis and grouping of aggregates for the legends used in the visualization menu.</li>
<li><strong>Calculate on Raw data</strong> Calculates the field values before applying grouping, pivot or other parameters.</li>
</ul>
<h3 id="group-aggregate">Group aggregate</h3>
<p>It displays consolidated values of grouped fields.</p>
<p><strong>a.</strong> Enable row grouping by selecting the checkbox.<br>
<strong>b.</strong> Explore the primary column fields data<br>
individually, which are grouped under the column field.<br>
<strong>c.</strong> Select the field to perform row grouping.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/657b29d2f18b269f2964e8150a3670df8db7869c/images/group_aggregate.png" alt="enter image description here"></p>
<h3 id="number-format--currency-option-for-fields">Number Format &amp; Currency option for fields</h3>
<p>Apply different number formats and currency options to measures.<br>
<strong>a.</strong>  Select required number format from list.<br>
<strong>b.</strong>  Select currency you would like to view.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/a289a74e21b8055ac795aa2bb25d4cb945bc02b0/images/number_format.png" alt="enter image description here"></p>
<h4 id="list-of-number-formats-applicable-on-measures-">list of number formats applicable on measures :</h4>

<table>
<thead>
<tr>
<th>Number formats</th>
</tr>
</thead>
<tbody>
<tr>
<td>#</td>
</tr>
<tr>
<td>#.00</td>
</tr>
<tr>
<td>#.000</td>
</tr>
<tr>
<td>#,##0</td>
</tr>
<tr>
<td>#,##0.0</td>
</tr>
<tr>
<td>#,##0.00</td>
</tr>
<tr>
<td>#,##0.00</td>
</tr>
<tr>
<td>#,##0.000</td>
</tr>
<tr>
<td>###,###</td>
</tr>
<tr>
<td>###,###.0</td>
</tr>
<tr>
<td>###,#»#.00</td>
</tr>
<tr>
<td>###,###.000</td>
</tr>
<tr>
<td>###.###,o</td>
</tr>
<tr>
<td>###,###.00</td>
</tr>
<tr>
<td>####,####.000</td>
</tr>
<tr>
<td>###.###,0</td>
</tr>
<tr>
<td>###.###,00</td>
</tr>
<tr>
<td>###.###,000</td>
</tr>
<tr>
<td>### ###</td>
</tr>
<tr>
<td>#%</td>
</tr>
<tr>
<td>#.0%</td>
</tr>
<tr>
<td>#.00%</td>
</tr>
<tr>
<td>#.000%</td>
</tr>
<tr>
<td>#K</td>
</tr>
<tr>
<td>#M</td>
</tr>
</tbody>
</table><h4 id="list-of-currency-applicable-on-measures-">list of currency applicable on measures :</h4>

<table>
<thead>
<tr>
<th>Currency</th>
</tr>
</thead>
<tbody>
<tr>
<td>$</td>
</tr>
<tr>
<td>₹</td>
</tr>
<tr>
<td>€</td>
</tr>
<tr>
<td>£</td>
</tr>
</tbody>
</table><h2 id="group--un-group">Group / Un-Group</h2>
<p>Select <strong>Group</strong> options to group fields and select <strong>Un-Group</strong> to release the same.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/12c2bc69fcf082dc620f2819ae901ae9c7a962a7/images/group.png" alt="enter image description here"></p>
<h2 id="calculated-column">Calculated column</h2>
<p>Calculated column is statement or expression or a function operator which can be used to derive the column values.</p>
<ul>
<li><strong>Field name</strong> unique identifier name to refer calculated column.</li>
<li><strong>Label</strong> labeling the calculated column.</li>
<li><strong>Data type</strong> data type used (string,number).</li>
<li><strong>Field type</strong> derives dimension or measure.</li>
<li><strong>Calculation</strong> derive arithmetical &amp; logical expressions.</li>
<li><strong>Calculate on the raw data</strong> this function is applied directly on the retrieved value of the fields, initially before pivot or grouping options are applied.</li>
</ul>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/c383b6e32c490bd5f0a32eb8cf2dcd4bb1fbfa9d/images/calculate%20column1.png" alt="enter image description here"></p>
<p><strong>Run</strong> the report after deriving calculated column, all the values obtained by applying calculation column is visible in green colour.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/c383b6e32c490bd5f0a32eb8cf2dcd4bb1fbfa9d/images/calculate%20column2.png" alt="enter image description here"></p>
<h2 id="pin-or-remove-pin">Pin or Remove Pin</h2>
<p>To freeze the field values click on ** Pin** options in drop down and click on <strong>Remove Pin</strong> to release it.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/b001b2f2f386a9730f3be339c38c54b73c69c5b9/images/pin.png" alt="enter image description here"></p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/f14d690d76bb1f0feacaf24259f67d1b9b55ea52/images/unpin.png" alt="enter image description here"></p>
<h2 id="field-visualization-on--off">Field Visualization On / Off</h2>
<p>To hide field values click  <strong>Hide Visualization</strong> option in the drop down option.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/bee13bc200cda9988be61a3c7b58de502a4915fa/images/hide_visu.png" alt="enter image description here"></p>
<h2 id="sql-query">SQL Query</h2>
<p>Selected fields will build a SQL query in data analysis :<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/cb3255937763c7b895145485b1da69d33684c675/images/sql.png" alt="enter image description here"></p>

