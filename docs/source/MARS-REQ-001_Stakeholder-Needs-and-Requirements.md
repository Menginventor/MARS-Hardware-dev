# Stakeholder Needs and Requirements

- **Document ID:** `MARS-REQ-001`
- **Version:** `v1.1`
- **Date:** `2026-11-12`
- **Author:** Dhamdhawach Horsuwan
- **Phase:** Requirements Engineering
- **Project:** Multi-Agent Robotic Systems (MARS) Hardware Platform

---

## Overview

Multi-Agent Robotic Systems (MARS) research requires a mobile robot platform capable of supporting experiments involving multiple autonomous agents operating and interacting within a shared environment. Unlike single-robot research, multi-agent experiments introduce additional challenges related to fleet scalability, inter-robot communication, distributed coordination, hardware consistency, and fleet-level operation.

To establish a rigorous requirements engineering baseline, this document:
1. **Identifies the intended stakeholder groups** involved in developing, operating, maintaining, and using the platform.
2. **Defines a stakeholder priority classification** (`Essential`, `Important`, `Desirable`) to manage cost and engineering complexity.
3. **Distinguishes Research Needs (`RN-01` – `RN-08`) from Stakeholder Requirements (`SR-01` – `SR-08`)**, expressing each Research Need from the stakeholder's perspective (desired research outcome) alongside the corresponding Stakeholder Requirement (expected platform capability).

---

## 1. Identified Stakeholders

The MARS hardware platform serves six primary stakeholder groups:

| Stakeholder ID | Stakeholder Group | Role & Primary Interest |
| :--- | :--- | :--- |
| **`SH-01`** | **MARS Researchers** | Formulate hypotheses, conduct multi-agent experiments, evaluate coordination behavior, and publish reproducible scientific results. |
| **`SH-02`** | **Robotics and Hardware Developers** | Design, fabricate, extend, and integrate mechanical structures, power systems, sensors, and actuator modules. |
| **`SH-03`** | **Software and Algorithm Developers** | Implement, deploy, and test decentralized control, state estimation, perception, and inter-robot communication algorithms. |
| **`SH-04`** | **Experimental Operators** | Configure, deploy, monitor, and supervise robot fleets safely and efficiently during live experimental sessions. |
| **`SH-05`** | **Laboratory Technicians** | Perform fleet charging, battery replacement, calibration, preventive maintenance, diagnostics, and hardware repairs. |
| **`SH-06`** | **External Research Collaborators** | Reproduce experiments, share hardware/software modules, and adopt or adapt the platform across partnering laboratories. |

---

## 2. Stakeholder Priority Classification

To guide design trade-offs and manage platform cost and complexity, each need and requirement is assigned one of three priority levels:

- **Essential**: Fundamental to executing multi-agent experiments safely and reliably; must be satisfied in the baseline platform release.
- **Important**: Significantly improves experimental versatility, development speed, or fleet-level operational efficiency; strongly targeted for the baseline design.
- **Desirable**: Enhances advanced physical interaction, convenience, or cross-laboratory technology transfer when budget and complexity margins permit.

---

## 3. Research Needs and Stakeholder Requirements

Based on practical experience operating a four-robot team, the following eight Research Needs (`RN-01` to `RN-08`) and corresponding Stakeholder Requirements (`SR-01` to `SR-08`) have been established:

### 1. Scalability of Multi-Agent Experiments
- **Priority:** `Essential`
- **Primary Stakeholders:** MARS Researchers (`SH-01`), Experimental Operators (`SH-04`), Robotics and Hardware Developers (`SH-02`)
- **Research Need (`RN-01`):** Researchers need to conduct experiments involving different numbers of autonomous robots to investigate how fleet size affects coordination performance, communication, task allocation, and overall multi-agent system behavior without prohibitive per-unit costs.
- **Stakeholder Requirement (`SR-01`):** The platform shall support scalable multi-robot deployments across varying fleet sizes and maintain a cost-effective unit design that enables the acquisition and operation of larger robot teams.

### 2. Decentralized Coordination and Communication
- **Priority:** `Essential`
- **Primary Stakeholders:** MARS Researchers (`SH-01`), Software and Algorithm Developers (`SH-03`)
- **Research Need (`RN-02`):** Researchers and algorithm developers need to investigate decentralized multi-agent architectures in which robots exchange information directly and make autonomous decisions under dynamic network topologies without relying on a central server.
- **Stakeholder Requirement (`SR-02`):** The platform shall provide onboard computation and peer-to-peer wireless communication interfaces that support decentralized decision-making and dynamic network topologies without requiring a centralized control server.

### 3. Consistent and Predictable Robot Behavior
- **Priority:** `Essential`
- **Primary Stakeholders:** MARS Researchers (`SH-01`), Software and Algorithm Developers (`SH-03`), Laboratory Technicians (`SH-05`)
- **Research Need (`RN-03`):** Researchers need individual robots within a team to exhibit consistent locomotion, sensing, and state estimation so that experimental outcomes reflect algorithmic performance rather than hardware-induced unit-to-unit variations.
- **Stakeholder Requirement (`SR-03`):** The platform shall deliver repeatable and uniform motor response, odometry, localization accuracy, and sensor performance across all robot units in the fleet.

