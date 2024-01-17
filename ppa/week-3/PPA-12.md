---
title: PPA-12
pagetitle: Week-3, PPA-12
---

## Question

Accept two strings as input and form a new string by removing all characters from the second string which are present in the first string. Print this new string as output. You can assume that all input strings will be in lower case.



## Hint

Iterating over strings can be done in two ways:

```python
word = 'abcdef'
for char in word:
    print(char)
```

This is the recommended way of iterating over a string. Here, we directly get hold of each character in the string without resorting to the use of string-indices. The other way uses string-indices:

```python
word = 'abcdef'
for i in range(len(word)):
    print(word[i])
```

Though this is not a wrong approach, this is not appropriate for this problem. The index-based approach should be used only if we need to know the character along with its index. In this problem, we are not interested in the index at all, we only need to know the characters present in the string.

To check if a character is present in a string or not, we can simply use the `in` operator. For example:

```python
if 'a' in 'abcde':
    print(True)
else:
    print(False)
```

You have enough information to construct a solution.



## Solution

This solution iterates over `string_2` once. It adds characters to `out` if they are not present in `string_1`.

```python
string_1 = input()
string_2 = input()

out = '' # empty string
for char in string_2:
    if char not in string_1:
        out = out + char

print(out)
```
