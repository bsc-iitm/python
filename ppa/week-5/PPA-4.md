---
title: PPA-4
pagetitle: Week-5, PPA-4
order: 4
---

## Question

Write a function named **`dim_equal`** that accepts two matrices `A` and `B` as arguments. It should return `True` if the dimensions of both matrices are the same and `False` otherwise.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

Consider the following solution to this problem:

```python
def dim_equal(A, B):
    dim_A = len(A)
    dim_B = len(B)
    return dim_A == dim_B
```

Do you think this solution is correct? Does it pass all the test cases? What is it missing? For what inputs will it fail?

## Solution

::: {.panel-tabset}

## Solution-1

```python
def dim_equal(A, B):
    m_A, n_A = len(A), len(A[0])
    m_B, n_B = len(B), len(B[0])
    if (m_A == m_B) and (n_A == n_B):
        return True
   	return False
```

## Solution-2

```python
def dim_equal(A, B):
    if ((len(A) == len(B)) and 
        (len(A[0]) == len(B[0]))):
        return True
    return False
```

## Solution-3

```python
def dim_equal(A, B):
    return ((len(A) == len(B)) and
            (len(A[0]) == len(B[0])))
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/22248c9d5d1d45289b17af0b71982e10?sid=c9925368-3d4c-4c25-8c76-43145c88b393" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>