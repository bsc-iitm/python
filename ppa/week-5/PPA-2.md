---
title: PPA-2
pagetitle: Week-5, PPA-2
order: 2
---

## Question

In the Gregorian calendar, a leap year has a total of $366$ days instead of the usual $365$ as a result of adding an extra day (February $29$) to the year. This calendar was introduced in $1582$ to replace the flawed Julian calendar. The criteria given below are used to determine if a year is a leap year or not.

- If a year is divisible by $100$ then it will be a leap year if it is also divisible by $400$.
- If a year is not divisible by $100$, then it will be a leap year if it is divisible by $4$.

<hr>

Write a function named **`check_leap_year`** that accepts a year between $1600$ and $9999$ as argument. It should return `True` if the year is a leap year and `False` otherwise.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

Assume that the year is not a leap year to begin with. Now use a binary variable, say `leap`, that is set to `False` to begin with. Next, use a bunch of `if-else` statements to update the value of `leap`. Finally, return `leap`. Just to make sure that you understand the conditions, are the following leap years?

- $1900$
- $2024$
- $2000$

## Solution

```python
def check_leap_year(year):
    leap = False
    if year % 100 == 0:
        if year % 400 == 0:
            leap = True
    else:
        if year % 4 == 0:
            leap = True
    return leap
```

