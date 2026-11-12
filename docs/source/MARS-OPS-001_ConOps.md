# MARS-OPS-001
# Concept of Operations (ConOps)

## General-Purpose Mobile Robot Platform for Multi-Agent Robotic Systems Research

| Document Information | Description |
|---|---|
| Document ID | MARS-OPS-001 |
| Document Title | Concept of Operations (ConOps) |
| System | General-Purpose MARS Mobile Robot Platform |
| Author | Dhamdhawach Horsuwan |
| Version | v1.0 |
| Release Date | 2026-11-12 |
| Document Type | Concept of Operations (ConOps) |
| Applicable Standard | ISO/IEC/IEEE 29148:2018 |

---

# 1. Introduction

## 1.1 Purpose

This Concept of Operations (ConOps) describes the intended operational concept of a general-purpose mobile robotic platform designed to support research, development, and experimentation in Multi-Agent Robotic Systems (MARS).

The platform provides a common experimental infrastructure through which researchers can investigate multi-robot behaviors, coordination strategies, communication mechanisms, autonomous decision-making, and cooperative tasks.

Rather than being dedicated to a single application, the platform is intended to accommodate different research objectives and experimental configurations. These include self-reconfigurable multi-robot systems, cooperative object transportation, multi-robot navigation, search and rescue (SAR), and cooperative region sweeping.

This document establishes the operational context, intended users, research applications, operational configurations, operational modes, representative scenarios, and lifecycle activities associated with the platform.

## 1.2 Scope

The scope of this document covers the operational use of multiple mobile robotic agents as an experimental system for MARS research.

It considers:

- Independent operation of individual robotic agents.
- Cooperative operation involving multiple robotic agents.
- Physical connection and disconnection of robots to form composite robotic systems.
- Manual wireless control of individual robots.
- Autonomous and decentralized multi-robot operation.
- Centralized fleet supervision and experiment management.
- Integration of different hardware modules, sensors, and experimental equipment.
- Experiment preparation, execution, monitoring, data collection, and evaluation.
- Routine maintenance, charging, and operational recovery.

The platform is intended to support different research applications without being restricted to a specific algorithm, task, or robot configuration.

This document describes the intended operation of the platform rather than prescribing detailed hardware designs, software architectures, communication protocols, or implementation technologies.

## 1.3 Intended Audience

This document is intended for:

- Principal investigators and research supervisors.
- Robotics researchers and graduate students.
- Robot hardware and software developers.
- Experiment operators and laboratory personnel.
- Researchers developing multi-agent algorithms.
- Future users adapting the platform for different research applications.

## 1.4 Document Organization

This document is organized into the following sections:

1. Introduction
2. Mission and Operational Objectives
3. Stakeholders and User Classes
4. Operational Environment
5. System Overview
6. Intended Research Applications
7. Operational Concept
8. Representative Operational Scenarios
9. Human-System Interaction
10. Operational Constraints and Assumptions
11. Safety and Operational Risk Considerations
12. Support and Maintenance Concept
13. Expected Operational Outcomes
14. Open Issues and Items Requiring Further Definition
15. Relationship to Other Engineering Documents

---

# 2. Mission and Operational Objectives

## 2.1 Mission Statement

The mission of the Multi-Agent Robotic Systems (MARS) platform is to provide a general-purpose, modular, and extensible robotic platform for research, development, and experimentation in multi-robot systems.

The platform is intended to support a broad range of research activities, including self-reconfigurable multi-robot systems, cooperative object transportation, multi-robot navigation, search and rescue, and cooperative area coverage.

It aims to provide researchers with a common and reusable experimental infrastructure for investigating multi-robot coordination, communication, control, perception, localization, and autonomous decision-making under various operational conditions.

## 2.2 Operational Objectives

The platform is intended to achieve the following operational objectives.

### O-01 — Research Flexibility

Support different research applications without requiring fundamental redesign of the entire robotic platform.

### O-02 — Multi-Robot Cooperation

Enable multiple robotic agents to perform individual and cooperative tasks.

### O-03 — Decentralized Operation

Support research into decentralized coordination and decision-making, where robots can exchange information and coordinate their actions without depending entirely on a central controller.

### O-04 — Physical Reconfiguration

