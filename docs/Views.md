## Defining new Fileds in a View (Custom Fields)
Using BI+ you create your own set of derived custom table that doesn’t already exist in your database.
   ![enter image description here](https://raw.githubusercontent.com/sv18042016/fp1/3b50165c4cf02e474b87d097aa2f8b0897fae1ae/images/custom_table.png)
   
**1.** Click on New Empty view button to create a derive a new custom view table.
**2.** Once the view is created label the database field and derive the custom table using a SQL query as a result a derived table is created.

#### List of parameters used while defining a custom table :

## Labelling a Database Field

- **Name** of the custom table derived
- **label** the custom table
- **Info** provides description for custom table
- **Type** datatype used for deriving a custom table
- **Database** table is used to retrieve the data fields
- **Connection** establish the database connection for deriving new fields.

### Syntax for deriving custom table :

``` 
{
"name": "CustomView_820",
	"label": "CustomView_820",
	"info": "Description",
	"type": "query",
	"sql": "(SELECT A.STATIONCODE SC,A.ORDERID ORID,A.WHENMADE ORTIME,B.NAME RECEPNAME, A.AMOUNT ORDVAL,A.QUANTITY QTY,A.WAYUSED ORDBY, A.PAYMENTMODE PM,C.NAME CUSTNAME,C.ADDRESS CUSTADDR FROM ROOT.ORDERS A INNER JOIN ROOT.EMPLOYEES B ON A.ORDERATTDID=B.EMPLOYEEID INNER JOIN ROOT.CUSTOMERS C ON A.CUSTOMERID=C.CUSTOMERID)",
	"database": "ROOT",
	"connection": "Oracle_Build",
}
```
## Lookup and Operators ( Query & Items)

                 welcome to biplus

## Login based Lookups

                 welcome to biplus

## Usage of functions, logical & arithmetical operations in Custom Fields

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
#### Syntax for defining fields in custom table :
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
## Summary ( aggregates as sum, min, max, avg, count)

                 welcome to biplus

## Adding Currency & Format to a field

                 welcome to biplus

## Defining map coordinates

                 welcome to biplus

## Drilldown featuer and specs

                 welcome to biplus

## Field Visibility On / Off

                 welcome to biplus

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc5MDUyODYzXX0=
-->