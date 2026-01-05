---
title: 'Chapter 2: Core Architecture'
sidebar_position: 3
---

# Chapter 2: Core Architecture

In this chapter, we will explore the core architecture of the ROS2 Nervous System. We will look at the fundamental components and how they interact with each other to create a cohesive and powerful system.

## The Three Main Layers

The ROS2 Nervous System is structured into three main layers:

1.  **The Sensory Layer:** This layer is responsible for gathering information from the robot's sensors. It takes raw sensor data and processes it into a format that can be used by the rest of the system.
2.  **The Cognitive Layer:** This is the "brain" of the system. It is where the robot's state is managed, decisions are made, and behaviors are executed. This layer is often implemented using behavior trees or state machines.
3.  **The Motor Layer:** This layer is responsible for controlling the robot's actuators. It takes commands from the cognitive layer and translates them into physical actions.

This layered architecture provides a clear separation of concerns and makes it easier to develop and maintain complex robotic systems.

## Communication Patterns

The ROS2 Nervous System uses a set of standard communication patterns to ensure that the different layers can communicate with each other in a reliable and predictable way. These patterns are based on the standard ROS2 interfaces:

- **Topics:** Used for streaming data, such as sensor readings or state updates.
- **Services:** Used for request/response interactions, such as querying the state of a component or triggering an action.
- **Actions:** Used for long-running tasks that provide feedback, such as navigating to a goal or manipulating an object.

By adhering to these standard patterns, the ROS2 Nervous System ensures that your application is interoperable with the wider ROS2 ecosystem.
