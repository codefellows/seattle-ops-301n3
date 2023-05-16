# Ops Challenge: Python Collections

## Overview

Python is known for its relevance to data science and consequently handles data quite well using collections (arrays). Today, you will be creating lists, tuples, sets and dictionaries.

## Resources

- [Python Lists](https://docs.python.org/3/tutorial/datastructures.html)

## Demonstration

- Refer to [DEMO.md](DEMO.md)
- [Hexx's Repl.it Demo](https://replit.com/@HexxKing1/Ops-301n3-Python-Lists#main.py)

## Notes

- What is a list in Python?
  - Python's version of an "array"
  - A built-in data structure that represents an ordered collection of elements.
  - Provides various methods and operations for manipulating and accessing the elements.
    - A method is a special type of function associated with the classes and objects that make up the Python language.
  - Lists are created by enclosing a comma-separated sequence of elements within square brackets `[ ]`.

- What kind of built-in operations are available for lists?
  - You can access elements, modify elements, remove elements plus other operations like returning the length of the list and concatenation.
    - Concatenation is combining two lists together.

- What is "slicing" in Python?
  - `sequence[start:stop:step]`
    - `start` is the index indicating the starting position of the slice (inclusive).
      - If omitted, it defaults to the beginning of the sequence (index 0).
    - `stop` is the index indicating the stopping position of the slice (exclusive). It represents the index of the first element that is not included in the slice.
      - If omitted, it defaults to the end of the sequence.
    - `step` is an optional value specifying the step or stride between elements in the slice. It determines the number of indices to move after each element is included in the slice.
      - If omitted, it defaults to 1.
  - Refers to the technique of extracting a portion (a subsequence) of a sequence object, such as a list, string, tuple, or any other iterable.
  - It allows you to retrieve a contiguous section of elements from the original sequence by specifying the start and end indices.
  - The resulting slice includes elements from the `start` index up to, but not including, the `stop` index, while following the specified step value.
    - The original sequence remains unchanged.
  - When slicing a list, a new list containing the specified portion of elements is returned

- What is a subsequence?
  - A subsequence refers to a sequence of elements that appears in the same relative order as another sequence but may not necessarily be contiguous.
  - It is a subset of the original sequence where the elements maintain their original order
  - In Python, you can extract subsequences from lists, strings, tuples, or any other sequence types using slicing or other methods.
  - Slicing allows you to specify a range of indices to create a subsequence.
  - The elements in the subsequences maintain their original order as in the original sequence, but there may be gaps or other elements in between.

- Some list methods you will see in today's challenge:
  - `.append()`:  add an element to the end of the list
  - `.clear()`: remove all elements from the list, resulting in an empty list
  - `.copy()`: returns a shallow copy of the list
  - `.count()`: returns the number of occurrences of a specified element in the list
  - `.extend()`: append multiple elements to the end of the list
  - `.index()`: returns the index of the first occurrence of a specified element in the list
  - `.insert()`: insert an element at a specified index in the list
  - `.pop()`: removes and returns the element at a specified index in the list
  - `.remove()`: remove the first occurrence of a specified element from the list
  - `.reverse()`: reverses the order of the elements in the list
  - `.sort()`: sort the elements of the list in ascending order

- What is a tuple?
  - `my_tuple = (1, 2, 3, 4, 5, 'apple')`
  - A tuple is an ordered, immutable collection of elements.
  - It is similar to a list, but cannot be modified once created.
  - Tuples are typically used to represent a collection of related values that should not be changed.
  - You can access tuple elements using indexing, just like lists.
    - For example, `my_tuple[0]` retrieves the first element of the tuple.
  - Tuples have methods too! Check out these:
    - `count()`: returns the number of occurrences of a specified element in the tuple
    - `index()`: returns the index of the first occurrence of a specified element in the tuple

- What is a set?
  - `my_set = {1, 2, 3, 4, 5}`
  - A set is an unordered collection of unique elements.
  - It is used when you want to store a group of items without any particular order and ensure that each item appears only once.
  - Sets are highly useful for tasks like membership testing, removing duplicates, and performing mathematical set operations.
  - Some commonly used set methods:
    - `add()`: Adds a single element to the set.
    - `update()`: Adds multiple elements to the set from an iterable.
    - `remove()`: Removes a specific element from the set. Raises a KeyError if the element does not exist.
    - `discard()`: Removes a specific element from the set if it exists. Does not raise an error if the element is not found.
    - `pop()`: Removes and returns an arbitrary element from the set.
    - `union()`: Returns a new set that contains all unique elements from both sets (using the | operator performs the same operation).
    - `intersection()`: Returns a new set that contains common elements between two sets (using the & operator performs the same operation).
    - `difference()`: Returns a new set that contains elements present in the first set but not in the second set (using the - operator performs the same operation).
    - `symmetric_difference()`: Returns a new set that contains elements present in either of the sets, but not both (using the ^ operator performs the same operation).
    - `len()`: Returns the number of elements in the set.
    - `clear()`: Removes all elements from the set.
    - `copy()`: Returns a shallow copy of the set.

- What is a dictionary?
  - 
  ```python
  my_dict = {
    'name': 'Ada', 
    'last': 'Lovelace', 
    'age': 19, 
    'famous_for': 'wrote history’s first computer program'}
  ```
  - A dictionary is an unordered collection of key-value pairs.
  - It is also known as a hash map or hash table in other programming languages and are sometimes compared to objects.
  - Dictionaries are extremely useful for storing and retrieving data based on unique keys rather than relying on positional indexing.
  - Some commonly used dictionary methods:
    - `dict[key]`: Retrieves the value associated with the specified key. Raises a KeyError if the key does not exist. Alternatively, the get() method can be used to retrieve values, which returns None or a default value if the key is not found.
    - `dict[key]` = value: Assigns a value to the specified key. If the key already exists, the existing value is updated.
    - `dict[key]` = value: Adds a new key-value pair to the dictionary. If the key already exists, the existing value is updated.
    - `dict.update(other_dict)`: Adds key-value pairs from another dictionary to the current dictionary.
    - `dict.pop(key)`: Removes the key-value pair associated with the specified key from the dictionary and returns its value. Raises a KeyError if the key does not exist.
    - `del dict[key]`: Deletes the key-value pair associated with the specified key from the dictionary.
    - `dict.clear()`: Removes all key-value pairs from the dictionary.
    - `keys()`: Returns a view object containing all the keys in the dictionary.
    - `values()`: Returns a view object containing all the values in the dictionary.
    - `items()`: Returns a view object containing all the key-value pairs in the dictionary.
    - `len()`: Returns the number of key-value pairs in the dictionary.