## Custom Fields

Custom fields are user defined fields for which we apply Arithmetic  and logical operations that are supported by database.
A view may join other views and there relationship are defined as part of data analysis section of model file..

**Derive custom view**

**1.** Click on **New Empty view** button to create or derive a new custom view table.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3b50165c4cf02e474b87d097aa2f8b0897fae1ae/images/custom_table.png)
   
**2.** Once the view is created label the database field and derive the custom table using a SQL query as a result a derived table is created.

``` 
{
"name": "CustomView_820",
	"label": "CustomView_820",
	"info": "Description",
	"type": "query",
	"sql": "(SELECT A.STATIONCODE SC,A.ORDERID ORID,A.WHENMADE ORTIME,B.NAME RECEPNAME, A.AMOUNT ORDVAL,A.QUANTITY QTY,A.WAYUSED ORDBY, A.PAYMENTMODE PM,C.NAME CUSTNAME,C.ADDRESS CUSTADDR FROM ROOT.ORDERS A INNER JOIN ROOT.EMPLOYEES B ON A.ORDERATTDID=B.EMPLOYEEID INNER JOIN ROOT.CUSTOMERS C ON A.CUSTOMERID=C.CUSTOMERID)",
	"database": "ROOT",
	"connection": "Oracle_Build",
"fields": [
		{
			"name": "SC",
			"label": "STATION CODE",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "\"CustomView_791\".SC",
			"summary": "",
			"visualise": "true",
			"country_ref": {
				"Station_1": "IND",
				"Station_2": "AUS"
			}
		},
		{
			"name": "ORID",
			"label": "ORDERSCOUNT",
			"data_type": "number",
			"type": "measure",
			"lookup": "",
			"operators": "",
			"sql": "COUNT(DISTINCT \"CustomView_820\".ORID)",
			"summary": "",
			"visualise": "true"
		},
		]
	}
```
- **Name** name identifier of custom table derived.

- **label** the custom table.

- **Info** provides description for custom table.

- **Type** datatype used for deriving a custom table.

- **Database** table is used to retrieve the data fields.

- **Connection** establish the database connection for deriving new fields.


##  Arithmetical operations in Custom Fields

```
{
			"name": "SC_SUBSTR",
			"label": "SC_SUBSTR",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "SUBSTR(${TABLE}.STATIONCODE,1,4)",
			"summary": "",
			"visualise": "true"
		},
		{
			"name": "SC_SUBSTR1",
			"label": "SC_SUBSTR1",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "SUBSTR(${TABLE}.STATIONCODE,5,7)",
			"summary": "",
			"visualise": "true"
		},
		{
			"name": "SC_CONCAT",
			"label": "SC_CONCAT",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "CONCAT(SUBSTR(${TABLE}.STATIONCODE,1,4),SUBSTR(${TABLE}.STATIONCODE,5,7))",
			"summary": "",
			"visualise": "true"
		},
```	

- **Name** Name identifier  of the field in custom table.

- **label** title the way you want the derived field to appear in custom table.

- **Data_type** define supporting parameters and string is used as  Default parameter while deriving the fields for custom table.
    - **String** for measures that contain letters or special characters.
   
  - **Date** measures that contain dates.
  
  - **Time_frame** is a derived list of formats from time stamps for instance the following are the available formats hour, day, week,month,quarter, year,date,week_day, date_month , date_quarter, date_hour, year_week.
 
  - **Number** for the measure that contain number.
 
  - **Int** for the measure that contains integers.
  
 - **Type** can be used as part of dimension or measure.

## Lookups

- **lookup** retrieve list of values for a specific field either from database using a query or from an item list (it is listed in the filter section during visualization).

- **Operator** is used to retrieve single or multiple values in the filter section while using lookup.

 - **SQL** parameter is used define a valid SQL expression that results in a field value.

 - **Summary** is used to retrieve the aggregate field values of the measures using the following options,
   - Sum 
   - count
   - Average 
   - maximum
   -  minimum

## Drill-down feature and specs

**Drill_down_fields** parameter is used to explore the data within the field. it works in query results tables and dashboards. Drilling disclose a new query that is restricted by the value you clicked on.
 **Show_drill_down_measure** parameter is used to retrieve the data from multiple levels by assigning the true or false condition to the parameter.

**Drill has different actions for dimensions and measures:**
- When **drilling on a dimension,** the new query filters on the drilled value. For example, if you click on country name it will show the SName assigned to the country.
```

		{
			"name": "COUNTRYNAME",
			"label": "COUNTRYNAME",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.COUNTRYNAME",
			"summary": "",
			"drill_down_fields": "STATENAME",
			"show_drill_down_measures": "true",
			"visualise": "true"
		},
		{
			"name": "STATENAME",
			"label": "STATENAME",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.STATENAME",
			"summary": "",
			"visualise": "true"
		},
```
- When **drilling on a measure,** the new query will show the data set that contributed to the measure. For example,  when drilling on a Revenue Account it shows the bonus-points.

```
{
			"name": "REVENUE_AMOUNT",
			"label": "REVENUE_AMOUNT",
			"data_type": "number",
			"type": "measure",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.REVENUE_AMOUNT",
			"summary": "sum,avg,max,min,count",
			"drill_down_fields": "BONUSPOINTS",
			"show_drill_down_measures": "true",
			"visualise": "true"
		},
		{
			"name": "BONUSPOINTS",
			"label": "BONUSPOINTS",
			"data_type": "number",
			"type": "measure",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.BONUSPOINTS",
			"summary": "sum,avg,max,min,count",
			"visualise": "true"
		}
		
``` 

## Field Visibility On / Off

**Visualize** parameter is used as display on-off option of the field in visualization section by assigning true or false condition to the parameter.

## Adding Currency & Format to a field

 **Number_format** it specifies different set of number formats used for the field values.

**Currency** is applied to retrieve the values in specified currency applicable.
 
### Syntax for defining fields in custom table :
```
"fields": [
		{
			"name": "CUSTNAME",
			"label": "CUSTOMER NAME",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "\"CustomView_820\".CUSTNAME",
			"summary": "",
			"drill_down_fields": "SC,ORID",
			"visualise": "true"
]
}
```    

## Defining map coordinates

## Login based Lookups

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM4MjQyOTY5OV19
-->