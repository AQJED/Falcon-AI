# 🦅 Falcon AI (Reinforcement Learning for Aerial Combat)

Falcon AI is an ongoing reinforcement learning research project that I've been developing as a solo engineer, focused on training autonomous fighter jets to perform intelligent aerial combat maneuvers in a simulated 2D dogfight environment.

This project leverages the power of multi-agent reinforcement learning (MARL) to create realistic air-to-air engagements using Python-based tools — with a future goal of integrating into military simulation middleware (e.g., DIS/CIGI systems).

---

## ✈️ Overview

The goal is to train an RL agent (a jet) to:
- Detect enemy positioning
- Maneuver strategically
- Engage in cannon-based dogfights
- Learn evasion and attack behavior through self-play

---

## 🧠 Core Technologies

| Component             | Tool/Library                | Purpose                                   |
|----------------------|-----------------------------|-------------------------------------------|
| 🛠️ Environment       | [PyFlyt](https://github.com/TAI-Jet/PyFlyt) + [PettingZoo](https://www.pettingzoo.ml/) | Multi-agent 2D jet simulation             |
| 🎓 RL Framework       | [Stable-Baselines3](https://github.com/DLR-RM/stable-baselines3) | PPO-based agent training                  |
| 🔬 Backend            | [PyTorch](https://pytorch.org/) | Neural network and RL algorithm backend  |
| 🖥️ Visualization      | PyBullet (via PyFlyt)        | Basic visual debugging and rendering       |
| 🔄 Model Export       | TorchScript / ONNX (planned) | Future deployment into C++ simulation     |

---

## 📊 Agent Observations

Each agent receives:
- Own aircraft position, velocity, heading
- Relative position and heading of enemy
- Ammo status, health status
- Proximity to combat zone boundaries

---

## 🎮 Action Space

Agent can perform:
- Turn left / Turn right
- Throttle up / Throttle down
- Fire weapon (cannon-based)
- Optional: Flare, dive, or climb (future features)

---

## 🏆 Reward Design

| Condition                         | Reward |
|----------------------------------|--------|
| Hitting opponent                 | +100   |
| Getting hit                      | -100   |
| Staying engaged (near enemy)     | +1     |
| Going out of bounds              | -10    |
| Evasion success                  | +0.5   |

---

## 📅 Project Milestones

- ✅ Phase 1: Environment setup with PyFlyt + PettingZoo  
- ✅ Phase 2: Define observations, actions, reward shaping  
- 🚧 Phase 3: Train RL agent with PPO using Stable-Baselines3  
- 🔜 Phase 4: Add human-pilot test mode  
- 🔜 Phase 5: Export model and connect to DIS/CIGI middleware


---

## 🤖 Training the Agent (Coming Soon)

Training pipeline using Stable-Baselines3's PPO will be provided soon.

---

## 📈 Future Work

- [ ] Add self-play loop with model saving
- [ ] Integrate keyboard-based human control
- [ ] Export model to TorchScript or ONNX
- [ ] Deploy RL model into real DIS/CIGI simulation middleware

---

## 📬 Contact

**Adeeb Alqahtani**  
Software Integration Engineer | AI + Simulation  
📫 [www.linkedin.com/in/adalqahtani]

