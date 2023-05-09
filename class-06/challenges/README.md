# Ops Challenge: Bash in Python

## Overview

Reputed in the cyber community for its various applications ranging from malware analysis to penetration testing, Python is one of the most in-demand and recommended coding languages to learn for a career in cyber security. Today, you will be executing a Linux terminal commands from within a Python script.

## Resources

- [Python.org's PEP8 Style Guide](https://www.python.org/dev/peps/pep-0008/)
- [Python: Why It Is Better for Cybersecurity in 2020](https://www.cybrary.it/blog/python-why-it-is-better-for-cybersecurity-in-2020/)
- [Python Examples](https://www.w3schools.com/python/python_examples.asp)
- [Variables and Data Types in Python](https://www.edureka.co/blog/variables-and-data-types-in-python/#1)

## Demonstration

Refer to [DEMO.md](DEMO.md)

## Notes

- Python is a high-level, interpreted programming language that was created by Guido van Rossum and first released in 1991.
    - What does it mean to be an interpreted programming language?
      - Being an interpreted programming language means that the code written in that language is not directly compiled into machine code before execution.
      - Instead, an interpreter executes the code line by line, translating and executing each statement in real-time.
      - Python, JavaScript, Ruby, PHP, Perl, R, and various shell scripting languages like Bash are all interpreted languages.
- It emphasizes code readability and simplicity, making it easy to learn and use.
- Python has gained popularity for its versatility and wide range of applications, from web development and data analysis to scientific computing, artificial intelligence and yes, even in ops and cybersecurity.
- Reputed in the cyber community for its various applications ranging from malware analysis to penetration testing, Python is one of the most in-demand and recommended coding languages to learn for a career in cybersecurity.
- Key features of Python include:
  - Easy-to-read syntax
    - Python uses indentation and a clear, expressive syntax that promotes readability and reduces the need for excessive punctuation
  - Interpretation
    - Python programs are executed by an interpreter, which allows for interactive development and quick testing of code snippets.
  - Dynamically typed
    - Python is dynamically typed, meaning that variable types are determined at runtime, allowing for flexibility and easier development.
      - When code is ran, the Python interpreter examines the value assigned to a variable and determines its type according to syntax.
  - Rich standard library
    - Python comes with a comprehensive standard library that provides a wide range of modules and functions for various tasks, reducing the need for external dependencies.
  - Extensibility
    - Python can be extended by integrating with other programming languages such as C or C++, allowing developers to harness performance-critical functionality or use existing libraries.
  - Large and active community
    - Python has a vibrant and supportive community of developers who contribute to its ecosystem by creating libraries, frameworks, and tools that further enhance its capabilities.
- Important Python files you might encounter:
  - A `poetry.lock` file is generated and used by the Poetry dependency management tool in Python. Poetry is a tool that helps manage dependencies, build and package Python projects, and create virtual environments.
    - The `poetry.lock` file serves as a lockfile that records the specific versions of the dependencies (including transitive dependencies) that Poetry resolved and used for a particular project. It ensures that the project's dependencies remain consistent across different environments and builds.
    - By using a lockfile like `poetry.lock`, you can achieve reproducible builds and avoid dependency version conflicts, making it easier to collaborate on projects and deploy them consistently.
- A `pyproject.toml` file is a configuration file commonly used in Python projects. It is part of the Python Packaging ecosystem and is primarily associated with the Poetry dependency management tool.
  - The `pyproject.toml` file is written in TOML (Tom's Obvious, Minimal Language) format, which is a human-readable configuration file format. It serves as a central place to define various aspects of a Python project, including dependencies, build settings, tool configurations, and more.