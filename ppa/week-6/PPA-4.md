---
title: PPA-4
pagetitle: Week-6, PPA-4
order: 4
---

## Question

Write a function named `value_to_keys` that accepts a dictionary `D` and a variable named `value` as arguments. It should return the list of all keys in the dictionary that have value equal to `value`. If the `value` is not present in the dictionary, the function should return the empty list.

<hr>
- You do not have to accept input from the user or print the output to the console. You just have to write the definition of the function.
- The keys inside the list could be in any order.

## Hint

<u>Approach-1</u>

Iterate over the keys:

```python
for key in D:
    pass
```

<u>Approach-2</u>

Iterate over the key-value pairs

```python
for key, value in D.items():
    pass
```

This should be sufficient for you to complete the code.

## Solutions

::: {.panel-tabset}

## Solution-1

```python
def value_to_keys(D, value):
    keys = [ ]
    for key in D:
        if D[key] == value:
            keys.append(key)
    return keys
```

## Solution-2

```python
def value_to_keys(D, value):
    keys = [ ]
    for key, val in D.items():
        if val == value:
            keys.append(key)
    return keys
```

:::
