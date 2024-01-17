---
title: PPA-6
pagetitle: Week-3, PPA-6
---

## Question

Accept a sequence of words as input and print the the shortest word in the sequence. The input will have $n + 1$ lines, where $n$ denotes the number of terms in the sequence. The $i^{th}$ line in the input will contain the $i^{th}$ word in the sequence for $1 \leq i \leq n$. 

The last line of the input will always be the string `abcdefghijklmnopqrstuvwxyz`. This string is not a part of the sequence. You can assume that each test case corresponds to a non-empty sequence of words. If there are multiple words that have the same minimum length, print the first such occurrence.



## Hint

This problem is similar to the [previous one](/ppa/week-3/PPA-5.md). Instead of dealing with integers, we are dealing with strings here. Rather than finding the maximum number in the sequence, we need to find the word that has the shortest length. From the CT days, you also know how to find the minimum of a sequence of numbers.



## Solution

```python
word = input()
min_len = len(word)
min_word = word

end_string = 'abcdefghijklmnopqrstuvwxyz'
while word != end_string:
    if len(word) < min_len:
        min_len = len(word)
        min_word = word
    word = input()
print(min_word)
```

