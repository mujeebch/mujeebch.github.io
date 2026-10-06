---
title: 'Scanning the Cycle: Using Execution Timing to Authenticate Industrial PLCs'
date: 2021-06-04
permalink: /posts/2021/06/scanning-cycle-plc-authentication/
tags:
  - programmable logic controllers
  - PLC authentication
  - industrial control systems
  - timing fingerprints
  - scan cycle
  - replay attacks
  - critical infrastructure
  - cybersecurity
---

Programmable Logic Controllers, commonly known as PLCs, are central to modern industrial control systems. They receive measurements from sensors, execute control logic, and issue commands to actuators controlling physical processes.

If an attacker compromises a PLC or impersonates it on the industrial network, malicious commands may appear to originate from a legitimate controller.

This blog post discusses our paper, *Scanning the Cycle: Timing-Based Authentication on PLCs* https://doi.org/10.1145/3433210.3453102, presented at the 2021 ACM Asia Conference on Computer and Communications Security.

# Why is PLC authentication important?

Industrial environments use PLCs to control processes in water treatment, electricity generation, manufacturing, transportation, and other critical sectors.

Many industrial communication protocols were designed for reliability and predictable operation rather than strong authentication and message integrity. An attacker who gains access to the control network may therefore attempt to impersonate a PLC or inject spoofed commands.

Conventional network intrusion detection may not identify such an attack if the adversary carefully reproduces the expected communication pattern.

We investigated whether properties of the PLC's execution behaviour could provide an additional means of authentication.

# What is a PLC scan cycle?

A PLC normally performs a repeated sequence of operations:

1. It reads its inputs.
2. It executes the programmed control logic.
3. It updates its outputs.
4. It performs communication and diagnostic tasks.
5. It begins the next execution cycle.

This repeated process is known as the scan cycle.

The duration and timing characteristics of the scan cycle are influenced by the controller, control logic, input and output activity, communications, and implementation environment.

Our central observation was that this timing behaviour can act as a fingerprint of the PLC.

# What did we propose?

We proposed a non-invasive authentication method that estimates PLC scan-cycle timing by passively observing network request and response messages.

The technique does not require substantial modification to the PLC hardware or control program. Instead, it extracts timing characteristics from the controller's normal network communication.

If an attacker attempts to impersonate a PLC, the timing pattern of the spoofed messages may deviate from the established fingerprint. The monitoring system can use this deviation as evidence of possible impersonation.

# How are replay attacks addressed?

An attacker might attempt to evade timing-based authentication by recording and replaying legitimate PLC messages.

To address this threat, we proposed **PLC Watermarking**. The method models the relationship between the PLC's scan cycle, control logic, inputs, outputs, and request-response messages.

The watermark enables the defender to determine whether observed communication corresponds to the current execution of the controller rather than simply reproducing previously captured traffic.

# How was the method evaluated?

We evaluated the technique using two operational cyber-physical testbeds:

- the Secure Water Treatment testbed, known as SWaT; and
- the Electric Power and Intelligent Control testbed, known as EPIC.

The experiments showed that PLCs could be distinguished through their scan-cycle timing characteristics.

Using two different testbed environments also helped demonstrate that timing-based authentication can be considered across different industrial processes rather than being restricted to one particular application.

## Perspective

The interesting aspect of this work is that authentication is derived from how a controller behaves rather than relying only on a stored credential.

Timing characteristics are not a replacement for cryptographic authentication. However, they can provide an additional and independent source of evidence, particularly in legacy industrial environments where replacing devices or protocols may be difficult.

The work also demonstrates how characteristics usually regarded as implementation details can become useful security signals.

The paper was co-authored with Martin Ochoa, Jianying Zhou, and Aditya Mathur.

## Research collaboration and consultancy

Our research examines the security of programmable logic controllers, industrial networks, and cyber-physical infrastructure.

We welcome enquiries relating to:

- PLC authentication and identification;
- timing-based device fingerprinting;
- industrial protocol security;
- PLC impersonation and command spoofing;
- replay attack detection;
- process-aware intrusion detection;
- SCADA and industrial control system security;
- security monitoring for legacy industrial equipment;
- cyber-physical security testbeds; and
- experimental evaluation of industrial cybersecurity controls.

We can support industrial operators, engineering organisations, cybersecurity vendors, researchers, and public-sector bodies through collaborative research, technical consultancy, threat modelling, security evaluation, training, and knowledge exchange.

For consultancy, research collaboration, advisory activities, or invited talks, contact **Dr Mujeeb Ahmed**, Senior Lecturer in Computing at Newcastle University:

**Email:** mujeeb.ahmed@newcastle.ac.uk

## Reference

https://doi.org/10.1145/3433210.3453102. In *Proceedings of the 2021 ACM Asia Conference on Computer and Communications Security*. ACM, 886–900. https://doi.org/10.1145/3433210.3453102
