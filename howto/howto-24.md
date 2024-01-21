---
title: Sort a list of numbers in ascending order
pagetitle: How-to
sidebar: false
order: 13
categories:
  - List
---

::: {.panel-tabset}

## Method-1

This is the simplest method. `sort` is a method of the list object. It sorts the list "in-place". That is, it doesn't create a new list in the process of sorting, but sorts the existing list itself. This method is to be avoided if you don't want to disturb the original list.

```python
L = [10, -4, 40, 30, 14, 5, -1, -4]
L.sort()
print(L)
```

## Method-2

This method sorts the list but creates a new list in the process. The original list is not distrubed.

```python
L = [10, -4, 40, 30, 14, 5, -1, -4]
sorted_L = sorted(L)
print(sorted_L)
```

## Method-3

This uses the algorithm mentioned in the course.

```python
L = [10, -4, 40, 30, 14, 5, -1, -4]
sorted_L = [ ]
while L != [ ]:
    smallest = min(L)
    L.remove(smallest)
    sorted_L.append(smallest)
print(sorted_L)
```

:::