Support experiments in which individual robots physically connect to form a larger composite robotic system and subsequently disconnect to resume independent operation.

### O-05 — Manual Operability

Allow operators to wirelessly control individual robots for testing, positioning, debugging, calibration, demonstrations, and recovery.

### O-06 — Experimental Reproducibility

Provide a common experimental infrastructure that allows researchers to configure, execute, observe, and evaluate experiments consistently.

### O-07 — Accessibility and Usability

Allow researchers from different technical backgrounds to prepare and operate experiments without requiring extensive expertise in every aspect of robotics.

### O-08 — Extensibility

Allow researchers to introduce new hardware modules, sensors, algorithms, and experimental configurations as research requirements evolve.

### O-09 — Operational Reliability

Provide a platform that can be prepared, deployed, operated, recovered, and maintained repeatedly for research activities.

---

# 3. Stakeholders and User Classes

The platform is intended to serve several categories of stakeholders.

| Stakeholder / User Class | Responsibilities and Interests |
|---|---|
| Principal Investigator | Defines research objectives, supervises experiments, and evaluates research outcomes. |
| Researcher | Develops algorithms, configures experiments, analyzes data, and investigates robot behaviors. |
| Robot Developer | Develops, integrates, and maintains robot hardware and software. |
| Experiment Operator | Prepares robots, deploys teams, supervises execution, and handles operational interruptions. |
| Student / New Researcher | Uses the platform to learn, develop, and conduct experiments. |
| Laboratory Technician | Performs routine inspection, charging, maintenance, and equipment management. |

Users may perform multiple roles depending on the experiment and laboratory organization.

## 3.1 User Responsibilities

### Researcher

The researcher is responsible for defining experiment objectives, selecting appropriate research methods, configuring algorithms, and evaluating experimental results.

### Experiment Operator

The experiment operator is responsible for preparing and deploying robots, initiating experiments, monitoring system conditions, and intervening when necessary.

### Robot Developer

The robot developer is responsible for maintaining the platform software and hardware, integrating additional modules, and supporting experimental customization.

### Laboratory Technician

The laboratory technician is responsible for routine maintenance, battery management, inspection, and preparation of the robotic equipment.

---

# 4. Operational Environment

## 4.1 Physical Environment

The platform is intended primarily for controlled research and experimental environments.

Potential operating environments include:

- Indoor research laboratories.
- Laboratory test areas and experimental arenas.
- Structured and semi-structured environments.
- Environments containing static and dynamic obstacles.
- Environments containing narrow passages and restricted areas.
- Outdoor test areas, where supported by the selected robot configuration.
- Simulated or controlled environments representing search-and-rescue scenarios.

The environment may contain other robotic agents, human operators, experimental objects, and obstacles.

The physical environment may be modified according to the research application.

## 4.2 Communication Environment

Robotic agents may communicate directly with other agents or through external communication infrastructure, depending on the experiment.

Communication conditions may vary during operation.

Researchers may intentionally investigate communication limitations, including:

- Limited communication range.
- Intermittent connectivity.
- Communication delays.
- Packet loss.
- Network partitioning.
- Changes in network topology due to robot movement.
- Communication between physically connected and independent agents.

The platform is intended to provide an experimental environment in which different communication and coordination approaches can be investigated.

## 4.3 Human Interaction Environment

Researchers and operators interact with the platform to configure, initiate, supervise, and evaluate experiments.

Human interaction may occur through:

- Onboard user interfaces.
- Wireless handheld controllers.
- Computer-based control interfaces.
- External fleet-monitoring interfaces.
- Development and experiment-management software.

The operator may supervise the overall experiment without necessarily controlling the individual decisions of every robot.

## 4.4 Computational Environment

The platform is intended to support different computational arrangements according to the research application.

Computational activities may be performed:

- Locally on individual robots.
- Across multiple robots through distributed computation.
- Through external computers or development systems.
- Through a combination of onboard and external computational resources.

The computational arrangement may vary between experiments.

---

# 5. System Overview

## 5.1 General Concept

The MARS platform consists of multiple mobile robotic agents that can operate independently or cooperate as a multi-robot team.

Each robot represents an individual agent with its own onboard hardware and computational capabilities.

