---
title: 'Our Cyber-Physical Security Research Cited in Evidence to the UK Parliament'
date: 2022-07-19
permalink: /posts/2022/07/research-cited-uk-parliament-connected-technology/
tags:
  - research impact
  - UK Parliament
  - connected technology
  - Internet of Things
  - cyber physical systems
  - industrial control systems
  - sensor security
  - anomaly detection
  - critical infrastructure
  - cybersecurity policy
---

Two of our research papers on industrial control system security and sensor attack detection were cited in written evidence submitted to a UK Parliament inquiry into smart and connected technologies.

The evidence, titled [*Connected tech: smart or sinister? Written evidence submitted by REPHRAIN*](https://committees.parliament.uk/writtenevidence/109488/pdf/), was submitted to the House of Commons inquiry examining the opportunities, risks, security, privacy, safety, and societal implications of increasingly prevalent connected devices.

I was also one of the researchers who contributed to the preparation of the evidence.

# The parliamentary inquiry

Smart and connected technologies are now used across homes, workplaces, cities, healthcare, transport, energy, agriculture, and critical infrastructure. Although these technologies create substantial benefits, their growing adoption also creates new cybersecurity, privacy, safety, maintenance, and governance challenges.

The written evidence was submitted by REPHRAIN, the National Research Centre on Privacy, Harm Reduction and Adversarial Influence Online. It brought together interdisciplinary expertise concerning smart and connected technologies, online harms, security, privacy, usability, responsible innovation, and the needs of vulnerable users.

The submission considered several important policy questions, including:

- the benefits and risks of smart and connected technologies;
- groups that may particularly benefit from or be vulnerable to these systems;
- incentives for safe, secure, environmentally responsible, and user-friendly design;
- short-term and long-term cybersecurity threats;
- digital literacy and consumer protection;
- international collaboration and technology standards; and
- whether existing legal and regulatory frameworks adequately address connected technologies.

# Cyber-physical systems create physical safety risks

An important message in the evidence is that connected technologies can affect more than information security and personal data. Cyberattacks against cyber-physical systems may also create consequences in the physical world.

Connected sensors, controllers, and actuators are used in industrial plants, energy systems, healthcare devices, transportation, smart homes, and other safety-relevant environments. Manipulation of these components may affect equipment, services, property, the environment, or human safety.

The evidence therefore recommends that inputs to sensors and computing devices should be validated at both the software and hardware levels.

# Research on real-time industrial anomaly detection

The first cited paper is *Challenges in Machine Learning Based Approaches for Real-Time Anomaly Detection in Industrial Control Systems* https://doi.org/10.1145/3384941.3409588.

Machine learning is increasingly used to detect anomalous behaviour in water treatment plants, electrical grids, manufacturing systems, and other critical infrastructure. However, a detector that performs well on a historical dataset may not necessarily operate effectively in a live industrial environment.

The paper examines practical challenges that must be addressed before machine-learning-based anomaly detectors can be deployed confidently in operational industrial control systems. These include real-time performance, changing process conditions, model maintenance, false alarms, attack coverage, and the difference between offline evaluation and deployment on a live physical plant.

This research supports the wider policy argument that connected technologies require evidence-based security evaluation. Security should be assessed under realistic operational conditions rather than inferred only from laboratory accuracy or benchmark results.

# Hardware fingerprints for protecting sensor measurements

The second cited paper is *NoiSense Print: Detecting Data Integrity Attacks on Sensor Measurements Using Hardware-Based Fingerprints* https://doi.org/10.1145/3410447.

The research investigates whether microscopic hardware variations and sensor noise can be used to identify physical sensors and detect attacks against their measurements.

NoiSense uses noise patterns associated with hardware imperfections to create sensor fingerprints. NoisePrint extends this idea by combining sensor and physical process noise. The study also proposes a challenge-response mechanism for exposing more powerful cyberattacks, including replay attacks.

The experimental results showed that sensor noise could uniquely identify devices with accuracy reaching 97% under the evaluated conditions. The work demonstrates how physical and hardware characteristics can provide an additional security layer alongside software and network-based protections.

# From research findings to public policy

The inclusion of these papers in parliamentary evidence illustrates how experimental cybersecurity research can contribute to wider discussions about public policy and responsible technology.

The two papers address complementary challenges:

1. **How can machine-learning-based anomaly detection be evaluated realistically before it is trusted in operational industrial systems?**
2. **How can hardware and physical signal characteristics help validate sensors and detect manipulated measurements?**

Together, they support a broader policy position: smart and connected technologies should be evaluated as complete cyber-physical systems. Security assessment must consider software, communication networks, hardware, sensors, physical processes, users, and the consequences of failure or malicious manipulation.

The written evidence subsequently formed part of the evidence base associated with the House of Commons inquiry *Connected tech: smart or sinister?* The Committee published its final report on 7 August 2023.

## Perspective

It is encouraging to see our work cited beyond the academic literature and used within a national policy discussion.

The transition from research to impact is not limited to developing a new algorithm or reporting improved detection accuracy. Research can also help policymakers understand where existing assumptions fail, which risks deserve greater attention, and what evidence should be required before connected technologies are deployed in safety-relevant environments.

Our work on industrial anomaly detection and hardware-based sensor fingerprints contributes to this discussion by showing that cybersecurity evaluation must be realistic, adversarial, and grounded in the behaviour of physical systems.

The machine learning paper was co-authored with Gauthama Raman M. R. and Aditya P. Mathur. The NoiSense Print paper was co-authored with Aditya P. Mathur and Martín Ochoa.

## Research collaboration and consultancy

Our research explores the security and assurance of connected technologies, industrial control systems, critical infrastructure, IoT devices, sensors, and cyber-physical systems.

We welcome enquiries from government bodies, policymakers, critical-infrastructure operators, engineering organisations, IoT developers, cybersecurity companies, and research institutions interested in:

- cybersecurity policy for smart and connected technologies;
- evidence-based evaluation of industrial cybersecurity systems;
- machine learning for industrial anomaly detection;
- security and assurance of AI-based detection tools;
- sensor authentication and hardware fingerprinting;
- data integrity and false-data injection attacks;
- cyber-physical risk and safety assessment;
- security of industrial control systems and critical infrastructure;
- realistic cybersecurity testbeds and evaluation methodologies;
- independent review of connected-device security;
- research evidence for policy and regulatory development; and
- collaborative research, consultancy, training, and knowledge exchange.

For research collaboration, policy engagement, technical consultancy, advisory activities, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Parliamentary evidence

[Connected tech: smart or sinister? Written evidence submitted by REPHRAIN](https://committees.parliament.uk/writtenevidence/109488/pdf/), reference TEC0043, UK Parliament.

## References

https://doi.org/10.1145/3384941.3409588. In *Proceedings of the 6th ACM Cyber-Physical System Security Workshop*. ACM, 23–29.

https://doi.org/10.1145/3410447. *ACM Transactions on Privacy and Security* 24, 1, Article 2, 35 pages.

[3] REPHRAIN. 2022. [Connected tech: smart or sinister? Written evidence submitted to the UK Parliament](https://committees.parliament.uk/writtenevidence/109488/pdf/). Written evidence TEC0043.
