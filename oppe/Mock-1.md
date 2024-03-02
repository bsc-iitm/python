---
title: Mock-1
pagetitle: Mock-1
order: 1

---

## Video Solution


<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/9df6518995c349f79c15d4d0df183737?sid=fe8eb579-1b25-441c-ba43-c57231a14bc5" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Solution

```python
def is_prime(n):
    if n == 1:
        return False

    for f in range(2, n):
        if n % f == 0:
            return False
    
    return True

def twin_primes(p, q):
    return (abs(p - q) == 2) and is_prime(p) and is_prime(q)
```

