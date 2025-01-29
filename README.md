 ## Trajectory Tracking with a Differential Robot in ROS

This project implements a **trajectory tracking controller** for a differential mobile robot using **Robot Operating System (ROS)**. The robot is tasked with following a **lemniscate (figure-eight)** pattern within a simulated environment (Gazebo), and the controller computes the necessary control signals for the robot to stay on track while minimizing tracking errors.

## Project Overview

The primary goals of the project are:
- **Trajectory Tracking**: Ensure the robot follows a specific trajectory (lemniscate) accurately, minimizing tracking errors in position and orientation.
- **Real-Time Control**: Compute and publish the robot's control signals in real-time using ROS, and display key parameters such as displacement, angular velocity, and tracking errors.

### Key Features

1. **Differential Kinematic Model**:
   - The controller uses the kinematic model of the differential robot to compute linear and angular velocities required for trajectory tracking.
   - The model focuses on position and orientation (yaw) control, utilizing **Jacobian** transformations for velocity adjustments.

2. **ROS Integration**:
   - ROS nodes interact with Gazebo to simulate the robot’s environment.
   - The **/cmd_vel** topic is used to publish control signals (linear and angular velocities), while the **/odom** topic provides feedback for odometry and position updates.

3. **Error Feedback**:
   - Tracking errors (ex, ey) are calculated to monitor deviations from the desired trajectory.
   - The control system adjusts velocities to minimize these errors and improve trajectory tracking.

4. **Real-Time Visualization**:
   - Real-time tracking errors and performance can be visualized using **rqt_plot** and **RViz**, offering valuable insights into the controller's effectiveness.

### Results
- **Trajectory Tracking**: The robot successfully tracked the lemniscate trajectory with minimal errors in position and orientation.
- **Smooth Control**: The velocity profiles (linear and angular) were adjusted smoothly, ensuring stable operation and avoiding abrupt changes in speed or direction.

### Future Work
- Extend the controller to handle more complex trajectories and dynamic obstacles.
- Integrate additional sensors to improve perception and robustness for real-world applications.
