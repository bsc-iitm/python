---
title: PPA-10
pagetitle: Week-6, PPA-10
order: 10
---

## Question

The scores dataset is a list of dictionaries one of whose entries is given below for your reference:

```python
{'SeqNo': 1, 'Name': 'Devika', 
 'Gender': 'F', 'City': 'Bengaluru', 
 'Mathematics': 85, 'Physics': 100, 'Chemistry': 79, 
 'Biology': 75, 'Computer Science': 88, 
 'History': 60, 'Civics': 88, 'Philosophy': 95}
```

Write the following functions:

- **`group_by_city`**: accepts the `scores_dataset` as argument. It should return a dictionary named `cities` whose keys are names of the cities that the students are from. The value corresponding to a key (city) is the list of names of all students who hail from this city. The order in which names are appended to the list doesn't matter.
- **`busy_cities`**: accepts the `scores_dataset` as argument. It should return a list of cities. Each city in this list has the property that the number of students from this city is greater than or equal to the number of students from every other city in the dataset. Your function should make use of `group_by_city`. The order in which the cities appended to the list doesn't matter.

<hr>

- You do not have to accept input from the user or print the output to the console. You just have to write the definition of both the functions.
- Do not try to process the output produced. We randomly sample a few elements from the dictionary or list returned by your function and print that in the desired form.

## Solution

<u>Group students by city</u>

A dictionary is a good data structure when we want to separate data into well defined clusters. For example, in this question, we have to group students by the place they belong to. Whatever is the common property becomes the key, city in this case. All objects that share this property are mapped to this key. Since there might be multiple objects sharing the same property, a list is a good choice to store all these objects. In this problem, the dict will look something like this:

```python
cities = {
    'Kanpur': ['Lalit', 'Sapana', 'Anita'],
    'Chennai': ['Karthik', 'Soumya'],
    'Trivandrum': ['George', 'Ankit']
}
```

Now, let us look at the code. The general structure should be familiar by now:

- if an item is not present as a key in the dict, include that as a key
- in each iteration of the loop, update the value corresponding to this key

```python
def group_by_city(scores_dataset):
    cities = dict()
    for student in scores_dataset:
       	name, city = student['Name'], student['City']
        if city not in cities:
            cities[city] = [ ]
        cities[city].append(name)
    return cities
```

<u>Identify busy cities</u>

Note the way we have broken down the problem into two parts. In the first part, we grouped students by city. Now, we have to use this grouping and identify busy cities. We could have clubbed both of them together, but that would have made life more difficult for us.

```python
def busy_cities(scores_dataset):
    cities = group_by_city(scores_dataset)
    busy, busy_count = [ ], 0
    for city, from_city in cities.items():
        if len(from_city) > busy_count:
            busy, busy_count = [city], len(from_city)
        elif len(from_city) == busy_count:
            busy.append(city)
    return busy
```

The basic catch here is that multiple cities could have the same maximum number of occupants. This is the reason we check for the equality in line-7. For example, in the second test case, Bengaluru, Delhi and Nagpur have the same value for the number of students hailing from these cities and this value happens to be maximum across all cities.
