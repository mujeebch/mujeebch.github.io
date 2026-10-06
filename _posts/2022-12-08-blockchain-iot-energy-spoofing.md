---
title: 'When IoT Devices Lie About Their Energy: Attacks and Blockchain-Based Countermeasures'
date: 2022-12-08
permalink: /posts/2022/12/blockchain-iot-energy-spoofing/
tags:
  - Internet of Things
  - blockchain
  - energy spoofing
  - malicious IoT devices
  - distributed trust
  - IoT security
  - smart homes
  - Industry 4.0
  - cybersecurity
---

Internet of Things (IoT) deployments often contain battery-powered and resource-constrained devices. Information about a device's remaining energy may influence routing, task allocation, network membership, and other operational decisions.

But what happens when a malicious device lies about its energy level?

This blog post discusses our paper, *Energy Level Spoofing Attacks and Countermeasures in Blockchain-Enabled IoT* https://doi.org/10.1109/GLOBECOM48099.2022.10001609, presented at the 2022 IEEE Global Communications Conference.

# Why do IoT devices report their energy levels?

IoT systems are used in smart homes, remote sensing, industrial automation, healthcare, environmental monitoring, and other distributed applications.

Many participating devices have limited battery capacity. The system may therefore use reported energy information to decide:

- whether a device should be admitted to the network;
- which device should perform a particular task;
- how communication routes should be constructed;
- whether a node is capable of forwarding information;
- when a device should enter a low-power state; and
- how workload should be distributed across the network.

These decisions assume that participating devices report their energy levels honestly.

# What is an energy-level spoofing attack?

In an energy-level spoofing attack, a malicious IoT device reports a false energy state.

A device might claim to have more energy than it actually possesses to gain admission to a network or obtain a strategically important role. It might also report less energy to avoid work while continuing to benefit from the services provided by other nodes.

False energy reports can influence routing, resource allocation, network lifetime, and the reliability of distributed decisions.

The consequences may extend beyond inefficient energy use. A malicious node that obtains a trusted position could drop, delay, inspect, or manipulate messages passing through it.

# Which attack scenarios did we consider?

We considered energy spoofing at different stages of IoT participation.

The first scenario concerns a device joining the network. A malicious device may falsify its energy level during the admission process to appear eligible for participation.

The second scenario concerns a device that is already part of the network. It may continue to submit false energy information to influence later decisions or avoid responsibilities.

These scenarios show that energy information must be protected throughout the device lifecycle rather than checked only when a device first connects.

# Why use blockchain?

IoT deployments are naturally distributed. A conventional security architecture may depend on a central service to validate and store device information, creating scalability concerns and a potential single point of failure.

Blockchain offers a distributed record in which participants can maintain and verify agreed information. Cryptographic mechanisms, linked records, and distributed consensus can make unauthorised alteration of historical information more difficult.

In our work, an IoT deployment is retrofitted with a blockchain-based mechanism to support trusted handling of device energy information.

The purpose is not to use blockchain simply because it is available. The blockchain provides a shared and tamper-resistant basis for validating reported energy states and coordinating defensive decisions across distributed participants.

# What countermeasure did we develop?

We developed a defence strategy for identifying IoT nodes that provide false information about their energy levels.

The strategy was evaluated under different attack scenarios to examine whether malicious devices could be identified during network admission and subsequent participation.

The results showed that the proposed defence could detect energy spoofing more than 75% of the time under the evaluated conditions.

This demonstrates that distributed trust mechanisms can help protect IoT decisions that depend on device-reported state.

# What are the practical considerations?

Blockchain does not automatically make an IoT system secure. Its use introduces computational, communication, storage, and governance requirements.

These costs are particularly important for devices with limited processing power, memory, bandwidth, and battery capacity.

A practical blockchain-enabled IoT solution must therefore consider:

1. Which devices participate directly in the blockchain.
2. Whether resource-intensive operations should be delegated to gateways or edge nodes.
3. Which consensus mechanism is appropriate.
4. How device identities and cryptographic keys are managed.
5. How unreliable or disconnected devices are handled.
6. Whether the security benefit justifies the additional system overhead.

The wider lesson is that distributed trust mechanisms should be designed around the constraints and security requirements of the target IoT deployment.

## Perspective

Energy reporting may initially appear to be a minor operational detail, but it can determine how an IoT network assigns trust, tasks, and communication responsibilities.

A malicious device can exploit this dependency by presenting a false account of its resources. This is an example of a wider IoT security problem: devices may provide inaccurate information about their identity, location, capabilities, sensor readings, or internal state.

The research demonstrates how blockchain can support distributed verification when multiple parties need to make decisions without relying entirely on a central authority. It also highlights the need to evaluate blockchain solutions against realistic IoT resource constraints.

The paper was co-authored with Ali Hussain Khan, Humza Ikram, Naveed Ul Hassan, and Zartash Afzal Uzmi.

## Research collaboration and consultancy

Our research explores the security of distributed IoT systems and the appropriate use of blockchain for establishing trust between connected devices.

We welcome enquiries from IoT companies, blockchain developers, telecommunications organisations, industrial operators, public-sector bodies, and research institutions interested in:

- blockchain-enabled IoT security;
- malicious and compromised IoT devices;
- device identity and trust management;
- energy spoofing and state falsification;
- secure admission of IoT devices;
- distributed trust and consensus;
- lightweight blockchain mechanisms;
- smart home and Industry 4.0 security;
- secure IoT routing and resource allocation;
- threat modelling for distributed IoT deployments;
- evaluation of blockchain-based security proposals; and
- collaborative research, consultancy, and technical training.

We are particularly interested in helping organisations determine when blockchain is appropriate for an IoT security problem and when a simpler trust mechanism may provide a more efficient solution.

For research collaboration, consultancy, system evaluation, invited talks, advisory activities, or related opportunities, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1109/GLOBECOM48099.2022.10001609. In *Proceedings of the 2022 IEEE Global Communications Conference (GLOBECOM 2022)*. IEEE, 4322–4327. https://doi.org/10.1109/GLOBECOM48099.2022.10001609
