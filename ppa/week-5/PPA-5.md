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

Coming back to this problem, consider the following snippet of code and see if you can extend it into a solution:

```python
fmax = max(L)
L.remove(fmax)
```

## Solutions

Refer to this [FAQ](https://docs.python.org/3/faq/programming.html#why-did-changing-list-y-also-change-list-x){target=_blank} to understand some of the finer points regarding lists and functions in the context of this problem. Read this FAQ and then look at solutions (1) and (2).

::: {.panel-tabset}

## Solution-1

```python
def first_three(L):
    fmax = max(L)
    L.remove(fmax)
    smax = max(L)
    L.remove(smax)
    tmax = max(L)
    return fmax, smax, tmax
```

In this solution we are modifying the list. For example if this code snippet is run:

```python
P = [6, 7, 1, 5, 4, 3, 2]
print(first_three(P))
print(P)
```

the output will be:

```
(7, 6, 5)
[1, 5, 4, 3, 2]
```

Notice that the list `P` has been modified in this process. If this is to be avoided, refer to solution-2.

## Solution-2

```python
def first_three(L):
    L_local = L.copy()
    fmax = max(L_local)
    L_local.remove(fmax)
    smax = max(L_local)
    L_local.remove(smax)
    tmax = max(L_local)
    return fmax, smax, tmax
```

Now, if we run this snippet:

```python
P = [6, 7, 1, 5, 4, 3, 2]
print(first_three(P))
print(P)
```

we get the output:

```
(7, 6, 5)
[6, 7, 1, 5, 4, 3, 2]
```

Note that `P` has not been disturbed. We achieved this by making sure that a copy of `L` was created in line-2.

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/59d1ae5341664dd8a0014e3a1cd3053e?sid=26fcca95-10c7-4e7d-b05f-e456514cfa17" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
