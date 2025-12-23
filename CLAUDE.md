# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Python tutorial repository written in Portuguese ("Tutorial sobre python"). It contains educational examples covering Python programming concepts from basics to advanced topics. The repository is designed as teaching material for classroom use and software development courses.

**Important**: This is a documentation-only repository. All Python code examples are embedded directly in [README.md](README.md) as code blocks. There are no separate Python source files, no build system, no test framework, and no dependencies to install.

## Content Structure

The tutorial is organized into major sections within README.md:

1. **General Language Concepts** - Basic Python syntax, operators, control flow, loops, functions, file I/O, data structures (lists, tuples, sets, dictionaries)
2. **Object-Oriented Programming** - Classes, inheritance, encapsulation, polymorphism
3. **MySQL/MariaDB** - Database operations with Python
4. **MongoDB** - NoSQL database operations
5. **Data Visualization** - Plotting with matplotlib, seaborn, numpy
6. **Statistics** - Statistical analysis, regression, pandas operations
7. **GUI** - Graphical interfaces with PyForms
8. **Data Analysis** - Numpy and Pandas usage
9. **3D Graphics** - 3D plotting with matplotlib

## Working with This Repository

### Editing Tutorial Content

When modifying README.md:
- The file is ~4,200 lines long and contains ~31,000 tokens
- Use `offset` and `limit` parameters when reading to avoid token limits
- All code examples are in Python 3
- Code examples assume the use of Spyder IDE
- Maintain Portuguese language for all documentation text
- Preserve the existing table of contents structure

### Code Examples

All Python examples in the README are:
- Standalone snippets meant to be copied and run in an IDE
- Written for educational purposes with clear, simple implementations
- Sometimes include Portuguese comments
- May reference external libraries (matplotlib, numpy, pandas, seaborn, mysql.connector, pymongo, pyforms)

### License

This repository uses Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) license. Any modifications must respect these terms.

## Common Patterns

Since this is a tutorial repository, typical tasks might include:
- Adding new Python examples to existing sections
- Creating new sections for additional topics
- Fixing code examples that may have syntax errors
- Updating examples to use newer Python syntax
- Ensuring code examples follow consistent formatting

When adding code examples:
- Use Python 3 syntax
- Include `# -*- coding: utf-8 -*-` when examples contain Portuguese text with accents
- Keep examples simple and focused on teaching a single concept
- Add appropriate navigation links (`[Voltar ao sumário](#sumário)`)
