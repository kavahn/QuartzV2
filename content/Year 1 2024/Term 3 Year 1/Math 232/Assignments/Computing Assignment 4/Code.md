```
% Part 1: Best-Fit Cubic Polynomial
% Given points
x = [0 1 2 3 4 5]';
y = [3 10 9 7 15 30]';

% Construct matrix A for the cubic polynomial
A = [ones(length(x),1) x x.^2 x.^3];

% Solve the normal equation A^T A c = A^T b
c = (A'*A)\(A'*y);

% The coefficients of the best-fit cubic polynomial
a = c(1); b = c(2); c2 = c(3); d = c(4); % c2 to avoid conflict with variable c

% Display the best-fit cubic polynomial
fprintf('The best-fit cubic polynomial is y = %.4f + %.4fx + %.4fx^2 + %.4fx^3\n', a, b, c2, d);

% Part 2: Matrix Computations
% Generate a random 4x3 matrix A
A = rand(4,3);

% Compute A^T A
ATA = A' * A;

% Compute eigen decomposition of A^T A
[P, D] = eig(ATA);

% Check if P is orthogonal
PTP = P' * P;

% Perform Singular Value Decomposition
[U, S, V] = svd(A);

% Compare S' * S with D
STS = S' * S;

% Display results
disp('Matrix A:');
disp(A);

disp('Matrix ATA:');
disp(ATA);

disp('Eigen decomposition:');
disp('Matrix P:');
disp(P);
disp('Matrix D:');
disp(D);

disp('Orthogonality check (P^T P):');
disp(PTP);

disp('Singular Value Decomposition:');
disp('Matrix U:');
disp(U);
disp('Matrix S:');
disp(S);
disp('Matrix V:');
disp(V);

disp('Comparison of S^T S and D:');
disp(STS);

disp('Comparison of V and P:');
disp('Matrix V:');
disp(V);
disp('Matrix P:');
disp(P);
```