# PID Control for Single-Heater Temperature System

## Overview
This project involves designing and implementing a PID controller for a single-heater temperature control system. The system regulates the temperature of a thermal system to meet desired specifications. MATLAB's Control System Designer was utilized for controller tuning, system modeling, and performance evaluation.

## Objectives
1. Characterize the system in open-loop mode to determine key parameters.
2. Develop a mathematical model using experimental data.
3. Design and implement a PID controller for improved system performance.
4. Validate the model and controller using MATLAB simulations.


## Key Results
### Open-Loop Characterization
- **Initial Temperature (T₀):** 21.75°C
- **Steady-State Temperature (Tₓ):** 32.06°C
- **Dead Time (θ):** 2 seconds
- **Time Constant (τ):** 42.2 seconds
- **System Gain (K):** Derived from experimental data.

### PID Controller Performance
- **Rise Time:** 0.5014 seconds
- **Settling Time:** 3.1598 seconds
- **Overshoot:** 17.93%
- **Steady-State Error:** 0%

## MATLAB Implementation
### Open-Loop Characterization
The heater's response to an 80% power input was recorded and analyzed to determine system dynamics.

### Controller Design
A PID controller was designed with the following goals:
- Fast response time.
- Minimal overshoot.
- Zero steady-state error.

MATLAB's `Control System Designer` was used to tune the PID parameters and validate the performance.

### Code Example
Below is an example of the MATLAB script for characterizing the system:

```matlab
clc; clear all; close all;

% System parameters
K = 0.132625 * 80; % Gain (from experimental data)
tau = 42.2; % Time constant (s)
theta = 2; % Dead time (s)

% Transfer function without delay (approximation for Control Designer)
num = [K];
den = [tau, 1];
Gs = tf(num, den);

% Open Control System Designer
controlSystemDesigner(Gs);
