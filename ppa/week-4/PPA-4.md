---
title: PPA-4
pagetitle: Week-4, PPA-4
---

## Question

A list `L` of words is already given to you. Print the longest word in the list. If there are multiple words with the same maximum length, print the one which appears at the rightmost end of the list.

## Hint

Consider the following snippet of code.

```python
long_word, long_len = '', 0
for word in L:
    if len(word) > long_len:
        long_len = len(word)
        long_word = word
```

At the end of execution of this code, do you think `long_word` is the longest word in the list `L`?

**<u>Key-point</u>**

While iterating through a list of strings, make it a point to avoid the use of indices as much as possible. That is, try to avoid the following:

```python
for i in range(len(L)):
    ## do something with L[i] ##
```

Rather, use the following template:

```python
for word in L:
    ## do something with word ##
```

Though both of them end up doing the same thing, the second template is more readable and **Pythonic**. That said, there would be problems (check next one) where you would require both the string and its index in the list. What can be done in such situations? Python provides a facility called `enumerate` for this.

**<u>enumerate</u>**

```python
L = ['zero', 'one', 'two', 'three']
for index, word in enumerate(L):
    print(index, word)
```

This gives the following output:

```default
0 zero
1 one
2 two
3 three
```

Instead of a single loop variable, note that we have two loop variables — `index` and `word` in line-2 of the code. Don't worry about why this works. The rationale behind this will become clear when we discuss tuples in week-6. The point to keep in mind is that Python provides a way to iterate through a list in a clean way without having to use the unwieldy `range(len(L))` construct.

## Solution

```python
max_word, max_len = '', 0
for word in L:
    if len(word) >= max_len:
        max_len = len(word)
        max_word = word
print(max_word)
```

