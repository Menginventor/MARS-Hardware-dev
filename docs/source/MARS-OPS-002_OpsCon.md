# MARS-OPS-002
# System Operational Concept (OpsCon)

## General-Purpose Research-Class Lightweight Mobile Robot Platform for Multi-Agent Robotic Systems

| Document Information | Description |
|---|---|
| Document ID | MARS-OPS-002 |
| Document Title | System Operational Concept (OpsCon) |
| System | MARS Research-Class Lightweight Mobile Robot Platform |
| Author | Dhamdhawach Horsuwan |
| Version | v1.0 |
| Release Date | 2026-11-12 |
| Document Type | System Operational Concept (OpsCon) |
| Related Document | MARS-OPS-001 — Concept of Operations |
| Reference Standard | ISO/IEC/IEEE 29148:2018 |

---

# 1. Introduction

## 1.1 Purpose

This System Operational Concept (OpsCon) describes how the Multi-Agent Robotic Systems (MARS) platform is intended to operate and interact with its users, supporting systems, and operational environment.

It establishes the system-level operational concept, including robot configurations, operational modes, human-system interaction, communication, experiment execution, and system lifecycle activities.

The document provides a common understanding of how individual robotic agents and multi-robot configurations are prepared, operated, monitored, and maintained.

It also establishes the expected interactions between the robotic platform, researchers, operators, and external systems throughout the operational lifecycle.

## 1.2 Scope

This document covers the system-level operation of a general-purpose Research-Class Lightweight Mobile Robot (RCLMR) platform intended for Multi-Agent Robotic Systems research.

The operational scope includes:

- Individual mobile robot operation.
- Multi-robot cooperative operation.
- Physical robot-to-robot connection and disconnection.
- Composite robotic system operation.
- Manual wireless robot control.
- Autonomous robot operation.
- Centralized fleet supervision.
- Decentralized robot coordination.
- Integration of sensors and small manipulation mechanisms.
- Experiment preparation, configuration, execution, and evaluation.
- Operational monitoring and recovery.
- Battery management, maintenance, and system updates.

This document describes expected system behavior and interactions rather than prescribing detailed implementation technologies.

## 1.3 Relationship to ConOps

The ConOps establishes the broader research mission and operational context.

This OpsCon translates that concept into a system-specific operational perspective.

| Aspect | ConOps | OpsCon |
|---|---|---|
| Primary perspective | Research laboratory | Robotic platform |
| Main question | Why and where is the platform used? | How does the platform operate? |
| Focus | Research applications and operational scenarios | System configurations, modes, interactions, and procedures |
| Users | Research stakeholders | System users and operators |
| Outputs | Operational objectives and scenarios | System operational behavior and interfaces |

## 1.4 System Boundary

The MARS platform consists of individual robotic agents and the supporting infrastructure required to configure, operate, and monitor them.

The system boundary includes:

1. Individual robotic agents.
2. Mechanical interfaces for robot-to-robot connection.
3. Onboard sensing and actuation.
4. Onboard computation and control.
5. Robot-to-robot communication.
6. Wireless operator-control interfaces.
7. External monitoring and fleet-management interfaces.
8. Supporting power and charging infrastructure.
9. Experiment configuration and data-management facilities.

External research algorithms, experimental objects, laboratory infrastructure, and development computers may interact with the platform but are not necessarily part of the core robotic system.

---

# 2. System Overview

## 2.1 System Description

The MARS platform is a collection of lightweight mobile robotic agents intended to support research and experimentation in multi-agent robotic systems.

Each robot is an independent physical unit with its own onboard computational, sensing, actuation, and communication capabilities.

Robots may operate individually or cooperate with other robots to accomplish shared objectives.

The platform additionally supports physical robot-to-robot connection, allowing multiple independent robotic agents to form a larger composite robotic configuration.

Depending on the experiment, connected robots may coordinate their actions while retaining their individual computational identities.

The platform is intended to support both manually controlled and autonomous operation, with centralized supervision and decentralized coordination available according to the experimental requirements.

## 2.2 Robot Classification

The platform is provisionally classified as a:

