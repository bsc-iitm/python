---
title: PPA-7
pagetitle: Week-2, PPA-7
---

## Question

A sequence of five words is called **magical** if the $i^{th}$ word is a substring of the $(i + 1)^{th}$ word for every $i$ in the range $1 \leq i < 5$. Accept a sequence of five words as input, one word on each line. Print `magical` if the sequence is magical and `non-magical` otherwise.

Note that `str_1` is a substring of `str_2` if and only if `str_1` is present as a sequence of consecutive characters in `str_2`.

## Hint

The `in` keyword is a powerful tool. For example, to see if a string `word1` is a substring of another string `word2`, you just need to type:

```python
word1 in word2
```

If `word1` is a substring of `word2` then this expression evaluates to `True`. If not, it evaluates to `False`. Now, it is just a question of repeatedly applying this condition across the sequence.



## Solutions

:::{.panel-tabset}

## Solution-1

```python
word_1 = input()
word_2 = input()
word_3 = input()
word_4 = input()
word_5 = input()

if ((word_1 in word_2) and
    (word_2 in word_3) and
    (word_3 in word_4) and
    (word_4 in word_5)):
    print('magical')
else:
    print('non-magical')
```

## Solution-2

```python
word_1 = input()
word_2 = input()
word_3 = input()
word_4 = input()
word_5 = input()

present = False
if word_1 in word_2:
    if word_2 in word_3:
        if word_3 in word_4:
            if word_4 in word_5:
                present = True
if present:
    print('magical')
else:
    print('non-magical')
```

:::
