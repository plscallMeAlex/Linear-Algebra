# 1. Transpose
Transpose of A is denoted as $A^{T}$ it use for swap rows and columns. 
$$
A=\begin{bmatrix}
1&2&3 \\
0&0&4
\end{bmatrix},then\ A^{T}=\begin{bmatrix}
1&0 \\
2&0 \\
3&4
\end{bmatrix}
$$
**Rules**
- The transpose of $A^{T}=A$
- $(A+B)^{T}=A^{T}+B^{T}$
- $(AB)^{T}=B^{T}A^{T}$ swap the position.
- $(A^{-1})^{T}=(A^{T})^{-1}$
- $L^{T}=U$
- $L^{-1}$ - Lower triangular.
- Can inverse the transpose or can transpose the inverse.
- $A^{T}$ is invertible when $A$ is invertible.
- When A movers from one side of a dot product to the other side it becomes $A^{T}$
**Formula**
$$
A=LDU
$$
D is the diagonal matrix (the pivot matrix) also $D=D^{T}$
## Example
The inverse of $A=\begin{bmatrix}1&0 \\ 6&1\end{bmatrix}$ is $A^{-1}=\begin{bmatrix}1&0 \\ -6&1\end{bmatrix}$
$(A^{-1})^{T}=(A^{T})^{-1}=\begin{bmatrix}1&-6 \\ 0&1\end{bmatrix}$

# 2. Symmetric Matrices
A symmetric matrix has this property $S^{T}=S$
- Also the inverse of symmetric matrix will be symmetric.
$$(S^{-1})^{T}=(S^{T})^{-1}=S^{-1}$$
## Example
Symmetric matrix and symmetric inverse
$$S=\begin{bmatrix}
1&2 \\
2&5
\end{bmatrix}=S^{T}$$
and
$$S^{-1}=\begin{bmatrix}
5&-2 \\
-2&1
\end{bmatrix}=(S^{-1})^{T}$$
## Symmetric Products
For any matrix A, the product $S=A^{T}A$ is symmetric.
$$S^{T}=S$$
$A^{T}A$ us symmetric but $A^{T}A\neq AA^{T}$ in general, but both are symmetric.
### Example
$Let A=\begin{bmatrix}1&2 \\ 3&4 \\ 5&6\end{bmatrix}$
- Find $A^{T}A$
$$A^{T}=\begin{bmatrix}
1&3&5 \\
2&4&6
\end{bmatrix}$$
Multiply $A^{T}\ by\ A$
$$
A^{T}A=\begin{bmatrix}
1&3&5 \\
2&4&6
\end{bmatrix}\begin{bmatrix}
1&2 \\
3&4 \\
5&6
\end{bmatrix}
$$
$$A^{T}A=\begin{bmatrix}
35&44 \\
44&56
\end{bmatrix}$$
- $A^{T}A$ is symmetric because $\begin{bmatrix}35&44 \\ 44&56\end{bmatrix}^{T}=\begin{bmatrix}35&44 \\ 44&56\end{bmatrix}$

Compare with $AA^{T}$
$$AA^{T}=\begin{bmatrix}
1&2 \\
3&4 \\
5&6
\end{bmatrix}
\begin{bmatrix}
1&3&5 \\
2&4&6
\end{bmatrix}
$$
- $AA^{T}$ is also symmetric, but it is a different matrix from $A^{T}A$
## Symmetric Elimination
The symmetric makes elimination faster because work only half the matrix (plus diagonal).
$$S=LDU$$
We add D into the normal formula $A=LU$ makes it symmetric.
### Example
Given $S=\begin{bmatrix}1&2 \\ 2&7\end{bmatrix}$, find $S=LU$ and $S=LDU$
$\begin{bmatrix}1&2 \\ 2&7\end{bmatrix}=\begin{bmatrix}1&0 \\ 2&1\end{bmatrix}\begin{bmatrix}1&2 \\ 0&3\end{bmatrix}$ LU misses the symmetry of S
$\begin{bmatrix}1&2 \\ 2&7\end{bmatrix}=\begin{bmatrix}1&0 \\ 2&1\end{bmatrix}\begin{bmatrix}1&0 \\ 0&3\end{bmatrix}\begin{bmatrix}1&2 \\ 0&1\end{bmatrix}$ $LDL^{T}$ captures the symmetry Now U is the $L^{T}$

