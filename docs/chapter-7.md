---
title: 'Chapter 7: Actuator Command Egress'
sidebar_position: 8
---

# Chapter 7: Actuator Command Egress

This chapter details the process for sending commands to motor controllers and other actuators from the ROS2 Nervous System. The actuator command egress layer is the robot's "muscles", allowing it to act on its environment.

## The Motor Layer

The motor layer is composed of a set of ROS2 nodes, each responsible for controlling a specific actuator or group of actuators. These nodes perform the following functions:

- **Subscribe to commands:** They subscribe to command topics, such as `/cmd_vel`, to receive instructions from the cognitive layer.
- **Interface with the hardware:** They communicate with the motor controllers and other actuator hardware using the appropriate drivers.
- **Provide feedback:** They may publish feedback on the status of the actuators, such as the current position or velocity of a motor.

## Example: Drive System Node

A drive system node in the motor layer would be responsible for:

1.  Subscribing to the `/cmd_vel` topic to receive `geometry_msgs/Twist` messages.
2.  Converting the `Twist` messages into low-level commands for the motor controllers (e.g., PWM signals).
3.  Sending the commands to the motor controllers.
4.  Optionally, publishing odometry information based on feedback from the motors.

This separation of concerns allows the cognitive layer to issue high-level commands without needing to know the low-level details of how the motors are controlled.
