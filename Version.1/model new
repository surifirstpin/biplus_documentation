---


---

<center><h1>Model</h1></center>
<p>A model is a customized gateway into the database for accessing data as per business logic. Bi+ provides an IDE, which allows mappings between views (database tables) and apply several filters on the data as per business requirement. It is designed in such a way that it provides a spontaneous data analysis to specific business users.</p>
<blockquote>
<p><strong>Example :</strong> If a sales manager wants to retrieve different data then material manager, we need to define login based filters on the model with specific assignments to the users.</p>
</blockquote>
<p>A Model can be defined in 3 steps, as followed</p>
<ul>
<li>Create a Project with required database and respective tables,</li>
<li>Customize the Model using IDE as per the business requirement,</li>
<li>Organize the fields in views with required manipulation.</li>
</ul>
<h2 id="creating-a-project">Creating a Project:</h2>
<blockquote>
<p>Navigation: Model → Projects → +New Project</p>
</blockquote>
<ol>
<li>Click on <strong>+New Project</strong> to create a new project.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/c9ed66676e23e0ae62ebdd2103760238d0a1b0f3/images/new_project.png" alt="enter image description here"></li>
</ol>
<p>The following are the list of entries made to create a project.</p>
<ul>
<li>
<p><strong>Project Name</strong> Enter the project name as per requirement.</p>
</li>
<li>
<p><strong>Connection</strong> Select the database connection from the list provided.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model2.png" alt="enter image description here"></p>
</li>
<li>
<p><strong>Database</strong>  Select the database for configuration from databases section. All the selected databases are visible under <strong>Selected Databases</strong> section.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model3.png" alt="enter image description here"></p>
</li>
<li>
<p><strong>Tables</strong> Select the required tables from which the data to be retrieved. Select the desired table fields from Table section, All the selected tables are visible under <strong>Selected Tables</strong> section.</p>
</li>
</ul>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/add_tables.png" alt="enter image description here"></p>
<ol start="2">
<li><strong>Auto Build Joins(check box)</strong> If selected, then it will adopt all the defined mappings or relations between different tables of a database &amp; displays it in model. Else only tables with no mappings will be adopted as views in model.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model%204.png" alt="enter image description here"></li>
</ol>
<ul>
<li><strong>Privacy</strong> Select one of the three options “Public”, “Private”, “Share” as per the requirement.</li>
<li><strong>Private ()</strong> report saved in private section and accessed by the user itself.</li>
<li><strong>Public ()</strong> the report is saved in public section and accessed by all the users.</li>
<li><strong>Share ()</strong> the report saved under share section and accessed by specific set of users.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/8dcf17faa6e3f50d5f3f79ae269a02c1eb7237c9/images/save_project.png" alt="enter image description here"></li>
</ul>
<ol start="3">
<li>Once all the entries are made click on <strong>Save project</strong> to save the project created.</li>
</ol>
<h2 id="model-and-customization">Model and Customization:</h2>
<p>After saving a project, Bi+ will display the views and relevant information of the project as a Model which can be customized as per the business requirement. Model Customization can be done among views in the following ways.</p>
<ol>
<li>A new mapping or relation can be defined among views based on a specific condition.</li>
<li>Edit the join criteria between views.</li>
<li>Define filters on the data with different mapped views.</li>
</ol>
<p><strong>The list of keywords used in Model are:</strong></p>

