### 1 Eigenvalues and Eigenvectors using the Power Method
**Procedure:**
- **Initial Vector:**
    - Start with the initial vector $( x_{0} = \begin{bmatrix} 1 & 0 & 0 & 0 \end{bmatrix} ).$
    - Normalize the initial vector to have a length of 1.
- **Power Method Iterations:**
    - Compute successive vectors $( x_1, x_2, x_3 )$ using $( x_{i+1} = A \cdot x_i )$ and normalize each time.
    - Continue iterations until the vectors agree to at least 4 decimal places.
- **Calculate Dominant Eigenvalue:**
    - Use the formula $( \lambda = \frac{(x \cdot A \cdot x)}{(x \cdot x)} )$ with the vector at convergence.
**Results:**
- ###### Part (a) Computed Vectors:
    
    - $x_0 = \begin{bmatrix} 1 & 0 & 0 & 0 \end{bmatrix}$
    - $x_1 = \begin{bmatrix} 0.7071 & 0.7071 & 0 & 0 \end{bmatrix}$
    - $x_2 = \begin{bmatrix} 0.8018 & 0.5345 & 0.2673 & 0 \end{bmatrix}$
    - $x_3 = \begin{bmatrix} 0.7182 & 0.6156 & 0.3078 & 0.1026 \end{bmatrix}$
- ###### Part (b) Convergence:
    
    - **Number of iterations until convergence:** 18
    - **Last two vectors:**
        - $\text{Previous vector} = \begin{bmatrix} 0.3955 & 0.5207 & 0.7073 & 0.2685 \end{bmatrix}$
        - $\text{Current vector} = \begin{bmatrix} 0.3954 & 0.5207 & 0.7074 & 0.2685 \end{bmatrix}$
    - **Dominant eigenvalue:** 3.6339

---
### 2 Market Share Model using a Markov Chain
**Procedure:**
- **Markov Process:**
    - Define the transition matrix $( P = \begin{bmatrix} 0.9 & 0.1 \ 0.3 & 0.7 \end{bmatrix} ).$
    - Start with the initial state vector $( x_0 = \begin{bmatrix} 0.5 & 0.5 \end{bmatrix} ).$
- **Calculate State Distribution:**
    - Find the state distribution after four months by calculating $( P^4 \cdot x_0 ).$
- **Determine Steady-State Distribution:**
    - Continue calculating $( P^k )$ until the matrices converge to a steady-state matrix.
    - Determine the steady-state distribution vector.
**Results:**
- ###### Part (a) State Distribution After Four Months:
    
    - **Matrix ( P^4 ):** $$ P^4 = \begin{bmatrix} 0.7824 & 0.2176 \ 0.6528 & 0.3472 \end{bmatrix} $$
    - **State distribution ( x_4 ):** $$ x_4 = \begin{bmatrix} 0.5000 & 0.5000 \end{bmatrix} $$
- ###### Part (b) Convergence:
    - **Number of iterations until convergence:** 17
    - **Steady-State Matrix ( Q ):** $$ Q = \begin{bmatrix} 0.7500 & 0.2500 \ 0.7499 & 0.2501 \end{bmatrix} $$
    - **Steady-state distribution vector:** $$ \begin{bmatrix} 0.5000 & 0.5000 \end{bmatrix} $$