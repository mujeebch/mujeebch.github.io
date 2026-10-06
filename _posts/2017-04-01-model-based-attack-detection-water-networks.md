---
title: 'How Model-Based Detection Can Reveal Cyberattacks on Smart Water Networks'
date: 2017-04-01
permalink: /posts/2017/04/model-based-attack-detection-water-networks/
tags:
  - smart water networks
  - water distribution security
  - model based attack detection
  - Kalman filter
  - CUSUM
  - false data injection
  - zero alarm attacks
  - cyber physical systems
  - critical infrastructure
  - cybersecurity
---

Smart water distribution systems use sensors, controllers, pumps, valves, and communication networks to deliver water efficiently and reliably.

These connected technologies improve visibility and control, but they also create opportunities for attackers to manipulate sensor readings or control commands. A compromised monitoring system may display apparently normal values while the physical process moves towards an undesirable state.

This blog post discusses our paper, *Model-Based Attack Detection Scheme for Smart Water Distribution Networks* https://doi.org/10.1145/3052973.3053011, presented at the 2017 ACM Asia Conference on Computer and Communications Security.

# What is model-based attack detection?

A model-based detector uses a mathematical representation of the physical process to estimate how the system should behave.

The detector compares the predicted behaviour with measurements received from the real or simulated system. The difference between the prediction and observation is called a residual.

Under normal operating conditions, the residual should remain within an expected range. If an attacker manipulates a sensor or actuator, the residual may change and provide evidence of abnormal behaviour.

# How did we model the water network?

We used EPANET, a simulation tool for water distribution systems, to model the behaviour of a water distribution network.

Data produced by the simulation was used with subspace identification techniques to obtain an input-output Linear Time-Invariant model of the network.

This model formed the basis of a Kalman filter that estimated the evolving state of the water distribution system.

The model estimates were then compared with the EPANET measurements to produce residual variables for attack detection.

# Which detection methods were considered?

We used two detection procedures:

1. **Bad-Data Detection**, which assesses whether the residual exceeds an expected statistical threshold.
2. **Dynamic Cumulative Sum**, or CUSUM, which accumulates evidence of small changes over time.

Bad-Data Detection can identify large deviations quickly. CUSUM can be useful when an attack introduces smaller but persistent changes that might not immediately exceed a conventional alarm threshold.

# Which attacks were evaluated?

The study considered several forms of malicious manipulation, including:

- false-data injection attacks against sensor readings;
- attacks against control inputs; and
- zero-alarm attacks designed to remain below detection thresholds.

Zero-alarm attacks are particularly important because the attacker deliberately selects the malicious signal according to the detector's behaviour.

The measurements may appear statistically acceptable even while the attack gradually moves the estimated or physical state away from normal operation.

# What did we find?

The simulation experiments illustrated how model-based detection can reveal attacks that create observable inconsistencies between the expected and measured process behaviour.

The analysis also demonstrated the limitations of residual-based detectors. An attacker who understands the model and detector may construct an attack that keeps the residual within its accepted range.

We therefore derived upper bounds on the estimator-state deviation that zero-alarm attacks could induce. This quantifies how far an attacker may be able to influence the estimated state without triggering the selected detector.

# Why are detection limits important?

It is not sufficient to show that a detector recognises some attack examples. Security evaluation should also investigate the strongest attack that can remain hidden.

Understanding this limit helps system designers determine:

- whether existing alarms provide adequate protection;
- how thresholds affect security and false alarms;
- how much process deviation can occur before detection;
- where additional sensors or security controls are required; and
- whether multiple detection mechanisms should be combined.

## Perspective

Model-based attack detection connects cybersecurity with control theory and process engineering.

The detector does not rely exclusively on known network signatures. It asks whether the observed measurements and control actions remain consistent with the expected physical behaviour of the water network.

However, the strength of a model-based detector depends on the quality of its model, the placement of sensors, the configuration of thresholds, and the attacker's knowledge.

The paper therefore contributes both a detection approach and an analysis of what a strategically designed zero-alarm attack may achieve.

The paper was co-authored with Carlos Murguia and Justin Ruths.

## Research collaboration and consultancy

Our research investigates model-based and process-aware approaches to securing water networks, industrial control systems, and critical infrastructure.

We welcome
