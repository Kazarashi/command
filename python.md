## Python

高速for文
```
[list[index]] for index in range(0, len(list))
```

三项运算
* too long version:
```
if flag==True:
    a=0
else:
    a=-1
```

* short version:
```
a = 0 if flag is True else 1
```

find key in json:
```
if 'key' in json:
    pass
else:
    pass
```

str -> json:
```
import json
json_data = json.dumps(str)
```

json -> dict:
```
import json
dict = json.loads(json_data)
```

unicode -> str:
```
str = unicode.encode('utf-8')
```

str -> unicode:
```
unicode = str.decode('utf-8')
```

多值传送:
```
def data_format ():
    return ((count=0, name='abc'))
count, name = data_format()
print(count) => 0
print(name) => abc
```

random string:
```
import random
# length is the str's length
str = ''.join([random.choice('abcdefgABCDEFG123456') for i in range (length)])
```

random number:
```
import random
t = random.randrange(1, 10)
```

datetime -> timestamp:
```
import datetime
import time
now_time = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
time_array = time.strptime(now_time, "%Y-%m-%d %H:%M:%S")
time_stamp = int(time.mktime(time_array))
```

timestamp -> datetime:
```
import datetime
get_time = datetime.datetime.strptime(time_stamp, "%Y-%m-%dT%H:%M:%S.%fZ").strftime("%Y-%m-%d %H:%M:%S")
```