**Research-Class Lightweight Mobile Robot (RCLMR).**

This is a project-specific engineering classification describing the intended physical characteristics and application of the platform. It is not an established international safety classification.

The preliminary design envelope is:

| Parameter | Preliminary Characteristic |
|---|---|
| Individual robot mass | Less than 1 kg |
| Normal operating speed | Up to 0.5 m/s |
| Extended operating speed | Up to 1.0 m/s |
| Mobility | Compact wheeled mobile robot |
| Manipulation | Optional small servo-actuated gripper |
| Power | Battery-powered |
| Control | Manual wireless and autonomous |
| Communication | Robot-to-robot and robot-to-operator |
| Intended environment | Primarily controlled research environments |
| Handling | Manually liftable by one person |

These values are preliminary design targets, not demonstrated safety thresholds.

The operating envelope of composite configurations must be assessed separately because connecting multiple robots changes the total moving mass and mechanical interaction characteristics.

## 2.3 System Composition

The platform is conceptually composed of the following subsystems.

| Subsystem | Operational Responsibility |
|---|---|
| Mobility | Provides robot movement and locomotion. |
| Power Management | Supplies and manages electrical power. |
| Computation and Control | Executes onboard software, control algorithms, and research applications. |
| Perception and Sensing | Acquires information about the robot and its environment. |
| Localization | Estimates the robot's position and movement. |
| Communication | Exchanges information between robots and external systems. |
| Manipulation | Performs physical interaction with objects through optional mechanisms. |
| Mechanical Reconfiguration | Enables physical connection and disconnection between robotic agents. |
| User Interface | Provides onboard status information and basic user interaction. |
| Fleet Management | Supports external monitoring, configuration, and supervision of multiple robots. |

The specific implementation and allocation of these functions are addressed in subsequent system architecture and requirements engineering activities.

---

# 3. System Actors and External Entities

## 3.1 Human Actors

The platform interacts with several categories of users.

| Actor | Operational Responsibilities |
|---|---|
| Researcher | Defines experiments, develops algorithms, configures robots, and evaluates results. |
| Experiment Operator | Prepares robots, deploys the team, monitors operation, and performs intervention. |
| Robot Developer | Develops and integrates hardware, firmware, and software. |
| Laboratory Technician | Performs inspection, charging, maintenance, and equipment management. |
| Principal Investigator | Supervises research activities and evaluates experimental outcomes. |

A person may perform multiple roles during an experiment.

## 3.2 External Entities

The platform may interact with the following external entities.

| External Entity | Interaction |
|---|---|
| Wireless Controller | Sends manual movement and operational commands. |
| Monitoring Computer | Displays robot and fleet information. |
| Experiment Computer | Configures and executes research algorithms. |
| External Sensors | Provides additional environmental or experimental information. |
| Experimental Objects | Objects used in transportation, manipulation, or interaction experiments. |
| Charging Equipment | Supplies electrical energy to robotic agents. |
| Simulation Environment | Supports simulation-based experimentation and algorithm development. |
| Laboratory Infrastructure | Provides the physical operating environment and supporting facilities. |

---

# 4. System Operational Configurations

The platform supports different physical configurations and operational arrangements.

Physical configuration, control authority, and coordination architecture are treated as separate dimensions.

## 4.1 Physical Configurations

### 4.1.1 Independent Robot

Each robot operates as an independent physical and computational agent.

The robot may perform an individual task, navigate independently, or participate in a multi-robot experiment.

### 4.1.2 Cooperative Multi-Robot Team

Multiple independent robots cooperate to accomplish a shared objective.

Each robot retains its own physical structure and computational identity.

Robots may exchange information and coordinate their actions.

### 4.1.3 Composite Robot

Two or more robots physically connect to form a larger robotic configuration.

The connected robots operate as a coordinated physical system.

The individual agents may retain their onboard computational capabilities and communicate internally or externally.

### 4.1.4 Mixed Configuration

A team may contain independent robots and one or more composite robotic systems.

This configuration supports experiments involving interactions between individual agents and connected groups.

## 4.2 Control Authority

