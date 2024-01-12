---
title: PPA-3
pagetitle: Week-3, PPA-3
---

## Question

Accept two positive integers $a$ and $b$ as input. Print the sum of all integers in the range $[1000, 2000]$, endpoints inclusive, that are divisible by both $a$ and $b$. If you find no number satisfying this condition in the given range, then print 0.



## Hint

This is an extension of the [previous problem](/ppa/week-3/PPA-2.md). Here, you have to filter out all the numbers that are divisible by both $a$ **and** $b$.



## Solution

```python
a = int(input())
b = int(input())

total = 0
for f in range(1000, 2001):
    if (f % a == 0) and (f % b == 0):
        total += f

print(total)
```

