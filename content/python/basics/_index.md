+++
title = "Basics"
date = 2019-03-05T10:41:14+09:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

This is the code for python 2. There are some lines that do not work with python 3 because of the grammar changes.

## Basic introduction to python
adapted from 'data_containers.ipynb' by Eric Firing at Univ. of Hawaii

Let's start with numbers.  

#### Numbers and Booleans

Python's system of numbers is quite simple: there are

+ integers
+ floating point numbers
+ complex numbers
+ Boolean (`True` or `False`) types  

The types are determined dynamically, so operations involving integers and floating point numbers yield floating point numbers.


```python
print 1 + 2
print 1.0 + 2
print(1 + 2)
```

    3
    3.0
    3


Division can be tricky because traditional computer languages use integer division on integers.  This was the case by default with Python 2.


```python
print 4/3
print 4.0/3
```

    1
    1.33333333333


There are some built-in functions that operate on numbers, e.g.:


```python
print int(4/3)
print round(4/3)
print abs(4.2 - 5) # Note binary floating point inability
                   # to represent a decimal number exactly.
print pow(2, 3)
```

    1
    1.0
    0.8
    8


The `pow()` function can be replaced by


```python
print 2**3
```

    8


For more math functions, one can import the `math` module from the standard library:


```python
import math
print(math.sin(1))
print(math.sqrt(2))
```

    0.841470984808
    1.41421356237


We will rarely use the `math` module, however, because `numpy` provides the same functionality and much more.

Boolean values are either `True` or `False`, and result from conditional expressions like this:


```python
print("1 > 2 is", 1 > 2, "but 1 < 2 is", 1 < 2)
```

    ('1 > 2 is', False, 'but 1 < 2 is', True)


Here is a more complex conditional expression:


```python
print(1 > 2 or 3 < 4)
```

    True


#### Strings

Python strings can be created with the `str()` function, and as literals using single quotes, double quotes, triple single quotes, or triple double quotes.  The triples can enclose blocks of text spanning multiple lines. The following are all valid strings, each assigned to a variable name:


```python
a = 'Single quotes'
b = "Double quotes"
c = "a string that has 'single quotes' inside it"
d = """This is a multiline
sentence string, ending with a linefeed.
"""
e = '''
This is also valid. It starts and ends with a linefeed.
'''
for example in (a, b, c, d, 3):
    print(example)
```

    Single quotes
    Double quotes
    a string that has 'single quotes' inside it
    This is a multiline
    sentence string, ending with a linefeed.

    3


Strings can be added (concatenated):


```python
print(d + e)
```

    This is a multiline
    sentence string, ending with a linefeed.

    This is also valid. It starts and ends with a linefeed.



#### Sequences: tuples and lists

Tuples and lists are very general sequences--that is, they are containers that preserve order, and they can contain any kind of object at all.  There is one big practical difference: tuples are *immutable*, lists are *mutable*.

To create a tuple from scratch, use round parentheses and commas.


```python
t1 = (1, 2)
t2 = (3, (4, 5), 7, 8, "some string")
print t1
print t2
print t1+t2
print t1*2
```

    (1, 2)
    (3, (4, 5), 7, 8, 'some string')
    (1, 2, 3, (4, 5), 7, 8, 'some string')
    (1, 2, 1, 2)


Lists have many methods, and support addition and multiplication:


```python
a = ["list1", 1, 2]
b = ["list2", 3, 4]
print a + b
print a * 2
c = a.extend(b)     # 'extend' adds elements to the end (assigning to c only to suppress printing)
print a             # This is identical to the sum, a + b, above.
c = a.append(b)     # 'append' addes the argument as a whole
print a
```

    ['list1', 1, 2, 'list2', 3, 4]
    ['list1', 1, 2, 'list1', 1, 2]
    ['list1', 1, 2, 'list2', 3, 4]
    ['list1', 1, 2, 'list2', 3, 4, ['list2', 3, 4]]


#### Sequences: indexing

Lists, tuples, and strings all support the same indexing syntax.

- Python indexing starts from zero.
- A sequence of N elements therefore has indices ranging from 0 through N-1.
- Negative indices count backwards from the end; they are handled by adding N to the negative index, so -1 is the last element, -2 the one before that, etc.
- Basic indexing accesses a single element or a range (*slice*).
- A slice *includes* the start of a range but *excludes* the end.
- A slice has an optional step, for subsampling a range.


```python
# Using the built-in "range" function,
# make a list on which we can practice indexing:
x = list(range(0, 100, 10))
print(x)
print range(0,100,10)
```

    [0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
    [0, 10, 20, 30, 40, 50, 60, 70, 80, 90]


Take the first 5 values, then the last 5 values:


```python
print(x[:5])
print(x[-5:])
```

    [0, 10, 20, 30, 40]
    [50, 60, 70, 80, 90]


See how easy that was?
Now take every second value starting from the second (index 1):


```python
print x[1::2]
```

    [10, 30, 50, 70, 90]
    [40, 30, 20, 10, 0]


In the above examples we are indexing a list with a slice, so we are getting a list back, even if it has only one element in it, or if it is empty.  If we want to get an element from the list, then we index with a single integer:


```python
print(x[0])
print(x[-1])
```

    0
    90