The platform is intended to support two primary control arrangements.

**Manual Control**

A human operator directly controls a robot through a wireless interface.

**Autonomous Control**

The robot executes an assigned task using onboard algorithms without requiring continuous human movement commands.

Manual and autonomous control may coexist within the same multi-robot experiment, subject to defined control-authority rules.

## 4.3 Coordination Architecture

The platform supports different approaches to multi-robot coordination.

| Architecture | Description |
|---|---|
| Centralized | A central system coordinates robot decisions or assigns tasks. |
| Decentralized | Individual robots make local decisions and coordinate through information exchange. |
| Hybrid | Centralized supervision or task assignment coexists with decentralized robot decision-making. |

The selected architecture depends on the research objective.

Centralized monitoring does not necessarily imply centralized autonomous control.

## 4.4 Configuration Matrix

The three operational dimensions can be combined.

| Physical Configuration | Manual Control | Autonomous Control | Coordination |
|---|---|---|---|
| Independent robot | Supported | Supported | Individual or externally coordinated |
| Cooperative team | Individual robot control | Supported | Centralized, decentralized, or hybrid |
| Composite robot | Subject to control-interface availability | Supported | Centralized or distributed |
| Mixed configuration | Supported | Supported | Centralized, decentralized, or hybrid |

Not every combination must be implemented simultaneously. The matrix defines the intended operational flexibility.

---

# 5. System Operational Modes

## 5.1 Overview

The platform supports several operational modes corresponding to its lifecycle and operational functions.

| Mode | Description |
|---|---|
| Power-Off | Robot is electrically switched off. |
| Initialization | Robot starts and initializes its onboard systems. |
| Standby | Robot is initialized and waiting for commands or experiment execution. |
| Manual Wireless Control | Operator directly controls robot movement and selected functions. |
| Independent Autonomous Operation | Individual robot autonomously executes its assigned task. |
| Cooperative Autonomous Operation | Multiple robots coordinate to execute a shared task. |
| Composite Operation | Physically connected robots operate as a composite system. |
| Reconfiguration | Robots establish or release physical connections. |
| Monitoring | Robot or fleet information is made available to users. |
| Recovery | Robot or team performs recovery activities after an interruption or fault. |
| Maintenance | Robot is placed in a condition suitable for inspection and maintenance. |

## 5.2 Power-Off Mode

The robot is electrically switched off.

In this condition, normal onboard computation, communication, and actuation are unavailable.

The robot may be transported, stored, charged, or prepared for subsequent operation according to its power-system design.

## 5.3 Initialization Mode

The robot starts its onboard systems and performs necessary initialization activities.

These may include:

- Hardware initialization.
- Sensor initialization.
- Communication initialization.
- Battery and power-system checks.
- Software initialization.
- Configuration loading.
- System diagnostics.

After successful initialization, the robot transitions to Standby.

If a critical initialization failure occurs, the robot should enter a defined fault or recovery condition.

## 5.4 Standby Mode

The robot is operationally ready but is not performing a movement or manipulation task.

In this mode, the robot may:

- Receive configuration parameters.
- Establish communication connections.
- Receive experiment commands.
- Report operational status.
- Wait for manual control.
- Wait for autonomous task execution.

## 5.5 Manual Wireless Control Mode

An operator remotely controls an individual robot using a wireless controller or computer-based interface.

Available functions may include:

- Forward and backward movement.
- Turning and rotational movement.
- Movement speed adjustment.
- Gripper opening and closing, where available.
- Selected operational commands.
- Manual positioning and recovery.

The robot receives operator commands and executes the corresponding actions.

The control interface should provide sufficient feedback for the operator to understand the robot's operational condition.

Loss of the wireless control connection must result in a defined response appropriate to the operating context.

Manual control does not replace emergency-stop or other required safety functions.

## 5.6 Independent Autonomous Operation Mode

An individual robot autonomously performs an assigned task.

The robot uses its onboard sensing, computation, and control capabilities to determine and execute its actions.

The operator may monitor its status and intervene when necessary.

## 5.7 Cooperative Autonomous Operation Mode

