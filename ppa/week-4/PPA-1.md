---
title: PPA-1
pagetitle: Week-4, PPA-1
order: 1
---

## Question

Accept a positive integer $n$ as input and print the list of first $n$ positive integers as output.

## Hint

There are two ways of growing a list:

- `append` method
- list concatenation

```python
L = [ ]
L.append(1)
L = L + [2]
print(L)
```

If you want a list of the first $n$ positive integers, then you need to use a loop.

## Solutions

Be careful to initialize `L` as the empty list before you begin populating it.

:::{.panel-tabset}

## Solution-1

```python
n = int(input())
L = [ ]
for x in range(1, n + 1):
    L.append(x)
print(L)
```

## Solution-2

```python
n = int(input())
L = [ ]
for x in range(1, n + 1):
    L = L + [x]
print(L)
```

:::
