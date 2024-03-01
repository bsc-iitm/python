---
title: PPA-8
pagetitle: Week-6, PPA-8
order: 8
---

## Question

Write the following functions:

- **`factors`**: accept a positive integer $n$ as argument. Return the set of all factors of $n$.
- **`common_factors`**: accept two positive integers $a$ and $b$ as arguments. Return the set of common factors of the two numbers. This function must make use of `factors`.
- **`factors_upto`**: accept a positive integer $n$ as argument. Return a dict `D`, whose keys are integers and values are sets. Each integer in the range $[1, n]$, endpoints inclusive, is a key of `D`. The value corresponding to a `key`, is the set of all factors of `key`. This function must use of `factors`.

The idea we are trying to bring out here is to make use of pre-defined functions whenever needed.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the definition of all three functions. Each test case will correspond to one function call.

## Solution

Note that the method to add an element to a set is `add` and not `append`.

**`factors`**

```python
def factors(n):
    fact = set()
    for f in range(1, n + 1):
        if n % f == 0:
            fact.add(f)
    return fact
```

**`common_factors`**

::: {.panel-tabset}

## Method-1

```python
def common_factors(a, b):
    return factors(a).intersection(factors(b))
```

## Method-2

```python
def common_factors(a, b):
    return factors(a) & factors(b)
```

:::

If `A` and `B` are two Pythonic sets, then their intersection is given by `A.intersection(B)`. Alternatively, we can use `A & B`. Mathematically, this would return $A \cap B$.

**`factors_upto`**

```python
def factors_upto(n):
    D = dict()
    for x in range(1, n + 1):
        D[x] = factors(x)
    return D
```