<table>
<thead>
<tr>
<th align="left"><strong>Serial No.</strong></th>
<th>Keyword</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">1</td>
<td><strong>For Model</strong></td>
<td></td>
</tr>
<tr>
<td align="left"></td>
<td>project</td>
<td>displays the project name</td>
</tr>
<tr>
<td align="left"></td>
<td>info</td>
<td>allows to describe the project with meaning full information</td>
</tr>
<tr>
<td align="left"></td>
<td>connections</td>
<td>displays the connection name erf the selected project</td>
</tr>
<tr>
<td align="left"></td>
<td>explore</td>
<td>displays the views (the tabes selected in the project) with the selected charecteristics</td>
</tr>
<tr>
<td align="left">2</td>
<td><strong>For View</strong></td>
<td></td>
</tr>
<tr>
<td align="left"></td>
<td>name</td>
<td>name of the table name in database</td>
</tr>
<tr>
<td align="left"></td>
<td>label</td>
<td>allows to customize the dts play name of the view in Bi+</td>
</tr>
<tr>
<td align="left"></td>
<td>filters</td>
<td>the list of filters to be applied on the data from the view and respective mapped views defined in the 'joins"section</td>
</tr>
<tr>
<td align="left"></td>
<td>joins</td>
<td>specifies the list of associated views which are mapped with the current view &amp; mention the mappng criteria</td>
</tr>
<tr>
<td align="left">2A</td>
<td><strong>Filter characteristics</strong></td>
<td>Filters can be date-based, string-based, value-based &amp; user-based</td>
</tr>
<tr>
<td align="left"></td>
<td>name</td>
<td>name of the filter</td>
</tr>
<tr>
<td align="left"></td>
<td>filter_sql</td>
<td>the query phrase which acts as a filter, Ex col name = “Employee Name’</td>
</tr>
<tr>
<td align="left"></td>
<td>apply</td>
<td>to specify 'tiirfor always applicability</td>
</tr>
<tr>
<td align="left"></td>
<td>position</td>
<td>describes the priority of the filter phrase with other data filters can be assigned as 'before" or 'tifter"</td>
</tr>
<tr>
<td align="left">2B</td>
<td><strong>Joins characteristics</strong></td>
<td></td>
</tr>
<tr>
<td align="left"></td>
<td>join</td>
<td>derive the relationship between 2 views based on the condition.</td>
</tr>
<tr>
<td align="left"></td>
<td>join_type</td>
<td>derives type of join condition to be applied (Left,Right,inner join)</td>
</tr>
<tr>
<td align="left"></td>
<td>join_on</td>
<td>defines the relationship between views by associated fields.</td>
</tr>
</tbody>
</table><p><strong>2.A  Filters in Model :</strong></p>
<p>To filter data from a view and the respective mapping views, the filter criteria can be defined in “filters” section.</p>
<pre><code> {
"name": "View_Name",
"label": "View_Name",
"filters": [{
"name": "filter_name",  // filter name
"filter_sql": Filter Expression ",  // expression or condition to be applied.
"apply": "all",
"position": "before"  // position of filter
            }],
"joins":[]
}
</code></pre>
<p>Filter can be mentioned with two specific attributes such as,</p>
<ol>
<li><strong>filter_sql :</strong> the filter expression or condition. Filter expression can be date-based, string-based, number-based &amp; even login-based.</li>
</ol>
<ul>
<li><strong>Date-based, String-based, Number-based :</strong> standard filters which are applicable on date, string, number fields in database are allowed.</li>
</ul>
<blockquote>
<p>Example :<br>
Date based : ROOT.Orders.OrderDate &lt; TRUNC(SYSDATE)<br>
String-based : ROOT.Orders.PaymentMode IN (‘Cash’,’PayTM’)<br>
Number-based : ROOT.BI_Orders.Amount IS NOT NULL.</p>
</blockquote>
<ul>
<li><strong>User-based :</strong> Bi+ allows to filter the data based on login user-specification. Using global parameters facility, data for the same combination of columns can be controlled for different users. That means, for a particular user login, the data retrievable in Analyze section will be constrained with a list of pre-defined values.</li>
</ul>
<pre><code> " DB.TABLE.COLUMN IN
  (#{GlobalParam.Ref_field,#userid#,gp_username_field})" 
</code></pre>
<ul>
<li><strong>GlobalParam</strong> the name of the global parameter which contains the user based list of values.</li>
<li><strong>Ref_field</strong> the column name in global parameter which contains the filter values.</li>
<li><strong>gp_username_field</strong> the column name in global parameter which contains the usernames</li>
</ul>
<blockquote>
<p>Example:<br>
" ROOT.Orders.StationCode IN (#{ModelParams.StationCode,#userid#,Username})"</p>
</blockquote>
<ol start="2">
<li><strong>Position</strong> It is the priority of the filter and can be “before” or “after”.</li>
</ol>
<ul>
<li><strong>Before</strong> the filter will be applied first to the data, before any other filters on data are applied in Analyze section.</li>
<li><strong>After</strong> the filter will be applied to the data only after other filters are applied in Analyze section.</li>
</ul>
<p><strong>2.B. Join Characteristics :</strong></p>
<p>The attributes in “joins” section will be as follows:</p>
<ul>
<li>** join** the view name to be joined with the primary view.</li>
<li><strong>join_type</strong>  the method of joining the two views. It can be left, right and is similar to the “join” functionality.</li>
<li><strong>join_on</strong> the specific criterion for joining to views with a relation among relevant fields.</li>
</ul>
<pre><code>{
"name": "View_1", // Primary View
"label": "View_1",
"filters":[],
"joins":
[ 
{
"join": "View_2",  // Secondary View
"join_type": "left",  // Type of Join
"join_on": "${View_1.Field} = ${View_2.Field}"  // Join criteria
} 
]
}
</code></pre>
<h2 id="views-and-fields">Views and Fields:</h2>
<p>Views are independent tables chosen while creating a project. All the columns in the table are called fields of view and will be adopted with relevant features.</p>
<p>BiPlus allows various actions and they are performed in views as follows:</p>
<ol>
<li>Creating a new field (User Defined Fields),</li>
<li>Defining the output in a new field as resultant of arithmetical or logical operations among the database fields of the self view or from mapped views,</li>
<li>Assigning currency &amp; number format for measure fields,</li>
<li>extracting different date formats from the date field permissible formats like hour,day,week,month,quarter, year,date, week_day,date_month,date_quarter, date_hour, year_week</li>
<li>Assigning drill down fields for a field.</li>
<li>Defining values for different map co-ordinates.</li>
</ol>
<p>The Associated keywords with the views are flowing :</p>

<table>
<thead>
<tr>
<th align="left"><strong>1</strong></th>
<th>name</th>
<th>identifier of a custom field</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">2</td>
<td>label</td>
<td>allows to customise the display name of the view in bi+</td>
</tr>
<tr>
<td align="left">3</td>
<td>data_type</td>
<td>the outcome of the field from database it can be string, date or number</td>
</tr>
<tr>
<td align="left">4</td>
<td>type</td>
<td>either of the two values dimension or measure, string and date belongs to dimension and number belongs to measure</td>
</tr>
<tr>
<td align="left">5</td>
<td>time_frame</td>
<td>feature that extract different formats from the date field, for instance:  hour,day,week, month quarter; year, date. week_day,date_ month date_quarter date_hour, year_week</td>
</tr>
<tr>
<td align="left">6</td>
<td>lookup</td>
<td>a set of filter values for a specific field ether from database using a query or from a defined item list</td>
</tr>
<tr>
<td align="left">7</td>
<td>operator</td>
<td>the option to select single or multiple filters from the assigned lookup</td>
</tr>
<tr>
<td align="left">8</td>
<td>sql</td>
<td>the query phase which retreives the data from database Ex: $ {TABLE }. username</td>
</tr>
<tr>
<td align="left">9</td>
<td>summary</td>
<td>the option to aggregate a measure field.For instance Supports sum avg, count, min, max.</td>
</tr>
<tr>
<td align="left">10</td>
<td>drill_down_fields</td>
<td>the option to define the drill fields for the current field</td>
</tr>
<tr>
<td align="left">11</td>
<td>show_drill_down_measures</td>
<td>it carry forward the current state of measures to further drill level. It can applied using true or false condition</td>
</tr>
<tr>
<td align="left">12</td>
<td>vocalise</td>
<td>it controls the visibility of the field in Analyze section</td>
</tr>
<tr>
<td align="left">13</td>
<td>number_format</td>
<td>to define a number format for the field. the list of valid formats are described as Amexure 1</td>
</tr>
<tr>
<td align="left">14</td>
<td>currency</td>
<td>it defines the currency for the field.For instance “$”, “€”, “£”, “₹”.</td>
</tr>
<tr>
<td align="left">15</td>
<td>country_ref</td>
<td>option for enabling map view for different values with different geographical locations</td>
</tr>
</tbody>
</table><p><strong>Among the above stated list, the following are the special attributes for user convenience :</strong></p>
<ol>
<li><strong>lookup and operator :</strong> Using “lookup” feature, Bi+ allows to define a set of filter values for a field. The assignment can be made in the following two ways:</li>
</ol>
<ul>
<li><strong>Query</strong> an sql query returning a set of values can be written in “lookup” for a field. It will be useful if the filter values are large in number and becomes tedious to mention all of them as a list.</li>
</ul>
<blockquote>
<p>Ex: “lookup” : “SELECT DISTINCT Name FROM ROOT.Employees”</p>
</blockquote>
<ul>
<li><strong>Items</strong>  known set of values can be given with comma separation. It may be useful if the list is small and the items are known exactly to the user.</li>
</ul>
<blockquote>
<p>Ex: “lookup” : “Antonio, Bessanio, Portia”</p>
</blockquote>
<ul>
<li><strong>operator</strong> Sometimes, data to be retrieved from multiple filter values. BiPlus provides an option associated with lookup which can be defined to select single or multiple filter values. For selecting more than one filter value, operator should be defined as “multiple”.</li>
</ul>
<pre><code>operator:multiple.
</code></pre>
<ol start="2">
<li><strong>Number_format &amp; currency</strong> for reports convenience, a particular number format and currency can be assigned to a particular field so that whenever the report is created using this field, the number_format and currency will automatically displayed.</li>
</ol>
<ul>
<li><strong>Number_format</strong> There are various formats designed based on the common business usage.</li>
</ul>
<p><strong>The permissible list are :</strong></p>

<table>
<thead>
<tr>
<th align="left">For the Number =</th>
<th>12345678.567</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">S. No.</td>
<td>Number format</td>
<td align="left">Example</td>
</tr>
<tr>
<td align="left">1</td>
<td>#</td>
<td align="left">12345679</td>
</tr>
<tr>
<td align="left">2</td>
<td>#.0</td>
<td align="left">12345678.6</td>
</tr>
<tr>
<td align="left">3</td>
<td>#.00</td>
<td align="left">12345678.57</td>
</tr>
<tr>
<td align="left">4</td>
<td>#.000</td>
<td align="left">12345678.567</td>
</tr>
<tr>
<td align="left">5</td>
<td>#,##0</td>
<td align="left">1.23.45,679</td>
</tr>
<tr>
<td align="left">6</td>
<td>#.##0.00</td>
<td align="left">1.23.45,678.6</td>
</tr>
<tr>
<td align="left">7</td>
<td>#,##0.00</td>
<td align="left">1.23.45,678.57</td>
</tr>
<tr>
<td align="left">8</td>
<td>#,##0.000</td>
<td align="left">1.23.45.678.567</td>
</tr>
<tr>
<td align="left">9</td>
<td>##,###</td>
<td align="left">12.345.679</td>
</tr>
<tr>
<td align="left">10</td>
<td>###,###,0</td>
<td align="left">12.345.678.6</td>
</tr>
<tr>
<td align="left">11</td>
<td>###,###,0</td>
<td align="left">12.345.678.57</td>
</tr>
<tr>
<td align="left">12</td>
<td>###,###,000</td>
<td align="left">12.345.678.567</td>
</tr>
<tr>
<td align="left">13</td>
<td>###,###,0</td>
<td align="left">12.345.678.6</td>
</tr>
<tr>
<td align="left">14</td>
<td>###,###,00</td>
<td align="left">12.345.678.57</td>
</tr>
<tr>
<td align="left">15</td>
<td>###,###,000</td>
<td align="left">12.345.678.567</td>
</tr>
<tr>
<td align="left">16</td>
<td>### ###</td>
<td align="left">12 345 679</td>
</tr>
<tr>
<td align="left">17</td>
<td>#%</td>
<td align="left">12345679</td>
</tr>
<tr>
<td align="left">18</td>
<td>#,00%</td>
<td align="left">123456.786</td>
</tr>
<tr>
<td align="left">19</td>
<td>#,00%</td>
<td align="left">123456.7857</td>
</tr>
<tr>
<td align="left">20</td>
<td>#,000%</td>
<td align="left">123456.78567</td>
</tr>
<tr>
<td align="left">21</td>
<td>#K</td>
<td align="left">12345 678566999999k</td>
</tr>
<tr>
<td align="left">22</td>
<td>#M</td>
<td align="left">12.345678567IM</td>
</tr>
</tbody>
</table><ul>
<li><strong>Currency</strong> Bi+ supports following currency formats “$”, “€”, “£”, “₹”.</li>
</ul>
<pre><code>currency : currency_symbol
</code></pre>
<blockquote>
<p>Example : “currency” : “$”</p>
</blockquote>
<ol start="3">
<li><strong>Time_frame:</strong> Bi+ provides an option to extract different components associated with time stamp for user convenience.</li>
</ol>
<p><strong>Below are the formats adopted by default :</strong></p>

<table>
<thead>
<tr>
<th>S. No.</th>
<th>component</th>
<th>Description</th>
<th>Range or Format like</th>
<th align="left">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>hour</td>
<td>extract hour component</td>
<td>00 to 23</td>
<td align="left">00</td>
</tr>
<tr>
<td>2</td>
<td>day</td>
<td>etract day number in the month</td>
<td>01 to 31</td>
<td align="left">1</td>
</tr>
<tr>
<td>3</td>
<td>week</td>
<td>extract week number in the year</td>
<td>01 to 53</td>
<td align="left">40</td>
</tr>
<tr>
<td>4</td>
<td>month</td>
<td>extract month name</td>
<td>January to December</td>
<td align="left">January</td>
</tr>
<tr>
<td>5</td>
<td>quarter</td>
<td>extract quarter number in the year</td>
<td>Q1 to Q4</td>
<td align="left">Q1</td>
</tr>
<tr>
<td>6</td>
<td>Year</td>
<td>extract year component</td>
<td>YYYY</td>
<td align="left">2018</td>
</tr>
</tbody>
</table><p><strong>Additional formats  provided are:</strong></p>

<table>
<thead>
<tr>
<th></th>
<th></th>
<th></th>
<th></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr>
<td>8</td>
<td>Week_day</td>
<td>extract the day component in the week</td>
<td>Sunday to Saturday</td>
<td align="left">Sunday</td>
</tr>
<tr>
<td>9</td>
<td>Date_month</td>
<td>extract date in the respective Month component</td>
<td>YYYY-MM</td>
<td align="left">Wed Jan 31 2018 11:30:00 GMT-0700 (MST)</td>
</tr>
<tr>
<td>10</td>
<td>date_quarter</td>
<td>extract year and respective Quarter component</td>
<td>YYYY-Q1 to YYYY-Q4</td>
<td align="left">2018-Q2</td>
</tr>
<tr>
<td>11</td>
<td>date_hour</td>
<td>extract Date and respective Hour component</td>
<td>YYYY/MM/DD 00 to YYYY/MM/DD 23</td>
<td align="left">2018/02/01 06</td>
</tr>
<tr>
<td>12</td>
<td>year_week</td>
<td>extract  year and respective week component</td>
<td>YYYY-WW to YYYY-WW</td>
<td align="left">2018-15</td>
</tr>
</tbody>
</table><h2 id="user-defined-fieldsudf">User Defined Fields(UDF):</h2>
<p>Bi+ has an ability to create new fields in a view with all attributes that are applicable to a database field and with return value (“sql” section of the field) as any of the following options:</p>
<ol>
<li>As a resultant of arithmetical operations done on fields of the same view.</li>
</ol>
<pre><code>"sql": "(${TABLE}.Field1 arithmetical operation ${TABLE}.Field2)"
</code></pre>
<blockquote>
<p>Example : “sql”: “(${TABLE}.Amount + ${TABLE}.Discount)”</p>
</blockquote>
<ol start="2">
<li>As a resultant of arithmetical operations done on fields of a mapped view.</li>
</ol>
<pre><code>"sql": "(${TABLE}.Field1 arithmetical operation ${Mapped_View.Field})"
</code></pre>
<blockquote>
<p><strong>Example</strong>  “sql”: “(${TABLE}.Amount) / ${Customers.Total_number})”</p>
</blockquote>
<ol start="3">
<li>As a resultant of logical operations(like case statement) done on fields of the same view.</li>
</ol>
<pre><code> "sql": "(case when (condition) then Expression_1 else Expression_2 end) "
</code></pre>
<p>Where condition is an expression on the fields of self view and Expression_1, Expression_2 are expressions which include fields of self view.</p>
<blockquote>
<p><strong>Example</strong>: “sql”: “(CASE WHEN (${TABLE}.Name is not null) THEN ${TABLE}.Salary ELSE 0 END)”</p>
</blockquote>
<ol start="4">
<li>As a resultant of logical operations (like case statement) done on fields of a mapped view.</li>
</ol>
<pre><code> "sql": "(case when (condition) then Expression\_1 else Expression\_2 end) "
</code></pre>
<p>Where condition is an expression can be on the fields of self view or mapped view and Expression_1, Expression_2 are expressions which include fields of self view or mapped view</p>
<blockquote>
<p><strong>Example</strong>  “sql”: “(CASE WHEN (${<a href="http://Customers.ID">Customers.ID</a>} is not null) THEN ${TABLE}.Amount ELSE 0 END)”</p>
</blockquote>
<ol start="5">
<li>As a resultant of database function operated on fields.</li>
</ol>
<pre><code>   "sql": "(${TABLE}.Field * ${DB}.function_name(parameters)) "
</code></pre>
<blockquote>
<p><strong>Example</strong> “sql” : “(${TABLE}.Amount <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mrow><mi>D</mi><mi>B</mi></mrow><mi mathvariant="normal">.</mi><mi>e</mi><mi>x</mi><mi>c</mi><mi>h</mi><mi>a</mi><mi>n</mi><mi>g</mi><msub><mi>e</mi><mi>r</mi></msub><mi>a</mi><mi>t</mi><mi>e</mi><mo>(</mo></mrow><annotation encoding="application/x-tex">{ DB }. exchange_rate(</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.75em;"></span><span class="strut bottom" style="height: 1em; vertical-align: -0.25em;"></span><span class="base"><span class="mord"><span class="mord mathit" style="margin-right: 0.02778em;">D</span><span class="mord mathit" style="margin-right: 0.05017em;">B</span></span><span class="mord mathrm">.</span><span class="mord mathit">e</span><span class="mord mathit">x</span><span class="mord mathit">c</span><span class="mord mathit">h</span><span class="mord mathit">a</span><span class="mord mathit">n</span><span class="mord mathit" style="margin-right: 0.03588em;">g</span><span class="mord"><span class="mord mathit">e</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 0.151392em;"><span class="" style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathit mtight" style="margin-right: 0.02778em;">r</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.15em;"></span></span></span></span></span><span class="mord mathit">a</span><span class="mord mathit">t</span><span class="mord mathit">e</span><span class="mopen">(</span></span></span></span></span>{TABLE}.OrderDate,${TABLE}.CurrencyID))”</p>
</blockquote>
<ol start="6">
<li>As a resultant of string, date, number based sql functions on fields</li>
</ol>
<pre><code>    "sql" : "sql_function(${TABLE}.Field)"
</code></pre>
<blockquote>
<p><strong>Example:</strong> Number  → “sql” : “SUM($  {TABLE}.Amount)”,<br>
Date → “sql”  : "TO_CHAR ( $ { TABLE}.OrderDate,‘Mon-YYYY’)"<br>
String  → “sql”  : “CONCAT('Date : ',${TABLE}.OrderDate)”</p>
</blockquote>
<ol start="7">
<li>As a resultant of single value returning sql query</li>
</ol>
<pre><code>     "sql" : "(select Expression from Database.Table)"
</code></pre>
<p>Where the expression contain the fields of self view and should result a single value.</p>
<blockquote>
<p><strong>Example:</strong> “sql”: "(select sum(x.Amount) from Orders x)”</p>
</blockquote>
<h2 id="drill-down-feature-">Drill-down feature :</h2>
<p>Drilldown is used for exploring the data further with respect to a field value. Bi+ has an ability to define drill option for a field with a set of derivable fields and when clicked on a particular value of an assigned field, the individual records that make up that cell will be displayed by limiting the query with the clicked value.</p>
<h2 id="show_drill_down_measures">Show_drill_down_measures:</h2>
<p>Sometimes, it may be necessary to bring the current stage measure fields to the next drill stage along with the drill fields.</p>
<p>Bi+ provides an additional attribute to drill down as <strong>Show_drill_down_ measures</strong> which  can be defined as <strong>TRUE or FALSE</strong>. If mentioned TRUE, then system will carry forward the measures of the current stage to the immediate drill level.</p>
<pre><code>"drill_down_fields": "Field1,Field2…….."

"show_drill_down_measures": "true / false"
</code></pre>
<blockquote>
<p><strong>Example</strong> Ex: {<br>
“name”: “StateName”,<br>
“label”: “StateName”,<br>
“data_type”: “string”,<br>
“type”: “dimension”,<br>
“lookup”: “”,<br>
“operators”: “”,<br>
“sql”: “${TABLE}.StateName”,<br>
“summary”: “”,<br>
“drill_down_fields”: “CityName,No_of_Employees”,<br>
“show_drill_down_measures”: “true”,<br>
“visualise”: “true”<br>
}</p>
</blockquote>
<p>In the above example, Drill down option is defined over field “State Name” with two fields of self view City Name, No_of_Employees. On Clicking on any of “State Name”, then filter will be applied on that value and relevant values of fields “City Name” and “No_of_Employees” will be displayed.</p>
<p>As <strong>Show_drill_down_measures</strong> is set <strong>TRUE</strong>, the associated measures (if exists) of the field “State Name” will also be brought to the next stage along with drill fields City Name and No_of_Employees.</p>
<h3 id="maps">Maps:</h3>
<p>Bi+ provides map view by covering various number of countries. Also, there are special attributes like colour change for specific range of values. For Model, Views and for a specific field the map co-ordinates may be assigned as follows :</p>
<pre><code>{
"name": "Field",
"label": "Field",
"data_type": "string",
"type": "dimension",
"lookup": "",
"operators": "",
"sql": "${TABLE}.DB\_Column\_Name",
"summary": "",
"visualise": "true",
"country_ref": {
"Field_Value_1": "IND",
"Field_Value_2": "AUS",
………………………….
………………………….
               }
}
</code></pre>
<pre><code>{
			"name": "SC",
			"label": "STATION CODE",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.SC",
			"summary": "",
			"visualise": "true",
			"country_ref": {
				"Station_1": "IND",
				"Station_2": "AUS"
			               }
		}
</code></pre>
<p><strong>The allowed List of country codes are:</strong></p>

<table>
<thead>
<tr>
<th>Country Name</th>
<th>Code</th>
<th></th>
<th>Country Name</th>
<th>Code</th>
<th></th>
<th>Country Name</th>
<th>Code</th>
<th></th>
<th>Country Name</th>
<th>Code</th>
</tr>
</thead>
<tbody>
<tr>
<td>Aruba</td>
<td>ABW</td>
<td></td>
<td>Colombia</td>
<td>COL</td>
<td></td>
<td>Croatia</td>
<td>HRV</td>
<td></td>
<td>Mozambique</td>
<td>MOZ</td>
</tr>
<tr>
<td>Afghanistan</td>
<td>AFG</td>
<td></td>
<td>Comoros</td>
<td>COM</td>
<td></td>
<td>Haiti</td>
<td>HTI</td>
<td></td>
<td>Mauritania</td>
<td>MRT</td>
</tr>
<tr>
<td>Angola</td>
<td>AGO</td>
<td></td>
<td>Cape Verde</td>
<td>CPV</td>
<td></td>
<td>Hungary</td>
<td>HUN</td>
<td></td>
<td>Montserrat</td>
<td>MSR</td>
</tr>
<tr>
<td>Anguilla</td>
<td>AIA</td>
<td></td>
<td>Costa Rica</td>
<td>CRI</td>
<td></td>
<td>Indonesia</td>
<td>IDN</td>
<td></td>
<td>Martinique</td>
<td>MTQ</td>
</tr>
<tr>
<td>Aland Islands</td>
<td>ALA</td>
<td></td>
<td>Cuba</td>
<td>CUB</td>
<td></td>
<td>Isle of Man</td>
<td>IMN</td>
<td></td>
<td>Mauritius</td>
<td>MUS</td>
</tr>
<tr>
<td>Albania</td>
<td>ALB</td>
<td></td>
<td>Christmas Island</td>
<td>CXR</td>
<td></td>
<td>India</td>
<td>IND</td>
<td></td>
<td>Malawi</td>
<td>MWI</td>
</tr>
<tr>
<td>Andorra</td>
<td>AND</td>
<td></td>
<td>Cayman Islands</td>
<td>CYM</td>
<td></td>
<td>British Indian Ocean Territory</td>
<td>IOT</td>
<td></td>
<td>Malaysia</td>
<td>MYS</td>
</tr>
<tr>
<td>Netherlands Antilles</td>
<td>ANT</td>
<td></td>
<td>Cyprus</td>
<td>CYP</td>
<td></td>
<td>Ireland</td>
<td>IRL</td>
<td></td>
<td>Mayotte</td>
<td>MYT</td>
</tr>
<tr>
<td>United Arab Emirates</td>
<td>ARE</td>
<td></td>
<td>Czech Republic</td>
<td>CZE</td>
<td></td>
<td>Iran, Islamic Republic of</td>
<td>IRN</td>
<td></td>
<td>Namibia</td>
<td>NAM</td>
</tr>
<tr>
<td>Argentina</td>
<td>ARG</td>
<td></td>
<td>Germany</td>
<td>DEU</td>
<td></td>
<td>Iraq</td>
<td>IRQ</td>
<td></td>
<td>New Caledonia</td>
<td>NCL</td>
</tr>
<tr>
<td>Armenia</td>
<td>ARM</td>
<td></td>
<td>Djibouti</td>
<td>DJI</td>
<td></td>
<td>Iceland</td>
<td>ISL</td>
<td></td>
<td>Niger</td>
<td>NER</td>
</tr>
<tr>
<td>American Samoa</td>
<td>ASM</td>
<td></td>
<td>Dominica</td>
<td>DMA</td>
<td></td>
<td>Israel</td>
<td>ISR</td>
<td></td>
<td>Norfolk Island</td>
<td>NFK</td>
</tr>
<tr>
<td>Antarctica</td>
<td>ATA</td>
<td></td>
<td>Denmark</td>
<td>DNK</td>
<td></td>
<td>Italy</td>
<td>ITA</td>
<td></td>
<td>Nigeria</td>
<td>NGA</td>
</tr>
<tr>
<td>French Southern Territories</td>
<td>ATF</td>
<td></td>
<td>Dominican Republic</td>
<td>DOM</td>
<td></td>
<td>Jamaica</td>
<td>JAM</td>
<td></td>
<td>Nicaragua</td>
<td>NIC</td>
</tr>
<tr>
<td>Antigua and Barbuda</td>
<td>ATG</td>
<td></td>
<td>Algeria</td>
<td>DZA</td>
<td></td>
<td>Jersey</td>
<td>JEY</td>
<td></td>
<td>Niue</td>
<td>NIU</td>
</tr>
<tr>
<td>Australia</td>
<td>AUS</td>
<td></td>
<td>Ecuador</td>
<td>ECU</td>
<td></td>
<td>Jordan</td>
<td>JOR</td>
<td></td>
<td>Netherlands</td>
<td>NLD</td>
</tr>
<tr>
<td>Austria</td>
<td>AUT</td>
<td></td>
<td>Egypt</td>
<td>EGY</td>
<td></td>
<td>Japan</td>
<td>JPN</td>
<td></td>
<td>Norway</td>
<td>NOR</td>
</tr>
<tr>
<td>Azerbaijan</td>
<td>AZE</td>
<td></td>
<td>Eritrea</td>
<td>ERI</td>
<td></td>
<td>Kazakhstan</td>
<td>KAZ</td>
<td></td>
<td>Nepal</td>
<td>NPL</td>
</tr>
<tr>
<td>Burundi</td>
<td>BDI</td>
<td></td>
<td>Western Sahara</td>
<td>ESH</td>
<td></td>
<td>Kenya</td>
<td>KEN</td>
<td></td>
<td>Nauru</td>
<td>NRU</td>
</tr>
<tr>
<td>Belgium</td>
<td>BEL</td>
<td></td>
<td>Spain</td>
<td>ESP</td>
<td></td>
<td>Kyrgyzstan</td>
<td>KGZ</td>
<td></td>
<td>New Zealand</td>
<td>NZL</td>
</tr>
<tr>
<td>Benin</td>
<td>BEN</td>
<td></td>
<td>Estonia</td>
<td>EST</td>
<td></td>
<td>Cambodia</td>
<td>KHM</td>
<td></td>
<td>Oman</td>
<td>OMN</td>
</tr>
<tr>
<td>Burkina Faso</td>
<td>BFA</td>
<td></td>
<td>Ethiopia</td>
<td>ETH</td>
<td></td>
<td>Kuwait</td>
<td>KWT</td>
<td></td>
<td>Pakistan</td>
<td>PAK</td>
</tr>
<tr>
<td>Bangladesh</td>
<td>BGD</td>
<td></td>
<td>Finland</td>
<td>FIN</td>
<td></td>
<td>Lao PDR</td>
<td>LAO</td>
<td></td>
<td>Panama</td>
<td>PAN</td>
</tr>
<tr>
<td>Bulgaria</td>
<td>BGR</td>
<td></td>
<td>Fiji</td>
<td>FJI</td>
<td></td>
<td>Lebanon</td>
<td>LBN</td>
<td></td>
<td>Pitcairn</td>
<td>PCN</td>
</tr>
<tr>
<td>Bahrain</td>
<td>BHR</td>
<td></td>
<td>Falkland Islands (Malvinas)</td>
<td>FLK</td>
<td></td>
<td>Liberia</td>
<td>LBR</td>
<td></td>
<td>Peru</td>
<td>PER</td>
</tr>
<tr>
<td>Bahamas</td>
<td>BHS</td>
<td></td>
<td>France</td>
<td>FRA</td>
<td></td>
<td>Libya</td>
<td>LBY</td>
<td></td>
<td>Philippines</td>
<td>PHL</td>
</tr>
<tr>
<td>Bosnia and Herzegovina</td>
<td>BIH</td>
<td></td>
<td>Faroe Islands</td>
<td>FRO</td>
<td></td>
<td>Saint Lucia</td>
<td>LCA</td>
<td></td>
<td>Palau</td>
<td>PLW</td>
</tr>
<tr>
<td>Saint-Barthélemy</td>
<td>BLM</td>
<td></td>
<td>Micronesia, Federated States of</td>
<td>FSM</td>
<td></td>
<td>Liechtenstein</td>
<td>LIE</td>
<td></td>
<td>Papua New Guinea</td>
<td>PNG</td>
</tr>
<tr>
<td>Belarus</td>
<td>BLR</td>
<td></td>
<td>Gabon</td>
<td>GAB</td>
<td></td>
<td>Sri Lanka</td>
<td>LKA</td>
<td></td>
<td>Poland</td>
<td>POL</td>
</tr>
<tr>
<td>Belize</td>
<td>BLZ</td>
<td></td>
<td>United Kingdom</td>
<td>GBR</td>
<td></td>
<td>Lesotho</td>
<td>LSO</td>
<td></td>
<td>Puerto Rico</td>
<td>PRI</td>
</tr>
<tr>
<td>Bermuda</td>
<td>BMU</td>
<td></td>
<td>Georgia</td>
<td>GEO</td>
<td></td>
<td>Lithuania</td>
<td>LTU</td>
<td></td>
<td>Korea (North)</td>
<td>PRK</td>
</tr>
<tr>
<td>Bolivia</td>
<td>BOL</td>
<td></td>
<td>Guernsey</td>
<td>GGY</td>
<td></td>
<td>Luxembourg</td>
<td>LUX</td>
<td></td>
<td>Portugal</td>
<td>PRT</td>
</tr>
<tr>
<td>Brazil</td>
<td>BRA</td>
<td></td>
<td>Ghana</td>
<td>GHA</td>
<td></td>
<td>Latvia</td>
<td>LVA</td>
<td></td>
<td>Paraguay</td>
<td>PRY</td>
</tr>
<tr>
<td>Barbados</td>
<td>BRB</td>
<td></td>
<td>Gibraltar</td>
<td>GIB</td>
<td></td>
<td>Macao, SAR China</td>
<td>MAC</td>
<td></td>
<td>Palestinian Territory</td>
<td>PSE</td>
</tr>
<tr>
<td>Brunei Darussalam</td>
<td>BRN</td>
<td></td>
<td>Guinea</td>
<td>GIN</td>
<td></td>
<td>Saint-Martin (French part)</td>
<td>MAF</td>
<td></td>
<td>French Polynesia</td>
<td>PYF</td>
</tr>
<tr>
<td>Bhutan</td>
<td>BTN</td>
<td></td>
<td>Guadeloupe</td>
<td>GLP</td>
<td></td>
<td>Morocco</td>
<td>MAR</td>
<td></td>
<td>Qatar</td>
<td>QAT</td>
</tr>
<tr>
<td>Bouvet Island</td>
<td>BVT</td>
<td></td>
<td>Gambia</td>
<td>GMB</td>
<td></td>
<td>Monaco</td>
<td>MCO</td>
<td></td>
<td>Réunion</td>
<td>REU</td>
</tr>
<tr>
<td>Botswana</td>
<td>BWA</td>
<td></td>
<td>Guinea-Bissau</td>
<td>GNB</td>
<td></td>
<td>Moldova</td>
<td>MDA</td>
<td></td>
<td>Romania</td>
<td>ROU</td>
</tr>
<tr>
<td>Central African Republic</td>
<td>CAF</td>
<td></td>
<td>Equatorial Guinea</td>
<td>GNQ</td>
<td></td>
<td>Madagascar</td>
<td>MDG</td>
<td></td>
<td>Russian Federation</td>
<td>RUS</td>
</tr>
<tr>
<td>Canada</td>
<td>CAN</td>
<td></td>
<td>Greece</td>
<td>GRC</td>
<td></td>
<td>Maldives</td>
<td>MDV</td>
<td></td>
<td>Rwanda</td>
<td>RWA</td>
</tr>
<tr>
<td>Cocos (Keeling) Islands</td>
<td>CCK</td>
<td></td>
<td>Grenada</td>
<td>GRD</td>
<td></td>
<td>Mexico</td>
<td>MEX</td>
<td></td>
<td>Saudi Arabia</td>
<td>SAU</td>
</tr>
<tr>
<td>Switzerland</td>
<td>CHE</td>
<td></td>
<td>Greenland</td>
<td>GRL</td>
<td></td>
<td>Marshall Islands</td>
<td>MHL</td>
<td></td>
<td>Sudan</td>
<td>SDN</td>
</tr>
<tr>
<td>Chile</td>
<td>CHL</td>
<td></td>
<td>Guatemala</td>
<td>GTM</td>
<td></td>
<td>Macedonia, Republic of</td>
<td>MKD</td>
<td></td>
<td>Senegal</td>
<td>SEN</td>
</tr>
<tr>
<td>China</td>
<td>CHN</td>
<td></td>
<td>French Guiana</td>
<td>GUF</td>
<td></td>
<td>Mali</td>
<td>MLI</td>
<td></td>
<td>Singapore</td>
<td>SGP</td>
</tr>
<tr>
<td>Côte d’Ivoire</td>
<td>CIV</td>
<td></td>
<td>Guam</td>
<td>GUM</td>
<td></td>
<td>Malta</td>
<td>MLT</td>
<td></td>
<td>South Georgia and the South Sandwich Islands</td>
<td>SGS</td>
</tr>
<tr>
<td>Cameroon</td>
<td>CMR</td>
<td></td>
<td>Guyana</td>
<td>GUY</td>
<td></td>
<td>Myanmar</td>
<td>MMR</td>
<td></td>
<td>Saint Helena</td>
<td>SHN</td>
</tr>
<tr>
<td>Congo, (Kinshasa)</td>
<td>COD</td>
<td></td>
<td>Hong Kong, SAR China</td>
<td>HKG</td>
<td></td>
<td>Montenegro</td>
<td>MNE</td>
<td></td>
<td>Svalbard and Jan Mayen Islands</td>
<td>SJM</td>
</tr>
<tr>
<td>Congo (Brazzaville)</td>
<td>COG</td>
<td></td>
<td>Heard and Mcdonald Islands</td>
<td>HMD</td>
<td></td>
<td>Mongolia</td>
<td>MNG</td>
<td></td>
<td>Solomon Islands</td>
<td>SLB</td>
</tr>
<tr>
<td>Cook Islands</td>
<td>COK</td>
<td></td>
<td>Honduras</td>
<td>HND</td>
<td></td>
<td>Northern Mariana Islands</td>
<td>MNP</td>
<td></td>
<td>Sierra Leone</td>
<td>SLE</td>
</tr>
</tbody>
</table>
