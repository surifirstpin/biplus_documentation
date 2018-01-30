
A model is a customized gateway into the database, it is designed in such a way that it provides a spontaneous data analysis to specific business users.
Using BI+ you can maintain multiple models for single project and each of them disclose different data to different users depending on parameters applied in model. 

 Once project is saved you can define your data in model section as shown in below image :
 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/ca01fdfd9787082af897b153cb9bb2e74a97c099/images/model_new.png)
 
## Defining new relations. 

Model defines explore and their relationship with other view it is derived using below parameters.

- **Project** used for the model.
- **Connection** database connection used for the model.

### Syntax for defining model parameters:
```
{
	"project": "Oracle_test2",
	"info": "Project Info",
	"connections": [
		"Oracle_Build",
                   ]
}
``` 
## mappings

### Mapping Parameters used in the model:

- **Name** identifier name to define a model.

- **Label** changes the way that model should appear in the visualization if not by default it uses the name of the model.

- **Filters** is optional list of filter expression derived for calculation of the measures.

- **Join** establishes the relationship between visualization and views,here we use 3 types of join parameter join,join_type,join_on.

  - **Join** derive the relationship between 2 views based on the condition.
  
  - **Join_type** derives type of join to apply (Left,Right,inner join).
  
  - **Join_on** derives the relationship between how to join two tables.
  
  ### Syntax for join parameters defined :
  
  ```
  {
			"name": "BI_DELIVERYREPORT",
			"label": "BI_DELIVERYREPORT",
			"filters": [],
			"joins": [
				{
					"join": "BI_CUSTOMERS",
					"join_type": "left",
					"join_on": "${BI_DELIVERYREPORT.CUSTOMERID} = ${BI_CUSTOMERS.CUSTOMERID}"
				}
			            ]
},
		```
		
## Model Filters

Filters defined under the model section are applied by default to all the fields.

### List of Parameters used in model filters :
**Name** identifier name to derive  
**Label** parameter helps you to change the title and the way they should appear in field picker.

**Filter_sql** enables the filter application to specified fields and to the query derived.

**Apply** filter applied to **all** the fields or any specific field.

**Position** apply filter before or after the data retreive.

### Syntax for model based filter
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

![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/05f4f8072b85b8252c162bcf0d494351bd30b232/images/login_based_filters.png)

### Syntax for login based filters:
```
#math#
bi.in_global_keys( ["UserName","Login_name"],[${ROOT.EMPLOYEES.NAME_661} 
,bi._globals("#userid#")],"CalcCol_Stage2.SeizeLimit

```
## Derived Table

Derived tables enables you to refine your data analysis more precisely. it creates a new temporary table that doesn't exist in your database already, they either be built at your query time or they can be stored in your database. These can be defined by writing a SQL query and results as derived table.

### Syntax for derived tables :

```select
ROOT.ORDERS.STATIONCODE AS STATIONCODE,
ROOT.ORDERS.WHENMADE AS WHENMADE,ROOT.ORDERS.ORDERID AS ORDERID,
SUM(ROOT.ORDERS.AMOUNT) AS sum_amount
FROM ROOT.ORDERS
where (ROOT.ORDERS.WHENMADE >= TRUNC(SYSDATE) AND ROOT.ORDERS.WHENMADE < SYSDATE)
Group by (ROOT.ORDERS.STATIONCODE),(ROOT.ORDERS.WHENMADE),(ROOT.ORDERS.ORDERID)

Select orderid,to_char(WHENMADE,'YYYY-MM-DD') AS WHENMADE_DATE,AMOUNT FROM ROOT.ORDERS WHERE 
(ROOT.ORDERS.WHENMADE > = TRUNC(SYSDATE) AND ROOT.ORDERS.WHENMADE < SYSDATE)
``` 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYxODUxNDI2NF19
-->