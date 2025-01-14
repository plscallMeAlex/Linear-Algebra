-  Compute $A^{T}$, given $A=\begin{bmatrix}2&3&4 \\ 6&1&6 \\ 0&-6&-5\end{bmatrix}$
	$A^{T}=\begin{bmatrix}2&6&0 \\ 3&1&-6 \\ 4&6&-5\end{bmatrix}$
- For 3x3 matrices, what is the permutation matrix to exchanges rows 2 and 1, then rows3 and 1?
	$P_{21}=\begin{bmatrix} 0&1&0 \\ 1&0&0 \\0&0&1\end{bmatrix}$
- Compute $A^{6} \ when \ A=\begin{bmatrix}1&9 \\ 0&1\end{bmatrix}$ 
	$A^{2}=\begin{bmatrix}1&18 \\ 0&1\end{bmatrix}$
	$A^{3}=\begin{bmatrix}1&27 \\ 0&1 \end{bmatrix}$
	$A^{6}=A^{3}A^{3}=\begin{bmatrix}1&54 \\ 0&1\end{bmatrix}$
- Given $A=\begin{bmatrix}3&3 \\ 8&2\end{bmatrix}$ find the upper triangular **matrix U** for the LU factorization of A.
	$U=\begin{bmatrix} E_{21}A\end{bmatrix}=\begin{bmatrix}3&3 \\ 0&-6\end{bmatrix}$
- Find the determinant of A
	$\det(A)=\begin{bmatrix}3&7 \\ 7&4\end{bmatrix}=12-49$
	$\det(A)=-37$
- Given $A=\begin{bmatrix}5&1 \\ 5&7\end{bmatrix}$ find the lower triangular matrix L for the LU factorization of A.
	Finding the Upper first $U=\begin{bmatrix}5&1 \\ 0&6\end{bmatrix}$
	Finding the Lower first $L=\begin{bmatrix}1&0 \\ 1&1\end{bmatrix}$
- Compute $PA=\begin{bmatrix}0&1&0 \\ 0&0&1 \\ 1&0&0\end{bmatrix}\begin{bmatrix}9&9&5 \\ -4&0&3 \\ -5&4&5\end{bmatrix}$
	$PA=\begin{bmatrix}-5&4&5 \\ 9&9&5 \\ -4&0&3\end{bmatrix}$
- Find the angle $\theta$ (in degree) between these two vectors $u=\begin{bmatrix}6 \\ 3 \\ 4\end{bmatrix},v=\begin{bmatrix}8 \\ 5 \\ 10\end{bmatrix}$
	$\cos \theta=\frac{u\cdot v}{||u||||v||}=\frac{48+15+40}{\sqrt{ 36+9+16 }\sqrt{ 64+25+100 }}=\frac{103}{\sqrt{ 61 }\sqrt{ 189 }}=0.959=\theta=16.0..^{o}$
- What is the inverse of $A=\begin{bmatrix}0&1&0 \\ 0&0&1 \\ 1&0&0\end{bmatrix}$
	From the property of Permutation matrix
	$P^{T}=P^{-1}$
	finding $A^{T}=\begin{bmatrix}0&0&1 \\ 1&0&0 \\ 0&1&0\end{bmatrix}$
	$A^{T}=A^{-1}$
- Find the length of the vector $v=\begin{bmatrix} 4 \\ 8 \\ 1\end{bmatrix}$.
	$||v||=\sqrt{ 16+64+1 }=\sqrt{ 81 }=9$
- What is inverse of $A=\begin{bmatrix}1&0&0 \\ 0&1&0 \\ 0&-4&1\end{bmatrix}$
	$A^{-1}=$