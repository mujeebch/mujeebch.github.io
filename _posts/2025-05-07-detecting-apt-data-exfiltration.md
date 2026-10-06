---
title: 'Detecting Advanced Persistent Threat Data Exfiltration During Network Transfer'
date: 2025-05-07
permalink: /posts/2025/05/detecting-apt-data-exfiltration/
tags:
  - advanced persistent threats
  - data exfiltration
  - deep learning
  - network security
  - intrusion detection
  - cybersecurity
---

Advanced Persistent Threats, commonly known as APTs, can remain hidden inside a compromised organisation for extended periods. Once established, an attacker may gradually transfer sensitive information while attempting to make the malicious traffic appear normal.

This blog post discusses our paper, *Detecting Advanced Persistent Threat Exfiltration with Ensemble Deep Learning Tree Models and Novel Detection Metrics* https://doi.org/10.1109/ACCESS.2025.3567772, published in *IEEE Access*.

# What problem did we investigate?

Many APT detection methods concentrate on preventing entry or identifying the early stages of an attack. However, preventive measures may fail, and an attacker may already be operating inside the target environment.

We therefore considered a different starting point: assume that the initial compromise has not been detected and that the attacker is attempting to exfiltrate data.

Detecting this activity is difficult because the attacker can use command-and-control channels, divide information into small transfers, or combine different techniques to avoid conventional network thresholds.

# What did we propose?

We examined three data-exfiltration traffic environments:

1. Exfiltration through command-and-control channels.
2. Exfiltration using transfer-size limitations.
3. Exfiltration combining both techniques.

We introduced two network-monitoring metrics: Package Transfer Rate and Byte Transfer Rate. These metrics describe the frequency of packet transfers and the volume of information transferred during network communication.

The metrics were used to train EDXGB, an ensemble deep learning tree model designed to distinguish APT exfiltration traffic from legitimate network activity.

# How was the method evaluated?

We evaluated the approach using two public datasets and constructed realistic traffic environments representing the three exfiltration conditions. EDXGB was also compared with six baseline methods.

The results showed that the proposed method could detect APT data exfiltration across different traffic environments. This indicates that continuous monitoring during data transfer can complement security controls that focus primarily on preventing the initial compromise.

## Perspective

One of the important assumptions in this work is that the attacker may already be inside the network. This reflects the reality that no preventive control is perfect.

Monitoring transfer behaviour gives defenders another opportunity to identify an attack before sensitive information leaves the organisation. The Package Transfer Rate and Byte Transfer Rate metrics also provide interpretable indicators of potentially suspicious activity.

The paper was co-authored with Xiaojuan Cai, Haibo Zhang, and Hiroshi Koide. The implementation is available in the associated https://github.com/cxjuan/EDXGB-for-APT.

## Reference

https://doi.org/10.1109/ACCESS.2025.3567772. *IEEE Access* 13 (2025), 81803–81822. https://doi.org/10.1109/ACCESS.2025.3567772
