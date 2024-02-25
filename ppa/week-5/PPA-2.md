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

## Solutions

::: {.panel-tabset}

## Solution-1

```python
def check_leap_year(year):
    if year % 100 == 0:
        if year % 400 == 0:
            return True
        return False
    else:
        if year % 4 == 0:
            return True
       	return False
```

## Solution-2

```python
def check_leap_year(year):
	if (year % 100 == 0) and (year % 400 == 0):
        return True
    elif (year % 100 != 0) and (year % 4 == 0):
        return True
    return False
```

## Solution-3

```python
def check_leap_year(year):
    if year % 100 == 0:
        return year % 400 == 0
    else:
        return year % 4 == 0
```

## Solution-4

This uses just one return statement at the end of the function.

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

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/ad6d9590769a44bfb28aa7603b0ac786?sid=0c768bd4-42cd-4141-9d39-f01929d9ad41" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

