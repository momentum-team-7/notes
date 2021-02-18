## Python Lists
#### Collections enclosed by [], trailing comma is used, indexed like JS arrays
```py
my_list = ['thing1', 'thing2', 'thing3',]
my_list[0] = 'thing1'
```
### Frequently used list methods
```py
my_list.append('thing4') = ['thing1', 'thing2', 'thing3', 'thing4']
my_list.pop() = ['thing1', 'thing2', 'thing3',]
my_list.remove('thing2') = ['thing1', 'thing3]
```
---
## Python Dictionaries
#### Similar to JS objects, key: value pairs enclosed by {}
```py
fruit_amounts = {
    'apples': 3,
    'bananas': 4,
    'papayas': 2,
    }
```
### Obtain values by their keys, NOT their position
```py
fruit_amounts['apples'] = 3
```
---
### Add or reassign values to dictionaries like this:
```py
fruit_amounts['pears'] = 5
fruit_amounts['bananas'] = 10
fruit_amounts = {
    'apples': 3,
    'bananas': 10,
    'papayas': 2,
    'pears': 5,
    }
```
---
## Python Tuples
#### Ordered collections enclosed by (), tuples are immutable (can't be changed)
```py
dimensions = (2, 4, 10)
```
### Obtain data using index, as with lists
```py
dimensions[1] = 4
```
---
### Unpack tuples by assigning each value to a variable
```py
length, width, height = (2, 4, 10)
length = 2
width = 4
height = 2
```
---


