
 Once we save the created project the data is reflected in model screen as shown in below image:
 
![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/49e5251756b8ccdaf049b25596aab34272f82085/images/project_final_model.png)

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
  ``` 


## Login based Filters

           welcome to biplus

## Custom Query

BI+ helps you yo create your own set of derived custom table that doesn’t already exist in your database.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQ0NTYyMTU5NF19
-->