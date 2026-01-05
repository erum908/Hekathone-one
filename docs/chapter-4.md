---
title: 'Chapter 4: Data Types and Schemas'
sidebar_position: 5
---

# Chapter 4: Data Types and Schemas

This chapter provides a specification of the custom message and service data structures used in the ROS2 Nervous System. These custom types ensure that data is exchanged in a structured and predictable way.

## Custom Message Types

### `RobotState.msg`

This message provides a comprehensive snapshot of the robot's current state.

```
# RobotState.msg
std_msgs/Header header
string mode
float64 battery_level
# ... other state variables
```

### `SensorData.msg`

This message is used to publish processed data from the sensory layer.

```
# SensorData.msg
std_msgs/Header header
string sensor_name
float64[] values
```

## Custom Service Types

### `GetRobotState.srv`

This service allows other nodes to query the current state of the robot.

```
# GetRobotState.srv
---
RobotState state
```

By defining these custom data types, we create a clear and explicit API for the different components of the ROS2 Nervous System. This makes the system easier to debug and maintain.
