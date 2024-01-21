---
title: Find the maximum element in a list
pagetitle: How-to
sidebar: false
order: 12
categories:
  - List
---

::: {.panel-tabset}

## Method-1

```python
L = [10, -4, 40, 30, 14]
max_elem = max(L)
print(max_elem)
```

## Method-2

This approaches the problem from first principles.

```python
L = [10, -4, 40, 30, 14]
max_elem = L[0]
for x in L:
    if x > max_elem:
        max_elem = x
print(max_elem)
```

:::
