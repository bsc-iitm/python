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

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/53b4c8ef589c4d148992210c9c85c93d?sid=05d20cd1-05a4-4b2f-8e94-a3aa854878b2" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
