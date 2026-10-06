---
title: 'Protecting Smart Grid Stability Prediction from Adversarial Attacks and Measurement Anomalies'
date: 2025-07-10
permalink: /posts/2025/07/defending-smart-grid-stability-prediction/
tags:
  - smart grids
  - adversarial machine learning
  - stability prediction
  - anomaly detection
  - uncertainty quantification
  - cybersecurity
---

Smart grids increasingly use artificial intelligence to predict system stability and support decisions about electricity distribution. However, an attacker may manipulate the measurements used by these models, causing an apparently accurate prediction system to produce unsafe results.

This blog post discusses our paper, *Fortifying Smart Grid Stability: Defending Against Adversarial Attacks and Measurement Anomalies* https://doi.org/10.1016/j.segan.2025.101799, published in *Sustainable Energy, Grids and Networks*.

# What problem did we investigate?

Machine learning models used for smart grid stability prediction may be affected by deliberately crafted adversarial inputs. They may also encounter abnormal measurements caused by faulty sensors or communication errors.

These situations can be difficult to distinguish from genuine grid behaviour. A security mechanism must therefore detect both intentional manipulation and non-malicious measurement anomalies without creating excessive disruption.

# What did we propose?

We developed a security framework consisting of two independent detection approaches.

The first uses a Gated Recurrent Unit, or GRU, trained with adversarial examples. It learns to distinguish normal grid behaviour from anomalous inputs associated with adversarial manipulation.

The second uses a Bayesian Long Short-Term Memory model and uncertainty quantification. It combines Predictive Entropy and Mutual Information through Joint Entropy and Mutual Information, referred to as JEM. This enables the model to identify inputs for which its predictions are unusually uncertain.

# Which attacks were considered?

The framework considers white-box and query-based grey-box attacks, including GAN-GRID. We also developed a modified form of GAN-GRID to represent targeted adversarial scenarios more realistically.

The evaluation used the Electrical Grid Stability Simulated Dataset and included both adversarial behaviour and measurement anomalies.

# What did we find?

The GRU-based system achieved accuracy of up to 0.984 when detecting adversarial behaviour. The uncertainty-based system achieved accuracy of 0.994 against the modified GAN-GRID attacks.

These findings demonstrate that adversarial training and uncertainty quantification offer complementary ways of protecting stability prediction models.

## Perspective

An AI model can produce accurate predictions under ordinary conditions while remaining vulnerable to carefully manipulated inputs. Accuracy on clean test data is therefore not sufficient evidence that a model is ready for deployment in critical infrastructure.

The combination of adversarial detection and uncertainty estimation provides a more complete view of whether a smart grid prediction should be trusted.

The paper was co-authored with Emad Efatinasab, Nahal Azadi, Gian Antonio Susto, and Mirco Rampazzo. The supporting implementation is available in the associated [open-source repository](https://github.com/emadef1/Fortifying-Stability-Prediction-).

## Reference

https://doi.org/10.1016/j.segan.2025.101799. *Sustainable Energy, Grids and Networks* 43 (2025), Article 101799. https://doi.org/10.1016/j.segan.2025.101799
