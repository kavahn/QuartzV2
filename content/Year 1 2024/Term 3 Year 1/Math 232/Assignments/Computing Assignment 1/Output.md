
---
# Output
```
Random Matrix A:
     9     4     4     3     1     2
     3     2     9     8     1     6
     9     3     6     8     6     5
     3     7     6     4     8     1
    10     5    10     6    10     4

Random Vector b:
     2
     8
     4
     6
     2

RREF of the augmented matrix [A|b]:
    1.0000         0         0         0         0    0.0795   -0.4841
         0    1.0000         0         0         0   -0.2980    0.9353
         0         0    1.0000         0         0    0.2396    0.0267
         0         0         0    1.0000         0    0.5367    0.9665
         0         0         0         0    1.0000   -0.0921   -0.3901

Solution set:\n
   -0.4841
    0.9353
    0.0267
    0.9665
   -0.3901

RREF of the augmented matrix [A|b] for B44:
     1     0     0   300
     0     1     0   600
     0     0     1   400

Armchair price: $300.00
Sofa bed price: $600.00
Double bed price: $400.00
Projection results:
Projection of x1 onto v:
    1.0000
    2.0000
    3.0000

Projection of x2 onto v:
    2.0000
    4.0000
    6.0000

Projection of x3 onto v:
   1.0e-16 *

    0.2776
    0.5551
         0

[R ◦ P]:
    0.1857    0.3714    0.5571
    0.1429    0.2857    0.4286
    0.1286    0.2571    0.3857

[P ◦ R]:
   -0.0714    0.1429    0.2143
   -0.1429    0.2857    0.4286
   -0.2143    0.4286    0.6429

RREF of A for basis calculation:
     1     0     5     0     2
     0     1    -2     0     1
     0     0     0     1    -7
     0     0     0     0     0

Basis for the subspace S:
     3     6     3   
     2     5     0    
     0     2    -4    
    -1     1    -7    

Dimension of S:
     3
```




---
# Code
```
%% 1

% 1(a) Generate a random 5x6 matrix A and a random 5x1 column vector b

A = randi(10, 5, 6);

b = randi(10, 5, 1);

% Form the augmented matrix [A|b]

augmentedMatrix = [A b];

% Calculate the Reduced Row Echelon Form

rrefMatrix = rref(augmentedMatrix);

% Display the results

disp('Random Matrix A:');

disp(A);

disp('Random Vector b:');

disp(b);

disp('RREF of the augmented matrix [A|b]:');

disp(rrefMatrix);

% Extract solution set for Ax = b (if possible)

if rank(A) == rank(augmentedMatrix)

disp('Solution set:\n');

solutions = rrefMatrix(:, end);

disp(solutions);

else

disp('No unique solution exists.');

end

% 1(b) Textbook Section 2.1 B44: Determine the cost for each item

% Define the coefficient matrix A and the vector b

A_b44 = [

20 10 8;

15 12 10;

12 20 10

];

b_b44 = [

15200;

15700;

19600

];

% Form the augmented matrix [A|b]

augmentedMatrix_b44 = [A_b44 b_b44];

% Calculate the Reduced Row Echelon Form

rrefMatrix_b44 = rref(augmentedMatrix_b44);

% Display the RREF of [A|b]

disp('RREF of the augmented matrix [A|b] for B44:');

disp(rrefMatrix_b44);

% Check if the system has a unique solution

if rank(A_b44) == rank(augmentedMatrix_b44)

% Extract the solutions

prices_b44 = rrefMatrix_b44(:, end);

armchair_price = prices_b44(1);

sofa_bed_price = prices_b44(2);

double_bed_price = prices_b44(3);

% Display the prices

fprintf('Armchair price: $%.2f\n', armchair_price);

fprintf('Sofa bed price: $%.2f\n', sofa_bed_price);

fprintf('Double bed price: $%.2f\n', double_bed_price);

else

disp('The sales slips must be in error; no unique solution exists.');

end

%% 2

% Vectors x1, x2, x3 and projection vector v

v = [1; 2; 3];

x1 = [3; 4; 1];

x2 = [2; 4; 6];

x3 = [1; 1; -1];

% Standard matrix for projection onto v

P = (v * v') / (norm(v)^2);

% Projections

Px1 = P * x1;

Px2 = P * x2;

Px3 = P * x3;

% Display the projections

disp('Projection results:');

disp('Projection of x1 onto v:');

disp(Px1);

disp('Projection of x2 onto v:');

disp(Px2);

disp('Projection of x3 onto v:');

disp(Px3);

% Define the rotation matrix R

R = [

0.8 0 0.6;

0 1 0;

-0.6 0 0.8

];

% Composition matrices

R_composed_P = R * P; % [R ◦ P] projection followed by rotation

P_composed_R = P * R; % [P ◦ R] rotation followed by projection

% Display the composition matrices

disp('[R ◦ P]:');

disp(R_composed_P);

disp('[P ◦ R]:');

disp(P_composed_R);

%% Section 3: Section 3.4

% Vectors for constructing matrix A

v1 = [3; 2; 0; -1];

v2 = [6; 5; 2; 1];

v3 = [3; 0; -4; -7];

v4 = [2; 0; -1; -1];

v5 = [-2; 9; 9; 6];

% Matrix with the vectors as columns

A_S = [v1 v2 v3 v4 v5];

% Calculate the RREF of A

rrefMatrix_S = rref(A_S);

% Display the RREF matrix

disp('RREF of A for basis calculation:');

disp(rrefMatrix_S);

% Basis and dimension from RREF of A

basisVectors = A_S(:, any(rrefMatrix_S));

dimension = size(basisVectors, 2);

disp('Basis for the subspace S:');

disp(basisVectors);

disp('Dimension of S:');

disp(dimension);

% Writing non-basis vectors as linear combinations (adjust based on actual non-basis vectors)

% Solve for coefficients: A_basis * c = v

if dimension < 5 % if some vectors are not in the basis

nonBasis1 = v3; % For example, assuming v3 not in basis

nonBasis2 = v4; % For example, assuming v4 not in basis

c_v3 = basisVectors \ nonBasis1;

c_v4 = basisVectors \ nonBasis2;

disp('v3 as a linear combination of basis vectors:');

disp(c_v3);

disp('v4 as a linear combination of basis vectors:');

disp(c_v4);

end
```