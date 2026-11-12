# Concept of Operations (CONOPS): Requirements for a Mobile Robot Platform in MARS Research

- **Document ID:** `MARS-REQ-002`
- **Version:** `v1.0`
- **Date:** `2026-11-12`
- **Author:** Dhamdhawach Horsuwan
- **Phase:** Requirements Engineering
- **Project:** Multi-Agent Robotic Systems (MARS) Hardware Platform

---

## Introduction

In Multi-Agent Robotic Systems (MARS) research, investigators must develop, deploy, and operate multiple robots concurrently. Compared with single-robot research, this introduces additional challenges associated with hardware maintenance, software development, system integration, and coordination among multiple agents.

Based on practical experience operating a four-robot team, several platform requirements have been identified as particularly important for MARS research. These requirements extend beyond the fundamental capabilities of an individual mobile robot, addressing the additional complexity introduced by multi-agent interactions and fleet-level operations.

A suitable research platform should prioritize reliability, modularity, ease of maintenance, and cost-effectiveness. These characteristics are essential for supporting long-term experiments, simplifying hardware and software development, and enabling researchers to scale their experiments by deploying larger numbers of robots within limited budgets.

Furthermore, the platform should support both centralized monitoring and decentralized agent operation, allowing researchers to investigate different multi-agent architectures without being constrained by the underlying hardware infrastructure.

Usability and accessibility should also be considered fundamental design objectives. Even in research laboratories with professional engineers and software developers, users should not be assumed to possess specialized knowledge across every discipline involved in robotics. Since robotics integrates multiple fields of engineering and computer science, operating and maintaining the platform should not require expertise in all of these areas. Therefore, adopting usability principles commonly found in commercial products, such as intuitive interfaces, straightforward configuration, accessible diagnostics, and simplified maintenance procedures, can significantly reduce the learning curve. This approach also makes the platform easier to transfer to other researchers and users, promoting reproducibility, collaboration, and long-term adoption.

---

## Robot Requirements Overview

The requirements and operational concepts are organized into seven key areas:

1. **Modularity and Extensibility**
2. **Power Management**
3. **Mobility and Manipulation**
4. **Perception and Sensing**
5. **Localization and State Estimation**
6. **Multi-Agent Coordination and Communication**
7. **User Interface and Fleet Management**

Each requirement is accompanied by practical use-case scenarios to illustrate its relevance to MARS research. Specific hardware implementations, technical specifications, and development methodologies are discussed in subsequent sections.

---

## 1. Modularity and Extensibility

Research objectives and interdisciplinary collaborations frequently introduce evolving hardware and software requirements. Therefore, the robot platform should adopt a modular architecture that accommodates modifications, component replacements, and the integration of additional hardware.

A modular design promotes hardware and software reuse across different research projects, reducing development time and costs when establishing new experimental configurations. Furthermore, standardized mechanical interfaces, electrical connections, and communication protocols simplify system integration and maintenance as the fleet expands.

> **Use Case Scenario: Research Adaptability**
> Researchers may need to integrate different sensors, actuators, or communication modules to investigate new research problems. A modular platform allows these components to be added or replaced without redesigning the entire robot.

---

## 2. Power Management

### 2.1 Power Regulation

Lithium-based batteries are preferred because of their compact form factor and high energy density. However, battery voltage varies with the state of charge and instantaneous load conditions. Therefore, dedicated voltage regulation should provide stable supply voltages to critical electronic components and drive motors.

Maintaining consistent motor supply voltage helps minimize variations in motor performance and preserve predictable motion characteristics across all agents.

> **Use Case Scenario: Consistent Motor Performance**
> During prolonged swarm experiments, dedicated voltage regulation helps maintain consistent motor response across the fleet. Proper power regulation also prevents controller resets caused by voltage fluctuations during sudden motor load changes.

### 2.2 Battery Management and Protection

Lithium-based batteries introduce operational hazards associated with overcharge, overdischarge, excessive current, and abnormal temperature conditions. An appropriate Battery Management System (BMS) should incorporate protection mechanisms to mitigate these risks.

As the fleet size increases, the number of individual battery systems and associated failure points also increases. Therefore, integrated battery protection is essential for maintaining operational safety and reducing the risk of battery-related failures during experiments.

> **Use Case Scenario: Battery Protection**
> When deploying multiple robots simultaneously, individual battery protection systems help prevent overdischarge, excessive current draw, and unsafe operating temperatures during extended field experiments.

### 2.3 Exchangeable Battery or Power Module

