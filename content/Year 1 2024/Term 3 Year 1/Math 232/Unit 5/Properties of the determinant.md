# Properties of the [[Determinant]]
- if A is transformed to R through the used of row operations, then det(A) is related to det(R)
- ### Scaling a row
	- ###### if B is obtained from A by multiplying a row by r, then det(B)=rdet(A)
		- (basically we can just reverse the scaling of matrices with determinant (determinant is proportional to the matrix ))
		- *if its like a 4x4 matrix with det(2A)* we must relise that *2A multiplies all entries by 2* $\therefore 2^{4}\det(A)$ .
- ### Row multiples
	- ###### If two rows of a matrix are *scalar multiplse* of another, then $\det=0$
- ### REF
	- ###### We can get the [[Determinant]] by reducing it to REF:
		- reduce a matrix (upper triangular)
			- then we can just get the product of the diagonal entries to get determinant
		- ###### We have to keep in mind the operations done to the matrix and the what the reverse is so we can do them bac to the original
			- (follow the row operations bacwards to get Det)


# Examples
- #### Using Upper triangular and the [[Properties of the determinant]]
	- ###### Find the determinant of 
$$
\begin{bmatrix}
1 & 1 & 1 \\
0 & 0 & 2 \\
0 & 3 & 4
\end{bmatrix}\implies\begin{bmatrix}
1 & 1 & 1 \\
0 & 3 & 4 \\
0 & 0 & 2
\end{bmatrix}
$$
- Now we can see that the matrix is uper triangular so the determinent is the products of the diagonal numbers 
	- $\det=1*3*2=6$
- #### Using REF to find 4x4 det
	- ###### find the determinant of
$$
\begin{align}
\begin{bmatrix}
0 & 1 & 2 & 2 \\
2 & 2 & 2 & 2 \\
1 & 2 & 5 & 5 \\
2 & 2 & 2 & 1
\end{bmatrix}\implies RREF\begin{bmatrix}
1 & 1 & 1 & 1 \\
0 & 1 & 2 & 2 \\
0 & 0 & 2 & 2 \\
0 & 0 & 0 & -1
\end{bmatrix} \\
Det(REF)=1*1*2*-1=-2 \\
Det(REF)*-1*2=Det(A) \\
Det(A)=4


\end{align}
$$
