---
title: PPA-9
pagetitle: Week-6, PPA-9
order: 9
---

## Question

Accept a sequence of words as input. Create a dictionary named `real_dict` whose keys are the letters of the English alphabet. For each key (letter), the corresponding value should be a list of words that begin with this key (letter). For any given key, the words should be appended to the corresponding list in the order in which they appear in the sequence. You can assume that all words of the sequence will be in lower case.

<hr>

You do not have to print the output to the console.

## Solution

The way we populate the dictionary here is similar to the second approach adopted in PPA-1. The only difference here is that the value is a list. 

- Every time a new letter is encountered, we make this a key of the dictionary whose value is an empty list.
- Line-9 is outside the if-block and will be executed in every iteration of the loop.

```python
L = input().split(',')

real_dict = dict()

for word in L:
    first = word[0]
    if first not in real_dict:
        real_dict[first] = [ ]
    real_dict[first].append(word)
```

