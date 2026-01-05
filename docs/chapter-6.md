---
title: 'Chapter 6: Sensory Data Ingestion'
sidebar_position: 7
---

# Chapter 6: Sensory Data Ingestion

This chapter outlines the process for receiving and routing data from various sensor modules into the ROS2 Nervous System. The sensory data ingestion layer is the robot's "senses", providing the information it needs to understand its environment.

## The Sensory Layer

The sensory layer is composed of a set of ROS2 nodes, each responsible for a specific sensor or group of sensors. These nodes perform the following functions:

- **Interface with the hardware:** They communicate with the sensor hardware using the appropriate drivers.
- **Process raw data:** They may perform some initial processing on the raw sensor data, such as filtering or calibration.
- **Publish data:** They publish the processed sensor data on a standardized topic, such as `/sensor_data`.

## Example: Lidar Node

A Lidar node in the sensory layer would be responsible for:

1.  Connecting to the Lidar sensor via its SDK.
2.  Receiving raw laser scan data.
3.  Converting the raw data into a ROS2 `sensor_msgs/LaserScan` message.
4.  Publishing the `LaserScan` message on the `/scan` topic.

The cognitive layer can then subscribe to the `/scan` topic to use the Lidar data for navigation and obstacle avoidance.
