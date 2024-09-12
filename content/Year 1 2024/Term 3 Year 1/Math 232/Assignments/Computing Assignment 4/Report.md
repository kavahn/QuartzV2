###### Part (a): Best-Fit Cubic Polynomial:
- **Normal System Equation Matrix (A^T A):** $A^T A = \begin{bmatrix} 6 & 15 & 55 & 225 \\ 15 & 55 & 225 & 979 \\ 55 & 225 & 979 & 4425 \\ 225 & 979 & 4425 & 20455 \end{bmatrix}$
- **Vector (A^T \mathbf{b}):** $A^T \mathbf{b} = \begin{bmatrix} 74 \\ 318 \\ 1322 \\ 6106 \end{bmatrix}$
- **Coefficients of the best-fit cubic polynomial:** $(\mathbf{c} = (A^T A)^{-1} A^T \mathbf{b} = \begin{bmatrix} 3.2857 \\ 11.1429 \\ -6.1429 \\ 1.0000 \end{bmatrix})$
- **Resulting cubic polynomial:** $\text{The best-fit cubic polynomial is } y = 3.2857 + 11.1429x - 6.1429x^2 + 1.0000x^3$
###### Part (b): Matrix Computations:
- **Matrix ( A ):** $A = \begin{bmatrix} 0.092126 & 0.934460 & 0.360230 \\ 0.988257 & 0.255036 & 0.353312 \\ 0.939325 & 0.973212 & 0.048558 \\ 0.464528 & 0.861630 & 0.870482 \end{bmatrix}$
    
- **Matrix ( A^T A ):** $A^T A = \begin{bmatrix} 2.0833 & 1.6525 & 0.8323 \\ 1.6525 & 2.6278 & 1.2240 \\ 0.8323 & 1.2240 & 1.0147 \end{bmatrix}$
- **Eigen decomposition:**
    - **Matrix ( P ):** $P = \begin{bmatrix} -0.089199 & 0.804189 & 0.587643 \\ 0.521047 & -0.465148 & 0.715645 \\ -0.848854 & -0.370024 & 0.377530 \end{bmatrix}$
        
    - **Matrix ( D ):** $D = \begin{bmatrix} 0.3508 & 0 & 0 \\ 0 & 0.7444 & 0 \\ 0 & 0 & 4.6305 \end{bmatrix}$
        
- **Orthogonality check ( ( P^T P ) ):** $P^T P = \begin{bmatrix} 1.0000 & 5.5511e-17 & 1.6653e-16 \\ 5.5511e-17 & 1.0000 & 2.7756e-17 \\ 1.6653e-16 & 2.7756e-17 & 1.0000 \end{bmatrix}$
- **Singular Value Decomposition:**
    
    - **Matrix ( U ):** $U = \begin{bmatrix} -0.3991 & -0.5724 & -0.2919 & -0.6541 \\ -0.4167 & 0.6321 & 0.4308 & -0.4911 \\ -0.5887 & 0.3300 & -0.6451 & 0.3583 \\ -0.5661 & -0.4049 & 0.5595 & 0.4500 \end{bmatrix}$
        
    - **Matrix ( S ):** $S = \begin{bmatrix} 2.1519 & 0 & 0 & 0 \\ 0 & 0.8628 & 0 & 0 \\ 0 & 0 & 0.5923 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}$
        
    - **Matrix ( V ):** $V = \begin{bmatrix} -0.587643 & 0.804189 & 0.089199 \\ -0.715645 & -0.465148 & -0.521047 \\ -0.377530 & -0.370024 & 0.848854 \end{bmatrix}$
        
- **Comparison of ( S^T S ) and ( D ):** $S^T S = \begin{bmatrix} 4.6305 & 0 & 0 \\ 0 & 0.7444 & 0 \\ 0 & 0 & 0.3508 \end{bmatrix}$
- **Comparison of ( V ) and ( P ):**
    
    - **Matrix ( V ):** $V = \begin{bmatrix} -0.587643 & 0.804189 & 0.089199 \\ -0.715645 & -0.465148 & -0.521047 \\ -0.377530 & -0.370024 & 0.848854 \end{bmatrix}$
        
    - **Matrix ( P ):** $P = \begin{bmatrix} -0.089199 & 0.804189 & 0.587643 \\ 0.521047 & -0.465148 & 0.715645 \\ -0.848854 & -0.370024 & 0.377530 \end{bmatrix}$
  