### 4. Adaptability to Different Research Problems
- **Priority:** `Important`
- **Primary Stakeholders:** Robotics and Hardware Developers (`SH-02`), Software and Algorithm Developers (`SH-03`), MARS Researchers (`SH-01`)
- **Research Need (`RN-04`):** Researchers and developers need to evaluate diverse algorithms, sensors, actuators, and experimental payloads across multiple projects without redesigning the core robot platform for each study.
- **Stakeholder Requirement (`SR-04`):** The platform shall feature modular mechanical mounting, standardized electrical/communication interfaces, and extensible software architecture to allow adding or swapping sensors, actuators, and compute modules without full-system redesign.

### 5. Reliable Long-Term and Fleet-Level Operation
- **Priority:** `Essential`
- **Primary Stakeholders:** Experimental Operators (`SH-04`), Laboratory Technicians (`SH-05`), MARS Researchers (`SH-01`)
- **Research Need (`RN-05`):** Experimental operators and technicians need to run multiple robots concurrently over extended experimental sessions with minimal downtime for recharging, battery swaps, routine maintenance, or fault recovery.
- **Stakeholder Requirement (`SR-05`):** The platform shall incorporate reliable power management, integrated battery protection, accessible battery replacement, efficient fleet charging, and modular serviceability to minimize operational downtime as fleet size scales.

### 6. Environmental Awareness and Physical Interaction
- **Priority:** `Important` (Navigation & Obstacle Avoidance) / `Desirable` (Cooperative Transport & Manipulation Attachments)
- **Primary Stakeholders:** MARS Researchers (`SH-01`), Robotics and Hardware Developers (`SH-02`), Software and Algorithm Developers (`SH-03`)
- **Research Need (`RN-06`):** Researchers need robots to perceive and navigate cluttered shared environments safely, avoid inter-robot and obstacle collisions, and—when required by specific studies—physically interact with objects or perform cooperative transport.
- **Stakeholder Requirement (`SR-06`):** The platform shall provide onboard environmental sensing for navigation and collision avoidance (`Essential`/`Important`), and shall accommodate optional mechanical attachments or payloads for physical interaction and cooperative object transport (`Desirable`).

### 7. Experimental Monitoring and Data Collection
- **Priority:** `Important`
- **Primary Stakeholders:** MARS Researchers (`SH-01`), Experimental Operators (`SH-04`), Software and Algorithm Developers (`SH-03`)
- **Research Need (`RN-07`):** Researchers and operators need to observe, record, and analyze the real-time state and historical behavior of both individual robots and the collective fleet without interfering with the robots' decentralized autonomy.
- **Stakeholder Requirement (`SR-07`):** The platform shall support non-intrusive centralized fleet monitoring, real-time telemetry streaming, synchronized experimental data logging, and visualization tools while preserving decentralized onboard execution.

### 8. Usability, Reproducibility, and Technology Transfer
- **Priority:** `Desirable`
- **Primary Stakeholders:** External Research Collaborators (`SH-06`), MARS Researchers (`SH-01`), Experimental Operators (`SH-04`), Laboratory Technicians (`SH-05`)
- **Research Need (`RN-08`):** Researchers, students, and external collaborators from varied engineering and software backgrounds need to onboard quickly, reproduce experimental setups reliably, and replicate or adopt the platform across different research groups.
- **Stakeholder Requirement (`SR-08`):** The platform shall provide intuitive user interfaces, standardized configuration workflows, built-in diagnostic indicators, and comprehensive documentation to reduce the learning curve and facilitate reproducibility and technology transfer.

---

## 4. Traceability Summary Matrix

| Need ID | Research Need (Researcher Perspective) | Req ID | Stakeholder Requirement (Platform Capability) | Stakeholders | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`RN-01`** | Conduct experiments across varying fleet sizes to study scalability | **`SR-01`** | Scalable, cost-effective unit design for multi-robot deployment | `SH-01`, `SH-02`, `SH-04` | **Essential** |
| **`RN-02`** | Investigate autonomous peer-to-peer coordination without central servers | **`SR-02`** | Onboard compute & direct inter-robot wireless communication | `SH-01`, `SH-03` | **Essential** |
| **`RN-03`** | Isolate algorithmic performance from unit-to-unit hardware variance | **`SR-03`** | Uniform locomotion, sensing & state estimation across fleet | `SH-01`, `SH-03`, `SH-05` | **Essential** |
| **`RN-04`** | Explore diverse sensors, actuators & algorithms across studies | **`SR-04`** | Modular mechanical, electrical & software expansion interfaces | `SH-01`, `SH-02`, `SH-03` | **Important** |
| **`RN-05`** | Operate concurrent robot fleets over long sessions with low downtime | **`SR-05`** | Battery protection, fast swap/charging & easy fleet maintenance | `SH-01`, `SH-04`, `SH-05` | **Essential** |
| **`RN-06`** | Study safe navigation, obstacle avoidance & physical object interaction | **`SR-06`** | Environmental perception suite & optional interaction attachments | `SH-01`, `SH-02`, `SH-03` | **Important / Desirable** |
| **`RN-07`** | Observe and evaluate individual and fleet behavior during experiments | **`SR-07`** | Centralized telemetry, logging & monitoring decoupled from control | `SH-01`, `SH-03`, `SH-04` | **Important** |
| **`RN-08`** | Enable rapid onboarding, reproducible setups & cross-lab adoption | **`SR-08`** | Accessible configuration, diagnostics & technology transfer docs | `SH-01`, `SH-04`, `SH-05`, `SH-06` | **Desirable** |
