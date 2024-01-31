---
title: PPA-9
pagetitle: Week-3, PPA-9
order: 9
---

## Question

Accept a positive integer $n$ as input and print a triangle of zeros for $n$ lines. The $i^{th}$ line should have $i$ zeros. There shouldn't be any spaces between consecutive zeros. Do not print a space at the end of a line.



## Hint

A nested loop is one way to solve the problem. What should be the ranges for the outer and inner `for` loops? How many rows are we printing? In each row, how many zeros are we printing? To move to the next row, just use `print()`.

There is a way to solve the problem using a single loop. A hint is given below:

- string
- integer
- multiplication

How can you use a combination of the three terms mentioned here to construct a solution?



## Solutions

::: {.panel-tabset}

## Solution-1

```python
n = int(input())
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print('0', end = '')
    print()
```

## Solution-2

```python
n = int(input())
for i in range(1, n + 1):
    print('0' * i)
```

:::
