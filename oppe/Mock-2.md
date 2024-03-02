---
title: Mock-2
pagetitle: Mock-2
order: 2

---

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/3b27ff72575841608156138675dda142?sid=ee9d427e-5f29-4af9-9b39-1509b759a6c1" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Solution

```python
def is_long_tail(x):
    num = str(x)
    first, second = num.split('.')
    return len(second) > len(first)

def long_tail(L):
    count = 0
    for x in L:
        if is_long_tail(x):
            count = count + 1
    return count
```

