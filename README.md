# to-read-today-s-date-only-date-Part-from-user

import datetime

now = datetime.datetime.now()
td = 0

print("Today's day:", now.day)

# Determine total days in the current month
if now.month == 2:
    # Check for leap year
    if (now.year % 4 == 0 and now.year % 100 != 0) or (now.year % 400 == 0):
        td = 29
    else:
        td = 28
elif now.month in (1,3,5,7,8,10,12):
    td = 31
else:
    td = 30

print("Total remaining days in the current month are:", td - now.day)

OUTPUT :

Today's day: 18
Total remaining days in the current month are: 11
