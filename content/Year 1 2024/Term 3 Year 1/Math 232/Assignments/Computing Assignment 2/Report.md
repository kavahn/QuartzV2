### 1 Rotation and Reflection of Vectors
**Procedure:**
- **Rotation:**
    - Start with the initial vector $( x_0 = \begin{bmatrix} 2 & 3 \end{bmatrix} ).$ 
    - Use a $(60^\circ)$ rotation matrix $( R = \begin{bmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & \frac{1}{2} \end{bmatrix} )$.
    - Compute successive vectors $( x_1, x_2, x_3, x_4, x_5 )$ using $( x_i = R \cdot x_{i-1} )$.
    - Plot the vectors using different colors.
- **Reflection:**
    - Reflect these vectors over the line ( y = 3x ) using the reflection matrix $( P = \begin{bmatrix} -0.8 & 0.6 \\ 0.6 & 0.8 \end{bmatrix} )$.
    - Compute the reflected vectors$[P]\vec{x}$ for ( i = 0, 1, 2, 3, 4, 5 ).
    - Plot the reflected vectors.
**Results:**
- ###### 1(a) **Plot of Rotated Vectors**:
    - ![[Report-20240704052919868.png|324]]
    - $\tiny x_{n}=\begin{bmatrix}  2.0000  & -1.5981  & -3.5981  & -2.000 1.5981  &  3.5981 \\3.0000  &  3.2321   & 0.2321  & -3.0000   -3.2321 &  -0.2321\end{bmatrix}$
- ###### 1(b) **Plot of Reflected Vectors**:
    - ![[Report-20240704053109336.png|357]]
    - $\tiny[P]x_{n}=\begin{bmatrix} 0.2000   & 3.2177  &  3.0177  & -0.2000  & -3.2177   &-3.0177 \\ 3.6000 &   1.6268   &-1.9732&   -3.6000  & -1.6268  &  1.9732 \end{bmatrix}$
    

---

### 2 Basis Transformation and Linear Mapping

**Problem Statement:** Given basis $( B = { v_1, v_2, v_3, v_4 } ): [ v_1 = \begin{bmatrix} 0 \ 1 \ 2 \ 1 \end{bmatrix}, \quad v_2 = \begin{bmatrix} 1 \ 5 \ 0 \ 1 \end{bmatrix}, \quad v_3 = \begin{bmatrix} 2 \ 3 \ 6 \ 4 \end{bmatrix}, \quad v_4 = \begin{bmatrix} 1 \ 3 \ -1 \ -1 \end{bmatrix} ]$
**Procedure:**
- Compute the basis transformation matrix ( P_{S \to B} ).
- Given the vector $( x = \begin{bmatrix} 1 \ 2 \ 3 \ 4 \end{bmatrix} )$, compute its representation in basis ( B ).
- Define the linear transformation: $[ L(x_1, x_2, x_3, x_4) = \begin{bmatrix} x_2 + 5x_4 \ x_1 - x_3 \ x_1 + x_2 + x_3 + x_4 \ 0 \end{bmatrix} ]$
- Compute the matrix representation of ( L ) in the basis ( B ) and use it to find $( (L(x))_B )$.

**Results:**

- **Transformation Matrix $( P_{S \to B} )$**: 
$$
\tiny PS\to B: \begin{bmatrix}
-1.1481  &  0.3704  &  0.6667  & -0.7037\\
   -0.2593 &  0.1481 &  -0.3333  &  0.5185\\
    0.4444  & -0.1111   & 0.0000   & 0.1111\\
    0.3704  &  0.0741  &  0.3333 &  -0.7407
\end{bmatrix}
$$
- **Coordinates of x in basis B:**
$$
\tiny x_{B}= \begin{bmatrix}
-1.2222\\
    1.1111\\
    0.6667\\
   -1.4444\\
\end{bmatrix}
$$
- **Matrix Representation of ( L ) in Basis ( B )**:
$$ \tiny L_{B}=\begin{bmatrix}
-4.9630 &  -6.4444 & -17.8889   & 4.3704\\
   -3.1852 &  -4.7778 & -11.5556  &  0.1481\\
    2.8889  &  4.3333 &  10.6667  & -1.1111\\
    3.4074   & 6.1111 &  13.2222  &  0.0741
\end{bmatrix}$$
- **Transformed Vector $( (L(x))_B )$**: 
$$
\tiny Lx_{b}= \begin{bmatrix}
-19.3333\\
   -9.3333\\
   10.0000\\
   11.3333\\
\end{bmatrix}
$$