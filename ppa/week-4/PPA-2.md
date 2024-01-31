---
title: PPA-2
pagetitle: Week-4, PPA-2
order: 2
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

::: {.panel-tabset}

## Solution-1

Notice that the loop variable `i` is not being used anywhere within the body of the loop. It just acts as a syntactic placeholder. Head to solution-2 to see what could be done in such cases. 

```python
n = int(input())
L = [ ]
for i in range(n):
    word = input()
    L.append(word)
print(L)
```

## Solution-2

When the loop variable is just a dummy placeholder, coders often use an `_` instead of a variable name such as `i` or `j`. Check out this [Stackoverflow](https://stackoverflow.com/questions/5893163/what-is-the-purpose-of-the-single-underscore-variable-in-python){target=_blank} answer for more details.

```python
n = int(input())
L = [ ]
for _ in range(n):
    word = input()
    L.append(word)
print(L)
```

:::
