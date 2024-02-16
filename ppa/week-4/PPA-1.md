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

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/aead52a3aa3a4605b07158bd902c7798?sid=04f90e09-4e24-4d15-998f-f4e19a5c2d93" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
