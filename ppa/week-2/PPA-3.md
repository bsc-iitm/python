---
title: PPA-3
pagetitle: Week-2, PPA-3
order: 3
---

## Question

Accept an integer as input and print the time of the day. Use the following table for reference.

| Input               | Output    |
| ------------------- | --------- |
| $T < 0$             | INVALID   |
| $0 \leq T \leq 5$   | NIGHT     |
| $6 \leq T \leq 11$  | MORNING   |
| $12 \leq T \leq 17$ | AFTERNOON |
| $18 \leq T \leq 23$ | EVENING   |
| $T \geq 24$         | INVALID   |

The input will be a single line containing an integer. The output should be one of these strings: NIGHT, MORNING, AFTERNOON, EVENING, INVALID.



## Hint

How is this problem related to the [previous problem](/ppa/week-2/PPA-2.md)? Do they have the same structure?

Think about the following code snippets:

:::{.panel-tabset}

## Snippet-1

```python
if T < 0:
    print('INVALID')
elif 0 <= T <= 5:
    print('NIGHT')
```

## Snippet-2

```python
if T < 0:
    print('INVALID')
if 0 <= T <= 5:
    print('NIGHT')
```

:::

Come up with two different solutions to the problem, one that develops snippet-1 and the other which develops snippet-2. What is the difference between these two solutions that you arrive at? Which one is better?



## Solutions

:::{.panel-tabset}

## Solution-1


```python
t = int(input())
if 0 <= t <= 5:
    print('NIGHT')
elif 6 <= t <= 11:
    print('MORNING')
elif 12 <= t <= 17:
    print('AFTERNOON')
elif 18 <= t <= 23:
    print('EVENING')
else:
    print('INVALID')
```

## Solution-2

It is better to stick to `if-elif-else` ladders wherever possible and avoid a sequence of `if` conditions. The `if-elif-else` ladder is more efficient. As soon as one of the conditions is satisfied, the control will exit from the ladder. An `if-if-if` ladder on the other hand will end up checking every one of the `if` conditions for every possible input.


```python
t = int(input())
if t < 0:
    print('INVALID')
if 0 <= t <= 5:
    print('NIGHT')
if 6 <= t <= 11:
    print('MORNING')
if 12 <= t <= 17:
    print('AFTERNOON')
if 18 <= t <= 23:
    print('EVENING')
if t >= 24:
    print('INVALID')
```

:::