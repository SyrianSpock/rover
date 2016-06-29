# Autonomous Rover

This project aims to build an autonomous rover using GPS, vision, and inertial sensors for navigation.
The goal is to run everything onboard an embedded computer running Ubuntu with ROS.
The rover consists of a modified RC car.

## Quickstart

### Simulation

Launch the simulation
```bash
roslaunch rover_simulation simulation.launch
```
Robot initial position and terrain are set through arguments passed to the launch file.

To move the robot you can run
```bash
rostopic pub /car/ackermann_cmd ackermann_msgs/AckermannDriveStamped \
    "{'drive':{'steering_angle':10, 'speed':0.3}}" -r 10
```

## Documentation

### Hardware

* RC Car chassis and motors
* Processing board: Jetson TK1 board connected to
* RGBD sensor: Intel Realsense camera R200
* IMU (accelerometer, gyroscope, magnetometer and barometer) 
* GPS


### Software
The current stack contains the following
* `rover_description` contains the robot description in URDF
* `rover_simulation` contains the controller parameters and launcher for simulation in Gazebo
