---
title: PPA-6
pagetitle: Week-1, PPA-6
---

## Question

Accept the registration number of a vehicle as input and print its state-code as output. Sample registration numbers:

- `TN-10-AB-2010`
- `HR-15-XZ-1999`

The template for registration numbers will be the same.



## Hint

Slice the string. Where to start the slice and where to end it? This is something you have to figure out after looking at the test-cases.



## Solutions

::: {.panel-tabset}

## Solution-1

```python
regno = input()
code = regno[0:2]
print(code)
```

## Solution-2

```python
regno = input()
code = regno[:2]
print(code)
```

:::
