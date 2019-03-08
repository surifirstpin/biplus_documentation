<center><h1>Timeline Filters</h1></center>

## Date 
|  **Example** | **Description** |
|  :------: | :------: |
|  today | from zero hour of today to current point of time |
|  this second | curren point of time |
|  this minute | from zero seconds of current minute to the current point of time |
|  this hour | from zero seconds of current hour to the current point of time |
|  this week | from zero hour of current week start date to current point of time |
|  this month | from zero hour of current month start date to current point of time |
|  this quarter | from zero hour of current quarter start date to current point of time |
|  this year | from zero hour of current year start date to current point of time |
|  **full** |  |
|  today full | from zero hour to last hour of today (if data exists) |
|  this full minute | from zero seconds of current minute to the 60th second(if data exists) |
|  this full hour | from zero minute, zero seconds of current hour to the 60th minute, 60th second(if data exists) |
|  this full week | from zero hour of current week start date to last hour of last day in the week(if data exists) |
|  this full month | from zero hour of current month start date to last hour of last day in the month(if data exists) |
|  this full quarter | from zero hour of current quarter start date to last hour of last day in the quarter(if data exists) |
|  this full year | from zero hour of current year start date to last hour of last day in the year(if data exists) |

## NOT

|  **Example** | **Description** |
|  ------ | ------ |
|  not today | all the data excluding data from zero hour to last hour of current day(if data exists) |
|  not this hour | all the data excluding data from zero second to 60th second of current hour (if data exists) |
|  not this week | all the data excluding data from zero hour of the start date to the last hour of the last date in the current week(if data exists) |
|  not this month | all the data excluding data from zero hour of the start date to the last hour of the last date in the current month(if data exists) |
|  not this quarter | all the data excluding data from zero hour of the start date to the last hour of the last date in the current quarter(if data exists) |
|  not this year | all the data excluding data from zero hour of the start date to the last hour of the last date in the current year(if data exists) |

## Last

|  **Example** | **Description** |
|  ------ | ------ |
|  last second | data of last second |
|  last minute | from the zero second to the 60th second in the last minute with reference to current point of time |
|  last hour | from the zero second, zero minute to the 60th second, 60th minute in the immediate previous hour with reference to current point of time |
|  Yesterday | from the zero hour to the last hour of yesterday with reference to current point of time |
|  last week | from the zero hour of the start date to the last hour of the last date in the immediate previous week with reference to current point of time |
|  last month | from the zero hour of the start date to the last hour of the last date in the immediate previous month with reference to current point of time |
|  last quarter | from the zero hour of the start date to the last hour of the last date in the immediate previous quarter with reference to current point of time |
|  last year | from the zero hour of the start date to the last hour of the last date in the immediate previous year with reference to current point of time |

## Next
|  **Example** | **Description** |
|  ------ | ------ |
|  next second | data of next second (if data exists) |
|  next minute | from the zero second to the 60th second in the next minute with reference to current point of time (if data exists) |
|  next hour | from the zero second, zero minute to the 60th second, 60th minute in the immediate hour with reference to current point of time (if data exists) |
|  tomorrow | from the zero hour to the last hour of tomorrow with reference to current point of time (if data exists) |
|  next week | from the zero hour of the start date to the last hour of the last date in the immediate week with reference to current point of time (if data exists) |
|  next month | from the zero hour of the start date to the last hour of the last date in the immediate month with reference to current point of time (if data exists) |
|  next quarter | from the zero hour of the start date to the last hour of the last date in the immediate quarter with reference to current point of time (if data exists) |
|  next year | from the zero hour of the start date to the last hour of the last date in the immediate year with reference to current point of time (if data exists) |
## Last & n
|  **Example** | **Description** |
|  ------ | ------ |
|  last n seconds | data from exactly ‘n’ seconds before the current point of time and up to current point of time |
|  last n minutes | data from exactly ‘n’ minutes before the current point of time and up to current point of time<br/>(minute resembles 60 seconds) |
|  last n hours | data from  exactly ‘n’ hours before the current point of time and up to current point of time<br/>(hour resembles 60 minutes) |
|  last n days | data from exactly ‘n’ days before the current point of time and up to current point of time<br/>(day resembles 24 hours not the zeroth hour to last hour) |
|  last n weeks | data from exactly ‘n’ weeks before the current point of time and up to current point of time<br/>(week here resembles 7 days and not from start date of a week to end date of week) |
|  last n month | data from exactly ‘n’ months before the current point of time and up to current point of time<br/>(month here resembles 30 days and not from start date of a month to end date of month) |
|  last n quarters | data from exactly ‘n’ quarters before the current point of time and up to current point of time<br/>(quarter here resembles 90 days and not from start date of a quarter to end date of quarter) |
|  last n years | data from exactly ‘n’ years before the current point of time and up to current point of time<br/>(year here resembles 365 days and not from start date of a year to end date of year) |
## last – n – full

