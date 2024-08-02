```
% Task 1: Generate the data points

rng(0); % For reproducibility

xi = -5 + 10*rand(15,1); % x-coordinates

yi = -5 + 10*rand(15,1); % y-coordinates

% Degrees of polynomials to fit

degrees = [1, 5, 10];

% Preparing plot

figure;

hold on; % Hold on to plot data points and polynomials together

% Plotting the original data points

plot(xi, yi, 'ro', 'MarkerFaceColor', 'r');

for degree = degrees

% Task 2: Fit polynomial of given degree

p = polyfit(xi, yi, degree);

% Creating x values for plotting the polynomial fit

x_plot = linspace(-5,5,1000);

% Evaluating the polynomial p at points in x_plot

y_plot = polyval(p, x_plot);

% Plotting

plot(x_plot, y_plot, 'DisplayName', ['Degree ', num2str(degree)]);

end

% Task 3: Showing the plot

title('Least Squares Polynomial Fitting');

xlabel('x'); ylabel('y');

legend show;

grid on;

hold off;
```