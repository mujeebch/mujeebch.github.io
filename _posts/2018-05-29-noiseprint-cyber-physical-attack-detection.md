---
title: 'NoisePrint: Detecting Cyber-Physical Attacks Through the Unique Noise of Sensors and Processes'
date: 2018-05-29
permalink: /posts/2018/05/noiseprint-cyber-physical-attack-detection/
tags:
  - NoisePrint
  - cyber physical systems
  - sensor security
  - sensor fingerprinting
  - process noise
  - Kalman filter
  - zero alarm attacks
  - attack detection
  - critical infrastructure
  - cybersecurity
---

Sensor measurements in cyber-physical systems contain noise produced by sensing hardware and the underlying physical process. This noise is normally viewed as an obstacle to accurate measurement and control.

NoisePrint investigates a different possibility: can the combined noise of a sensor and physical process provide a fingerprint for detecting cyberattacks?

This blog post discusses our paper, *NoisePrint: Attack Detection Using Sensor and Process Noise Fingerprint in Cyber Physical Systems* https://doi.org/10.1145/3196494.3196532, presented at the 2018 ACM Asia Conference on Computer and Communications Security.

# What security problem did we investigate?

Cyber-physical systems use sensor measurements to monitor and control physical processes. An attacker who manipulates these measurements may be able to conceal an unsafe physical condition or cause a controller to issue damaging commands.

Conventional detectors often compare sensor measurements with an expected process value. An attacker with sufficient knowledge of the system may design a zero-alarm or stealthy attack that keeps the detector's output below its alarm threshold.

We investigated whether the noise characteristics within the measurements could reveal attacks that appear normal to conventional statistical detectors.

# What is NoisePrint?

NoisePrint creates a combined fingerprint of sensor noise and physical process noise during normal system operation.

The method begins with a mathematical model describing the expected behaviour of the process. A Kalman filter uses this model to estimate the system state.

The difference between the estimated state and the observed state produces a residual. Under normal steady-state conditions, this residual contains information about both sensor noise and process noise.

We extract time-domain and frequency-domain features from the residual and provide them to a machine learning algorithm. The resulting model learns the characteristic noise pattern associated with particular sensors and processes.

# How can NoisePrint detect an attack?

A spoofing or false-data injection attack changes the measurements received by the monitoring system.

Even when an attacker carefully controls the magnitude of the measurement changes, the injected values may not reproduce the expected relationship between sensor noise, process noise, and system dynamics.

The resulting residual can therefore exhibit a different pattern from the fingerprint learned during normal operation.

NoisePrint uses this deviation to provide evidence that the received measurements may have been manipulated.

# Why consider both time and frequency features?

Noise patterns can be represented in different ways.

Time-domain features describe properties such as the distribution and variation of the residual over time. Frequency-domain features describe how the signal's energy is distributed across different frequencies.

An attack may preserve some statistical properties while altering others. Combining time-domain and frequency-domain information enables the detector to examine the signal from complementary perspectives.

# How was NoisePrint evaluated?

We evaluated NoisePrint using two cyber-physical security testbeds:

- the Secure Water Treatment testbed, known as SWaT; and
- the Water Distribution testbed, known as WADI.

The experiments included zero-alarm attacks designed to evade conventional statistical detectors.

The results showed that NoisePrint could detect the evaluated zero-alarm attacks. The noise fingerprints also distinguished multiple sensors with accuracy above 90% in the reported experiments.

# How does NoisePrint differ from conventional anomaly detection?

A conventional anomaly detector usually asks whether the measurement is sufficiently different from an expected value.

NoisePrint asks an additional question: does the noise contained in the measurement look like the noise normally produced by this sensor and process?

This distinction matters because a forged measurement may remain within the detector's expected range while lacking the underlying signal characteristics of the legitimate physical source.

## Perspective

NoisePrint demonstrates the value of retaining and analysing information that conventional processing might discard.

The approach does not assume that noise is perfectly fixed. Environmental changes, sensor ageing, maintenance, and process variation can affect the fingerprint. Practical deployment therefore requires continuing evaluation and appropriate mechanisms for updating fingerprints.

Nevertheless, noise provides a promising additional security signal because it is connected to the physical device and process rather than only to the digital content of a message.

The paper was co-authored with Martin Ochoa, Jianying Zhou, Aditya P. Mathur, Rizwan Qadeer, Carlos Murguia, and Justin Ruths.

## Research collaboration and consultancy

Our research explores process-aware and signal-based security for sensors, industrial control systems, and critical infrastructure.

We welcome enquiries relating to:

- NoisePrint and sensor fingerprinting;
- sensor and process noise analysis;
- zero-alarm and stealthy cyberattacks;
- false-data injection detection;
- Kalman filter-based security monitoring;
- machine learning for sensor authentication;
- process-aware intrusion detection;
- water infrastructure cybersecurity;
- industrial control system security; and
- evaluation of cyber-physical attack detection systems.

We can help organisations develop, evaluate, and independently review detection methods that combine machine learning with physical process knowledge.

For consultancy, collaborative research, system evaluation, advisory activities, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1145/3196494.3196532. In *Proceedings of the 2018 ACM Asia Conference on Computer and Communications Security*. ACM, 483–497. https://doi.org/10.1145/3196494.3196532