Depending on the research application, multiple agents may:

1. Operate independently while performing separate tasks.
2. Cooperate through information exchange and coordinated decision-making.
3. Coordinate their movement to accomplish a shared task.
4. Physically connect to form a composite robotic system.
5. Disconnect from a composite configuration and resume independent operation.

The platform is intended to support both centralized supervision and decentralized robot operation.

Centralized supervision may be used for experiment preparation, fleet monitoring, and operator intervention. However, the research algorithms running on individual robots may make decisions locally and coordinate directly with other agents.

## 5.2 Individual Robotic Agent

An individual robotic agent is a mobile robot capable of operating independently.

It provides the physical and computational resources required for an individual agent to participate in experiments.

An individual agent may:

- Navigate within an experimental environment.
- Acquire information from its sensors.
- Execute local control and decision-making algorithms.
- Communicate with other agents.
- Receive operator commands.
- Participate in cooperative tasks.
- Physically connect to other robotic agents when the experiment requires it.

## 5.3 Composite Robotic System

A composite robotic system is formed when two or more individual robotic agents physically connect to one another.

The connected robots form a larger physical robotic configuration that can perform tasks collectively.

A composite system may involve multiple computational agents coordinating their actions.

Physical connection does not necessarily imply that the connected robots become a single software agent or share a single controller.

The control and coordination arrangement may depend on the research experiment.

## 5.4 Operational Configurations

The platform is expected to support the following conceptual configurations.

### A. Independent Robot Configuration

Each robot operates as an independent agent.

Robots may perform separate tasks, navigate individually, or participate in experiments where their interactions are limited.

### B. Cooperative Multi-Robot Configuration

Multiple robots operate as a team to accomplish a shared objective.

Each robot maintains its own operational state and participates in coordination with other agents.

### C. Composite Robot Configuration

Two or more robots physically connect to form a larger robotic structure.

After connection, the resulting composite system operates as a coordinated physical configuration.

### D. Reconfigurable Multi-Robot Configuration

Robots may transition between independent and composite configurations through physical connection and disconnection.

The resulting configuration may change according to the task, environment, or experimental objective.

### E. Mixed Operational Configuration

A team may contain both independent robots and one or more composite robotic systems.

This configuration allows researchers to investigate interactions between independently operating agents and physically connected groups.

---

# 6. Intended Research Applications

The platform is intended to support the following research application areas.

## 6.1 Self-Reconfigurable Multi-Robot Systems

Multiple independent robotic agents physically connect to form a composite robotic system.

Researchers investigate how robots identify connection opportunities, approach one another, establish physical connections, coordinate their actions, and change their physical configuration.

Representative research activities include:

- Robot-to-robot docking and undocking.
- Physical self-reconfiguration.
- Distributed configuration planning.
- Cooperative movement of connected agents.
- Coordination between independent and connected robots.
- Fault handling during connection or disconnection.
- Transitions between independent and composite operation.

## 6.2 Multi-Robot Object Transportation

Multiple robots cooperate to transport a shared object or payload.

Robots may approach an object, establish physical interaction, coordinate their movements, and transport the object toward a designated destination.

Representative research activities include:

- Cooperative transportation.
- Formation and position coordination.
- Distributed load management.
- Cooperative path planning.
- Coordination under limited communication.
- Transportation through constrained environments.
- Handling disturbances during transportation.

## 6.3 Multi-Robot Navigation

Multiple robots navigate through an environment either independently or cooperatively.

Researchers investigate navigation strategies, coordination mechanisms, and interactions between agents operating in shared environments.

Representative research activities include:

- Distributed path planning.
- Cooperative navigation.
- Collision avoidance.
- Formation control.
- Navigation through narrow passages.
- Navigation under limited communication.
- Distributed localization and state estimation.
- Coordination in dynamic environments.

## 6.4 Search and Rescue (SAR)

Multiple robots cooperate to explore an environment and search for designated targets, simulated victims, or other objects of interest.

The research may involve environments that are unknown, partially known, or contain obstacles and restricted passages.

Representative research activities include:

- Cooperative exploration.
- Search area allocation.
- Target detection and localization.
- Information sharing.
- Distributed decision-making.
- Coordination under communication constraints.
- Multi-robot navigation in challenging environments.
- Search efficiency and coverage evaluation.

