---
title: PPA-11
pagetitle: Week-4, PPA-11
---

## Question

`L` is a list of real numbers that is already given to you. You have to sort this list in descending order and store the sorted list in a variable called `sorted_L`.



## Hint

Let us go with the "obvious sort" approach that was covered in the lecture. We have to keep removing the largest element from the list:

<u>Step-0</u>

```python
[1, 4, 3, 2, 5]

[ ]
```

<u>Step-1</u>

```python
[1, 4, 3, 2]

[5]
```

<u>Step-2</u>

```python
[1, 3, 2]

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

The logic is quite clear. How can we implement this? First, note that we can use `L.remove(x)` to remove the element `x` from the list `L`. What is this element `x` that we are interested in during each step? It is the maximum element in the list. So, each step has three sub-steps:

- Find the maximum element (loop)
- Remove this from the original list (single line statement)
- Append this to a new list (single line statement)

Clearly, the whole thing has to be within a loop. How many times should this outer loop run? Should this outer loop be a for or a while loop? Which do you think is better?



## Solutions

::: {.panel-tabset}

## Solution-1

```python
sorted_L = [ ]
while L != [ ]:
    max_elem = L[0]
    for elem in L:
        if elem > max_elem:
            max_elem = elem
    L.remove(max_elem)
    sorted_L.append(max_elem)
```

## Solution-2

```python
sorted_L = [ ]
while L != [ ]:
    max_elem = max(L)
    L.remove(max_elem)
    sorted_L.append(max_elem)
```

:::