Multiple robots cooperate to accomplish a shared objective.

Robots may exchange information, allocate tasks, coordinate movement, and update their decisions according to the selected research algorithm.

The coordination mechanism may be centralized, decentralized, or hybrid.

## 5.8 Composite Operation Mode

Multiple physically connected robots operate as a composite robotic system.

The connected agents coordinate their actions to achieve a shared physical objective.

The composite configuration may perform movement, transportation, or other tasks according to the experiment.

The control arrangement may involve a shared control process or distributed control among the connected agents.

## 5.9 Reconfiguration Mode

Robots establish or release physical connections to change their overall configuration.

The reconfiguration process may be initiated by:

- An autonomous algorithm.
- An operator command.
- An experimental procedure.

The system should establish the resulting physical and operational configuration before proceeding with the next task.

## 5.10 Monitoring Mode

Robot and fleet information is presented to researchers or operators.

Information may include:

- Robot identity.
- Operational mode.
- Position and movement status.
- Battery condition.
- Communication connectivity.
- Sensor and subsystem status.
- Task progress.
- Fault and warning information.

Monitoring may be performed through onboard interfaces or external software.

## 5.11 Recovery Mode

The robot or team performs recovery activities following an interruption or abnormal condition.

Recovery may involve:

- Returning to a safe or stationary condition.
- Manual wireless control.
- Reinitialization.
- Communication reconnection.
- Physical retrieval.
- Battery replacement or charging.
- Operator intervention.

The appropriate recovery procedure depends on the nature of the fault and operating environment.

## 5.12 Maintenance Mode

The robot is placed in a condition suitable for inspection, servicing, repair, or component replacement.

Normal autonomous task execution is not expected during maintenance.

Maintenance personnel should be able to identify the operational condition of the robot and prevent unintended movement during maintenance activities.

---

# 6. System Operational Procedures

## 6.1 General Experiment Lifecycle

A typical experiment follows the operational sequence below.

### Phase 1 — Preparation

The researcher defines the experiment objective and prepares the experimental environment.

The required robots, accessories, sensors, and software are selected.

### Phase 2 — Inspection and Initialization

The operator inspects the robots and verifies their readiness.

The robots are powered on and initialized.

### Phase 3 — Configuration

The researcher configures:

- Robot identities.
- Number of participating agents.
- Robot roles.
- Initial positions.
- Experimental parameters.
- Coordination algorithms.
- Communication settings.
- Required operational configuration.

### Phase 4 — Deployment

Robots are placed in the experimental environment.

The operator verifies that the participating robots are ready for operation.

### Phase 5 — Execution

The experiment begins.

Robots perform their assigned tasks using manual or autonomous control as defined by the experiment.

### Phase 6 — Monitoring

Researchers observe robot status, task progress, and overall system behavior.

The operator may intervene when necessary.

### Phase 7 — Data Collection

Experimental information is collected for subsequent analysis.

### Phase 8 — Termination

The experiment is terminated.

Robots stop their assigned tasks and transition to an appropriate operational condition.

### Phase 9 — Reset and Maintenance

Robots are inspected, recharged, reconfigured, or maintained as necessary before subsequent experiments.

## 6.2 Manual Wireless Operation Procedure

1. Operator prepares the robot and wireless controller.
2. Robot is powered on and initialized.
3. Operator establishes a wireless control connection.
4. Operator verifies robot identity and control availability.
5. Operator issues movement or selected function commands.
6. Robot executes the commands.
7. Operator observes robot response.
8. Operator terminates manual control.
9. Robot returns to Standby or another permitted mode.

## 6.3 Autonomous Experiment Procedure

1. Researcher prepares the experimental algorithm.
2. Robot or team is initialized.
3. Experiment parameters and task objectives are configured.
4. Robots receive their assigned tasks.
5. Autonomous execution begins.
6. Robots perform their assigned activities.
7. Researchers monitor operational progress.
8. The experiment terminates or is interrupted.
9. Robots return to an appropriate operational condition.

## 6.4 Multi-Robot Configuration Procedure

