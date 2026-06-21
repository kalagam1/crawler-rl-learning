# 🎮 Crawler Bot Reinforcement Learning

A reinforcement learning project focused on training a simulated crawler agent to optimize forward movement through **trial-and-error policy learning**. This project implements and compares **Monte Carlo**, **SARSA**, and **Q-Learning** approaches for controlling a two-joint crawler bot in a discretized state space.

The goal of the project is to learn movement policies that improve the crawler’s displacement over time by updating joint angles based on observed rewards and state transitions.

---

## 🚀 Project Overview

This project explores how reinforcement learning can be applied to robotic movement optimization in a simulated environment. The crawler’s behavior is modeled as a sequential decision-making problem, where each state represents a pair of joint angles and each action modifies the crawler’s configuration to maximize forward progress.

To solve this problem, I implemented three classic reinforcement learning methods:

* **Monte Carlo Learning**
* **SARSA (Temporal Difference Learning)**
* **Q-Learning**

Each algorithm updates the crawler’s policy based on reward signals tied to forward displacement, enabling the agent to gradually improve its movement strategy over repeated episodes.

---

## 🧠 Key Concepts Implemented

* **State-space modeling** using crawler joint angles
* **Action-space design** with 9 possible angle update combinations
* **ε-greedy exploration** for balancing exploration vs. exploitation
* **Q-value learning and policy updates**
* **Monte Carlo return estimation**
* **SARSA temporal-difference updates**
* **Q-Learning with Bellman optimality updates**
* **Policy improvement through repeated training episodes**

---

## ⚙️ Environment Design

The crawler agent operates in a discretized environment defined by two joint angles:

* **Angle 1 range:** -35° to 55°
* **Angle 2 range:** 0° to 180°
* **Step size:** 5° increments

This creates a structured state space where each state corresponds to a unique crawler posture. At every step, the agent selects one of **9 possible joint-action combinations**, adjusting the two angles to improve movement performance.

### Action Space

Each action updates the crawler’s two joint angles using one of the following combinations:

* (-1, -1)
* (-1, 0)
* (-1, 1)
* (0, -1)
* (0, 0)
* (0, 1)
* (1, -1)
* (1, 0)
* (1, 1)

The reward function is based on **forward displacement**, encouraging the crawler to discover movement patterns that maximize progress.

---

## 🛠️ Algorithms Implemented

### 1. Monte Carlo Learning

Implemented an episodic Monte Carlo approach that estimates action values by averaging returns observed across full trajectories. This method updates the value of state-action pairs based on cumulative reward over an episode.

### 2. SARSA (TD Learning)

Implemented on-policy temporal-difference learning using the **SARSA** update rule. The crawler updates its Q-values using the current state, chosen action, reward, next state, and next chosen action.

### 3. Q-Learning

Implemented off-policy **Q-Learning** using the Bellman optimality principle. This approach updates Q-values based on the maximum estimated future reward, helping the crawler learn an increasingly optimal movement policy.

---

## 📊 What the Project Demonstrates

* Hands-on implementation of **core reinforcement learning algorithms**
* Practical understanding of **state-action value estimation**
* Experience designing **reward-driven learning systems**
* Ability to model robotic control as a **sequential optimization problem**
* Comparative experimentation across multiple RL approaches

---

## 🧰 Tech Stack

* **Python**
* **NumPy**
* Reinforcement Learning fundamentals
* Monte Carlo methods
* SARSA
* Q-Learning

---

## 📌 Highlights

* Built a reinforcement learning framework for a simulated crawler bot using **Monte Carlo, SARSA, and Q-Learning**
* Modeled a discretized **19 × 37 state space** with **9 action combinations per state**
* Implemented **ε-greedy action selection** and Q-value updates for iterative policy improvement
* Optimized crawler movement using **reward signals based on forward displacement**
* Explored differences between episodic return estimation, on-policy TD learning, and off-policy Q-Learning

---

## 📚 Learning Outcomes

This project strengthened my understanding of:

* reinforcement learning fundamentals
* reward engineering and exploration strategies
* value-function updates and policy improvement
* how agent behavior evolves under different learning paradigms
* building ML systems from algorithmic foundations rather than only using high-level libraries

---

## 🔍 Future Improvements

Potential next steps for extending this project include:

* visualizing policy convergence over time
* plotting reward progression across training episodes
* comparing algorithm performance quantitatively
* tuning hyperparameters such as learning rate, discount factor, and epsilon
* experimenting with function approximation or deep reinforcement learning methods

---

## 👩‍💻 Author

**Mahitha Kalaga**
M.S. Computer Science, University of Dayton
Interests: Security Engineering, Detection Engineering, Applied Machine Learning, Secure Systems
