```
%% A16: Car Rental Company Steady-State Distribution

disp('A16: Car Rental Company');

% Initial state vector

x0_a16 = [0.1; 0.6; 0.3];

% Transition matrix for A16 scenario

P_a16 = [0.8 0.3 0.3;

0.1 0.6 0.1;

0.1 0.1 0.6];

% Initialize vectors to track state evolution

vAirport = [x0_a16(1)];

vTrainStation = [x0_a16(2)];

vCityCenter = [x0_a16(3)];

% Iteratively apply transition matrix to find steady state for A16

for i = 1:500

x1_a16 = P_a16^i * x0_a16;

vAirport = [vAirport x1_a16(1)];

vTrainStation = [vTrainStation x1_a16(2)];

vCityCenter = [vCityCenter x1_a16(3)];

end

% Plotting for A16

subplot(2,1,1); % Subplot for A16

hold on

plot(vAirport, 'g+-');

plot(vTrainStation, 'ro--');

plot(vCityCenter, 'b*');

legend('Airport', 'Train Station', 'City Center');

xlabel('Days');

ylabel('Proportion of Cars');

title('A16: Car Distribution Evolution');

%% B15: Bicycle Pool Steady-State Distribution

disp('B15: Bicycle Pool');

% Transition matrix based on B15 problem description

P_b15 = [160/200, 40/200, 60/200;

20/200, 140/200, 40/200;

20/200, 20/200, 100/200];

% Initial state: equal number of bicycles at each location

x0_b15 = [1/3; 1/3; 1/3];

% Initialize vectors to track state evolution

vResidence = [x0_b15(1)];

vLibrary = [x0_b15(2)];

vAthleticCentre = [x0_b15(3)];

% Iteratively apply P to find steady state for B15

for i = 1:500

x1_b15 = P_b15 * x0_b15;

vResidence = [vResidence x1_b15(1)];

vLibrary = [vLibrary x1_b15(2)];

vAthleticCentre = [vAthleticCentre x1_b15(3)];

x0_b15 = x1_b15; % Prepare for the next iteration

end

% Plotting for B15

subplot(2,1,2); % Subplot for B15

hold on

plot(vResidence, 'g');

plot(vLibrary, 'r');

plot(vAthleticCentre, 'b');

legend('Residence', 'Library', 'Athletic Centre');

xlabel('Days');

ylabel('Proportion of Bicycles');

title('B15: Bicycle Distribution Evolution');p
```