---
title: PPA-10
pagetitle: Week-2, PPA-10
order: 10
---

## Question

Accept a real number $x$ as input and print the greatest integer less than or equal to $x$ on the first line, followed by the smallest integer greater than or equal to $x$ on the second line.



## Hint

The crux of this problem is to look at three cases, two of which are given below:

- What happens when $x$ is positive? 
- What happens when $x$ is negative? 

Here is another hint:

```python
f = int(3.3)
print(f)
```

`int(3.3)` retains the integer part while truncating whatever comes after the decimal, including the decimal point. Try out the following:

```python
f = int(-3.3)
print(f)
```

Can you now go ahead and construct a solution for this problem? These are the [floor and ceiling functions](https://en.wikipedia.org/wiki/Floor_and_ceiling_functions){target=_blank} that we study in mathematics. Why do you think these functions have been named in this manner?



## Solution

```python
x = float(input())

if x == int(x):
    floor = ceil = int(x)
elif x > 0:
    floor = int(x)
    ceil = floor + 1
elif x < 0:
    ceil = int(x)
    floor = ceil - 1

print(floor)
print(ceil)
```

