---
title: 'AGRITRUST: Building a Realistic Testbed for Secure and Trustworthy Smart Agriculture'
date: 2023-07-11
permalink: /posts/2023/07/agritrust-trustworthy-smart-agriculture/
tags:
  - smart agriculture
  - agricultural technology
  - AgriTech
  - Internet of Things
  - IoT security
  - LoRaWAN
  - environmental monitoring
  - trustworthy systems
  - cyber physical systems
---

Smart agriculture increasingly relies on Internet of Things (IoT) sensors to monitor soil, weather, crops, and environmental conditions. The resulting data can support decisions about irrigation, fertilisation, crop management, and sustainable use of natural resources.

However, useful agricultural data must also be trustworthy. Farmers and other stakeholders need confidence that the sensors are operating correctly, the communication network is reliable, and the reported measurements have not been lost, corrupted, or manipulated.

This blog post discusses our paper, *AGRITRUST: A Testbed to Enable Trustworthy Smart AgriTech* https://doi.org/10.1145/3597512.3600209, presented at the First International Symposium on Trustworthy Autonomous Systems.

# What problem did we investigate?

Many smart agriculture systems concentrate on collecting and visualising environmental data. Although these capabilities are important, deploying IoT technology in agriculture creates wider questions about security, resilience, reliability, and stakeholder trust.

Agricultural sensors are commonly deployed outdoors and may remain unattended for long periods. They can experience unreliable connectivity, harsh weather conditions, power limitations, hardware faults, and possible cyberattacks.

If a communication gateway becomes unavailable, measurements may be lost. If a sensor produces inaccurate values, an automated decision system may provide inappropriate recommendations. If the integrity of the collected data cannot be established, users may be reluctant to rely on the technology.

Trustworthy smart agriculture must therefore consider the complete data journey, from sensing and local storage to network transmission, processing, and decision-making.

# What is the AGRITRUST testbed?

AGRITRUST is a testbed for studying trustworthy IoT technologies in agriculture and environmental monitoring.

A central component of the testbed is the **Squirrel Box**, a robust outdoor sensing device designed to collect soil and environmental information. The device can monitor:

- soil temperature;
- soil moisture;
- soil pH;
- nitrogen, phosphorus, and potassium levels;
- ambient temperature; and
- other environmental conditions.

The measurements are communicated using Long Range Wide Area Network technology, commonly known as LoRaWAN. LoRaWAN is suitable for many agricultural environments because it can support long-range communication while maintaining relatively low energy consumption.

The device also supports local data storage. This is important because measurements can be retained when access to the LoRaWAN gateway is temporarily interrupted.

# Why is trust important in smart agriculture?

A smart agriculture system may be technically functional without necessarily being trustworthy. Trust depends on more than whether the device can collect a measurement.

Stakeholders may reasonably ask:

1. Is the sensor producing accurate readings?
2. Can the device continue operating when network connectivity is unavailable?
3. Will data be lost during a gateway outage?
4. Can an attacker alter sensor measurements or transmitted information?
5. How can users assess the reliability of the system's recommendations?
6. Who is responsible when inaccurate data contributes to a poor agricultural decision?

AGRITRUST provides an experimental environment in which such questions can be investigated systematically.

# Which trust properties did we consider?

The work discusses two trust-focused projects.

The first examines **system resilience and reliability**, particularly when a LoRaWAN gateway becomes unavailable. An agricultural monitoring platform should tolerate temporary communication failures without permanently losing valuable environmental data.

The second examines **data accuracy and integrity**. Even when data reaches the platform, users need assurance that the values accurately represent conditions in the physical environment and have not been improperly modified.

These two concerns illustrate why trust in smart agriculture has both technical and human dimensions. Secure communication is important, but it must be accompanied by reliable sensing, resilient operation, and credible evidence about data quality.

# Why use a testbed?

Security and reliability mechanisms are often evaluated using simulated conditions. Simulations support repeatable experiments, but they may not capture the practical challenges associated with outdoor sensor deployments.

A physical testbed enables researchers to study issues such as:

- intermittent wireless communication;
- changing environmental conditions;
- battery and energy limitations;
- sensor degradation;
- missing or inconsistent measurements;
- local data recovery;
- malicious data manipulation; and
- interactions between technical performance and stakeholder trust.

AGRITRUST therefore creates a bridge between theoretical security research and the realities of deploying IoT systems in agricultural environments.

## Perspective

The main contribution of AGRITRUST is not simply another environmental sensor. The testbed provides a platform for studying what makes smart agricultural technology dependable, secure, and worthy of stakeholder confidence.

This is particularly important as agriculture becomes more data-driven. Decisions concerning crops, water, energy, fertilisers, and environmental management may increasingly depend on information produced by connected devices. Errors or malicious manipulation in these systems can have economic, operational, and environmental consequences.

A trustworthy smart agriculture platform should therefore combine secure hardware, reliable communication, resilient data management, meaningful security testing, and an understanding of the people and organisations expected to use the technology.

The paper was co-authored with Carl Dickinson, Shishir Nagaraja, and Richard Hyde.

## Research collaboration and consultancy

Our research explores the security, resilience, and trustworthiness of IoT and cyber-physical systems, including technologies used in agriculture, environmental monitoring, and critical infrastructure.

We welcome enquiries from agricultural technology companies, IoT developers, farms, environmental organisations, public-sector bodies, research institutions, and technology investors interested in:

- security testing of smart agriculture systems;
- trustworthy agricultural IoT;
- LoRaWAN security and resilience;
- environmental and soil-monitoring technologies;
- integrity and reliability of sensor data;
- cyber risk assessment for connected agriculture;
- secure edge computing for agricultural applications;
- threat modelling for smart farming platforms;
- design and evaluation of IoT security testbeds;
- assurance of AI-supported agricultural decisions;
- collaborative research and grant development; and
- independent technical consultancy and system evaluation.

We are particularly interested in projects that require experimental evaluation of connected technologies under realistic faults, attacks, communication failures, and environmental conditions.

For research collaboration, technical consultancy, advisory work, invited talks, knowledge exchange, or related opportunities, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1145/3597512.3600209. In *Proceedings of the First International Symposium on Trustworthy Autonomous Systems (TAS '23)*. ACM, Article 22, 13 pages. https://doi.org/10.1145/3597512.3600209
