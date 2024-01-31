---
title: PPA-6
pagetitle: Week-4, PPA-6
order: 6
---

## Question

Accept a sequence of comma-separated words as input. Reverse the sequence and print it as output.



## Hint

<u>Approach-1</u>

Consider the following sequence of operations on a list `L = [1, 2, 3, 4, 5]`. To reverse this list, you can pick up its last element and make it the first element of a new list.

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

```python
[1]

[5, 4, 3, 2]
```

<u>Step-5</u>

```python
[ ]

[5, 4, 3, 2, 1]
```

You don't necessarily have to remove the elements from the first list. But let us continue with the approach of removing an element from the first list and adding it to the second list. How will you remove an element from a list?

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

Solutions galore! Do make it a point to go through every one of them.

:::{.panel-tabset}

## Solution-1

```python
L = input().split(',')

out = [ ]
for x in L:
    out = [x] + out

# Printing: common to all solutions
n = len(out)
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-2

```python
L = input().split(',')

n = len(L)
out = [ ]
for i in range(n):
    out.append(L[n - 1 - i])
    
# Printing: common to all solutions
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-3

Take a look at line-5. As the loop proceeds, we are swapping the first and last element, then the second and the penultimate element, and so on. Also take a look at the end-point of the `range` function. This solution stands out from all the previous two in one detail: it reverses the list in-place, meaning, it doesn't require a new list.

```python
L = input().split(',')

n = len(L)
for i in range(n // 2):
    L[i], L[-i - 1] = L[-i - 1], L[i]

# Printing: common to all solutions
for i in range(n - 1):
    print(L[i], end = ',')
print(L[-1])
```

## Solution-4

Here we are reversing the range. We start from $n - 1$ and go all the way till $0$. The step-size is $-1$. Hence the range function looks like this: `range(n - 1, -1, -1)`. The end-point is one less than where we want to stop, hence it is $-1$ and not $0$.

```python
L = input().split(',')
n = len(L)
out = [ ]
for i in range(n - 1, -1, -1):
    out.append(L[i])

# Printing: common to all solutions
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-5

The best is reserved for the last. This uses some advanced slicing. We know that `L[start:end]` gives the slice from `L[start]` to `L[end - 1]`. The third argument in the slice is the step size. So when we have `L[::-1]`, it means start from the end of the list and go all the way till the beginning of the list in steps of $-1$.

```python
L = input().split(',')
out = L[::-1]

# Printing: common to all solutions
n = len(out)
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-6

If you thought solution-5 was the best of the lot, here is something better. This reverses the list in-place.

```python
L = input().split(',')
L.reverse()

# Printing: common to all solutions
n = len(L)
for i in range(n - 1):
    print(L[i], end = ',')
print(L[-1])
```

## Solution-7

We will not go into the details, but there is a construct called `reversed` that helps us iterate over a reversed sequence.

```python
L = input().split(',')
out = [ ]
for x in reversed(L):
    out.append(x)

# Printing: common to all solutions
n = len(out)
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

## Solution-8

We can directly convert this into a list. Try removing `list` and see what you get.

```python
L = input().split(',')
out = list(reversed(L))

# Printing: common to all solutions
n = len(out)
for i in range(n - 1):
    print(out[i], end = ',')
print(out[-1])
```

:::
