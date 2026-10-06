---
title: 'Noise Matters: Turning Sensor Noise into a Security Fingerprint for Cyber-Physical Systems'
date: 2018-12-07
permalink: /posts/2018/12/noise-matters-sensor-security-fingerprint/
tags:
  - cyber physical systems
  - sensor security
  - sensor authentication
  - device fingerprinting
  - data integrity attacks
  - industrial control systems
  - stealthy cyberattacks
  - critical infrastructure
  - cybersecurity
---

Noise in sensor measurements is generally treated as an unwanted disturbance. Engineers often use filters and estimation techniques to reduce its effect and obtain a clearer representation of the underlying physical process.

However, sensor and process noise can also contain useful security information. Small variations caused by manufacturing imperfections, sensing hardware, installation conditions, and physical process behaviour can form patterns that help distinguish one sensor from another.

This blog post discusses our paper, *Noise Matters: Using Sensor and Process Noise Fingerprint to Detect Stealthy Cyber Attacks and Authenticate Sensors in CPS* https://doi.org/10.1145/3274694.3274748, presented at the 34th Annual Computer Security Applications Conference.

# Why is sensor authentication important?

Cyber-physical systems rely on sensors to observe physical processes. A controller may use measurements of pressure, flow, temperature, water level, or chemical properties to determine its next action.

If an attacker manipulates a sensor reading, the controller may make an unsafe decision while believing that it is responding to a genuine process condition.

A malicious participant may also attempt to impersonate a legitimate sensor. Conventional authentication can establish which device possesses a cryptographic key, but it does not always show whether the measurements genuinely originated from the expected physical sensor and process.

We investigated whether the natural noise contained in measurements could provide an additional source of authentication.

# What is a sensor noise fingerprint?

Two sensors of the same type may appear identical, but small variations can arise from manufacturing tolerances, electronics, installation, calibration, environmental conditions, and interaction with the physical process.

These variations influence the noise embedded within sensor measurements.

We use these sensor and process noise characteristics to create a fingerprint. The fingerprint describes the statistical and frequency characteristics normally associated with a particular sensor operating within a particular physical process.

If measurements are manipulated or originate from a different source, their noise characteristics may deviate from the established fingerprint.

# How is the fingerprint created?

We first use a system model to estimate the expected behaviour of the physical process. The difference between the expected and observed measurements provides information about sensor and process noise.

Features representing this noise are extracted during normal system operation. These features can include statistical and frequency-domain characteristics.

A machine learning classifier then learns the fingerprint associated with each sensor.

When new measurements arrive, their noise characteristics are compared with the learned fingerprint. A significant deviation can indicate sensor impersonation or a data integrity attack.

# How was the approach evaluated?

The approach was evaluated using data from the Secure Water Treatment testbed, commonly known as SWaT.

SWaT is a realistic water treatment environment containing tanks, pumps, valves, sensors, programmable logic controllers, communication networks, and supervisory control components.

This environment allowed us to investigate whether sensor fingerprints remained distinguishable under realistic process conditions and whether attacks caused detectable changes in the noise pattern.

# What did we find?

The results showed that different sensors could be identified from their noise fingerprints, with identification accuracy reaching as high as 98% in the evaluated experiments.

We also designed stealthy attacks against the proposed method and conducted a detailed security analysis. The results demonstrated that deviations in sensor and process noise could help identify data integrity attacks that attempted to preserve apparently normal process behaviour.

# Why does noise matter?

The important observation is that noise is not always meaningless randomness.

When a sensor and physical process operate normally, their combined noise may contain persistent characteristics. Removing all noise during analysis may consequently discard security-relevant information.

Noise fingerprinting provides an additional detection layer based on the physical origin of measurements rather than relying only on network addresses, software identities, or message contents.

## Perspective

This work turns a traditional engineering problem into a security feature. Instead of treating noise only as something to remove, we examine whether it can help establish the origin and integrity of sensor measurements.

Noise-based fingerprints are not a replacement for cryptographic authentication or process-aware anomaly detection. They provide an additional and independent source of evidence.

Combining cyber, physical, and hardware characteristics can make it more difficult for an attacker to produce manipulated measurements that remain convincing across every monitoring layer.

The paper was co-authored with Jianying Zhou and Aditya P. Mathur.

## Research collaboration and consultancy

Our research examines how physical signals, sensor characteristics, process dynamics, and machine learning can support the security of cyber-physical and industrial systems.

We welcome enquiries relating to:

- sensor authentication and identification;
- sensor and device fingerprinting;
- detection of data integrity attacks;
- stealthy attack detection;
- hardware-based security signals;
- process-aware anomaly detection;
- industrial control system security;
- security of critical-infrastructure sensors;
- machine learning for cyber-physical security; and
- experimental evaluation using industrial testbeds.

We can support collaborative research, security assessment, consultancy, technology evaluation, training, and knowledge exchange involving IoT, industrial, and cyber-physical systems.

For consultancy, research collaboration, advisory work, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1145/3274694.3274748. In *Proceedings of the 34th Annual Computer Security Applications Conference*. ACM, 566–581. https://doi.org/10.1145/3274694.3274748
