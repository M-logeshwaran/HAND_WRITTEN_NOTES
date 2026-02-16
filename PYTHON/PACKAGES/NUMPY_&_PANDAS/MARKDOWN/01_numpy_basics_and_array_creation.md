📄 01_numpy_basics_and_array_creation.md

# NumPy Basics and Array Creation

NumPy (Numerical Python) is a library used for fast operations on large data.

It provides:
- Fast computation
- Continuous memory allocation
- Multi-dimensional arrays
- Rich mathematical and statistical functions

---

# 1. Import NumPy

```python
import numpy as np


---

2. Creating Arrays

2.1 One Dimensional Array (1D)

n = np.array([3, 4, 5, 6])
print(n)

Output:

[3 4 5 6]


---

2.2 Two Dimensional Array (2D)

n1 = np.array([[3, 4], [1, 2]])
print(n1)

Output:

[[3 4]
 [1 2]]


---

3. Creating Array with Zeros

n2 = np.zeros((3, 5))
print(n2)

Output:

[[0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0.]]


---

4. Creating Array with Ones

n3 = np.ones((2, 3, 3), dtype=np.int32)
print(n3)

Output:

[[[1 1 1]
  [1 1 1]
  [1 1 1]]

 [[1 1 1]
  [1 1 1]
  [1 1 1]]]

(3-Dimensional array)


---

5. Creating Empty Array

n4 = np.empty((2, 3))
print(n4)

Output: (Contains random values because memory is not initialized)

Example:

[[1.0432e-38 0.0000e+00 4.9206e-43]
 [0.0000e+00 0.0000e+00 0.0000e+00]]


---

6. Creating Array with Range of Values

6.1 arange()

n5 = np.arange(0, 21, 5)
print(n5)

Output:

[ 0  5 10 15 20]


---

6.2 linspace()

Creates evenly spaced values.

n6 = np.linspace(0, 20, 8)
print(n6)

Output:

[ 0.          2.85714286  5.71428571  8.57142857
 11.42857143 14.28571429 17.14285714 20.        ]

Includes start and stop values.


---

7. Creating Array with Same Value

n7 = np.full((2, 5), 99)
print(n7)

Output:

[[99 99 99 99 99]
 [99 99 99 99 99]]


---

8. Array Attributes

n8 = np.array([[3, 4, 5], [6, 7, 8]])

print(n8.ndim)
print(n8.shape)
print(n8.size)
print(n8.dtype)
print(n8.itemsize)
print(n8.nbytes)

Output:

2               # number of dimensions
(2, 3)          # shape (rows, columns)
6               # total elements
int64           # data type (may vary)
8               # size of one element in bytes
48              # total bytes occupied


---

Summary

NumPy provides fast multi-dimensional arrays.

np.array() creates arrays.

zeros(), ones(), empty(), full() create initialized arrays.

arange() and linspace() generate sequences.

.ndim, .shape, .size, .dtype provide array information.


---
