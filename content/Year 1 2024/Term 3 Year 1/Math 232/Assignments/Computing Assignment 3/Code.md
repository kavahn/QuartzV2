```
% Task 1: Power Method to approximate the dominant eigenvalue and eigenvector

%===============================================================

% Define the matrix A

A = [1 2 0 0; 1 1 1 1; 0 1 1 5; 0 0 1 1];

% Part (a): Choose an initial vector x0 with a length of 1

x0 = [1; 0; 0; 0]; % Example initial vector, normalized to length 1

% Normalizing the initial vector

x0 = x0 / norm(x0);

% Perform iterations of the Power Method, normalizing each time

x1 = A*x0; x1 = x1 / norm(x1);

x2 = A*x1; x2 = x2 / norm(x2);

x3 = A*x2; x3 = x3 / norm(x3);

% Display results for Part (a)

fprintf('Part 1 (a): Values of chosen x0 and resulting vectors x1, x2, x3\n');

disp('x0:'); disp(x0');

disp('x1:'); disp(x1');

disp('x2:'); disp(x2');

disp('x3:'); disp(x3');

% Part (b): Continue iterations until convergence

tolerance = 1e-4;

previous_vector = x3;

current_vector = A * previous_vector;

current_vector = current_vector / norm(current_vector);

iteration_count = 3;

while max(abs(current_vector - previous_vector)) > tolerance

iteration_count = iteration_count + 1;

previous_vector = current_vector;

current_vector = A * previous_vector;

current_vector = current_vector / norm(current_vector);

end

% Calculating the dominant eigenvalue

dominant_eigenvalue = (current_vector' * A * current_vector) / (current_vector' * current_vector);

% Display results for Part (b)

fprintf('Part 1 (b): Power Method Convergence\n');

fprintf('Number of iterations until convergence: %d\n', iteration_count);

disp('Last two vectors:');

disp(previous_vector');

disp(current_vector');

fprintf('Dominant eigenvalue: %.4f\n', dominant_eigenvalue);

% Task 2: Markov Chain Model for Internet Services Market Share

%===============================================================

% Define the transition matrix P and the initial state vector x0

P = [0.9, 0.1; 0.3, 0.7];

x0 = [0.5; 0.5];

% Part (a): Calculate P^4 and the state distribution after four months

P4 = P^4;

x4 = P4 * x0;

fprintf('Part 2 (a): Matrix P^4 and Market Share After Four Months x4\n');

fprintf('P^4:\n');

disp(P4);

fprintf('x4: Market share after four months (NewServices, RealWest): (%.4f, %.4f)\n', x4(1), x4(2));

% Part (b): Calculate P^k until convergence and find the steady-state distribution

previous_Pk = P;

current_Pk = P * P;

iteration_count = 2;

% Iterate until convergence to 4 decimal places or reach max iterations

while max(max(abs(current_Pk - previous_Pk))) > tolerance && iteration_count < max_iterations

iteration_count = iteration_count + 1;

previous_Pk = current_Pk;

current_Pk = current_Pk * P;

end

Q = current_Pk;

steady_state_vector = Q * x0;

fprintf('Part 2 (b): Convergence and Steady-State Distribution\n');

fprintf('The highest exponent calculated until convergence: %d\n', iteration_count);

fprintf('Matrix Q (P^%d):\n', iteration_count);

disp(Q);

fprintf('Steady-state vector (NewServices, RealWest): (%.4f, %.4f)\n', steady_state_vector(1), steady_state_vector(2));

%================= End of MATLAB Script ======================
```