# Ops Challenge: Directory Creation

## Overview

Functions are universally useful across all coding languages for their role as a subroutine within a script that can accept input parameters. Today, you will be creating a Python script that utilizes a function from the `os` library to generate directory information.

## Resources

- [Python Functions](https://www.learnpython.org/en/Functions)
- [`os.walk()` Documentation](https://docs.python.org/3/library/os.html)
- [Tuple Objects in Python](https://docs.python.org/3/c-api/tuple.html)

## Demonstration

- Refer to [DEMO.md](DEMO.md)
- [Hexx's Repl.it Demo](https://replit.com/@HexxKing1/Ops-301n3-Python-Functions)

## Notes

- `os.walk(directory_path)` is a function from the os module in Python that generates the file names in a directory tree by walking the tree either top-down or bottom-up.
  - parameter vs argument
    - parameter defines the value that the function is going to take in
    - argument is the input into that function - it is the value! 
- It returns a generator that yields a tuple containing three values for each directory it visits:
  - `root`: The current directory being visited (as a string).
  - `dirs`: A list of sub-directories in the current directory.
  - `files`: A list of files in the current directory.
- Use a loop to iterate over the tuple and read the values.
- By using `os.walk()`, you can explore the entire directory tree, including all sub-directories and files, and access their paths within the loop.

- In Python, a tuple is an ordered, immutable collection of elements enclosed in parentheses (). It is similar to a list, but unlike lists, tuples cannot be modified once created.
- Tuples are commonly used when you want to represent a collection of values that should not be modified, such as coordinates, database records, or multiple return values from a function.
- Tuples maintain the order of elements, meaning that the elements have a specific position and can be accessed using indexing similar to an array or list.
  - For example, `my_tuple[0]` will access the first element of the tuple.