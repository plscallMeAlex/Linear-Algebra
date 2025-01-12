# 1. Inverse Matrices
A matrix A is invertible if we can find the $A^{2}$ such that

$A\cdot A^{-1}=I$ and $A^{-1}\cdot A=I$

and I is the Identity Matrix.

## Pivot
A pivot is the first non-zero element in a row of a matrix that has been transformed into row echelon or reduced row echelon form.
$$
A=\begin{bmatrix}
**1**&0&0 \\
0&**1**&0 \\
0&0&**1**
\end{bmatrix}
$$

## The invertible matrices
- We can find the inverse of matrix if and only if elimination produces n pivots
- matrix A cannot have two different inverse $\to$ If BA = I and CA = I, then B = C
- If A invertible then $Ax=b$ solving by $x=A^{-1}b$
- Suppose there is a nonzero vector x (x,y,z,... have the answer) such that $Ax=0\to A$ not invertible. Because no matrix bring the zero back.
- If the above A is invertible, then $Ax=0$  then x = 0 so there have no solution for solving.
**Formula** to find the inverse of 2x2 matrix is:
$$
\begin{bmatrix}
a&b \\
c&d
\end{bmatrix}^{-1}
=\frac{1}{ad-bc}\begin{bmatrix}
d&-b \\
-c&a
\end{bmatrix}=
\frac{1}{\det A}\begin{bmatrix}
d&-b \\
-c&a
\end{bmatrix}
$$
**Note:**
- The $ad-bc$ is det A.
- Its invertible if and only if $ad-bc$ is not zero.
- If $A=\begin{bmatrix}d_{1}&&& \\ &\dots \\ &&&dn \end{bmatrix}$ then $A^{-1}=\begin{bmatrix}\frac{1}{d_{1}}&&& \\ &\dots \\ &&& \frac{1}{dn} \end{bmatrix}$

# 2. The Inverse of a Product
If A and B are invertible matrices, their product AB is also invertible. The inverse is given by:
$$(AB)^{-1}=B^{-1}\cdot A^{-1}$$
**Example:**
Let $A=\begin{bmatrix}2&0 \\ 0&3\end{bmatrix}$ and $B=\begin{bmatrix}4&1 \\ 2&5\end{bmatrix}$. The inverse of AB requires first computing the $B^{-1}$ and $A^{-1}$, after that multiplying $B^{-1}\cdot A^{-1}$
**As you can see the order must be reverse.**

**Ex1:**
Inverse of an elimination matrix If an Elimination Matrix E subtracts 5 times row 2, then $E^{-1}$ adds 5 times row 1 from row 2.
$$E=\begin{bmatrix}
1&0&0 \\
-5&1&0 \\
0&0&1
\end{bmatrix},E^{-1}=\begin{bmatrix}
1&0&0 \\
5&1&0 \\
0&0&1
\end{bmatrix}$$

# 3. Calculating $A^{-1}$ Using Gauss-Jordan Elimination
**Steps:**
1. Combine A with I to form an augmented matrix \[A | I].
2. Apply row operations to transform A into I. The operations on I result in $A^{-1}$

Multiply \[A I] by $A^{-1}$ to get \[I $A^{-1}$]
**In short is making the A to I.**
## Symmetric Matrices
A matrix A is symmetric if it equals its transpose (change rows to columns and columns to rows):
$$A=A^{T}$$
**Example:**
$$A=\begin{bmatrix}
2&3&4 \\
3&5&6 \\
4&6&7 \\
\end{bmatrix}$$
Here, $A^{T}=A$, so A is symmetric.
## Tridiagonal Matrices
A tridiagonal matrix is a square matrix where nonzero entries. In short is have 3 diagonal line in the matrix.
**Example:**
$$T=\begin{bmatrix}
2&-1&0 \\
-1&2&-1 \\
0&-1&2
\end{bmatrix}$$
This tridiagonal matrix is also symmetric.
## Product of Pivots
The product of pivots is the determinant of the matrix in triangular form (upper or lower triangular matrix).
- During Gaussian Elimination, the diagonal entries of the resulting triangular matrix are the pivots.
- The det of the matrix is the product of these pivots.
**Properties:**
- If any pivot is zero, the det is zero, and the matrix is singular (non-invertible).
**Example:**
Consider $A=\begin{bmatrix}2&1 \\ 4&3\end{bmatrix}$
Gaussian elimination produces $U=\begin{bmatrix}2&1 \\ 0&1\end{bmatrix}$
Pivots: 2, 1
Det(A)=$2\cdot1=2$
## Combined Example: Symmetric, Tridiagonal Matrix and Pivots
Let K be a symmetric, tridiagonal matrix:
$$K=\begin{bmatrix}
2&-1&0 \\
-1&2&-1 \\
0&-1&2
\end{bmatrix}$$
- $K=K^{T}$
- Tridiagonal because it no zero in the diagonal zone.
- Pivots
	Eliminate below the main diagonal:
	- Subtract $-\frac{1}{2}$ of row 1 from row 2.
	- Subtract $-\frac{1}{2}$ of row 2 from row 3.
	Pivots: $2, \frac{3}{2}, \frac{4}{3}$
	Determinant: $2\cdot \frac{3}{2} \cdot \frac{4}{3}=4$
	
