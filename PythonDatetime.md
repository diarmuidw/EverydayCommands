### Some simple bits of Python code to manipulate dates

~~~
# The imports
from datetime import date, datetime, timedelta
~~~


~~~
# The basics!
today = date.today()
yesterday = today  - timedelta(days=1)

#Today as a string
tds = today.strftime("%d/%m/%Y") 
tds = today.strftime("%Y\%m\%d") # A differnet format
filename = today.strftime("Some-file-%Y%m%d.txt")


~~~
