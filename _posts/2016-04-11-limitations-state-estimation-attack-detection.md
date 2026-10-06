---
title: 'Where State-Estimation-Based Cyberattack Detection Fails in Industrial Control Systems'
date: 2016-04-11
permalink: /posts/2016/04/limitations-state-estimation-attack-detection/
tags:
  - industrial control systems
  - state estimation
  - Kalman filter
  - Chi Square detector
  - replay attacks
  - false data injection
  - cyber physical systems
  - water treatment security
  - critical infrastructure
  - cybersecurity
---

Industrial control systems use sensors and state estimators to understand the condition of a physical process. If a measurement differs significantly from the estimated state, a failure detector may raise an alarm.

This approach is useful for identifying faults and random disturbances, but does it provide sufficient protection against an intelligent attacker who understands how the detector works?

This blog post discusses our paper, *Limitations of State Estimation Based Cyber Attack Detection Schemes in Industrial Control Systems* https://doi.org/10.1109/SCSPW.2016.7509557, presented at the 2016 Smart City Security and Privacy Workshop.

# What is state estimation?

A state estimator uses a mathematical model and available measurements to estimate variables that describe the condition of a physical process.

In this work, we used a Kalman filter. The Kalman filter combines model predictions with sensor measurements and accounts for expected uncertainty and noise.

A detector can then examine the difference between the estimated and observed values. A sufficiently large difference may indicate a fault or attack.

# How does a Chi-Square detector work?

We combined the Kalman filter with a Chi-Square detector.

The detector evaluates whether the residual between measured and estimated values is statistically consistent with normal system behaviour.

If the residual exceeds a selected threshold, the system raises an alarm.

This type of method is effective against faults or attacks that create large and unexpected deviations. Its limitations become more apparent when an attacker deliberately constructs a signal to remain within the accepted statistical range.

# Which attacks did we investigate?

We experimentally examined three categories of attack:

1. **Random attacks**, in which sensor measurements are altered 
