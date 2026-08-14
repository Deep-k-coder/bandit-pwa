# 🎰 Multi-Armed Bandit Interactive Simulation

An interactive web-based simulation for learning the **Multi-Armed Bandit problem** and understanding the exploration–exploitation trade-off in reinforcement learning.

## 📌 Overview

The Multi-Armed Bandit problem models sequential decision-making under uncertainty. An agent repeatedly selects among actions (arms), observes rewards, and learns which choices are likely to produce higher long-term reward.

This project provides a simple visual environment for experimenting with bandit strategies and observing how different policies behave over time.

## 🧠 Core Concept

```text
Bandit Environment
       ↓
Select an Arm
       ↓
Receive Reward
       ↓
Update Knowledge
       ↓
Choose Next Arm
       ↓
Maximize Reward / Minimize Regret
```

## 🎯 Learning Objectives

- Understand exploration vs. exploitation.
- Compare action-selection strategies.
- Observe cumulative reward and regret.
- Build intuition for sequential decision-making.
- Experiment with reinforcement-learning concepts through an interactive UI.

## ✨ Features

- Interactive bandit simulation
- Visual comparison of action-selection behavior
- Reward-based feedback
- Browser-based interface
- Lightweight front-end implementation

## 🛠️ Tech Stack

- HTML5
- CSS3
- JavaScript
- Progressive Web App (PWA) concepts

## 🚀 Run Locally

Clone the repository:

```bash
git clone https://github.com/Deep-k-coder/bandit-pwa.git
cd bandit-pwa
```

Then open the project in a local browser/server environment. For a more realistic PWA test, serve the directory with a local HTTP server rather than opening files directly.

## 📊 Concepts Demonstrated

```text
Exploration
    +
Exploitation
    ↓
Action Selection
    ↓
Reward Collection
    ↓
Cumulative Reward
    ↓
Regret Analysis
```

## 🔬 Reinforcement Learning Context

The project is a practical visualization of the **n-armed bandit problem**, a foundational reinforcement-learning setting where an agent must make repeated choices without knowing the underlying reward distributions in advance.

## 👨‍💻 Author

**Deep Koshiya**

GitHub: https://github.com/Deep-k-coder

## 🚀 Future Improvements

- Add configurable bandit environments.
- Add more exploration policies such as ε-greedy, UCB, and Thompson Sampling.
- Add reward and regret charts.
- Add experiment export and comparison.
- Improve accessibility and mobile interaction.
