---
title: PPA-1
pagetitle: Week-2, PPA-1
---

## Question

Accept an integer as input. Print `positive` if it is greater than zero and `negative` if it is less than zero. You can assume that the input will be non-zero.

## Hint

An incomplete outline of the solution is given below:

```python
if x > 0:
    print('positive')
```

Can you complete it?

## Solution

Since the problem statement assures us that the input will be non-zero, the following solution will work.

```python
x = int(input())
if x > 0:
    print('positive')
else:
    print('negative')
```

If the input could be zero, then we need to modify the code as follows:

```python
x = int(input())
if x > 0:
    print('positive')
elif x < 0:
    print('negative')
```

This snippet will not print anything when $0$ is passed as input.