## 6.5 Multi-Robot Region Sweeping

Multiple robots cooperate to cover a designated region while attempting to minimize redundant coverage and improve overall task efficiency.

Representative research activities include:

- Region decomposition.
- Task allocation.
- Coverage path planning.
- Distributed coordination.
- Coverage monitoring.
- Recovery from robot failure or communication loss.
- Scalability with increasing team size.

## 6.6 Cross-Application Research

In addition to the application-specific activities above, the platform is intended to support research topics that can be investigated across multiple applications.

These include:

- Centralized and decentralized control.
- Robot-to-robot communication.
- Distributed task allocation.
- Multi-agent decision-making.
- Communication network topology.
- Fault detection and recovery.
- Scalability of multi-robot systems.
- Human supervision of autonomous robot teams.
- Performance evaluation of multi-agent algorithms.

---

# 7. Operational Concept

## 7.1 General Operational Workflow

A typical research experiment follows the operational sequence below.

### Phase 1 — Experiment Preparation

Researchers define the research objective, select the intended application, prepare the experimental environment, and determine the required number and configuration of robots.

### Phase 2 — Robot Preparation

Robots are inspected, charged, configured, and prepared for deployment.

Required sensors, modules, software, and communication settings are checked according to the experiment.

### Phase 3 — Experiment Configuration

Researchers configure the experiment parameters, including:

- Task objectives.
- Number of participating robots.
- Robot roles.
- Initial positions.
- Coordination strategies.
- Communication settings.
- Navigation or control algorithms.
- Experimental conditions.

### Phase 4 — Deployment

Robots are placed in the experimental environment and initialized.

The operator verifies that the required robots are ready before starting the experiment.

### Phase 5 — Experiment Execution

Robots perform their assigned tasks.

Depending on the experiment, robots may operate independently, coordinate as a team, or physically connect to form a composite system.

Manual wireless control may also be used for selected operations.

### Phase 6 — Monitoring and Intervention

Researchers monitor the experiment and observe robot states and overall team behavior.

When necessary, operators may intervene to pause, stop, manually control, or recover robots.

### Phase 7 — Data Collection and Evaluation

Experimental data are collected and analyzed to evaluate system behavior and research outcomes.

### Phase 8 — Shutdown and Reset

Robots are stopped, recovered, disconnected if necessary, inspected, and prepared for subsequent experiments.

## 7.2 Operational Modes

The platform is intended to support the following operational modes.

| Mode | Description |
|---|---|
| Preparation | Robots are inspected, charged, and prepared for an experiment. |
| Configuration | Experiment parameters and robot configurations are established. |
| Standby | Robots are initialized and waiting for an experiment to begin. |
| Manual Wireless Control | An operator remotely controls an individual robot through a wireless interface. |
| Independent Autonomous Operation | An individual robot autonomously performs its assigned task. |
| Cooperative Autonomous Operation | Multiple robots autonomously coordinate to perform a shared task. |
| Composite Operation | Physically connected robots operate as a composite robotic system. |
| Reconfiguration | Robots establish or release physical connections to change their configuration. |
| Monitoring | Researchers observe robot states and experiment progress. |
| Recovery | Robots or the team recover from an interruption or operational failure. |
| Shutdown | Robot operation is terminated and the platform is prepared for storage or another experiment. |

### 7.2.1 Manual Wireless Control

Manual Wireless Control allows an operator to remotely control an individual robot using a wireless control interface, such as a handheld controller or computer-based interface.

The operator may control robot movement and selected operational functions without executing an autonomous research algorithm.

This mode is intended for:

- Manual robot positioning and deployment.
- Hardware and mobility testing.
- Sensor calibration and inspection.
- Software debugging and development.
- Manual recovery and repositioning.
- Demonstration and educational activities.

Manual wireless control may be used independently of multi-robot autonomous experiments.

Depending on the experimental configuration, an operator may control individual robots while other robots continue autonomous operation.

Loss of the wireless control connection should result in a defined robot response appropriate to the operating context.

Manual wireless control does not replace emergency-stop or other required safety functions.

### 7.2.2 Independent Autonomous Operation

