---
title: Mock-3
pagetitle: Mock-3
order: 3

---

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/badd0659940c4c39b37299437157575b?sid=471913c7-b257-457f-b765-78f87d0a5b34" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Solution

::: {.panel-tabset}

## Solution-1

```python
date = input()

mm, dd, yyyy = date.split('/')
yy = yyyy[-2:]

out = dd + '-' + mm + '-' + yy

print(out)
```

## Solution-2

```python
date = input()

mm, dd, yyyy = date.split('/')
yy = yyyy[-2:]

out = f'{dd}-{mm}-{yy}'

print(out)
```

## Solution-3

```python
date = input()

mm, dd, yyyy = date.split('/')
yy = yyyy[-2:]

print(dd, mm, yy, sep = '-')
```

## Solution-4

```python
date = input()

mm, dd, yy = date[:2], date[3:5], date[-2:]

print(dd, mm, yy, sep = '-')
```

:::
