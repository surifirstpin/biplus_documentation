<center><h1>Views</h1></center>


Custom fields are user defined fields for which we apply arithmetic  and logical operations that are supported by database.
A view may join other views and there relationship are defined as part of data analysis section of model file.

## Creating a view

**1.** Click on **New Empty view** to create or derive a new custom view table.

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3b50165c4cf02e474b87d097aa2f8b0897fae1ae/images/custom_table.png)
   
**2.** Once the view is created, label the database field and derive the custom table using a SQL query as a result a derived table is created.
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
- **label** label the custom table the way it should appear in model section. 
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

- **Name** identifier for the field in custom table.
- **label**  the way derived field should appear in custom table.
- **Data_type** define supporting parameters and string is used as  default parameter while deriving the fields for custom table.
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
   - Count
   - Average 
   - Maximum
   - Minimum

## Drill-down features 

**Drill_down_fields** parameter is used to explore the data within the field. it should be enabled in model for a particular field. 
 **Show_drill_down_measure** parameter is used to carryout the measure data in the current level to the immediate drill level.
 
**Drill has different actions for dimensions and measures:**

- When **drilling on a dimension,** the new query filters on the drilled value. For example, if you click on **COUNTRY NAME** it will show the **STATE NAME** assigned to the country.
> drill down should be specified in field properties with the following syntax
```
{
			
			"drill_down_fields": "Level1_drillfields",
			"show_drill_down_measures": "true",
			"visualise": "true"
			},

```
- When **drilling on a measure,** the new query will show the data set that contributed to the measure. For example,  when drilling on a **REVENUE_AMOUNT** it shows the **BONUS POINTS** assigned to it.
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
- **Visualize** parameter is used as, display on-off option for fields in data analyse section by assigning true or false condition to the parameter.


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTU2MDMwMTA3NV19
-->