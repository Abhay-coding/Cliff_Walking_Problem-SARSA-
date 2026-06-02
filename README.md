# 🧠 Cliff Walking using SARSA (Reinforcement Learning)

## 📌 Overview
This project implements the **SARSA (State-Action-Reward-State-Action)** algorithm to solve the **Cliff Walking problem** using OpenAI Gym.

The agent learns to navigate a grid environment while avoiding the cliff and reaching the goal with maximum reward.

---

## 🎯 Objective
- Learn optimal policy using **on-policy learning (SARSA)**
- Balance **exploration vs exploitation (ε-greedy)**
- Avoid cliff penalties and reach the goal efficiently

---

## 🧩 Environment
- **Environment**: `CliffWalking-v1`
- Grid world with:
  - Start (S)
  - Goal (G)
  - Cliff (large negative reward)

---

## ⚙️ Algorithm: SARSA

### 🔁 Workflow
1. Observe current state \( S_t \)
2. Choose action \( A_t \) using ε-greedy policy
3. Take action → get reward \( R_{t+1} \), next state \( S_{t+1} \)
4. Choose next action \( A_{t+1} \)
5. Update Q-value

---

## 🔥 Update Rule

Q(s, a) = Q(s, a) + α [ R + γ Q(s', a') − Q(s, a) ]


Where:
- α → learning rate  
- γ → discount factor  
- ε → exploration probability  

---

## 🎲 Exploration Strategy
- Uses **ε-greedy policy**
- With probability ε → random action (explore)
- With probability (1-ε) → best action (exploit)

---

## 🚀 Features
- On-policy learning (SARSA)
- Handles exploration-exploitation tradeoff
- Step-by-step learning (Temporal Difference)

---

## 📊 Results
- Agent learns to avoid cliff over episodes
- Converges to safer path instead of shortest risky path

---

## ▶️ How to Run

```bash
pip install gym numpy
