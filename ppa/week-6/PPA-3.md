---
title: PPA-3
pagetitle: Week-6, PPA-3
order: 3
---

## Question

Write the following functions:

- `is_key`: accept a dictionary `D` and a variable `key` as arguments. Return `True` if the variable key is a key of the dictionary `D`, and `False` otherwise.
- `value`: accept a dictionary `D` and a variable `key` as arguments. If the variable `key` is not a key of the dictionary `D`, return `None`, otherwise, return the value corresponding to this key.

<hr>

You do not have to accept input from the user or print the output to the console. You just have to write the definition of both the functions.

## Hint

`key in D` evaluates to `True` if `key` is one of the keys and `False` otherwise.

## Solution

```python
def is_key(D, key):
    return key in D

def value(D, key):
    if key not in D:
        return None
    return D[key]
```

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/1b9715d38f1440d1806ae05690103727?sid=c298eb56-acc2-4009-8e74-aeab96d3bb2d" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
