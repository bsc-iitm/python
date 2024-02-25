---
title: PPA-1
pagetitle: Week-6, PPA-1
order: 1
---



## Question

Accept a sequence of words as input. Create a dictionary named `freq` whose keys are the distinct words in the sequence. The value corresponding to a key (word) should be the frequency of occurrence of the key (word) in the sequence.

<hr>

(1) You can assume that all words will be in lower case.

(2) You do not have to print the output to the console. This will be the responsibility of the autograder.

## Hint

Split the input based on `,` and store the words in a list. Now consider the following approaches:

<u>Approach-1</u>

Use two loops. In the first loop, populate the keys of the dictionary with the value $0$ for each key. In another loop, iterate through the words again and increment the value of a word every time it is found.

<u>Approach-2</u>

Use a single loop to do both these things:

- Create a key-value pair for a word and 
- Update a word's value whenever it occurs. 

You would have to use appropriate if statements to achieve this.

<u>Approach-3</u>

Explore the `get` method in dictionaries and figure out how that can be used to arrive at a solution.

## Solutions

::: {.panel-tabset}

## Solution-1

```python
L = input().split(',')

freq = dict()

for word in L:
    freq[word] = 0

for word in L:
    freq[word] += 1
```

## Solution-2

This approach requires a single pass through the list and is more efficient.

```python
L = input().split(',')

freq = dict()

for word in L:
    if word in freq:
        freq[word] += 1
    else:
        freq[word] = 1
```

## Solution-3

This is a small variation compared to the previous solution.

```python
L = input().split(',')

freq = dict()

for word in L:
    if word not in freq:
        freq[word] = 0
    freq[word] += 1
```

The increment operation in line-6 is outside the if-block and will be executed in every iteration of the loop. We will stick to this approach in all subsequent problems.

## Solution-4

This is probably the shortest. It uses the `get` method of dictionaries. If `word` is a key, then `freq.get(word, 0)` will return the value corresponding to it. If not, it will return $0$ (the second argument passed to `get`). Once we get the value, we can update it.

```python
L = input().split(',')

freq = dict()

for word in L:
    freq[word] = freq.get(word, 0) + 1
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/6c5ed8e4a2a544929e5ff38f4f16b35a?sid=b38f2bae-fb5c-431a-9b26-2697a12cec63" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>