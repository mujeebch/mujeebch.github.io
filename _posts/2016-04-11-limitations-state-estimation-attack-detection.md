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

1. **Random attacks**, in which sensor measurements are altered without carefully considering the state estimator.
2. **Stealthy bias attacks**, in which measurements are modified gradually or strategically to remain within the detector's threshold.
3. **Replay attacks**, in which legitimate historical measurements are recorded and later retransmitted while the physical process is manipulated.

Random attacks are comparatively straightforward to identify because they often create large residuals.

Stealthy bias and replay attacks present a more difficult challenge. The manipulated measurements may remain statistically plausible even though they no longer accurately represent the current physical process.

# How was the study evaluated?

The experiments were conducted on the Secure Water Treatment testbed, commonly known as SWaT.

Using a physical water treatment environment allowed us to observe the behaviour of the Kalman filter and Chi-Square detector under realistic sensors, controllers, communication, process dynamics, and attack conditions.

This experimental evaluation was important because detection performance observed in simulation may not fully represent the behaviour of an operational cyber-physical system.

# What did we find?

The results showed that state-estimation-based detection could identify random attacks that produced clear deviations.

However, stealthy false-data injection and replay attacks could remain undetected by the legacy failure-detection approach.

This occurs because the detector was designed primarily to identify faults and statistically unusual measurements. An intelligent attacker can study the detector and construct malicious values that remain within its accepted range.

# Why does this limitation matter?

A detector may perform well against accidental failures without providing equivalent protection against malicious behaviour.

A component failure does not normally attempt to hide. An attacker does.

This distinction has important consequences for industrial cybersecurity. Evaluation should not be limited to random corruption or large measurement changes. It should include attackers who understand the physical system, estimation algorithm, detection threshold, and operator response.

The findings motivate additional safeguards such as:

- active or physical watermarking;
- sensor and process noise fingerprinting;
- timing-based device authentication;
- diverse and redundant detection methods;
- protected communication and message authentication; and
- process-aware security monitoring.

## Perspective

This work helped establish an important direction in our research: methods developed for fault detection cannot automatically be assumed to provide cyberattack detection.

State estimation remains valuable, but the associated detector must be evaluated against adversaries who adapt their behaviour to its design.

The question is therefore not only whether a detector identifies abnormal values. We must also ask how much damage a knowledgeable attacker can cause while keeping the detector below its alarm threshold.

The paper was co-authored with Sridhar Adepu and Aditya Mathur.

## Research collaboration and consultancy

Our research investigates the strengths and limitations of cyberattack detection methods for industrial control systems and critical infrastructure.

We welcome enquiries relating to:

- state-estimation-based attack detection;
- Kalman filters and statistical detectors;
- Chi-Square attack detection;
- replay and false-data injection attacks;
- stealthy manipulation of industrial sensors;
- assessment of legacy failure-detection systems;
- water treatment and critical-infrastructure security;
- process-aware intrusion detection;
- adversarial testing of industrial security controls; and
- experimental evaluation using cyber-physical testbeds.

We can support infrastructure operators, engineering teams, cybersecurity vendors, public-sector organisations, and researchers through independent evaluation, threat modelling, consultancy, collaborative research, and specialist training.

For consultancy, research collaboration, advisory work, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1109/SCSPW.2016.7509557. In *Proceedings of the 2016 Smart City Security and Privacy Workshop*. IEEE, 1–5. https://doi.org/10.1109/SCSPW.2016.7509557
