
 Once project is saved you can derive your data in model section as shown in below image:
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

- **Name** of the database table.

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
		
**1.** Click on **Save** button.

## Model Filters

Model filters helps you to extract the relevant information based on the applied filter options.

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

           welcome to biplus

## Custom Query

Using BI+ you create your own set of derived custom table that doesn’t already exist in your database.
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/master/images/custom_table.png)**1.** Click on New Empty view button to create a derive a new custom view table.
**2.** Once the view is created label the database field and derive the custom table using a SQL query as a result a derived table is created.

#### List of parameters used while defining a custom table :

- **Name** of the custom table derived
- **label** the custom table
- **Info** provides description for custom table
- **Type** datatype used for deriving a custom table
- **Database** table is used to retrieve the data fields
- **Connection** establish the database connection for deriving new fields.

### Syntax for deriving custom table:

``` 
{
"name": "CustomView_791",
	"label": "CustomView_791",
	"info": "Description",
	"type": "query",
	"sql": "(SELECT A.STATIONCODE SC,A.ORDERID ORID,A.WHENMADE ORTIME,B.NAME RECEPNAME, A.AMOUNT ORDVAL,A.QUANTITY QTY,A.WAYUSED ORDBY, A.PAYMENTMODE PM,C.NAME CUSTNAME,C.ADDRESS CUSTADDR FROM ROOT.ORDERS A INNER JOIN ROOT.EMPLOYEES B ON A.ORDERATTDID=B.EMPLOYEEID INNER JOIN ROOT.CUSTOMERS C ON A.CUSTOMERID=C.CUSTOMERID)",
	"database": "ROOT",
	"connection": "Oracle_Build",
}
```
#### Below are the list of function and parameters used while defining a fields under table :

- **Name** of the field.
- **label** the derived field.
- **Data_type** have supporting parameters and string is used as  Default parameter while deriving the fields for custom table.
list of supporting parameters used while defining the custom fields:

   - **String** for measures that contain letters or special characters.
  - **Date** measures that contain dates.
  - **Time_frame** is a derived list of formats from time stamps for instance the following are the available formats hour, day, week,month,quarter, year,date,week_day, date_month , date_quarter, date_hour, year_week.
  - **Number** for the measure that contain number.
  - **Int** for the measure that contains integers.
- **Type** can be used as part of dimension or measure.
- **lookup** retrieves a list of values for a specific field either from database using a query or from an item list (it is listed in the filter section during visualization).
- **Operator** is used to retrieve single or multiple values in the filter section while using lookup.
- **SQL** parameter is used define a valid SQL expression that results in a field value.
- **Summary** is used to retrieve the aggregate field values of the measures using the following options Sum,count,average, maximum, minimum.
- **Drill_down_fields** parameter is used to explore the data within the field.
- **Show_drill_down_measure** parameter is used to retrieve the data from multiple levels by assigning he true or false condition to the parameter.
- **Visualize** parameter is used as display on-off option of the field in visualization section by assigning true or false condition to the parameter.
- **Number_format** it specifies different set of number formats used for the field values.
- **Currency** is applied to retrieve the values in specified currency applicable.
#### Syntax for defining fields in custom table:
```
"fields": [
		{
			"name": "CUSTNAME",
			"label": "CUSTOMER NAME",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "\"CustomView_791\".CUSTNAME",
			"summary": "",
			"drill_down_fields": "SC,ORID",
			"visualise": "true"
]
}
```
**3.** Click on save** button to save the custom table view.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg5MTA3NzgwXX0=
-->