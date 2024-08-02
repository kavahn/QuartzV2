#### Question 1: Solving Systems of Linear Equations

**1(a)** Generate a random matrix $A$ and vector $b$, find the RREF and the solution set.

We generate a random 5x6 matrix $A$ and a random 5x1 vector $b$. The augmented matrix $[A|b]$ is then computed and its Reduced Row Echelon Form (RREF) is determined using MATLAB to find the solution set.

**1(b)** Answer textbook question Section 2.1 B44.

#### Question 2: Linear/Matrix Mappings and Projections

**2(a)** Project vectors onto $\mathbf{v} = (1, 2, 3)$.

The projection matrix $P$ is given by: $$ P = \frac{\mathbf{v} \mathbf{v}^T}{| \mathbf{v} |^2} $$ We compute the projections of $\mathbf{x}_1 = (3, 4, 1)$, $\mathbf{x}_2 = (2, 4, 6)$, and $\mathbf{x}_3 = (1, 1, -1)$ using MATLAB.

**2(b)** Composition of rotation and projection matrices.

Given the rotation matrix $R$: $$ R = \begin{bmatrix} 0.8 & 0 & 0.6 \ 0 & 1 & 0 \ -0.6 & 0 & 0.8 \end{bmatrix} $$ We calculate the composition matrices $RP$ (projection followed by rotation) and $PR$ (rotation followed by projection) using MATLAB.

#### Question 3: Basis from Column Space

**3(a)** Find the basis for the subspace $S = \text{span}{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3, \mathbf{v}_4, \mathbf{v}_5}$.

Given the vectors: $$ \mathbf{v}_1 = \begin{bmatrix} 3 \\ 2 \\ 0 \\ -1 \end{bmatrix}, \quad \mathbf{v}_2 = \begin{bmatrix} 6 \\ 5 \\ 2 \\ 1 \end{bmatrix}, \quad \mathbf{v}_3 = \begin{bmatrix} 3 \\ 0 \\ -4 \\ -7 \end{bmatrix}, \quad \mathbf{v}_4 = \begin{bmatrix} 2 \\ 0 \\ -1 \\ -1 \end{bmatrix}, \quad \mathbf{v}_5 = \begin{bmatrix} -2 \\ 9 \\ 9 \\ 6 \end{bmatrix} $$ We construct matrix $A$ using these vectors as columns and find its RREF to identify the basis vectors for subspace $S$.

**3(b)** Express non-basis vectors as a linear combination.

Using the RREF results from part (3a), we identify the non-basis vectors and express them as a linear combination of the basis vectors identified from the pivot columns in the RREF.