An individual robot autonomously performs an assigned task using its onboard computational and sensing capabilities.

The robot may operate without continuous human input while remaining available for monitoring and operator intervention.

### 7.2.3 Cooperative Autonomous Operation

Multiple robots autonomously coordinate to accomplish a shared objective.

Coordination may involve information exchange, task allocation, cooperative navigation, and distributed decision-making.

The coordination approach may be centralized, decentralized, or hybrid depending on the research experiment.

### 7.2.4 Composite Operation

Two or more physically connected robots operate as a composite robotic configuration.

The connected agents coordinate their actions to accomplish tasks that may not be practical for an individual robot.

The control arrangement may be centralized within the composite configuration or distributed across its constituent agents.

### 7.2.5 Reconfiguration

Robots establish or release physical connections to change the overall configuration of the robotic system.

Reconfiguration may be initiated by an autonomous algorithm or through operator intervention, depending on the experiment.

### 7.2.6 Monitoring

Researchers observe the operational condition of individual robots and the overall team.

Monitoring may include robot status, position, connectivity, battery condition, task progress, and other experimental information.

Monitoring does not necessarily imply direct control of the robots.

### 7.2.7 Recovery

Robots or the team respond to an operational interruption or failure.

Recovery may involve autonomous behavior, operator intervention, manual wireless control, or physical assistance.

## 7.3 Operational Control Arrangements

The platform is intended to support different arrangements for human supervision and robot decision-making.

### A. Manual Robot Control

An operator directly controls the movement of an individual robot through a wireless interface.

### B. Centralized Fleet Supervision

An operator or external system monitors multiple robots and may issue commands to individual robots or the team.

This arrangement is primarily intended for experiment management and supervision.

### C. Decentralized Autonomous Operation

Individual robots make local decisions and coordinate with other agents through robot-to-robot communication.

The system does not depend entirely on a central controller for operational decision-making.

### D. Hybrid Operation

The system combines centralized supervision with decentralized robot autonomy.

For example, an operator may supervise the fleet and define experiment objectives while individual robots independently determine their actions and coordinate with neighboring agents.

These arrangements are distinct operational concepts and may be selected according to the research application.

---

# 8. Representative Operational Scenarios

## 8.1 Scenario A — Self-Reconfigurable Multi-Robot Experiment

**Objective:** Investigate physical reconfiguration and cooperative operation of multiple robotic agents.

**Operational sequence:**

1. Researchers prepare multiple independent robots.
2. Robots are deployed into the experimental environment.
3. Each robot initially operates as an independent agent.
4. The robots identify a reconfiguration objective.
5. Selected robots approach one another and physically connect.
6. The connected robots establish a composite configuration.
7. The composite system performs a designated task.
8. Robots may disconnect and return to independent operation.
9. Researchers evaluate the reconfiguration process and cooperative behavior.

**Expected research outcomes:**

- Physical connection and disconnection behavior.
- Reconfiguration strategies.
- Coordination between connected agents.
- Transition between independent and composite operation.

## 8.2 Scenario B — Cooperative Object Transportation

**Objective:** Investigate how multiple robots cooperate to transport a shared object.

**Operational sequence:**

1. Researchers prepare the robots and transportation object.
2. Robots are deployed around the object.
3. The robots identify their respective roles and transportation objectives.
4. Robots establish physical interaction with the object.
5. The team coordinates its movement.
6. Robots transport the object toward the designated destination.
7. Researchers monitor the transportation process.
8. The team completes the task or terminates the experiment.
9. Researchers evaluate transportation performance and coordination.

**Expected research outcomes:**

- Cooperative movement.
- Task coordination.
- Object transportation performance.
- Robustness to disturbances and communication limitations.

## 8.3 Scenario C — Multi-Robot Navigation

**Objective:** Investigate navigation strategies involving multiple robotic agents.

**Operational sequence:**

1. Researchers define the navigation environment and objectives.
2. Robots are placed at their initial positions.
3. Robots initialize their navigation systems.
4. Robots navigate toward their respective destinations.
5. When required, robots exchange information and coordinate movement.
6. Robots respond to obstacles and interactions with other agents.
7. Researchers monitor navigation performance.
8. The experiment terminates after the navigation objectives are completed or an interruption occurs.

