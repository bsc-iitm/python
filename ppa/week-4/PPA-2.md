---
title: PPA-2
pagetitle: Week-4, PPA-2
---

## Question

Accept a sequence of words as input, append all these words to a list in the order in which they are entered, and print this list as output. The first line in the input is a positive integer $n$ that denotes the number of words in the sequence. The next $n$ lines will have one word on each line.

## Hint

There are two steps here:

- accept a string during each iteration of the loop
- append this string to a list

The easiest thing would be a `for` loop as the number of iterations is known to us (first line of the input). But what if we go for a while loop?

```python
while n > 0:
    ### accept string as input ###
    ### append string to list ###
    n -= 1
```

Do you think the above code works?

## Solution

```python
n = int(input())
L = [ ]
for i in range(n):
    word = input()
    L.append(word)
print(L)
```

