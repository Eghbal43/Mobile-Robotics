# Mobile-Robotics
Linear Model Predictive Control (MPC) for Lane Keeping and Obstacle Avoidance
This project implements a Model Predictive Control (MPC) framework for autonomous vehicle control, focusing on lane keeping and obstacle avoidance on low curvature roads. The controller was designed and tested using MATLAB, leveraging the state-space representation of vehicle dynamics.

Project Overview
The primary goals of the project are:

Lane Keeping: Maintain the vehicle within lane boundaries while minimizing lateral position errors.
Obstacle Avoidance: Adjust the vehicle's trajectory to navigate around obstacles without leaving the lane.
Key Features
Linear State-Space Model:

Includes lateral velocity, yaw angle, yaw angle error, lateral position error, and steering angle.
Discretized for digital control implementation.
Predictive Control:

Optimizes future control actions over a prediction horizon.
Uses a quadratic cost function to minimize tracking errors and control efforts.
Constraints Handling:

Enforces vehicle mechanical limits (steering angle, rate of change, and tire slip).
Maintains lane boundaries and avoids collisions.
Robustness to Disturbances:

Handles variations in road curvature, vehicle speed, and road surface conditions.
Results
Lane Keeping: Demonstrated effectiveness in maintaining the vehicle's trajectory with minimal lateral position errors, even at higher speeds.
Obstacle Avoidance: Successfully navigated around single and multiple obstacles while ensuring stability and adherence to lane constraints.
Future Work
Extend to more complex road geometries.
Integrate additional sensors for enhanced perception and robustness.
How to Use
Clone this repository:
bash
Copy code
git clone https://github.com/your-repo-name/Linear-MPC-Autonomous-Driving.git
Open MATLAB and navigate to the project directory.
Run the main script to simulate lane keeping and obstacle avoidance scenarios:
matlab
Copy code
run Prepare.m
View results through generated plots and performance metrics.
Dependencies
MATLAB with Optimization Toolbox
A basic understanding of state-space modeling and MPC theory is recommended.
