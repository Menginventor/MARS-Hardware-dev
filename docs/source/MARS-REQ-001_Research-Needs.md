# Research Needs

- **Document ID:** `MARS-REQ-001`
- **Version:** `v1.0`
- **Date:** `2026-11-12`
- **Author:** Dhamdhawach Horsuwan
- **Phase:** Requirements Engineering
- **Project:** Multi-Agent Robotic Systems (MARS) Hardware Platform

---

Multi-Agent Robotic Systems (MARS) research requires a mobile robot platform capable of supporting experiments involving multiple autonomous agents operating and interacting within a shared environment. Unlike single-robot research, multi-agent experiments introduce additional challenges related to fleet scalability, inter-robot communication, distributed coordination, hardware consistency, and fleet-level operation.

Based on practical experience operating a four-robot team, the following research needs have been identified:

## 1. Scalability of Multi-Agent Experiments

The platform should support experiments involving different fleet sizes, allowing researchers to investigate how the number of agents affects coordination performance, communication, task allocation, and overall system behavior. The platform should also be cost-effective enough to enable the deployment of larger robot teams.

## 2. Decentralized Coordination and Communication

The platform should support research into decentralized multi-agent architectures in which robots exchange information and make decisions autonomously. It should accommodate direct inter-robot communication and dynamic network topologies without requiring a centralized decision-making server.

## 3. Consistent and Predictable Robot Behavior

Robots operating as a team should exhibit sufficiently consistent locomotion, sensing, and state estimation characteristics. Differences in motor response, localization accuracy, or sensor performance can affect coordination and experimental results. Therefore, the platform should provide reliable and repeatable individual robot behavior.

## 4. Adaptability to Different Research Problems

MARS research involves diverse algorithms, sensors, actuators, and experimental configurations. The platform should allow researchers to modify or extend hardware and software components without redesigning the entire robot, supporting interdisciplinary collaboration and reuse across research projects.

## 5. Reliable Long-Term and Fleet-Level Operation

Multi-agent experiments require multiple robots to operate concurrently, often over extended periods. The platform should minimize downtime through reliable power management, battery protection, convenient battery replacement, and efficient fleet charging. It should also simplify maintenance and troubleshooting as the fleet grows.

## 6. Environmental Awareness and Physical Interaction

The platform should support research involving navigation, obstacle avoidance, collision avoidance, and physical interaction with the environment. Depending on the research objective, robots may also need to transport objects cooperatively or use interchangeable manipulation attachments.

## 7. Experimental Monitoring and Data Collection

Researchers need to observe and evaluate the behavior of individual robots and the entire fleet. The platform should support centralized monitoring, telemetry collection, experimental logging, and data visualization while allowing the robots' internal decision-making processes to remain decentralized.

## 8. Usability, Reproducibility, and Technology Transfer

The platform should be accessible to researchers with different engineering and software backgrounds. Intuitive interfaces, straightforward configuration, accessible diagnostics, and simplified maintenance procedures can reduce the learning curve. These characteristics also support reproducibility, collaboration, and the transfer of the platform to other research groups.

