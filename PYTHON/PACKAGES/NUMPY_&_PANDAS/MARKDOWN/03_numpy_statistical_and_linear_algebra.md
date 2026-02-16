📄 03_numpy_statistical_and_linear_algebra.md

# NumPy Statistical Functions and Linear Algebra

This section covers statistical functions and basic linear algebra operations.

---

# 1. Statistical Functions

## 1.1 Mean

```python
import numpy as np

n = np.array([10, 20, 30, 40])
print(np.mean(n))

Output:

25.0


---

1.2 Median

print(np.median(n))

Output:

25.0


---

1.3 Standard Deviation

print(np.std(n))

Output:

11.180339887498949


---

1.4 Variance

print(np.var(n))

Output:

125.0


---

1.5 Sum

print(np.sum(n))

Output:

100


---

1.6 Minimum and Maximum

print(np.min(n))
print(np.max(n))

Output:

10
40


---

1.7 Axis Based Operations (2D)

n1 = np.array([[1, 2, 3],
               [4, 5, 6]])

print(np.sum(n1, axis=0))  # column wise
print(np.sum(n1, axis=1))  # row wise

Output:

[5 7 9]
[ 6 15]


---

2. Linear Algebra Operations

NumPy provides linear algebra functions in numpy.linalg


---

2.1 Matrix Addition

a = np.array([[1, 2],
              [3, 4]])

b = np.array([[5, 6],
              [7, 8]])

print(a + b)

Output:

[[ 6  8]
 [10 12]]


---

2.2 Matrix Multiplication

Using dot()

print(np.dot(a, b))

Output:

[[19 22]
 [43 50]]

Using @ operator:

print(a @ b)


---

2.3 Transpose of Matrix

print(a.T)

Output:

[[1 3]
 [2 4]]


---

2.4 Determinant

print(np.linalg.det(a))

Output:

-2.0


---

2.5 Inverse of Matrix

print(np.linalg.inv(a))

Output:

[[-2.   1. ]
 [ 1.5 -0.5]]


---

2.6 Eigenvalues and Eigenvectors

values, vectors = np.linalg.eig(a)
print(values)
print(vectors)

Output:

[-0.37228132  5.37228132]
[[ -0.82456484 -0.41597356]
 [  0.56576746 -0.90937671]]


---

3. Broadcasting

NumPy automatically expands smaller array to match larger array shape.

n2 = np.array([[1, 2, 3],
               [4, 5, 6]])

n3 = np.array([10, 20, 30])

print(n2 + n3)

Output:

[[11 22 33]
 [14 25 36]]


---

Summary

Statistical functions: mean, median, std, var, sum, min, max.

Axis parameter controls row-wise or column-wise operation.

Linear algebra functions are in numpy.linalg.

dot() or @ is used for matrix multiplication.

Broadcasting allows operations on arrays of different shapes.


---
