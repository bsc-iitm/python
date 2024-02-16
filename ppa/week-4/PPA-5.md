---
title: PPA-5
pagetitle: Week-4, PPA-5
order: 5
---

## Question

Accept a space-separated sequence of positive real numbers as input. Convert each element of the sequence into the greatest integer less than or equal to it. Print this sequence of integers as output, with a comma between consecutive integers.

## Hint

A very important task that will keep repeating throughout the course is to print a sequence of items separated by a specific delimiter, say a comma or a space. For example, given a list `L = [1, 2, 3, 4, 5]`, how does one print the sequence `1,2,3,4,5`?

The first idea is to just add a comma after every element:

```python
L = [1, 2, 3, 4, 5]
for x in L:
    print(str(x) + ',')
```

Is `str(x)` needed here? Can't it be just `x`? 

When this code is executed, it displays the output on five separate lines. By default, `print` adds a new line at the end after whatever item it is supposed to print. This default behaviour can be suppressed using the end argument:

```python
L = [1, 2, 3, 4, 5]
for x in L:
    print(str(x) + ',', end = '')	# there is no space between the quotes
```

This prints `1,2,3,4,5,`. While this is an improvement from the previous case, there is a problem with the comma right at the end. Before addressing that issue, this code can be simplified in the following manner:

```python
L = [1, 2, 3, 4, 5]
for x in L:
    print(x, end = ',')
```

This also gives the same output as before: `1,2,3,4,5,`. Now, it is time to get rid of the last comma. There are two ways to do it:

:::{.panel-tabset}

## Method-1

```python
L = [1, 2, 3, 4, 5]
for num in L[: -1]:
	print(num, end = ',')
print(L[-1])
```

## Method-2

```python
L = [1, 2, 3, 4, 5]
for index, num in enumerate(L):
    if index == len(L) - 1:
        print(num)
    else:
        print(num, end = ',')
```

:::

- Method-1 iterates over the first `len(L) - 1` elements of the list and adds a comma after every element. It then gets out of the loop and just prints the last element without a comma.

- Method-2 iterates over all the elements. If `index` corresponds to `len(L) - 1`, it just prints that element. If not, it prints the element and adds a comma at the end. 

Both are valid methods.



## Solution

Why can't we directly do `L[i] = int(L[i])`? Why do we need line-4 to happen before line-5? Try deleting line-4 and see what happens.

```python
L = input().split(' ')

for i in range(len(L)):
    L[i] = float(L[i])
    L[i] = int(L[i])

for i in range(len(L)):
    if i != len(L) - 1:
        print(L[i], end = ',')
    else:
        print(L[i])
```

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/3d61bab80caa4f3abd48b4cea18d0ab7?sid=fbcfbfa5-6fc8-4d31-b48e-66cd146619a1" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
