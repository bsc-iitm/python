---
title: Iterate through the elements in a list
pagetitle: How-to
sidebar: false
order: 5
categories:
  - List
---

:::{.panel-tabset}

## Method-1

This is more Pythonic.

```python
L = ['this', 'is', 'a', 'list']
for word in L:
    print(word)
```

## Method-2

This is less Pythonic.

```python
L = ['this', 'is', 'a', 'list']
n = len(L)
for i in range(n):
    print(L[i])
```

:::