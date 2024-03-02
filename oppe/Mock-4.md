---
title: Mock-4
pagetitle: Mock-4
order: 4

---

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/63b81b8c309b47409fbec12247e9b7c1?sid=3547cfad-6924-4ce7-a3b3-3fc5ae3fd592" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Solution

```python
stats = dict()

for i in range(4):
    L = input().split(',')
    name = L[0]
    total = 0
    
    for runs in L[1:]:
        total = total + int(runs)
    
    stats[name] = total
    
print(stats)
```

