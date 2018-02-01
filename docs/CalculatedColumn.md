Calculation is a statement or expression or a function operator which can be used to derive the column values, lets get deep into calculated column function.

## Usage of #math# 

Custom made mathematical operations.

### Syntax for using math functionality :

```
Check the number of working days in each month:

#math#
bi.days_in_month
(${ROOT.BI_ORDERS.date_month_WHENMADE}) 
```
```
To calculate the cubical value of the field

#math#
bi.cube(${ROOT.BI_ORDERS.count_AMOUNT})
```
**Similarly we can use all the below functionality Using Bi+:**


|   |  |  |
|  ------ | ------ | ------ |
|  **Name** | **Description** | **Example** |
|  date_to_week | Returns the number of current day week in the year | date_to_week(Give reference to month_date)   |
|  date_to_quarter | Returns the Quarter number for current date or the month parameter given inside () | date_to_quarter-> it returns quarter number like Q1,Q2,Q3,Q4 |
|  date_to_year | Returns the Year value for current date or the month parameter given inside () | date_to_year("2017-10-22")   it returns  only  year = 2017 |
|  date_to_month | Returns the Month Number for current date or the month parameter given inside () | date_to_month("2017-10-23")--> it returns month number = 10 |
|  date_format | Returns the required format of a date parameter mentioned after it & inside () | date_format(To_date,'YYYY-MM-DD') |
|  date_diff | Returns the number of days between two dates given inside () | date_diff("2017-10-20" to "2017-10-23") = 3 |
|  days_in_month | Returns the total number of days completed in the present month including today | days_in_month (january) = 31 |
ry) = 31 |
|  days_till_month | Returns the total number of days completed in the present month including today | days _till_month(october) = 23 it shows  how many days completed in given month |

## Usage of #math#plugin# for Grid View

            welcome to Biplus


## Arithmetic & Logical operations on Data Fields

            welcome to Biplus


## Usage of Global Functions with paramerts from Data Fields

            welcome to Biplus


## Usage of Global Parameters with reference from Data Field values

            welcome to Biplus


## Usage of Global Parameters with reference from Data Field values & Login Control

            welcome to Biplus


## Calculate on Raw functionality

            welcome to Biplus
 

## Calc column with Pivot Option On /Off

            welcome to Biplus

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3ODM1Nzc2ODJdfQ==
-->