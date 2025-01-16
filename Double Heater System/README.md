# PID Control for Double-Heater Temperature System

## Overview
This project explores PID control for a double-heater temperature system, addressing the cross-coupling effects between Heater 1 and Heater 2. The system aims to control two temperatures (T₁ and T₂) independently or through multivariable control strategies. MATLAB was used to simulate and evaluate the performance of the designed controllers.

## Objectives
1. Model the system dynamics with two heaters and sensors.
2. Design independent PID controllers for T₁ and T₂.
3. Implement multivariable control using a decoupling matrix to address cross-coupling effects.
4. Compare the performance of independent and combined control strategies under simulation.

## Project Structure
- `docs/`: Contains the project report and relevant documentation.
- `scripts/`: MATLAB scripts for system modeling, controller design, and simulation.
- `results/`: Graphs and numerical results from the experiments and simulations.
- `references/`: External references used in this project.

## Key Details
### Experimental Setup
- **Heater-Sensor Relationships:**
  - Heater 1 influences T₁ (primary) and T₂ (secondary).
  - Heater 2 influences T₂ (primary) and T₁ (secondary).

- **System Transfer Functions:**
  - G₁₁(s): Heater 1’s effect on T₁.
  - G₂₂(s): Heater 2’s effect on T₂.
  - G₁₂(s): Heater 2’s cross-effect on T₁.
  - G₂₁(s): Heater 1’s cross-effect on T₂.

### Simulation
#### Independent Control
PID controllers designed independently for T₁ and T₂:
- **PID₁ (T₁):** Kₚ=5, Kᵢ=1, Kₒ=0.5
- **PID₂ (T₂):** Kₚ=4, Kᵢ=1.2, Kₒ=0.3

## Results
### Independent Control
- **Rise Time:** T₁ = 60 s, T₂ = 50 s.
- **Overshoot:** 10% for both heaters.
- **Settling Time:** 150 s.

### Combined Control
- Decoupling reduced interference significantly.
- Faster rise times: T₁ = 50 s, T₂ = 40 s.
- Overshoot remained minimal (<15%).

## Discussion
1. **Independent Control:**
   - Easy to implement but limited by cross-coupling effects.
   - Performance is degraded when heaters interact strongly.

2. **Multivariable Control:**
   - Using decoupling significantly reduced cross-coupling.
   - Improved accuracy and response times.

## Future Directions
1. **Real-World Applications:**
   - HVAC systems where multiple heaters interact.
   - Industrial ovens or reactors requiring multivariable temperature control.

2. **Advanced Control:**
   - Implementing Model Predictive Control (MPC) for better performance.
   - Adaptive control strategies for changing environmental conditions.

## Conclusion
The two-heater control system demonstrates the challenges of cross-coupling. While independent PID control provides a baseline, multivariable control with decoupling offers significant performance improvements. The simulation results highlight the importance of addressing cross-coupling for systems with interacting actuators.