1. Researchers determine the required number of robots.
2. Robots are individually prepared and initialized.
3. Robot identities and communication relationships are established.
4. The desired team configuration is selected.
5. Robots are deployed.
6. The team begins the assigned experiment.
7. Robot interactions and team performance are monitored.
8. The experiment is terminated or reconfigured.

## 6.5 Composite Robot Formation Procedure

1. Individual robots are prepared for physical connection.
2. Robots approach their designated connection positions.
3. The docking process is initiated.
4. Physical connections are established.
5. The resulting configuration is checked.
6. The connected agents establish the required operational coordination.
7. The composite system performs its assigned task.
8. The composite system stops or prepares for disconnection.
9. Robots disconnect when required.
10. Individual agents return to independent operation.

The detailed docking mechanism and connection-verification method remain subject to system design.

---

# 7. Human-System Interaction

## 7.1 Interaction Overview

The platform provides interaction through onboard and external interfaces.

The interaction concept aims to allow researchers and operators to configure, control, and monitor the robots without requiring direct access to internal hardware or software.

## 7.2 Onboard Interface

Each robot is expected to provide basic onboard interaction capabilities.

These may include:

- Operational status indication.
- Battery and power status.
- Communication status.
- Mode indication.
- Basic configuration access.
- Wireless pairing.
- Data-recording control.
- Selected diagnostic functions.

Physical buttons and visual indicators may be used to support these functions.

## 7.3 Wireless Manual Control Interface

The wireless control interface allows an operator to control an individual robot remotely.

It may be implemented through a handheld controller or computer-based application.

The interface should provide:

- Robot selection or identification.
- Movement commands.
- Speed adjustment.
- Selected function commands.
- Connection-status feedback.
- Operational feedback.

## 7.4 Fleet Monitoring Interface

An external monitoring interface may provide an overview of the entire robot team.

The interface is intended to support:

- Robot identification.
- Fleet status monitoring.
- Robot position visualization.
- Communication status monitoring.
- Battery monitoring.
- Experiment progress monitoring.
- Operator commands.
- Fault and warning notifications.

The monitoring interface is not required to participate in every autonomous decision.

## 7.5 Experiment Configuration Interface

Researchers may use external software to configure experimental parameters.

Configuration activities may include:

- Selecting robot identities.
- Defining task objectives.
- Assigning robot roles.
- Configuring algorithms.
- Setting communication parameters.
- Defining initial conditions.
- Configuring data recording.

The exact configuration interface depends on the software architecture.

## 7.6 Control Authority

The platform should maintain a clear distinction between:

- Human movement commands.
- Autonomous algorithm commands.
- Fleet-management commands.
- Emergency intervention.

The system should define how conflicting commands are handled and how control authority changes between manual and autonomous operation.

Emergency intervention must remain independent of ordinary operational commands.

---

# 8. Communication and Information Exchange

## 8.1 Communication Overview

The platform supports communication between robotic agents and external systems.

Communication is required for manual control, robot coordination, monitoring, configuration, and experimental data exchange.

## 8.2 Robot-to-Robot Communication

Robots may exchange information directly or through supporting communication infrastructure.

Information may include:

- Robot identity.
- Position and motion information.
- Operational state.
- Task assignments.
- Perception information.
- Coordination messages.
- Reconfiguration information.
- Fault and status notifications.

## 8.3 Robot-to-Operator Communication

Robots may exchange information with wireless controllers and external monitoring systems.

This communication supports:

- Manual movement commands.
- Mode selection.
- Operational configuration.
- Status reporting.
- Monitoring.
- Operator intervention.

## 8.4 Communication Limitations

Communication conditions may vary according to the experimental environment.

The platform is intended to support research into:

- Limited communication range.
- Intermittent connectivity.
- Communication delay.
- Packet loss.
- Network partitioning.
- Changes in network topology.

The behavior of robots during communication interruption should be defined according to their current operational mode.

## 8.5 Communication Independence

The loss of an external monitoring connection should not automatically terminate all autonomous activities.

Where appropriate, robots should retain the ability to perform local operations and continue decentralized coordination.

