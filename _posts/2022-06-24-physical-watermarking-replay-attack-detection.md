---
title: 'Detecting Replay Attacks in Cyber-Physical Systems with Practical Physical Watermarking'
date: 2022-06-24
permalink: /posts/2022/06/physical-watermarking-replay-attack-detection/
tags:
  - cyber physical systems
  - replay attacks
  - physical watermarking
  - industrial control systems
  - water distribution systems
  - attack detection
  - critical infrastructure
  - cybersecurity
---

Cyber-physical systems combine computing, communication, sensing, and control with physical processes. They are used in water infrastructure, power systems, transportation, manufacturing, medical devices, and robotic platforms.

Attacks against these systems can have consequences that extend beyond computers and networks. A successful attack may manipulate a physical process while presenting apparently legitimate sensor measurements to the control system.

This blog post discusses our paper, *A Practical Physical Watermarking Approach to Detect Replay Attacks in a CPS* https://doi.org/10.1016/j.jprocont.2022.06.002, published in the *Journal of Process Control*.

# What is a replay attack?

Industrial control systems continually collect measurements from sensors. These measurements are used by controllers, operators, and monitoring systems to understand the state of the physical process.

In a replay attack, an adversary records legitimate sensor measurements during normal operation. The attacker later replays those old measurements while manipulating the physical system.

Because the replayed values were originally produced by the real system, they may appear realistic to conventional anomaly-detection mechanisms. The monitoring interface may therefore continue to show normal behaviour even when the physical process is moving towards an unsafe state.

# Why are replay attacks dangerous?

Replay attacks exploit the trust that control systems place in sensor data. If an attacker can replace current measurements with previously recorded values, the controller and operator may lose visibility of the actual process.

This can delay incident detection and allow the attacker to continue manipulating equipment such as pumps, valves, motors, and actuators.

The challenge is to determine whether an observed sensor measurement represents the current physical process or is merely a recording of an earlier state.

# What is physical watermarking?

Physical watermarking introduces a carefully designed signal into the control process. This signal produces a subtle but expected effect on the physical system.

Because the defender knows the watermark, it can check whether the corresponding effect appears in subsequent sensor measurements.

Current and authentic measurements should contain evidence of the watermark. Previously recorded measurements should not contain the effect of the newly introduced signal. This difference can reveal that an attacker is replaying old sensor data.

The concept is similar to introducing a controlled challenge into the physical process and verifying whether the sensors provide the expected response.

# What did we propose?

We developed a practical method for designing and using a physical watermark to detect replay attacks in a cyber-physical system.

An effective watermark must satisfy two competing requirements:

1. It must influence the physical process sufficiently to support reliable attack detection.
2. It must not cause unacceptable disruption to the system's normal operation.

A watermark that is too small may be hidden by ordinary process noise. A watermark that is too large may affect operational performance or cause noticeable changes in the controlled process.

The practical design of the watermark must therefore consider the behaviour, safety requirements, and physical constraints of the target system.

# How was the approach evaluated?

The method was experimentally evaluated using the WAter DIstribution testbed, commonly known as WADI.

WADI is a physical water distribution system containing tanks, pumps, valves, sensors, programmable logic controllers, communication networks, and supervisory control components. It provides a realistic environment for evaluating attacks and security mechanisms against critical water infrastructure.

Using a physical testbed allowed us to investigate how the watermark interacted with genuine process dynamics, sensor noise, control actions, and operational constraints.

# What did we learn?

The experiments demonstrated how a carefully designed watermark signal can help distinguish current sensor measurements from replayed data.

The work also highlighted that physical watermarking must be adapted to the target process. A signal that performs well in one system may not be appropriate for another system with different dynamics, operating limits, or noise characteristics.

Physical watermarking should therefore be considered a process-aware defence rather than a generic network-security control.

## Perspective

An interesting feature of physical watermarking is that it uses the physical process as part of the security mechanism.

Traditional cybersecurity tools often monitor network traffic, software events, or access-control records. A physical watermark instead asks whether sensor data contains evidence of a known and recent physical action.

This makes it difficult for an attacker to remain hidden by replaying historical data alone. To evade the detector, the attacker would need to predict or reproduce the physical effect of the watermark in real time.

The paper demonstrates why cyber-physical security requires knowledge of control systems, process dynamics, sensors, and physical operations in addition to conventional computing and network security.

The paper was co-authored with Venkata Reddy Palleti and Vishrut Kumar Mishra.

## Research collaboration and consultancy

Our research examines cyberattacks that manipulate sensors, controllers, networks, and physical processes in critical infrastructure and industrial control systems.

We welcome enquiries from water utilities, industrial operators, engineering companies, cybersecurity vendors, government bodies, and research organisations interested in:

- replay attack detection;
- false-data injection and sensor attacks;
- physical and dynamic watermarking;
- industrial control system security;
- SCADA and programmable logic controller security;
- security of water treatment and distribution systems;
- process-aware intrusion detection;
- cyber-physical attack detection;
- security testbed design;
- critical-infrastructure threat modelling;
- experimental validation of security mechanisms; and
- independent cybersecurity assessment and consultancy.

We can contribute to collaborative research, security reviews, threat-modelling activities, experimental evaluation, training, and the development of process-aware detection methods for cyber-physical infrastructure.

For research collaboration, consultancy, invited talks, advisory activities, or related opportunities, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1016/j.jprocont.2022.06.002. *Journal of Process Control* 116 (2022), 136–146. https://doi.org/10.1016/j.jprocont.2022.06.002
