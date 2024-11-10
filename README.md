# Control_System_Workshop
```bash
s = tf('s');  % Laplace variable
G = 1 / (5*s^2 + 15*s + 1);  % Motor transfer function

% PID Controller parameters
Kp = 90;    % Proportional gain
Ki = 5;     % Integral gain
Kd = 20;    % Derivative gain
C = pid(Kp, Ki, Kd);  % PID controller

% Closed-loop transfer function
T = feedback(C*G, 1);

% Plot step response
figure;
step(T);
hold on;

% Highlight the ESS error line at value = 1
yline(1, 'g--', 'ESS Error Line');  % Green dashed line at y = 1

% Title and labels
title('Step Response of DC Motor with PID Control');
xlabel('Time (s)');
ylabel('Motor Output');

% Legend
legend('System Response', 'ESS Error Line (1)');
grid on;
```
# Kahoot Winner
## 1st
- Khoo Kai Ze
- Darshan Kumar
- Sanjif
- Nick Wong

## 2ns
- Edmund
- Affan
- Damien
- Fasih

## 3nd
- Lim Zhan Hung
- Maha
- Firdaus