**Expected research outcomes:**

- Navigation performance.
- Collision avoidance.
- Cooperative path planning.
- Coordination under communication constraints.

## 8.4 Scenario D — Search and Rescue Experiment

**Objective:** Investigate multi-robot exploration and target-search strategies.

**Operational sequence:**

1. Researchers prepare an environment containing designated search areas and simulated targets.
2. Robots are deployed into the environment.
3. Robots begin exploring the environment.
4. The team distributes search activities according to the selected coordination strategy.
5. Robots detect potential targets and share relevant information.
6. The team updates its search activities based on newly acquired information.
7. Researchers monitor search progress.
8. The experiment terminates when the search objectives are achieved or the experiment is stopped.

**Expected research outcomes:**

- Exploration performance.
- Search efficiency.
- Target detection and localization.
- Distributed task allocation.
- Information sharing under communication constraints.

## 8.5 Scenario E — Multi-Robot Region Sweeping

**Objective:** Investigate cooperative coverage of a designated area.

**Operational sequence:**

1. Researchers define the region to be covered.
2. Robots are deployed at designated initial positions.
3. The team determines or receives its coverage objectives.
4. Robots distribute coverage tasks.
5. Robots execute their assigned coverage paths.
6. Robots exchange information about coverage progress.
7. The team responds to changes in operational conditions.
8. The experiment terminates when the coverage objective is achieved or the experiment is stopped.

**Expected research outcomes:**

- Coverage efficiency.
- Task allocation performance.
- Coordination strategies.
- Redundant coverage reduction.
- Scalability with increasing team size.

## 8.6 Scenario F — Manual Wireless Operation

**Objective:** Allow an operator to manually control a robot for testing, positioning, debugging, and recovery.

**Operational sequence:**

1. The operator prepares the robot and wireless control interface.
2. The robot is powered on and initialized.
3. The operator establishes a wireless control connection.
4. The operator verifies the control connection and robot response.
5. The operator manually controls robot movement or selected functions.
6. The robot performs the requested manual operation.
7. The operator terminates manual control.
8. The robot returns to standby or another permitted operational mode.

**Alternative conditions:**

- If the wireless connection is interrupted, the robot follows its defined communication-loss response.
- If the robot enters an abnormal operating condition, the operator may initiate recovery or shutdown.
- If manual intervention is no longer required, the robot may be prepared for autonomous operation.

**Expected operational outcomes:**

- Direct control of individual robots.
- Convenient positioning and deployment.
- Hardware and software testing.
- Simplified debugging and maintenance.
- Manual recovery capability.

## 8.7 Scenario G — Mixed Manual and Autonomous Operation

**Objective:** Support experiments in which some robots are manually controlled while other robots operate autonomously.

**Operational sequence:**

1. Researchers prepare multiple robots.
2. The operator establishes the required wireless control connections.
3. Selected robots are assigned to manual wireless control.
4. Other robots are configured for autonomous operation.
5. The experiment begins.
6. Manually controlled robots perform operator-directed activities.
7. Autonomous robots continue executing their assigned algorithms.
8. Researchers monitor interactions between manually controlled and autonomous agents.
9. The experiment terminates or returns robots to standby.

**Expected research outcomes:**

- Human-robot interaction.
- Coordination between human-controlled and autonomous agents.
- Mixed autonomy experiments.
- Human intervention in multi-robot systems.

---

# 9. Human-System Interaction

## 9.1 Researcher Interaction

Researchers interact with the platform throughout the experiment lifecycle.

Their activities include:

- Selecting the research application.
- Configuring robot parameters.
- Loading or executing experimental algorithms.
- Assigning experiment objectives.
- Initializing and deploying robots.
- Monitoring robot and team status.
- Collecting experimental data.
- Evaluating experimental results.

## 9.2 Operator Supervision

An operator may supervise the overall team through an external interface.

The interface is intended to provide visibility into the operational condition of individual robots and the overall team.

Depending on the experimental setup, the operator may:

- Monitor robot connectivity.
- Observe robot positions and operating states.
- Monitor battery and system status.
- Start or stop experiments.
- Pause or resume operation where supported.
- Issue commands to individual robots.
- Establish or terminate manual wireless control.
- Respond to robot failures or abnormal conditions.

