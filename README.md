# Mobile-Robotics
# Linear Model Predictive Control (MPC) for Lane Keeping and Obstacle Avoidance

This project implements a **Model Predictive Control (MPC)** framework for autonomous vehicle control, focusing on lane keeping and obstacle avoidance on low curvature roads. The controller was designed and tested using MATLAB, leveraging the state-space representation of vehicle dynamics.

## Project Overview

The primary goals of the project are:
- **Lane Keeping**: Maintain the vehicle within lane boundaries while minimizing lateral position errors.
- **Obstacle Avoidance**: Adjust the vehicle's trajectory to navigate around obstacles without leaving the lane.

### Key Features
1. **Linear State-Space Model**:
   - Includes lateral velocity, yaw angle, yaw angle error, lateral position error, and steering angle.
   - Discretized for digital control implementation.

2. **Predictive Control**:
   - Optimizes future control actions over a prediction horizon.
   - Uses a quadratic cost function to minimize tracking errors and control efforts.

3. **Constraints Handling**:
   - Enforces vehicle mechanical limits (steering angle, rate of change, and tire slip).
   - Maintains lane boundaries and avoids collisions.

4. **Robustness to Disturbances**:
   - Handles variations in road curvature, vehicle speed, and road surface conditions.

### Results
- **Lane Keeping**: Demonstrated effectiveness in maintaining the vehicle's trajectory with minimal lateral position errors, even at higher speeds.
- **Obstacle Avoidance**: Successfully navigated around single and multiple obstacles while ensuring stability and adherence to lane constraints.

### Future Work
- Extend to more complex road geometries.
- Integrate additional sensors for enhanced perception and robustness.
