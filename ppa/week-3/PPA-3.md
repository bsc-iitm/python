---
title: PPA-3
pagetitle: Week-3, PPA-3
order: 3
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

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/c05bc1da9b8941b4ba28c0c31057443d?sid=ce60c3a8-5847-4bdc-bde4-cec47ec14f0b" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
