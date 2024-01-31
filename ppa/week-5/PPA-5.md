---
title: PPA-5
pagetitle: Week-5, PPA-5
order: 5
---

## Question

Write a function named **`first_three`** that accepts a list `L` of distinct integers as argument. It should return the first maximum, second maximum and third maximum in the list, in this order. You can assume that the input list will have a size of at least three. What concept in CT does this remind you of?

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

This function returns three different values at the same time. Let us first take up a simpler example that involves two return values

```python
def floor_ceil(x):
    '''x is a positive real number'''
    if x == int(x):
        floor = ceil = int(x)
    else:
        floor = int(x)
        ceil = floor + 1
    return floor, ceil
```

Let us call the function with some value, say `floor(4.3)` and see what happens:

```python
a = floor_ceil(4.3)
print(a)
```

It prints the output `(4, 5)`. This is called a tuple (refer to week-6). A tuple is very much like a list. So, when multiple values are simultaneously returned in a single return statement, what is being returned is a tuple. But, let us not worry too much about that. What is more useful is the following:

```python
a, b = floor_ceil(4.3)
print(a)
print(b)
```

Since the function returns two values, we have two variables — `a, b` — on the LHS of the assignment statement in line-1.

Check out the code below that finds out the first two maximums. Try to extend it to three maximums.

```python
def first_two(L):
    fmax, smax = L[0], L[1]
    
    for x in L:
        if x > fmax:
            smax = fmax
            fmax = x
        elif x > smax and x < fmax:
            smax = x
    
    return fmax, smax
```

## Solutions

We have used the fact that the elements of the list are distinct in the solution. Can you identify where it is being used? Even before that, why do you think this restriction has been imposed? 

::: {.panel-tabset}

## Solution-1

```python
def first_three(L):
    fmax, smax, tmax = L[0], L[1], L[2]
    for x in L:
        if x > fmax:
            tmax = smax
            smax = fmax
            fmax = x
        elif x > smax and x < fmax:
            tmax = smax
            smax = x
        elif x > tmax and x < smax:
            tmax = x
    return fmax, smax, tmax
```

## Solution-2

```python
def first_three(L):
    fmax, smax, tmax = L[0], L[1], L[2]
    for x in L:
        if x > fmax:
            tmax = smax
            smax = fmax
            fmax = x
        elif smax < x < fmax:
            tmax = smax
            smax = x
        elif tmax < x < smax:
            tmax = x
    return fmax, smax, tmax
```

:::
