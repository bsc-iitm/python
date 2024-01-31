---
title: PPA-8
pagetitle: Week-3, PPA-8
order: 8
---

## Question

Accept a positive integer $n$ as input and print the first $n$ integers on a line separated by a comma.



## Hint

Consider the following piece of code:

```python
n = int(input())

for x in range(1, n + 1):
    print(x, end = ',')
```

For an input of $5$, this ends up printing `1,2,3,4,5,` and the last comma is undesirable. How do we get rid of it? You can use an `if-else` block:

- If `x == n`, which is the last number you are printing, then just `print(x)`.
- If `x != n`, which is any other number in the sequence, then `print(x, end = ',')`

You have enough information to complete the code.



## Solution

:::{.panel-tabset}

## Solution-1

```python
n = int(input())

for x in range(1, n + 1):
    if x != n:
        print(x, end = ',')
    else:
        print(x)
```

## Solution-2

Here we stop short of the last number and print it outside the loop.

```python
n = int(input())

for x in range(1, n):
    print(x, end = ',')
print(n)
```

:::