Operator supervision does not necessarily imply centralized control of robot decisions.

## 9.3 Onboard Interaction

Researchers and operators may interact directly with individual robots through onboard controls and indicators.

This interaction supports basic operational activities such as:

- Checking robot status.
- Performing initial configuration.
- Accessing selected settings.
- Establishing wireless connections.
- Starting or stopping data recording.
- Identifying abnormal operating conditions.

## 9.4 Manual Control Interface

Manual wireless control may be provided through a handheld controller or computer-based interface.

The interface is intended to allow operators to issue movement commands and access selected robot functions.

The specific interface and control arrangement may vary according to the experimental configuration.

---

# 10. Operational Constraints and Assumptions

## 10.1 Operational Assumptions

The following assumptions establish the initial operational concept.

1. Multiple robotic agents are available for experiments.
2. Each robot can operate as an individual agent.
3. The platform supports communication between robotic agents, subject to the capabilities and limitations of the selected configuration.
4. Some experiments require physical connection between robots.
5. Researchers may develop and execute different algorithms on the platform.
6. Experiment environments and objectives may vary between research activities.
7. A human operator is available to prepare and supervise experiments.
8. Centralized monitoring may coexist with decentralized robot decision-making.
9. Wireless manual control is available for selected operational activities.
10. Additional hardware and sensing modules may be integrated according to research requirements.

## 10.2 Operational Constraints

Potential constraints include:

- Limited battery capacity and operating duration.
- Limited communication range and network connectivity.
- Physical dimensions and mobility limitations.
- Mechanical limitations during robot-to-robot connection.
- Sensor accuracy and environmental conditions.
- Available computational resources.
- Safety limitations of the experimental environment.
- Wireless control range and reliability.
- Availability of researchers and laboratory resources.

The specific constraints will be characterized during subsequent requirements engineering and system development.

---

# 11. Safety and Operational Risk Considerations

## 11.1 General Safety

The platform is intended to operate in research environments where human operators, other robotic agents, and experimental equipment may be present.

Operational activities should consider potential hazards associated with robot movement, physical interaction, electrical power, and mechanical reconfiguration.

## 11.2 Manual Control Safety

Manual wireless control introduces the possibility of unintended movement resulting from operator error, communication interruption, or incorrect control input.

Operational procedures should consider:

- Clear indication of the current control mode.
- Defined behavior following wireless communication loss.
- Prevention of unintended mode transitions.
- Operator awareness of robot movement.
- Availability of appropriate emergency-stop functions.

## 11.3 Multi-Robot Safety

Cooperative operation introduces additional considerations associated with interactions between multiple robots.

These include:

- Robot-to-robot collisions.
- Interference during cooperative movement.
- Unexpected changes in robot trajectories.
- Communication loss during coordinated tasks.
- Unintended interaction with human operators.

## 11.4 Physical Reconfiguration Safety

Physical connection and disconnection may introduce mechanical hazards.

Operational procedures should consider:

- Mechanical alignment during docking.
- Secure connection verification.
- Prevention of unintended disconnection.
- Controlled movement during composite operation.
- Safe handling of failed docking attempts.

## 11.5 Emergency Intervention

Emergency intervention should remain available independently of the selected research algorithm or manual wireless control mode.

Software commands, wireless control, and ordinary power switches should not be assumed to provide safety-rated emergency-stop functionality.

Detailed safety requirements and protective measures will be established during subsequent system engineering.

---

# 12. Support and Maintenance Concept

## 12.1 Preparation and Charging

Robots are prepared before each experiment.

This includes:

- Battery charging.
- Physical inspection.
- Configuration checks.
- Verification of essential system functions.
- Inspection of communication interfaces.
- Verification of required sensors and modules.

## 12.2 Maintenance

Routine maintenance is performed to maintain platform reliability and availability.

Maintenance activities may include:

- Mechanical inspection.
- Battery inspection and replacement.
- Sensor calibration.
- Communication system inspection.
- Software updates.
- Firmware updates.
- Inspection of physical docking interfaces.
- Replacement of damaged components.

## 12.3 Software and Experiment Management

Researchers may update software and experimental algorithms independently of the core platform where practical.

