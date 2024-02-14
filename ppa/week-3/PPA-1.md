---
title: PPA-1
pagetitle: Week-3, PPA-1
order: 1
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



## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/16200504943643148b73a5ef8521f7c2?sid=4ef97866-97d1-46ee-a408-d639d182ad3b" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>