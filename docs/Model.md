<center><h1>Model</h1></center>

## Definition

A model is a customized gateway into the database, it is designed in such a way that it provides a spontaneous data analysis to specific business users.model derives the relation between two views , you can apply model based filter globally to restricted data at user level, so each model displays different data to different users.
**Example :** 
if sales manager need different data then material management then we need to develop two models to offer views of database appropriate for each user. 

> Using BI+ you can maintain multiple models for single project and each of them disclose different data to different users depending on parameters applied in model. 

**Getting Started :**
 Once **project** is saved you can define the data in model section as shown in below image :
 ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/5f41bf1e6bf7e11e52fb03d555ce35e47060280b/images/model_new.png)
 
 
## Defining relations. 

```
		{
			"name": "BI_DELIVERYREPORT",
			"label": "BI_DELIVERYREPORT",
			"filters": [],
			"joins": [
				{
					"join": "BI_EMPLOYEES",
					"join_type": "left",
					"join_on": "${BI_DELIVERYREPORT.DELIVERYATTDID} = ${BI_EMPLOYEES.EMPLOYEEID}"
				},
				{
					"join": "BI_CUSTOMERS",
					"join_type": "left",
					"join_on": "${BI_DELIVERYREPORT.CUSTOMERID} = ${BI_CUSTOMERS.CUSTOMERID}"
				}
			        ]
		}

```
- **Name** identifier name to define a model.
- **Label** changes the way that model should appear in the visualization if not by default it uses the name of the model.
- **Filters** optional list of filter expression derived for calculation of the measures.
- **Join** establishes the relationship between visualization and views,here we use 3 types of join parameter join,join_type,join_on.
  - **Join** derive the relationship between 2 views based on the condition.
   - **Join_type** derives type of join condition to apply (Left,Right,inner join).
   - **Join_on** derives the relationship between how to join two tables.
 
##  Model Filters

Filters defined under the model section are applied globally to all the fields.

**Name** identifier name to derive a field.

**Label** parameter helps you to change the title and the way they should appear in field picker.
**Filter_sql** enables the filter application to specified fields and to the query derived.
**Apply** filter applied to **all** the fields or any specific field.
**Position** Applying filter before or after the data retrieval.

```
{
			"name": "BI_ORDERS",
			"label": "BI_ORDERS",
			"filters": [
{
  "name": "AppliedDate",
  "filter_sql": "ROOT.BI_ORDERS.WHENMADE >= TO_DATE('2016-01-01','YYYY-MM-DD HH24:MI:SS') AND ROOT.BI_ORDERS.WHENMADE < TO_DATE('2017-07-01','YYYY-MM-DD HH24:MI:SS')",
  "apply": "all",
  "position": "before"
},
{
  "name": "UserAccessibility",
  "filter_sql": " ROOT.BI_ORDERS.AREACODE IN (#{Model_Stage1.Customer_AreaCode,#userid#,UserName}) AND ROOT.BI_PRODUCTS.MODEL IN (#{Model_Stage1.Products_Model,#userid#,UserName})",
  "apply": "all",
  "position": "before"
},
{
  "name": "RateRange",
  "filter_sql": " ROOT.BI_ORDERS.RATE >= 200 AND ROOT.BI_ORDERS.RATE < 500",
  "apply": "all",
  "position": "after"
}
                      ]
}
  ``` 
  
## Login based Filters

Login based filter enables you to apply user-specific restrictions. To carry out this you need to be associated with global parameter under settings section in BI+ to work efficiently.
```
bi.in_global_keys( ["UserName","Login_name"],[${ROOT.EMPLOYEES.NAME_661} 
,bi._globals("#userid#")],"CalcCol_Stage2.SeizeLimit
```
## Derived Table

Derived tables enables you to refine your data analysis more precisely. it creates a new temporary table that doesn't exist in your database already, they either be built at your query time or they can be stored in your database. These can be defined by writing a SQL query and results as derived table.
```
{
	"name": "derivedtable",
	"label": "derivedtable",
	"info": "Description",
	"type": "query",
	"sql": "(SELECT
ROOT.BI_ORDERS.STATIONCODE AS "STATIONCODE_655",
to_char(ROOT.BI_ORDERS.WHENMADE,'HH24') AS "hour_WHENMADE"
FROM ROOT.BI_ORDERS "BI_ORDERS"
LEFT JOIN ROOT.BI_EMPLOYEES "BI_EMPLOYEES" ON (BI_ORDERS.ORDERATTDID = BI_EMPLOYEES.EMPLOYEEID)
LEFT JOIN ROOT.BI_PRODUCTS "BI_PRODUCTS" ON (BI_ORDERS.PRODUCTID = BI_PRODUCTS.PRODUCTID)
LEFT JOIN ROOT.BI_CUSTOMERS "BI_CUSTOMERS" ON (BI_ORDERS.CUSTOMERID = BI_CUSTOMERS.CUSTOMERID))",
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
			"sql": "\"${table}.stationcode,
			"summary": "",
			"visualise": "true",
			"country_ref": {
				"Station_1": "IND",
				"Station_2": "AUS"
			               }
	    },
	{
			"name": "WHENMADE",
			"label": "WHENMADE",
			"data_type": "date",
			"time_frame": "hour,day,week,month,quarter,year,date,week_day,date_month,date_quarter,date_hour,year_week",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "${TABLE}.WHENMADE",
			"summary": "",
			"visualise": "true"
	}
			   ]
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4OTEyODNdfQ==
-->