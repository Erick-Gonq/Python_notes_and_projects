# Python Operators and Data Structures — A Complete Overview

This document provides a structured overview of Python operators and basic data structures, including examples and explanations.

---

## 1. Types of Operators in Python

Python offers several types of operators:

1. **Arithmetic Operators**
2. **Comparison Operators**
3. **Logical Operators**
4. **Assignment Operators**

---

## 2. Arithmetic Operators

Arithmetic operators are used for mathematical calculations.

```python
a = 32
b = 14

# Addition
print("Result:", a + b)   # 46

# Subtraction
print("Result:", a - b)   # 18

# Division
print("Result:", a / b)   # 2.2857
```

### Exercise
- Define `num1 = 27` and raise it to the power of 2 → `27 ** 2 = 729`
- Perform integer division:
  - `84 // 2 = 42`
  - `85 // 2 = 42` (floor division drops the decimal)
- Regular division: `85 / 2 = 42.5`

### Operator Precedence
```python
print(12 + 5 * 6)      # 42  (multiplication first)
print((12 + 5) * 6)    # 102 (parentheses change order)
```

---

## 3. Common Arithmetic Functions

```python
# Rounding
print(round(42.48888, 3))   # 42.489
print(round(42.5))          # 42
print(round(42.6))          # 43

# Absolute value
print(abs(42))   # 42
print(abs(-42))  # 42
```

⚠️ **Note on rounding:**  
Python uses **Banker's rounding**. Values ending in `.5` are rounded to the nearest even integer.

```python
print(round(42.5))  # 42
print(round(43.5))  # 44
```

---

## 4. Strings (Text Variables)

```python
var = "Hello"
print(var)

# Concatenation
"Hello" + " World"

# Repetition
print("Hi! " * 5)

# Length of string
len("house")   # 5
```

⚠️ **Mixing strings and numbers without conversion will cause an error:**
```python
print("Age: " + str(25))   # Correct
```

---

## 5. Data Types

Use `type()` to identify the data type:

```python
print(type(2))        # <class 'int'>
print(type(42.78))    # <class 'float'>
print(type("hello"))  # <class 'str'>
```

---

## 6. Practice Problems

1. How many seconds are in **42 minutes 42 seconds**? → `(42 * 60) + 42 = 2562`
2. Convert **42.2 km to miles** (1 mile = 1.61 km): `42.2 / 1.61 ≈ 26.21 miles`
3. Average seconds per km for a **10 km run in 42:42**: `2562 / 10 = 256.2`
4. Average seconds per mile: `256.2 / 1.61 ≈ 159.13`

---

## 7. Comparison Operators

```python
a = 32
b = 14

print(a == b)   # False
print(a != b)   # True
print(a > b)    # True
print(a < b)    # False

```

---

## 8. Logical Operators

```python
x = True
y = False

print(x and y)   # False
print(x or y)    # True
print(not x)     # False
```

##Truth Table Summary

| Expression                          | Evaluation                     | Result  |
|-------------------------------------|--------------------------------|---------|
| `(a == b)`                          | 32 == 14                       | False   |
| `(a != b)`                          | 32 != 14                       | True    |
| `(a == b) and (a != b)`             | False AND True                 | False   |
| `(a == b) or (a != b)`              | False OR True                  | True    |
| `not(a == b)`                       | not(False)                     | True    |
| `not(a != b)`                       | not(True)                      | False   |
| `not(a == b) and (a != b)`          | True AND True                  | True    |
| `not(a != b) or (a == b)`           | False OR False                 | False   |
| `(a > b) and (a < b)`               | True AND False                 | False   |
| `(a > b) or (a < b)`                | True OR False                  | True    |
| `not((a > b) and (a < b))`          | not(False)                     | True    |
| `not((a > b) or (a < b))`           | not(True)                      | False   |


---

## 9. Lists

Lists can store multiple values, including mixed types.

```python
numbers = [12, 43, 23, 10, 52]
print(numbers[0])     # First element
print(numbers[1:3])   # Slice
print(numbers * 2)    # Repetition

mixed = ["house", 23, False, "hello", 23.87]
print(mixed[3])       # "hello"
```

Nested lists:

```python
nested = [1, 2, 3, ["a", "z", [4, 5, 6]]]
nested[3][2][2] = 69   # Access deeply nested element
```

---

## 10. Tuples

Tuples are **immutable** sequences.

```python
t = (1, 2, 3, 4, 5)
print(t[2])      # 3
t[2] = 21        # ❌ Error: cannot modify a tuple
```

---

## 11. Dictionaries

Dictionaries store **key-value pairs**.

```python
person = {
    "names": ["Carlos", "Ana"],
    "age": [23, 31],
    "province": ["SJ", "AL"]
}

print(person.keys())     # dict_keys(['names', 'age', 'province'])
print(person.values())   # dict_values([...])
```

---

## 12. Data Conversion

```python
# int → float
i = 10
f = float(i)   # 10.0

# float → int
f = 10.68
i = int(f)     # 10

# string → int
s = "123"
i = int(s)     # 123

# int → string
i = 4
s = str(i)     # "4"
```

---

# ✅ Summary

- Arithmetic, comparison, logical, and assignment operators are fundamental in Python.
- Strings allow concatenation, repetition, and length calculation.
- Lists are mutable, tuples are immutable, and dictionaries store key-value pairs.
- Python provides built-in functions for type conversion and mathematical operations.
- Rounding in Python follows the "Banker's rule."

This covers the essentials of Python operators and basic data structures.