However, loss of manual control communication must result in a defined response that prevents unintended behavior.

---

# 9. Operational Faults and Recovery

## 9.1 General Concept

The platform should provide defined responses to operational abnormalities.

The response depends on the affected subsystem, current operating mode, and experimental context.

## 9.2 Communication Failure

Potential conditions include:

- Loss of operator wireless control.
- Loss of robot-to-robot communication.
- Loss of external monitoring connectivity.
- Temporary network partitioning.

The system should distinguish between loss of operator control and loss of inter-robot communication.

These conditions may require different responses.

## 9.3 Battery Depletion

When battery capacity becomes insufficient for continued operation, the robot should provide an appropriate warning or status indication.

Depending on the operational context, the robot may:

- Complete a controlled stop.
- Terminate its assigned task.
- Return to a designated location.
- Request operator intervention.
- Enter a recovery condition.

## 9.4 Robot Failure

A robot may experience hardware, software, sensing, or communication failure.

The remaining robots may continue operating depending on the experiment and the nature of the failure.

Researchers should be able to identify the affected robot and evaluate the impact on the overall team.

## 9.5 Sensor Failure

If required sensor information becomes unavailable or unreliable, the robot should follow a defined response appropriate to its assigned task.

This may involve stopping, switching to an alternative operating strategy, or requesting operator intervention.

## 9.6 Physical Connection Failure

Potential conditions include:

- Failed docking.
- Incomplete physical connection.
- Unexpected disconnection.
- Mechanical damage.
- Incorrect composite configuration.

The system should not assume that a physical connection is valid until its required connection conditions have been established.

## 9.7 Recovery Principles

Recovery activities should follow these general principles:

1. Identify the affected robot or subsystem.
2. Determine the operational condition.
3. Prevent further unintended movement or interaction.
4. Notify the operator when intervention is required.
5. Restore normal operation only when appropriate.
6. Record relevant failure information for subsequent analysis.

---

# 10. Safety and Risk Considerations

## 10.1 Safety Philosophy

The MARS platform is intended to be a lightweight research robotic system with relatively low mechanical energy compared with larger industrial mobile robots.

However, lightweight construction and low operating speed do not automatically establish that the system is safe.

Potential hazards must be evaluated according to the complete robot configuration and intended operating conditions.

ISO 12100 is proposed as the primary reference for machinery risk assessment and risk reduction, subject to applicability.

Other relevant safety standards may be considered according to the final system scope.

## 10.2 Individual Robot Hazards

Potential hazards include:

- Collision with people or objects.
- Pinching by moving components.
- Sharp edges or protruding components.
- Unexpected movement.
- Electrical faults.
- Battery overheating or failure.

## 10.3 Manipulator Hazards

The optional small servo-actuated gripper introduces additional mechanical hazards.

Potential hazards include:

- Finger pinching.
- Localized crushing.
- Unexpected gripper actuation.
- Mechanical trapping.
- Contact with exposed moving linkages.

The manipulator should be evaluated separately and as part of the complete robotic system.

## 10.4 Multi-Robot Hazards

Multi-robot operation introduces hazards associated with interactions between multiple moving agents.

These include:

- Robot-to-robot collisions.
- Unexpected cooperative movement.
- Interference during transportation.
- Mechanical trapping between robots.
- Unexpected movement during coordination failure.

## 10.5 Composite Robot Hazards

A composite robot may have a greater total mass and different mechanical characteristics than an individual robot.

The composite configuration should therefore be assessed using its actual total moving mass, speed, geometry, actuation, and potential contact conditions.

The individual robot mass limit should not automatically be treated as the composite system mass limit.

## 10.6 Manual Control Safety

Manual wireless control should consider:

- Unintended movement.
- Wireless connection interruption.
- Incorrect operator commands.
- Unexpected mode transitions.
- Simultaneous conflicting commands.

## 10.7 Emergency Intervention

Emergency intervention should remain available independently of normal autonomous and manual control functions.

A software pause, wireless stop command, or ordinary power switch should not automatically be considered a safety-rated emergency-stop function.

Detailed safety requirements will be established through risk assessment and subsequent system requirements engineering.