**Example:**
$A=\begin{bmatrix}2&1 \\ 3&4\end{bmatrix}$, solve \[A | I]:
$$\begin{bmatrix}
2&1&1&0 \\
3&4&0&1
\end{bmatrix}$$
Perform elimination to get $\begin{bmatrix}1&0&\dots \\ 0&1&\dots\end{bmatrix}$

# 4. Elimination and Factorization (A=LU)
Factorize A into:
- L - Lower triangular matrix $A=\begin{bmatrix}1&0 \\ 4&5\end{bmatrix},B=\begin{bmatrix}1&0&0 \\ 4&5&0 \\ 7&8&9\end{bmatrix}$
- U - Upper triangular matrix $A=\begin{bmatrix}1&2 \\ 0&4\end{bmatrix}, B=\begin{bmatrix}1&2&3 \\ 0&5&6 \\ 0&0&9\end{bmatrix}$
**Process:**
- Forward elimination transform A to U by multiplies by a matrix $E_{ij}$ to produce zero in the (i, j) position.
- Backward substitution involves L to revert to the original system.
If A is 3 x 3, we multiply by $E_{21},E_{31},E_{32}$ it will produce 0 in the position (2, 1), (3, 1), (3, 2) positions to get the upper triangular U.
**Tricks:**
We can move to another side to make a new equation.
$$
(E_{32},E_{31},E_{21})A=U \to A=(E_{21}^{-1}E^{-1}_{31}E^{-1}_{32})U
$$
After we inverse to opposite side and order we will get the product of 3 inverses is L by the formula.
$$A=LU$$
## $l_{ij}$
$l_{ij}$ is the multiplier value used to eliminate the element in the i-th row and j-th column of a matrix during the elimination  process. It is calculated as:
$$l_{ij}=\frac{a_{ij}}{a_{jj}}$$
Where:
- $a_{ij}$ - The element being eliminated.
- $a_{jj}$ - The pivot element (on the diagonal)
**Example:**
Consider the matrix A:
$$A=\begin{bmatrix}
2&1&-1 \\
-3&-1&2 \\
-2&1&2
\end{bmatrix}$$
**Steps:**
1. Eliminate the first column below the pivot ($a_{11}=2$)
	For row 2 (i=2):
	$$l_{21}=\frac{-3}{2}$$
	Update row 2:
	$$R_{2}\to R_{2}-l_{21}R_{1}=\begin{bmatrix}
-3&-1&2
\end{bmatrix}-\frac{-3}{2}\begin{bmatrix}
2&1&-1
\end{bmatrix}$$
	Update row 3:
	$$R_{3}\to R_{3}-l_{31}R_{1}$$
**Resulting Matrix:**
After eliminating the first column, the matrix becomes:
$$
\begin{bmatrix}
2&1&-1 \\
0&0.5&0.5 \\
0&2&1
\end{bmatrix}
$$
The multipliers $l_{21}=-1.5$ and $l_{31}=-1$ were used to perform these operations.
### Connection to L in LU Decomposition
In **LU decomposition,** the lower triangular matrix L contains the multipliers $l_{ij}$. For the above example, L would be:
$$L=\begin{bmatrix}
1&0&0 \\
-1.5&1&0 \\
-1&2&1
\end{bmatrix}$$
- $l_{21}=-1.5$ Multiplier used to eliminate the first element in row 2.
- $l_{31}=-1.5$ Multiplier used to eliminate the first element in row 3.
**Properties of Multipliers**
1. We store multiplier inside the L below the diagonal.
2. The diagonal of L (Lower triangular) always contain 1s.
3. Multiplier don't change when applying Gaussian elimination without row exchanges. 

## Example:
For $A=\begin{bmatrix}2&1 \\ 6&8\end{bmatrix}$
1. Eliminate 6 using row operations.
2. Result in $L=\begin{bmatrix}1&0 \\ 3&1\end{bmatrix},U=\begin{bmatrix}2&1 \\ 0&5\end{bmatrix}$
So $A=LU$

# 5. Singular v. Invertible Matrices
## A matrix is invertible (nonsingular) if:
- All rows/columns are independent (no zero rows/columns or called $\det(A)\neq 0$
- The matrix has a full rank.
- The determinant of the matrix is 0: $\det(A)\neq 0$
- The rows and columns are linearly independent.
**Ex:**
$$A=\begin{bmatrix}
1&2 \\
3&4
\end{bmatrix}$$
- The rows \[1, 2] and \[3, 4] are linearly independent.
- $\det(A)=1\cdot4-2\cdot 3=-2\neq0$, so A is invertible.
## A matrix is Singular (does not have an inverse) if:
- The determinant of the matrix is 0: $\det(A)=0$
- The rows or columns of the matrix are linearly dependent (some rows or columns can be expressed as linear combinations of others).
- The matrix does not have a full rank (more on this below).
**Ex:**
$$A=\begin{bmatrix}
1&2 \\
2&4
\end{bmatrix}$$
- The second row (\[2, 4]) is a multiple of the first row (\[1, 2])
- $\det(A)=1\cdot 4-2\cdot 2=0$, so A is singular.

# 6. Cost of Elimination
- Computational Time:
	For $n*n$ matrices, the cost of Gaussian elimination is proportional to $n^{3}$
- Efficiency:
	Sparse matrices (with many zero entries) reduce computational cost significantly.