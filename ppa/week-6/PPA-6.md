---
title: PPA-6
pagetitle: Week-6, PPA-6
order: 6
---

## Question

<u>Scores Dataset Revisited</u>

Recall the Scores dataset from CT. We shall be using a variant of this dataset for this problem. Each student-entry in the dataset is represented as a dictionary. For example, one of the entries would look like this:

```python
{'SeqNo': 1, 'Name': 'Devika', 
 'Gender': 'F', 'City': 'Bengaluru',
 'Mathematics': 85, 'Physics': 100, 'Chemistry': 79,
 'Biology': 75, 'Computer Science': 88, 
 'History': 60, 'Civics': 88, 'Philosophy': 95}
```

All keys of the dict are strings. For `SeqNo` and all the subjects, the corresponding values are integers. The values corresponding to `Name`, `Gender` and `City` are strings.

The entire dataset is represented as a list of dictionaries. That is, each element of the list will be a dictionary like the one given above. This list is named **`scores_dataset`**. The `SeqNo` is a unique identifier for each student that runs from $0$ to $n - 1$, where $n$ is the total number of students in the dataset.

<hr>

Write a function named **`get_marks`** that accepts the `scores_dataset` and a variable named `subject` as arguments. It should return the marks scored by all students in `subject` as a list of tuples. Each element in this list is of the form `(Name, Marks)`. The order in which the tuples are appended to the list doesn't matter

<hr>

- You do not have to accept input from the user or print the output to the console. You just have to write the definition of the function.
- Do not try to process the output produced. We randomly sample five elements from the list returned by your function and print that in the desired form.

## Solution

Let us consider the dictionary for one student:

```python
student = {
    'SeqNo': 1, 
    'Name': 'Devika', 
    'Gender': 'F', 
    'City': 'Bengaluru', 
    'Mathematics': 85, 
    'Physics': 100, 
    'Chemistry': 79, 
    'Biology': 75, 
    'Computer Science': 88, 
    'History': 60, 
    'Civics': 88, 
    'Philosophy': 95
}
```

What we need is a tuple of the form `(name, marks)`. If the subject is Physics, then this tuple is:

```python
(student['Name'], student['Physics'])
```

All that we need to do is iterate over each student in the `scores_dataset`. Note that the dataset is a list of dictionaries. One such dictionary is `student` as shown above.

::: {.panel-tabset}

## Method-1

```python
def get_marks(scores_dataset, subject):
    marks = [ ]
    for student in scores_dataset:
        T = (student['Name'], student[subject])
        marks.append(T)
    return marks
```

## Method-2

This is the same as the previous method. Rather than creating an intermediate variable, the tuple is directly appended to `marks`.

```python
def get_marks(scores_dataset, subject):
    marks = [ ]
    for student in scores_dataset:
        marks.append((student['Name'], 
                      student[subject]))
    return marks
```

:::

Note the loop variable that we have used: `student`. This is an apt choice because each element in `scores_dataset` is a dictionary that corresponds to some student. Good choice of loop variables greatly improves the readability of code.

::: {.callout-note}

- Avoid indiscriminate use of  `i` and `j` as loop variables. Reserve them for specific uses like iterating through matrices.

- Avoid `for i in range(len(L))` construct and instead use `for item in L` wherever possible.

:::