The platform should allow experimental configurations to be recorded and reproduced to support research continuity.

## 12.4 Storage and Transportation

Robots may be stored, transported, and redeployed between experimental sessions.

The platform should support practical handling and preparation by laboratory personnel.

## 12.5 Operational Recovery

When a robot becomes unavailable or experiences an operational failure, researchers or operators may perform recovery activities.

These may include:

- Manual wireless repositioning, where safe and available.
- Physical retrieval.
- Battery replacement or recharging.
- Software restart.
- Hardware inspection.
- Replacement of damaged components.

The recovery approach depends on the nature of the failure and the experimental environment.

---

# 13. Expected Operational Outcomes

The MARS platform is intended to provide the following outcomes:

1. A reusable experimental infrastructure for multi-agent robotic research.
2. Support for multiple independent and cooperative robotic agents.
3. Support for physical robot-to-robot connection and reconfiguration.
4. Support for diverse multi-robot research applications.
5. Support for manual wireless operation and autonomous experimentation.
6. An environment for investigating decentralized coordination and communication.
7. Support for mixed human-controlled and autonomous robot operation.
8. Improved accessibility for researchers with different technical backgrounds.
9. Improved reproducibility and consistency of robotic experiments.
10. An extensible foundation for future MARS research and development.

---

# 14. Open Issues and Items Requiring Further Definition

The following items require further discussion before this ConOps can be baselined.

| ID | Topic | Open Question |
|---|---|---|
| OI-01 | Operating Environment | Is the initial platform intended primarily for indoor use, or must outdoor operation also be considered? |
| OI-02 | Fleet Scale | What is the expected minimum and maximum number of robots in a team? |
| OI-03 | Robot Reconfiguration | Can robots connect in multiple physical arrangements, or is there one primary composite configuration? |
| OI-04 | Composite Operation | Do physically connected robots operate under a shared controller, distributed controllers, or both depending on the experiment? |
| OI-05 | Object Transportation | Will the platform include dedicated manipulation mechanisms, or will transportation be investigated using external attachments? |
| OI-06 | SAR Applications | Are SAR experiments limited to controlled laboratory environments, or should realistic outdoor scenarios be included? |
| OI-07 | Fleet Supervision | What level of centralized monitoring and operator intervention is expected? |
| OI-08 | Safety | What safety provisions are required for autonomous operation, physical docking, and cooperative transportation? |
| OI-09 | Experiment Data | What types of experimental data must be recorded and retained? |
| OI-10 | Simulation | Should the platform support simulation-to-real experimentation as part of its intended operation? |
| OI-11 | Manual Control | Should one operator be able to control multiple robots simultaneously? |
| OI-12 | Manual Control | Should manual wireless control support only movement, or also selected onboard functions? |
| OI-13 | Control Transition | What conditions are required to transition between manual and autonomous operation? |
| OI-14 | Mixed Autonomy | Should manual and autonomous robots be allowed to participate in the same experiment? |
| OI-15 | Control Loss | What behavior is expected when wireless manual-control communication is interrupted? |
| OI-16 | Composite Control | Should a physically connected composite system also support manual wireless control? |

---

# 15. Relationship to Other Engineering Documents

This ConOps provides the operational foundation for subsequent requirements engineering activities.

| Document | Purpose | Relationship to This ConOps |
|---|---|---|
| Research Needs / Stakeholder Needs | Identifies research objectives and stakeholder expectations. | Establishes why the platform is needed and what stakeholders expect to achieve. |
| Stakeholder Requirements Specification (StRS) | Defines stakeholder needs and expectations in a structured, verifiable manner. | Captures stakeholder requirements arising from the operational concept. |
| System Operational Concept (OpsCon) | Describes the system-specific operational concept. | Provides a more detailed view of how users operate and interact with the robotic platform. |
| Platform Requirements Description (PRD) | Describes the desired platform capabilities. | Identifies the capabilities needed to support the operational scenarios. |
| System Requirements Specification (SyRS) | Defines measurable technical system requirements. | Translates stakeholder and platform needs into verifiable system requirements. |

These documents should be developed iteratively, maintaining traceability between operational scenarios, stakeholder needs, platform capabilities, and system requirements.

---

# End of Document

