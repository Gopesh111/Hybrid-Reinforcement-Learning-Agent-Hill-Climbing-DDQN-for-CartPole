# Hybrid Reinforcement Learning Agent  
## Hill Climbing + Double Deep Q-Network (DDQN) for CartPole

This project implements a **hybrid reinforcement learning framework** that combines **Hill Climbing (HC)** with **Double Deep Q-Network (DDQN)** to solve the **CartPole-v1** control problem.

The goal of this project is to improve **training stability and convergence speed** by leveraging the strengths of both **policy-based optimization** and **value-based deep reinforcement learning**.

---

## Problem Statement

Traditional reinforcement learning approaches often suffer from:
- Slow convergence
- High variance during early training
- Instability in value-based methods

While **Hill Climbing** can quickly discover reasonable policies, it lacks long-term learning capability.
On the other hand, **DDQN** provides stable learning but requires significant exploration and warm-up time.

This project combines both approaches to build a **more efficient and stable learning agent**.

---

## Project Objective

- Design a hybrid RL agent using Hill Climbing and DDQN
- Improve convergence speed compared to standalone DDQN
- Stabilize training using replay memory and target networks
- Evaluate performance on the CartPole-v1 environment

---

## Key Contributions

- Hybrid RL framework combining **policy optimization + deep Q-learning**
- Replay memory prefilled using Hill Climbing-generated policies
- Stable DDQN training with target network updates
- Real-time visualization and performance analysis

---

## System Workflow

CartPole Environment
↓
Hill Climbing Policy Search
↓
Replay Memory Prefill
↓
DDQN Training
↓
Target Network Updates
↓
Optimized Control Policy

---

## Methodology

### 1. Hill Climbing Policy Optimization
- Initialized random policy parameters
- Iteratively perturbed parameters to maximize episode reward
- Selected high-performing policies
- Used these policies to generate experience samples

### 2. Replay Memory Prefill
- Hill Climbing-generated transitions were stored in replay memory
- Reduced random exploration phase
- Accelerated DDQN convergence during early training

### 3. Double Deep Q-Network (DDQN)
- Implemented Q-networks using **PyTorch**
- Used separate:
  - Online network
  - Target network
- Applied periodic target network updates for stability

### 4. Exploration Strategy
- Implemented **epsilon-greedy exploration**
- Gradually decayed epsilon over training episodes
- Balanced exploration and exploitation

---

## Environment & Simulation

- Used **OpenAI Gym (CartPole-v1)** for environment simulation
- Live agent rendering implemented using **Pygame**
- Training metrics visualized using **Matplotlib**

---

## Results & Performance

- Faster convergence compared to standalone DDQN
- Improved average reward across training episodes
- More stable learning behavior
- Reduced variance in early-stage training

> **Observation:** Prefilling replay memory with Hill Climbing policies significantly improves early learning efficiency.

---

## Tech Stack

**Programming Language**
- Python

**Reinforcement Learning**
- OpenAI Gym
- PyTorch

**Numerical & Visualization**
- NumPy
- Matplotlib
- Pygame

---


