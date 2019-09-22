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
