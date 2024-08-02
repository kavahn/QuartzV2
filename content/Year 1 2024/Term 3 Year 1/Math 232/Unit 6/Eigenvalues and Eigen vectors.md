# What are Eigenvalues and eigen vectors
- Recall in the (not yet noted) the standard matrix for the reflection about the line y =2x: 
$$
\begin{bmatrix}
L
\end{bmatrix}=\begin{bmatrix}
-\frac{3}{5}& \frac{4}{5}\\ \frac{4}{5} & \frac{3}{5}
\end{bmatrix}
$$
- And when we scale a vector by this the vector it self changes
- #### An eigenvalue/vector is a matrix that was part of the original matrix that stays the same after the transformation 
	- ###### let A be an nxn matrix. if there exists a nonzero vector $\vec{v} \in \mathbb{R}^n$ such that $A\vec{v}=\lambda \vec{v}$ for some $\lambda \in \mathbb{R}$ 
		- we say $\lambda$ is an eigen value of A and $\vec{v}$ is an eigenvector of A corresponding to $\lambda$ 

# How to find eigenvalues and eigenvectors
- ### Eigenvalues
	- Suppose $\vec{v}$ is a nonzero vector such that $A\vec{v}=\lambda \vec{v}$ then 
		- $\small A\vec{v}=\lambda \vec{v}=(\lambda I_{n})\vec{v}\implies A\vec{v}-(\lambda I_{n})\vec{v}=0\implies(A-\lambda I_{n})\vec{v}=\vec{0}$
			- that is, $\vec{v}$ is a nontrivial solution to $(A-\lambda I)\vec{x}=\vec{0}$
				- for $\vec{v}$ to be non zero it $(A-\lambda I)$ [[Determinant]] needs to be non zero
- ### Eigenvectors
	- once we got the eigenvalues of A are found, we can find all eigen vectors (the vectors that dont change under the transformation) by solving $(A-\lambda I)\vec{x}=\vec{0}$
		- so on the diagonals you would remove $\lambda$ and find the resulting matrix (like finding the linear combination for the zero vector)


- ### Characteristic polynomial!
	- the eigen polynomail of the vector (remember)