### Rules
- If $S=S^{T}$ can be factored into $LDU$ with no row exchanges, then U is $L^{T}$
- The symmetric factorization of a symmetric matrix is $S=LDL^{T}$
- The transpose of $LDL^{T}$ is also $LDL^{T}\to$ will faster during elimination half of it. 

# 3. Permutation matrices
A permutation matrix P has the rows of the identity I in any order.
$P^{T}$ is also a permutation matrix it might be $P$ or different matrix.
## Example
There are six $3x 3$ permutation matrices.
$$
I=\begin{bmatrix}
1&& \\
&1& \\
&&1
\end{bmatrix} \ P_{21}=\begin{bmatrix}
&1& \\
1&& \\
&&1
\end{bmatrix}
\ P_{32}P_{21}=
\begin{bmatrix}
&1& \\
&&1 \\
1&&
\end{bmatrix}
$$
$$
P_{31}=\begin{bmatrix}
&&1 \\
&1& \\
1&&
\end{bmatrix}
\ P_{32}=\begin{bmatrix}
1&& \\
&&1 \\
&1&
\end{bmatrix}
\ P_{21}P_{32}=
\begin{bmatrix}
&1& \\
&&1 \\
1&&
\end{bmatrix}
$$Do from the right to the left. There are $n!$ permutation matrices of order n.
## Rules
- $P^{-1}$ is also a permutation matrix
- $P^{-1}$ is always the same as $P^{T}$
## Example
Given $P=\begin{bmatrix}0&1&0 \\ 0&0&1 \\ 1&0&0\end{bmatrix}$, find $P^{T},P^{-1}$ and $PP^{T}$
$P^{T}=\begin{bmatrix}0&0&1 \\ 1&0&0 \\ 0&1&0\end{bmatrix}$ and $P^{-1}=\begin{bmatrix}0&0&1 \\ 1&0&0 \\ 0&1&0\end{bmatrix}$
$PP^{T}=\begin{bmatrix}0&1&0 \\ 0&0&1 \\ 1&0&0\end{bmatrix}\begin{bmatrix}0&0&1 \\ 1&0&0 \\ 0&1&0\end{bmatrix}=\begin{bmatrix}1&0&0 \\ 0&1&0 \\ 0&0&1\end{bmatrix}=I$

# 4. The PA = LU Factorization
The ... factorization is a process in linear algebra that decomposes any **invertible matrix A**
into:
- P - A permutation matrix that rearranges rows to handle pivoting.
- L - A lower triangular matrix with ones on the diagonal.
- U - A upper triangular matrix.
This is the extension of $A=LU$ that have P accounting for row exchanges to ensure the stability during pivoting.
## Use for: 
- Handle the cases where A requires row exchanges for accurate factorization (zero or small pivot element)
- Compute determinants or inverses of matrices.
- Solve systems of linear equations efficiently.
## Example 1:
Let:
$$A=\begin{bmatrix}
0&1&2 \\
1&3&4 \\
2&7&6
\end{bmatrix}$$
1. Pivoting
- The first pivot element is 0 so swap rows 1 and 2:
$$P=\begin{bmatrix}
0&1&0 \\
1&0&0 \\
0&0&1
\end{bmatrix}$$
$$PA=\begin{bmatrix}
1&3&4 \\
0&1&2 \\
2&7&6
\end{bmatrix}$$
2. Perform Gaussian Elimination
- Eliminate PA to form U:
$$U=\begin{bmatrix}
1&3&4 \\
0&1&2 \\
0&0&-2
\end{bmatrix}$$
3. Find L
- The multipliers used during elimination are stored in L:
Final factorization:
$$PA=LU$$
## Example 2:
1. Solving Linear Systems:
- Solve $Ax=b$ using
$$PAx=Pb ,LUx=Pb$$
2. Matrix Inverses:
- Multiply P x A:
$$PxA=\begin{bmatrix}
0&0&1 \\
0&1&0 \\
1&0&0
\end{bmatrix}\ x 
\begin{bmatrix}
1&2&3 \\
0&1&4 \\
5&6&0
\end{bmatrix}=
\begin{bmatrix}
5&6&0 \\
0&1&4 \\
1&2&3
\end{bmatrix}
$$
3. Determinants:
- The determinant of A can be found from U:
$$\det(A)=(-1)^{k}\cdot \det(U)$$
where k is the number of row swaps in P.

# 5. Vector Spaces
# 6. Subspaces
