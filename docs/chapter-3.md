---
title: 'Chapter 3: Communication Interfaces'
sidebar_position: 4
---

# Chapter 3: Communication Interfaces

This chapter defines the standard communication interfaces used within the ROS2 Nervous System. These interfaces are the primary channels for data exchange between the different layers of the system.

## Standard Interfaces

The ROS2 Nervous System uses the following standard ROS2 interfaces:

- **Topics:** For continuous, one-way data streams.
- **Services:** For request-response interactions.
- **Actions:** For long-running tasks that provide feedback.

## Key Topics

Below are some of the key topics used in the system:

- `/sensor_data`: Publishes processed data from the sensory layer.
- `/robot_state`: Publishes the current state of the robot from the cognitive layer.
- `/cmd_vel`: Subscribes to velocity commands for the motor layer.

## Key Services

- `/get_robot_state`: A service to query the current state of the robot.
- `/trigger_behavior`: A service to trigger a specific behavior in the cognitive layer.

By standardizing these interfaces, the ROS2 Nervous System ensures that components can be easily interchanged and that the system as a whole is more modular and maintainable.
