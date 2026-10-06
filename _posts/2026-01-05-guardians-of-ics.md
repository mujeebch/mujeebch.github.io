---
title: 'Guardians of Industrial Control Systems: Which Anomaly Detection Methods Work Best?'
date: 2026-01-05
permalink: /posts/2026/01/guardians-of-ics/
tags:
  - industrial control systems
  - anomaly detection
  - machine learning
  - cyber physical systems
  - cybersecurity
---

Industrial Control Systems (ICS) operate essential services such as water treatment, energy generation, manufacturing, and transportation. Detecting cyberattacks against these systems is therefore extremely important. However, selecting a suitable anomaly detection method is not straightforward, particularly when the system must detect previously unseen attacks.

This blog post presents our recent paper, https://doi.org/10.1049/cps2.70037, published in *IET Cyber-Physical Systems: Theory and Applications*.

# What problem did we investigate?

Machine learning methods for ICS anomaly detection are generally divided into supervised and unsupervised approaches. Supervised models learn from labelled normal and attack data. They can provide accurate predictions when future attacks resemble those represented in the training data. However, obtaining comprehensive labelled attack data from operational industrial systems is difficult.

Unsupervised models learn patterns of normal system behaviour without requiring labelled examples of every attack. This makes them potentially useful for detecting previously unseen attacks, but they may also generate more false alarms.

A major challenge is that studies often evaluate these approaches using different datasets, experimental settings, and performance measures. It is consequently difficult to determine which type of model is more suitable for protecting an ICS.

# What did we do?

We developed a common experimental framework for comparing supervised and unsupervised anomaly detection methods. Using operational data from the Secure Water Treatment (SWaT) testbed, we evaluated six unsupervised methods and five supervised methods.

An important feature of the study was its focus on unknown attacks. This allowed us to investigate how well the models generalised beyond the attacks available during training.

# What did we find?

The results demonstrate an important security trade-off. Supervised models generally achieved higher precision, meaning that their alerts were more likely to correspond to real attacks. However, they also left a greater proportion of attacks undetected.

The unsupervised models achieved better recall and detected more anomalous behaviour, but this came at the cost of additional false alarms. Consequently, neither family of models provides a universal solution.

## Perspective

This work shows why model selection for ICS security should not be based on accuracy alone. In a critical system, the consequences of a missed attack may be substantially different from the consequences of investigating a false alarm. Detection approaches must therefore be selected according to operational requirements, attack assumptions, and the risks associated with different types of errors.

The paper was co-authored with Zequn Wang, Muhammad Azmi Umer, Haibo Zhang, and Naveed ul Hassan.
