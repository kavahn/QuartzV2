```
% MATLAB Scrip for Computing Assignment 2

% Task 1: Create Hexagon
v_initial = [cos(pi/3), sin(pi/3)];
theta = pi/3;
R = [cos(theta), -sin(theta); sin(theta), cos(theta)];

hexagon_points = v_initial;
for i=1:5
    new_v = R * hexagon_points(end, :)';
    hexagon_points = [hexagon_points; new_v'];
end

% Plotting the hexagon
figure;
plot([hexagon_points(:, 1); hexagon_points(1, 1)], [hexagon_points(:, 2); hexagon_points(1, 2)], '-o');
axis equal;
grid on;
title('Hexagon Created by Rotating an Initial Unit Vector');
xlabel('x');
ylabel('y');

% Task 2: Apply Transformations
theta_rotation = pi/4;
R_rotation = [cos(theta_rotation), -sin(theta_rotation); sin(theta_rotation), cos(theta_rotation)];
R_reflection_x = [1, 0; 0, -1];

hexagon_rotated = (R_rotation * hexagon_points')';
hexagon_reflected_x = (R_reflection_x * hexagon_points')';

% Plotting the transformed hexagons
figure;
subplot(1,2,1);
plot([hexagon_points(:, 1); hexagon_points(1, 1)], [hexagon_points(:, 2); hexagon_points(1, 2)], '-o', ...
    [hexagon_rotated(:, 1); hexagon_rotated(1, 1)], [hexagon_rotated(:, 2); hexagon_rotated(1, 2)], '-o');
title('Hexagon Rotated by 45°');
axis equal; grid on;

subplot(1,2,2);
plot([hexagon_points(:, 1); hexagon_points(1, 1)], [hexagon_points(:, 2); hexagon_points(1, 2)], '-o', ...
    [hexagon_reflected_x(:, 1); hexagon_reflected_x(1, 1)], [hexagon_reflected_x(:, 2); hexagon_reflected_x(1, 2)], '-o');
title('Hexagon Reflected Across x-axis');
axis equal; grid on;

% Task 3: Comparisons of Composition of Transformations
theta1 = pi/6; % 30 degrees
theta2 = pi/3; % 60 degrees
R_theta1 = [cos(theta1), -sin(theta1); sin(theta1), cos(theta1)];
R_theta2 = [cos(theta2), -sin(theta2); sin(theta2), cos(theta2)];

% Compositions
T1_T2 = R_theta1 * R_theta2;
T2_T1 = R_theta2 * R_theta1;

% Reflection matrix
R_reflection = R_reflection_x;
% Compositions of rotation and reflection
T1ref_T2rot = R_reflection * R_theta1; % Reflection then rotation
T2rot_T1ref = R_theta1 * R_reflection; % Rotation then reflection

% Comparisons
disp(isequal(T1_T2, T2_T1)); % Should be true for rotations
disp(isequal(T1ref_T2rot, T2rot_T1ref)); % Should be false for rotation and reflection
```