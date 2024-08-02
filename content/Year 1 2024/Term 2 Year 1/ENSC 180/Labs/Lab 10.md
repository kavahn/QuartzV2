# Lab 10 of [[ENSC 180]]

## Code:
```
% ENSC 180 Introduction to Engineering Analysis

% Lab 10


syms T x

a = 28.90;

b = -0.1571e-2;

c = 0.8081e-5;

d = -2.873e-9;

Cp = 30;

% ==== Question 1 ====

% Corrected energy balance equation for heat capacity

energy_balance_equation = Cp == a + (b*T) + (c*T^2) + (d*T^3); % Ensure explicit multiplications

disp('Energy Balance Equation:');

disp(energy_balance_equation)

% Solve the energy balance equation for T

T_solutions = solve(energy_balance_equation, T);

disp('Solutions for T:');

disp(vpa(T_solutions))

% ==== Question 2 ====

% Corrected function for integration (ax^2 + bx + c)

% Ensure correct symbolic expression with explicit multiplication

function_to_integrate = a*(x^2) + b*x + c; % Ensure explicit multiplication

% Perform the definite integration from 3.5 to 24

definite_integral_result = int(function_to_integrate, x, 3.5, 24);

disp('Result of the Definite Integral:');

disp(vpa(definite_integral_result))

% ==== Question 3 ====

% Define the function y and find its first and second derivatives clearly.

function_y = cos(2*x)*sin(x); % Clear use of symbols

first_derivative = diff(function_y, x);

second_derivative = diff(first_derivative, x);

disp('First derivative:');

disp(first_derivative)

disp('Second derivative:');

disp(second_derivative)
```

## Output:
```
Energy Balance Equation:  
30 == - (6946487759505659*T^3)/2417851639229258349412352 + (1192545110877175*T^2)/147573952589676412928 - (3622479367474713*T)/2305843009213693952 + 289/10  

Solutions for T:  
-274.56474139582861403582232106081  
549.4782186680423378650676431704  
2537.8258196299789832331114457949  
  
Result of the Definite Integral:  
132757.72817336883333335759707201  

First derivative:  
cos(2*x)*cos(x) - 2*sin(2*x)*sin(x)  
  
Second derivative:  
- 5*cos(2*x)*sin(x) - 4*sin(2*x)*cos(x)
```

## Explanation
- Define symbols, constants with `syms`.
- Correct equation; ensure clear syntax.
- Display energy balance explicitly shown.
- Solve equation, display `T` solutions.
- Define integration function correctly formed.
- Perform integration within specified limits.
- Calculate derivatives; cos and sin.
- Explicit multiplication, avoid syntax issues.
- Use `disp` for displaying results.