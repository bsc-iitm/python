---
title: PPA-6
pagetitle: Week-2, PPA-6
order: 6
---

## Question

Accept a string as input. If the input string is of odd length, then continue with it. If the input string is of even length, make the string of odd length as below:

- If the last character is a period (`.`), then remove it
- If the last character is not a period, then add a period (`.`) to the end of the string

Call this string of odd length `word`. Select a substring made up of three consecutive characters from `word` such that there are an equal number of characters to the left and right of this substring. Print this substring as output. You can assume that all input strings will be in lower case and will have a length of at least four.

## Hint

In case you are confused with the terminology, a period is another term for the full-stop.

This problem can be split into two parts:

- Get a string of odd length.
- Extract the required substring.

If the string is already of odd length, you don't have to do much. If not, then you have to follow the procedure given in the question. A small snippet is given to help you; where do you think you would find this useful?

```python
if word[-1] == '.':
    new_word = word[: -1]
```

If `word = 'abcde'`, then `word[: -1]` is `abcd`. Do you see what is happening here?

Now, how do you extract the substring? The hint is to focus on the character that is at the center of the string. Do you see why this is important? If you do, then how do you obtain the index of the middle chatacter in a string? What does all this have to do with the length of the string being odd? If the string had an even number of characters, what problems would you face?

## Solution

```python
word = input()
if len(word) % 2 == 0:
    if word[-1] == '.':
        word = word[: -1]
    else:
        word = word + '.'
mid = len(word) // 2
out = word[mid - 1:mid + 2]
print(out)
```

