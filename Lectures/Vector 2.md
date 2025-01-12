# 1. Combination of Vectors
Matrix  can be formed by combining vectors Assume the vectors
$$
u=\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix},
v=\begin{bmatrix}
4 \\
5 \\
6
\end{bmatrix}
$$
**Ex1:** A matrix A is the combining form of vector u and v:
$$
A=\begin{bmatrix}
1 \ \ 4 \\
2 \ \ 5 \\
3 \ \ 6 
\end{bmatrix}
$$

# 2. Matrices
A matrix is a rectangular array of numbers arranged in rows and columns.
## Matrix Identifier
- ### Matrix Times Vector:
	$A=\begin{bmatrix}1&0&0 \\ -1&1&0 \\ 0&-1&1\end{bmatrix}$
	$x=\begin{bmatrix}x_{1} \\ x_{2} \\ x_{3}\end{bmatrix}$
	$Ax=\begin{bmatrix}x_{1} \\ -x_{1}+x_{2} \\ -x_{2}+x_{3}\end{bmatrix}$
	**Ex1:**
	$A=\begin{bmatrix}1&0 \\ 0&1\end{bmatrix},$
	$x=\begin{bmatrix}3 \\ 5\end{bmatrix}$
	$Ax=\begin{bmatrix}3 \\ 5\end{bmatrix}$
This show the combination of columns or **dot products with rows**.
- ### Types of Matrices:
	- Identity Matrix:
		$I=\begin{bmatrix}1&0&0 \\ 0&1&0 \\ 0&0&1 \end{bmatrix}$

# 3. Solving Linear Equations
Equation will represented as this format $Ax=b$
**Example:**
$x+2y+3z=6$
$2x+5y+2z=4$
$6x-3y+z=2$
To solving using the technique called **elimination or matrix inversion**.
**Ex1:**
$x+2y=5$
$2x-3y=-1$
Represent as $A=\begin{bmatrix}1&2 \\ 2&-3\end{bmatrix},b=\begin{bmatrix}5 \\ -1\end{bmatrix}$ . Solve for x.
$Ax=b$

# 4. Vectors & Linear Equations
## Linear Combination 
using vectors to form new vectors.
Example:
$$
x_{1}\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix}+
x_{2}\begin{bmatrix}
-1 \\
1 \\
0
\end{bmatrix}
+x_{3}\begin{bmatrix}
0 \\
-1 \\
1
\end{bmatrix}
=b
$$
## Independence
If no vector in a set is a linear combination of the others. Describes a set of vectors in a vector space where no vector can be written as a linear combination of the others.
### Linearly independent
If a set of vectors is linearly independent, it means they contribute unique information to the space and do not overlap in terms of direction or magnitude.
### Example 1
$$c_{1}v_{1}$+c_{2}v_{2}+\dots+c_{n}v_{n}$$
is:
$$c_{1}=c_{2}=\dots=c_{n}=0$$
Where:
- $c_{1},c_{2},\dots,c_{n}$ are scalar coefficients.
- 0 is the zero vector.
If there exists any non-zero $c_{i}$ that satisfies the equation, the vectors are linearly dependent.
### Example 2
**Linearly Independent Vectors:**
$$v_{1}=\begin{bmatrix}
1 \\
0
\end{bmatrix},v_{2}=\begin{bmatrix}
0 \\
1
\end{bmatrix}$$
In 2D space, these vectors are the standard basis vectors.
$c_{1}v_{1}+c_{2}v_{2}=0\implies c_{1}=0 \cap c_{2}=0$
**Linearly Dependent Vectors**
$$v_{1}=\begin{bmatrix}
1 \\
2
\end{bmatrix}
,v_{2}=\begin{bmatrix}
2 \\
4
\end{bmatrix}$$
Here, $v_{2}=2v_{1}$, so they are linearly dependent.
The equation $c_{1}v_{1}+c_{2}v_{2}=0$ has non-trivial solutions like $c_{1}=2,c_{2}=-1$
### Summary
- A set of vectors is linearly independent if the only solution to $c_{1}v_{1}+c_{2}v_{2}+\dots+c_{n}v_{n}=0$ is $c_{1}=c_{2}=\dots=c_{n}=0$
- If any non-zero values of $c_{1},c_{2},c_{3},\dots,c_{n}$ make the equation true, then the vectors are linearly dependent.
#### In-short
- Independent - Only c = 0 works.
- Dependent - Non-zero c also works.

# 5. Idea of Elimination
To simplify the system of equations to find solutions.
**Process:**
convert the system into an upper triangular matrix.
**Back Substitution:**
Solve the simplified system starting from the last equation.
**Examples:**
$x-2y=1$
$3x+2y=11$
After elimination: $y=1,x=3$

# 6. Breakdowns in Elimination
There will have 2 conditions that might occur during the elimination.
- **No Solution:**
	$x-2y=1$
	$3x-6y=11\to Parallel \ lines$
- **Infinite Solutions**
	$x-2y=1$
	$3x-6y=3\to Same \ line$
