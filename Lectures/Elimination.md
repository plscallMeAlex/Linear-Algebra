# 1. Elimination Using Matrices
Following this formula $Ax=b$ to solve the system of linear equations using row operations to reduce A to a simpler form
**Example:**
$2x_{1}+4x_{2}-2x_{3}=2$
$4x_{1}+9x_{2}-3x_{2}=8$
$-2x_{1}-3x_{2}+7x_{3}=10$
Represented as:
$$
A=\begin{bmatrix}
2&4&-2 \\
4&9&-3 \\
-2&-3&7
\end{bmatrix}
, b=\begin{bmatrix}
2 \\
8 \\
10
\end{bmatrix}
$$

# 2. Matrix Multiplication
Combining elimination steps can be expressed as matrix multiplication.
$$AB_{ij}=(row\ i \ of \ A)\cdot(column \ j \ of \ B)$$
## Properties:
- Associative: A(BC) = (AB)C
- AB $\neq$BA
**Example:**
$$
A=\begin{bmatrix}
1&1 \\
2&-1
\end{bmatrix}
, B=\begin{bmatrix}
2&2 \\
3&4
\end{bmatrix}
$$
Result
$$
AB=\begin{bmatrix}
1\cdot 2+1\cdot 3&1\cdot 2+1\cdot 4 \\
2\cdot2 - 1\cdot3& 2\cdot2-1\cdot 4
\end{bmatrix}
=\begin{bmatrix}
5&6 \\
1&0
\end{bmatrix}
$$

# 3. Rules for Matrix Operations
Addition and Scalar Multiplication Rules must following this:
- Have the same dimension to add (or subtract)
- Scalar multiplication must applies the scalar to all element.
**Example:**
For $A=\begin{bmatrix}1&2 \\ 3&4\end{bmatrix},2A=\begin{bmatrix}2&4 \\ 6&8\end{bmatrix}$

# 4. The Augmented Matrix
Is the combined between 2 matrices for example A and b into one matrix \[Ab] for simultaneous row operations.
**Example:**
$x+2y+2z=1$
$4x+8y+9z=3$
$3y+3z=1$
Augmented matrix:
$$
[Ab]=\begin{bmatrix}
1&2&2&1 \\
4&8&9&3 \\
0&3&2&1
\end{bmatrix}
$$

# 5. Matrix $P_{ij}$ for Row Exchange
A permutation matrix $P_{ij}$ swaps rows i and j.
**Example:**
$P_{23}=\begin{bmatrix}1&0&0 \\ 0&0&1 \\ 0&1&0\end{bmatrix}$

# 6. Block Matrices
Matrices can be divided into smaller blocks for simplified operations . (Like a Divide and Conquer)
Use for Elimination, Augmentation, or even multiplication on blocks instead of individual elements.
**Example:**
$$A=\begin{bmatrix}
A_{11}&A_{12} \\
A_{21}&A_{22}
\end{bmatrix}
B=\begin{bmatrix}
B_{11} \\
B_{21}
\end{bmatrix}
$$
Result
$$AB=\begin{bmatrix}
A_{11}B_{11}+A_{12}B_{21} \\
A_{21}B_{11}+A_{22}B_{21}
\end{bmatrix}$$
