# 🚀 Crawler Bot Reinforcement Learning

This project implements **Reinforcement Learning algorithms** to train a crawler robot to walk efficiently using two articulated arms.

The agent learns an optimal movement policy using:
- Monte Carlo (MC)
- SARSA (Temporal Difference Learning)
- Q-Learning (TD Bellman)

---

## 🧠 Problem Overview

The crawler is modeled as a **state-space problem** where:

- **State = (angle1, angle2)**
  - `angle1`: angle of the top arm
  - `angle2`: angle between the two arms

The goal is to learn a policy that **maximizes forward movement** by adjusting these angles efficiently.

---

## ⚙️ Tech Stack

- Python
- OpenCV (for simulation and visualization)
- Reinforcement Learning (Tabular methods)

---

## 🏗️ Project Structure
- ├── CrawlerSimulator.py # GUI + simulation (provided framework) 
- ├── RLearning.py # RL algorithms (implemented)
- ├── README.md


---

## 🎮 Controls (Manual Mode)

| Key | Action |
|-----|--------|
| W   | Decrease angle1 |
| S   | Increase angle1 |
| A   | Increase angle2 |
| D   | Decrease angle2 |
| Q   | Toggle Q-value / State-value visualization |

---

## 🧩 Core Implementation

### ε-Greedy Policy
- With probability **ε** → random action (exploration)
- Otherwise → best known action (exploitation)

---

### Algorithms Implemented

#### 🔹 Monte Carlo (MC)
- Learns from full trajectories
- Updates Q-values using total return

#### 🔹 SARSA (On-policy TD)
- Updates using current state-action and next state-action pair

#### 🔹 Q-Learning (Off-policy TD)
- Updates using maximum future reward

---

## 📊 State & Action Space

- Angle1 range: `[-35, 55]` → 19 states  
- Angle2 range: `[0, 180]` → 37 states  
- Actions per state: **9**

Total Q-table size:
19 x (37 x 9)

---

## 📈 Reward Function

The agent is rewarded based on forward movement:
Reward = Final_X_Position - Initial_X_Position

---

## 🧪 Training Configuration

Key parameters:
- `steps` → number of iterations
- `alpha` → learning rate
- `gamma` → discount factor
- `epsilon` → exploration rate

---

## 📸 Results

- The agent gradually learns efficient crawling behavior
- Q-values converge to optimal actions
- State-value visualization highlights high-reward states

*(i gotta add a ss here)*

---

## 📌 Key Learnings

- Practical implementation of reinforcement learning algorithms
- Understanding exploration vs exploitation trade-offs
- Working with discrete state and action spaces
- Policy learning through iterative updates

---

## 🚧 Future Improvements

- Implement Deep Q-Networks (DQN)
- Extend to continuous action spaces
- Improve reward shaping
- Add performance comparisons between algorithms

---

## 👨‍💻 Author

Mahitha Kalaga
M.S. Computer Science, University of Dayton

---
