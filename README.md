# PID-Control-Temperature-System

## Overview
This repository presents the design and implementation of PID control systems for single and double-heater temperature systems. These projects explore the principles of control engineering, addressing challenges such as system dynamics modeling, parameter estimation, and cross-coupling effects. Through MATLAB simulations and validations, we successfully demonstrated how precise control can improve performance metrics like rise time, settling time, and overshoot.

## Objectives
1. **Single-Heater System:**
   - Characterize the system in open-loop mode to determine key parameters.
   - Develop a mathematical model using experimental data.
   - Design and implement a PID controller for improved performance.
   - Validate the model and controller using MATLAB simulations.

2. **Double-Heater System:**
   - Model the system dynamics with two heaters and sensors.
   - Design independent PID controllers for each heater.
   - Implement multivariable control using a decoupling matrix to address cross-coupling.
   - Compare the performance of independent and combined control strategies.

## Key Features
- Accurate system characterization and parameter estimation.
- Application of First-Order Plus Dead Time (FOPDT) modeling.
- PID controller design using MATLAB's Control System Designer.
- Comprehensive simulations for validation and performance evaluation.
- Implementation of multivariable control for complex systems with cross-coupling.

## Results
### Single-Heater System
- **Open-Loop Characterization:**
  - Initial Temperature: 21.75°C
  - Steady-State Temperature: 32.06°C
  - Dead Time: 2 seconds
  - Time Constant: 42.2 seconds
  - System Gain: Derived from experimental data.

- **PID Controller Performance:**
  - Rise Time: 0.5014 seconds
  - Settling Time: 3.1598 seconds
  - Overshoot: 17.93%
  - Steady-State Error: 0%

### Double-Heater System
#### Independent Control:
- Rise Time: T₁ = 60 s, T₂ = 50 s.
- Overshoot: 10% for both heaters.
- Settling Time: 150 s.

#### Combined Control:
- Decoupling significantly reduced interference.
- Faster rise times: T₁ = 50 s, T₂ = 40 s.
- Overshoot remained minimal (<15%).

## Discussion
- **Single-Heater System:**
  - Successfully modeled and controlled a single-heater system using PID.
  - Demonstrated the importance of precise parameter estimation for achieving desired performance.

- **Double-Heater System:**
  - Highlighted the challenges of cross-coupling in multivariable systems.
  - Showcased how multivariable control with decoupling enhances accuracy and response time.
  - Provided a comparative analysis between independent and combined control strategies.

## Future Directions
1. Real-world applications:
   - Integration into HVAC systems.
   - Industrial processes requiring precise multivariable temperature control.

2. Advanced control strategies:
   - Implementing Model Predictive Control (MPC) for better adaptability.
   - Designing adaptive control systems to manage dynamic environmental conditions.

## Project Structure
- **`Single Heater System/`**:
  - Focused on the single-heater system.
  - Contains documentation, and results.
- **`Double Heater System/`**:
  - Explores the double-heater system with multivariable control.
  - Includes independent and combined control strategies.

## Tools and Technologies
### MATLAB
- Used for system modeling, controller design, and performance evaluation.
- Includes MATLAB’s Control System Designer for PID tuning.

### MATLAB Plots
- Visualized step responses and control system dynamics.

## Conclusion
This repository showcases a comprehensive exploration of PID control systems for single and double-heater temperature systems. The successful implementation of both independent and multivariable control strategies highlights the potential of these methods in real-world applications. By addressing challenges such as system characterization, parameter estimation, and cross-coupling, this project serves as a robust framework for advancing control engineering practices.

## Acknowledgments
- **Group No. 8, Obinna Ndubuisi**
  - Department of Mechanical and Mechatronics Engineering
  - Southern Illinois University Edwardsville

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

