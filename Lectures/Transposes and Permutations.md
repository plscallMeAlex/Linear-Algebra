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