---

# 11. Power and Charging Operations

## 11.1 Power Operation

Each robot operates using an onboard electrical power source.

The power system supplies the energy required by computation, sensing, communication, mobility, and optional manipulation.

## 11.2 Battery Management

The platform is expected to provide appropriate battery-status information.

This may include:

- Remaining battery capacity.
- Battery voltage.
- Charging status.
- Battery fault conditions.
- Low-battery warnings.

## 11.3 Battery Replacement

Where exchangeable batteries or power modules are provided, the operator should be able to replace them through a defined procedure.

Battery replacement should not require unnecessary disassembly of the robot.

## 11.4 Charging Infrastructure

Robots are charged between experiments using the designated charging arrangement.

The charging process should provide appropriate protection and status indication.

## 11.5 Power-On and Power-Off

The operator should be able to switch the robot on and off through an accessible physical control.

The normal power switch and emergency intervention functions are separate operational concepts.

---

# 12. Maintenance and Lifecycle Operations

## 12.1 Preparation

Before deployment, the operator performs appropriate inspection and preparation activities.

These include:

- Mechanical inspection.
- Battery inspection.
- Sensor inspection.
- Communication checks.
- Software and configuration checks.
- Verification of optional attachments.

## 12.2 Routine Maintenance

Routine maintenance may include:

- Cleaning.
- Mechanical inspection.
- Wheel and drivetrain inspection.
- Sensor calibration.
- Battery replacement.
- Gripper inspection.
- Docking-interface inspection.
- Firmware and software updates.

## 12.3 Software Maintenance

The platform should support the development and updating of experimental software.

Researchers may update algorithms and application software while maintaining the integrity of the underlying platform functions.

## 12.4 Hardware Modification

The platform may be modified through the integration of additional sensors, modules, and experimental attachments.

Hardware modifications should be evaluated for their effects on:

- Robot mass.
- Mobility.
- Power consumption.
- Stability.
- Communication.
- Mechanical safety.
- Operational behavior.

## 12.5 Storage and Transportation

Robots may be stored and transported between experiments.

The storage and transportation arrangement should protect the robot, battery, sensors, and mechanical connection interfaces.

## 12.6 Retirement and Replacement

When a robot or subsystem becomes unsuitable for further use, it may be repaired, replaced, or retired.

Retired components should be handled according to applicable laboratory procedures and electrical or battery safety practices.

---

# 13. Operational Data and Experiment Management

## 13.1 Experiment Data

The platform is intended to support the collection of information required for research evaluation.

Potential data include:

- Robot position and movement.
- Robot operational state.
- Sensor measurements.
- Communication information.
- Battery status.
- Task execution progress.
- Coordination information.
- Manipulation or docking events.
- Fault and recovery events.

## 13.2 Data Recording

Data may be recorded onboard individual robots or through external monitoring systems.

The recording arrangement may vary according to the research experiment.

## 13.3 Data Retrieval

Researchers should be able to retrieve experiment data for subsequent analysis.

The data-management approach should support the association of recorded information with the relevant robot, experiment, and configuration.

## 13.4 Experimental Reproducibility

The platform should support recording relevant experimental parameters and configurations.

This information may include:

- Robot identities.
- Software versions.
- Algorithm configurations.
- Initial conditions.
- Robot configurations.
- Communication settings.
- Experimental environment.
- Operating parameters.

The objective is to support repeatable experiments and meaningful comparison of results.

---

# 14. Operational Scenarios and System Responsibilities

The following matrix maps the intended research applications to the main system functions involved.

| Research Application | Main System Functions | Operational Configuration |
|---|---|---|
| Self-Reconfigurable Multi-Robot Systems | Mobility, communication, docking, coordination | Independent, composite, mixed |
| Multi-Robot Object Transportation | Mobility, manipulation, communication, coordination | Cooperative, composite |
| Multi-Robot Navigation | Mobility, sensing, localization, communication | Independent, cooperative |
| Search and Rescue | Perception, localization, navigation, communication, exploration | Cooperative |
| Region Sweeping | Navigation, localization, task allocation, communication | Cooperative |
| Manual Robot Operation | Wireless control, mobility, status feedback | Independent |
| Mixed Manual-Autonomous Experiments | Wireless control, autonomous operation, monitoring | Mixed |