|  **Example** | **Description** |
|  ------ | ------ |
|  last n full minutes | data belongs to the last n completed minutes with reference to the current point of time |
|  last n full hours | data belongs to the last n completed hours with reference to the current point of time |
|  last n full days | data belongs to the last n completed days with reference to the current point of time |
|  last n full weeks | data belongs to the last n completed weeks with reference to the current point of time<br/>(week resembles start date of week to last date of week) |
|  last n full months | data belongs to the last n completed months with reference to the current point of time<br/>(month resembles start date of month to last date of month) |
|  last n full quarters | data belongs to the last n completed quarters with reference to the current point of time<br/>(quarter resembles start date to the last date of te quarter) |
|  last n full years | data belongs to the last n completed years with reference to the current point of time<br/>(year resembles start date to the last date of the year) |
## next & ‘n’
|  **Example** | **Description** |
|  ------ | ------ |
|  next n seconds | data from current point of time to exactly coming ‘n’ seconds |
|  next n minutes | data from current point of time to exactly coming ‘n’ minutes<br/>(minute resembles 60 seconds) |
|  next n hours | data from current point of time to exactly coming ‘n’ hours<br/>(hour resembles to 60 minutes) |
|  next n days | data from current point of time to exactly coming ‘n’ days <br/>(day resembles 24 hours not from zeroth hour to last hour) |
|  next n weeks | data from current point of time to exactly ‘n’ coming weeks<br/>(week here resembles 7 days and not from start date of a week to end date of week) |
|  next n months | data from current point of time to exactly coming ‘n’ months <br/>(month here resembles 30 days and not from start date of a month to end date of month) |
|  next n quarters | data from current point of time to exactly coming ‘n’ quarters <br/>(quarter here resembles 90 days and not from start date of a quarter to end date of quarter) |
|  next n Years | data from current point of time to exactly coming ‘n’ years <br/>(year here resembles 365 days and not from start date of a year to end date of year) |

## next – n – full
|  **Example** | **Description** |
|  ------ | ------ |
|  next n full minutes | data belongs to the next n completed minutes with reference to the current point of time (if data exists) |
|  next n full hours | data belongs to the next n completed hours with reference to the current point of time (if data exists) |
|  next n full days | data belongs to the next n completed days with reference to the current point of time (if data exists) |
|  next n full weeks | data belongs to the next n completed weeks with reference to the current point of time (if data exists)<br/>(week resembles start date of week to next date of week) |
|  next n full months | data belongs to the next n completed months with reference to the current point of time (if data exists)<br/>(month resembles start date of month to next date of month) |
|  next n full quarters | data belongs to the next n completed quarters with reference to the current point of time (if data exists)<br/>(quarter resembles start date to the next date of te quarter) |
|  next n full years | data belongs to the next n completed years with reference to the current point of time (if data exists)<br/>(year resembles start date to the next date of the year) |

## Ago
|  **Example** | **Description** |
|  ------ | ------ |
|  n days ago for m days | data from exactly ‘n’ days before the current point of time to the next ‘m’ successive days<br/>(day resembles 24 hours not the zeroth hour to last hour) |

## ago & full

|  **Example** | **Description** |
|  ------ | ------ |
|  n full days ago for m days | data from exactly ‘n’ completed days before the current point of time to the next ‘m’ successive days<br/>(day resembles 24 hours not the zeroth hour to last hour) |
|  n full days ago for m full days | data from exactly ‘n’ completed days before the current point of time to the next ‘m’ successive completed days<br/>(day resembles 24 hours not the zeroth hour to last hour) |

## After

|  **Example** | **Description** |
|  ------ | ------ |
|  n days after for m days | data excluding ‘n’ coming days with respect to the current point of time and then for ‘m’ successive days (if data exists)<br/>(day resembles 24 hours not the zeroth hour to last hour) |

