📄 02_numpy_operations_and_manipulation.md

# NumPy Operations and Array Manipulation

This document covers indexing, slicing, reshaping, sorting, stacking, splitting, copying, mathematical operations, and random numbers.

---

# 1. Indexing

## 1.1 One Dimensional Indexing

```python
import numpy as np

n = np.array([3, 4, 5, 2])
print(n[0])

Output:

3


---

1.2 Two Dimensional Indexing

n1 = np.array([[1, 2, 3],
               [4, 5, 6]])

print(n1[0, 1])

Output:

2


---

2. Slicing

2.1 1D Slicing

n2 = np.array([0, 1, 2, 3, 4, 5])
print(n2[1:4])

Output:

[1 2 3]


---

2.2 2D Slicing

n3 = np.array([[1, 2, 3],
               [4, 5, 6]])

print(n3[0:2, 1:3])

Output:

[[2 3]
 [5 6]]


---

3. Boolean Indexing

n4 = np.arange(10)
print(n4[n4 < 5])

Output:

[0 1 2 3 4]

Using multiple conditions:

print(n4[(n4 > 3) & (n4 < 8)])

Output:

[4 5 6 7]


---

4. Reshaping Array

n5 = np.arange(8)
n6 = n5.reshape(4, 2)
print(n6)

Output:

[[0 1]
 [2 3]
 [4 5]
 [6 7]]


---

5. Adding New Axis

Convert 1D to 2D (row):

n7 = np.arange(8)
n8 = n7[np.newaxis, :]
print(n8.shape)

Output:

(1, 8)

Convert 1D to 2D (column):

n9 = n7[:, np.newaxis]
print(n9.shape)

Output:

(8, 1)


---

6. Sorting Arrays

6.1 1D Sorting

n10 = np.array([3, 2, 1, 9, 5, 10, 8])
print(np.sort(n10))

Output:

[ 1  2  3  5  8  9 10]


---

6.2 2D Sorting (Row-wise)

n11 = np.array([[3, 1],
                [4, 2]])

print(np.sort(n11))

Output:

[[1 3]
 [2 4]]

Column-wise sorting:

print(np.sort(n11, axis=0))


---

7. Joining Arrays

7.1 Concatenate

a = np.arange(4)
b = np.arange(5, 9)

c = np.concatenate((a, b))
print(c)

Output:

[0 1 2 3 5 6 7 8]


---

7.2 Horizontal Stack

n12 = np.array([[1, 2],
                [3, 4]])

n13 = np.array([[5, 6],
                [7, 8]])

print(np.hstack((n12, n13)))

Output:

[[1 2 5 6]
 [3 4 7 8]]


---

7.3 Vertical Stack

print(np.vstack((n12, n13)))

Output:

[[1 2]
 [3 4]
 [5 6]
 [7 8]]


---

8. Splitting Arrays

n14 = np.arange(20)
print(np.split(n14, 4))

Output:

[array([0, 1, 2, 3, 4]),
 array([5, 6, 7, 8, 9]),
 array([10, 11, 12, 13, 14]),
 array([15, 16, 17, 18, 19])]


---

9. Copying Arrays

9.1 Shallow Copy

n15 = np.array([1, 2, 3])
n16 = n15

n15[0] = 100
print(n16)

Output:

[100   2   3]

(Changes affect both arrays)


---

9.2 Deep Copy

n17 = np.array([1, 2, 3])
n18 = n17.copy()

n17[0] = 200
print(n18)

Output:

[1 2 3]

(Original array remains unchanged)


---

10. Mathematical Operations

n19 = np.array([[1, 2],
                [3, 4]])

n20 = np.array([[5, 6],
                [7, 8]])

print(n19 + n20)

Output:

[[ 6  8]
 [10 12]]

Element-wise multiplication:

print(n20 * n20)

Output:

[[25 36]
 [49 64]]


---

Aggregation

print(n20.sum())
print(n20.max())
print(n20.min())


---

11. Random Numbers

11.1 Random Float Values

print(np.random.rand(3, 3))

Output: (3x3 array with values between 0 and 1)


---

11.2 Random Integers

print(np.random.randint(0, 20, size=(4, 2)))

Output:

[[ 1  8]
 [11  4]
 [12  8]
 [ 0  9]]


---

Summary

Indexing and slicing allow element access.

Boolean indexing filters data.

reshape() changes dimensions.

concatenate(), hstack(), vstack() join arrays.

split() divides arrays.

.copy() creates deep copy.

NumPy supports element-wise operations.

random.rand() and random.randint() generate random numbers.


---
