---
title: 'Chapter 9: Configuration Parameters'
sidebar_position: 10
---

# Chapter 9: Configuration Parameters

This chapter provides a list and description of the external parameters available to configure the behavior of the ROS2 Nervous System. These parameters allow you to tune the system for your specific robot and application without needing to modify the code.

## Parameter Management

The ROS2 Nervous System uses the standard ROS2 parameter system for configuration. Parameters are typically defined in a YAML file and loaded by the ROS2 launch system.

## Key Parameters

Below are some of the key parameters that can be configured:

### General Parameters

- `update_rate`: The main update rate of the cognitive layer, in Hz.
- `robot_name`: The name of the robot, used for identification.

### Topic Name Parameters

- `sensor_topic`: The name of the topic for processed sensor data. Default: `/sensor_data`.
- `state_topic`: The name of the topic for the robot's state. Default: `/robot_state`.
- `cmd_vel_topic`: The name of the topic for velocity commands. Default: `/cmd_vel`.

### Behavior Parameters

- `max_linear_velocity`: The maximum linear velocity of the robot, in m/s.
- `max_angular_velocity`: The maximum angular velocity of the robot, in rad/s.

By exposing these parameters, the ROS2 Nervous System allows for a high degree of flexibility and adaptability. You can easily create different configurations for different robots or different operating conditions.