## after & full
|  **Example** | **Description** |
|  ------ | ------ |
|  n full days after m day | data excluding coming ‘n’ completed days with respect to the current point of time and then for ‘m’ successive days (if data exists)<br/>(day resembles 24 hours not the zeroth hour to last hour) |
|  n full days after m full day | data excluding coming ‘n’ completed days with respect to the current point of time and then for ‘m’ successive completed days (if data exists)<br/>(day resembles 24 hours not the zeroth hour to last hour) |
## before & ‘n’
|  **Example** | **Description** |
|  ------ | ------ |
|  before n seconds | data from the beginning to exactly ‘n’ seconds before the current point of time |
|  before n minutes | data from the beginning to exactly ‘n’ minutes before the current point of time |
|  before n hours | data from the beginning to exactly ‘n’ hours before the current point of time |
|  beofre n days | data from the beginning to exactly ‘n’ days before the current point of time |
|  before n weeks | data from the beginning to exactly ‘n’ weeks before the current point of time<br/>(week here resembles 7 days and not from start date of a week to end date of week) |
|  before n months | data from the beginning to exactly ‘n’ month before the current point of time<br/>(month here resembles 30 days and not from start date of a month to end date of month) |
|  before n quarters | data from the beginning to exactly ‘n’ quarter before the current point of time <br/>(quarter here resembles 90 days and not from start date of a quarter to end date of quarter) |
|  befroe n years | data from the beginning to exactly ‘n’ years before the current point of time<br/>(year here resembles 365 days and not from start date of a year to end date of year) |

## before – n – full
|  **Example** | **Description** |
|  ------ | ------ |
|  before n full seconds | data from beginning to exactly  ‘n’ completed seconds before the current point of time |
|  before n full minutes | data from beginning to exactly  ‘n’ completed minutes before the current point of time |
|  before n full hours | data from beginning to exactly  ‘n’ completed hours before the current point of time |
|  before n full days | data from beginning to exactly  ‘n’ completed days before the current point of time |
|  before n full weeks | data from beginning to exactly  ‘n’ completed Weeks before the current point of time (excludes current week)<br/>(week here resembles time between start date of the week to last date of the week) |
|  beforen full months | data from beginning to exactly  ‘n’ completed months before the current point of time (excludes current month)<br/>(week here resembles time between start date of the month to last date of the month) |
|  before n full quarters | data from beginning to exactly  ‘n’ completed quarters before the current point of time (excludes current quarter)<br/>(week here resembles time between start date of the quarter to last date of the quarter) |
|  before n full years | data from beginning to exactly  ‘n’ completed year before the current point of time (excludes current year)<br/>(week here resembles time between start date of the year to last date of the year)|

## after & ‘n’
|  **Example** | **Description** |
|  ------ | ------ |
|  after n seconds | data from exactly ‘n’ seconds after the current point of time to the last available record |
|  after n minutes | data from exactly ‘n’ minutes after the current point of time to the last available record |
|  after n hours | data from exactly ‘n’ hours after the current point of time to the last available record |
|  aftter n days | data from exactly ‘n’ days after the current point of time to the last available record |
|  after n weeks | data from exactly ‘n’ weeks after the current point of time to the last available record<br/>(week here resembles 7 days and not from start date of a week to end date of week) |
|  after n months | data from exactly ‘n’ months after the current point of time to the last available record<br/>(month here resembles 30 days and not from start date of a month to end date of month) |
|  after n quarters | data from exactly ‘n’ quarter after the current point of time to the last available record<br/>(quarter here resembles 90 days and not from start date of a quarter to end date of quarter) |
|  after n years | data from exactly ‘n’ years after the current point of time to the last available record<br/>(year here resembles 365 days and not from start date of a year to end date of year) |

## after – n – full

|  **Example** | **Description** |
|  ------ | ------ |
| after n full seconds | data from exactly ‘n’ completed seconds after the current point of time to the last available record |
|  after n full minutes | data from exactly ‘n’ completed minutes after the current point of time to the last available record |
|  after n full hours | data from exactly ‘n’ completed hours after the current point of time to the last available record |
|  after n full days | data from exactly ‘n’ completed days after the current point of time to the last available record (excludes today) |
|  after n full weeks | data from exactly ‘n’ completed weeks after the current point of time to the last available record <br/>(excluded the current week and week here resembles 7 days and not from start date of a week to end date of week) |
|  after n full months | data from exactly ‘n’ completed months after the current point of time to the last available record<br/>(excluded the current month and month here resembles 30 days and not from start date of a month to end date of month) |
|  after n full quarters | data from exactly ‘n’ completed quarter after the current point of time to the last available record<br/>(excluded the current quarter and quarter here resembles 90 days and not from start date of a quarter to end date of quarter) |
|  after n full years | data from exactly ‘n’ completed years after the current point of time to the last available record<br/>(excluded the currentyear and year here resembles 365 days and not from start date of a year to end date of year) |

## over series

