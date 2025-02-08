# FuzzyPID
Converting specified Matlab optimization code into Python.

# Fuzzy PID Control System
This project implements a fuzzy logic-based PID controller to tune the control parameters dynamically in a control system. The core of this project is the main function, which integrates the system dynamics and adjusts the PID parameters (Kp, Ki, Kd) based on fuzzy logic. It then generates plots for system tracking performance, control input, and parameter variation.

# Features
Fuzzy Logic-based PID Tuning: The PID controller parameters (Kp, Ki, Kd) are tuned dynamically based on fuzzy logic rules, which improves control performance over traditional PID controllers.
System Integration: The code simulates the evolution of the system state over time based on the control inputs, disturbance, and reference trajectory.
Performance Evaluation: The code calculates the root mean square error (RMSE) for system tracking performance and visualizes the results in multiple plots.
# File Description
Input Parameters:
xref, xr: Reference values (desired system states).
Ts, T: Sampling time and total simulation time.
Kpmax, Kpmin, Kimax, Kimin, Kdmax, Kdmin: Maximum and minimum limits for PID gains.
xd, xdnew: System states and their derivatives.
x, dist, e, u, t: System variables, disturbances, errors, control inputs, and time.
Kp1, Kp2, Kp3, Ki1, Ki2, Ki3, Kd1, Kd2, Kd3: Arrays to store the PID gains for each of the system states.

Loop Structure:
The control loop runs for the duration T with a time step Ts. The loop calculates the control inputs u based on the current tracking error (e) and its rate of change (edot).
The fuzzy PID parameters (Kp, Ki, Kd) are dynamically tuned based on fuzzy logic functions (fuzzyPID1, fuzzyPID2), which adjust the parameters for each state.

System Integration:
The system state is updated using system_integration() to simulate the effect of the control inputs, disturbances, and the system's dynamics.

Plots:
grafik_1.png: System tracking vs. reference trajectory.
grafik_2-1.png, grafik_2-2.png, grafik_2-3.png: Tracking performance for each state (x1, x2, x3).
grafik_3.png: Control input over time.
grafik_4.png: PID parameters (Kp_1, Ki_1, Kd_1) over time.
