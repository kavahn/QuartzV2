##### 1(a) Generating Random Matrix and Vector to solve 
**Procedure:**
- A random (5 x 6) matrix (A) and a random (5 x 1) column vector  were generated using MATLAB.
- The augmented matrix was formed.
- The Reduced Row Echelon Form (RREF) of the augmented matrix was calculated to determine the solution set of the system.
**Results:** $$ \tiny A = \begin{bmatrix}
9 & 5 & 5 & 3 & 5 & 8 \\
7 & 4 & 5 & 7 & 10 & 3 \\
4 & 8 & 7 & 7 & 4 & 6 \\
1 & 2 & 8 & 2 & 3 & 9
\end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix}
10 \\
6 \\
2 \\
2 \\
3
\end{bmatrix} $$$$\tiny RREF(A|b) = \begin{bmatrix} 1 & 0 & 0 & 0 & 0 & 1.3629 & 2.6597 \\ 0 & 1 & 0 & 0 & 0 & -1.5508 & -2.9987 \\ 0 & 0 & 1 & 0 & 0 & 1.6848 & 1.0419 \\ 0 & 0 & 0 & 1 & 0 & 1.1110 & 2.4740 \\ 0 & 0 & 0 & 0 & 1 & -1.6538 & -2.3151 \end{bmatrix} $$ The solution set: $let,f=t$
$$\tiny \begin{bmatrix}a\\b\\c\\d\\e\\f
\end{bmatrix}=t\begin{bmatrix}
-1.3629 \\
1.5508 \\
-1.6848 \\
-1.1110 \\
1.6538 \\ 1
\end{bmatrix}+\begin{bmatrix} 2.6597 \\ -2.9987 \\ 1.0419 \\ 2.4740 \\ -2.3151\\0 \end{bmatrix} $$
---
##### 1(b) Textbook Question Section 2.1 B44
**Problem Statement:** A bookkeeper needs to determine the prices of armchairs, sofa beds, and double beds using the following information: $$\tiny \begin{cases} 20a + 10s + 8d = 15200 \\ 15a + 12s + 10d = 15700 \\ 12a + 20s + 10d = 19600 \end{cases} $$
**Procedure:**
- Define the coefficients matrix (A) and the constants vector .
- Form the augmented matrix.
- Calculate the RREF of the augmented matrix to solve for prices of armchair ((a)), sofa bed ((s)), and double bed ((d)).
**Results:** The RREF form of the provided matrix solution: 
$$ \tiny \begin{bmatrix}
1 & 0 & 0 & |300 \\
0 & 1 & 0 & |600 \\
0 & 0 & 1 & |400
\end{bmatrix} $$
Thus, the prices are:
- Armchair: ( $300 )
- Sofa Bed: ( $600 )
- Double Bed: ( $400 )
---
#### Section 2: Linear Transformations and Projections
##### 2(a) Projection of Vectors
**Procedure:**
- Define vectors $(\mathbf{x}_1), (\mathbf{x}_2), (\mathbf{x}_3),$ and the projection vector$(\mathbf{v})$.
- Calculate the projection matrix (P) for $(\mathbf{v})$.
- Use the projection matrix to project $(\mathbf{x}_1), (\mathbf{x}_2)$, and $(\mathbf{x}_3)$ onto $(\mathbf{v})$.
**Results:** $$ \tiny P(\mathbf{x}_1) = \begin{pmatrix} 1.0000 \\ 2.0000 \\ 3.0000 \end{pmatrix}, \quad P(\mathbf{x}_2) = \begin{pmatrix} 2.0000 \\ 4.0000 \\ 6.0000 \end{pmatrix}, \quad P(\mathbf{x}_3) = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix} $$
##### 2(b) Composition of Projection and Rotation
**Procedure:**
- Define the rotation matrix (R).
- Compute the composition matrices $([R \circ P])$ and $([P \circ R])$.
**Results:** 
$$ \tiny [R \circ P] = \begin{pmatrix} 0.1857 & 0.3714 & 0.5571 \\ 0.1429 & 0.2857 & 0.4286 \\ 0.1286 & 0.2571 & 0.3857 \end{pmatrix}, \quad [P \circ R] = \begin{pmatrix} -0.0714 & 0.1429 & 0.2143 \\ -0.1429 & 0.2857 & 0.4286 \\ -0.2143 & 0.4286 & 0.6429 \end{pmatrix} $$
---
#### Section 3: Basis and Linear Combinations
##### 3(a) Basis of Column Space
**Procedure:**
- Define matrix (A) using given column vectors.
- Calculate the RREF of (A) to determine which vectors form a basis.
**Results:** The RREF form of (A): $$ \tiny \begin{pmatrix} 1 & 0 & 5 & 0 & 2 \\ 0 & 1 & -2 & 0 & 1 \\ 0 & 0 & 0 & 1 & -7 \\ 0 & 0 & 0 & 0 & 0 \end{pmatrix} $$
Thus, the basis vectors for (S) are $([v1, v2, v4, v5])$ with dimension 3 and: $$ \tiny
Basis:\begin{bmatrix}
3 & 6 & 2 \\ 2 & 5 & 0\\-1 & 1 & -1
\end{bmatrix}
$$