|  **Example** | **Description** |
|  ------ | ------ |
|  doy | data belongs to exactly current day in the all the available years (gives future data if exists) |
|  dom | data belongs to exactly current day in the all the available months (gives future data if exists) |
|  doq | data belongs to exactly current day(that is current day number in the present quarter) in the all the available quarters (gives future data if exists) |
|  dow | data belongs to exactly current day(that is current day number in the present week) in the all the available week (gives future data if exists) |
|  woy | data belongs to exactly current week(that is current week number in the present year) in the all the available years (gives future data if exists) |
|  wom | data belongs to exactly current week(that is current week number in the present month) in the all the available months (gives future data if exists) |
|  woq | data belongs to exactly current week(that is current week number in the present quarter) in the all the available months (gives future data if exists) |
|  moy | data belongs to exactly current month(that is current month number in the present year) in the all the available years (gives future data if exists) |
|  moq | data belongs to exactly current month(that is current month number in the present quarter) in the all the available quarters (gives future data if exists) |
|  qoy | data belongs to exactly current quarter(that is current quarter number in the present year) in the all the available years (gives future data if exists) |

## over & ‘n’ series

|  **Example** | **Description** |
|  ------ | ------ |
|  doy n | data belongs to exactly ‘n’th day after the current day in all the available years (gives future data if exists) |
|  dom n | data belongs to exactly ‘n’th day after the current day in all the availbale months (gives future data if exists) |
|  doq n | data belongs to exactly ‘n’th day after the current day(that is current day number in quarter) in all the availbale quarters (gives future data if exists) |
|  dow n | data belongs to exactly ‘n’th day after the current day(that is current day number in week) in all the availbale weeks (gives future data if exists) |
|  woy n | data belongs to exactly ‘n’th week after the current week(that is current week number in year) in all the availbale years (gives future data if exists) |
|  wom n | data belongs to exactly ‘n’th week after the current week(that is current week number in month) in all the availbale months (gives future data if exists) |
|  woq n | data belongs to exactly ‘n’th week after the current week(that is current week number in quarter) in all the availbale quarters (gives future data if exists) |
|  moy n | data belongs to exactly ‘n’th months after the current month(that is current month number in year) in all the availbale years (gives future data if exists) |
|  moq n | data belongs to exactly ‘n’th month after the current month(that is current month number in quarter) in all the availbale quarters (gives future data if exists) |
|  qoy n | data belongs to exactly ‘n’th quarter after the current quarter(that is current quarter number in year) in all the availbale years (gives future data if exists) |

## over & ‘-n’ series
|  **Example** | **Description** |
|  ------ | ------ |
|  doy -n | data belongs to exactly ‘n’th day before the current day in all the available years (gives future data if exists) |
|  dom -n | data belongs to exactly ‘n’th day before the current day in all the availbale months (gives future data if exists) |
|  doq -n | data belongs to exactly ‘n’th day before the current day(that is current day number in quarter) in all the availbale quarters (gives future data if exists) |
|  dow -n | data belongs to exactly ‘n’th day before the current day(that is current day number in week) in all the availbale weeks (gives future data if exists) |
|  woy -n | data belongs to exactly ‘n’th week before the current week(that is current week number in year) in all the availbale years (gives future data if exists) |
|  wom -n | data belongs to exactly ‘n’th week before the current week(that is current week number in month) in all the availbale months (gives future data if exists) |
|  woq -n | data belongs to exactly ‘n’th week before the current week(that is current week number in quarter) in all the availbale quarters (gives future data if exists) |
|  moy -n | data belongs to exactly ‘n’th months before the current month(that is current month number in year) in all the availbale years (gives future data if exists) |
|  moq -n | data belongs to exactly ‘n’th months before the current month(that is current month number in quarter) in all the availbale quarters (gives future data if exists) |
|  qoy -n | data belongs to exactly ‘n’th quarter before the current quarter(that is current quarter number in year) in all the availbale years (gives future data if exists) |

## over & to date series
|  **Example** | **Description** |
|  ------ | ------ |
|  Doy  to date | All the available data in every year from start date of the year to the current date of the year |
|  dom to date | All the available data in every month from start date of the month to the current day number of the month |
|  doq to date | All the available data in every quarter from start date of the quarter to the current day number in the quarter |
|  dow to date | All the available data in every week from start date of the week to the current day name in the week |
|  woy to date | All the available data in every year from first day of the year  to the current week |
|  wom to date | All the available data in every month from first day of the month to the current week |
|  woq to date | All the available data in every quarter from first day of the quarter to the current numbered week |
|  moy to date | All the available data in every year from first day of the year  to the current numbered month |
|  moq  to date | All the available data in every quarter from first day of the quarter to the current numbered month |
|  qoy to date | All the available data in every quarter from first day of the year to the current numbered quarter |