---

# 15. Operational Constraints and Assumptions

## 15.1 Operational Assumptions

The following assumptions are used to establish this operational concept.

1. Each individual robot is capable of independent operation.
2. Multiple robots can participate in the same experiment.
3. Robots may communicate with one another.
4. Selected robots can physically connect to form composite configurations.
5. A small servo-actuated gripper may be integrated as an optional manipulation mechanism.
6. Researchers can develop and execute different algorithms.
7. Manual wireless control is available for selected operations.
8. Autonomous operation may occur without continuous human movement commands.
9. Centralized monitoring may coexist with decentralized decision-making.
10. Experimental configurations may vary between research applications.

## 15.2 Operational Constraints

Potential constraints include:

- Individual robot mass and physical dimensions.
- Available battery capacity.
- Maximum operating speed.
- Computational resources.
- Communication range and reliability.
- Sensor performance.
- Mechanical connection limitations.
- Manipulator force and movement characteristics.
- Environmental conditions.
- Laboratory safety requirements.

The specific limits must be established during subsequent system requirements engineering.

---

# 16. Open Issues and Decisions

The following items require further definition before the OpsCon can be baselined.

| ID | Topic | Open Question |
|---|---|---|
| OI-01 | Robot Mass | Is the <1 kg limit applicable to the complete individual robot, including battery and attachments? |
| OI-02 | Operating Speed | Is 0.5 m/s the enforced normal maximum, with 1.0 m/s available as an experimental limit? |
| OI-03 | Composite Mass | Is there a maximum permitted mass for a physically connected composite system? |
| OI-04 | Docking | What physical configurations and connection arrangements are intended? |
| OI-05 | Composite Control | Do connected robots retain independent control processes, or can they use a shared control arrangement? |
| OI-06 | Gripper | What gripping force, torque, and closing speed are intended? |
| OI-07 | Manual Control | Can one operator control multiple robots simultaneously? |
| OI-08 | Control Transition | What conditions are required when switching between manual and autonomous operation? |
| OI-09 | Communication Loss | What should each robot do when operator or robot-to-robot communication is lost? |
| OI-10 | Fleet Management | Is external fleet monitoring required for every experiment? |
| OI-11 | Charging | Will robots use exchangeable batteries, individual charging ports, or a shared charging station? |
| OI-12 | Data Management | Which data must be recorded by default? |
| OI-13 | Operating Environment | Is outdoor operation within the initial platform scope? |
| OI-14 | Safety | What risk-reduction measures are required for human interaction and composite operation? |
| OI-15 | Simulation | Is simulation-to-real experimentation part of the initial platform scope? |

---

# 17. Relationship to Other Engineering Documents

This OpsCon provides system-level operational information for subsequent engineering activities.

| Document | Purpose | Relationship |
|---|---|---|
| Research Needs | Identifies research problems and motivations. | Establishes the need for the platform. |
| Concept of Operations (ConOps) | Describes the broader research mission and intended operational context. | Provides the operational foundation. |
| System Operational Concept (OpsCon) | Describes how the platform operates and interacts with users and external systems. | Defines the system-level operational concept. |
| Stakeholder Requirements Specification (StRS) | Defines stakeholder needs and expectations. | Formalizes stakeholder expectations derived from the operational concept. |
| Platform Requirements Description (PRD) | Describes desired platform capabilities. | Organizes the capabilities needed to support research applications. |
| System Requirements Specification (SyRS) | Defines measurable and verifiable system requirements. | Establishes the technical requirements for implementation. |
| System Architecture | Defines system components, interfaces, and relationships. | Allocates system requirements to architectural elements. |
| Verification Plan | Defines requirement verification activities. | Establishes how system compliance will be demonstrated. |

These documents should be developed iteratively, maintaining traceability between operational scenarios, stakeholder needs, platform capabilities, and technical system requirements.

---

# End of Document

