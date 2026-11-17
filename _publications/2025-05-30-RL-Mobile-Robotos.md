---
title: "Reinforcement Learning for Robust Control of Individual Wheel Drive Mobile Robots with Passive Articulated Steering for Reverse Maneuvering"
date: "2025-05-30"
authors:
  - "Benedict Bauer"
  - "Manuel Schulz"
  - "Timo Hufnagel"
  - "Dieter Schramm"
  - "Carsten Wittenberg"
venue: "HCII 2025"
doi: "https://doi.org/10.1007/978-3-031-93429-2_8"
paper_url: ""
---

## Abstract

Mobile robots with individual wheel drive and passive articulated steering offer significant advantages in applications such as logistics and agriculture. This vehicle architecture combines maneuverability, energy efficiency and stability, but is a challenge to control due to its non-linear dynamics and complex kinematics, especially in reverse mode. Classical methods are reaching their limits, so data-driven approaches such as reinforcement learning (RL) are becoming increasingly important.

This contribution investigates the control of such robots using a Twin Delayed Deep Deterministic Policy Gradient (TD3) agent augmented by a Recurrent Neural Network (RNN). The TD3 algorithm provides robust solutions for continuous control problems and is extended to model temporal dependencies and the dynamics of the passive articulated joint angle. The aim is to prevent problems such as jackknifing and to develop precise control strategies.

Kinematic models were created for a simulation environment, and a digital twin served as the basis for training the RL agent. Initial tests showed that the approach can keep the articulated joint angle stable within safe limits and avoid jackknifing, even in the presence of disturbances or varying conditions.

The results show the potential of this method for practical use in autonomous robots. Future work should focus on experimental validations, optimization of the reward function and real-time capability of the system to enable industrial applications.

## Additional materials

Here comes additional information about the research.
Link zu vorhandenem Repo

## Figures

![Floribot](/assets/publications/)
