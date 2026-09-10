# Code Audit Report — Factorial Calculator

## 1. Project Overview

**Project:** Factorial Calculator
**Language:** Python
**Source:** `factorial.py` / `factorial.ipynb`

The program accepts an integer from the user and calculates its factorial using an iterative `for` loop.

## 2. Code Review

### Input Handling

The program accepts user input using:

```python
n = int(input("Enter a number: "))
```

The input is converted to an integer before processing.

### Factorial Calculation

The factorial calculation starts with:

```python
factorial = 1
```

The program then iterates from `1` through `n`:

```python
for i in range(1, n + 1):
    factorial *= i
```

Each value is multiplied into the running factorial.

### Output

The calculated result is displayed using:

```python
print("Factorial of", n, "=", factorial)
```

## 3. Complexity Analysis

**Time Complexity:** `O(n)`

The loop executes `n` times for a non-negative integer `n`.

**Space Complexity:** `O(1)`

The program uses a constant amount of additional memory apart from the integer value being calculated.

## 4. Findings

| Category                | Status         | Observation                                 |
| ----------------------- | -------------- | ------------------------------------------- |
| Basic functionality     | ✅ Pass         | Correct iterative factorial calculation     |
| Input conversion        | ✅ Pass         | Converts input to integer                   |
| External dependencies   | ✅ Pass         | No external libraries required              |
| Time complexity         | ✅ Acceptable   | `O(n)`                                      |
| Space complexity        | ✅ Acceptable   | `O(1)` auxiliary space                      |
| Code simplicity         | ✅ Pass         | Simple and easy to understand               |
| Negative input handling | ⚠️ Improvement | No explicit validation for negative numbers |
| Invalid input handling  | ⚠️ Improvement | Non-integer input will raise an error       |

## 5. Recommendations

For a more robust version, the program could:

1. Validate that the input is a non-negative integer.
2. Handle invalid user input using `try-except`.
3. Add comments or a function definition for improved reusability.
4. Add test cases for values such as `0`, `1`, and larger positive integers.

## 6. Overall Assessment

**Status: ✅ PASS**

The implementation is suitable as a basic Python factorial program. The logic is straightforward, uses an efficient iterative approach, and does not require external dependencies.

The main improvements recommended are input validation and error handling.

## 7. Conclusion

The factorial calculator successfully demonstrates the basic use of:

* User input
* Variables
* `for` loops
* Arithmetic operations
* Output statements

The current implementation is appropriate for a beginner-level Python project.
