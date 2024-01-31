---
title: PPA-3
pagetitle: Week-4, PPA-3
order: 3
---

## Question

Accept a sequence of comma-separated integers as input and print the maximum value in the sequence as output.



## Hint

Consider the following piece of code.

```python
num = '1,2,3,4,5'
L = num.split(',')
print(L)
```

When this code is executed, it gives the following output:

```
['1', '2', '3', '4', '5']
```

The method `split` is a string method. It can be used with any string variable. The string that is passed as an argument to the `split` method, in this case it is a comma, is called a delimiter. Sometimes you may have to split using a space. For example:

```python
num = '1 2 3 4 5'
L = num.split(' ') # there is a single space between the quotes
print(['1', '2', '3', '4', '5'])
```

The value returned by `num.split(' ')` is a list of strings. The next step is to convert each element of the string into an integer. This could be done in two ways.

:::{.panel-tabset}

## Method-1

```python
L = ['1', '2', '3', '4', '5']
for i in range(len(L)):
    L[i] = int(L[i])
```

## Method-2

```python
L = ['1', '2', '3', '4', '5']
L_ints = [ ]
for x in L:
    x_int = int(x)
    L_ints.append(x_int)
```

:::

Method-1 modifies the list **in-place**. Method-2 creates a new list. Both methods are valid. From here, it is all about finding the maximum element, something that you should be quite familiar with by now.

## Solution

```python
nums = input()
nums = nums.split(',')

max_num = int(nums[0])
for num in nums:
    num = int(num)
    if num > max_num:
        max_num = num
        
print(max_num)
```

