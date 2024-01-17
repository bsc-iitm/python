---
title: PPA-1
pagetitle: Week-3, PPA-1
---

## Question

Accept a positive integer $n$ as input and print the first $n$ positive integers, one number on each line.



## Hint

Which loop should we use here, `while` or `for`?

If we go with a `for` loop, is the following solution correct?

```python
n = int(input())
for x in range(n):
    print(x)
```

If it is not correct, then what is the mistake?



## Solutions

:::{.panel-tabset}

## Solution-1

```python
n = int(input())
k = 1
while k <= n:
    print(k)
    k += 1
```

## Solution-2

```python
n = int(input())
for x in range(1, n + 1):
    print(x)
```

:::