## over - ‘n’ - to date series
|  **Example** | **Description** |
|  ------ | ------ |
|  doy n to date | In Every Year from 1st to till tomorrow |
|  dom n to date | In Every Year In Every Month from 1st to till tomorrow |
|  doq n to date | in Every quarter from 1st to till tomorrow  |
|  dow n to date | in Every week from 1st to till tomarrow  |
|  woy n to date | In Every Year from 1st to till next week |
|  wom n to date | In Every Month from 1st to till next week |
|  woq n to date | in Every quarter from 1st week to till next week |
|  moy n to date | In  every Year from 1st month to till next month |
|  moq n to date | In Every Quarter from 1st month to till next month |
|  qoy n to date | In Every Year from 1st quarter to till next quarter |

## over - ‘-n’ - to date series
|  **Example** | **Description** |
|  ------ | ------ |
|  Doy -n to date | Every Year of  Starting date to  Previous day  |
|  dom  -n to date | Every month of Starting date Previous day |
|  doq -n to date | Every Quarter of  Starting date to Previous day |
|  dow -n to date | Every Week of  Starting date to Previous day |
|  woy -n to date | Every year of  Starting week to  Previous week |
|  wom -n to date | Every month of Starting week tovPrevious week |
|  woq -n to date | Every quarter of starting week to Previous week |
|  moy -n to date | Every year of  Starting month to Previous month |
|  moq -n to date | Every quarter of Starting month to Previous month |
|  qoy -n to date | Every year of  Previous quarter |

## in series
|  **Example** | **Description** |
|  ------ | ------ |
|  day in year n | Every year of  first day  |
|  day in month n | Every  month of first day  |
|  day in quarter n | Every quarter of first day |
|  day in week n | Every week of first  day |
|  week in year n | Every year of first week |
|  week in month n  | Every month of first week |
|  week in quarter n | Every quarter of first week |
|  month in year n  | Every year of first month  |
|  month in quarter n | Every quarter of first month  |
|  quarter in year n  | Every year of first quarter |

## in & to date series
|  **Example** | **Description** |
|  ------ | ------ |
|  day in year n to date | Every year of  first day to  nth day |
|  day in month n to dtae | Every  month of first day to nth day |
|  day in quarter n to date | Every quarter of first day to nth day |
|  day in week n to date | Every week of first  day to nth day |
|  week in year n to date | Every year of first week to nth week |
|  week in month n to date | Every month of first week to nth week |
|  week in quarter n to date | Every quarter of first week to nth week |
|  month in year n to date | Every year of first month  to nth month |
|  month in quarter n to date | Every quarter of first month  to nth month |
|  quarter in year n to date | Every year of first quarter to nth month |

## Regular Filters
|  **Example** | **Description** |
|  ------ | ------ |
|  Date (equal) | From Zero hour to last hour of the selected date through calendar |
|  Date (notequal) | All the Data excluding the values from zero hour to last hour of the selected date through calender |
|  Date (between) | From Zero hour of the first selected date to the last hour of the second selected date |
|  Date (Not between) | From Zero hour of the first selected date to the last hour of the second selected date |
|  Date (less or equal) | All the data before the zero hour of the selected date |
|  WhenMadedate(greater or equal) | All the data after the last hour of the selected date |
|  WhenMadedate(Is Not Null) | Data where date field is not Null |
|  WhenMadedate(Is Null) | Data where date field is Null |
|  WhenMade(date_month)(Is Not Null) | Data where date_month field (month number in the year) is not Null |
|  WhenMade(date_month)(Is Null) | Data where date_month field (month number in the year) is Null |
|  WhenMade(date_quarter)(Is Not Null) | Data where date_quarter field (quarter number in the year) is not Null |
|  WhenMade(date_quarter)(Is Null) | Data where date_quarter field (quarter number in the year) is  Null |
|  WhenMade(year_week)(Is Not Null) | Data where year_week field (week number in the year) is not Null |
|  WhenMade(year_week)(Is Null) | Data where year_week field (week number in the year) is Null |
|  WhenMade(date_hour)(Is Not Null) | Data where date_hour field (hour number in the year) is not Null |
|  WhenMade(date_hour)(Is Null) | Data where date_hour field (hour number in the year) is Null |
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUxMDQ1NzgwMiw1MzE2NDYzNjMsMzIzNT
YwMjY1XX0=
-->