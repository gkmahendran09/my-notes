## Sorting

```
ls = [3, 2, 1]
ls = 'python'

sorted(ls) # Ascending

sorted(ls, reverse=True) # Decending

```

## Convert datetime to time_stamp

```
def convert_datetime_to_time_stamp(from_datetime):
    ts = (from_datetime - datetime.date(1970, 1, 1)).total_seconds() 
    return ts
```

```
from_datetime = datetime.date(2017, 6, 30)
convert_datetime_to_time_stamp(from_datetime)
```

## Make API Call
`pip install requests`

`import requests`

```
def fetch_data(url, payload):
    result = requests.get(url, params=payload).json()
    
    return result
```


## Ternary Operator

`[on_true] if [expression] else [on_false]`

`a if a < b else b`


## Get first/last day of the previous month

```
from datetime import date
from dateutil.relativedelta import relativedelta
today = date.today()
d = today - relativedelta(months=1)

date(d.year, d.month, 1)
>>> datetime.date(2008, 12, 1)

date(today.year, today.month, 1) - relativedelta(days=1)
>>> datetime.date(2008, 12, 31)
```


## String to Date Time Object

```
import datetime

date_time_str = '2018-06-29 08:15:27.243860'
date_time_obj = datetime.datetime.strptime(date_time_str, '%Y-%m-%d %H:%M:%S.%f')

print('Date:', date_time_obj.date())
print('Time:', date_time_obj.time())
print('Date-time:', date_time_obj)
```

## strftime() - datetime object to string

```
from datetime import datetime
# current date and time
now = datetime.now()
s1 = now.strftime("%m/%d/%Y, %H:%M:%S")
# mm/dd/YY H:M:S format
```
