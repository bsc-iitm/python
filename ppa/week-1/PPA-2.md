---
title: PPA-2
pagetitle: Week-1, PPA-2
---

## Question

Print the following pattern.

```default
*
**
***
****
*****
```

There are no spaces between consecutive stars. There are no spaces at the end of each line.

## Hint

There are two ways of solving this problem. Consider the third line of the output. We could either do it this way:

```python
print('***')
```

Or this way:

```python
print('*' * 3)
```

Multiplying a string by a number results in replication of the string. For example:

```python
print('ab' * 3)
```

This gives the output:

```default
ababab
```

As a follow up question, what do you think will happen if we multiply a string by $0$?

```python
print('ab' * 0)
```

And what about multiplying a string by a number that is not an integer?

```python
print('abc' * 1.5)
```



## Solutions

::: {.panel-tabset}

## Solution-1

```python
print('*')
print('**')
print('***')
print('****')
print('*****')
```



## Solution-2

```python
print('*')
print('*' * 2)
print('*' * 3)
print('*' * 4)
print('*' * 5)
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/cac72342d7624ca8bd168a5460a181f3?sid=e5df2824-9536-4253-80eb-efc3a2f538c2" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
