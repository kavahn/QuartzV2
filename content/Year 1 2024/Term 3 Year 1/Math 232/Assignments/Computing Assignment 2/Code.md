# Code

```
%% Question 1

% Initial vector

x0 = [2; 3];

% Rotation matrix for 60 degrees

theta = deg2rad(60);

R = [cos(theta), -sin(theta); sin(theta), cos(theta)];

% Calculate x1, x2, ..., x5

x_vectors = zeros(2, 6);

x_vectors(:, 1) = x0;

for i = 2:6

x_vectors(:, i) = R * x_vectors(:, i-1);

end

% Plotting all vectors x0 to x5 on the same plot

figure;

colors = lines(6);

hold on;

for i = 1:6

quiver(0, 0, x_vectors(1, i), x_vectors(2, i), 'Color', colors(i, :), 'DisplayName', ['x_' num2str(i-1)]);

end

legend('Location', 'Best');

title('Rotation of vector x0 by 60 degrees');

xlabel('x');

ylabel('y');

grid on;

hold off;

% Print vectors

disp('Vectors after each rotation:')

disp(x_vectors)

% Reflection matrix

P = [-0.8, 0.6; 0.6, 0.8];

% Reflect vectors x0 to x5

reflected_vectors = P * x_vectors;

% Plotting all reflected vectors

figure;

hold on;

for i = 1:6

quiver(0, 0, reflected_vectors(1, i), reflected_vectors(2, i), 'Color', colors(i, :), 'DisplayName', ['P*x_' num2str(i-1)]);

end

legend('Location', 'Best');

title('Reflection of vectors over the line y = 3x');

xlabel('x');

ylabel('y');

grid on;

hold off;

% Print reflected vectors

disp('Reflected vectors:')

disp(reflected_vectors)

%% Question 2

% Basis vectors

v1 = [0; 1; 2; 1];

v2 = [1; 5; 0; 1];

v3 = [2; 3; 6; 4];

v4 = [1; 3; -1; -1];

% Construct the basis matrix

B = [v1, v2, v3, v4];

% Calculate the transition matrix PS->B

PS_to_B = inv(B);

% Given vector x

x = [1; 2; 3; 4];

% Calculate the coordinates of x in the new basis B

x_B = PS_to_B * x;

% Print answers for part (a)

disp('Transition matrix PS->B:')

disp(PS_to_B)

disp('Coordinates of x in basis B:')

disp(x_B)

% Define the linear mapping L

L = @(x1, x2, x3, x4) [x2 + 5*x4; x1 - x3; x1 + x2 + x3 + x4; 0];

% Calculate the images of the basis vectors under L

L_B = [L(v1(1), v1(2), v1(3), v1(4)), L(v2(1), v2(2), v2(3), v2(4)), ...

L(v3(1), v3(2), v3(3), v3(4)), L(v4(1), v4(2), v4(3), v4(4))];

% Transition matrix to the new basis B

L_B = PS_to_B * L_B;

% Print the matrix [L]_B

disp('Matrix [L]_B:')

disp(L_B)

% Calculate the image of (x_B) under the linear map [L]_B

Lx_B = L_B * x_B;

% Print the image of (x_B)

disp('Image of (x_B) under [L]_B:')

disp(Lx_B)
```

# Output
```
Vectors after each rotation:
    2.0000   -1.5981   -3.5981   -2.0000    1.5981    3.5981
    3.0000    3.2321    0.2321   -3.0000   -3.2321   -0.2321

Reflected vectors:
    0.2000    3.2177    3.0177   -0.2000   -3.2177   -3.0177
    3.6000    1.6268   -1.9732   -3.6000   -1.6268    1.9732

Transition matrix PS->B:
   -1.1481    0.3704    0.6667   -0.7037
   -0.2593    0.1481   -0.3333    0.5185
    0.4444   -0.1111    0.0000    0.1111
    0.3704    0.0741    0.3333   -0.7407

Coordinates of x in basis B:
   -1.2222
    1.1111
    0.6667
   -1.4444

Matrix [L]_B:
   -4.9630   -6.4444  -17.8889    4.3704
   -3.1852   -4.7778  -11.5556    0.1481
    2.8889    4.3333   10.6667   -1.1111
    3.4074    6.1111   13.2222    0.0741

Image of (x_B) under [L]_B:
  -19.3333
   -9.3333
   10.0000
   11.3333
```