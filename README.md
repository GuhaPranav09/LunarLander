# Lunar Lander with Deep Q-Network (DQN)

This project demonstrates the implementation of a **Deep Q-Network (DQN)** to train an autonomous agent to land a lunar module safely using reinforcement learning.

## 🚀 Project Overview

The **Lunar Lander** environment is a dynamic control problem simulated using **Gymnasium**, where the agent learns to fire the lander's thrusters optimally to achieve a smooth landing.

## 📈 Performance

- **Solved in:** 359 episodes
- **Test Results (100 episodes):**
  - Avg Reward: 231.10
  - Std Dev: 36.46
  - Max Reward: 307.81
  - Min Reward: 143.33
  - Success Rate: 83%

## 🔮 Future Work

- Implement **Rainbow DQN**
- Explore **PPO, A3C, SAC** for other action spaces
- Use **Optuna** for hyperparameter tuning
- Add harder environmental challenges (e.g., wind, gravity)
- Explore **multi-agent** scenarios

## 📌 Conclusion

This project showcases the strength of Deep Q-Networks in dynamic control environments. By combining experience replay, target networks, and neural approximators, the agent successfully learns to master the Lunar Lander environment.
