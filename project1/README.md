# Project 1: Python Fundamentals

English | [简体中文](README_zh.md)


Fourteen introductory Python exercises covering variables, data types, operators, control flow, functions and compound data types.

## Repository Structure

```
project1/
├── README.md           # This file
├── 1.1.py              # Read a positive integer and output its square
├── 1.2.py              # Print student admission information from a template
├── 1.3.py              # Calculate a right triangle's hypotenuse
├── 2.1.py              # Calculate distance between two points
├── 2.2.py              # Sum cubes of the digits of a positive three-digit integer
├── 2.3.py              # Count English letters case-insensitively
├── 3.1.py              # Classify grade levels
├── 3.2.py              # Identify character types
├── 4.1.py              # Count digits in an integer
├── 4.2.py              # Calculate 1! + 2! + … + 10!
├── 5.1.py              # Calculate a hypotenuse using a function
├── 5.2.py              # Square root of the sum of numbers within n divisible by both 3 and 7
├── 6.1.py              # Generate an uppercase English letter list
└── 6.2.py              # Look up grade and college from a student ID
```

## Topics

### 1. Data Types (1.1–1.3)

| Number | Exercise | Concepts |
|------|------|--------|
| 1.1 | Square a positive integer | `int()` conversion and basic arithmetic |
| 1.2 | Format admission information | f-strings and list indexing |
| 1.3 | Find a right triangle's hypotenuse | `map()`, `split()` and exponentiation |

### 2. Operators and Expressions (2.1–2.3)

| Number | Exercise | Concepts |
|------|------|--------|
| 2.1 | Distance between two points | `eval()` input parsing, Euclidean distance and formatted output |
| 2.2 | Sum of cubes of a three-digit integer's digits | Integer division `//`, remainder `%` and digit decomposition |
| 2.3 | Case-insensitive letter counting | `str.lower()`, `str.count()` and case-insensitive matching |

### 3. Conditional Statements (3.1–3.2)

| Number | Exercise | Concepts |
|------|------|--------|
| 3.1 | Grade classification | if-elif-else branches and range validation |
| 3.2 | Character classification | `isdigit()`, `isupper()` and `islower()` |

### 4. Loops (4.1–4.2)

| Number | Exercise | Concepts |
|------|------|--------|
| 4.1 | Count an integer's digits | while loops and `//=10` iteration |
| 4.2 | Sum 1! through 10! | for loops and `math.factorial()` |

### 5. Functions (5.1–5.2)

| Number | Exercise | Concepts |
|------|------|--------|
| 5.1 | Hypotenuse calculation with a function | Function definitions, parameters and `return` |
| 5.2 | Square root of a filtered sum | Function encapsulation and conditional filtering loops |

### 6. Lists, Tuples and Dictionaries (6.1–6.2)

| Number | Exercise | Concepts |
|------|------|--------|
| 6.1 | Generate uppercase letters | List comprehensions, `chr()` and ASCII codes |
| 6.2 | Look up year and department from an identifier | String slicing, dictionary mappings and `dict.get()` |

## Running the Scripts

Each file runs independently, without additional third-party libraries:

```bash
cd project1
python 1.1.py
```

Each script reads standard input (`input()`) and writes to standard output (`print()`).

## Requirements

- Python 3.6+ (3.12+ recommended)
- No third-party dependencies; only the standard library and `math` are used
