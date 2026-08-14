# 🎰 Multi-Armed Bandit — Interactive PWA

### A visual reinforcement-learning simulation for understanding exploration vs. exploitation.

[![PWA](https://img.shields.io/badge/App-PWA-5C3EE8)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?logo=javascript&logoColor=black)](#)
[![Reinforcement Learning](https://img.shields.io/badge/Topic-Reinforcement%20Learning-33D6A6)](#)

## 📌 Overview

This project turns the **10-armed bandit problem** into an interactive browser simulation.

Each thumbnail represents an arm with an unknown click probability. On every impression, the policy chooses one thumbnail, receives a binary reward (click or no click), updates its estimates, and decides what to try next.

The goal is to make the exploration–exploitation trade-off visible rather than purely theoretical.

## 🧠 Core Mapping

| Bandit concept | Simulation |
|---|---|
| Arm | Thumbnail variant |
| Pull | Impression shown to a viewer |
| Reward | Click (`1`) or no click (`0`) |
| Q(a) | Estimated click rate |
| Policy | Rule used to select the next thumbnail |

## 🎯 Policies Implemented

The current UI exposes these action-selection policies:

### ε-greedy

With probability ε, explore a random arm; otherwise exploit the arm with the highest estimated reward.

```text
if random() < ε:
    choose a random arm
else:
    choose argmax Q(a)
```

### Greedy

Always selects the arm with the highest current estimated reward. This provides a useful baseline and demonstrates the risk of insufficient exploration.

### UCB1

Uses an upper-confidence-bound bonus so that arms with limited observations receive additional consideration.

```text
UCB(a) = Q(a) + sqrt(2 ln(t) / N(a))
```

where `t` is the total number of impressions and `N(a)` is the number of times arm `a` has been selected.

## 🔄 Simulation Workflow

```text
┌─────────────────────┐
│  10 Thumbnail Arms  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Select an arm using │
│ the chosen policy   │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Observe reward      │
│ click = 1 / no = 0  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Update Q(a), pulls  │
│ and cumulative data │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Repeat / compare    │
└─────────────────────┘
```

## ✨ Features

- Interactive 10-arm bandit environment
- ε-greedy policy with adjustable ε
- Greedy baseline
- UCB1 policy
- Step-by-step simulation
- Continuous run mode
- Adjustable simulation speed
- Estimated reward and pull statistics
- Running click-rate tracking
- Best-thumbnail rate display
- Cumulative performance visualization
- Reveal option for inspecting the hidden reward rates
- Responsive browser UI
- Installable Progressive Web App structure

## 📊 What You Can Explore

Try the same environment with different policies and observe:

```text
Exploration  ←──────────────→  Exploitation

ε = high                         ε = 0
More discovery                   More exploitation
More experimentation             Faster commitment
```

Useful experiments:

1. Start with **ε-greedy, ε = 0.10**.
2. Run the simulation for several hundred impressions.
3. Repeat with **Greedy**.
4. Repeat with **UCB1**.
5. Compare cumulative clicks and estimated rates.
6. Use **Reveal true rates** after an experiment to understand why the policies behaved differently.

## 🛠️ Tech Stack

- HTML5
- CSS3
- JavaScript
- Canvas-based visualization
- Web App Manifest
- Service Worker / PWA APIs

## 📂 Repository Structure

```text
bandit-pwa/
├── README.md
└── bandit-pwa/
    ├── index.html       # Main UI, simulation logic and visualization
    ├── manifest.json    # PWA metadata
    ├── sw.js            # Service worker
    ├── icon-192.png     # PWA icon
    └── icon-512.png     # PWA icon
```

The current repository keeps the web application inside the nested `bandit-pwa/` directory.

## 🚀 Run Locally

Clone the repository:

```bash
git clone https://github.com/Deep-k-coder/bandit-pwa.git
cd bandit-pwa
```

Because this is a PWA, serve the application through a local HTTP server rather than opening `index.html` directly.

For example, if Python is installed:

```bash
cd bandit-pwa
python -m http.server 8000
```

Then open the local server in your browser.

## 📱 PWA Support

The project includes:

- `manifest.json` for application metadata
- 192px and 512px application icons
- `sw.js` service worker
- Mobile-friendly viewport configuration

## 📈 Results & Interpretation

The simulation is designed for **interactive learning**, so results depend on the generated hidden reward rates and the selected policy.

Instead of claiming a fixed accuracy or performance score, use repeated runs to compare:

- Total clicks
- Running click rate
- Estimated arm values
- Pull counts
- Performance relative to the best available arm

## 🚧 Future Improvements

- Add Thompson Sampling
- Add configurable number of arms
- Add configurable reward distributions
- Add regret tracking and a dedicated regret chart
- Add experiment export (CSV/JSON)
- Add persistent experiment history
- Add side-by-side policy comparison mode
- Add automated benchmark runs

## 🎓 Learning Outcomes

This project demonstrates practical understanding of:

- Sequential decision-making
- Exploration vs. exploitation
- Action-value estimation
- ε-greedy action selection
- UCB1
- Reward accumulation
- Online learning
- Interactive data visualization
- Progressive Web App development

## 👨‍💻 Author

**Deep Koshiya**  
AI & ML Developer • Python Developer • Computer Vision • Deep Learning

- GitHub: https://github.com/Deep-k-coder
- LinkedIn: https://www.linkedin.com/in/deepkoshiya/
- Portfolio: https://deep-about.netlify.app

---

⭐ If you find this project useful for learning reinforcement learning, consider starring the repository.
