# 1. Introduction Vectors
Vectors 2D represent as:
$$
v=
\begin{bmatrix}
v_{1} \\
v_{2}
\end{bmatrix}
$$
Vector 3D:
$$
v=
\begin{bmatrix}
v_{1} \\
v_{2} \\
v_{3}
\end{bmatrix}
$$
## Finding length
to finding the length (magnitude) of the vector by these following formula.
$$
||v||=\sqrt{v^{2}_{1}+v^{2}_{2}}
$$
**Ex1:**
If $v=\begin{bmatrix} 3 \\ 4 \end{bmatrix}$ , its magnitude (length) can be found as:
$$
||v||=\sqrt{3^{2}+4^{2}}=\sqrt{9+16}=5
$$

# 2. Vectors and Linear Combinations
We can scaling the vector by using the constant make it more larger.
$$
Linear \ combination:\ cv+dw=c\cdot
\begin{bmatrix}
v_{1} \\ v_{2}
\end{bmatrix}
+d\cdot
\begin{bmatrix}
w_{1} \\ w_{2}
\end{bmatrix}
$$
**Ex1:**
If $v=\begin{bmatrix}1\\1\end{bmatrix}$ and $w=\begin{bmatrix}2 \\ 3\end{bmatrix}$
For $c=2\cap d=3$
$$
cv+dw=2\cdot \begin{bmatrix}
1 \\
1
\end{bmatrix}
+
3\cdot
\begin{bmatrix}
2 \\
3
\end{bmatrix}
=
\begin{bmatrix}
2 \\
2
\end{bmatrix}
+
\begin{bmatrix}
6 \\
9
\end{bmatrix}
=
\begin{bmatrix}
8 \\
11
\end{bmatrix}
$$

# 3. Lengths and Dot Products
The length of of vector is magnitude and the dot product is an operation that combines two vectors to give a scalar value.
**The length formula**
$$
||v||=\sqrt{ v_{1}^{2}+v^{2}_{2}+\dots+v^{2}_{n}}
$$
**The dot product formula**
$$
v\cdot w=v_{1}\cdot w_{1} +v_{2} \cdot w_{2} +\dots+v_{n}\cdot w_{n}
$$
## Key Point:
- If $v\cdot w=0$, the vector are perpendicular

**Ex1:**
Let v = (1,2) and w = (3,4)
Dot product
$$
v\cdot w=1\cdot 3 +2\cdot 4=3+8=11
$$

# 4. Angles Between Vectors
The angle $\theta$ between two vectors v and w is determined using the dot product.
**Angle formula:**
$$
\cos \theta=\frac{v\cdot w}{(||v||||w||)}
$$
## Key Point:
- If $\cos \theta=0$, the vector are perpendicular ($\theta=90$).
- The Schwarz Inequality ensures that: $|v\cdot w|\leq||v||||w||$

**Ex1:**
Let $v=\begin{bmatrix}1 \\ 3\end{bmatrix}$ and $w=\begin{bmatrix}3 \\ 1\end{bmatrix}$
Find $\cos \theta$
1. $v\cdot w=1\cdot 3+3\cdot 1=6$
2. $||v||=\sqrt{ 1^{2}+3^{2} }=\sqrt{ 10 }$
3. $||w||=\sqrt{ 3^{2}+1^{2} }=\sqrt{ 10 }$
4. $\cos \theta=\frac{6}{(\sqrt{ 10 }\cdot \sqrt{ 10 })}=\frac{6}{10}=0.6$
Thus that $\theta=\cos^{-1}(0.6)$

# 5. Unit Vector
A unit vector has length of 1 and points in the same direction as a given vector.
**Unit Vector formula:**
$$
u=\frac{v}{||v||}
$$
**Ex1:**
Let $v=(3,4)$
1. Find $||v||=\sqrt{ 3^{2}+4^{2} }=5$
2. Unit Vector $u=\frac{1}{5} \begin{bmatrix}3 \\ 4\end{bmatrix}=\begin{bmatrix}0.6 \\ 0.8\end{bmatrix}$
