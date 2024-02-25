---
title: PPA-5
pagetitle: Week-6, PPA-5
order: 5
---

## Question

Write the following functions:

- `dict_to_list`: accept a dictionary `D` as argument. Return the key-value pairs in `D` as a list `L` of tuples. That is, every element of `L` should be of the form `(key, value)` such that `D[key] = value`. Going the other way, every key-value pair in the dictionary should be present as a tuple in the list `L`.
- `list_to_dict`: accept a list of tuples `L` as argument. Each element of `L` is of the form `(x, y)`. Return a dict `D` such that each tuple `(x, y)` corresponds to a key-value pair in `D`. That is, `D[x] = y`.

<hr>

- For the function `dict_to_list`, the order in which the key-value pairs are appended to the list doesn't matter.
- For the function `list_to_dict`, you can assume that if `(x1, y1)` and `(x2, y2)` are two different elements in `L`, `x1 != x2`. Why is this assumption important?
- You do not have to accept input from the user or print the output to the console. You just have to write the definition of both the functions.

## Hint

- For the function `dict_to_list`, execute `list(D.items())` and observe what you get.
- For the function `list_to_dict`, execute `dict(L)` and observe what you get.

## Solutions

Refer to this [document](https://docs.python.org/3/tutorial/datastructures.html#dictionaries){target=_blank} and this [document](https://docs.python.org/3/library/stdtypes.html#dictionary-view-objects){target=_blank} for more details regarding some aspects of dictionaries.

::: {.panel-tabset}

## Solution-1

```python
def dict_to_list(D):
    L = [ ]
    for key, value in D.items():
        L.append((key, value))
    return L

def list_to_dict(L):
    D = dict()
    for key, value in L:
        D[key] = value
    return D
```

## Solution-2

```python
def dict_to_list(D):
    return list(D.items())

def list_to_dict(L):
    return dict(L)
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/71dd33ea29494cb6a7d13bc0a73f4f98?sid=1d670138-a551-45b0-8601-202de44cc1d9" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
