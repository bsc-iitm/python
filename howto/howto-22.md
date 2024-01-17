---
title: Extract the sublist that does not contain the first and last elements
pagetitle: How-to
sidebar: false

---

::: {.panel-tabset}

## Method-1

```python
L = [1, 2, 3, 4, 5, 6, 7, 8]
sub_L = L[1:-1]
print(sub_L)
```

## Method-2

```python
L = [1, 2, 3, 4, 5, 6, 7, 8]
n = len(L)
sub_L = L[1:n - 1]
print(sub_L)
```

:::
