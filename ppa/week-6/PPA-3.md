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

