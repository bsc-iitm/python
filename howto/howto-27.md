---
title: Reverse a list of numbers
pagetitle: How-to
sidebar: false
order: 14
categories:
  - List
---

::: {.panel-tabset}

## Method-1

This is the most straightforward snippet that reverses a list in-place.

```python
L = [1, 2, 3, 4, 5]
L.reverse()
print(L)
```

## Method-2

```python
L = [1, 2, 3, 4, 5]
rev = [ ]
for x in L:
    rev = [x] + rev
print(rev)
```

## Method-3

Here we are using the step-size parameter. By starting with the last element of the list, we go back all the way till the beginning of the list, in steps of $-1$. We leave the middle index unspecified so that it goes back all the way till the beginning.

```python
L = [1, 2, 3, 4, 5]
n = len(L)
rev = L[n-1::-1]
print(rev)
```

## Method-4

We can leave the first index also unspecified.

```python
L = [1, 2, 3, 4, 5]
rev = L[::-1]
print(rev)
```

:::