The robot should support an exchangeable battery or power module to minimize downtime during experiments and simplify fleet maintenance. A modular power system allows researchers to replace depleted batteries quickly without waiting for individual units to recharge.

The power module should incorporate standardized mechanical mounting and electrical interfaces to ensure compatibility across all robots in the fleet. Furthermore, the connection mechanism should provide secure attachment, correct polarity, and reliable electrical contact while allowing convenient removal and replacement.

The design should also consider integrated battery protection and safe disconnection procedures to prevent electrical hazards during module replacement.

> **Use Case Scenario: Rapid Battery Replacement**
> During prolonged multi-agent experiments, robots with depleted batteries can be quickly returned to operation by replacing their power modules with fully charged units. This allows experiments to continue with minimal interruption while depleted batteries are recharged separately.

### 2.4 Fleet Charging Infrastructure

Charging a large fleet using individual battery chargers introduces considerable operational overhead and occupies valuable laboratory workspace. Therefore, the platform should support efficient fleet charging through centralized multi-port charging stations, shared power distribution systems, or automated docking stations.

A standardized charging interface also simplifies battery maintenance and reduces the time required to prepare robots for subsequent experimental runs.

> **Use Case Scenario: Fleet Power Maintenance**
> When operating a fleet of ten robots, centralized charging stations allow researchers to recharge multiple units simultaneously. Alternatively, automated docking stations can support autonomous battery replenishment, reducing manual intervention between experimental runs.

### 2.5 Power On/Off Control

The robot should incorporate an easily accessible physical power switch to allow operators to safely turn the system on and off. The power control mechanism should provide convenient access without requiring researchers to remove the enclosure to access, disconnect the battery, or remove the power module.

The power switch should be appropriately rated for the system's maximum operating voltage and current. Furthermore, the power architecture should distinguish between the main power supply and controlled shutdown of electronic subsystems to prevent unexpected system behavior or data loss.

An additional consideration is the implementation of an emergency power-disconnection mechanism that allows operators to quickly isolate the power supply when necessary.

> **Use Case Scenario: Operational Power Control**
> During multi-robot experiments, operators can quickly power individual robots on or off during deployment, maintenance, and troubleshooting. An accessible power switch also simplifies fleet preparation and reduces the risk of accidental electrical disconnection.

---

## 3. Mobility and Manipulation

### 3.1 Locomotion and Motor Control

The robot should support reliable and predictable locomotion suitable for multi-agent navigation and coordination. An omnidirectional or holonomic drive system is preferred because it decouples translational motion from robot orientation, simplifying trajectory planning and control algorithms.

Furthermore, closed-loop motor control using position feedback encoders is desirable for achieving consistent motion characteristics and reducing trajectory errors.

> **Use Case Scenario: Formation Control**
> During formation control experiments, low-cost DC motors equipped with reliable position feedback encoders provide sufficient motion control capabilities for executing predefined trajectories and maintaining relative positions among agents.

### 3.2 Object Transportation and Manipulation

The platform should provide a modular mechanical interface that supports physical interaction with the environment. Basic manipulation capabilities may include directly pushing lightweight objects or transporting payloads using interchangeable attachments, such as U-shaped claws designed to secure cylindrical objects.

Furthermore, the chassis should accommodate auxiliary actuators and specialized end-effectors, including electromagnets, heating elements, and vacuum suction systems, to support diverse research applications.

> **Use Case Scenario: Collaborative Object Transportation**
> Multiple robots can cooperate to transport objects that exceed the payload capacity of an individual robot. Interchangeable mechanical attachments allow researchers to investigate different object transportation and manipulation strategies without redesigning the entire platform.

---

## 4. Perception and Sensing

### 4.1 Environmental Perception

The robot should incorporate onboard sensors capable of providing low-latency spatial measurements and reliable obstacle detection. These measurements support local environmental awareness, real-time path planning, and collision avoidance.

The sensing system should provide sufficient update rates and detection ranges to accommodate the robot's maximum operating speed and the expected density of surrounding obstacles.

> **Use Case Scenario: Obstacle Avoidance**
> When navigating dynamic environments, robots must continuously detect obstacles and adjust their trajectories accordingly. High-frequency sensor measurements enable immediate local motion adjustments and reduce the likelihood of collisions.

> **Use Case Scenario: Reciprocal Collision Avoidance**
> In high-density multi-agent deployments, onboard perception allows robots to detect nearby agents and estimate their relative positions and movements. This information supports reciprocal collision avoidance strategies, enabling agents to adjust their trajectories cooperatively while minimizing unnecessary stops and deadlocks.

