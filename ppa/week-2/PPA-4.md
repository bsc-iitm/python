---
title: PPA-4
pagetitle: Week-2, PPA-4
order: 4
---

## Question

Accept a point in 2D space as input and find the region in space that this point belongs to. A point could belong to one of the four quadrants, or it could be on one of the two axes, or it could be the origin. The input is given in 2 lines: the first line is the x-coordinate of the point while the second line is its y-coordinate. The possible outputs are `first`, `second`, `third`, `fourth`, `x-axis`, `y-axis`, and `origin`. Any other output will not be accepted. Note that all outputs should be in lower case.

## Hint

For a point `(x, y)`, you have to construct a table such as this:

| Condition                           | Result |
| ----------------------------------- | ------ |
| Both `x` and `y` are positive       | first  |
| `x` is positive and `y` is negative | fourth |

Your task is twofold. First, complete this table. How many rows does it have? Secondly, convert the conditions into Python expressions. Now, you just have to write a sequence of conditional statements and print the appropriate string. Study the following snippets:

:::{.panel-tabset}

## Snippet-1

```python
if x > 0:
    if y > 0:
        print('first')
```

## Snippet-2

```python
if x > 0 and y > 0:
    print('first')
```

## Snippet-3

```python
if x > 0 or y > 0:
    print('first')
```

:::

Here is a follow-up question to help you with the second task:

- Among the three snippets, which one would you choose to include in your solution to the problem?
- What are the differences and similarities between snippet-1 and snippet-2?

## Solutions

An image of the coordinate plane with the regions marked on it:

![](/assets/images/img_003.png)

:::{.panel-tabset}

## Solution-1

```python
x = float(input())
y = float(input())

if x > 0:
    if y > 0:
        print('first')
    elif y < 0:
        print('fourth')
    else:
        print('x-axis')
elif x < 0:
    if y > 0:
        print('second')
    elif y < 0:
        print('third')
    else:
        print('x-axis')
else:
    if y != 0:
        print('y-axis')
    else:
        print('origin')
```

## Solution-2

```python
x = float(input())
y = float(input())

if x > 0 and y > 0:
    print('first')
elif x < 0 and y > 0:
    print('second')
elif x < 0 and y < 0:
    print('third')
elif x > 0 and y < 0:
    print('fourth')
elif x != 0 and y == 0:
    print('x-axis')
elif x == 0 and y != 0:
    print('y-axis')
elif x == 0 and y == 0:
    print('origin')
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/5797a6d4f0d145169a0a8ec036190809?sid=7b324a75-1891-4aeb-9346-5888754dca49" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

