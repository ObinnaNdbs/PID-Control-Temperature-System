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

## Future Directions
This platform can be extended to:
- Real-time process control in manufacturing systems.
- Implementing advanced strategies like model predictive control (MPC).
- Educational purposes for understanding PID control systems.

## Conclusion
This project successfully demonstrated the design and implementation of a PID controller for a single-heater temperature control system. Through precise modeling and validation using MATLAB, the system achieved desired performance metrics, including fast response, minimal overshoot, and zero steady-state error. The project highlights the importance of accurate parameter estimation and control system tuning in achieving optimal performance. Future advancements, such as real-time implementation and predictive control strategies, can further enhance the system's applicability across various industries.
