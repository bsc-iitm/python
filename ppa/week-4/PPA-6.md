---
title: PPA-6
pagetitle: Week-4, PPA-6
---

## Question

Accept a sequence of comma-separated words as input. Reverse the sequence and print it as output.



## Hint

<u>Approach-1</u>

Consider the following sequence of operations on a list `L = [1, 2, 3, 4, 5]`. Think about this list as a train having five compartments. Reversing is the process of rearranging the compartments by moving the last compartment of the current train to the end of a new train. To begin with, this new train will have no compartments.

<u>Step-0</u>

```python
[1, 2, 3, 4, 5]

[ ]
```

<u>Step-1</u>

```python
[1, 2, 3, 4]

[5]
```

<u>Step-2</u>

```python
[1, 2, 3]

[5, 4]
```

<u>Step-3</u>

```python
[1, 2]

[5, 4, 3]
```

<u>Step-4</u>

```
[1]

[5, 4, 3, 2]
```

<u>Step-5</u>

```python
[ ]

[5, 4, 3, 2, 1]
```

You don't necessarily have to remove the elements from the first list. But let us continue with the approach of removing an element from the first list and adding it to the second list. How will you remove an element from a list? This is a challenge for you to think about.

<u>Approach-2</u>

Consider the two lists:

```python
P = [1, 2, 3, 4, 5]
Q = [5, 4, 3, 2, 1]
```

We note the following:

| `x`  | Index of `x` in `P` | Index of `x` in `Q` |
| ---- | ------------------- | ------------------- |
| 1    | 0                   | 4                   |
| 2    | 1                   | 3                   |
| 3    | 2                   | 2                   |
| 4    | 3                   | 1                   |
| 5    | 4                   | 0                   |

Do you see any pattern in the index of the element `x` in `P` and `Q`? Is there a way you can use this pattern to reverse the list?



## Solutions

:::{.panel-tabset}

## Solution-1

```python
L = input().split(',')

out = [ ]
for x in L:
    out = [x] + out

n = len(out)
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-2

Why do we have line-4 where we initialize `out` to `L.copy()`? What happens if we just set `out = L`? Try this and see what happens.

```python
L = input().split(',')

n = len(L)
out = L.copy()
for i in range(n):
    out[i] = L[n - 1 - i]
    
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-3

Take a look at line-5. We are swapping the first and last element, then the second and the penultimate element, and so on. Also take a look at the end-point of the `range` function.

```python
L = input().split(',')

n = len(L)
for i in range(n // 2):
    L[i], L[-i - 1] = L[-i - 1], L[i]

for i in range(n - 1):
    print(L[i], end = ',')
print(L[-1])
```

## Solution-4

Here we are reversing the range. We start from $n - 1$ and go all the way till $0$.

```python
L = input().split(',')
n = len(L)
out = [ ]
for i in range(n - 1, -1, -1):
    out.append(L[i])

for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

:::
