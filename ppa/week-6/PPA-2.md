---
title: PPA-2
pagetitle: Week-6, PPA-2
order: 2
---

## Question

Accept a positive integer as input and print the digits present in it from left to right. Each digit should be printed as a lower case word on a separate line. How would you use dictionaries to solve this problem?

## Hint

It is good to retain the input as a string. A dictionary can be used to map each number to its corresponding word. An incomplete table is given for your reference:

| Key  | Value |
| ---- | ----- |
| 0    | zero  |
| 1    | one   |
| 2    | two   |

Can you create the dictionary using this table and complete the code?

## Solution

We just need to iterate through the characters in the input and use the dictionary appropriately.  Note the way in which the dictionary has been formatted: each key is written on a separate line. This has been done to improve readability.

```python
mapper = {
    '0': 'zero',
    '1': 'one',
    '2': 'two',
    '3': 'three',
    '4': 'four',
    '5': 'five',
    '6': 'six',
    '7': 'seven',
    '8': 'eight',
    '9': 'nine'
}

num = input()

for digit in num:
    print(mapper[digit])
```

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/c47148c8882447b2ae307188d816dec5?sid=d24963eb-f9fa-4d61-b824-9f0f19f13e89" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
