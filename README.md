# Autonomous Rover

This project aims to build an autonomous rover using GPS, vision, and inertial sensors for navigation.
The goal is to run everything onboard an embedded computer running Ubuntu with ROS.
The rover consists of a rocker-bogie 3D printed rover.

## Quickstart

### Simulation

Launch the simulation
```bash
roslaunch rover_simulation simulation.launch
```
Robot initial position and terrain are set through arguments passed to the launch file.

To move the robot you can use the RQT robot steering interface that will stream commands over the `cmd_vel` topic.

## Documentation

### Hardware

* Custom 3D printed rocker-bogie rover structure
* Processing board: Jetson TK1 board connected to
* RGBD sensor: Intel Realsense camera R200
* IMU (accelerometer, gyroscope, magnetometer and barometer)
* GPS


### Software
The current stack contains the following
* `rover_description` contains the robot description in URDF
* `rover_control` contains the controller parameters and localization pipeline
* `rover_simulation` contains launcher for simulation in Gazebo