---

## 5. Localization and State Estimation

### 5.1 Pose Estimation

Each robot requires a reliable state estimation system to determine its position and orientation within the operating environment. This can be achieved by combining onboard wheel odometry and inertial measurement unit (IMU) data with external tracking systems or vision-based localization methods.

Sensor fusion helps compensate for the limitations of individual sensors, improving the accuracy and robustness of pose estimation.

> **Use Case Scenario: Coordinate Alignment**
> Consistent pose estimation allows individual robots to express their positions within a shared global coordinate frame. This enables agents to interpret spatial information consistently and coordinate their movements within a common map reference.

---

## 6. Multi-Agent Coordination and Communication

### 6.1 Inter-Robot Communication

Reliable wireless communication is essential for information exchange and coordination among agents. The communication system should provide sufficiently low latency, adequate throughput, and reliable data transmission to support decentralized coordination and state synchronization.

Furthermore, the communication architecture should support direct information exchange between neighboring agents without requiring every communication transaction to pass through a central server.

> **Use Case Scenario: Distributed Task Allocation**
> Participating agents exchange relevant state information and negotiate task assignments autonomously. This enables distributed task allocation and coordination without relying on a centralized decision-making server.

### 6.2 Decentralized Network Architecture

The communication architecture should support decentralized network topologies, allowing robots to establish direct peer-to-peer connections with neighboring agents.

Unlike conventional infrastructure-based wireless networks that depend on a centralized access point, decentralized communication architectures can reduce dependence on fixed infrastructure and eliminate certain single points of failure.

The network should also accommodate changes in connectivity as robots move throughout the environment, supporting dynamic network topologies and scalable multi-agent deployments.

> **Use Case Scenario: Infrastructure-Independent Operation**
> When deploying robots in environments without existing wireless infrastructure, agents can communicate directly with one another through peer-to-peer connections. This allows the fleet to operate without depending on a dedicated wireless access point.

---

## 7. User Interface and Fleet Management

### 7.1 Fleet Monitoring and Control

A centralized monitoring interface should provide operators with an overview of individual robot states and overall fleet performance. Essential capabilities include monitoring battery levels, communication status, operational states, and sensor information.

The interface should also support fleet-level commands, such as starting, pausing, and stopping experiments, as well as distributing software updates when required.

Importantly, centralized monitoring and command interfaces should remain independent of the agents' internal decision-making processes, allowing decentralized algorithms to operate without relying on a central controller.

> **Use Case Scenario: Experiment Management**
> During experimental trials, operators use monitoring software to inspect individual robot statuses, record system telemetry, and issue fleet-wide pause or emergency-stop commands when necessary.

### 7.2 Onboard User Interface

An onboard user interface should provide convenient access to essential robot information and configuration parameters. A small graphical display can be particularly useful during hardware development, firmware updates, and system debugging.

The display may provide information such as the robot's identification number, network configuration, MAC address, battery voltage, and operational status.

At least one button should be provided to cycle display data, enter calibration, configuration, or pairing mode, and start or stop onboard data recording.

> **Use Case Scenario: Onboard Diagnostics**
> During firmware development, researchers can quickly inspect network configurations and runtime parameters directly on the robot without connecting an external computer or accessing serial debugging interfaces.

### 7.3 Visual Status Indicators

The robot should incorporate multi-color signal LEDs to communicate its operational status through simple visual indications. These indicators provide immediate feedback and simplify diagnostics when multiple robots are operating simultaneously.

Possible status indications include normal operation, low battery, communication loss, initialization, and system errors.

> **Use Case Scenario: Fleet Diagnostics**
> When monitoring multiple robots in a laboratory or field environment, visual indicators allow researchers to identify malfunctioning or disconnected units quickly without inspecting each robot individually.

### 7.4 Experimental Data Acquisition and Monitoring Software

Dedicated monitoring software should support experimental data acquisition, visualization, and performance analysis across the entire fleet.

The software should collect relevant telemetry from individual agents, maintain experimental logs, and provide tools for analyzing system behavior over time. This enables researchers to evaluate algorithm performance, investigate unexpected behaviors, and compare experimental results across different configurations.

> **Use Case Scenario: Multi-Agent Performance Evaluation**
> During scalability experiments, monitoring software collects information such as robot trajectories, communication statistics, task completion times, and individual agent states. Researchers can subsequently analyze these datasets to evaluate the performance and scalability of different multi-agent coordination algorithms.

