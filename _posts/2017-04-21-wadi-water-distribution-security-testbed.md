---
title: 'Inside WADI: A Water Distribution Testbed for Cyber-Physical Security Research'
date: 2017-04-21
permalink: /posts/2017/04/wadi-water-distribution-security-testbed/
tags:
  - WADI
  - water distribution
  - cyber physical systems
  - industrial control systems
  - critical infrastructure
  - security testbed
  - SCADA security
  - programmable logic controllers
  - cyberattack detection
  - cybersecurity
---

Water distribution is a critical public service. Modern distribution networks use sensors, communication systems, programmable controllers, pumps, and valves to monitor and control the movement of water across large geographical areas.

These technologies improve operational efficiency, but they also introduce cyber and physical security risks. Evaluating these risks requires realistic environments in which researchers can conduct experiments without disrupting a live water network.

This blog post discusses our paper, *WADI: A Water Distribution Testbed for Research in the Design of Secure Cyber Physical Systems* https://doi.org/10.1145/3055366.3055375, presented at the Third International Workshop on Cyber-Physical Systems for Smart Water Networks.

# Why was WADI developed?

Many industrial cybersecurity studies rely on software simulations or small laboratory demonstrations. These methods are useful, but they may not capture the interactions between physical equipment, control logic, sensors, networks, and human operators.

Testing attacks on operational water infrastructure is generally unsafe and impractical. A physical testbed provides an alternative: a controlled environment that reproduces important characteristics of a real facility while allowing experiments to be conducted safely.

The WAter DIstribution testbed, known as WADI, was designed to support experimental research into the security of water distribution systems.

# What does WADI represent?

WADI is a scaled-down, high-fidelity representation of a modern water distribution facility.

The physical process includes water storage, pumping, elevated reservoirs, consumer tanks, return water, chemical dosing, valves, instrumentation, and analysers.

The system is controlled through industrial automation equipment, including programmable logic controllers and remote terminal units. Sensors estimate the current condition of the system, while actuators influence the movement and quality of water.

This combination enables researchers to investigate both the cyber and physical dimensions of an attack.

# What can researchers study using WADI?

WADI was designed to support several forms of research:

1. Security analysis of water distribution networks.
2. Experimental evaluation of cyberattack detection methods.
3. Evaluation of physical attack detection.
4. Study of sensor and actuator manipulation.
5. Investigation of control and communication failures.
6. Generation of realistic industrial cybersecurity datasets.
7. Assessment of cascading effects between connected infrastructures.

The testbed includes facilities for studying water leakage, burst pipes, malicious chemical injection, and other abnormal physical conditions.

# How is WADI connected to other systems?

WADI complements the Secure Water Treatment testbed, known as SWaT. SWaT represents the treatment of raw water, while WADI represents the subsequent distribution of water to consumers.

Connecting these facilities enables researchers to investigate how an attack in a treatment system might affect water distribution and how an incident in the distribution network might influence the wider infrastructure.

WADI can also support research into interdependent infrastructure when water systems interact with energy, communication, and control systems.

# Why are realistic testbeds important?

A detection technique may perform well in a simulation while encountering unexpected problems in an operational environment.

Realistic testbeds expose security methods to:

- genuine sensor and process noise;
- physical delays and system dynamics;
- equipment limitations;
- industrial communication protocols;
- interactions between controllers;
- changing operating conditions; and
- consequences that propagate through a physical process.

They enable researchers to examine not only whether an attack is detected, but also when it is detected and what physical consequences occur before an alarm is raised.

## Perspective

WADI provides more than a dataset or simulation. It creates an experimental environment in which cybersecurity methods can be assessed against physical processes and industrial automation equipment.

This is essential for cyber-physical security. A network alert may not explain whether a physical process has become unsafe, while an unusual sensor value may be caused by an attack, equipment failure, or a legitimate operational transition.

Testbeds such as WADI allow these interactions to be investigated in a controlled, repeatable, and safe manner.

The paper was co-authored with Venkata Reddy Palleti and Aditya P. Mathur.

## Research collaboration and consultancy

Our research uses realistic cyber-physical testbeds to evaluate attacks, defences, datasets, and operational risks affecting critical infrastructure.

We welcome enquiries relating to:

- industrial and cyber-physical security testbeds;
- water treatment and distribution security;
- SCADA and programmable logic controller security;
- cyberattack and anomaly detection;
- industrial cybersecurity datasets;
- physical attack simulation;
- cascading risks in connected infrastructure;
- security evaluation of detection technologies;
- testbed design and experimental methodology; and
- training and exercises for industrial cybersecurity.

We can support utilities, engineering organisations, cybersecurity companies, public-sector bodies, and research groups through collaborative experimentation, independent evaluation, consultancy, training, and knowledge exchange.

For consultancy, research collaboration, testbed evaluation, advisory activities, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1145/3055366.3055375. In *Proceedings of the Third International Workshop on Cyber-Physical Systems for Smart Water Networks*. ACM, 25–28. https://doi.org/10.1145/3055366.3055375
